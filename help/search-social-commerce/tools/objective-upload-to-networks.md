---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッド ポートフォリオの目標を [!DNL Google Ads] および [!DNL Microsoft Advertising]にアップロードする方法を説明します。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
TQID: https://experienceleague.adobe.com/qZwJg4s5MvfUoNBiA-VGhrfKKRt9MjjJOq9jLAdRzi0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b2ff290c2cee19c8acdc8001433189ea9bdbf83f
workflow-type: tm+mt
source-wordcount: 676
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*アカウントと[!DNL Google Ads] アカウントのみを持つ[!DNL Microsoft Advertising]広告主*

*ハイブリッド最適化のみ有効な広告主*

Search, Social, &amp; Commerceでは、広告主アカウントのポートフォリオの目標を[!DNL Google Ads]および[!DNL Microsoft Advertising]にアップロードできるため、ハイブリッド最適化に使用できます。 アップロードされた目標は、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート入札戦略を含むキャンペーンを含むポートフォリオ内の目標のアップロードが自動的にトリガーされます。 Search, Social, &amp; Commerceは、該当する各目的に対して、広告ネットワーク上でコンバージョンを生み出します。 コンバージョンは、EF ID （クリック ID）レベルで、目的のすべての重み付けされたコンバージョン指標を表します。 [!DNL Google Ads] クリックの場合、EF IDは[!DNL Google Ads] `gclid`です。[!DNL Microsoft Advertising] クリックの場合、EF IDは[!DNL Microsoft Advertising] `msclkid`です。 このクリック IDにより、コンバージョンデータを特定のキーワードとクリック時間にマッピングできます。

アップロードされた各コンバージョンの名前は次のとおりです。

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

`<network_ID>`はSearch, Social, &amp; Commerceがアドネットワークに使用する数値ID、`<objective_id>`は数値目標ID、`<network_account_ID>`はアドネットワークアカウントまたはマネージャーアカウントの数値IDです。

[!DNL Google Ads]および[!DNL Microsoft Advertising]へのアップロードは、通常、1日に1時間ごとに実行されます。 大規模なアカウントやカスタム設定を持つ広告主の場合、1日に少なくとも3回はアップロードが発生します。

>[!IMPORTANT]
>
>[!DNL Google Ads]および[!DNL Microsoft Advertising] ユニバーサル イベント トラッキング （UET） タグによってトラッキングされたコンバージョンは、広告ネットワークに再アップロードされません。 目標に含める場合は、広告ネットワークのエディター内のキャンペーン目標にそれらを追加する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**&#x200B;をクリックします。

1. **[!UICONTROL Enable Objective Upload]**&#x200B;の横にあるチェックボックスをオンにします。

1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う[!DNL Google Ads] アカウントを持つ広告主。オプション）広告目的でデータをアップロードするためにEEAおよび英国のユーザーから同意を得た場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**&#x200B;の横にあるチェックボックスをオンにします

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （コンバージョンがマネージャーアカウントレベルで追跡されている場合） [&#x200B; マネージャーアカウントの資格情報](/help/search-social-commerce/admin/manager-accounts.md)を&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;に追加します。

1. `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`という名前の各目的が2日以内に広告ネットワークに表示されることを確認します。

   [!DNL Google Ads] エディターで、[&#x200B; コンバージョンアクション &#x200B;](https://support.google.com/google-ads/answer/11461796)を検索します。 [!DNL Microsoft Advertising] エディターで、[&#x200B; コンバージョン目標](https://help.ads.microsoft.com/#apex/ads/en/56709)を検索します。

   必要に応じて、アップロード日を含めるように日付範囲を更新します。

## 重み付けされた目標の計算方法

広告ネットワークに渡される重み付けされた目標は、[!DNL Google Ads]または[!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET）タグによって追跡されたコンバージョンを除いて、収集されたすべての指標値の合計です。 この値は、広告主のSearch, Social, &amp; Commerce アカウントに設定されたアトリビューション方式を使用して計算されます。

たとえば、目的の目標指標が25の重みの付いたカート追加数であり、アシスト指標には重みが1のGGL_LeadとRevenue、重みが0.5のDownloadsが含まれているとします。

![重み付けされた目標の例](/help/search-social-commerce/assets/objective-example.png "重み付けされた目標の例")

キーワードがポートフォリオに対して次のアクションを生み出したとします。

* 買い物かごに10個追加
* 500 ドルの収益
* 50 ダウンロード
* 5 GGL_Lead

GGL_LeadはGoogle Adsで追跡される指標であるため、計算/アップロードには含まれません。 したがって、重み付けされた目標値は（（10 x 25） + （500 x 1） + （50 x 0.5）） = 775として計算されます。

>[!TIP]
>
>広告ネットワークのレポート内で、Adobe Advertisingの加重売上に関するデータを表示できます。 ベストプラクティスとして、重み付けされた収益を[!DNL Google Ads] 「すべての変換」と比較します。 （convによる。 time）&quot;指標または[!DNL Microsoft Advertising] メトリック &quot;All conv. 「収益」は、O_ACS_OBJ*指標にセグメント化されています。<!--clarify -->

## 目標がない場合のトラブルシューティング

いずれかのポートフォリオの目標（`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`）が広告ネットワークに表示されない場合は、次の点を確認してください。

* （[!DNL Google Ads]） コンバージョンをアカウントレベルまたはマネージャーレベルにアップロードする必要があるかどうかを確認します。 マネージャーレベルでアップロードする必要がある場合：

   * [!DNL Google Ads] マネージャーアカウントの資格情報が&#x200B;**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**&#x200B;に提供されているかどうかを確認します。 必要に応じて、マネージャーアカウントの資格情報を[追加します](/help/search-social-commerce/admin/manager-accounts.md)。

   * 広告ネットワークアカウントに同じメトリック名が既に含まれているかどうかを確認します。 その場合は、適切なマネージャーレベルのプロパティを作成できるように、指標の名前を変更します。

* ポートフォリオの「ハイブリッド」オプションが選択されており、目的に有効な収益があることを確認します。

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [検索、ソーシャル、Commerceで追跡したコンバージョン指標を [!DNL Google Ads]](conversion-metrics-upload-to-google.md)にアップロード
