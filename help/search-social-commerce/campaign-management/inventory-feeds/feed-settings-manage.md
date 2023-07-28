---
title: フィードデータの設定
description: フィードデータの処理方法を制御する設定の設定方法について説明します。
exl-id: fc72d1bc-aac7-4280-80c6-4fc53a96a49f
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '1147'
ht-degree: 0%

---

# フィードデータの設定

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

フィード設定を使用して、フィードデータファイルで広告グループ、キーワードおよび広告を処理する方法や、FTP ファイルでデータを特に処理する方法を設定できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Settings]**.

1. 次を指定します。 [フィードデータ設定](#feed-data-settings):

   1. Adobe Analytics の [!UICONTROL Obsolete Item Auto-Processing] 「 」セクションで、「 」フィールドの情報を選択します。

   1. （広告主が FTP 経由またはマーチャントセンターアカウントへの直接リンク経由でデータをアップロードする場合） [!UICONTROL FTP/GMC Account Auto-Processing] 「 」セクションで、「 」フィールドの情報を選択します。

   1. Adobe Analytics の [!UICONTROL Miscellaneous Auto-Processing] 「 」セクションで、「 」フィールドの情報を選択します。

1. クリック **[!UICONTROL Save]**.

## フィードデータ設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** 次のすべてを適用 [!UICONTROL Obsolete Item Auto-processing] 次の設定に従います。

* *[!UICONTROL Ad Groups Only]:* 古い広告グループのみ。

* *[!UICONTROL Keywords Only]:* 古いキーワードと製品グループのみ。

* *[!UICONTROL Ad Variations Only]* （デフォルト）：古い広告のみ。

* *[!UICONTROL Keywords and Ad Variations]:* 古いキーワード/製品ターゲット/製品グループと古い広告の両方。

>[!NOTE]
>
>* の場合 [!DNL Google Ads] 買い物広告。影響を受けるのは最下位レベルの製品グループのみです。
>* の場合 [!DNL Yandex] アカウント、古くなった項目の自動処理タスクは、この設定に関係なく、常に広告バリエーションで実行されます。

**[!UICONTROL When the Scheduled End Date is reached]:** （手動で投稿されたデータのみ）終了日時が来てから、指定した終了日時で投稿されたフィードファイル内の行項目に対して行項目を処理する方法を次に示します。

* *[!UICONTROL Delete]* （デフォルト）：指定された終了時間になると、関連するすべてのコンポーネントを削除します。 この操作を元に戻すことはできません。

* *[!UICONTROL Pause]:* 指定された終了時間に達したら、関連するすべてのコンポーネントを一時停止します。 必要に応じて、後でコンポーネントを再アクティブ化できます。

* *[!UICONTROL None]:* 関連するコンポーネントのステータスは変更しないでください。

**[!UICONTROL Missing line items in a manually uploaded feed]:** 手動でアップロードされた新しいフィードファイルに含まれていない場合や、テンプレートの「マップのみ」設定で既存のキャンペーンまたは広告グループにマッピングされていない場合の、既存の項目の処理方法：

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいフィードファイルに同じ行項目が含まれ、その履歴と品質スコアが保持される場合、再アクティブ化されます。 **注意：** 親製品グループの子製品グループがすべて見つからない場合、製品グループを一時停止できないので、親製品グループは削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントは変更しません。

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** (1)FTP ディレクトリや b) 次回検索、ソーシャル、コマースが同期する際、または 2) 既存のキャンペーンや広告グループにマッピングしない場合は、既存の項目を使用する方法 [!UICONTROL Map Only] 設定を使用します。

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいデータに同じ行項目が含まれ、履歴と品質スコアが保持される場合、再アクティブ化されます。 **注意：** 親製品グループの子製品グループがすべて見つからない場合、製品グループを一時停止できないので、親製品グループは削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントは変更しません。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** 在庫レベルを含む品目の処理は、次の場合におこないます。

* （指定した列に数値のみの在庫値を持つフィードの場合）在庫レベルは、指定した数量以下になります。 デフォルトの数量は 0 です。

* （指定した列にテキスト値を持つフィードの場合） [!UICONTROL Availability] が&quot;[!UICONTROL out of stock]&quot;；値では大文字と小文字が区別されません。 **注意：** **フィードテンプレートで、「[!UICONTROL This column has non-numeric values].&quot;

次の両方の場合に、アクションを選択します。

* *[!UICONTROL Delete]* （デフォルト）コンポーネントを削除します。

* *[!UICONTROL Pause]:* コンポーネントを一時停止します。 データが更新されると、数値の在庫値が指定した数量を超えたり、 [!UICONTROL Availability] が&quot;[!UICONTROL in stock]&quot;または&quot;[!UICONTROL preorder]&quot;. コンポーネントは、履歴と品質スコアを保持します。

各行項目の在庫レベルは、「[!UICONTROL Stock Level]」フィールドを使用して、個々のテンプレートに割り当てます。

>[!TIP]
>
>* 在庫の再設定や可用性の向上を期待する製品やサービスの場合は、広告グループ、キーワードおよび広告を一時停止して再作成するのではなく、一時停止する必要があります。 一時停止すると、品質スコアを保持できます。
>* 広告グループの古い自動処理を有効にし、新しいデータに広告グループの在庫レベルが含まれる場合、指定された在庫レベルがブランド/項目レベルではなくカテゴリレベルにある場合にのみ、広告グループを削除または一時停止すると効果的です。 例えば、広告グループが「コンバージョン数」である場合、広告グループの在庫レベルは、広告グループに表されるすべての個々のコンバーチブルモデルの合計にする必要があります。

**[!UICONTROL Propagate feed data through all applicable templates]:** （広告主が FTP またはマーチャントセンターアカウントを使用してデータファイルをアップロードする場合）新しいデータを適切なテンプレートを使用して自動的に伝播します。 このオプションはデフォルトで選択されています。 このオプションを無効にした場合でも、フィードファイルやアカウント、または任意のテンプレートに対して、データを手動で伝達できます。

>[!NOTE]
>
>* FTP ファイルの場合、フィードサービスは、2 時間ごとに FTP ディレクトリの更新をチェックします（PST タイムゾーンでは偶数時間）。 このオプションは、最後のチェック以降にアップロードされたすべてのファイルを処理します。
>* マーチャントセンターアカウントの場合、Search、Social、および Commerce は、広告主のタイムゾーンの約 06:00 に毎日アカウントと同期します。 このオプションは、前回の同期以降に更新されたすべてのデータを処理します。
>* 反映されたデータは、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] データが広告ネットワークまたは [!UICONTROL Bulksheets] 表示。

**[!UICONTROL Post to the SE]:** （広告主が FTP またはマーチャントセンターのアカウントを使用してデータファイルをアップロードする場合）新しいデータが適切なテンプレートを伝搬した後、関連する広告ネットワークに適した形式のバルクシートファイルを自動的に作成します。 また、このオプションを選択すると、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ（サブコンポーネントにエラーがない場合）

このオプションはデフォルトでは無効になっています。 このオプションを有効にするには、チェックボックスをオンにして、一括送信シートファイルを広告ネットワークに投稿するかどうかを指定します。

* *[!UICONTROL Immediately]* （デフォルト）：データがテンプレートを通じて伝播された後、関連する広告ネットワークにバルクシートファイルを投稿します。 バルクシートファイルは、 [!UICONTROL Bulksheets] 30 日間表示されます。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**関連する広告ネットワークにバルクシートファイルを投稿しませんが、 [!UICONTROL Bulksheets] 表示。後で投稿できます。 バルクシートファイルは、 [!UICONTROL Bulksheets] 30 日間表示されます。 バルクシートファイルが 10 MB を超え、2 GB 未満の場合、ファイルは ZIP 形式になるので、投稿するためにファイルを解凍する必要はありません。 **ヒント：** ランディングページをまだ検証していない場合は、このオプションを使用して、 [!UICONTROL Bulksheets] 表示してから、データを広告ネットワークに投稿します。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** 指定した単語数を超えるキーワード語句を広告ネットワークに投稿しないようにします。 このオプションを選択すると、最大語数を超えるキーワードフレーズが伝播され、 [!UICONTROL Keywords] 」タブに表示されますが、データを投稿しようとした際には投稿されません。

このオプションはデフォルトで無効になっているので、フレーズに含まれる単語の数に関係なく、すべてのキーワードが投稿されます。 このオプションを選択した場合、投稿する単語の最大数 (3 ～ 10) を選択します。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [テンプレートを通じてフィードデータを伝達](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [フィードから広告ネットワークに生成されたキャンペーンデータを投稿します](propagated-data-post.md)
