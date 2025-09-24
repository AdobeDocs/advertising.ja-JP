---
title: 動的広告のワークフロー
description: 動的広告を管理するためのワークフローについて説明します。
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '281'
ht-degree: 0%

---

# 動的広告のワークフロー

1. 使用可能なアセットに基づいて、動的広告用に [ 広告テンプレートを作成 ](/help/creative/ad-templates/ad-template-manage.md) します

1. 広告要素を設定します。

   * （単一の静的HTML5 広告の場合）広告の収集と [ 画像アセットのアップロード ](/help/creative/feeds/asset-manage.md)。

   * （動的なHTML5 広告の場合）広告要素のカタログを作成します。

      1. Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルを、広告バリエーションごとに 1 行ずつ作成します。 各行に画像名またはAdobe Experience Managerへの参照を含めます。 関連する画像アセットを個別に収集します。

      1. [ フィードファイルと画像アセットをアップロードします ](/help/creative/feeds/asset-manage.md)。

      1. [ フィードテンプレートを作成 ](/help/creative/feeds/feed-template-manage.md) して、フィードファイル（スプレッドシート）のフィールドをAdvertising Creative バックエンドのフィールドにマッピングします。

      1. 指定したフィードファイルと指定したフィードテンプレートから [ カタログを作成 ](/help/creative/feeds/catalog-manage.md#feed-catalog-create) してから [ カタログを処理 ](/help/creative/feeds/catalog-manage.md#feed-catalog-process) して、そのファイルから作成できる広告のバリエーションを確認します。

         各フィードファイルは、1 つのカタログにのみ使用できます。

         [ ーザー/](/help/creative/feeds/job-status-track.md) ーザー/[!UICONTROL Creative] ーザー [!UICONTROL Feeds] タブで、[!UICONTROL Job Status] カタログ処理ジョブのステータスを追跡する）ことができます。

1. クリエイティブライブラリの [ ダイナミッククリエイティブの作成 ](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5 広告については、指定した広告テンプレートとカタログを使用します。

1. 広告エクスペリエンスにすべてを一度に添付できる [ 動的広告バンドルを作成 ](/help/creative/creative-libraries/bundle-manage.md) します。

1. [ ターゲティングを使用 ](/help/creative/experiences/experience-create-targeting.md) または [ ターゲティングを使用せずに ](/help/creative/experiences/experience-create-no-targeting.md) 動的な広告エクスペリエンスを作成し、[ クリエイティブバンドルをエクスペリエンスに割り当てる ](/help/creative/experiences/experience-assign-creative-bundles.md) ことができます。

1. [ad experience タグを生成および実装 ](/help/creative/experiences/experience-tag-export.md) して、DSPの広告として実行します。

   広告エクスペリエンスをAdobe Advertising DSPの広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 異なるDSPの広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。
