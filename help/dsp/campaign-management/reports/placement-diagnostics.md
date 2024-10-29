---
title: プレースメント診断レポートの表示
description: プレースメントの設定とペーシングに関する問題を診断する方法を説明します。
feature: DSP Placements
exl-id: 95e88c9c-09f2-44f1-9d6c-3fe533963f9a
source-git-commit: fa4cee46135c85849daa7faa4059c77fc753c2c8
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# プレースメント診断レポートの表示

<!-- Does this really belong in the Campaign Management > Reports section or in the Placements section? -->

診断レポートは、キャンペーンがライブになった後のプレースメントの設定とペーシングに関する問題を診断するのに役立ちます。

## プレースメント診断レポートの情報

* **[!UICONTROL Change Log]:** 名前、ステータス、最大入札額など、主要なプレースメント設定に対する変更を表示します。 各エントリには、変更を行ったユーザーの日付とユーザー名が含まれます。

* **[!UICONTROL Ad Approvals]:** 広告が在庫プロバイダーによって承認または却下されたかどうかを表示します。 オプションで、広告のステータスを変更したり（却下された広告を一時停止するなど）、広告設定を開いたりできます。

* **[!UICONTROL Non Bids]:** DSPがプレースメントに入札しなかった理由を示します。

## プレースメント診断レポートを開く

1. 診断レポートを開きます。

   1. プレースメント設定を開きます。

      1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

      1. キャンペーンの名前をクリックし、「**[!UICONTROL Placements]**」をクリックします。

      1. プレースメント名の横で、**[!UICONTROL ...]**/**[!UICONTROL Edit]** をクリックします。

   1. 右上で、「![ プレースメント診断 ](/help/dsp/assets/placement-diagnostics.png)」をクリックします。

1. 次のいずれかの操作をおこないます。

   * 変更ログを表示するには、次の手順に従います。

      1. 「**[!UICONTROL Change Log]**」をクリックします。

      1. （任意）レポート結果のフィルタリング：

         * 日付メニューで、レポート期間をデフォルトの過去 14 日間から別の期間（*[!UICONTROL Last 30 days]、*、*[!UICONTROL Last 60 days]、*、*[!UICONTROL Last 90 days]、* または *[!UICONTROL Last 1 year]*）に変更します。

         * 左側のメニューで、特定のユーザー名でレポートをフィルタリングします。

         * 右側のメニューで、特定のプレースメント設定を使用してレポートをフィルタリングします。

   * 広告承認のステータスを表示するには：

      1. 右上で、「**[!UICONTROL Ad Approvals]**」をクリックします。

      1. （オプション）広告を一時停止またはアクティブ化するには、広告列のステータススイッチ（![ ステータススイッチ ](/help/dsp/assets/status-switch.png)）をクリックします。

      1. （任意）広告の設定を開くには、広告の横にある「**[!UICONTROL View Ad]**」をクリックします。

   * DSPがプレースメントに入札しなかった理由を確認するには、次の手順を実行します。

      1. 右上で、「**[!UICONTROL Non Bids]**」をクリックします。

      1. （任意）特定のプライベート取引ターゲットでプレースメントをフィルタリングするには、取引を選択します。<!-- Admin users only: Optionally filter the deal by one or more regions ([!UICONTROL US-EAST], [!UICONTROL US-WEST]) [!UICONTROL EU-WEST], [!UICONTROL HKG]) by selecting the regions. -->

      1. （オプション）日付範囲を変更するには、日付フィールドをクリックして、別の日付または日付範囲を選択します。

<!-- Later, add link to >* Definitions for NBRs (Reading No Bid Reports (NBRs)) -->

>[!MORELIKETHIS]
>
>* [Campaign Management ビューにおけるパフォーマンスレポートのタイプ ](campaign-reports-about.md)
>* [ 配置予測レポートの表示 ](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
