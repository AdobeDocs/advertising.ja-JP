---
title: プレースメント [!UICONTROL Diagnostics] レポートを表示
description: プレースメントの設定とペーシングに関する問題を診断する方法について説明します。
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
TQID: https://experienceleague.adobe.com/aRELxvUfrIZVu7-qzxO8QfrlMGNP17YJk0ru04oRFQQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# プレースメント [!UICONTROL Diagnostics] レポートを表示

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

診断レポートは、キャンペーンが公開された後に、配置の設定とペーシングに関する問題を診断するのに役立ちます。

## プレースメント [!UICONTROL Diagnostics] レポートの情報

* **[!UICONTROL Change Log]:**&#x200B;名前、ステータス、最大入札額など、主要なプレースメント設定の変更を表示します。 各エントリには、変更を行ったユーザーの日付とユーザー名が含まれます。

* **[!UICONTROL Ad Approvals]:**&#x200B;広告が在庫プロバイダーによって承認または拒否されたかどうかを表示します。 オプションで、任意の広告のステータスを変更したり（拒否された広告を一時停止するなど）、広告設定を開いたりできます。

* **[!UICONTROL Non Bids]:** DSPがプレースメントに入札しなかった理由を示します。

## プレースメント [!UICONTROL Diagnostics] レポートを開きます

1. [!UICONTROL Diagnostics] レポートを開きます。

   1. プレースメント設定を開きます。

      1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

      1. キャンペーンの名前をクリックし、**[!UICONTROL Placements]**&#x200B;をクリックします。

      1. プレースメント名の横にある「**[!UICONTROL ...]** > **[!UICONTROL Edit]**」をクリックします。

   1. 右上の「![配置診断](/help/dsp/assets/placement-diagnostics.png)」をクリックします。

1. 次のいずれかの操作を行います。

   * 変更ログを表示するには：

      1. **[!UICONTROL Change Log]**&#x200B;をクリックします。

      1. （オプション）レポート結果をフィルタリングします。

         * 日付メニューで、レポート期間をデフォルトの過去14日間から別の期間（*[!UICONTROL Last 30 days],* *[!UICONTROL Last 60 days],* *[!UICONTROL Last 90 days],*, *[!UICONTROL Last 1 year]*）に変更します。

         * 左側のメニューで、特定のユーザー名でレポートをフィルタリングします。

         * 右側のメニューで、特定の配置設定でレポートをフィルタリングします。

   * 広告承認のステータスを表示するには：

      1. 右上の「**[!UICONTROL Ad Approvals]**」をクリックします。

      1. （オプション）広告を一時停止またはアクティブにするには、広告列のステータススイッチ（![ ステータススイッチ ](/help/dsp/assets/status-switch.png)）をクリックします。

      1. （オプション）広告の設定を開くには、広告の横にある「**[!UICONTROL View Ad]**」をクリックします。

   * DSPが入札しなかった理由を確認するには：

      1. 右上の「**[!UICONTROL Non Bids]**」をクリックします。

      1. （オプション）特定のプライベート契約ターゲットでプレースメントをフィルタリングするには、契約を選択します。<!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. （オプション）日付範囲を変更するには、日付フィールドをクリックし、別の日付または日付範囲を選択します。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [ キャンペーン管理ビューのパフォーマンスレポートの種類](campaign-reports-about.md)
>* [ プレースメント予測レポートを表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
