---
title: ' [!DNL Google Ads]  アカウントに必要なバルクシートデータ'
description: ' [!DNL Google Ads]  アカウントの必須ヘッダーフィールドとデータフィールドを一括シートで参照します。'
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/mxs4XjmBxho29VLjSzREkA-w6eWMn6e-8cXihLgh7ZA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 7898
ht-degree: 0%

---

# 付録 – [!DNL Google Ads] アカウントに必要なバルクシート データ

[!DNL Google Ads]件のキャンペーンデータを一括で作成および更新するには、[!DNL Google Ads]件のアカウントに特化してフォーマットされたSearch、Social、およびCommerceのバルクシート ファイルを使用できます。 a） [必要なファイル形式で既存のアカウントの一括シートファイルを生成するか、b）手動で作成できます（サポートされているファイル形式に関する一般的な情報については、「](../bulksheet-download.md) サポートされている一括シートファイル形式[」を参照）。](bulksheet-file-formats.md)

各バルクシートには、実行する[特定の操作（広告の作成など）に必要なヘッダーフィールドと対応するデータフィールドを含める必要があります。 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)フィールドが必須でない場合は、ヘッダー行とデータ行からフィールドを省略できます。 一括シートファイルをアップロードすると、すべてのカスタム列が削除されます。

次に、利用可能なすべてのデータフィールドの表と、個々のエンティティ（キャンペーンやキーワードなど）のデータを追加、編集、または削除するために必要なフィールドを示す追加の表を示します。

## 使用可能なすべてのデータフィールド {#bulksheet-fields-all-google}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、「[各アカウントコンポーネントの作成、編集、または削除に必要なフィールド &#x200B;](#bulksheet-fields-per-component-google)」を参照してください。

>[!NOTE]
>
>* すべてのテキスト列の値では、大文字と小文字が区別されます。
>* 新しいレコードを作成し、すべての必須データフィールドの値を含まない場合、これらのフィールドの一部には、指定されたデフォルト値が割り当てられます。
>* 以下に指定されていないフィールドの場合、広告ネットワークのデフォルト値が使用されます。
>* [!UICONTROL Download Bulksheet] ダイアログで使用可能なバルクシート行のリストについては、「[広告ネットワーク別バルクシート行](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)」を参照してください。

| フィールド | 説明 |
| ---- | ---- |
| [!UICONTROL Platform] | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | 金銭的な記号や句読点の有無にかかわらず、キャンペーンの1日の支出制限。 この値は上書きされますが、アカウントの予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | <p>キャンペーンの広告を毎日表示する速度：</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを一日中広げます。</p></li><li><p><i>[!UICONTROL Accelerated]:</i> （2019年10月に非推奨）予算に達するまで、広告を可能な限り頻繁に表示します。 その結果、広告が後で表示されない場合があります。</p></li></ul> |
| [!UICONTROL Channel Type] | <p>広告を配置するチャネル。 1つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Search]</i> （新しいキャンペーンのデフォルト）: [!DNL Google Ads]検索ネットワーク（[!DNL Google Ads]検索および検索パートナーのweb サイトを含む）およびオプションで[!DNL Google Ads]表示ネットワークにも広告を配置します。 <b>注：</b>検索ネットワークと表示ネットワークの両方をターゲットとするキャンペーンは、入札最適化のポートフォリオに追加できません。</p></li><li><p><i>[!UICONTROL Display]</i>: [!DNL Google Ads] ディスプレイ ネットワークにのみ広告を配置するには。</p></li><li><p><i>[!UICONTROL Shopping]</i>: [!DNL Google Ads]個のショッピング ネットワーク （一部の国）と[!DNL Google Ads]個の検索ネットワーク （[!DNL Google Ads]個の検索および検索パートナーのweb サイトを含む）にショッピング広告を配置します。 ショッピング広告を作成するには、[!DNL Google Merchant Center] アカウントに商品があり、[Search, Social, &amp; Commerceがアカウントからデータをダウンロードできるようにする](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)必要があります。 ショッピング広告の作成プロセスについて詳しくは、「[実装 [!DNL Google Ads]  ショッピングキャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)」を参照してください。</p></li></ul> |
| [!UICONTROL Networks] | <p>広告を配置する場所。 1つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Google Search]</i>: Google Search Networkでのみスポンサー付き検索リストが表示されます。</p></li><li><p><i>[!UICONTROL Search Partners]</i>: Googleの検索パートナーのスポンサー検索リスト。</p></li><li><p><i>[!UICONTROL Content]</i>：表示ネットワーク リストの入札を配置します。</p></li><li><p><i>[!UICONTROL All]</i> （新しいキャンペーンのデフォルト）: Google Search、Search Partners、Contentをターゲットにします。</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>（検索ネットワークのみ。拡張された動的検索広告にのみ適用されます）広告ネットワークが動的検索広告のターゲットに使用するコンテンツを含むweb サイトのルートドメイン（example.comなど）またはサブドメイン（shoes.example.comなど）。<br><br><b> メモ：</b></p><ul><li><p>キーワードではなく、web サイトのコンテンツをターゲットとする動的検索広告を拡大。</p></li><li><p>ターゲットにするドメインは、広告ネットワークのオーガニック検索インデックスでインデックス付けする必要があります。</p></li><li><p>ドメインを指定しない場合は、各広告グループに対して、すべてのweb サイトページまたはそのサブセットをターゲットとする動的検索ターゲットを作成する必要があります。</p></li></ul> |
| [!UICONTROL DSA Domain Language] | （検索ネットワークのみ。拡張された動的検索広告にのみ適用）指定したweb サイトドメインの言語。 <b>注：</b> ドメインに複数の言語のページが含まれており、それらすべてをターゲットにする場合は、各言語に対して個別のキャンペーンを作成します。 |
| [!UICONTROL GDN Custom Bid Level] | （ディスプレイネットワークのみをターゲットとするキャンペーン）入札方法：<i>[!UICONTROL Ad Group]</i> （デフォルト）、<i>[!UICONTROL Keyword]</i>、<i>[!UICONTROL Placement]</i> （web サイト）、または<i>[!UICONTROL None]</i> （既存の値をリセットする）による。 その他のディメンション（<i>Age</i>、<i>Gender</i>、<i>Interest and List</i>、<i>Topic</i>、および<i>Vertical</i>）は、[!DNL Google Ads] インターフェイスから利用できます。 [!DNL Google Ads] インターフェイスを使用して別のディメンションによる入札を設定した場合、その値は表示されますが、これらのディメンションを選択または入力することはできません。</p><p><b> メモ：</b></p><ul><li><p>キーワードで入札する場合は、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメントで入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他のディメンションについては、広告レベルでトラッキングテンプレートを作成します。</p></li><li><p>サポートされていないディメンション（年齢、性別、興味関心、リスト、トピック）で入札した場合、Search, Social, &amp; Commerceではディメンションの入札が最適化されず、すべてのアトリビューションが広告グループに適用されます。</p></li><li><p>検索ネットワーク上の広告は、常にキーワード入札を使用します。</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>（ショッピングキャンペーンのみ）複数のキャンペーンが同じ製品を宣伝する際にキャンペーンが使用される優先度：<i>[!UICONTROL Low]</i> （新しいキャンペーンのデフォルト）、<i>[!UICONTROL Medium]</i>、または<i>[!UICONTROL High]</i>。</p><p>同じ製品が複数のキャンペーンに含まれている場合、広告ネットワークは、最初にキャンペーンの優先順位を使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを決定します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Has EU Political Ads] | （欧州連合（EU）のオーディエンスをターゲットとするキャンペーンに適用されます） キャンペーンに、EU規則2024/90に基づいて欧州連合で提供される広告の要件に従った政治的広告が含まれているかどうか：<i>[!UICONTROL Yes]</i>または<i>[!UICONTROL No]</i>。 |
| [!UICONTROL Merchant ID] | （ショッピングキャンペーンとオーディエンスキャンペーンは加盟店フィードにリンクされている場合のみ）キャンペーンに使用される製品の加盟店アカウントの顧客ID。 |
| [!UICONTROL Sales Country] | （ショッピングキャンペーンのみ。既存のキャンペーンの読み取り専用）キャンペーンの製品が販売される国。 製品はターゲット国に関連付けられているため、この設定によって、キャンペーンで宣伝される製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （ショッピングネットワーク [!DNL Google Ads]を使用するキャンペーンのみ） キャンペーン用にショッピング広告を作成できる[!DNL Google Merchant Center] アカウント内の製品。 dimension=attribute形式を使用して、商品をフィルタリングする商品ディメンションと属性の組み合わせを最大7つ入力できます。 「>>」区切りで複数のフィルターを区切ります。 使用可能な製品ディメンションのリストについては、「[&#x200B; ショッピングキャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。</p><p>例：「CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies」</p><p>既存の値を削除するには、値<code>[delete]を使用します</code> （括弧を含む）。</p> |
| [!UICONTROL Languages] | <p>（検索および表示ネットワークのみ）キャンペーン内の広告のターゲット言語。</p><p>このフィールドまたは新しいキャンペーンの[!UICONTROL Geo Targeting] フィールドの値を入力しない場合、アカウントに指定された通貨によってデフォルトの言語が決まります。ただし、特定の言語（EURなど）にマッピングされていない通貨を含むキャンペーンは、すべての言語を対象としています。 このフィールドに値を入力せずに、新しいキャンペーンの[!UICONTROL Geo Targeting] フィールドに値を入力した場合、デフォルトは<i>[!UICONTROL All]</i>になります。 既存のキャンペーンでこのフィールドを空白のままにすると、既存の値が保持されます。</p><p>すべての言語をターゲットにするには、<span style="font-style: italic;">&lt;i&lt;ph[!UICONTROL >All]</i></span>と入力します。 特定の言語をターゲットにするには、<a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads]の言語名</a> （<i>英語；日本語</i>など、正しい数値コードで置換）または数値コード（<i>1000;1005</i>など）を使用して、セミコロンで区切られた値を入力します。 値では大文字と小文字は区別されません。</p> |
| [!UICONTROL Location] | キャンペーン用に広告を配置する場所、または広告を除外する場所。 このフィールドまたは新しいキャンペーンの「言語」フィールドに値を入力しない場合、アカウントに指定された通貨によってデフォルトの場所が決まります。ただし、特定の場所（EURなど）にマッピングされていない通貨を含むキャンペーンは、すべての場所が対象となります。 このフィールドに値を入力せずに、新しいキャンペーンの[!UICONTROL Languages] フィールドに値を入力した場合、デフォルトは<i>[!UICONTROL All]</i>になります。 既存のキャンペーンでこのフィールドを空白のままにすると、既存の値が保持されます。</p><p>特定の場所をターゲットにするには、[[!DNL Google Ads] 場所の名前](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （正しい数値コードで置き換えられます）または場所コードのいずれかを使用します。</p><ul><li><p>国/地域：国/地域の名前（<i>United States;Japan</i>など）または数値コード（<i>2840;2392</i>など）を入力します。</p></li><li><p>州/県/地域：関連する国/地域の略語（<i>Tokyo, JP;New York, US</i>など）または数値コード（<i>20636;21167</i>など）を使用して、州/県/地域名を入力します。</p></li><li><p>米国以外の都市：市名、都道府県/地域名、国/地域の略語（<i>足立、東京、日本、北、東京、日本</i>など）または数値コード（<i>1028850;1009293</i>など）を入力します</p></li><li><p>米国のメトロ地域：市名、州名、国名の略語（<i>Buffalo NY, US;New York NY, US</i>など）または数値コード（<i>514;501</i>など）を入力します。</p></li></ul><p>場所を除外するには、場所の名前またはコードの前に`-`-Japan<i>などのマイナス記号（</i>）を付けます。</p><p><b>注意：</b>値では大文字と小文字は区別されません。</p> |
| [!UICONTROL Location Type] | （場所を含める場合） [場所タイプ &#x200B;](https://developers.google.com/google-ads/api/data/geotargets)。 |
| [!UICONTROL Device] | キャンペーンまたは広告グループレベルで入札調整が行われるデバイスタイプ：<i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>、または<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | <p>（ターゲット [!UICONTROL Location]、[!UICONTROL Device]または[!UICONTROL RLSA]を含める場合）特定の場所、特定のデバイスタイプ、または特定のオーディエンスターゲットを使用して広告の入札額を調整するかどうか：</p><ul><li><p>キーワードレベルの入札（0%の差）を使用するには、0と入力します。 新しいターゲットの場合は、空白のままにすることもできます。</p></li><li><p>このターゲットに別の入札額を使用するには、入札額を増減する割合を入力します。</p></li><ul><li><p>場所とRLSAのターゲットの場合、有効な割合は–90 ～ 900です。</p></li><li><p>デバイス入札調整の場合、有効なパーセンテージは次のとおりです。</p></li><ul><li><p>（キャンペーン）–100 （デバイスタイプの広告には入札しない）、-90 ～ 900の範囲で設定します。</p></li><li><p>（広告グループ） - 100 スマートフォンやタブレットの場合（デバイスの種類に入札しない場合）、およびすべてのデバイスの種類に対して–90から900まで。</p></li></ul></ul><li><p>（既存のキャンペーンと広告グループ）既存の入札調整を使用するには、空白のままにします。</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | （情報目的で生成されたバルクシートに含まれる） Adobeがキャンペーンレベルの場所ターゲットまたはRLSAに推奨する読み取り専用の入札調整。 キャンペーンが重み付けされたコンバージョン指標を使用する目的を持つポートフォリオ内にあり（[!UICONTROL Maximize Clicks]の目的ではない）、キャンペーンに少なくとも2つのロケーションターゲットまたは過去90日間のコストが少なくとも5 クリックまたは5米ドルのRLSAが含まれている場合にのみ計算されます。</p><p>推奨値を使用するために位置情報ターゲットまたはRLSAを手動で編集する場合は、位置情報ターゲットまたはRLSAを作成してから少なくとも2週間待って、十分なデータ収集を行い、値を週に1回以上変更しないでください。 |
| [!UICONTROL Device Targets] | <p>（従来のキャンペーンタイプのみ）広告を表示するデバイス：<i>[!UICONTROL All]</i>、<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Smartphones]</i>、または<i>[!UICONTROL Tablets]</i>。 新しいキャンペーンの場合、デフォルトは<i>[!UICONTROL All]</i>です。</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | （従来のキャンペーンの種類のみ。デバイス ターゲットに「スマートフォン」または「タブレット」が含まれている場合に適用されます）広告が表示されるオペレーティングシステム：<i>[!UICONTROL All]</i>、<i>[!UICONTROL Android]</i>、<i>[!UICONTROL iOS]</i>、または<i>[!UICONTROL Palm]</i>。 新しいキャンペーンの場合、デフォルトは<i>[!UICONTROL All]</i>です。</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>（従来のキャンペーンタイプのみ。[!UICONTROL Device Targets]に「[!UICONTROL All]」または「[!UICONTROL Smartphones]」が含まれる場合のみ適用されます） スマートフォンが接続される可能性のある携帯電話会社：<i>[!UICONTROL All]</i>、または&lt;c<i>carrier code</i>>、&lt;<i>country code</i>> （T-Mobile,USなど）が<a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">の利用可能な通信事業者とコードのリストを使用して示す1つ以上の通信事業者。 [!DNL Google Ads]</a>複数のキャリアをセミコロンで区切ります（T-Mobile,US;T-Mobile,GBなど）。 新しいキャンペーンの場合、デフォルトは<i>[!UICONTROL All]</i>です。</p> |
| [!UICONTROL Ad Group Name] | <p>広告グループを識別する一意の名前。 最大長は255文字です。末尾の空白文字は保存されません（例えば、「広告グループ 1」は「広告グループ 1」として保存されます）。 このフィールドは、キャンペーンレベルのサイトリンクまたはキャンペーンレベルのデバイスターゲットには適用されません。</p> |
| [!UICONTROL Ad Group Type] | <p>広告グループの種類：<i>[!UICONTROL Demand Gen]</i> （デマンドジェネレーションキャンペーンのみ）、<i>[!UICONTROL Display]</i> （ディスプレイキャンペーンの場合）、<i>[!UICONTROL Search Dynamic]</i> （拡張動的検索広告の場合）、<i>[!UICONTROL Search Standard]</i> （検索広告の場合）、<i>[!UICONTROL Shopping Product]</i> （ショッピング製品広告の場合）、<i>[!UICONTROL Shopping Showcase]</i> （作成と編集はサポートされていません）、または<i>[!UICONTROL Unknown]</i>。</p> |
| [!UICONTROL Max CPC] | <p>（CPC キャンペーンのみ）広告ネットワーク上の広告クリックに対して支払う最大クリック単価（CPC）で、金銭的な記号と句読点の有無にかかわらず支払われる最高額です。 広告グループとキーワード、商品グループ、動的検索対象の値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 製品グループの場合は、最も低い製品グループ層の値を設定できます。新しい層のデフォルトは、親層から継承されます。</p><p>最適化されたポートフォリオ内の既存の製品グループと動的検索対象の場合、更新は1日のみ有効で、次の最適化サイクル中に上書きされます。</p> |
| [!UICONTROL Max Content CPC] | <p>（CPC キャンペーンのみ）最大クリック単価（CPC）。これは、表示用ネットワークサイトからの広告クリックに対する支払い額として最も高い金額で、金銭記号と句読点の有無にかかわらず使用されます。 プレースメントのターゲットではないキャンペーンでは、広告グループレベルで値を設定および編集できます。</p> |
| [!UICONTROL Audience Target Method] | <p>（検索ネットワークのみのキャンペーン、およびディスプレイネットワーク上の既存の読み取り専用[!DNL Gmail] キャンペーン）次の項目を実行するかどうか：</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>：広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーにのみ広告を表示します。</p></li><li><p><i>[!UICONTROL Bid Only]</i>：他の広告グループレベルの目標を満たす限り、ターゲットオーディエンスに関連付けられていない人にも広告を表示します。</p><p>ただし、特定のオーディエンスに対して高い入札額を設定することで、広告が表示される可能性を高めることができます。</p></li></ul> |
| [!UICONTROL Keyword] | キーワード文字列。 最大長は80文字、10文字以下で、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [ ] ' + . / :`</p><p><b> メモ：</b></p><ul><li><p>広告グループまたはキャンペーンレベルでキーワードを除外するには、[!UICONTROL Match Type]を<i>[!UICONTROL Negative]</i>に設定します。 行に広告グループ名が含まれている場合、広告グループのキーワードは除外されます。 行に広告グループ名が含まれていない場合、キャンペーン全体でキーワードが除外されます。</p></li><li><p>[!DNL Google Ads] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。</p></li></ul> |
| [!UICONTROL Placement] | （コンテンツマッチを使用したキャンペーンのみ）広告を表示するディスプレイネットワーク内のプレースメント。 次のいずれかを指定します。</p><ul><li><p>Web サイト：有効なURLを入力してください。 トップレベルのドメイン、ファーストレベルのサブドメイン、または単一のディレクトリ名を持つドメインを指定できます。 URLに疑問符（?）を含めることはできません。 例：<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>特定のページの広告位置：`<URL> >> <location,sublocation>`形式（`finance.google.com >> Company pages,Top right`など）を使用します。</p></li><li><p>トピック カテゴリ：構文`<category::<category> > <subcategory>`などを使用します（`category::Industries > Energy & Utilities > Oil & Gas`など）。</p></li></ul><p><b> メモ：</b>広告グループまたはキャンペーンレベルでプレースメントを除外するには、[!UICONTROL Match Type]を<i>[!UICONTROL Negative]</i>に設定します。 行に広告グループ名が含まれている場合、広告グループのプレースメントは除外されます。 行に広告グループ名が含まれていない場合、キャンペーン全体のプレースメントは除外されます。</p> |
| [!UICONTROL Auto Target Expression] | <p>（キャンペーン設定で「[!UICONTROL Use my website contents to target my ads]」が有効になっていない場合は必須。それ以外の場合はオプション）広告グループの動的検索ターゲット。</p><p>すべてのターゲットには、アスタリスク（*）を使用します。</p><p>最大3つの動的検索条件をターゲットにするには、形式`<category>=<target>`を使用します。ここで、`<category>`には以下のカテゴリのいずれかを含めることができます。 個々のカテゴリの複数のターゲットを&quot;\[空白\]と\[空白\]&quot;で結合し、&quot;[空白]と[空白]&quot;で複数のカテゴリを結合します。</p><ul><li><p><i>[!UICONTROL Category]</i>：特定の[!DNL Google Ads] コンテンツカテゴリを持つインデックス付きページの拡張動的検索広告を表示します。</p></li><li><p><i>[!UICONTROL URL]</i>：特定のURLを持つインデックス付きページの拡張動的検索広告を表示するには、URL内の任意の場所に値を含めることができます。</p></li><li><p><i>[!UICONTROL Page Title]</i>: ページタイトルに特定のテキストを含むインデックス付きページの拡張動的検索広告を表示します。</p></li><li><p><i>[!UICONTROL Page Content]</i>：特定のコンテンツを含むインデックス付きページの拡張動的検索広告を表示します。</p></li></ul><p>例：url=shoes.example.com and page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | 親プロダクトグループの階層。<br><br>例：`All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>製品グループ （「brand=acme」や「すべての製品」など）。</p><p><b> メモ：</b></p><ul><li><p>指定した商品グループが[!UICONTROL Parent Product Groupings]階層に存在しない場合、Search, Social, &amp; Commerceは、階層の必要な部分を作成します。</p></li><li><p>Search, Social, &amp; Commerceでは、[!UICONTROL All Products] ショッピング キャンペーンで広告グループを作成し、デフォルトの入札額を広告グループのデフォルト入札額に設定すると、「[!DNL Google Ads]」グループが自動的に作成されます。 Search, Social, &amp; Commerceは、商品グループ階層の各レベルで広告グループのデフォルト入札額を使用して、「[!UICONTROL Everything Else]」グループを自動的に作成します。 これらのデフォルトグループを明示的に作成し、それらを除外するか、入札を変更することができます。</p></li><li><p>各広告グループには、「[!UICONTROL All Products]」やその他7つの階層を含め、最大8つの階層の製品グループを含めることができます。</p></li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティションの種類：<i> サブディビジョン </i> （子製品グループがある場合）または<i> ユニット </i> （子製品グループがない場合）。 |
| [!UICONTROL Match Type] | <p>動的検索ターゲットまたは製品グループの場合：動的検索ターゲットまたは製品グループのキーワードマッチングオプション：<i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索ターゲットのデフォルト）、<i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）、または<i>[!UICONTROL Negative Product Group]</i> （製品グループを除外）。</p><p>キーワードの場合：キーワードのキーワードマッチングオプション：<i>[!UICONTROL Broad]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Exact]</i>、または<i>[!UICONTROL Negative]</i> （表示ネットワーク上のキーワードまたはプレースメントを除外するため）。ショッピング広告で使用される製品グループのマッチタイプは<i>[!UICONTROL Product Group]</i>です。 <i>[!UICONTROL Negative]</i>を使用する場合は、除外する一致タイプも含める必要があります（「否定的なフレーズ」など）。</p><p>新しいキーワードの場合、デフォルトは<i>[!UICONTROL Broad]</i>です。 一致タイプまたはキーワード IDの値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。</p><p><b> メモ：</b></p><ul><li><p>一致タイプは、キーワードを使用しない拡張動的検索広告には適用されません。</p></li><li><p>[!DNL Google Ads] キーワードの一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。</p></li><li><p>Broad Match Modifierでは、「Broad」を選択し、近いバリエーションが必要なキーワード内の任意の単語の前に「+」を挿入します（「red」と「shoes」の両方の近いバリエーションが必要な場合は「+red +shoes」など）。 <b>注意：</b>一部の言語で、部分一致と同じ一致の動作が使用されるようになりました。また、2021年7月以降、新しい部分一致のキーワードを作成できていません。 詳しくは、[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/7042511)を参照してください。</p> |
| [!UICONTROL First Page Bid] | （情報目的で生成されたバルクシートに含まれる）検索結果の最初のページに広告を配置するために必要な入札額。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Quality Score] | （情報目的で生成されたバルクシートに含まれる）検索エンジンがキーワードに割り当てた現在の品質スコア。 この値は広告ネットワークには投稿されません）。 |
| [!UICONTROL Creative Preferred Devices] | （テキスト広告、拡張された動的検索広告、強化されたサイトリンク。オプション）広告を表示するデバイスの種類：<i>[!UICONTROL All]</i> （デフォルト）または<i>[!UICONTROL Mobile]</i>。 <i>[!UICONTROL Mobile]</i>を指定すると、ネットワークはデスクトップ ユーザーやタブレット ユーザーではなく、モバイル デバイス ユーザーに広告を表示しようとします。 それ以外の場合、ネットワークは任意のデバイスタイプに広告を表示します。</p><p><b> メモ：</b></p><ul><li><p>この設定を編集できるのは、管理者と[!DNL Adobe] アカウント マネージャーのユーザーのみです。</p></li><li><p>ネットワークは、広告が好みのデバイスタイプで表示されることを保証するものではありません。</p></li><li><p>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンでのみ作成できるか、サイトリンクを含まないキャンペーンにのみ作成できます。</p></li></ul> |
| [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]-15 | （拡張テキスト広告とレスポンシブ検索広告のみ）広告の見出し。各見出しを縦のパイプ（&vert;）で区切ります。 各広告タイトルフィールドの最大長は、ダイナミックテキスト（キーワードや広告カスタマイザーの値など）を含めて、30文字または15文字の2 バイト文字です。</p><p>レスポンシブ検索広告の場合、[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]および[!UICONTROL Ad Title 3]は必須であり、その他のすべての広告タイトルフィールドはオプションです。 必須ではないフィールドの既存の値を削除するには、値<code>[delete]を使用します</code> （括弧を含む）。</p><p>レスポンシブ検索広告の場合は、次の形式を使用して広告カスタマイザーを挿入します。<code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>など、<code>{CUSTOMIZER.Discount:10%}</code></p><p>作成または編集することはできませんが、2022年6月に非推奨となった[!DNL Google Ads]の拡張テキスト広告を削除することはできます。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>（レスポンシブ検索広告のみ。オプション）対応する広告タイトルをピン留めする位置：`[null]` （値なし。これにより、広告タイトルがすべてのポジションに適用されます）、<i>1</i>、<i>2</i>、または<i>3</i>。 例えば、[!UICONTROL Ad Title Position]の値が1の場合、広告タイトルは位置1にのみ表示されます。 デフォルトでは、すべての広告タイトルはnullです（値はありません）。</p><p>既存の値を削除するには、値<code>[delete]を使用します</code> （括弧を含む）。</p><p><b> メモ：</b>複数の広告タイトルを同じ位置に固定できます。 広告ネットワークは、位置にピン留めされた広告タイトルの1つを使用します。 3番目にピン留めされたタイトルは、広告で表示されない場合があります。</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>（拡張された動的検索広告、拡張されたテキスト広告、およびレスポンシブ検索広告のみ）広告の本文。 説明フィールドの最大長は、動的テキスト（キーワードや広告カスタマイザーの値など）を含む90文字または45文字です。</p><p>レスポンシブ検索広告の場合は、次の形式を使用して広告カスタマイザーを挿入します。`{CUSTOMIZER.AdCustomizerName:DefaultText}` （`{CUSTOMIZER.Discount:10%}`など）</p><p>拡張された動的検索広告の場合は、[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]のみを使用してください。 <b> メモ：</b>この広告タイプでは、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</p><p>作成または編集することはできませんが、2022年6月に非推奨となった[!DNL Google Ads]の拡張テキスト広告を削除することはできます。</p><p>レスポンシブ検索広告の場合、[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]は必須であり、[!UICONTROL Description Line 3]と[!UICONTROL Description Line 4]はオプションです。 既存の値を削除するには、値<code>[delete]を使用します</code> （括弧を含む）。</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索の広告のみ。オプション）対応する説明を固定する位置：`[null]` （値なし、すべての位置に対して説明を有効にする）、<i>1</i>、<i>2</i>、または<i>3</i>。 例えば、[!UICONTROL Description 1 Position]の値が1の場合、[!UICONTROL Description 1]は位置1にのみ表示されます。 デフォルトでは、説明は位置に固定されません。</p><p>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。</p><p><b> メモ：</b>複数の説明を同じ位置に固定できます。 広告ネットワークは、位置にピン留めされた説明の1つを使用します。 位置2にピン留めされた説明は、広告で表示されない場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれるURL。<br><br>拡張された動的検索広告の場合、[!DNL Google Ads]はこの値をweb サイト ドメインから動的に生成します。値を入力する必要はありません。<br><br> レスポンシブ検索広告の場合、値を入力する必要はありません。 表示URLは、最終的なURLのドメインから自動的に抽出されます。 オプションで、「パス 1」フィールドと「パス 2」フィールドを使用してURLをカスタマイズできます。<br><br>作成または編集することはできませんが、2022年6月に非推奨となった[!DNL Google Ads]の拡張テキスト広告を削除することはできます。<br><br><b> メモ：</b> （最終URLを持つアカウント）表示URLと最終URLのドメイン名は一致する必要があります。</p> |
| [!UICONTROL Display Path 1] | <p>（拡張テキスト広告<span>およびレスポンシブ検索広告</span>のみ）</p><p>（オプション）最終的なURLから自動的に抽出される表示URLに追加されるテキスト。 URLの先頭には、スラッシュ（/）が付きます。 パスにスラッシュ （/）または改行（\n）を含めることはできません。 最大長は15文字または7文字のダブルバイト文字です。</p><p>広告カスタマイザーを挿入するには、次の形式を使用します。フィード ファイルに有効な値&lt; `Default text`が含まれていない場合は、`{CUSTOMIZER.AdCustomizerName:Default text}`はオプションで挿入できます（`{CUSTOMIZER.Discount:10%}`など）。</p><p>例えば、[!UICONTROL Display Path 1]が「deals」の場合、表示URLは&lt;<i>display URL</i>>/deals （www.example.com/dealsなど）です。</p><p>作成または編集することはできませんが、2022年6月に非推奨となった[!DNL Google Ads]の拡張テキスト広告を削除することはできます。</p> |
| [!UICONTROL Display Path 2] | 2番目の表示パスです。[!UICONTROL Display Path 1]のエントリを参照してください。<br><br>例：[!UICONTROL Display Path 1]が「deals」で、[!UICONTROL Display Path 2]が「local」の場合、表示URLは&lt;<i>display URL</i>>/deals/local （www.example.com/deals/localなど）です。</p><p>作成または編集することはできませんが、2022年6月に非推奨となった[!DNL Google Ads]の拡張テキスト広告を削除することはできます。</p> |
| [!UICONTROL Promotion Line] | （商品リスト広告のみ）検索結果に商品リストに含めるオプションのプロモーションライン。 最大長は45文字です。</p><p>プロモーションラインは、広告がページ上のどこに表示されるかに応じて、広告とは異なる場所（広告の下など）に表示されます。 |
| [!UICONTROL Link Name] | <p>サイトリンクのテキスト： 最大25文字まで含めることができます。</p><p>新しいサイトリンクの場合は、サイトリンクの行内にキャンペーン名を含める必要があります。 広告グループレベルのサイトリンクの場合は、広告グループ名も含める必要があります。</p><p><b>注：</b> 35文字の既存のテキストは、デスクトップやタブレットでは広告に表示されますが、モバイルデバイスでは表示されません。</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | （既存のアプリインストール広告のみ）モバイルアプリケーションが実行されるオペレーティングシステム：<i>Android™</i>または<i>ios</i>。 |
| [!UICONTROL Mobile App ID (Google Adwords)] | （既存のアプリインストール広告のみ） <p>アプリケーション IDまたはパッケージ名。 |
| [!UICONTROL Mobile App Name (Google Adwords)] | （既存のアプリインストール広告のみ） アプリケーションの名前。 |
| [!UICONTROL Start Date] | <p>（拡張サイトリンクのみ）広告主のタイムゾーンおよび次のいずれかの形式で、サイトリンクに入札を配置できる最初の日付：<i>m/d/yyyy</i>、<i>m/d/yy</i>、<i>m-d-yyyy</i>、または<i>m-d-yy</i>。 新しい拡張サイトリンクのデフォルトは現在の日付です。</p><p><b>注意：</b>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーン内でのみ作成できます。または、サイトリンクは作成できません。</p> |
| [!UICONTROL End Date] | <p>（拡張サイトリンクのみ）広告主のタイムゾーンおよび次のいずれかの形式で、サイトリンクに入札を配置できる最後の日付。  <i>m/d/yyyy</i>、<i>m/d/yy</i>、<i>m-d-yyyy</i>または<i>m-d-yy</i>。 デフォルトはnone （終了日なし）です。</p><p><b>注意：</b>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーン内でのみ作成できます。または、サイトリンクは作成できません。</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | （既存のアプリインストール広告のみ）</p><p>（オプション） [!DNL Google Ads]がタブレット ユーザーに広告を表示しないようにします。 値には、<i>yes</i>と<i>no</i>を含めることができます。 |
| [!UICONTROL Landing Page Suffix] | 最後のURLの末尾に追加するパラメーターを指定して、情報を追跡します。 例：`param2=value1&param3=value2`<br><br> 「[のクリックトラッキング形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md)を参照してください。」<br><br>下位レベルの最終URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、[!DNL Google Ads] エディターを使用します。 |
| [!UICONTROL Tracking Template] | トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLを[!DNL ValueTrack] パラメーターに埋め込みます。 最も詳細なレベル（キーワードが最も詳細）のトラッキングテンプレートは、より高いレベルのすべての値を上書きします。<br><br> キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceに独自のリダイレクトコードとトラッキングコードが自動的に追加されます。<br><br> サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 トラッキングテンプレートの最終的なURLを示す[!DNL ValueTrack] パラメーターのリストについては、[!DNL ValueTrack] ドキュメント [[!DNL Google Ads] の「使用可能な](https://support.google.com/google-ads/answer/2375447) パラメーター」の節の「トラッキングテンプレートのみ」パラメーターを参照してください。<br><br>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Base URL/Final URL] | 検索エンジンユーザーが広告をクリックしたときに取得されるランディングページのURL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 キーワードレベルのベース/最終URLは、広告レベル以上のURLを上書きします。<br><br>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Destination URL] | （情報目的で生成されたバルクシートに含まれ、検索エンジンには投稿されません）宛先URLを持つアカウントの場合、これは、広告を広告主のweb サイト上のベース URL/ランディングページにリンクするURLです（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを介して送信する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URLを生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 検索エンジン固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br>最終URLを持つアカウントの場合、この列には基本URL/最終URL列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | 検索アカウントまたはキャンペーン設定のトラッキングパラメーターに変数が含まれている場合に、`{custom_code}`動的変数の代わりにデータを使用します。 トラッキング URLにカスタム値を挿入するには、「トラッキング URLを生成」オプションを使用してバルクシート ファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式：<i>[!UICONTROL Text ad]</i>、<i>[!UICONTROL Expanded text ad]</i>、<i>[!UICONTROL Demand Gen Carousel Ad]</i> （複数の画像カルーセル広告）、<i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>、<i>[!UICONTROL Demand Gen Product Ad]</i>、および<i>[!UICONTROL Demand Gen Video Ad]</i>、<i>[!UICONTROL Dynamic search ad]</i> （非推奨）広告タイプ、<i>[!UICONTROL Expanded Dynamic Search ad]</i>、&lt;[!UICONTROL i>Display ad]</i>、<i>[!UICONTROL App Install ad]</i> （非推奨）、<i>[!UICONTROL Image]</i>、<i>[!UICONTROL Product ad<]/i> （ショッピング広告）、または<i>[!UICONTROL Responsive search ad]</i>。 新規広告のデフォルトは<i>[!UICONTROL Text ad]</i>です。<br><br>製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Param1] | <p>`{param1}`広告パラメーターの数値。広告コピーに含めることも、バルクシート ファイル内の任意の広告のURLを表示することもできます。 最大長は25文字です。次の非数値を含めることができます。</p><ul><li><p>値の前に通貨記号またはコードを追加できます。 例えば、`£2.000,00`と`2000GBP`は有効です。</p></li><li><p>値には、区切り記号としてコンマ （`,`）またはピリオド （`.`）を含めることができ、オプションのピリオド （`.`）または分数の値にはコンマ （`,`）を含めることができます。 例えば、`1,000.00`と`2.000,10`は有効です。</p></li><li><p>値の先頭または末尾にパーセント記号（`%`）、プラス記号（`+`）、マイナス記号（`- `）を追加できます。 例えば、`20%`、`208+`、`-42.32`は有効です。</p></li><li><p>2つの数字をスラッシュで埋め込むことができます。 例えば、`4/1`と`0.95/0.45`は有効です。</p></li></ul><p>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。</p> |
| [!UICONTROL Param2] | `{param2}`広告パラメーターの数値。広告コピーに含めることも、バルクシート ファイル内の任意の広告のURLを表示することもできます。 詳しくは、Param1のエントリを参照してください。 |
| [!UICONTROL Audience] | 検索広告用リマーケティングリスト（RLSA）は、キャンペーンまたは広告グループのターゲットオーディエンスまたは除外オーディエンスをターゲットにします。 「ターゲットタイプ」フィールドで、ターゲットか除外かを指定します。 |
| [!UICONTROL Target Type] | （オーディエンスが指定されている場合）指定されたオーディエンスが<i>包含</i> （ターゲット）または<i>除外</i>であるかどうか。 |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Ended]</i> （編集不可）、または<i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新規キャンペーンのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブまたは一時停止したキャンペーンを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新規広告グループのデフォルトは[!UICONTROL Active]です。 アクティブな広告グループまたは一時停止した広告グループを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは[!UICONTROL Active]です。 アクティブ キーワードまたは一時停止キーワードを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Ad Status] | 広告の表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告のみ）、<i>[!UICONTROL Disapproved]</i> （編集不可）、または<i>[!UICONTROL Paused]</i>。 新規広告のデフォルトは[!UICONTROL Active]です。 アクティブな広告または一時停止した広告を削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Placement Status] | Web サイトのプレースメントのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存の広告のみ）。 新しいWeb サイトのデフォルトは<i> アクティブです。</i> アクティブまたは一時停止したプレースメントを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新規ターゲットのデフォルトは<i> アクティブです。</i> アクティブなターゲットまたは一時停止したターゲットを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス：<i>[!UICONTROL Active]</i> <span>または</span> <i>[!UICONTROL Deleted]</i> （既存の製品グループのみ）。 新しい製品グループのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブな製品グループを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス：<i> アクティブまたは削除済み</i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブなサイトリンクを削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Location Status] | 場所ターゲットの状態：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトは[!UICONTROL Active]です。 アクティブな場所を削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL RLSA Target Status] | キャンペーンまたは広告グループレベルのRLSA ターゲットまたは除外のステータス：<i>[!UICONTROL Active]</i>または[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは<i>[!UICONTROL Active]</i>です。 アクティブなターゲットまたは除外を削除するには、値<i>[!UICONTROL Deleted]</i>を入力します。 |
| [!UICONTROL Device Target Status] | <p>キャンペーン レベルまたは広告グループ レベルのデバイス ターゲットの状態：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i>。 新しいキャンペーンと広告グループの場合、デフォルトは<i>[!UICONTROL Active]</i>です。</p> |
| \[広告主固有ラベル分類\] | （広告主固有のラベル分類の名前。例えば、「カラー」というラベル分類の「カラー」など）エンティティに関連付けられている指定された分類の値。 エンティティごとに分類ごとに1つの値のみを含めることができます（キャンペーン Aの「カラー」ラベル分類の「赤」など）。 最大長は100文字で、値にはASCII文字と非ASCII文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も詳細）レベルに適用されます。<br><br>分類名も分類値も大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられた制約。 エンティティごとに割り当てることができる制約は1つだけです。<br><b>>制約は子エンティティによって継承されるので、継承された値を上書きしない限り、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1] キャンペーン名を変更する場合にのみ必要です。行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り除きます。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]広告グループの「[!UICONTROL AMO ID]」が行に含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にa）キーワードを識別するのに十分なプロパティ列またはb）「[!UICONTROL AMO ID]」が含まれていない限り、キーワードを変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには、広告IDまたはAMO IDが必要です。 その他のすべてのエンティティ タイプでは、行に広告を識別するのに十分な広告プロパティ列（a）またはb）「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ、広告IDが必要です。」 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。</p><p><b>注意：</b>既存の広告のステータスを除くa）広告プロパティ列またはb）レスポンシブ検索広告のデータを編集し、[!UICONTROL Ad ID]または[!UICONTROL AMO ID]のいずれも含まない場合、新しい広告が作成され、既存の広告は変更されません。</p> |
| [!UICONTROL Placement ID] | Web サイトの配置を識別する一意のID。 プレースメントを変更または削除する場合にのみ必要です。ただし、行にa）プレースメントを識別するのに十分なプロパティ列またはb）「[!UICONTROL AMO ID]」が含まれていない限り必要です。 |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意のID。 自動ターゲットを変更または削除する場合にのみ必須です。ただし、行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL Product Group ID] | 既存の製品グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]製品グループを変更または削除する場合にのみ必要です。行にa）製品グループを識別するのに十分なプロパティ列またはb）「[!UICONTROL AMO ID]」が含まれていない限り除きます。 |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にa）サイトリンクを識別するのに十分なプロパティ列またはb）「[!UICONTROL AMO ID]」が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。 ただし、[!UICONTROL Sitelink ID]と[!UICONTROL AMO ID]のどちらも含めず、プロパティ列が複数のサイトリンクに一致する場合、サイトリンクの1つのみのステータスが変更されます。</p><p><b>注意：</b>既存のサイトリンクのステータス以外のサイトリンクプロパティ列を編集し、[!UICONTROL Sitelink ID]と[!UICONTROL AMO ID]のどちらも含まない場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルのRLSA ターゲットまたは除外を識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1]行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットまたは除外を変更または削除する場合にのみ必要です。 |
| [!UICONTROL Device Target ID] | <p>既存のキャンペーンレベルまたは広告グループレベルのデバイスターゲットまたは除外を識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に一重引用符（&#39;）を付ける必要があります。[^1] ターゲットを変更または削除する場合にのみ必要です。行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。</p> |
| [!UICONTROL AMO ID] | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意のID。 レスポンシブ検索広告の場合、広告IDを含めない限り、AMO IDは広告の編集または削除に必要です。 AMO IDを持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ IDと親エンティティ IDを含めない限り、AMO IDがデータの編集または削除に必要です。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |
| [!UICONTROL EF Error Message] | （情報目的で生成されたバルクシートに含まれる）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報目的で生成されたバルクシートに含まれる）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報目的で生成されたバルクシートに含まれる）広告が違反する[!DNL Google Ads]広告ポリシーの名前とテキストを表示するためのプレースホルダー。 |
| [!UICONTROL Retail Hash] | （高度なキャンペーン管理を使用して生成されたバルクシートに情報目的で含まれます）高度な（ACM）ビューを使用して生成されたことを示す英数字のハッシュコード（f9639f40cdf56524b541e5dacf55a991など）。 |

[^1]: [!DNL Excel]は、ファイルを開いたときに、大きな数値を科学表記法（2115585666の場合は2.12E+09など）に変換します。 標準表記法で数値を表示するには、列内の任意のセルを選択し、数式バー内をクリックします。

## 各アカウントコンポーネントの作成、編集、削除に必要なフィールド {#bulksheet-fields-per-component-google}

以下のセクションには、特定のアカウントエンティティに関連するフィールドが含まれます。

>[!NOTE]
>
>フィールドがアクションに適用されない場合、フィールドに入力された値は無視されます。

### キャンペーンフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Campaign Budget] | キャンペーンの作成に必要です。 |
| [!UICONTROL Delivery Method] | キャンペーンの作成に必要です。 |
| [!UICONTROL Channel Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Networks] | キャンペーンの作成に必要です。 |
| [!UICONTROL DSA Domain Name] | 検索ネットワーク上に動的検索広告を含むキャンペーンを作成する必要があります。 |
| [!UICONTROL DSA Domain Language] | 検索ネットワーク上に動的検索広告を含むキャンペーンを作成する必要があります。 |
| [!UICONTROL Campaign Priority] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Has EU Political Ads] | キャンペーンの作成に必要です。 |
| [!UICONTROL Merchant ID] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Sales Country] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Product Scope Filter] | （ショッピングキャンペーン）オプション |
| [!UICONTROL Languages] | オプション |
| [!UICONTROL Device Targets] | オプション |
| [!UICONTROL Device Targets (Google Adwords)] | オプション |
| [!UICONTROL Mobile Carriers (Google Adwords)] | オプション |
| [!UICONTROL Audience Target Method] | なし |
| [!UICONTROL Landing Page Suffix] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Campaign Status] | キャンペーンを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | キャンペーン名を変更する場合にのみ必須です。行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 広告グループフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Networks] | なし |
| [!UICONTROL GDN Custom Bid Level] | オプション |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Group Type] | 広告グループの作成に必要です。 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Max Content CPC] | オプション |
| [!UICONTROL Audience Target Method] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Group Status] | 広告グループを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Ad Group ID] | 広告グループ名を変更する場合にのみ必要です。行に広告グループの「[!UICONTROL AMO ID]」が含まれていない限り除きます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### キーワードフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Keyword] | 必須 |
| [!UICONTROL Match Type] | 複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード IDの値が必要です。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Param1] | オプション |
| [!UICONTROL Param2] | オプション |
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必須です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | キーワードを編集または削除する場合にのみ必要です。ただし、行にa）キーワードを識別するのに十分なプロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれている場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 配置フィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max Placement CPC (Google Adwords)] | オプション |
| [!UICONTROL Max Placement CPM (Google Adwords)] | オプション |
| [!UICONTROL Placement] | 必須 |
| [!UICONTROL Match Type] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Placement Status] | プレースメントを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Placement ID] | プレースメントを編集または削除する場合にのみ必要です。ただし、行にa）プレースメントを識別するのに十分なプロパティ列またはb） 「[!UICONTROL AMO ID]」が含まれていない限りではありません。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### dynamic search広告を拡張

この広告タイプは、[!DNL Google Ads]で「動的検索広告」と呼ばれるようになりました。 動的検索広告の作成について詳しくは、「[動的検索広告の実装 [!DNL Google Ads] 2&rbrace;」を参照してください。](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html?lang=ja)

この広告タイプでは、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 広告の作成または説明の編集に必要です。 <b> メモ：</b>この広告タイプでは、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告のステータスを変更する場合にのみ必要です。行にa）広告を識別するのに十分な広告プロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 製品リスト/ショッピング広告フィールド

ショッピング広告の作成について詳しくは、「[実装 [!DNL Google Ads]  ショッピングキャンペーン &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html)」を参照してください。

この広告タイプでは、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Promotion Line] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告のステータスを変更する場合にのみ必要です。行にa）広告を識別するのに十分な広告プロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### レスポンシブ検索広告のフィールド

この広告タイプでは、[!UICONTROL Responsive Search Ad] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]-15 | レスポンシブ検索広告の場合、広告を作成するには[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]および[!UICONTROL Ad Title 3]が必要であり、その他のすべての広告タイトルフィールドはオプションです。 必須ではないフィールドの既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、広告を作成するには[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]が必要であり、[!UICONTROL Description Line 3]と[!UICONTROL Description Line 4]はオプションです。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告の作成が必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない限り、広告を編集または削除する必要があります。 |
| [!UICONTROL AMO ID] | 広告IDを含まない限り、広告の編集または削除が必要です。 |

### テキスト広告フィールド

この広告タイプでは、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

>[!NOTE]
>
>拡張テキスト広告は、2022年6月に非推奨（廃止予定）となりました。 既存のテキスト広告のみを削除できます。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | 読み取り専用 |
| [!UICONTROL Ad Title]、広告タイトル 2-3 | 読み取り専用 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 読み取り専用 |
| [!UICONTROL Display URL] | 読み取り専用 |
| [!UICONTROL Display Path 1] | 読み取り専用 |
| [!UICONTROL Display Path 2] | 読み取り専用 |
| [!UICONTROL Tracking Template] | 読み取り専用 |
| [!UICONTROL Base URL/Final URL] | 読み取り専用 |
| [!UICONTROL Custom URL Param] | 読み取り専用 |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Ad Status] | 必須 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告ステータスを変更する場合にのみ必要です。行にa&amp;rpar；広告またはb&amp;rparを識別するのに十分な広告プロパティ列が含まれていない限り、「[!UICONTROL AMO ID]」が必要です。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 動的な検索ターゲット（自動ターゲット）フィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Auto Target Expression] | 「[!UICONTROL Use my website contents to target my ads]」へのキャンペーン設定が有効になっていない場合にのみ必要です。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Target Status] | ターゲットを削除する必要があります |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 自動ターゲットを変更または削除する場合にのみ必須です。ただし、行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 買い物商品のグループフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | 製品グループの作成に必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループの作成に必要です。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Product Group Status] | 製品グループを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 製品グループを変更または削除する場合にのみ必要です。ただし、行にa）製品グループを識別するのに十分なプロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのサイトリンクフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのサイトリンクに必要。 キャンペーンレベルのサイトリンクには適用されません。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Link Name] | 必須 |
| [!UICONTROL Start Date] | オプション |
| [!UICONTROL End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Sitelink Status] | サイトリンクの削除のみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Sitelink ID] | サイトリンクを変更または削除する場合にのみ必須です。ただし、行にa） サイトリンクを識別するのに十分なプロパティ列またはb） 「[!UICONTROL AMO ID]」が含まれている場合を除きます。 ただし、[!UICONTROL Sitelink ID]も[!UICONTROL AMO ID]も含めず、プロパティ列が複数のサイトリンクに一致する場合、サイトリンクの1つのみのステータスが変更されます。<br><br><b>注意：</b>既存のサイトリンク用に[!UICONTROL Status]を除くサイトリンクプロパティ列を編集し、[!UICONTROL Sitelink ID]と[!UICONTROL AMO ID]のどちらも含まない場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### 位置情報

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | 場所ターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | [!UICONTROL Campaign ID]が含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスターゲットフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットの作成または編集に必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必要です。 キャンペーンレベルのデバイスターゲットには適用できません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのデバイスターゲットにのみ適用されます。 |
| [!UICONTROL Device Target ID] | ターゲットを変更または削除する場合にのみ必須です。行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り必須です。 |
| [!UICONTROL AMO ID] | Device Target IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのRLSA ターゲット/除外フィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットと除外に必要です。 キャンペーンレベルのターゲットと除外には適用できません。 |
| [!UICONTROL Audience] | 新しいターゲットまたは除外を作成するために必要です。 |
| [!UICONTROL Target Type] | 新しいターゲットまたは除外を作成するために必要です。 |
| [!UICONTROL RLSA Target Status] | ターゲットまたは除外を削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのターゲットと除外にのみ適用されます。 |
| [!UICONTROL RLSA Target ID] | ターゲットを変更または削除する場合にのみ必須です。行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り必須です。 |
| [!UICONTROL AMO ID] | RLSA ターゲット IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceは、値を使用して正しいIDを判断しますが、そのIDを広告ネットワークに投稿しません。 |

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [&#x200B; バルクシートで実行できる操作](bulksheet-operations.md)
>* [&#x200B; サポートされているバルクシート ファイル形式](bulksheet-file-formats.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
>* [の [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md) クリックトラッキング形式
>* [&#x200B; バルクシート ファイルをアップロードするか、エラーファイルを修正](../bulksheet-upload.md)
