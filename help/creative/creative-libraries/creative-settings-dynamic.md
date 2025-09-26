---
title: 動的クリエイティブ設定
description: ダイナミッククリエイティブの設定を参照します。
feature: Creative Dynamic Creatives
source-git-commit: 31651c4e30d22b4d1639ef3fc05d5ff9e02dd040
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 0%

---

# 動的クリエイティブ設定

<!-- add a description -->

<!-- This looks the same for me for either HTML5 type as of 9/24:

## Dynamic ad settings for static HTML5 ads {#dynamic-ad-settings-static-html5}

### Basic Details

**[!UICONTROL Advertiser]:** The advertiser for which to create the ads.

**[!UICONTROL Library]:** The creative library in which to create the ads.

**[!UICONTROL Dynamic Ad Name]:** A unique name for the creative.

**[!UICONTROL Ad Template Size]:** The ad dimensions for the ad template from which to create the ad. If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template Type]:** The type of ad template from which to create the ad: *[!UICONTROL Static HTML5]* or *[!UICONTROL Dynamic HTML5]*.  If you first select a specific [!UICONTROL Ad Template], then this value is automatically selected.

**[!UICONTROL Ad Template]:** The ad template from which to create the ad.

**[!UICONTROL clickURL]:** A valid landing page URL to which users are redirected when they click the ad.

### [!UICONTROL Attributes Details]

-->

## 動的広告設定 <!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本詳細

**[!UICONTROL Dynamic Ad Name]:** クリエイティブの一意の名前。

**[!UICONTROL Advertiser]:** 広告を作成する広告主。

**[!UICONTROL Library]:** 広告を作成するクリエイティブライブラリ。 [!UICONTROL Creatives] > [!UICONTROL Creative Libraries] 内から広告を作成する場合、ライブラリ名は既に選択されており、読み取り専用です。

**[!UICONTROL Ad Template Size]:** 広告の作成元となる広告テンプレートの [ 広告ディメンション ](/help/creative/creative-libraries/creative-sizes.md)。 最初に特定の [!UICONTROL Ad Template] を選択すると、この値が自動的に選択されます。

## 広告テンプレート

**[!UICONTROL Ad Template]:** 広告の作成元となる広告テンプレート。 既存の広告テンプレートを選択するか、新しい広告テンプレートをアップロードして、テンプレートタイプ（*静的* または *動的*）を選択します。 アップロードするテンプレートは、ZIP 形式であり、HTML5 ファイルとテンプレート定義ファイル（template.TDF）が含まれている必要があります。<!-- Need to add more specs for that -->

**[!UICONTROL Number of offers (Max 50)]:** カルーセルに表示する製品数。

## カタログ

**[!UICONTROL Template]:** 広告の作成に使用するフィードテンプレート。

**\[ カタログ\]**：広告を生成する 1 つ以上のカタログ。 既存のカタログを選択するか、既存のフィードテンプレートをダウンロードして新しいカタログを作成してアップロードすることで、新しいカタログを作成します。

アップロードするカタログは、ZIP 形式で、かつ次の内容が含まれている必要があります。

* CSV、TSV またはMicrosoft Excel スプレッドシート（XLSX）形式の 1 つ以上のフィードファイル。<!-- Need to add more specs for that -->

* GIF、JPEG、JPG、PNG 形式の画像アセット

* （オプション） MP4 または WEBM 形式のビデオアセット

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**: <!-- "targeting options/filters," but I don't think this means user targeting since that is set in the experience/ad on DSP --> 広告を作成するために値が存在する必要があるフィードファイルの列のタイプ：*[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **メモ：** これらの設定は、広告エクスペリエンス設定の詳細設定とは独立して機能します。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

指定した広告テンプレートの各属性（動的広告フィールド）を、指定したカタログ（カタログラベル）の列にマッピングするか、静的な値を入力します。

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリへのダイナミッククリエイティブの追加 ](creative-add-dynamic.md)
>* [ クリエイティブライブラリ内のダイナミッククリエイティブの編集 ](creative-edit-dynamic.md)
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
