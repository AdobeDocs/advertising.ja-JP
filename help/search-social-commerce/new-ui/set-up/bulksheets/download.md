---
title: （新しいUI）バルクシートファイルのダウンロード/作成
description: 新しい検索、ソーシャル、Commerce UIで広告ネットワークのアカウントデータをダウンロードして、バルクシートファイルを作成する方法を説明します。
feature: Search Bulksheets
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: e58024d1-d6da-420c-80af-6be211808316id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 1637
ht-degree: 0%

---

# （新しいUI）バルクシートファイルのダウンロード/作成

1つ以上の[ サポートされている広告ネットワーク ](about.md#bulksheet-functionality-by-network)で、1つ以上のアカウントのカスタム設定を使用してバルクシートを作成できます。 Bulksheetsには、Search, Social, &amp; Commerce内のデータが含まれます。

同期済みキャンペーンの場合は、データをダウンロードする前にオプションで広告ネットワークと同期して、広告ネットワーク側の最近のデータ変更を確実に含めることができます。 すべての広告ネットワークに対して、オプションで、ファイルに含める新しいクリックトラッキング URLを生成できます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Bulksheets]**&#x200B;をクリックします。

1. ツールバーで、**[!UICONTROL Bulk Operations]** \> **[!UICONTROL Download Bulksheet]**&#x200B;をクリックします。

1. [ バルクシート設定](#bulksheet-settings)を指定します。

   1. 「**[!UICONTROL Selections]**」タブで、バルクシートのオプションを含めたり設定したりするアカウント、キャンペーン、または広告グループを選択します。

   1. （オプション）「**[!UICONTROL Rows and Columns]**」タブをクリックし、バルクシートに行を含めるアカウントコンポーネントとコンポーネントステータスを指定し、選択した各コンポーネントに含める列を指定します。

      使用可能なバルクシート行のリストについては、「[広告ネットワーク別バルクシート行](#bulksheet-rows-by-ad-network)」を参照してください。

   1. （オプション）「**[!UICONTROL Filters]**」タブをクリックし、バルクシートに含める特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、プレースメント、その他のエンティティの条件を指定します。

1. **[!UICONTROL Download]**&#x200B;をクリックします。

タスクが開始されると、ウィンドウに通知が表示されますが、開いたままなので、必要に応じて追加のバルクシートを作成し続けることができます。 ファイルを作成すると、ファイルへのリンクが記載されたメール通知が届きます。編集するデータ量によっては、通知に数分以上かかる場合があります。 ファイルの生成に失敗した場合は、エラーファイルが一括処理ビューに表示され、エラーファイルへのリンクを含むメール通知が届きます。

## バルクシート設定 {#bulksheet-settings}

### 「選択」タブ {#bulksheet-selections-settings}

**\[ アカウント、キャンペーン、広告グループの選択\]**

ネットワークとアカウントの階層を展開し、バルクシートにデータを含める各アカウント、キャンペーン、または広告グループの横にあるチェックボックスを選択します。

* アカウントのすべてのキャンペーンと広告グループを含めるには、アカウント名の横にあるチェックボックスをオンにします。

* 特定のキャンペーンを含めるには、アカウントを展開し、含める各キャンペーンの横にあるチェックボックスを選択します。 特定の広告グループを含めるには、キャンペーンをさらに展開し、各広告グループの横にあるチェックボックスをオンにします。

>[!NOTE]
>
>* 1つのバルクシートを複数の広告ネットワーク内の複数のアカウントに適用することができます。 広告ネットワーク固有の列には、広告ネットワーク名（「Mobile Carriers （Google Ads）」など）が付いたバルクシートでラベル付けされます。
>* アイテムの種類を確認するには、アイテムの上にカーソルを置きます。
>* デフォルトでは、アクティブなアカウントと有効なアカウントとそのアクティブなコンポーネントのみが一覧表示されます。

**[!UICONTROL Generate Tracking URLs]:** （オプション）トラッキングテンプレートを持つアカウントのトラッキングテンプレートとランディングページのサフィックス（該当する広告ネットワークの場合）、またはターゲット URLを持つアカウントのトラッキングコードを持つ宛先URL （キーワード、広告、プレースメント、サイトリンク、およびバルクシートの[!DNL Google Ads]製品グループ）を含みます。 デフォルトでは、このオプションが選択されています。

このオプションを選択すると、アカウント設定またはキャンペーン設定の[!UICONTROL Campaign Tracking] セクションのパラメーターに従ってURLが生成されます。 デフォルトでは、トラッキング URLが既に存在する場合、新しいURLが必要でない限り再生成されません（例えば、キーワードの一致タイプ、広告テキスト、アカウントのトラッキングパラメーターが変更された場合など）。

>[!NOTE]
>
>* 広告主がAdobe Advertising コンバージョントラッキングを使用しており、関連するアカウントがトラッキング URLを自動生成してアップロードするように設定されていない場合は、ベース URLが変更されたときに新しいトラッキング URLを生成する必要があります。
>* このオプションを選択しない場合でも、後でファイルをアップロードまたは投稿するときにトラッキング URLを生成できます。

**[!UICONTROL Perform pre-sync]:** （オプション）すべてのデータが同じであることを確認するために、Search、Social、およびCommerceで指定されたキャンペーンとファイルを同期するように指示します。 デフォルトでは、このオプションは選択されていません。

>[!NOTE]
>
>Search, Social, &amp; Commerceは、1日1回、広告ネットワーク上で新しいキャンペーンを検出するたびに、Search, Social, &amp; Commerce内からキャンペーンデータを変更するたびに、広告ネットワークと自動的に同期します。 広告ネットワークまたは広告ネットワークのデスクトップエディターを使用して、キャンペーンやアカウントのデータに対する最近の変更が直接行われたと思われる場合は、このオプションを選択します。 このオプションを選択すると、一括作成に時間がかかります。

**[!UICONTROL Bulksheet Name]:**&#x200B;新しいバルクシートの名前とファイルの種類。 デフォルトでは、ファイルはタブ区切りの値フォーマットで作成され、次のいずれかの名前が付けられます。

* （広告ネットワークのすべてのアカウント） `<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* （1つのアカウントの場合） `<account name>_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`
* （複数のアカウントの場合） `MultipleAccounts_<search_engine name>_<creation date in the format MMDDYYYY>.tsv`

ファイルの名前を変更できます。 名前に次の文字を含めることはできません：`# % & * | \ : " < > . ? /`

必要に応じて、ファイルの種類を変更します。 オプションには、*[!UICONTROL .tsv]* （タブ区切り値の場合）、*[!UICONTROL .txt (unicode)]* （Unicode準拠のASCII テキストの場合）、*[!UICONTROL .csv]* （コンマ区切り値の場合）、または&#x200B;*[!UICONTROL .zip]* （圧縮されたZIP形式の場合、TSV ファイルに展開）が含まれます。

>[!TIP]
>
>国際文字を含むバルクシートの場合は、TSVまたはTXT形式を使用します。

### 「行と列」タブ {#bulksheet-rows-columns-settings}

**[!UICONTROL Bulksheet Rows]:** エンティティとそれに対応するステータスは、バルクシートにデータ行として含め、エントリごとに1行にします。 例えば、アクティブなキャンペーンを含める場合、バルクシートにはアクティブなキャンペーンごとに1行が含まれます。 選択したステータスを持つ選択したエンティティのみが含まれます。 デフォルトは、指定した広告ネットワークに基づいて事前に選択されています。 デフォルトでは、選択したエンティティのアクティブなインスタンスのみが含まれます。

エンティティを追加または削除するには、エンティティの横にあるチェックボックスをオンまたはオフにします。 エンティティのステータスを追加または削除するには、エンティティの横にあるステータスメニューをクリックし、該当するステータスのチェックボックスをオンまたはオフにします。

広告ネットワーク別の使用可能な行のリストについては、「[広告ネットワーク別のバルクシート行](#bulksheet-rows-by-ad-network)」を参照してください。

**[!UICONTROL Cascading Status Hierarchy]:**&#x200B;は、AND操作を使用して、指定された親エンティティのステータスを持つエンティティに子エンティティをフィルタリングします。 例えば、「Active Campaign」、「Active Adgroup」、「Active Keyword」を選択した場合、バルクシートには、アクティブなキャンペーンのアクティブな広告グループ内のアクティブなキーワードのみが含まれます。

このオプションを選択しない場合、親ステータスは考慮されず、フィルターはOR操作を使用します。 例えば、「Active Campaign」、「Active Adgroup」、「Active Keyword」を選択した場合、バルクシートには、アクティブなすべてのキャンペーン、親キャンペーンのステータスに関係なくすべてのアクティブな広告グループ、親キャンペーンと広告グループのステータスに関係なくすべてのアクティブなキーワードが含まれます。

**[!UICONTROL Bulksheet Columns]:** ダウンロードしたバルクシート ファイルに含める列：

* *[!UICONTROL AMO ID]:* （「[!UICONTROL SE ID]」が選択されていない場合は必須）各エンティティ/行に[!DNL Adobe]が生成した一意のIDが含まれます。 Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、広告ネットワークには投稿しません。 後で、エンティティ IDと親エンティティ IDではなく、[!UICONTROL AMO ID]を識別子として使用して、エンティティのデータを編集できます。

* *[!UICONTROL SE ID]:* （「[!UICONTROL AMO ID]」が選択されていない場合は必須）含まれる各列とその親エンティティに対する広告ネットワークの一意のIDが含まれます。 後で、[!UICONTROL SE ID]を識別子として使用して任意のエンティティのデータを編集する場合は、親エンティティの行（[!UICONTROL SE ID]の値を含む）も含める必要があります。

* *[!UICONTROL Platform]:*&#x200B;各行の先頭に[!UICONTROL Platform]列が含まれ、広告プラットフォーム（「Baidu」など）を示します。

* *[!UICONTROL Acct Name]:* （「[!UICONTROL AMO ID]」が選択されていない場合は必須）各エンティティ/行の広告ネットワークアカウント名が含まれます。

* \[ エンティティ固有の列\]: [!UICONTROL Bulksheet Rows]で選択した各エンティティに関連するすべての列、なし、または選択した列のみを含めるには、エンティティ名の横にある![右矢印](/help/search-social-commerce/assets/compressed-item.png "右矢印")をクリックして展開し、個々の列のチェックボックスを選択またはオフにします。 デフォルトでは、選択した各エンティティ行に関連するすべての列が含まれます。

>[!TIP]
>
>バルクシートファイルの各行にアイテムを識別するための適切な列を含めるようにしてください。 例えば、[!UICONTROL Bulksheet Rows] セレクターにキーワード行を含めながら、キーワードに関連するすべての列を除外した場合、結果のバルクシートには、キーワードインスタンスごとに1つの行が含まれますが、どのキーワードインスタンスが特定の行に属しているかは特定できません。 この場合、適切なID列と値を手動で追加しない限り、バルクシートを使用してデータを更新することはできません。

### 「フィルター」タブ {#bulksheet-filters-settings}

特定のキャンペーン、広告グループ、広告/クリエイティブ、キーワード、またはバルクシートに含める配置の条件：

1. パラメーター（エンティティ名またはID、またはクリエイティブ、キーワード、またはプレースメントの任意の要素）を選択し、演算子を選択して、該当する値を入力します。

   例えば、[!DNL Google Ads] アカウントの見出しに「shoes」が付いた広告のみを返すには、*[!UICONTROL Headline]*&#x200B;を選択し、*[!UICONTROL contains]*&#x200B;を選択して、入力フィールドに`shoes`と入力します。

1. （追加のフィルターを適用するには）追加の各フィルターについて、**[!UICONTROL +Add Filter]**&#x200B;をクリックし、**[!UICONTROL AND]**&#x200B;または&#x200B;**[!UICONTROL OR]**&#x200B;を選択し、広告要素またはキーワードと演算子を選択して、該当する値を入力します。

## 広告ネットワーク別のバルクシート行 {#bulksheet-rows-by-ad-network}

| バルクシート行 | [!DNL Baidu] | [!DNL Google Ads] | [!DNL LY Ads] | [!DNL Microsoft Advertising] | [!DNL Naver] | [!DNL Pinterest] | [!DNL Yahoo! Display Network] | [!DNL Yahoo Native] | [!DNL Yandex] | メモ |
|----|----|----|----|-------|----|----|----|----|----|----|
| [!UICONTROL Campaign] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Adgroup] | はい | はい | はい | はい | はい | はい | はい | はい | はい | — |
| [!UICONTROL Creative] *または* [!UICONTROL Creative (except RSA)] | はい | はい | はい | はい | — | — | はい | はい | はい | （[!DNL Google Ads]） [!UICONTROL Responsive Search Ad]行にあるレスポンシブ検索広告を除くすべての広告タイプで使用します。 |
| [!UICONTROL Responsive Search Ad] | — | はい | — | はい | — | — | — | — | — | — |
| [!UICONTROL Keyword] | はい | はい | はい | はい | はい | はい | — | はい | はい | 非負のキーワードにのみ使用します。 キャンペーンまたは広告グループレベルで作成された否定的なキーワードを表示するには、使用可能な場合は[!UICONTROL Campaign Negative Keyword]行または[!UICONTROL Adgroup Negative Keyword]行を使用します。 |
| [!UICONTROL Promoted Pin] | — | — | — | — | — | はい | — | — | — | — |
| [!UICONTROL Placement] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Auto Target] | — | はい | — | はい | — | — | — | — | — | 広告グループの動的検索ターゲットに使用します。 |
| [!UICONTROL Shopping Product Group] | — | はい | — | はい | — | — | — | — | — | — |
| [!UICONTROL Campaign Site Link] | — | はい | — | はい | — | — | — | はい | — | — |
| [!UICONTROL Campaign Negative Keyword] | はい | はい | はい | はい | — | — | — | はい | — | キャンペーンまたは広告グループレベルで作成されたネガティブキーワードにのみ使用します。 負でないキーワードを表示するには、使用可能な場合は[!UICONTROL Keyword]行を使用します。 |
| [!UICONTROL Campaign Negative Website] | — | はい | — | はい | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Site Link] | — | はい | — | — | — | — | — | はい | — | — |
| [!UICONTROL Creative Site Link] | — | — | — | — | — | — | — | — | はい | — |
| [!UICONTROL Adgroup Negative Keyword] | はい | はい | はい | はい | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Negative Website] | — | はい | — | はい | — | — | — | — | — | — |
| [!UICONTROL Campaign Location Target] | はい | はい | はい | はい | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Location Target] | — | — | — | はい | — | — | — | はい | — | — |
| [!UICONTROL Campaign Device Target] | — | はい | — | はい | — | — | — | はい | — | — |
| [!UICONTROL Adgroup Device Target] | — | はい | — | はい | — | — | — | はい | — | — |
| [!UICONTROL Campaign RLSA Target] | — | はい | — | はい | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Target] | — | はい | — | はい | — | — | — | — | — | — |
| [!UICONTROL Campaign RLSA Negative] | — | はい | — | — | — | — | — | — | — | — |
| [!UICONTROL Adgroup RLSA Negative] | — | はい | — | — | — | — | — | — | — | — |

各広告ネットワークの必須列とオプション列について詳しくは、広告ネットワーク固有のバルクシート データ形式の記事を参照してください。

* [ [!DNL Baidu]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)
* [ [!DNL Google Ads]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)
* [ [!DNL LY Ads]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md)
* [ [!DNL Microsoft Advertising]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)
* [ [!DNL Naver]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
* [ [!DNL Yahoo! Display Network]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)
* [ [!DNL Yandex]  アカウントの必須およびオプションのバルクシート データ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)

>[!MORELIKETHIS]
>
>* [ （新しいUI）バルクシートを使用したキャンペーンデータの管理について](about.md)
>* [ （新しいUI） バルクシートまたは修正されたエラーファイルをアップロード ](upload.md)
>* [ （新しいUI）バルクシートの投稿またはエラーファイルの修正](post.md)
>* [ （新しいUI）バルクシート ファイルのランディングページを検証](validate-landing-pages.md)
