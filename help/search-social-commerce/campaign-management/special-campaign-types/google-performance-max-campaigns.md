---
title: 実装方法 [!DNL Google Ads] 最大パフォーマンスキャンペーン
description: 設定のワークフローについて説明します [!DNL Google Ads] 最大パフォーマンスキャンペーン数
exl-id: afad96b2-d4a6-41ee-ad84-38aa1306d73e
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# 実装方法 [!DNL Google Ads] 最大パフォーマンスキャンペーン

In [!DNL Google Ads] パフォーマンスの最大キャンペーン数に制限される場合は、広告グループ、広告、キーワードは設定されません。 代わりに、キャンペーン設定で、ヘッドライン、説明、アップロードされた画像、ロゴおよび [!DNL YouTube videos]. [!DNL Google Ads] チャネルに基づいて広告を提供するために、アセットを自動的に組み合わせます ( 例： [!DNL YouTube], [!DNL Gmail]または [!DNL Search]) をクリックします。

既存のパフォーマンス最大キャンペーンを、テーブルおよびトレンドグラフ形式のパフォーマンスデータと共に、 [!DNL Campaigns] ビュー。低いレベルではデータを使用できません。 キャンペーンレベルのパフォーマンスデータは、レポートおよびAdobe Analytics( [Analytics の統合](/help/integrations/analytics/overview.md). で最大パフォーマンスキャンペーンのパフォーマンスデータを表示するには [!DNL Analytics]を使用する場合、キャンペーンは [アップグレードされた s_kwcid トラッキングコード](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md) （キャンペーン ID および広告グループ ID を追跡します）。

>[!NOTE]
>
>* すべての画像ファイルを手動でアップロードする必要があります。 リンク先 [!DNL Google Merchant Center] 製品フィードはサポートされていません。
>* 必要な設定のみを使用できます。 オプション設定の場合は、 [!DNL Google Ads] 編集者です。
>* リストグループのサポートは利用できません。 リストグループのデータを管理および表示するには、 [!DNL Google Ads] 編集者です。

## 設定の手順 [!DNL Google Ads] 最大パフォーマンスキャンペーン

最大パフォーマンスキャンペーンは、 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示。

1. [キャンペーンの作成](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) キャンペーンタイプ **[!UICONTROL Performance Max]**.

   次を指定します。 [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Campaign Targeting]、および [!UICONTROL URL Options]. 必要に応じて、 [!UICONTROL Negative Keywords]，と入力します。 [!UICONTROL Negative Websites]、または上書き [!UICONTROL Campaign Tracking] オプション。

1. アセットグループを作成し、キャンペーン用のアセットをアップロードします。

   1. キャンペーン設定の下部で、 **[!UICONTROL Manage Asset Groups]**.

   1. 最初のアセットグループの設定を指定し、アセットグループの画像、ロゴおよびオプションのビデオをアップロードします。

      詳しくは、 [アセットグループ設定の説明](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) 要件と仕様を理解する。

   1. 必要に応じて、他のアセットグループを追加します。

1. クリック **[!UICONTROL Post]**.

1. （オプション）最適化のためにハイブリッドポートフォリオにキャンペーンを追加します。
