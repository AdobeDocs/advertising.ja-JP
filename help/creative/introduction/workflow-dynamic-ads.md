---
title: 動的広告のワークフロー
description: 動的広告を管理するワークフローについて説明します。
feature: Creative Dynamic Creatives
exl-id: eb1cdfbc-9514-4530-a50a-3ae6f6247662
TQID: https://experienceleague.adobe.com/2ysfPVepzFjlxE-ecuAVpX-ntQBWB9dN61AELW74ZvI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 643
ht-degree: 0%

---

# 動的広告のワークフロー

*動的な広告を作成する権限を持つユーザー*

動的広告は、次の2つの方法のいずれかで設定できます。

* ワークフロー1：動的な広告をクリエイティブライブラリに追加する際、動的な広告設定の中で広告テンプレートと広告バリエーションのカタログを直接アップロードします。 既存のフィード テンプレートをダウンロードして、カタログを作成できます。

  このワークフローは、同じユーザーが広告を作成するためにすべての情報（フィードテンプレートを除く）を提供できる場合に使用します。 アップロードされたファイルは、今後の使用に使用できます。

* ワークフロー2：広告テンプレートと広告バリエーションのカタログを個別のビュー内に設定し、既存の広告テンプレートとカタログを使用してクリエイティブに動的な広告を個別に追加します。

  このワークフローは、異なるユーザーが異なるタスクを完了する場合や、一度に1つのタスクのみを完了する場合に使用します。

## ワークフロー1

>[!PREREQUISITES]
>
>* 広告テンプレート：ディスプレイ広告テンプレート（HTML5 ファイル付きのZIP ファイル）またはビデオ広告テンプレート（シーン付きのZIP ファイル）
>* CSV、TSV、またはMicrosoft Excel スプレッドシート（XLSX）形式の商品カタログ

1. クリエイティブライブラリ用の[動的クリエイティブを作成](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5およびビデオ広告の場合は、既存の広告テンプレートとカタログをアップロードまたは選択します。

1. 広告エクスペリエンスにダイナミッククリエイターを活用する：

   1. [動的な広告バンドル &#x200B;](/help/creative/creative-libraries/bundle-manage.md)を作成して、広告エクスペリエンスにすべてを一度に添付できます。

   1. ターゲティング [と](/help/creative/experiences/experience-create-targeting.md)を使用せずに、ターゲティング [または](/help/creative/experiences/experience-create-no-targeting.md)を使用して動的な広告エクスペリエンス [を作成し、クリエイティブ バンドルをエクスペリエンス &#x200B;](/help/creative/experiences/experience-assign-creative-bundles.md)に割り当てます。

   1. [広告エクスペリエンスタグを生成して実装し](/help/creative/experiences/experience-tag-export.md)、広告としてDSPで実行します。

      Adobe Advertising DSPで広告エクスペリエンスを広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 別のDSPで広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。

## ワークフロー2

1. [使用可能なアセットに基づいて、動的広告用の広告テンプレート &#x200B;](/help/creative/ad-templates/ad-template-manage.md)を作成します。 広告テンプレートはZIP形式で次を含んでいる必要があります：<!-- Need to add more specs for templates -->

* クリエイティブの表示：目的の広告フォーマットを含むHTML5 ファイルと、広告属性（.tdf）を含むファイル（動的HTML5 adsのみ）

* ビデオクリエイティブ：目的の広告形式を持つ.scene ファイルと、広告属性（.tdf）を持つファイル

1. 広告要素を設定する：

   * （1つの静的なHTML5広告の場合）広告用の画像アセット [を収集して](/help/creative/feeds/asset-manage.md) アップロードします。

   * （ダイナミックなHTML5広告および動画広告の場合）広告要素のカタログを作成します。

      1. Microsoft Excel スプレッドシート（XLSX）形式で、広告バリエーションごとに1行のフィードファイルを作成します。 各行に画像またはビデオ名を含めます。 関連する画像とビデオアセットを個別に収集します。

      1. [&#x200B; フィード ファイルとアセットをアップロード &#x200B;](/help/creative/feeds/asset-manage.md)。

      1. [&#x200B; フィードテンプレート &#x200B;](/help/creative/feeds/feed-template-manage.md)を作成して、フィードファイル（スプレッドシート）のフィールドをAdvertising Creative バックエンドのフィールドにマッピングします。 オプションで、任意のキャンペーンタイプに関連するフィールドを含むユニバーサルフィードテンプレートをダウンロードして入力できます。

      1. [指定したフィード ファイルと指定したフィード テンプレートからカタログ &#x200B;](/help/creative/feeds/catalog-manage.md#feed-catalog-create)を作成し、[&#x200B; カタログ &#x200B;](/help/creative/feeds/catalog-manage.md#feed-catalog-process)を処理して、作成できる広告バリエーションを確認します。

         各フィードファイルは1つのカタログにのみ使用できます。

         [&#x200B; カタログ処理ジョブのステータスを](/help/creative/feeds/job-status-track.md)で[!UICONTROL Creative] > [!UICONTROL Feeds] > [!UICONTROL Job Status] タブで追跡できます。

1. クリエイティブライブラリ用の[動的クリエイティブを作成](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5広告の場合は、指定した広告テンプレートと指定したカタログを使用します。

1. 広告エクスペリエンスにダイナミッククリエイターを活用する：

   1. [動的な広告バンドル &#x200B;](/help/creative/creative-libraries/bundle-manage.md)を作成して、広告エクスペリエンスにすべてを一度に添付できます。

   1. ターゲティング [と](/help/creative/experiences/experience-create-targeting.md)を使用せずに、ターゲティング [または](/help/creative/experiences/experience-create-no-targeting.md)を使用して動的な広告エクスペリエンス [を作成し、クリエイティブ バンドルをエクスペリエンス &#x200B;](/help/creative/experiences/experience-assign-creative-bundles.md)に割り当てます。

   1. [広告エクスペリエンスタグを生成して実装し](/help/creative/experiences/experience-tag-export.md)、広告としてDSPで実行します。

      Adobe Advertising DSPで広告エクスペリエンスを広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 別のDSPで広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。
