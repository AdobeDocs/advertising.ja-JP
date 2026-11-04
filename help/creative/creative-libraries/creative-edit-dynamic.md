---
title: 動的なクリエイティブの編集と品質確認
description: クリエイティブライブラリで動的なクリエイティブ設定を編集し、カタログコンテンツの品質を確認する方法を説明します。
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: ed1682eff9ce28df30a5314de90f6f67c10f338a
workflow-type: tm+mt
source-wordcount: '1118'
ht-degree: 0%
---
# 動的なクリエイティブの編集と品質確認

クリエイティブ設定を編集して、クリエイティブの名前、カタログ、属性マッピングなどの設定を変更します。 QA エージェントを使用して、結果の広告を確認し、カタログ値を修正します。

## クリエイティブ設定の編集 {#edit-creative-settings}

### 新しいUIから {#from-the-new-ui}

1. クリエイティブ設定を開きます。

   * クリエイティブライブラリから：

     1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

     1. 次のいずれかの方法でライブラリを開きます。

        * ライブラリ名をクリックします。

        * ライブラリ名の横にある「**[!UICONTROL ...]**」 > 「**[!UICONTROL Open]**」をクリックします。

     1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Edit]**」をクリックします。

   * [!UICONTROL Creative Studio]から：

     1. メインメニューで、**[!UICONTROL Creative]>[!UICONTROL Creative Studio]**&#x200B;をクリックします。

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

### レガシーUIから {#from-the-legacy-ui}

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. **[!UICONTROL Switch to classic UI]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. クリエイティブ行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [動的広告設定](creative-settings-dynamic.md)を編集します。

1. 生成するクリエイティブをプレビューするには、**[!UICONTROL Continue]**&#x200B;をクリックします。 プレビュー内で次のいずれかを実行できます。

   * カタログ、フィルター値<!-- explain more-->、広告サイズでクリエイティブをフィルタリングするには、プレビュー領域の上にあるフィルターを使用します。

   * プレビュー領域の下にある検索フィールドで、製品を一意のIDで検索する。

   * 表示される列を変更するには、プレビュー領域の下にある![列フィルター](/help/creative/assets/custom-columns.png "列フィルター")をクリックします。

   * 特定のクリエイティブをプレビューするには、行のチェックボックスをオンにします。

   * コンテンツを変更する：

     * （表示広告のみ）表内のセルの値を編集するには、セル内をクリックして値を編集します。 セルの外側をクリックするか、**[!DNL Enter]** キーを押して変更を保存します。

     * 1つの商品をデフォルト <!--Explain what this means. -->としてマークするには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Set as Default]**&#x200B;をクリックします。

     * （広告に複数のオファーが含まれる場合）複数の商品をデフォルトとしてマークするには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Set as Default]**」をクリックします。

     * 商品をカタログから削除するには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete Row]**&#x200B;をクリックします。

     * （広告に複数のオファーが含まれる場合）カタログから複数の商品を削除するには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Delete Row]**」をクリックします。

1. クリエイターを救う：

   * 広告を保存し、ライブラリの[ クリエイティブバンドル ](bundle-manage.md)に追加するには：

     1. **[!UICONTROL Save and Attach to Bundle]**&#x200B;をクリックします。

     1. **[!UICONTROL Save]**&#x200B;をクリックして広告を保存します。

     1. バンドルを選択し、**[!UICONTROL Attach Creative to Bundles]**&#x200B;をクリックします。

   * 広告を保存して設定を終了するには、**[!UICONTROL Save]**&#x200B;をクリックし、もう一度&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

## 動的なクリエイティブの品質チェック（新しいUIのみ） {#qa-dynamic-creative}

新しいUIのQA エージェントを使用して、動的なクリエイティブのテンプレートに対してカタログ行を分析し、結果の広告をプレビューし、潜在的なコンテンツの問題を特定します。 **[!UICONTROL AI Assistant]**&#x200B;を使用して広告をフィルタリングおよびグループ化し、カタログアラートを確認し、変更を公開する前にカタログ値を手動で修正できます。

>[!NOTE]
>
>[!UICONTROL Creative Libraries]または[!UICONTROL Creative Studio]から動的なクリエイティブを品質チェックできます。 その他のエントリポイントについては、「[Creative Studioの動的なクリエイティブの品質チェック ](/help/creative/creative-studio/creative-studio-manage-dynamic-ads.md#qa-dynamic-creative)」を参照してください。

QA Agentは、動的テンプレートに基づく動的ディスプレイクリエイターにのみ使用でき、標準的なクリエイターや動的なビデオクリエイターには使用できません。

### QA エージェントを開きます {#open-qa-agent}

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. 次のいずれかの方法でライブラリを開きます。

   * ライブラリ名をクリックします。
   * ライブラリ名の横にある「**[!UICONTROL ...]**」 > 「**[!UICONTROL Open]**」をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、動的クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL QA Agent]**」をクリックします。

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

* 既存の動的クリエイティブを保存し、カタログ編集を公開するには：

  1. ヘッダーの&#x200B;**[!UICONTROL Save Dynamic Creative]**&#x200B;をクリックします。

  1. **[!UICONTROL Update Dynamic Creative]**&#x200B;確認ダイアログで、**[!UICONTROL Update]**&#x200B;をクリックします。

     クリエイティブライブラリに戻ります。

* 保留中のカタログ編集を公開せずに終了するには、ページヘッダーの「**[!UICONTROL Cancel]**」をクリックします。

>[!MORELIKETHIS]
>
>* [動的なクリエイティブ設定](creative-settings-dynamic.md)
>* [ クリエイティブライブラリに動的なクリエイティブを追加](creative-add-dynamic.md)
>* [ クリエイティブの変更ログを表示](/help/creative/creative-libraries/creative-view-change-log.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
