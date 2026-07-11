---
title: Creative Studioでの広告テンプレートの管理
description: Adobe Advertising Creativeの「Creative Studio テンプレート」タブで、広告テンプレートを作成、読み込み、整理、管理する方法について説明します。
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 24e27656edda50f29292cb75823ef6cacdb685fe
workflow-type: tm+mt
source-wordcount: 2509
ht-degree: 2%

---

# [!UICONTROL Creative Studio]での広告テンプレートの管理

*Beta機能*

広告生成セッションで使用するディスプレイ広告とビデオ広告のテンプレートを作成、インポート、管理します。

## [!UICONTROL Creative Studio] > [!UICONTROL Templates] ビュー

「**[!UICONTROL Templates]**」タブには、新しい広告テンプレートを作成または読み込むためのクイックアクションが表示されます。

このタブには、ページ <!-- Only in the Templates tab -->の下部にある既存の広告テンプレートも、[個々のカード（デフォルト）またはテーブル/リスト ](/help/creative/introduction/customize-data-views.md)として一覧表示されます。 広告テンプレートリストには、[!UICONTROL All]、[!UICONTROL System Templates] （Adobe アカウントチームによってアカウントにアップロードされます）、および[!UICONTROL User Templates]のタブが含まれます。 デフォルトでは、すべての広告主向けの広告テンプレートが表示されます。 特定の広告主の広告テンプレートのみを表示するには、ページ上部の広告主リストから選択します。

<!-- 

Probably not necessary:

* **[!UICONTROL Card view]** &mdash; Displays templates as cards. Each card shows a preview thumbnail and the ad dimensions. Hovering a card reveals action controls.

* **[!UICONTROL Table view]** &mdash; Displays templates in a table with columns for **[!UICONTROL Name]**, **[!UICONTROL Type]**, **[!UICONTROL Status]**, **[!UICONTROL Size/Duration]**, **[!UICONTROL Advertiser]**, and **[!UICONTROL Updated]**. Click the **[!UICONTROL Name]** or **[!UICONTROL Updated]** column header to sort ascending or descending. Pagination controls appear at the bottom of the list.

-->

### 使用可能なアクション

<!--  Figure out how to handle these, which relate to the template list at the bottom of the page: * [Browse and search templates](#browse-search) -->

制作：

* [HTML5広告テンプレートの読み込み](#templates-import)

* [広告テンプレートを手動で作成](#template-create)

既存のテンプレートに対するアクション：

* [ディスプレイ広告テンプレートからの広告バリエーションの生成](#ad-variations-generate)

* [広告テンプレートの編集](#template-edit)

* [広告テンプレートのラベルの追加または削除](#template-labels)

* [広告テンプレートのプレビュー](#template-preview)

* [広告テンプレートのダウンロード](#template-download)

* [広告テンプレートをお気に入りとして追加または削除](#template-favorite)

* [広告テンプレートの削除](#template-delete)

<!--

Move to a Common Tasks chapter:

## Browse and search templates {#browse-search}

### Search

Type in the **[!UICONTROL Search templates]** field and press **[!UICONTROL Enter]** to find templates by name. Click the **[!UICONTROL Clear search]** button to reset.

### Filter by source

Use the filter pills in the toolbar to show a subset of templates:

* **[!UICONTROL All]** &mdash; Shows all templates.
* **[!UICONTROL System Templates]** &mdash; Shows Adobe-provided templates only.
* **[!UICONTROL User Templates]** &mdash; Shows templates you or your team have created or imported.

### Filter by status or format

1. In the main menu, click **[!UICONTROL Creative Studio].**

1. Click the **[!UICONTROL Templates]** tab.

1. Click **[!UICONTROL Filter]** in the toolbar.

1. In the **[!UICONTROL Filters]** dialog, select a filter category:

   * **[!UICONTROL Status]:** Filter by **[!UICONTROL Live]** or **[!UICONTROL Draft]**.
   * **[!UICONTROL Ad Format]:** Filter by **[!UICONTROL Display]** or **[!UICONTROL Video]**.

1. Select one or more options in the category, then click **[!UICONTROL Apply]**.

Applied filters appear as chips below the toolbar. To refine or remove an active filter, click its chip to open a popover where you can toggle options, then click **[!UICONTROL Apply]** or **[!UICONTROL Delete]** to remove the filter. To remove all active filters at once, click **[!UICONTROL Clear All]**.

-->

## HTML5広告テンプレートの読み込み {#templates-import}

ZIP ファイルとしてパッケージ化された1つ以上の事前定義済みHTML 5 テンプレートをアップロードします。 テンプレートは読み込み時に検証されます。HTMLが200,000文字を超えた場合、CSSが60,000文字を超えた場合、テンプレートに5,000を超えるDOM要素が含まれている場合、またはテンプレートにサポートされていないスクリプトタグが含まれている場合、読み込みは失敗します。

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. ページの上部にある広告主を選択します。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. **[!UICONTROL Upload HTML5 Templates]** ボックスで、**[!UICONTROL Upload]**&#x200B;をクリックし、**[!UICONTROL Display Ad Template]**&#x200B;または&#x200B;**[!UICONTROL Video Ad Template]**&#x200B;を選択します。

1. デバイスまたはネットワークから1つ以上のZIP ファイルを選択します。

1. **[!UICONTROL Import Templates]** ダイアログで、次の操作を行います。

   1. **[!UICONTROL Advertiser]**&#x200B;を選択します。

      ページの上部で特定の広告主を既に選択している場合、その広告主は事前に選択されています。

   1. （オプション）各ファイルについて、**[!UICONTROL Template Name]**&#x200B;を編集します。

      ファイル名はデフォルトで使用されます。

   1. （オプション）さらにファイルを追加するには、**[!UICONTROL Add more]**&#x200B;をクリックし、追加のZIP ファイルを選択します。 追加ファイルごとに&#x200B;**[!UICONTROL Template Name]**&#x200B;を指定します。

1. **[!UICONTROL Import Templates]**&#x200B;をクリックします。

>[!NOTE]
>
>インポートが失敗した場合は、テンプレートを簡略化するか、Adobeアカウントチームにお問い合わせください。

## 広告テンプレートを手動で作成 {#template-create}

テンプレートエディターを使用して、空白のディスプレイまたはビデオテンプレートを作成します。

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. **[!UICONTROL Create New Ad Template]** ボックスで、**[!UICONTROL Create]**&#x200B;をクリックし、**[!UICONTROL Display Ad Template]**&#x200B;または&#x200B;**[!UICONTROL Video Ad Template]**&#x200B;を選択します。

1. （広告を表示）広告テンプレートのサイズを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. テンプレートエディター](#template-controls)の[ コントロールを使用して、テンプレート設定を構成します。

1. （オプション）定義されたテンプレートのコピーをダウンロードするには、**[!UICONTROL ...]** > **[!UICONTROL Download]**&#x200B;をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

1. テンプレートを保存します。

   1. 次のいずれかの操作を行います。

      * **[!UICONTROL Save]**&#x200B;をクリックします。

      * テンプレートをドラフトとして保存するには、**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**&#x200B;をクリックします。

   1. **[!UICONTROL Template name]**&#x200B;を入力し、**[!UICONTROL Advertiser]**&#x200B;を選択し、必要に応じて既存のタグを選択するか、新しいタグをテンプレートに追加してから、**[!UICONTROL Save]**&#x200B;をクリックします。

## 広告テンプレートの編集 {#template-edit}

*広告テンプレートのみを表示します。*

>[!IMPORTANT]
>
>AI エージェントは、テンプレートレイアウト、エレメントの位置、間隔、タイポグラフィを変更できません。 コンテンツを生成する前に、テンプレートエディターで構造変更を行います。

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードまたはテーブルの行にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Template]**&#x200B;をクリックします。

1. テンプレートエディター](#template-controls)の[ コントロールを使用して、テンプレートレイアウトまたは要素を編集します。

1. （オプション）定義されたテンプレートのコピーをダウンロードするには、**[!UICONTROL ...]** > **[!UICONTROL Download]**&#x200B;をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

1. テンプレートを保存します。

   * **[!UICONTROL Save]**&#x200B;をクリックします。

   * テンプレートをドラフトとして保存するには、**[!UICONTROL ...]** > **[!UICONTROL Save as Draft]**&#x200B;をクリックします。 **[!UICONTROL Template name]**&#x200B;を入力し、**[!UICONTROL Advertiser]**&#x200B;を選択し、必要に応じて既存のタグを選択するか、新しいタグをテンプレートに追加してから、**[!UICONTROL Save]**&#x200B;をクリックします。

<!--

I don't see this anywhere:

1. Click **[!UICONTROL Generate Ad Variations]** to proceed to content generation, or navigate away to save your changes.

-->

## テンプレートエディターコントロール {#template-controls}

ディスプレイテンプレートエディターとビデオテンプレートエディターの両方が、編集キャンバスの上と右側の[!UICONTROL Layers] パネルの上に同じ一般的なアクションツールバーを共有します。 左側のパネル、広告テンプレート編集コントロール、およびタイムラインは、ディスプレイテンプレートとビデオテンプレートで異なります。

<!--

Removing -- these are actions that are used within specific procedures:

### Top toolbar

The top toolbar above the canvas is the same for both display and video templates.

| Control | Description |
| --- | --- |
| Template name | The current template name, shown at the top of the editor. Click the **[!UICONTROL Edit name]** icon next to the name to rename it inline. |
| **[!UICONTROL Save]** | Saves and publishes the template. |
| **[!UICONTROL ...]** > **[!UICONTROL Save As Draft]** | Saves the template as a draft without publishing. Enter or update the name, select the advertiser, optionally add tags, and click **[!UICONTROL Save]**. |
| **[!UICONTROL ...]** > **[!UICONTROL Download]** | Downloads the current template as a ZIP file. |
| **[!UICONTROL Cancel]** | Discards unsaved changes and returns to the Templates list. |

-->

### 一般アクションツールバー

一般アクションツールバーは、広告テンプレートエディターの編集キャンバスの上に配置され、2つの部分（左と右）に分割されます。

#### ディスプレイ広告テンプレート

| 制御 | 説明 |
| --- | --- |
| **[!UICONTROL Undo]** | 最後のアクションを取り消します。 |
| ![やり直し](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 最後の取り消しアクションをやり直します。 |
| **[!UICONTROL Links]** | テンプレート内の要素に添付されたクリックスルーURLを管理するパネルを開きます。 |
| ズームコントロール | 「**[!UICONTROL Zoom out]**」または「**[!UICONTROL Zoom in]**」をクリックして、カンバスの倍率を調整します（10% ～ 150%、10%単位）。 ズームレベルのラベル（キャンバスが自動的にフィットする場合は&#x200B;**[!UICONTROL Auto]**、手動で設定する場合は割合）をクリックして、オプションのメニューを開きます（**[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**、および&#x200B;**[!UICONTROL Zoom Out]**）。 |
| 広告サイズ | 現在の広告ディメンションを表示します（例：300 × 250）。 クリックしてサイズピッカーを開きます。このサイズピッカーには、一般的に使用される6つのIAB標準サイズがカードとして表示され、さらに19の標準IAB ディスプレイ広告サイズすべてを含むドロップダウンが表示されます。 新しいテンプレートのデフォルトサイズは300 × 250 （Medium Rectangle）です。 |
| ![ レイヤーパネルを開く](/help/creative/assets/layers-panel-open.png " レイヤーパネルを開く") | [!UICONTROL Layers] パネルを開きます。 [!UICONTROL Layers] パネルを閉じた場合にのみ表示されます。 |

#### ビデオ広告テンプレート

| 制御 | 説明 |
| --- | --- |
| **[!UICONTROL Undo]** / ![やり直し](/help/creative/assets/cs-icon-redo.png) **[!UICONTROL Redo]** | 最後のアクションを取り消すか、やり直します。 |
| ズームコントロール | **[!UICONTROL Zoom out]**&#x200B;または&#x200B;**[!UICONTROL Zoom in]**&#x200B;をクリックして、キャンバスの倍率を調整します。 ズームレベルをクリックして、オプション **[!UICONTROL Auto-Fit Page]**、**[!UICONTROL 100% Zoom]**、**[!UICONTROL 50% Zoom]**、**[!UICONTROL Zoom In]**、**[!UICONTROL Zoom Out]**&#x200B;のメニューを開きます。 |
| ![ レイヤーパネルを開く](/help/creative/assets/layers-panel-open.png " レイヤーパネルを開く") | [!UICONTROL Layers] パネルを開きます。 [!UICONTROL Layers] パネルを閉じた場合にのみ表示されます。 |

<!-- Not there as of 7/10:  | **[!UICONTROL Preview]** | Opens a preview of the video template. | -->

### 左パネル

左側のパネルには、アイコンの列が表示されます。 アイコンをクリックしてコンテンツパネルを開き、同じアイコンをもう一度クリックして閉じます。

#### ディスプレイ広告テンプレート

| アイコン | 説明 |
| --- | --- |
| **[!UICONTROL Search]** | ライブラリ内のすべてのアセットタイプを検索します。 |
| **[!UICONTROL Upload]** | 画像<!-- not there as of 7/10:  or font files (TTF, OTF, WOFF, WOFF2)-->をエディターにアップロードして、現在のテンプレートで使用します。 一度に最大20個のファイルをアップロードできます。 |
| **[!UICONTROL Templates]** | Creative Studio ライブラリから広告テンプレートを参照し、ベースレイヤーや参照要素として使用できます。 |
| **[!UICONTROL My Assets]** | Creative Studioの「Assets」タブにアップロードしたすべてのアセットを参照します。 |
| **[!UICONTROL Images]** | Creative Studioの「Assets」タブにアップロードした画像アセットのみを参照します。 |
| **[!UICONTROL Text]** | アップロードしたカスタムフォントを含むテキスト要素をカンバスに追加します。 |
| **[!UICONTROL Elements]** | ボタンや長方形などのシェイプやレイアウト要素を追加します。 |

任意のパネルからカンバスにアイテムを直接ドラッグするか、クリックしてデフォルトの位置に配置できます。

#### ビデオ広告テンプレート

| アイコン | 説明 |
| --- | --- |
| **[!UICONTROL Search]** | ライブラリ内のすべてのアセットタイプを検索します。 |
| **[!UICONTROL Upload]** | 画像、ビデオ、オーディオまたはフォントファイル（TTF、OTF、WOFF、WOFF2）をエディターにアップロードして、現在のテンプレートで使用します。 一度に最大20個のファイルをアップロードできます。 |
| **[!UICONTROL Templates]** | Creative Studio ライブラリから広告テンプレートを参照します。 |
| **[!UICONTROL My Assets]** | Creative Studioの「Assets」タブにアップロードしたすべてのアセットを参照します。 |
| **[!UICONTROL Images]** | Creative Studioの「Assets」タブにアップロードした画像アセットのみを参照します。 |
| **[!UICONTROL Video]** | Creative Studioの「Assets」タブにアップロードしたビデオアセットのみを参照します。 |
| **[!UICONTROL Audio]** | 「Creative Studio Assets」タブにアップロードしたオーディオアセットのみを参照します。 |
| **[!UICONTROL Text]** | アップロードしたカスタムフォントを含むテキスト要素をカンバスに追加します。 |
| **[!UICONTROL Elements]** | シェイプとベクター要素を追加します。 |

任意のパネルからカンバスにアイテムを直接ドラッグするか、クリックしてデフォルトの位置に配置できます。

### 広告テンプレート編集コントロール

編集キャンバス上の要素をクリックして選択します。 テンプレートタイプに応じて、1つまたは複数のツールバーが、その要素のコントロールとともに表示されます。

#### インスペクターツールバーとパネル

コントロールはエレメントのタイプによって異なります。

<!-- From inspectorbar.ts -->

##### ディスプレイ広告テンプレート

| 制御 | エレメントタイプ | 説明 |
| --- | --- | --- |
| **[!UICONTROL Properties]** | すべて | パネルを開いてレイヤー名を編集し、レイヤーを動的（広告生成時にスワップ可能）としてマークし、クリックスルーURLを設定します（リンクのみ）。 その下で、**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**、または&#x200B;**[!UICONTROL Focus]**&#x200B;状態を選択して、そのインタラクション状態の要素のスタイルを設定し、タイポグラフィ（テキストとリンクのみ）、デコレーション（塗り、境界線、コーナーの半径）、寸法、位置のスタイルを要素タイプに基づいて調整します。 |
| **[!UICONTROL Effects]** | すべて | パネルを開き、**[!UICONTROL Default]**、**[!UICONTROL Hover]**、**[!UICONTROL Click]**、または&#x200B;**[!UICONTROL Focus]**&#x200B;状態を選択して、そのインタラクション状態にエフェクトを適用し、**[!UICONTROL Transform]**、**[!UICONTROL Transition]**、**[!UICONTROL Box Shadow]**、**[!UICONTROL Filter]**、**[!UICONTROL Blend Mode]**、および&#x200B;**[!UICONTROL Cursor]**&#x200B;のセクションを調整します。 テキスト要素には&#x200B;**[!UICONTROL Text Shadow]** セクションも含まれます。 |
| **[!UICONTROL Animations]** | すべて | パネルを開いて、タイムライン上でのレイヤーの開始時間と終了時間を設定し、デュレーションとイージングを使用して&#x200B;**[!UICONTROL Entrance Animation]**、**[!UICONTROL Loop Animation]**、**[!UICONTROL Exit Animation]**&#x200B;のプリセットを設定します。 **[!UICONTROL Copy]**、**[!UICONTROL Paste]**&#x200B;および&#x200B;**[!UICONTROL Reset]**&#x200B;個のアクションが含まれます。 |
| **[!UICONTROL Crop]** | 画像 | 画像を切り抜くためのツールバーを開きます。 **[!UICONTROL Aspect Ratio]** プリセット （または&#x200B;**[!UICONTROL Free]**）を選択し、**[!UICONTROL Apply]**&#x200B;または&#x200B;**[!UICONTROL Cancel]**&#x200B;をクリックします。 |
| **[!UICONTROL Position]** | すべて | **[!UICONTROL Move]**&#x200B;個のオプション （**[!UICONTROL Forward]**、**[!UICONTROL Backward]**、**[!UICONTROL To front]**、**[!UICONTROL To back]**）、**[!UICONTROL Align to Page]**&#x200B;個のオプション （**[!UICONTROL Top]**、**[!UICONTROL Left]**、**[!UICONTROL Middle]**、**[!UICONTROL Center]**、**[!UICONTROL Bottom]**、**[!UICONTROL Right]**、**[!UICONTROL Fit Vertically]**、**[!UICONTROL Fit Horizontally]**、**[!UICONTROL Fit to Page]**）および画像以外の要素の場合は&#x200B;**[!UICONTROL Layer Level Alignment]**&#x200B;個のオプション （同じ6個の整列オプション、および&#x200B;**[!UICONTROL Fit to Content]**）を含むメニューを開きます。 |

##### ビデオ広告テンプレート

| 制御 | エレメントタイプ | 説明 |
| --- | --- | --- |
| **[!UICONTROL Shape]** | シェイプ | シェイプ固有のオプションを設定します。 |
| **[!UICONTROL Group]** / **[!UICONTROL Ungroup]** | 複数の選択された要素、またはグループ | 選択した要素をグループ化したり、選択したグループをグループ解除したりします。 |
| **[!UICONTROL Combine]** | 互換性のあるシェイプ | 選択したシェイプを1つのシェイプに結合します。 |
| **[!UICONTROL Audio replace]** | オーディオとビデオ | オーディオトラックをアセットライブラリのファイルに置き換えます。 |
| **[!UICONTROL Typeface]**, **[!UICONTROL Bold]**, **[!UICONTROL Italic]**, **[!UICONTROL Font size]**, **[!UICONTROL Align horizontal]**, **[!UICONTROL Advanced]** | テキスト | フォントファミリー、太さ、サイズ、水平方向の整列、その他の高度なタイポグラフィ設定を調整します。 |
| **[!UICONTROL Image]** / **[!UICONTROL Video]** | 画像とビデオ | エレメントの塗りつぶし画像またはビデオソースを設定します。 |
| **[!UICONTROL Trim]** | ビデオとオーディオ | トリミングモードを開いて、クリップの開始点と終了点を設定します。 |
| ![ ボリューム ](/help/creative/assets/volume.png " ボリューム ") （[!UICONTROL Volume]） | ビデオとオーディオ | オーディオレベルを調整します。 |
| ![再生速度](/help/creative/assets/speed.png "再生速度") （[!UICONTROL Playback speed]） | ビデオとオーディオ | 再生率を調整します。 |
| ![切り抜き](/help/creative/assets/crop.png "切り抜き") （[!UICONTROL Crop]） | すべて | 要素をカスタム領域に切り抜きます。 |
| ![線](/help/creative/assets/stroke.png "線") （[!UICONTROL Stroke]） | すべて | 境界線の色と幅を設定します。 |
| **[!UICONTROL Text Background]** | テキスト | テキストの背景に背景色を追加します。 |
| **[!UICONTROL Animations]** | すべて | エントリ、終了、ループのアニメーションを追加または編集します。 |
| **[!UICONTROL Style]** | すべて | **[!UICONTROL Adjustments]**、**[!UICONTROL Filter]**、**[!UICONTROL Effect]**、**[!UICONTROL Blur]**&#x200B;のオプションを含むメニューを開きます。 |
| **[!UICONTROL Shadow]** | すべて | ドロップシャドウを追加または編集します。 |
| **[!UICONTROL Opacity]** | すべて | エレメントの透明度レベルを設定します。 |
| **[!UICONTROL Position]** | すべて | エレメントのサイズ、位置、回転を数値で調整します。 |

#### 一般的な編集コントロール

##### ディスプレイ広告テンプレート

| アクション | 説明 |
| --- | --- |
| **[!UICONTROL Replace]** | （画像エレメントのみ）画像パネルが開き、画像をアセットライブラリの画像に置き換えることができます。 |
| ![前進](/help/creative/assets/cs-icon-move-forward.png) **[!UICONTROL Move forward]** | エレメントを積み重ね順に一歩進めます（前面に向かって）。 |
| ![前へ移動](/help/creative/assets/cs-icon-move-backward.png) **[!UICONTROL Move backward]** | エレメントを積み重ね順に1段階後方（後ろ向き）に移動します。 |
| ![重複](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate]** | 要素のコピーを作成します。 |
| ![削除](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete]** | カンバスから要素を削除します。 |

選択したエレメントをドラッグして位置を変更し、その周りにハンドルをドラッグしてサイズを変更することもできます。

##### ビデオ広告テンプレート

| アクション | 説明 |
| --- | --- |
| **[!UICONTROL Edit text]** | （テキスト要素のみ）テキスト編集モードに切り替えて、キャンバス上で直接テキストを入力して書式設定できます。 テキスト編集モードでは、セカンダリメニューに&#x200B;**[!UICONTROL Text color]**、**[!UICONTROL Bold]**、**[!UICONTROL Italic]**&#x200B;および&#x200B;**[!UICONTROL Text variables]** （テンプレートプレースホルダー）が表示されます。 |
| **[!UICONTROL Replace]** | （画像エレメントのみ）アセットライブラリが開き、画像を入れ替えることができます。 |
| **[!UICONTROL Bring forward]** | エレメントを積み重ね順に1歩進めます。 |
| **[!UICONTROL Send backward]** | エレメントを積み重ね順に1つ下に移動します。 |
| **[!UICONTROL Duplicate]** | 要素のコピーを作成します。 |
| **[!UICONTROL Delete]** | カンバスから要素を削除します。 |
| **... >[!UICONTROL Flip horizontal]** | エレメントを水平方向に180度反転します。 |
| **... >[!UICONTROL Flip vertical]** | エレメントを垂直方向に180度反転します。 |
| **... >[!UICONTROL Copy Element]** | 要素をカンバスクリップボードにコピーします。 |
| **... >[!UICONTROL Pastes Element]** | コピーしたエレメントをペーストします。 |

選択したエレメントをドラッグして位置を変更し、その周りにハンドルをドラッグしてサイズを変更することもできます。

### タイムライン

ディスプレイエディターとビデオエディターの両方で、カンバスの下部にタイムラインパネルが表示されます。

#### ディスプレイ広告テンプレート

タイムラインには、カンバス上の各レイヤーのトラックが表示されます。このトラックは、レイヤーが表示される時間範囲にまたがり、レイヤーの出入りのアニメーションタイミングに基づいて表示されます。 トラックの開始ハンドルまたは終了ハンドルをドラッグして入力または終了時間を調整するか、トラックをドラッグしてレイヤーを並べ替えます。 定規をクリックするか、再生ヘッドをドラッグして、ある時点に移動します。

タイムラインツールバーには、**[!UICONTROL Duration]** フィールド （0 ～ 60秒）、**[!UICONTROL Play]**/**[!UICONTROL Pause]**、現在の時間/合計時間表示、ループトグル、**[!UICONTROL Timeline Scale]** ズームコントロール、**[!UICONTROL Fit View]** ボタン、折りたたみ/展開トグルが含まれます。

#### ビデオ広告テンプレート

タイムラインには、テンプレート内のすべてのビデオクリップとオーディオクリップが表示されます。 タイムラインを使用して、クリップが時間内にどのように配置されているかを確認し、開始ハンドルと終了ハンドルをドラッグしてクリップをトリミングします。 タイムライン上に新しいクリップを直接追加することはできません。代わりに左側のパネルまたはキャンバスから追加すると、タイムライン上にクリップとして表示されます。

### [!UICONTROL Layers] パネル

キャンバスの右側にある[!UICONTROL Layers] パネルには、テンプレート内のすべての要素が一覧表示され、その順序、表示、およびプロパティを管理できます。 表示テンプレートの場合は、カンバスツールバーの「**[!UICONTROL Open Layers]**」をクリックして開きます。 ビデオテンプレートの場合、パネルはデフォルトで開きます。

任意のレイヤーをクリックして、カンバス上の対応する要素を選択します。

**タブ（ディスプレイ広告テンプレートのみ）**

表示テンプレートには、[!UICONTROL Layers] パネルの上部に2つのタブがあります。

* **[!UICONTROL Dynamic]** — AI エージェントが置き換えることができる画像やテキストなど、広告生成中にスワップできるレイヤーのみを一覧表示します。 これは、広告バリエーションを生成するためのデフォルトのビューです。
* **[!UICONTROL All]** – 構造コンテナを含む、テンプレートの完全なレイヤー階層を表示します。 このビューを使用すると、エレメントのネスト方法を調べたり整理したりできます。

ビデオテンプレートでは、タブを持たない単一のリストにすべてのレイヤーが表示されます。

**レイヤーごとのアクション**

レイヤーの上にカーソルを置くと、次のアクションが表示されます。

| アクション | 説明 |
| --- | --- |
| ![ レイヤー名を変更](/help/creative/assets/edit.png) **[!UICONTROL Rename layer]** | パネルに新しいレイヤー名を入力できます。 |
| ![ レイヤーをロック ](/help/creative/assets/cs-icon-lock.png) **[!UICONTROL Lock layer]** / ![ レイヤーをロック解除](/help/creative/assets/cs-icon-unlock.png) **[!UICONTROL Unlock layer]** | レイヤーの移動、編集、並べ替えを防止または許可します。 |
| ![ レイヤーを非表示](/help/creative/assets/cs-icon-hidden.png) **[!UICONTROL Hide layer]** / ![ レイヤーを表示](/help/creative/assets/cs-icon-visible.png) **[!UICONTROL Show layer]** | カンバス上のレイヤーを表示または非表示にします。 非表示のレイヤーはテンプレート内に保持されますが、テンプレートのレンダリング時には表示されません。 |
| ![ ドラッグして並べ替え](/help/creative/assets/cs-icon-drag.png) ドラッグして並べ替え | （広告テンプレートの表示のみ）並べ替えアイコンをドラッグして、レイヤーの重なり順の位置を変更します。 レイヤーをロック解除して並べ替える必要があります。 |

**パネルフッター**

| アクション | 説明 |
| --- | --- |
| ![選択したレイヤーを複製](/help/creative/assets/cs-icon-duplicate.png) **[!UICONTROL Duplicate selected layer]** | 選択したレイヤーのコピーを作成します。 |
| ![選択したレイヤーを削除](/help/creative/assets/cs-icon-delete.png) **[!UICONTROL Delete selected layer]** | 選択したレイヤーを削除します。 |
| **[!UICONTROL Group selected layers]** （ビデオテンプレートのみ） | 選択した2つ以上のレイヤーを1つのグループにグループ化します。 2つ以上のレイヤーが選択されている場合にのみ表示されます。 グループ化されたレイヤーをグループ解除したり、グループ行のコントロールを使用してグループから個々のレイヤーを削除したりできます。 |

<!--

These are all saved with the template, but they aren't what you see, as-is, in the template settings per se. Rethink if I should include this, and how to frame it:

## Template settings {#template-settings}

### Display ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Type]** | (Required) The HTML5 template type: **[!UICONTROL Static HTML5]** or **[!UICONTROL Dynamic HTML]**. |
| **[!UICONTROL Size]** | (Required) The ad dimensions. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **[!UICONTROL Tags]** | (Optional) One or more labels. Click **[!UICONTROL Add More]** to add additional tags. |
| **ZIP file** | The HTML5 creative ZIP file. For **[!UICONTROL Dynamic HTML]** templates, also upload the template data file (TDF). |

### Video ad template settings

| Setting | Description |
| --- | --- |
| **[!UICONTROL Advertiser]** | (Required) The advertiser this template belongs to. |
| **[!UICONTROL Ad Template Name]** | (Required) A unique name for the template. |
| **[!UICONTROL Description]** | (Optional) A description of the template. |
| **ZIP file** | The video ad template ZIP file. |

-->

## ディスプレイ広告テンプレートからの広告バリエーションの生成 {#ad-variations-generate}

*広告テンプレートのみを表示します。*

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードまたはテーブルの行にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**&#x200B;をクリックします。

   テンプレートが事前に読み込まれた状態で[!UICONTROL Ad Variations Generator]が開きます。

1. AI チャットインターフェイスを使用して、広告コンテンツを生成、調整します。 ワークフローの詳細については、「[Creative Studioで標準広告を管理](creative-studio-manage-standard-ads.md)」を参照してください。

## 広告テンプレートのラベルの追加または削除 {#template-labels}

*広告テンプレートのみを表示します。*

ラベルは、ユーザーテンプレートの整理とフィルタリングに役立ちます。 システムテンプレートにラベルを追加することはできません。

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードまたはテーブルの行にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit Labels]**&#x200B;をクリックします。

1. **[!UICONTROL Edit Labels]** ダイアログで、次の操作を行います。

   * ラベルを追加するには、既存のラベルを選択するか、入力フィールドに名前を入力して、**[!UICONTROL Add Tag]**&#x200B;をクリックします。

   * ラベルを削除するには、ラベルタグの横にある「**[!UICONTROL X]**」をクリックします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 広告テンプレートのプレビュー {#template-preview}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードの上にカーソルを置きます。

1. 次のいずれかの操作を行います。

   * （カード表示） **[!UICONTROL Preview template]** アイコンをクリックするか、**[!UICONTROL ...]** > **[!UICONTROL Preview]**&#x200B;をクリックします。

   * （テーブルビュー）「**[!UICONTROL ...]** > **[!UICONTROL Preview]**」をクリックします。

1. ビデオテンプレートの場合は、![再生](/help/creative/assets/play.png "再生")をクリックします。

## 広告テンプレートのダウンロード {#template-download}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードまたはテーブルの行にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Download]**&#x200B;をクリックします。

   テンプレートは、ブラウザーの通常の手順に従ってZIP ファイルとしてダウンロードされます。

## 広告テンプレートをお気に入りとして追加または削除 {#template-favorite}

*カード表示のみ*

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードの上にカーソルを置きます。

1. 次のいずれかの操作を行います。

   * テンプレートをお気に入りとして追加するには、![お気に入り](/help/creative/assets/favorite-null.png)をクリックします。

   * テンプレートをお気に入りとして削除するには、![お気に入り](/help/creative/assets/favorite.png)をクリックします。

## 広告テンプレートの削除 {#template-delete}

1. メインメニューで、**[!UICONTROL Creative Studio].**&#x200B;をクリックします

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. テンプレートカードまたはテーブルの行にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising CreativeのCreative Studioについて](creative-studio-about.md)
>* [Creative Studioでアセットを管理](creative-studio-manage-assets.md)
>* [Creative Studioで標準広告を管理](creative-studio-manage-standard-ads.md)
>* [Creative Studioで動的なクリエイティブを管理](creative-studio-manage-dynamic-ads.md)
