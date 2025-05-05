---
title: フィードデータ設定の指定
description: フィードデータの処理方法を制御する設定の設定方法について説明します。
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1155'
ht-degree: 0%

---

# フィードデータ設定の指定

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

フィードデータファイルで広告グループ、キーワードおよび広告を処理する方法と、FTP ファイルのデータをフィード設定を使用して処理する方法を設定できます。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Settings]**] をクリックします。

1. [ フィードデータ設定 ](#feed-data-settings) を指定します。

   1. 「[!UICONTROL Obsolete Item Auto-Processing]」セクションで、フィールド内の情報を選択します。

   1. （FTP またはマーチャントセンターアカウントへの直接リンクを介してデータをアップロードする広告主） [!UICONTROL FTP/GMC Account Auto-Processing] のセクションで、フィールドの情報を選択します。

   1. 「[!UICONTROL Miscellaneous Auto-Processing]」セクションで、フィールド内の情報を選択します。

1. 「**[!UICONTROL Save]**」をクリックします。

## フィードデータの設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:**&#x200B;[!UICONTROL Obsolete Item Auto-processing] のすべての設定を次の場合に適用します。

* *[!UICONTROL Ad Groups Only]:* 古い広告グループのみ。

* *[!UICONTROL Keywords Only]:* 古いキーワードおよび製品グループのみ。

* *[!UICONTROL Ad Variations Only]* （デフォルト）：古い広告のみ。

* *[!UICONTROL Keywords and Ad Variations]:* 古いキーワード/製品ターゲット/製品グループと古い広告の両方。

>[!NOTE]
>
>* 買い物広告 [!DNL Google Ads] 場合は、最下位レベルの製品グループのみが影響を受けます。
>* [!DNL Yandex] アカウントの場合、この設定に関係なく、古いアイテムの自動処理タスクは常に広告バリエーションで実行されます。

**[!UICONTROL When the Scheduled End Date is reached]:** （手動で投稿されたデータのみ）指定した終了日時に終了時刻が投稿されたフィード ファイルの行項目の処理方法：

* *[!UICONTROL Delete]* （デフォルト）：指定した終了時刻になると、関連するすべてのコンポーネントを削除します。 この操作は元に戻すことができません。

* *[!UICONTROL Pause]:* 指定された終了時刻に、関連するすべてのコンポーネントを一時停止します。 必要に応じて、後でコンポーネントを再アクティブ化できます。

* *[!UICONTROL None]:* 関連するコンポーネントのステータスは変更しないでください。

**[!UICONTROL Missing line items in a manually uploaded feed]:** 既存の項目が手動でアップロードされた新しいフィードファイルに含まれていない場合や、テンプレートの「マップのみ」設定に従って既存のキャンペーンや広告グループにマッピングされていない場合の対処方法は次のとおりです。

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいフィードファイルに同じ行項目が含まれている場合は再アクティブ化され、履歴と品質のスコアは保持されます。 **注意：** 親製品グループのすべての子製品グループがない場合、製品グループを一時停止できないので、親製品グループは削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントを変更しません。

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** 既存のアイテムに対する処理は、1） FTP ディレクトリにアップロードされた新しいフィードファイルに含まれていない場合、または b） マーチャントセンターアカウントで次回 Search、Social、およびCommerceが同期される場合、または 2） テンプレートの [!UICONTROL Map Only] 設定に従って既存のキャンペーンまたは広告グループにマッピングされていない場合です。

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいデータに同じ行項目が含まれている場合は再アクティブ化され、履歴と品質スコアは保持されます。 **注意：** 親製品グループのすべての子製品グループがない場合、製品グループを一時停止できないので、親製品グループは削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントを変更しません。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** 在庫レベルを含むライン項目に対して実行する操作：

* （指定した列に数値のみの在庫値を含むフィードの場合）在庫レベルが指定した数量以下になっている。 デフォルトの数量は 0 （ゼロ）です。

* （指定した列にテキスト値を含むフィードの場合） [!UICONTROL Availability] の値は「[!UICONTROL out of stock]」です。値では大文字と小文字が区別されません。 **メモ：** **フィードテンプレートで、「[!UICONTROL This column has non-numeric values]」のチェックボックスを使用して、テキストベースの在庫レベル列を指定します。

両方のケースでアクションを選択します。

* *[!UICONTROL Delete]* （デフォルト）コンポーネントを削除します。

* *[!UICONTROL Pause]:* コンポーネントを一時停止します。 データを更新すると、在庫数値が指定した数量を超えた場合や、[!UICONTROL Availability] が「[!UICONTROL in stock]」または「[!UICONTROL preorder]」の場合、コンポーネントが再アクティブ化されます。 コンポーネントは、履歴と品質スコアを保持します。

各行項目の在庫レベルは、各テンプレートの「[!UICONTROL Stock Level]」フィールドに指定されているフィードファイルの列から取得されます。

>[!TIP]
>
>* 再入荷や可用性の向上を予定している製品やサービスの場合、広告グループ、キーワードおよび広告を削除して再作成するのではなく、一時停止する必要があります。 一時停止することで、品質スコアを保持できます。
>* 広告グループに対して古い自動処理を有効にしたときに、新しいデータに広告グループのストックレベルが含まれている場合は、指定されたストックレベルがブランド/品目レベルではなくカテゴリレベルにある場合にのみ、広告グループを削除または一時停止すると便利です。 例えば、「コンバーチブル」という広告グループがある場合、広告グループの在庫レベルは、広告グループで表されるすべての個々のコンバーチブルモデルの合計にする必要があります。

**[!UICONTROL Propagate feed data through all applicable templates]:** （FTP またはマーチャントセンターアカウントを使用してデータファイルをアップロードする広告主）該当するテンプレートを介して新しいデータを自動的に伝播します。 このオプションはデフォルトで選択されています。 このオプションを無効にした場合でも、任意のフィードファイルやアカウント、または任意のテンプレートのデータを手動で反映できます。

>[!NOTE]
>
>* FTP ファイルの場合、フィードサービスは 2 時間ごとに FTP ディレクトリの更新を確認します（PST タイムゾーンの偶数番号の時間）。 このオプションは、前回のチェック以降にアップロードされたすべてのファイルを処理します。
>* マーチャントセンターアカウントの場合、検索、ソーシャル、Commerceは、広告主のタイムゾーンの約 06:00 に毎日アカウントと同期します。 このオプションは、前回の同期以降に更新されたすべてのデータを処理します。
>* 伝播されたデータは、データが広告ネットワークまたは [!UICONTROL Bulksheets] ビューにポストされるまで、「[!UICONTROL Campaigns]」、「[!UICONTROL Ad Groups]」、「[!UICONTROL Keywords]」および「[!UICONTROL Ads]」タブから使用できます。

**[!UICONTROL Post to the SE]:** （FTP またはマーチャントセンターアカウントを使用してデータファイルをアップロードする広告主）新しいデータが該当するテンプレートに反映された後、関連する広告ネットワークに適した形式でバルクシートファイルを自動的に作成します。 また、このオプションでは、サブコンポーネントにエラーがない限り、「[!UICONTROL Campaigns]」、「[!UICONTROL Ad Groups]」、「[!UICONTROL Keywords]」および「[!UICONTROL Ads]」タブからデータが削除されます。

このオプションは、デフォルトでは無効になっています。 このオプションを有効にするには、チェック ボックスをオンにし、バルクシート ファイルを広告ネットワークに投稿するかどうかを指定します。

* *[!UICONTROL Immediately]* （デフォルト）：データがテンプレートを通じて伝播された後、バルクシートファイルを関連する広告ネットワークに投稿します。 バルクシート ファイルは、[!UICONTROL Bulksheets] ビューで 30 日間使用できます。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**バルクシート ファイルは関連する広告ネットワークには投稿されませんが、[!UICONTROL Bulksheets] ビューに一覧表示され、後で投稿できます。 バルクシート ファイルは、[!UICONTROL Bulksheets] ビューで 30 日間使用できます。 バルクシートファイルが 10 MB を超えて 2 GB 未満の場合、ファイルは ZIP 形式です。投稿するためにファイルを解凍する必要はありません。 &#x200B;** ヒント：** ランディングページの検証をまだ行っていない場合は、このオプションを使用して、データを広告ネットワークに投稿する前に [!UICONTROL Bulksheets] ビューからランディングページを検証できます。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** 指定された単語数を超えるキーワード フレーズを広告ネットワークに投稿することを禁止します。 このオプションを選択すると、単語の最大数を超えるキーワードフレーズが伝播され、「[!UICONTROL Keywords]」タブに表示されますが、データを投稿しようとしても投稿されません。

このオプションはデフォルトで無効になっており、フレーズに含まれる単語数に関係なく、すべてのキーワードが投稿されます。 このオプションを選択した場合は、投稿する単語の最大数（3 ～ 10）を選択します。

>[!MORELIKETHIS]
>
>* [ 在庫フィードについて ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [ テンプレートを使用したフィードデータの伝播 ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [ フィードから広告ネットワークにキャンペーンデータを投稿する ](propagated-data-post.md)
