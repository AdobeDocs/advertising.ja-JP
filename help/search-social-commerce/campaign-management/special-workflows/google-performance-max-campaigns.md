---
title: パフォーマンスの最大キャンペーンを [!DNL Google Ads] 実装する
description: 'パフォーマンスの最大キャンペーンを設定するワークフローについて説明します。 [!DNL Google Ads] '
exl-id: 4208774c-e4dd-499d-987e-933fe073c04f
feature: Search Campaign Management
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '286'
ht-degree: 0%

---

# パフォーマンスの最大数[!DNL Google Ads]件のキャンペーンを実装

[!DNL Google Ads] パフォーマンスの最大キャンペーンでは、広告グループ、広告、キーワードを設定していません。 代わりに、キャンペーン設定内で、見出し、説明、アップロードされた画像、ロゴ、および[!DNL YouTube videos]を含む1つ以上のアセットグループを指定します。 [!DNL Google Ads]は、チャネル （[!DNL YouTube]、[!DNL Gmail]、または[!DNL Search]など）に基づいて、アセットを自動的に組み合わせて広告を配信します。

パフォーマンス データが表およびトレンドチャート形式の既存のパフォーマンス最大キャンペーンを[!DNL Campaigns] ビューで表示できます。データは下位レベルでは使用できません。 キャンペーンレベルのパフォーマンスデータは、レポートおよびAdobe Analyticsでも利用できます（[Analyticsとの統合](/help/integrations/analytics/overview.md)を持つ広告主向け）。 パフォーマンスの最大キャンペーンのパフォーマンスデータを[!DNL Analytics]で表示するには、キャンペーンで[&#x200B; アップグレードされたAMO ID トラッキングコード &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items) （キャンペーン IDと広告グループ IDをトラッキング）を使用する必要があります。

>[!NOTE]
>
>* すべての画像ファイルを手動でアップロードする必要があります。 [!DNL Google Merchant Center]個の製品フィードへのリンクはサポートされていません。
>* 必要な設定のみが使用できます。 オプションの設定については、[!DNL Google Ads] エディターにログインしてください。
>* リストグループのサポートは利用できません。 リスト グループのデータを管理および表示するには、[!DNL Google Ads] エディターにログインします。

## [!DNL Google Ads] パフォーマンス最大キャンペーンを設定する手順

パフォーマンスの最大キャンペーンは、[!UICONTROL Campaigns] > [!UICONTROL Campaigns] ビューから個別に設定できます。

1. [&#x200B; キャンペーンの種類](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)を含むキャンペーン **[!UICONTROL Performance Max]**&#x200B;を作成します。

   [!UICONTROL Campaign Details]、[!UICONTROL Budget Options]、[!UICONTROL Campaign Targeting]、[!UICONTROL URL Options]を指定します。 オプションで[!UICONTROL Negative Keywords]を入力し、[!UICONTROL Negative Websites]と入力するか、[!UICONTROL Campaign Tracking] オプションを上書きします。

1. アセットグループを作成し、キャンペーン用のアセットをアップロードします。

   1. キャンペーン設定の下部にある「**[!UICONTROL Manage Asset Groups]**」をクリックします。

   1. 最初のアセットグループの設定を指定し、アセットグループの画像、ロゴ、オプションのビデオをアップロードします。

      要件と仕様については、[&#x200B; アセットグループ設定の説明](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)を参照してください。

   1. 必要に応じてアセットグループを追加します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

1. （オプション）最適化のためにキャンペーンをハイブリッドポートフォリオに追加します。
