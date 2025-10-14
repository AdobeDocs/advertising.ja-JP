---
title: タグに追加  [!DNL Analytics for Advertising]  マクロ  [!DNL Google Campaign Manager 360]  追加
description: 広告タグにマクロを追加する理由  [!DNL Analytics for Advertising]  方法  [!DNL Google Campaign Manager 360]  説明します
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
source-git-commit: aa41ba08ba83bfacbc2541c0f0d90336b3c36305
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# [!DNL Google Campaign Manager 360] Ad タグへの [!DNL Analytics for Advertising] マクロの追加

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

*Advertising DSPにのみ適用*

Advertising DSP広告に [!DNL Google Campaign Manager 360] の広告タグを使用する場合は、[`%p` マクロ &#x200B;](https://support.google.com/campaignmanager/table/6096962) を使用して、ランディングページの URL に [!DNL Analytics for Advertising] のパラメーターを追加します。 パラメーターは、AMO ID （`s_kwcid`）および `ef_id` クエリ文字列パラメーターをランディングページの URL に記録するので、Adobe Advertisingは、広告のクリックデータをAdobe Analyticsに送信できます。

次のタイプの [!DNL Analytics for Advertising] 実装 [!DNL Campaign Manager 360] ディスプレイ広告とビデオ広告にマクロを使用します。

* **Web サイトに実装された [!DNL Adobe] [!DNL Analytics for Advertising] JavaScript コードを持つ広告主**:JavaScript コードは既に AMO ID （`s_kwcid`）とクエリ文字列パラメーター `ef_id` 記録しています。 ただし、サードパーティ cookie がサポートされていない場合に、マクロを使用すると、トラッキングが拡張されて、クリックベースの変換が含まれます。 ベストプラクティスは、JavaScript コードを通じて取得されないクリックスルーのデータをさらに取得するために、次のセクションのマクロを広告タグに追加することです。

>[!NOTE]
>
>JavaScript コードは、cookie が使用可能な状態でのクリックの追跡にのみ使用できるソリューションです。 Cookie が廃止されると、次のマクロの実装が必要になります。

* **Web サイトで [!DNL Analytics for Advertising] JavaScript コードを使用せず、代わりにクリックスルーデータのみの [!DNL Analytics] サーバーサイド転送に依存している広告主** （ビュースルーデータがない）:Adobe Advertisingで購入した広告から発生するオンサイトクリックアクティビティをレポートするには、次のマクロが必要です。

## [!DNL Google Campaign Manager 360] 広告にマクロを追加する

[!DNL Google Campaign Manager 360] 内で、ディスプレイおよびビデオ広告ごとに、ランディングページ URL に次のパラメーターを追加します。`%pamo=!;`

ランディングページ URL は複数の方法で指定できます。 各オプションの説明は、次のサブセクションに含まれています。

次に、サフィックスを使用して書式設定されたランディングページ URL の例を示します。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>&#x200B;>* ランディングページ URL に、一般的ではないハッシュシンボル（#）が含まれる場合は、ハッシュシンボルの前に `amo` パラメーターを配置します。
>* `amo` パラメーターの後に他のパラメーターが含まれていない場合は、その後にパラメーター（例：&amp;a=b）を追加します。 例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 広告主レベルのランディングページ URL サフィックスの設定

1. 詳しくは、[&#x200B; 広告主のプロパティを開く手順 &#x200B;](https://support.google.com/campaignmanager/answer/2829344) を参照してください。
1. [!UICONTROL Landing page URL suffix] の設定で、[!UICONTROL URL suffix] フィールドに `%pamo!;` を含めます。

### キャンペーンレベルのランディングページ URL サフィックスの設定

1. [&#x200B; キャンペーンのプロパティを開く手順 &#x200B;](https://support.google.com/campaignmanager/answer/2838056#set) を参照してください。
1. [!UICONTROL Landing page URL suffix] の設定で、[!UICONTROL URL suffix] フィールドに `%pamo!;` を含めます。

### クリエイティブレベルのランディングページ URL サフィックスの設定

1. クリエイティブプロパティを開きます。
1. [!UICONTROL Click tags] 設定で、クリックタグの [!UICONTROL Landing page] 列に `%pamo!;` を含めます。

## DSP[!DNL Analytics for Advertising] マクロを展開する方法

DSPでは、[!DNL Analytics for Advertising] パラメーター（`amo`）を含む広告を作成すると、`ef_id` マクロと `s_kwcid` マクロがクリック URL に自動的に追加されます。 ベストプラクティスは、DSPでタグを確認して、`ef_id` マクロと `s_kwcid` マクロが存在することを確認することです。

次に、DSPに表示される [!DNL Google Campaign Manager 360] [ins タグ &#x200B;](https://support.google.com/campaignmanager/answer/6080468) の例を示します。

```
<ins class='dcmads' style='display:inline-block;width:160px;height:600px'
data-dcm-placement='N6482.2155306TUBEMOGUL/B23486129.261313631'
data-dcm-rendering-mode='iframe'
data-dcm-https-only
data-dcm-resettable-device-id=''
data-dcm-app-id='' data-dcm-click-tracker='${TM_CLICK_URL}'
data-dcm-param-amo='ef_id=${TM_USER_ID}:${TM_DATETIME}:d&s_kwcid=AC!${TM_AD_ID}!${TM_PLACEMENT_ID}'>
<script src='https://www.googletagservices.com/dcm/dcmads.js'></script>
</ins>
```

ユーザーが広告をクリック [!DNL Google Campaign Manager 360] ると、URL サフィックスに `%pamo` が表示され、`amo` パラメーターの値が URL に動的に挿入されます。

>[!MORELIKETHIS]
>
>* [&#x200B; 概要  [!DNL Analytics for Advertising]](overview.md)
>* [&#x200B; 使用Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Append [!DNL Analytics for Advertising] Macros to [!DNL Flashtalking] Ad タグ &#x200B;](macros-flashtalking.md)
