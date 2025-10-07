---
title: 動的広告のワークフロー
description: 動的広告を管理するためのワークフローについて説明します。
feature: Creative Dynamic Creatives
source-git-commit: 0d7a7ab23173a061961c4b5c66ace5b69a746e86
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 0%

---

# 動的広告のワークフロー

*動的広告を作成する権限を持つユーザー*

動的広告は、次の 2 つの方法のいずれかで設定できます。

* ワークフロー 1：動的広告をクリエイティブライブラリに追加する場合は、動的広告設定内に広告テンプレートと広告バリエーションカタログを直接アップロードします。 既存のフィードテンプレートをダウンロードしてカタログを作成できます。

  このワークフローは、同じ人物がすべての情報（フィードテンプレートを除く）を提供して広告を作成できる場合に使用します。 アップロードされたファイルは、引き続き使用できます。

* ワークフロー 2：広告テンプレートと広告バリエーションカタログを別々のビューに設定し、既に使用可能な広告テンプレートとカタログを使用してクリエイティブに個別に動的広告を追加する。

  このワークフローは、複数のユーザーが異なるタスクを完了する場合、または一度に 1 つのタスクのみを完了する場合に使用します。

## ワークフロー 1

>[!PREREQUISITES]
>
>* HTML5 形式の広告テンプレート
>* CSV、TSV、Microsoft Excel スプレッドシート（XLSX）形式の商品カタログ

1. クリエイティブライブラリの [&#x200B; ダイナミッククリエイティブの作成 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5 広告の場合は、広告テンプレートとカタログをアップロードします。

1. 広告エクスペリエンス用の動的クリエイティブを使用します。

   1. 広告エクスペリエンスにすべてを一度に添付できる [&#x200B; 動的広告バンドルを作成 &#x200B;](/help/creative/creative-libraries/bundle-manage.md) します。

   1. [&#x200B; ターゲティングを使用 &#x200B;](/help/creative/experiences/experience-create-targeting.md) または [&#x200B; ターゲティングを使用せずに &#x200B;](/help/creative/experiences/experience-create-no-targeting.md) 動的な広告エクスペリエンスを作成し、[&#x200B; クリエイティブバンドルをエクスペリエンスに割り当てる &#x200B;](/help/creative/experiences/experience-assign-creative-bundles.md) ことができます。

   1. [ad experience タグを生成および実装 &#x200B;](/help/creative/experiences/experience-tag-export.md) して、DSPの広告として実行します。

      広告エクスペリエンスをAdobe Advertising DSPの広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 異なるDSPの広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。

## ワークフロー 2

1. 使用可能なアセットに基づいて、動的広告用に [&#x200B; 広告テンプレートを作成 &#x200B;](/help/creative/ad-templates/ad-template-manage.md) します。 広告テンプレートには、目的の広告フォーマットを持つHTML5 ファイルと、広告属性を持つ（動的HTML5 広告のみ）ファイルが含まれます。

1. 広告要素を設定します。

   * （単一の静的HTML5 広告の場合）広告の収集と [&#x200B; 画像アセットのアップロード &#x200B;](/help/creative/feeds/asset-manage.md)。

   * （動的なHTML5 広告の場合）広告要素のカタログを作成します。

      1. Microsoft Excel スプレッドシート（XLSX）形式のフィードファイルを、広告バリエーションごとに 1 行ずつ作成します。 各行に画像名を含めます。 関連する画像アセットを個別に収集します。

      1. [&#x200B; フィードファイルと画像アセットをアップロードします &#x200B;](/help/creative/feeds/asset-manage.md)。

      1. [&#x200B; フィードテンプレートを作成 &#x200B;](/help/creative/feeds/feed-template-manage.md) して、フィードファイル（スプレッドシート）のフィールドをAdvertising Creative バックエンドのフィールドにマッピングします。

      1. 指定したフィードファイルと指定したフィードテンプレートから [&#x200B; カタログを作成 &#x200B;](/help/creative/feeds/catalog-manage.md#feed-catalog-create) してから [&#x200B; カタログを処理 &#x200B;](/help/creative/feeds/catalog-manage.md#feed-catalog-process) して、そのファイルから作成できる広告のバリエーションを確認します。

         各フィードファイルは、1 つのカタログにのみ使用できます。

         [&#x200B; ーザー/](/help/creative/feeds/job-status-track.md) ーザー/[!UICONTROL Creative] ーザー [!UICONTROL Feeds] タブで、[!UICONTROL Job Status] カタログ処理ジョブのステータスを追跡する）ことができます。

1. クリエイティブライブラリの [&#x200B; ダイナミッククリエイティブの作成 &#x200B;](/help/creative/creative-libraries/creative-add-dynamic.md)。 動的なHTML5 広告については、指定した広告テンプレートとカタログを使用します。

1. 広告エクスペリエンス用の動的クリエイティブを使用します。

   1. 広告エクスペリエンスにすべてを一度に添付できる [&#x200B; 動的広告バンドルを作成 &#x200B;](/help/creative/creative-libraries/bundle-manage.md) します。

   1. [&#x200B; ターゲティングを使用 &#x200B;](/help/creative/experiences/experience-create-targeting.md) または [&#x200B; ターゲティングを使用せずに &#x200B;](/help/creative/experiences/experience-create-no-targeting.md) 動的な広告エクスペリエンスを作成し、[&#x200B; クリエイティブバンドルをエクスペリエンスに割り当てる &#x200B;](/help/creative/experiences/experience-assign-creative-bundles.md) ことができます。

   1. [ad experience タグを生成および実装 &#x200B;](/help/creative/experiences/experience-tag-export.md) して、DSPの広告として実行します。

      広告エクスペリエンスをAdobe Advertising DSPの広告として使用するには、広告エクスペリエンスタグをAdvertising DSP キャンペーンにアップロードします。 異なるDSPの広告として広告エクスペリエンスを使用するには、そのDSPに広告エクスペリエンスタグを実装します。
