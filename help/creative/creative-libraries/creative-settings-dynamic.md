---
title: 動的クリエイティブ設定
description: ダイナミッククリエイティブの設定を参照します。
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
source-git-commit: 164ee92f85c0e649dc2bd6c0224a531eb72d1962
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 動的クリエイティブ設定

<!-- add a description -->

## 動的広告設定 <!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本詳細

**[!UICONTROL Creative Type]:** クリエイティブが *[!UICONTROL Display]* 広告（HTML5）か *[!UICONTROL Video]* 広告か。

**[!UICONTROL Dynamic Display Ad Name]** または **[!UICONTROL Dynamic Video Ad Name]:** クリエイティブの一意の名前。

**[!UICONTROL Advertiser]:** 広告を作成する広告主。 [!UICONTROL Creatives]/[!UICONTROL Creative Libraries] 内から広告を作成している場合、広告主は既に選択されており、読み取り専用です。

**[!UICONTROL Library]:** 広告を作成するクリエイティブライブラリ。 [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] 内から広告を作成する場合、ライブラリ名は既に選択されており、読み取り専用です。

## 広告テンプレート

**[!UICONTROL Ad Template]:** 広告の作成元となる広告テンプレート。 既存の広告テンプレートを選択するか、新しい広告テンプレートをアップロードして、テンプレートタイプ（*静的* または *動的*）を選択します。 テンプレートは、ZIP 形式で、次を含む必要があります。<!-- Need to add more specs for templates -->

* クリエイティブの表示：目的の広告フォーマットを持つHTML5 ファイルと、広告属性（.tdf）を持つ（ダイナミック HTML5 広告のみ）ファイル

* ビデオクリエイティブ：目的の広告形式を持つ.scene ファイル。 ZIP ファイルは最大 512 MB にすることができます。

続行するには、[**[!UICONTROL Select Ad Template]**] をクリックします。

**[!UICONTROL Size]:** （動的なディスプレイ広告のみ。読み取り専用）選択した広告テンプレートの [ 広告ディメンション ](/help/creative/creative-libraries/creative-sizes.md)。広告の作成に使用されます。

**[!UICONTROL Card Count (Max 50)]:** （広告の表示のみ） カルーセルに表示する製品の数。

**[!UICONTROL Duration]:** （ビデオ広告のみ、読み取り専用）選択した広告テンプレートから派生したビデオ再生時間。 各ビデオの再生時間は 1 ～ 90 秒にする必要があります。

## カタログ

**\[ カタログ\]**：広告を生成する 1 つ以上のカタログ。 既存のカタログを選択するか、既存のフィードテンプレートをダウンロードして新しいカタログを作成してアップロードすることで、新しいカタログを作成します。 「**[!UICONTROL Select Catalog]**」をクリックします。

アップロードするカタログは、ZIP 形式で、かつ次の内容が含まれている必要があります。

* （動的表示およびビデオ広告） CSV、TSV またはMicrosoft Excel スプレッドシート（XLSX）形式の 1 つ以上のフィードファイル。 最大ファイルサイズは 512 MB です。<!-- Need to add more specs for the feed files -->

* （広告を表示）GIF、JPEG、JPGまたは PNG 形式の画像アセット

* （ビデオ広告） MP4、MOV、WEBM 形式のビデオアセット。 サポートされる広告テンプレートには、開始カード、終了カード、上部のオーバーレイ、下部のオーバーレイまたは L字型があります。 各ビデオの再生時間は 1 ～ 90 秒にする必要があります。

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP --> 広告を作成するために値が存在する必要があるフィードファイルの列のタイプ：*[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **メモ：** これらの設定は、広告エクスペリエンス設定の詳細設定とは独立して機能します。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

指定した広告テンプレートの各属性（動的広告フィールド）を、指定したカタログ（カタログラベル）の列にマッピングするか、静的な値を入力します。

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリへのダイナミッククリエイティブの追加 ](creative-add-dynamic.md)
>* [ クリエイティブライブラリ内のダイナミッククリエイティブの編集 ](creative-edit-dynamic.md)
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
