---
title: フィードデータ設定の設定
description: フィード データの処理方法を制御する設定を構成する方法について説明します。
exl-id: 7eaac751-ecdf-4e73-9eae-a961bd9b7360
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/kmaWPmbN4HFZmI0u9KE2PXMyt9jltTHAM9tWM0Bj7e0
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 1164
ht-degree: 0%

---

# フィードデータ設定の設定

*[!DNL Google Ads]、[!DNL LY Ads] （削除操作のみ）、[!DNL Microsoft Advertising]、および[!DNL Yandex] アカウントのみ*

フィード データ ファイル内の広告グループ、キーワード、広告の処理方法、およびFTP ファイル内のデータの処理方法を、フィード設定を使用して具体的に設定できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Settings]**&#x200B;をクリックします。

1. [ フィード データ設定](#feed-data-settings)を指定します。

   1. 「[!UICONTROL Obsolete Item Auto-Processing]」セクションで、フィールドの情報を選択します。

   1. （FTP経由またはマーチャント センターのアカウントへの直接リンク経由でデータをアップロードする広告主）「[!UICONTROL FTP/GMC Account Auto-Processing]」セクションで、フィールドの情報を選択します。

   1. 「[!UICONTROL Miscellaneous Auto-Processing]」セクションで、フィールドの情報を選択します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## フィードデータの設定 {#feed-data-settings}

**[!UICONTROL Enable obsolete item auto-processing for]:**&#x200B;すべての[!UICONTROL Obsolete Item Auto-processing]設定を次の場所に適用します：

* *[!UICONTROL Ad Groups Only]:*&#x200B;古い広告グループのみ。

* *[!UICONTROL Keywords Only]:*&#x200B;古いキーワードと製品グループのみ。

* *[!UICONTROL Ad Variations Only]* （デフォルト）：古い広告のみ。

* *[!UICONTROL Keywords and Ad Variations]:*&#x200B;古いキーワード/製品ターゲット/製品グループと古い広告の両方。

>[!NOTE]
>
>* [!DNL Google Ads]件のショッピング広告の場合、最も低いレベルの商品グループのみが影響を受けます。
>* [!DNL Yandex] アカウントの場合、この設定に関係なく、古い項目の自動処理タスクは常に広告バリエーションに対して実行されます。

**[!UICONTROL When the Scheduled End Date is reached]:** （手動でデータを投稿した場合のみ）終了日時が指定されたフィード ファイル内の行項目の処理：

* *[!UICONTROL Delete]* （既定値）：指定された終了時刻が到達したときに、関連するすべてのコンポーネントを削除します。 この操作を元に戻すことはできません。

* *[!UICONTROL Pause]:*&#x200B;指定された終了時刻が届いたときに、関連するすべてのコンポーネントを一時停止します。 必要に応じて、後でコンポーネントを再アクティブ化できます。

* *[!UICONTROL None]:*&#x200B;関連するコンポーネントのステータスを変更しないでください。

**[!UICONTROL Missing line items in a manually uploaded feed]:**&#x200B;既存のアイテムが、手動でアップロードされた新しいフィード ファイルに含まれていない場合、またはテンプレートのマップのみの設定に従って既存のキャンペーンまたは広告グループにマッピングされない場合の対処方法：

* *[!UICONTROL Delete]:*&#x200B;既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:*&#x200B;既存のコンポーネントを一時停止します。 新しいフィード ファイルに同じ行アイテムが含まれ、履歴と品質スコアが保持されている場合は、再アクティブ化されます。 **注意：**&#x200B;親製品グループの子製品グループがすべて見つからない場合、製品グループを一時停止できないため、親製品グループは削除されます。

* *[!UICONTROL None]* （既定値）：既存のコンポーネントは変更しないでください。

**[!UICONTROL Missing line items in an FTP feed/GMC account]:**&#x200B;既存のアイテムが1）含まれていない場合の対処法a）新しいフィードファイルの中のFTP ディレクトリにアップロードされたアイテムまたはb）マーチャント センターのアカウントの次回のSearch, Social, &amp; Commerceが同期する場合、または2）テンプレートの[!UICONTROL Map Only]設定に従って既存のキャンペーンまたは広告グループにマッピングされない場合。

* *[!UICONTROL Delete]:*&#x200B;既存のコンポーネントを削除します。

* *[!UICONTROL Pause]:*&#x200B;既存のコンポーネントを一時停止します。 新しいデータに同じ行アイテムが含まれ、履歴と品質スコアが保持されると、再アクティブ化されます。 **注意：**&#x200B;親製品グループの子製品グループがすべて見つからない場合、製品グループを一時停止できないため、親製品グループは削除されます。

* *[!UICONTROL None]* （既定値）：既存のコンポーネントは変更しないでください。

**[!UICONTROL When a numeric stock level reaches N units, or where a text-based value is 'out of stock']:**&#x200B;次の場合に在庫レベルを含む行項目の処理：

* （指定列に数値のみの在庫値を含むフィードの場合）在庫レベルが指定数量を下回っています。 デフォルトの数量はゼロ（0）です。

* （指定された列にテキスト値を含むフィードの場合） [!UICONTROL Availability]の値は「[!UICONTROL out of stock]」です。値では大文字と小文字が区別されません。 **注：** **フィード テンプレートでは、「[!UICONTROL This column has non-numeric values]」のチェック ボックスを使用して、テキストベースの在庫レベル列を示します。

両方の場合のアクションを選択します。

* *[!UICONTROL Delete]* （既定値）コンポーネントを削除します。

* *[!UICONTROL Pause]:* コンポーネントを一時停止します。 データが更新されると、在庫数値が指定された数量を超えた場合、または[!UICONTROL Availability]が「[!UICONTROL in stock]」または「[!UICONTROL preorder]」の場合、コンポーネントが再アクティブ化されます。 コンポーネントは履歴と品質スコアを保持します。

各行項目の在庫レベルは、各テンプレートの「[!UICONTROL Stock Level]」フィールドで指定されているように、フィードファイルの列から取得されます。

>[!TIP]
>
>* 再入荷したり、利用可能性を高めたりすると予想される製品やサービスの場合は、広告グループ、キーワード、広告を削除して再作成するのではなく、一時停止する必要があります。 一時停止すると、品質スコアを保持できます。
>* 広告グループに対して古い自動処理を有効にし、新しいデータに広告グループの在庫レベルが含まれる場合は、指定された在庫レベルがブランド/アイテムのレベルではなくカテゴリーレベルにある場合にのみ、広告グループを削除または一時停止することが意味があります。 例えば、広告グループ「コンバーチブル」がある場合、広告グループの在庫レベルは、広告グループで表されるすべての個々のコンバーチブルモデルの合計である必要があります。

**[!UICONTROL Propagate feed data through all applicable templates]:** （FTPまたはマーチャント センターのアカウントを介してデータ ファイルをアップロードする広告主）は、該当するテンプレートを通じて新しいデータを自動的に伝達します。 このオプションはデフォルトで選択されています。 このオプションを無効にした場合でも、任意のフィードファイルやアカウント、または任意のテンプレートのデータを手動で反映できます。

>[!NOTE]
>
>* FTP ファイルの場合、フィードサービスは2時間ごとにFTP ディレクトリの更新を確認します（PST タイムゾーンの偶数時間数）。 このオプションは、前回のチェック以降にアップロードされたすべてのファイルを処理します。
>* マーチャント センターのアカウントの場合、Search、Social、およびCommerceは、広告主のタイムゾーンの約06:00で毎日アカウントと同期します。 このオプションは、前回の同期以降に更新されたすべてのデータを処理します。
>* データが広告ネットワークまたは[!UICONTROL Bulksheets] ビューに投稿されるまで、伝達されたデータは[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]、[!UICONTROL Ads]のタブから利用できます。

**[!UICONTROL Post to the SE]:** （広告主がFTPまたはマーチャント センターのアカウントを介してデータ ファイルをアップロードしている場合）は、新しいデータが該当するテンプレートを通じて伝達された後、関連する広告ネットワークに適した形式でバルクシート ファイルを自動的に作成します。 このオプションは、サブコンポーネントにエラーがない限り、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Keywords]および[!UICONTROL Ads] タブからもデータを削除します。

このオプションはデフォルトでは無効です。 このオプションを有効にするには、チェックボックスをオンにし、バルクシートファイルを広告ネットワークに投稿するかどうかを指定します。

* *[!UICONTROL Immediately]* （既定値）: データがテンプレートを通じて伝達された後、一括シート ファイルを関連する広告ネットワークに投稿します。 バルクシートファイルは、30日間[!UICONTROL Bulksheets] ビューで引き続き利用できます。

* *[!UICONTROL Preview in Bulksheet Management area only, post later]:**は、バルクシート ファイルを関連する広告ネットワークに投稿しませんが、後で投稿できる[!UICONTROL Bulksheets] ビューに一覧表示します。 バルクシートファイルは、30日間[!UICONTROL Bulksheets] ビューで引き続き利用できます。 バルクシートファイルが10 MBを超えて2 GB未満の場合、ファイルはZIP形式になります。投稿するためにファイルを解凍する必要はありません。 **ヒント：**&#x200B;以前にランディングページを検証していない場合は、このオプションを使用して、データを広告ネットワークに投稿する前に[!UICONTROL Bulksheets] ビューから検証できます。

**[!UICONTROL Exclude keywords from posting when keyword length is greater than]:**&#x200B;は、指定された文字数以上のキーワードフレーズを広告ネットワークに投稿することを禁止します。 このオプションを選択すると、最大文字数を超えるキーワードフレーズが反映され、[!UICONTROL Keywords] タブに表示されますが、データを投稿しようとすると投稿されません。

このオプションはデフォルトでは無効になっているので、フレーズに含まれる単語の数に関係なく、すべてのキーワードが投稿されます。 このオプションを選択した場合は、投稿する最大文字数（3 ～ 10）を選択します。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [ テンプレートを通じてフィード データを伝達](/help/search-social-commerce/campaign-management/inventory-feeds/feed-data-propagate.md)
>* [ フィードから生成されたキャンペーンデータを広告ネットワークに投稿](propagated-data-post.md)
