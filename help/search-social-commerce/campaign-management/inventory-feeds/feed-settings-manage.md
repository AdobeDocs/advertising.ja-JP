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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

フィードデータファイルで広告グループ、キーワードおよび広告を処理する方法と、FTP ファイルのデータをフィード設定を使用して処理する方法を設定できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Settings]**.

1. を指定 [フィードデータ設定](#feed-data-settings):

   1. が含まれる [!UICONTROL Obsolete Item Auto-Processing] セクションで、フィールドの情報を選択します。

   1. （FTP またはマーチャントセンターアカウントへの直接リンクを介してデータをアップロードする広告主）で [!UICONTROL FTP/GMC Account Auto-Processing] セクションで、フィールドの情報を選択します。

   1. が含まれる [!UICONTROL Miscellaneous Auto-Processing] セクションで、フィールドの情報を選択します。

1. クリック **[!UICONTROL Save]**.

## フィードデータの設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:** 次のすべてを適用 [!UICONTROL Obsolete Item Auto-processing] 設定：

* *[!UICONTROL Ad Groups Only]:* 古い広告グループのみ。

* *[!UICONTROL Keywords Only]:* 古いキーワードおよび製品グループのみ。

* *[!UICONTROL Ad Variations Only]* （デフォルト）：古い広告のみ。

* *[!UICONTROL Keywords and Ad Variations]:* 古いキーワード/製品ターゲット/製品グループと古い広告の両方。

>[!NOTE]
>
>* の場合 [!DNL Google Ads] ショッピング広告では、最下位レベルの製品グループのみが影響を受けます。
>* の場合 [!DNL Yandex] アカウント、古い項目自動処理タスクは、この設定に関係なく、常に広告バリエーションで実行されます。

**[!UICONTROL When the Scheduled End Date is reached]:** （手動で投稿されたデータのみ）指定した終了日時に終了時刻が到着した後に投稿されたフィードファイルの行項目の処理方法：

* *[!UICONTROL Delete]* （デフォルト）：指定した終了時刻に関連するすべてのコンポーネントを削除します。 この操作は元に戻すことができません。

* *[!UICONTROL Pause]:* 指定された終了時刻に、関連するすべてのコンポーネントを一時停止します。 必要に応じて、後でコンポーネントを再アクティブ化できます。

* *[!UICONTROL None]:* 関連するコンポーネントのステータスを変更しないでください。

**[!UICONTROL Missing line items in a manually uploaded feed]:** 手動でアップロードされた新しいフィードファイルに含まれていない場合や、テンプレートのマップのみの設定に従って既存のキャンペーンや広告グループにマッピングされていない場合は、既存の項目をどのように処理すればよいですか？

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいフィードファイルに同じ行項目が含まれている場合は再アクティブ化され、履歴と品質のスコアは保持されます。 **注意：** 親製品グループのすべての子製品グループがない場合は、製品グループを一時停止できないので、親製品グループが削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントは変更しません。

**[!UICONTROL Missing line items in an FTP feed/GMC account]:** 既存のアイテムを使用する場合、1） アイテムが含まれていない場合、a） FTP ディレクトリにアップロードされた新しいフィードファイルに含まれている場合、または b） マーチャントセンターアカウントで次回 Search、Social、およびCommerceが同期される場合、または 2） アイテムが既存のキャンペーンまたは広告グループにマッピングされない場合 [!UICONTROL Map Only] テンプレートの設定。

* *[!UICONTROL Delete]:* 既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:* 既存のコンポーネントを一時停止します。 新しいデータに同じ行項目が含まれている場合は再アクティブ化され、履歴と品質スコアは保持されます。 **注意：** 親製品グループのすべての子製品グループがない場合は、製品グループを一時停止できないので、親製品グループが削除されます。

* *[!UICONTROL None]* （デフォルト）：既存のコンポーネントは変更しません。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:** 在庫レベルを含むライン項目に対して実行する操作：

* （指定した列に数値のみの在庫値を含むフィードの場合）在庫レベルが指定した数量以下になっている。 デフォルトの数量は 0 （ゼロ）です。

* （指定した列にテキスト値を含むフィードの場合）の値 [!UICONTROL Availability] が&quot;[!UICONTROL out of stock]``；値では大文字と小文字が区別されません。 **注意：** **フィードテンプレートで、「」のチェックボックスを使用してテキストベースのストックレベル列を指定します[!UICONTROL This column has non-numeric values].」と入力します。

両方のケースでアクションを選択します。

* *[!UICONTROL Delete]* （デフォルト）コンポーネントを削除します。

* *[!UICONTROL Pause]:* コンポーネントを一時停止します。 データを更新すると、在庫数値が指定した数量を超えた場合や、 [!UICONTROL Availability] が&quot;[!UICONTROL in stock]「または」[!UICONTROL preorder]」と入力します。 コンポーネントは、履歴と品質スコアを保持します。

各行項目の在庫レベルは、「」で指定されているように、フィードファイルの列から取得されます[!UICONTROL Stock Level]各テンプレートの「」フィールド

>[!TIP]
>
>* 再入荷や可用性の向上を予定している製品やサービスの場合、広告グループ、キーワードおよび広告を削除して再作成するのではなく、一時停止する必要があります。 一時停止することで、品質スコアを保持できます。
>* 広告グループに対して古い自動処理を有効にしたときに、新しいデータに広告グループのストックレベルが含まれている場合は、指定されたストックレベルがブランド/品目レベルではなくカテゴリレベルにある場合にのみ、広告グループを削除または一時停止すると便利です。 例えば、「コンバーチブル」という広告グループがある場合、広告グループの在庫レベルは、広告グループで表されるすべての個々のコンバーチブルモデルの合計にする必要があります。

**[!UICONTROL Propagate feed data through all applicable templates]:** （FTP またはマーチャントセンターアカウントを介してデータファイルをアップロードする広告主）該当するテンプレートを使用して、新しいデータを自動的に伝播します。 このオプションはデフォルトで選択されています。 このオプションを無効にした場合でも、任意のフィードファイルやアカウント、または任意のテンプレートのデータを手動で反映できます。

>[!NOTE]
>
>* FTP ファイルの場合、フィードサービスは 2 時間ごとに FTP ディレクトリの更新を確認します（PST タイムゾーンの偶数番号の時間）。 このオプションは、前回のチェック以降にアップロードされたすべてのファイルを処理します。
>* マーチャントセンターアカウントの場合、検索、ソーシャル、Commerceは、広告主のタイムゾーンの約 06:00 に毎日アカウントと同期します。 このオプションは、前回の同期以降に更新されたすべてのデータを処理します。
>* 伝播されたデータは、 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] データが広告ネットワークまたは [!UICONTROL Bulksheets] 表示。

**[!UICONTROL Post to the SE]:** （FTP またはマーチャントセンターアカウントを介してデータファイルをアップロードする広告主）新しいデータが該当するテンプレートに反映された後、関連する広告ネットワークに適した形式でバルクシートファイルを自動的に作成します。 また、このオプションはからデータを削除します。 [!UICONTROL Campaigns], [!UICONTROL Ad Groups], [!UICONTROL Keywords]、および [!UICONTROL Ads] タブ（サブコンポーネントにエラーがない場合）

このオプションは、デフォルトでは無効になっています。 このオプションを有効にするには、チェック ボックスをオンにし、バルクシート ファイルを広告ネットワークに投稿するかどうかを指定します。

* *[!UICONTROL Immediately]* （デフォルト）：データがテンプレートを通じて伝播された後、バルクシートファイルを関連する広告ネットワークに投稿します。 バルクシートファイルは、引き続き [!UICONTROL Bulksheets] 30 日間表示します。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**バルクシートファイルは関連する広告ネットワークには投稿されませんが、にリストされます [!UICONTROL Bulksheets] を表示します。このビューから、後で投稿できます。 バルクシートファイルは、引き続き [!UICONTROL Bulksheets] 30 日間表示します。 バルクシートファイルが 10 MB を超えて 2 GB 未満の場合、ファイルは ZIP 形式です。投稿するためにファイルを解凍する必要はありません。 **ヒント：** ランディングページを以前に検証したことがない場合は、このオプションを使用して、から検証できるようにします [!UICONTROL Bulksheets] 広告ネットワークにデータを投稿する前に、を表示します。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:** 指定された単語数を超えるキーワード フレーズを広告ネットワークに投稿することを禁止します。 このオプションを選択すると、単語の最大数を超えるキーワードフレーズが適用され、 [!UICONTROL Keywords] タブが表示されますが、データを投稿しようとしても投稿されません。

このオプションはデフォルトで無効になっており、フレーズに含まれる単語数に関係なく、すべてのキーワードが投稿されます。 このオプションを選択した場合は、投稿する単語の最大数（3 ～ 10）を選択します。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [テンプレートを使用したフィードデータの伝播](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [フィードから広告ネットワークにキャンペーン データを投稿](propagated-data-post.md)
