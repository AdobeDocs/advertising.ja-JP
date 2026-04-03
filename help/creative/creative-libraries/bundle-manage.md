---
title: クリエイティブバンドルの管理
description: クリエイティブグループの管理と使用方法について説明します。
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
TQID: https://experienceleague.adobe.com/hat5puvy5qIpBrShro3QpZoqt2kkd4nnmi4zT7G9Vfg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1587
ht-degree: 0%

---

# クリエイティブバンドルの管理

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

バンドルとは、1つのユニットとしてエクスペリエンスに追加できるクリエイターのグループです。 バンドルコンテナを作成した後、クリエイティブをバンドルに添付できます。 標準ディスプレイバンドルには標準ディスプレイ広告のみを含めることができ、標準ビデオバンドルには標準ビデオ広告のみを含めることができます。動的ディスプレイバンドルには動的ディスプレイ広告のみを含めることができます。動的ビデオバンドルには動的ビデオ広告のみを含めることができます。 エクスペリエンスの決定ツリー内からエクスペリエンスに割り当てられているバンドル内のすべてのクリエイターのランディングページ、インプレッション追跡タグ、クリック追跡タグを、ベースとなるクリエイターに影響を与えることなく上書きできます。

[!DNL Creative]は、バンドルが割り当てられている各エクスペリエンスに対して指定されたとおりに、バンドル内のクリエイターを経由して回転します。 オプションで、[!DNL Creative]が[!DNL Adobe AI]を利用したアルゴリズム広告のローテーションを使用して、パフォーマンスに基づいて任意のエクスペリエンスの広告要素を最適化することを許可できます。

広告エクスペリエンスのバンドル全体で広告要素の最適化を有効にするには、各バンドルに各\[ クリエイティブサイズまたは期間+言語\]の組み合わせのいずれかを1つだけ含めることができます。 例えば、バンドルに250 x 250のクリエイティブが1つ含まれ、デフォルト言語が「フランス語」の場合、2つ目の250 x 250のクリエイティブをデフォルト言語「フランス語」で追加することはできません。 同じサイズのクリエイターが同じ言語に複数いる場合は、それらを個別にエクスペリエンスに追加します。

バンドルに添付されているクリエイターは、個々のクリエイターとして引き続き使用できます。 1つのクリエイティブを複数のバンドルに追加できます。 バンドルに添付されているクリエイティブの設定を編集すると、変更がバンドルに反映されます。 ただし、エクスペリエンス内のクリエイティブに設定されたカスタムランディングページ、インプレッション追跡タグ、クリックトラッキングタグは、常にエクスペリエンスに使用されます。

<!-- multiselect only to duplicate and delete -->

## クリエイティブライブラリ用のバンドルの作成

複数のバンドルにクリエイティブを添付できます。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]** > **[!UICONTROL Bundles]** > **[!UICONTROL Bundle]**&#x200B;をクリックします。

1. 一意の&#x200B;**[!UICONTROL Bundle Name]**&#x200B;と&#x200B;**[!UICONTROL Bundle Type]:** *標準ディスプレイ* （標準ディスプレイクリエイティブの場合）、*動的ディスプレイ* （動的ディスプレイクリエイティブの場合）、*標準ビデオ* （標準ビデオクリエイティブの場合）、または&#x200B;*Dynamic Video* （動的ビデオクリエイティブの場合）を入力します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## バンドル内のクリエイティブのリスト

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックして、バンドル内のすべてのクリエイターを表示します。

## 重複したバンドル

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 複製するバンドルを選択します。

   * 1つのバンドルを複製するには：

      * カード表示で、バンドル名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

   * 1つまたは複数のバンドルを複製するには、複製する各バンドルのチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Duplicate].**&#x200B;をクリックします

     すべての行を選択するには、左上の「グローバル」チェックボックスをオンにします。

   新しいバンドルの名前は`<original name> (copy) # 1` （またはシーケンス内の次の番号）です。 例えば、「テストバンドル」の2つの複製を作成する場合、複製の名前は「テストバンドル（コピー）#1」と「テストバンドル（コピー）#2」になります。

## バンドル名の編集

バンドル名の変更は、関連するすべてのエクスペリエンスに反映されます。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、ライブラリ名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Edit]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Bundle Name]**&#x200B;を編集します。

   [!UICONTROL Bundle Name]は一意である必要があります。

1. **[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->をクリックします

## バンドルへのクリエイティブの添付

既存の標準ディスプレイクリエイティブを標準ディスプレイバンドルに、標準ビデオクリエイティブを標準ビデオバンドルに、動的ディスプレイクリエイティブを動的バンドルに、動的ビデオクリエイティブをビデオバンドルに添付できます。 クリエイティブをバンドルにアタッチすると、そのクリエイティブは、バンドルが割り当てられているすべてのエクスペリエンスで使用できるようになります。 各バンドルには、各\[ クリエイティブサイズまたはデュレーション+言語\]の組み合わせのいずれかを1つだけ含めることができます。

>[!NOTE]
>
>標準広告および動的広告ビュー[からクリエイティブをバンドルに](creative-attach-detach-bundles.md)添付することもできます。

### バンドルリストからバンドルへのクリエイティブの添付

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、バンドル名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Attach Creatives]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Attach Creatives]**&#x200B;をクリックします。

   バンドルタイプの対象となる各クリエイティブは、右側のフレームに一覧表示されます。 バンドルに既に添付されているクリエイターはリストに表示されますが、選択できません。

1. （オプション） ![&#x200B; カード表示](/help/creative/assets/card-view-button.png " カード表示")をクリックしてカード表示を開くか、![表/リスト表示](/help/creative/assets/table-view-button.png "テーブルビュー")をクリックしてテーブル表示に戻すことで、デフォルトのテーブルビューと使用可能なバンドルのカード表示を切り替えます。

1. 右側のフレームで、バンドルに添付する各クリエイティブの横にあるチェックボックスをオンにし、**[!UICONTROL Attach Creative to Bundle]**&#x200B;をクリックします。

### バンドルのクリエイティブリストからバンドルへのクリエイティブの添付

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックして、バンドル内のすべてのクリエイターを表示します。

1. 右上の「**[!UICONTROL Attach Creatives]**」をクリックします。

1. 右側のパネルで、アタッチする各クリエイティブのチェックボックスをオンにします。

1. **[!UICONTROL Attach Creatives to Bundle]**&#x200B;をクリックします。

## バンドルからのクリエイティブの分離 {#bundle-detach-creatives}

クリエイティブをバンドルから分離すると、2つのクリエイティブ間の関連付けが削除されるため、クリエイティブはバンドルをターゲットとするエクスペリエンスに使用されなくなります。

バンドルからクリエイティブを分離しても、クリエイティブライブラリの「クリエイティブ」タブからクリエイティブが削除されることはありません。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックして、バンドル内のすべてのクリエイターを表示します。

1. バンドルから分離するクリエイティブを選択します。

   * 単一のクリエイティブを切り離すには：

      * カード表示で、クリエイティブ名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Detach]**&#x200B;をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Detach]**&#x200B;をクリックします。

   * 1人以上のクリエイティブを分離するには、分離する各クリエイティブのチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Detach]**&#x200B;をクリックします。

     すべての行を選択するには、左上の「グローバル」チェックボックスをオンにします。

## バンドル内の単一のクリエイティブのプレビュー

ハイパーリンクを含むクリエイティブは、ビューアに表示されるので、プレビューできます。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックして、バンドル内のすべてのクリエイターを表示します。

1. クリエイティブを選択します。

   * カード表示で、クリエイティブ名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Preview]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Preview]**&#x200B;をクリックします。

1. （オプション）画面内の画像のサイズを変更するには、**[!UICONTROL Zoom]** リストで、画像サイズの10%から100%のオプションを選択します。

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. （オプション）クリエイティブのランディングページを開くには、クリエイティブをクリックします。

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （オプション）クリエイティブをダウンロードするには、![&#x200B; ダウンロード &#x200B;](/help/creative/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## バンドル内のすべてのクリエイティブのプレビュー

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、バンドル名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Preview]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Preview]**&#x200B;をクリックします。

1. （オプション）言語でクリエイターをフィルタリングするには、**[!UICONTROL Language]** リストでオプションを選択し、プレビューの右上にある&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。

1. （オプション）クリエイターをサイズでフィルタリングするには、**[!UICONTROL Size]** リストでオプションを選択し、プレビューの右上にある&#x200B;**[!UICONTROL Preview]**&#x200B;をクリックします。

1. （オプション）画面内の画像のサイズを変更するには、**[!UICONTROL Zoom]** リストで、画像サイズの10%から100%のオプションを選択します。

1. （オプション）クリエイティブのランディングページを開くには、クリエイティブをクリックします。

<!-- Verify:  Will the creative click be tracked like a regular ad click but not linked to a publisher and placement? Explain effect/consequences. -->

1. （オプション）デモ URLを共有して、[!DNL Creative]にログインしていない他のユーザーがクリエイティブをプレビューできるようにするには、次の手順を実行します。

   1. プレビューの右上にある「![共有](/help/creative/assets/share.png "共有")」をクリックします。

   1. [!UICONTROL Share Demo URL] ダイアログで、**[!UICONTROL Copy]**&#x200B;をクリックしてURLをクリップボードにコピーし、他のユーザーと共有できるようにします。

<!--
 Not there as of 1/22/25:

## Edit the landing page and tracking tags for the creatives in a standard creative bundle

*Standard creative bundles only*

[Verify and edit all this, including the command names and where they're available. This is supposed to be a single and bulk action from within the right frame when you've open bundle details for a single bundle -- not from the Bundles table view.]

This procedure customizes the landing page, impression-tracking tags, and click-tracking tags for the creatives only within the context of the bundle. It doesn't change the settings for the base creative in [!UICONTROL Creative Libraries].

The custom URL and tags are applied to a creative when the bundle is assigned to an experience and the creative is served for the experience.

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. (Optional) [Customize the view](/help/creative/introduction/customize-data-views.md) to include specific libraries.

1. Click the library name.

1. Click the **[!UICONTROL Bundles]** tab.

1. Click the bundle name.

1. In the right pane, XXXXXXXXXXXX.

1. 

1. Edit any of the following settings: **[!UICONTROL Landing Page]**, **[!UICONTROL Click Tags]**, **[!UICONTROL Impression Tags]**.[Verify, and is can you do this for only one creative or is multiselect available?]

1.

 -->

## バンドルの変更ログの表示

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、バンドル名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Change Log]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]** > **[!UICONTROL Change Log]**&#x200B;をクリックします。

1. （オプション）報告される時間範囲を変更します。

1. （オプション）メモを追加するには、行の上にカーソルを置いて「**[!UICONTROL Add Notes]**」をクリックします。 メモを入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

1. （オプション）追加されたメモを含む変更ログエントリを表示するには、行の上にカーソルを置いて「**[!UICONTROL View Details]**」をクリックします。

## バンドルの削除

[live](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses) エクスペリエンスに割り当てられていないバンドルを削除できます。 バンドルがライブエクスペリエンスに割り当てられている場合は、続行する前に、そのバンドルを決定ツリー[から削除してください。](/help/creative/experiences/experience-target-node-delete.md)

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. （オプション） [特定のライブラリを含めるようにビュー](/help/creative/introduction/customize-data-views.md)をカスタマイズします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 削除するバンドルを選択します。

   * 単一のバンドルを削除するには：

      * カード表示で、バンドル名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Delete]**&#x200B;をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Delete]**&#x200B;をクリックします。

   * 1つまたは複数のバンドルを削除するには、削除する各バンドルのチェックボックスをオンにします。 一括操作ツールバーで、**[!UICONTROL Delete].**&#x200B;をクリックします

     すべての行を選択するには、左上の「グローバル」チェックボックスをオンにします。

1. 確認メッセージで、**[!UICONTROL Delete].**&#x200B;をクリックします

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [&#x200B; エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [&#x200B; クリエイティブをプレビュー](/help/creative/creative-libraries/creative-preview.md)
>* [標準クリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-standard.md)
>* [&#x200B; クリエイティブライブラリの管理](/help/creative/creative-libraries/creative-library-manage.md)
>* [&#x200B; クリエイティブライブラリについて](/help/creative/creative-libraries/creative-libraries-about.md)
