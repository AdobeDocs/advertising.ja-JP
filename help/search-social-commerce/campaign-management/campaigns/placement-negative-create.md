---
title: ネガティブプレースメントを作成
description: ' [!DNL Google Ads] 件のキャンペーンと広告グループに対してネガティブプレースメントを作成する方法について説明します。'
exl-id: 9cc2dd8d-5563-4e02-af8f-6181165494d8
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/LFHoipRyiY36uTj-0G3lFahitrT9ZHD958V-4T-XIUA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 202
ht-degree: 0%

---

# [!DNL Google Ads]件のネガティブプレースメント用に作成

*[!DNL Google Ads]アカウントのみ*

ディスプレイ ネットワークをターゲットとするキャンペーンの[!DNL Google Ads]広告グループに対して、ネガティブなプレースメントを作成できます。 ネガティブプレースメントは、広告をトリガーしないディスプレイネットワーク内のサイトです。

>[!NOTE]
>また、[広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)および[ キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)でネガティブプレースメントを作成および編集することもできます。

>[!TIP]
>一度に多数のネガティブプレースメントを作成するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックし、**[!UICONTROL Campaign]**&#x200B;をクリックしてキャンペーンレベルのネガティブプレースメントを作成するか、**[!UICONTROL Ad Group]**&#x200B;をクリックして広告グループレースメントを作成します。

1. 広告ネットワーク、アカウント、キャンペーン、および（関連する場合）広告グループを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. 否定的なweb サイト URLを入力します。

   複数の文字列を指定するには、それらをコンマで区切るか、別々の行に入力します。 有効な形式は次のとおりです。

   * Web サイト：www.example.comなどの有効なURLを入力します。 許可される形式は、https://support.google.com/google-ads/answer/2454012の「除外URLを追加する方法」を参照してください。

   * トピック、カテゴリ、ドキュメントの垂直方向。 [[!DNL Google Ads]  ガイドライン ](https://support.google.com/google-ads/editor/answer/30517)とすべての業種の[ リスト ](https://developers.google.com/adwords/api/docs/appendix/verticals)を参照してください。 例：`category::Industries > Energy & Utilities > Oil & Gas`。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ プレースメントについて](placement-about.md)
>* [入札可能なプレースメントの管理](placement-manage.md)
>* [ プレースメントとネガティブプレースメントのステータスを変更](placement-status-edit.md)
