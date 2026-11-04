---
title: Creative Studioで動的なクリエイティブを管理する
description: Adobe Advertising Creative Studioで、カタログを活用した動的クリエイティブを構築、品質確認、編集、複製、削除する方法を説明します。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 88fead9ffc4eaa572be090877790422e67831036
workflow-type: tm+mt
source-wordcount: '1469'
ht-degree: 0%
---
# [!UICONTROL Creative Studio]での動的クリエイティブの管理

[!UICONTROL Creative Studio]の「**[!UICONTROL Creatives]**」タブには、動的なクリエイターがライブラリ別に一覧表示されます。 ここから、新しいカタログ駆動型の動的クリエイティブの作成、AIを使用したクリエイターの品質確認、既存のクリエイターの詳細と属性マッピングの編集、変更ログの表示、クリエイターの複製、クリエイターの削除を行うことができます。

## ダイナミックなクリエイティブを作成 {#build-dynamic-creative}

このワークフローは、カタログ主導のダイナミックなクリエイティブを作成するために使用します。 4段階のガイド付きウィザードでは、テンプレートの選択、カタログの接続、カタログフィールドとテンプレート要素のマッピングについて説明します。 セットアップ後、[!UICONTROL AI Assistant]を使用すると、カタログデータから生成された各広告の組み合わせをプレビューおよび品質チェックできます。

動的なクリエイターは、標準的な広告とは大きく異なります。AI エージェントはカタログから提供されたコンテンツを変更できません。 問題をフィルタリング、分析、フラグ付けできますが、広告コンテンツを変更するには、QA画面またはソースカタログから、カタログ値を手動で更新する必要があります。

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

   QAを続行すると、**[!UICONTROL Dynamic Creative QA]**&#x200B;画面が開き、プレビューキャンバスと&#x200B;**[!UICONTROL AI Assistant]** チャットパネルが表示されます。

1. QAを続行する場合は、「[動的クリエイティブの品質チェック &#x200B;](#qa-dynamic-creative)」の手順に従って、[広告の分析とフィルタリング &#x200B;](#analyze-ads)、[&#x200B; プレビューとアラートのレビュー](#review-previews)、およびオプションで[&#x200B; カタログ値](#correct-catalog-values)を修正します。 完了したら、[動的クリエイティブを保存](#save-or-exit)します。

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

## 動的なクリエイティブの品質チェック {#qa-dynamic-creative}

QA エージェントを使用すると、動的なクリエイティブのテンプレートに対してカタログ行を分析し、結果の広告をプレビューし、潜在的なコンテンツの問題を特定できます。 **[!UICONTROL AI Assistant]**&#x200B;を使用して広告をフィルタリングおよびグループ化し、カタログアラートを確認し、変更を公開する前にカタログ値を手動で修正できます。

エージェントは[!UICONTROL Creative Libraries]または[!UICONTROL Creative Studio]から&#x200B;**[!UICONTROL Dynamic Creative QA]**&#x200B;画面を開きます。 メニューラベルは異なりますが、どちらのエントリポイントも同じQA機能を提供します。 分析は、選択したクリエイティブ、カタログ、リクエストによって異なります。

>[!NOTE]
>
>QA Agentは、標準のクリエイティブや動的なビデオのクリエイティブではなく、動的なディスプレイのクリエイティブに使用できます。 [!UICONTROL Creative Libraries]では、このアクションは、動的テンプレートに基づく動的クリエイターにのみ使用できます。

### QA エージェントを開きます {#open-qa-agent}

1. 次のいずれかの方法で、保存されたQA用の動的クリエイティブを開きます。

   * **[!UICONTROL Creative Libraries]から：**

     1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

     1. ライブラリ名をクリックしてライブラリを開きます。

     1. 「**[!UICONTROL Creatives]**」タブで、動的クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL QA Agent]**」をクリックします。

   * **[!UICONTROL Creative Studio]から：**

     1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Studio]**&#x200B;をクリックします。

     1. 「**[!UICONTROL Creatives]**」タブで、「[!UICONTROL Generate or Build Creatives]」セクションの下にあるクリエイティブライブラリで、ダイナミッククリエイティブを見つけます。

     1. クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL QA Assistant]**&#x200B;をクリックします。

   **[!UICONTROL Dynamic Creative QA]**&#x200B;画面が開き、プレビューキャンバスと&#x200B;**[!UICONTROL AI Assistant]** チャットパネルが表示されます。

1. クリエイティブで複数のカタログを使用している場合は、ヘッダーの&#x200B;**[!UICONTROL Catalog]**&#x200B;からレビューするカタログを選択します。

   アシスタントは、選択したカタログを分析します。 クリエイティブが1つのカタログのみを使用する場合、カタログセレクターは無効になります。

### AIを活用した広告の分析とフィルタリング {#analyze-ads}

1. **[!UICONTROL AI Assistant]** パネルで、**[!UICONTROL Ask anything]**&#x200B;にリクエストを入力して&#x200B;**[!UICONTROL Enter]**&#x200B;を押すか、提案されたプロンプトのいずれかをクリックします。

   * **[!UICONTROL Run a comprehensive QA pass on this dynamic creative]**
   * **[!UICONTROL Group ads by product]**
   * **[!UICONTROL Filter ads by geography]**
   * **[!UICONTROL Show all ads with headlines over 80 characters]**

   アシスタントはチャットパネルで応答し、一致するカタログ行をキャンバス上の広告プレビューとして表示します。 リクエストを送信するまで、キャンバスはアシスタントにカタログの分析を依頼するよう求めます。

1. フォローアップリクエストを使用してレビューの改善を続行します。 Ai アシスタントでは、次のことが可能になります。

   * オーディエンスセグメント、言語、地域、郵便番号などで広告をフィルタリング。
   * 指定したしきい値を使用して、文字の長さを確認します。
   * フィードのエラー、コンテンツの欠落、疑わしいコンテンツを確認します。
   * 翻訳ステータスの確認。
   * A/B テストのバリエーション。
   * 製品や問題など、レビュー用に広告をグループ化できます。

   変更を保存する前に、アシスタントの応答を確認し、プレビューを調べます。

### プレビューとアラートの確認 {#review-previews}

* カンバスツールバーを使用して、以下を行います。

  * ズームを調整します。
  * **[!UICONTROL Thumbnail view]**&#x200B;と&#x200B;**[!UICONTROL Actual size]**&#x200B;を切り替えます。
  * プレビューを再生するには、**[!UICONTROL Replay animations]**&#x200B;をクリックします。
  * ページあたりの行数を選択するか、ページ番号を選択するか、**[!UICONTROL Previous page]**&#x200B;と&#x200B;**[!UICONTROL Next page]**&#x200B;を使用します。

* アシスタントが結果をグループ化したら、リンクをクリックして、グループ内のすべてのクリエイターを表示します。 **[!UICONTROL Back to groups]**&#x200B;を使用してグループ化された結果に戻るか、**[!UICONTROL Catalog Rows]**&#x200B;を使用してグループ化されたビューを終了します。

* プレビューに&#x200B;**[!UICONTROL Issues detected]**&#x200B;が表示されたら、インジケーターの上にカーソルを置くと、問題の詳細が表示されます。

* カタログアラートが使用可能な場合は、**[!UICONTROL View Alerts]**&#x200B;をクリックします。 **[!UICONTROL Alerts]** ダイアログには、各問題のカタログ、行番号、列、エラーメッセージが一覧表示されます。 **[!UICONTROL Close]**&#x200B;をクリックしてキャンバスに戻ります。

### 正しいカタログ値 {#correct-catalog-values}

QA画面を離れることなく、広告プレビューからカタログ値を手動で編集できます。

1. 修正するプレビューで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. 編集ダイアログで、**[!UICONTROL Catalog columns to edit]**&#x200B;の下で変更する列を選択します。 列を検索するには、**[!UICONTROL Search columns]**&#x200B;を使用します。

1. **[!UICONTROL Columns content]**&#x200B;で、選択したフィールド値を更新します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

   プレビューが更新され、更新された値が反映されます。 カタログの変更は、ダイナミッククリエイティブを保存するまで公開されません。

>[!IMPORTANT]
>
>これらの編集は、広告プレビューだけでなく、カタログデータも更新します。 値を公開する前に、値を確認します。

### 変更を保存または終了 {#save-or-exit}

* ダイナミッククリエイティブを保存してカタログ編集を公開するには：

  1. ヘッダーの&#x200B;**[!UICONTROL Save Dynamic Creative]**&#x200B;をクリックします。

  1. 保存を確認します。

     * 新しいクリエイティブの場合は、**[!UICONTROL Create Dynamic Creative]**&#x200B;の確認ダイアログで「**[!UICONTROL Create]**」をクリックします。
     * 既存のクリエイティブの場合、**[!UICONTROL Update Dynamic Creative]**&#x200B;の確認ダイアログで「**[!UICONTROL Update]**」をクリックします。

     QA画面を開いた場所に応じて、クリエイティブライブラリまたは[!UICONTROL Creative Studio]に戻ります。

* 保留中のカタログ編集を公開せずに終了するには、ページヘッダーの「**[!UICONTROL Cancel]**」をクリックします。

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
