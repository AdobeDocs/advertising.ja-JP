---
title: ネガティブな配置の作成
description: 除外配置の作成方法を学ぶ [!DNL Google Ads] キャンペーンと広告グループの両方に割り当てられます。
exl-id: 8bddfc12-de95-46c3-aa2d-bcce2a5e0de9
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 作成対象 [!DNL Google Ads] 負の配置

*[!DNL Google Ads]アカウントのみ*

以下の場合に、ネガティブな配置を作成できます。 [!DNL Google Ads] ディスプレイネットワークをターゲットとするキャンペーンの広告グループ。 負の配置は、広告をトリガーしないディスプレイネットワーク内のサイトです。

>[!NOTE]
>また、 [広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) および [キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>一度に多数の否定的な配置を作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Negatives]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成")をクリックし、 **[!UICONTROL Campaign]** キャンペーンレベルのネガティブな配置を作成するには、または **[!UICONTROL Ad Group]** 広告グループレベルのネガティブな配置を作成する。

1. 広告ネットワーク、アカウント、キャンペーン、および（関連する場合）広告グループを選択し、「 **[!UICONTROL Continue]**.

1. 否定的な Web サイトの URL を入力します。

   複数の文字列を指定するには、コンマで区切るか、複数の文字列を別々の行に入力します。 有効な形式は次のとおりです。

   * Web サイト：有効な URL(www.example.comなど ) を入力します。 https://support.google.com/google-ads/answer/2454012の「除外 URL の追加方法」で、使用可能な形式を参照してください。

   * トピック、カテゴリ、またはドキュメントのバーティカル。 詳しくは、 [[!DNL Google Ads] ガイドライン](https://support.google.com/google-ads/editor/answer/30517) および [すべての業種のリスト](https://developers.google.com/adwords/api/docs/appendix/verticals). 例： `category::Industries > Energy & Utilities > Oil & Gas`.

1. クリック **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [配置について](placement-about.md)
>* [入札可能な配置の管理](placement-manage.md)
>* [配置と負の配置のステータスの変更](placement-status-edit.md)
