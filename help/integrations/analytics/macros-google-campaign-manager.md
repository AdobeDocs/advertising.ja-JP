---
title: ' [!DNL Analytics for Advertising]  マクロを [!DNL Google Campaign Manager 360] 広告タグに追加'
description: ' [!DNL Analytics for Advertising] 広告タグに [!DNL Google Campaign Manager 360]  マクロを追加する理由と方法について説明します'
feature: Integration with Adobe Analytics
exl-id: 89cd4e1d-277a-4a43-9c38-ae6641302e09
TQID: https://experienceleague.adobe.com/9qDSGAIk2uelZpEekvKmQMxIMAQeCT8cy55zub-uFv4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 487
ht-degree: 0%

---

# [!DNL Analytics for Advertising]個のマクロを[!DNL Google Campaign Manager 360]個の広告タグに追加

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

*Advertising DSPにのみ適用*

Advertising DSP広告に[!DNL Google Campaign Manager 360]の広告タグを使用する場合は、[!DNL Analytics for Advertising] マクロ [`%p`を使用して、ランディングページ URLに](https://support.google.com/campaignmanager/table/6096962)個のパラメーターを追加します。 パラメーターは、ランディングページ URLのAMO ID （`s_kwcid`）と`ef_id` クエリ文字列パラメーターを記録し、Adobe Advertisingが広告のクリックデータをAdobe Analyticsに送信できるようにします。

次の種類の[!DNL Campaign Manager 360]実装では、[!DNL Analytics for Advertising]件のディスプレイ広告とビデオ広告にマクロを使用します。

* **Web サイトに実装された[!DNL Adobe] [!DNL Analytics for Advertising] JavaScript コードを持つ広告主**: JavaScript コードには、AMO ID （`s_kwcid`）と`ef_id` クエリ文字列パラメーターが既に記録されています。 ただし、マクロを使用すると、サードパーティのCookieがサポートされていない場合に、トラッキングを拡張してクリックベースのコンバージョンを含めることができます。 ベストプラクティスは、次のセクションのマクロを広告タグに追加して、JavaScript コードでキャプチャされないクリックスルーのデータを取り込むことです。

>[!NOTE]
>
>JavaScript コードは、Cookieがまだ利用可能な間のみクリックを追跡するためのソリューションです。 Cookieが廃止されると、次のマクロを実装する必要があります。

* **Web サイトで[!DNL Analytics for Advertising] JavaScript コードを使用せず、代わりに[!DNL Analytics] サーバーサイド転送によるクリックスルー情報の提供のみ** （ビュースルーデータなし）を利用している広告主：Adobe Advertisingを通じて購入した広告からクリック活動を報告するには、次のマクロが必要です。

## [!DNL Google Campaign Manager 360]広告にマクロを追加

[!DNL Google Campaign Manager 360]内で、ディスプレイ広告とビデオ広告のそれぞれのランディングページ URLに次のパラメーターを追加します：`%pamo=!;`

ランディングページのURLは、いくつかの方法で指定できます。 各オプションの手順については、次のサブセクションを参照してください。

次に、接尾辞でフォーマットされたランディングページ URLの例を示します。

```
https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;
```

>[!NOTE]
>
>>* ランディングページのURLにハッシュ記号（#）が含まれている場合は、ハッシュ記号の前に`amo` パラメーターを配置します。
>* `amo` パラメーターの後に他のパラメーターが含まれていない場合は、その後にパラメーター（&amp;a=bなど）を追加します。 例：`https://www.adobe.com/home?someparam1=somevalue1&%pamo=!;&a=b#login`

### 広告主レベルのランディングページ URL サフィックスの設定

1. 広告主のプロパティを開くには、[手順を参照してください](https://support.google.com/campaignmanager/answer/2829344)。
1. [!UICONTROL Landing page URL suffix]設定で、`%pamo!;` フィールドに[!UICONTROL URL suffix]を含めます。

### キャンペーンレベルのランディングページ URL サフィックスの設定

1. キャンペーンのプロパティを開くには、[手順を参照してください](https://support.google.com/campaignmanager/answer/2838056#set)。
1. [!UICONTROL Landing page URL suffix]設定で、`%pamo!;` フィールドに[!UICONTROL URL suffix]を含めます。

### クリエイティブレベルのランディングページ URL サフィックスの設定

1. クリエイティブプロパティを開きます。
1. [!UICONTROL Click tags]設定で、クリックタグの`%pamo!;`列に[!UICONTROL Landing page]を含めます。

## DSPで[!DNL Analytics for Advertising] マクロを展開する方法

DSPで、[!DNL Analytics for Advertising] パラメーター（`amo`）を含む広告を作成すると、`ef_id`および`s_kwcid` マクロが自動的にクリック URLに追加されます。 ベストプラクティスは、DSPでタグを確認して、`ef_id`および`s_kwcid` マクロが存在することを確認することです。

次に、DSPに表示される[!DNL Google Campaign Manager 360] [ins タグ ](https://support.google.com/campaignmanager/answer/6080468)の例を示します。

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

ユーザーが広告をクリックすると、[!DNL Google Campaign Manager 360]はURL サフィックスに`%pamo`を表示し、`amo` パラメーターの値をURLに動的に挿入します。

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [様が使用している [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID
>* [追加 [!DNL Analytics for Advertising]  マクロを [!DNL Flashtalking] 広告タグ ](macros-flashtalking.md)に追加
