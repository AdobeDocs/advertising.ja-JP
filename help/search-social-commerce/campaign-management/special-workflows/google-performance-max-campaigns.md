---
title: パフォ  [!DNL Google Ads]  マンス最大化キャンペーンの実装
description: パフォーマンス最大化キャンペーンを設定するためのワークフロー  [!DNL Google Ads]  ついて説明します。
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 283fced2b3faa64b6383b6ab2a41696cba0da06f
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# [!DNL Google Ads] パフォーマンス最大化キャンペーンの実装

パフォ [!DNL Google Ads] マンス最大化キャンペーンでは、広告グループ、広告またはキーワードを設定しません。 代わりに、キャンペーン設定内で、ヘッドライン、説明、アップロードされた画像、ロゴおよび [!DNL YouTube videos] ータを含む、1 つ以上のアセットグループを指定します。 [!DNL Google Ads] では、アセットを自動的に組み合わせ、チャネル（[!DNL YouTube]、[!DNL Gmail]、[!DNL Search] など）に基づいて広告を提供します。

[!DNL Campaigns] ビューでは、既存の Performance MAX キャンペーンのパフォーマンスデータを表形式およびトレンドグラフ形式で表示できます。下位レベルではデータを利用できません。 また、キャンペーンレベルのパフォーマンスデータは、レポートやAdobe Analyticsでも入手することができます（[Analytics 統合を利用する広告主向け ](/help/integrations/analytics/overview.md)。 [!DNL Analytics] で Performance MAX キャンペーンのパフォーマンスデータを表示するには、キャンペーンは [ アップグレードされた AMO ID トラッキングコード ](/help/integrations/analytics/ids.md#amo-id-formats) を使用する必要があります（これはキャンペーン ID と広告グループ ID をトラッキングします）。

>[!NOTE]
>
>* すべての画像ファイルを手動でアップロードする必要があります。 [!DNL Google Merchant Center] 製品フィードへのリンクはサポートされていません。
>* 必要な設定のみ使用できます。 オプション設定の場合は、[!DNL Google Ads] エディターにログインします。
>* グループの一覧表示はサポートされていません。 グループをリストするデータを管理および表示するには、[!DNL Google Ads] エディターにログインします。

## [!DNL Google Ads] Performance MAX キャンペーンの設定手順

[!UICONTROL Campaigns]/[!UICONTROL Campaigns] ビューから個別に Performance MAX キャンペーンを設定できます。

1. キャンペーンタイプ **[!UICONTROL Performance Max]** の [ キャンペーンを作成 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)。

   [!UICONTROL Campaign Details]、[!UICONTROL Budget Options]、[!UICONTROL Campaign Targeting]、[!UICONTROL URL Options] を指定します。 必要に応じて、[!UICONTROL Negative Keywords] を入力し、[!UICONTROL Negative Websites] を入力するか、[!UICONTROL Campaign Tracking] のオプションを上書きします。

1. アセットグループを作成し、キャンペーン用のアセットをアップロードします。

   1. キャンペーン設定の下部にある「**[!UICONTROL Manage Asset Groups]**」をクリックします。

   1. 最初のアセットグループの設定を指定し、そのアセットグループの画像、ロゴおよびオプションのビデオをアップロードします。

      要件と仕様については、[ アセットグループ設定の説明 ](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) を参照してください。

   1. 必要に応じて、アセットグループを追加します。

1. 「**[!UICONTROL Post]**」をクリックします。

1. （任意）最適化のために、キャンペーンをハイブリッドポートフォリオに追加します。
