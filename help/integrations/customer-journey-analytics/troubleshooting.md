---
title: Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング
description: Customer Journey AnalyticsのAdobe Advertising データに関する問題のトラブルシューティングと解決方法について説明します。
feature: Integration with Adobe Customer Journey Analytics
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 3ca788a8a15277a105c065087ad9a5fbc9108311
workflow-type: tm+mt
source-wordcount: 627
ht-degree: 0%

---

# Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング

次に、潜在的なデータの問題とその原因を示します。

## 概要レポート

+++ Customer Journey Analytics for Advertising DSPまたはAdvertising Search, Social, &amp; Commerceでは、概要レポートデータは利用できません。

次の点を確認します。

* Adobe AdvertisingからCustomer Journey Analyticsへのフィードが有効になっています。 Adobeのアカウントチームにお問い合わせください。

* Adobe Advertising ディメンション/分類/参照データセットとサマリーデータセットは、Customer Journey Analytics接続に含まれます。

* Adobe Advertisingのディメンションと概要指標は、Customer Journey Analytics データビューに含まれます。

* Customer Journey Analytics Workspaceが正しいデータビューを参照しています。

上記のすべての設定を確認しても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。

+++

+++ 概要レポートデータは、Customer Journey Analytics for Advertiser 1では利用できますが、Advertiser 2では利用できません。

Adobe AdvertisingからCustomer Journey AnalyticsへのフィードがAdvertiser 2に対して有効になっていることを確認します。 Adobeのアカウントチームにお問い合わせください。

広告主に対してフィードが有効になっていても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。

+++

+++ （Search, Social, &amp; Commerce ユーザー）概要レポート データは、Customer Journey Analyticsで1つの[!DNL Google Ads]、[!DNL Meta Ads]、または[!DNL Microsoft Advertising] アカウントで利用できますが、別のアカウントでは利用できません。

Adobe AdvertisingからCustomer Journey Analyticsへのフィードが、特定の広告ネットワークアカウントに対して有効になっていることを確認します。 Adobeのアカウントチームにお問い合わせください。

フィードがアカウントに対して有効になっていても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。

+++

+++ Customer Journey Analytics Workspaceの概要レポートデータは、Advertising DSPまたはAdvertising Search, Social, &amp; Commerceのデータと異なり、一部のキャンペーンおよびキャンペーンエンティティの概要データが見つかりません。

次の点を確認します。

* [!DNL Workspace]とAdobe Advertising レポートの両方で同じ日付範囲を使用しています。

* [!DNL Workspace]とAdobe Advertising レポートに適用されているフィルターとセグメントは、データの違いを引き起こしません。

データの相違が確認できる場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。
.スクリーンショットとスプレッドシートを含めて、食い違いの証拠を示します。Adobe アカウントチームは、必要に応じてデータフィードを過去にさかのぼって修正し、差異を解決できます。

+++

## イベントレベルのレポート

+++ コンバージョンデータ （`Page Views`など）は、CJA Customer Journey Analytics Workspaceのレポートディメンション （`Campaign`など）では使用できません。

以下を検証します。最初に、検証に対する障壁が最も少ない項目を確認します。

* 該当するコンバージョン指標は、web/オンラインイベントで、Adobe Advertisingはディメンションに関連付けることができます。

* 正しいデータビューを使用していること。

* Adobe Advertisingでは、該当するサイトのクリックスルーとビュースルーを追跡しています。<!-- Link to validation instructions in the user guide -->

* 分類データセットのCustomer Journey Analytics接続で、[!DNL Key]および[!DNL Matching Key]設定の値が正しいです：[!DNL Key]: `Tracking Code` （_customername.adLens2.trackingCode）、[!DNL Matching Key]: `Tracking Code` （event._experience.adcloud.conversionDetails.trackingCode）

* [!DNL Adobe Advertising] サービスがAdobe Experience Platform データストリームに追加され、データストリーム用にマッピングされたスキーマが`XDM ExperienceEvent Schema`になり、フィールドグループ `Adobe Advertising Cloud ExperienceEvent Full Extension`がスキーマに追加されます。

* Adobe Advertisingの設定は、WebSDK拡張機能で正しく設定され、公開されます。

上記の設定をすべて確認しても、コンバージョンデータが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。

+++


<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [前提条件](prerequisites.md)
>* [&#x200B; データ収集、データ転送、レポートの設定](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md)。
