---
title: 動的広告のワークフロー
description: 動的広告を管理するためのワークフローについて説明します。
feature: Creative Dynamic Creatives
source-git-commit: 02ac4175c1d91f4f6d65bb2d683a7909f06a287c
workflow-type: tm+mt
source-wordcount: '533'
ht-degree: 0%

---

# 動的広告のワークフロー

動的広告は、次の 2 つの方法のいずれかで設定できます。

* ワークフロー 1：動的広告をクリエイティブライブラリに追加する場合は、動的広告設定内に広告テンプレートと広告バリエーションカタログを直接アップロードします。 既存のフィードテンプレートをダウンロードしてカタログを作成できます。

  このワークフローは、同じ人物がすべての情報（フィードテンプレートを除く）を提供して広告を作成できる場合に使用します。 アップロードされたファイルは、引き続き使用できます。

* ワークフロー 2：広告テンプレートと広告バリエーションカタログを別々のビューに設定し、既に使用可能な広告テンプレートとカタログを使用してクリエイティブに個別に動的広告を追加する。

  このワークフローは、複数のユーザーが異なるタスクを完了する場合、または一度に 1 つのタスクのみを完了する場合に使用します。

## ワークフロー 1

1. クリエイティブライブラリの [ ダイナミッククリエイティブの作成 ](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5 広告の場合は、広告テンプレートとカタログをアップロードします。

1. 広告エクスペリエンス用の動的クリエイティブを使用します。

   1. 広告エクスペリエンスにすべてを一度に添付できる [ 動的広告バンドルを作成 ](/help/creative/creative-libraries/bundle-manage.md) します。

   1. [ ターゲティングを使用 ](/help/creative/experiences/experience-create-targeting.md) または [ ターゲティングを使用せずに ](/help/creative/experiences/experience-create-no-targeting.md) 動的な広告エクスペリエンスを作成し、[ クリエイティブバンドルをエクスペリエンスに割り当てる ](/help/creative/experiences/experience-assign-creative-bundles.md) ことができます。

   1. [ad experience タグを生成および実装 ](/help/creative/experiences/experience-tag-export.md) して、DSPの広告として実行します。

      広告エクスペリエンスをAdobe Advertising DSPの広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 異なるDSPの広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。

## ワークフロー 2

1. 使用可能なアセットに基づいて、動的広告用に [ 広告テンプレートを作成 ](/help/creative/ad-templates/ad-template-manage.md) します。

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

1. 広告エクスペリエンス用の動的クリエイティブを使用します。

   1. 広告エクスペリエンスにすべてを一度に添付できる [ 動的広告バンドルを作成 ](/help/creative/creative-libraries/bundle-manage.md) します。

   1. [ ターゲティングを使用 ](/help/creative/experiences/experience-create-targeting.md) または [ ターゲティングを使用せずに ](/help/creative/experiences/experience-create-no-targeting.md) 動的な広告エクスペリエンスを作成し、[ クリエイティブバンドルをエクスペリエンスに割り当てる ](/help/creative/experiences/experience-assign-creative-bundles.md) ことができます。

   1. [ad experience タグを生成および実装 ](/help/creative/experiences/experience-tag-export.md) して、DSPの広告として実行します。

      広告エクスペリエンスをAdobe Advertising DSPの広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 異なるDSPの広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。
