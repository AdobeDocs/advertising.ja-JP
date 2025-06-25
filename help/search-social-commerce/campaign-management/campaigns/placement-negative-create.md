---
title: 負のプレースメントを作成
description: キャンペーンおよび広告グループのネガティブプレースメントを作成する方法に  [!DNL Google Ads]  いて説明します。
exl-id: 9cc2dd8d-5563-4e02-af8f-6181165494d8
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# 負のプレースメント [!DNL Google Ads] 作成

*[!DNL Google Ads]アカウントのみ*

ディスプレイネットワークをターゲットとするキャンペーンで、[!DNL Google Ads] の広告グループに対して負のプレースメントを作成できます。 ネガティブプレースメントは、ディスプレイネットワーク内の広告をトリガーしないサイトです。

>[!NOTE]
>また、[ 広告グループ設定 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) および [ キャンペーン設定 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) で、ネガティブプレースメントを作成および編集することもできます。

>[!TIP]
>一度に多くの負のプレースメントを作成するには、[campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]** をクリックします。

1. データ テーブルの上にあるツールバーで、![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ") をクリックし、**[!UICONTROL Campaign]** をクリックしてキャンペーンレベルの負の配置を作成するか、**[!UICONTROL Ad Group]** をクリックして広告グループレベルの負の配置を作成します。

1. 広告ネットワーク、アカウント、キャンペーン、（該当する場合は）広告グループを選択し、「**[!UICONTROL Continue]**」をクリックします。

1. 負の Web サイト URL を入力します。

   複数の文字列を指定する場合は、コンマで区切るか、別の行に入力します。 有効な形式は次のとおりです。

   * Web サイト：有効な URL （www.example.comなど）を入力します。 https://support.google.com/google-ads/answer/2454012にある「除外 URL の追加方法」で許可されている形式を参照してください。

   * トピック、カテゴリ、または文書の垂直方向。 [[!DNL Google Ads]  ガイドライン ](https://support.google.com/google-ads/editor/answer/30517) および [ すべての垂直軸のリスト ](https://developers.google.com/adwords/api/docs/appendix/verticals) を参照してください。 例：`category::Industries > Energy & Utilities > Oil & Gas`。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ プレースメントについて ](placement-about.md)
>* [ 入札可能プレースメントの管理 ](placement-manage.md)
>* [ プレースメントとネガティブプレースメントのステータスの変更 ](placement-status-edit.md)
