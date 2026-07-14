---
title: Creative Studioで動的なクリエイティブを管理する
description: Adobe Advertising Creative Studioで、カタログを活用した動的クリエイティブを構築、編集、複製、削除する方法を説明します。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1044
ht-degree: 0%

---

# [!UICONTROL Creative Studio]での動的クリエイティブの管理

*Beta機能*

[!UICONTROL Creative Studio]の「**[!UICONTROL Creatives]**」タブには、動的なクリエイターがライブラリ別に一覧表示されます。 ここから、新しいカタログ駆動型の動的クリエイティブを作成したり、既存のクリエイティブの詳細と属性マッピングを編集したり、変更ログを表示したり、クリエイティブを複製したり、クリエイティブを削除したりできます。

## ダイナミックなクリエイティブを作成 {#build-dynamic-creative}

このワークフローは、カタログ主導のダイナミックなクリエイティブを作成するために使用します。 4段階のガイド付きウィザードでは、テンプレートの選択、カタログの接続、カタログフィールドとテンプレート要素のマッピングについて説明します。 セットアップ後、[!UICONTROL AI Assistant]を使用すると、カタログデータから生成された各広告の組み合わせをプレビューおよび品質チェックできます。

動的なクリエイターは、標準的な広告とは大きく異なります。AI エージェントはカタログから提供されたコンテンツを変更できません。 問題のフィルタリング、分析、フラグ付けができますが、広告コンテンツを変更するには、ソースカタログを更新する必要があります。

### 前提条件

* テンプレートライブラリには、少なくとも1つのユーザー作成の表示広告テンプレート（システムテンプレートではない）が存在する必要があります。
* 商品またはコンテンツカタログ（フィード）がアカウントで利用できます。

### 手順1: [!UICONTROL Build Dynamic Creative] ウィザードを開く {#open-wizard}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Build dynamic creatives from catalog data]** クイックアクションカードの&#x200B;**[!UICONTROL Build]**&#x200B;をクリックします。

   4段階の&#x200B;**[!UICONTROL Build Dynamic Creative]** ダイアログが開きます。

### 手順2：テンプレートの選択 {#select-template}

>[!NOTE]
>
>テンプレートギャラリーには、作成した広告テンプレートのみが表示されます。 システムテンプレートと動画広告テンプレートは、動的なクリエイティブを生み出す出発点としては利用できません。

1. テンプレートギャラリーで、テンプレートをクリックして選択します。

   テンプレートが選択されるまで、**[!UICONTROL Next]** ボタンは無効になります。

1. **[!UICONTROL Use this template]**&#x200B;をクリックします。

### 手順3：カタログの選択 {#select-catalog}

1. クリエイティブ設定を行います。

   * **[!UICONTROL Ad Library]:** クリエイティブを保存するクリエイティブ ライブラリを選択します。
   * **[!UICONTROL Dynamic creative name]:**&#x200B;動的クリエイティブの名前を入力します。
   * **[!UICONTROL Number of cards]:**&#x200B;各広告の組み合わせに含めるカタログオファーの数を入力します（1 ～ 50）。
   * **[!UICONTROL Assign dynamic creative to a bundle]:** （オプション）有効にすると、保存されたクリエイターがバンドルに添付されます。 ライブラリからバンドルを選択します。

1. 1つ以上のカタログを選択：

   1. （オプション） **[!UICONTROL Catalog template]**&#x200B;を使用して、カタログリストを特定のテンプレートファミリーにフィルタリングします。 必要に応じてテンプレートファイルをダウンロードしてレビューするには、**[!UICONTROL Download feed template]**&#x200B;をクリックします。

   1. リストからカタログを検索して選択します。 選択したすべてのカタログは、同じカタログ テンプレート ファミリに属している必要があります。ファミリを混在させようとした場合は、警告が表示されます。

   1. （オプション）新しいカタログファイルをアップロードするには、ファイルをアップロード領域にドラッグ&amp;ドロップするか、**[!UICONTROL Browse Files]**&#x200B;をクリックします。 サポートされているフォーマット：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP、MP4。 最大ファイルサイズ：25 MB。 一度に1つのファイルをアップロードできます。 アップロードされたカタログは、**（アップロード済み）**&#x200B;というラベルの付いたチップリストに表示されます。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

### 手順4：カタログフィールドをテンプレート要素にマッピングする {#attribute-mapping}

各カタログフィールドをテンプレート内の対応する要素にマッピングします。 例えば、カタログの製品名フィールドをテンプレートの見出し要素にマッピングし、製品画像フィールドを背景画像要素にマッピングします。

1. **[!UICONTROL Targeting]**&#x200B;の下で、クリエイティブをパーソナライズするデータソースを少なくとも1つ選択してください：**[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**、または&#x200B;**[!UICONTROL Audience Segment]**。

1. 各テンプレート要素について、ドロップダウンから一致するカタログフィールドを選択します。

1. **[!UICONTROL Continue]**&#x200B;をクリックします。

### ステップ 5:AIを活用したプレビューとQA {#qa}

1. *[!UICONTROL Save Dynamic Creative & Skip QA]*&#x200B;にするか&#x200B;*[!UICONTROL Continue to QA]*&#x200B;にするかを選択します。

   QAを続行すると、キャンバスには、カタログから生成されたすべての広告の組み合わせが表示され、テンプレートでレンダリングされた各カタログエントリのプレビューが行として表示されます。

1. QAを続ける場合：

   1. 次のいずれかの操作を行います。

      * **[!UICONTROL Zoom in]**&#x200B;および&#x200B;**[!UICONTROL Zoom out]** コントロールを使用して、キャンバス表示を調整します。

      * ページネーション コントロール（**X-Y of Z**）を使用して、カタログ行をページ化します。

      * 広告の組み合わせを編集するには：

         1. カタログ行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

         1. **[!UICONTROL Edit Row]** ダイアログで、フィールド値を更新します。

         1. **[!UICONTROL Save]**&#x200B;をクリックします。

        カンバスが更新され、更新された値が反映されます。

      * **[!UICONTROL AI Assistant]** チャットパネルを使用して、カタログの組み合わせを分析およびフィルタリングします。 **[!UICONTROL Ask anything]** フィールドにリクエストを入力するか、提案されたプロンプトのいずれかをクリックします。

         * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
         * **[!UICONTROL Show me side-by-side comparisons of A/B testing creatives]**
         * **[!UICONTROL Show me all ads for millennial women in urban markets]**

        AI エージェントは次のことが可能です。

         * キャンバスをフィルタリングして、特定のオーディエンスセグメント、地域、言語、カテゴリー、その他のカタログフィールドに一致する広告を表示できます。
         * 文字数制限の超過、コンテンツのオーバーフローや裁ち落とし、画像リンクの破損、免責条項の表示など、品質の問題を確認します。
         * A/B テスト分析のための広告の組み合わせを比較します。
         * 広告をグループ化して並べてレビューできます。

        AI エージェントは、カタログから取得したコンテンツを変更できません。 広告コンテンツを変更するには、ソースカタログを更新します。

   1. ヘッダーに&#x200B;**[!UICONTROL Save Dynamic Creative]**&#x200B;を保存します。

   1. 確認メッセージで、**[!UICONTROL Create]**&#x200B;をクリックします。

## ダイナミッククリエイティブの編集 {#edit-dynamic-creative}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックします。

   左側に広告プレビュー、右側に設定パネルが表示されたフルスクリーンエディターが開きます。

1. 「**[!UICONTROL Details]**」タブと「**[!UICONTROL Attribute Mapping]**」タブを使用して、クリエイティブ設定を編集します。

   **[!UICONTROL Details]** タブ：

   * **[!UICONTROL Advertiser]**、**[!UICONTROL Ad Library]**&#x200B;および&#x200B;**[!UICONTROL Ad template]**&#x200B;は読み取り専用です。
   * **[!UICONTROL Dynamic creative name]:** クリエイティブの表示名。
   * **[!UICONTROL Number of cards]:**&#x200B;各広告の組み合わせに含まれるカタログ オファーの数（1 ～ 50）。
   * （オプション） **[!UICONTROL Catalogs]**&#x200B;で、カタログの選択を更新します。
      * **[!UICONTROL Catalog template]**&#x200B;を使用して、使用可能なカタログをフィルタリングします。 必要に応じてテンプレートファイルをダウンロードするには、**[!UICONTROL Download feed template]**&#x200B;をクリックします。
      * リストからカタログを検索して選択するか、アップロードエリアにドラッグするか、**[!UICONTROL Browse Files]**&#x200B;をクリックして新しいカタログファイルをアップロードします（サポートされている形式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP、MP4、最大25 MB、一度に1つのファイル）。 アップロードされたカタログは、チップリストに「**（アップロード）**」というラベルが付けられます。

     すべてのカタログは、同じカタログテンプレートファミリーに属している必要があります。

   **[!UICONTROL Attribute Mapping]** タブ：

   * **[!UICONTROL Targeting]**&#x200B;で、少なくとも1つのデータソースを選択してください：**[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**、または&#x200B;**[!UICONTROL Audience Segment]**。
   * **[!UICONTROL Attribute Mapping]**&#x200B;で、各テンプレートレイヤー名から対応するカタログ列ラベルへのマッピングを更新します。

1. **[!UICONTROL Update Creative]**&#x200B;をクリックします。

## ダイナミッククリエイティブのQA アシスタントを再度開きます {#qa-dynamic-creative}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**&#x200B;をクリックします。

   QA画面が開きます。 使用可能なキャンバス制御とAI アシスタント機能については、「[手順5:AIを使用したプレビューとQA](#qa)」を参照してください。

## 動的なクリエイティブの変更ログを表示する {#view-change-log}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Change Log]**&#x200B;をクリックします。

## 動的なクリエイティブの複製 {#duplicate-dynamic-creative}

ダイナミッククリエイティブを複製して、同じ設定の新しいクリエイティブをライブラリに追加します。 後で新しいクリエイティブの名前を変更し、必要に応じて設定を編集できます。

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**&#x200B;をクリックします。

   新しいクリエイティブ名は`<original name> (copy)`です。

## ダイナミッククリエイティブの削除 {#delete-dynamic-creative}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising CreativeのCreative Studioについて](creative-studio-about.md)
>* [Creative Studioで標準広告を管理](creative-studio-manage-standard-ads.md)
>* [Creative Studioでテンプレートを管理](creative-studio-manage-templates.md)

