---
title: Adobe AdvertisingとCustomer Journey Analyticsを統合するための前提条件
description: Adobe AdvertisingとCustomer Journey Analyticsを統合するための前提条件
feature: Integration with Adobe Customer Journey Analytics
exl-id: 4bd14178-5003-4da6-9034-d070c57f0e9b
TQID: https://experienceleague.adobe.com/I86BXjKORkYZIBn9EqPy3eWPJZi27n5STWcXUtp9gwo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b23e006f-0a29-4f1d-8fd0-77aa56f3d12bid: d3cdead0-685a-4489-9250-4bb709942f66id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: d2b474e24ef2dbf951ea40c42497f6d6d37993ee
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 0%

---

# Adobe AdvertisingとCustomer Journey Analyticsを統合するための前提条件

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*&#x200B;の広告主

* （Customer Journey Analyticsを使用しているが[!DNL Analytics for Advertising]ではない広告主）:

  * [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html) バージョン 2.36以降。

  * [Adobe Experience Platform タグ ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) （バージョン 2.37以降の[[!DNL Web SDK] 拡張機能](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/tags-configuration/install-web-sdk#add-the-web-sdk-extension)を含む）。

* Adobe Customer Journey Analyticsからデータ管理ツールにアクセス

  データセットへの接続を設定し、レポートを設定するには、社内のweb アナリストのサポートが必要です。

* （広告主が[!DNL Analytics for Advertising]）Adobe Experience Platform データモデリングおよび管理テクノロジー（[ スキーマ ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/home)および[ データセット ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/overview)を含む）および[ データ収集テクノロジー](https://experienceleague.adobe.com/en/docs/experience-platform/collection/home) （[ データストリーム ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/overview)および[ タグ ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home)を含む）

  これらのテクノロジには、Experience Platform サイト管理者のサポートが必要です。

* （[!DNL Analytics for Advertising]を持たない広告主）CollaborationとAdobe アカウントチーム（設定中に様々なタスクを完了する）。

  Adobe Experience PlatformおよびAdobe Customer Journey Analytics アカウントへのAdobe アカウントレベルのアクセス権を付与する場合は、チームと相談できます。 アクセスは統合を完了する必要はありませんが、アクセスを使用すると、Adobe アカウントチームは、統合のオンボーディング、設定とデータの検証の完了、Adobe Advertising レポートディメンションと指標の使用方法のトレーニングを最大限にサポートできます。

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>*  [!DNL Customer Journey Analytics]](ids.md)様が使用している[Adobe Advertising ID
>* [ データ収集、データ転送、レポートの設定](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション ](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md)。
>* [ トラブルシューティング ](troubleshooting.md)
