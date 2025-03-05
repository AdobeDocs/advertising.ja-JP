---
title: クリエイティブバンドルの管理
description: xxxx について説明します。
feature: Creative Bundles
exl-id: a9ed4e8f-db93-46d5-9231-2b3bb0aa072a
source-git-commit: 97e0f562153983202a2f3641e17dd682ff3d00ea
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%

---

# クリエイティブバンドルの管理

*クローズドベータ版*

<!--
**I'll probably split this up into multiple pages since the creative-related topics are separate**
-->

バンドルは、1 つのユニットとしてエクスペリエンスに追加できるクリエイティブのグループです。 バンドルコンテナを作成した後、バンドルにクリエイティブを添付できます。 標準バンドルには標準広告のみを含めることができ、動的バンドルには動的広告のみを含めることができます。 基本クリエイティブに影響を与えることなく、エクスペリエンスの決定ツリー内からエクスペリエンスに割り当てられたバンドル内のすべてのクリエイティブについて、ランディングページ、インプレッショントラッキングタグ、クリック追跡タグを上書きできます。

[!DNL Creative] は、バンドルが割り当てられている各エクスペリエンスに対して指定されたとおりに、バンドル内のクリエイティブを循環します。 オプションで、Adobe Senseiを活用し [!DNL Creative] アルゴリズム広告ローテーションを使用して、パフォーマンスに基づいて任意のエクスペリエンスの広告要素を最適化できるようにできます。

広告エクスペリエンス内のバンドル間で広告要素の最適化を有効にするために、各バンドルには各\[ クリエイティブサイズ +言語\] の組み合わせのいずれか 1 つのみを含めることができます。 例えば、バンドルにデフォルト言語が「フランス語」の 250 x 250 クリエイティブが 1 つ含まれている場合、デフォルト言語が「フランス語」の 250 x 250 クリエイティブを 2 つ追加することはできません。 同じ言語に同じサイズの複数のクリエイティブがある場合は、エクスペリエンスに別々に追加します。

バンドルに添付されたクリエイティブは、引き続き個々のクリエイティブとして使用できます。 1 つのクリエイティブを複数のバンドルに追加できます。 バンドルにアタッチされているクリエイティブの設定を編集すると、変更内容がバンドルに反映されます。 ただし、エクスペリエンス内のクリエイティブに設定されたカスタムランディングページ、インプレッショントラッキングタグ、クリック追跡タグは、常にエクスペリエンスに使用されます。

<!-- multiselect only to duplicate and delete -->

## クリエイティブライブラリ用のバンドルを作成します

1 つのクリエイティブを複数のバンドルに添付できます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 右上で、**[!UICONTROL Create]**/**[!UICONTROL Bundles]**/**[!UICONTROL Bundle]** をクリックします。

1. 一意の **[!UICONTROL Bundle Name]** を入力し、**[!UICONTROL Bundle Type]:** *標準* （標準クリエイティブの場合）または *動的* （ダイナミッククリエイティブの場合）を入力します。

1. 「**[!UICONTROL Create]**」をクリックします。

## バンドル内のクリエイティブのリスト

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックすると、バンドル内のすべてのクリエイティブが表示されます。

## 重複するバンドル

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 複製するバンドルを選択：

   * 単一のバンドルを複製するには：

      * カード表示で、バンドル名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Duplicate]**」をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Duplicate]** をクリックします。

   * 1 つ以上のバンドルを複製するには、複製する各バンドルのチェックボックスをオンにします。 一括アクションツールバーで、「**[!UICONTROL Duplicate].**」をクリックします。

     すべての行を選択するには、左上の「グローバル」チェック・ボックスを選択します。

   新しいバンドルには `<original name> (copy) # 1` という名前（またはシーケンス内の次の番号）が付けられます。 例えば、「Test bundle」の重複を 2 つ作成した場合、その重複の名前は「Test bundle （copy） # 1」および「Test bundle （copy） # 2」になります。

## バンドル名を編集

バンドル名に対する変更は、関連するすべてのエクスペリエンスに反映されます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、ライブラリ名の横にある **[!UICONTROL ...]** をクリックし、[**[!UICONTROL Edit]**] をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Edit]** をクリックします。

1. **[!UICONTROL Bundle Name]** を編集します。

   [!UICONTROL Bundle Name] は一意である必要があります。

1. 「**[!UICONTROL Update]**.<!-- inconsistent with "Edit" for creative libraries and creatives -->」をクリックします。

## バンドルにクリエイティブを添付

[ 既存の標準クリエイティブ ](/help/creative/creative-libraries/creative-libraries-about.md) を標準バンドルに添付し、既存の動的クリエイティブ <!-- [existing dynamic creatives](creative-dynamic-manage.md) --> を動的バンドルに添付できます。 クリエイティブをバンドルに添付すると、バンドルが割り当てられているすべてのエクスペリエンスでクリエイティブが使用できるようになります。 各バンドルには、各\[creative size + language\] の組み合わせをそれぞれ 1 つだけ含めることができます。

<!--
>[!NOTE]
>
>You can also [attach creatives to bundles from the Standard Ads and Dynamic Ads views](creative-attach-detach-bundles.md).
-->

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルを選択します。

   * カード表示で、バンドル名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Attach Creatives]**」をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Attach Creatives]** をクリックします。

   バンドルタイプに適格な各クリエイティブが、右側のフレームに表示されます。 既にバンドルに添付されているクリエイティブが一覧表示されますが、選択することはできません。

1. 右側のフレームで、バンドルに添付する各クリエイティブの横にあるチェックボックスをオンにして、「**[!UICONTROL Attach Creative to Bundle]**」をクリックします。

## バンドルからクリエイティブを分離 {#bundle-detach-creatives}

バンドルからクリエイティブを分離すると、2 つの間の関連付けが削除され、バンドルをターゲットとするエクスペリエンスにクリエイティブは使用されなくなります。

バンドルからクリエイティブを分離しても、クリエイティブライブラリの「クリエイティブ」タブからクリエイティブが削除されるわけではありません。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックすると、バンドル内のすべてのクリエイティブが表示されます。

1. バンドルから分離するクリエイティブを選択します。

   * 1 つのクリエイティブを分離するには：

      * カード表示で、クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Detach]**」をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Detach]** をクリックします。

   * 1 つ以上のクリエイティブを分離するには、分離する各クリエイティブのチェックボックスを選択します。 一括アクションツールバーで、「**[!UICONTROL Detach]**」をクリックします。

     すべての行を選択するには、左上の「グローバル」チェック・ボックスを選択します。

## バンドル内のクリエイティブのプレビュー

ハイパーリンクを含むクリエイティブは、ビューアに表示されるとおりにプレビューできます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. バンドルカードまたは行をクリックすると、バンドル内のすべてのクリエイティブが表示されます。

1. クリエイティブを選択：

   * カード表示で、クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Preview]**」をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Preview]** をクリックします。

1. （オプション）画面内の画像のサイズを変更するには、画像リストで **[!UICONTROL Zoom]** 像サイズの 10～100% の範囲でオプションを選択します。

<!-- Not there as of 1/22/24:  1. (Flexible HTML5 creatives; optional) To show all frames for the creative, select **Show frames**. -->

1. （任意）クリエイティブをダウンロードするには、「![ ダウンロード ](/help/creative/assets/download.png " ダウンロード ")」をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。


<!-- Not there as of 1/22/25:

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

## バンドルを削除

[ ライブ ](/help/creative/experiences/experience-about.md#experience-statuses-experience-statuses) エクスペリエンスに割り当てられていないバンドルを削除できます。 バンドルがライブエクスペリエンスに割り当てられている場合は、続行する前に、エクスペリエンスの [ デシジョンツリーからバンドルを削除 ](/help/creative/experiences/experience-target-node-delete.md) します。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Bundles]**」タブをクリックします。

1. 削除するバンドルを選択：

   * 単一のバンドルを削除するには：

      * カード表示で、バンドル名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Delete]**」をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Delete]** をクリックします。

   * 1 つ以上のバンドルを削除するには、削除する各バンドルのチェックボックスを選択します。 一括アクションツールバーで、「**[!UICONTROL Delete].**」をクリックします。

     すべての行を選択するには、左上の「グローバル」チェック・ボックスを選択します。

1. 確認メッセージで、「**[!UICONTROL Delete].**」をクリックします。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [ エクスペリエンスの最終ノードへのクリエイティブバンドルの割り当てと割り当て解除 ](/help/creative/experiences/experience-assign-creative-bundles.md)
>* [ クリエイティブライブラリへの標準クリエイティブの追加 ](/help/creative/creative-libraries/creative-add-standard.md)
>* [ クリエイティブライブラリの管理 ](/help/creative/creative-libraries/creative-library-manage.md)
>* [ クリエイティブライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md)
