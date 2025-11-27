---
title: アカウントに必須のバルクシート デ  [!DNL Google Ads]  タ
description: アカウントのバルクシートで、必須のヘッダーフィールドとデータフィ  [!DNL Google Ads]  ルドを参照します。
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '7859'
ht-degree: 0%

---

# 付録 – [!DNL Google Ads] アカウントに必須のバルクシートデータ

キャンペーンデータ [!DNL Google Ads] 一括で作成および更新するには、[!DNL Google Ads] アカウント用に特別にフォーマットされた検索、ソーシャル、Commerceのバルクシートファイルを使用できます。 a） [&#x200B; 既存のアカウント用のバルクシートファイルを必要なファイル形式で生成する &#x200B;](../bulksheet-download.md) または b）手動で作成できます（サポートされるファイル形式について詳しくは、「[&#x200B; サポートされるバルクシートファイル形式 &#x200B;](bulksheet-file-formats.md)」を参照してください）。

各バルクシートには、ヘッダーフィールドと、[&#x200B; 実行する特定の操作 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) に必要な対応するデータフィールド（広告の作成など）を含める必要があります。 フィールドが不要な場合は、ヘッダー行とデータ行から省略できます。 バルクシートファイルをアップロードすると、すべてのカスタム列が削除されます。

次の表は、使用可能なすべてのデータフィールドと、個々のエンティティ（キャンペーンやキーワードなど）のデータを追加、編集または削除するために必要なフィールドを示す追加のテーブルです。

## すべての使用可能なデータフィールド {#bulksheet-fields-all-google}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、[&#x200B; 各アカウントコンポーネントの作成、編集、削除に必要なフィールド &#x200B;](#bulksheet-fields-per-component-google) を参照してください。

>[!NOTE]
>
>* すべてのテキスト列の値は、大文字と小文字が区別されます。
>* 新しいレコードを作成するときに、すべての必須データフィールドに値を指定しなかった場合、それらのフィールドの一部に、指定したデフォルト値が割り当てられます。
>* 以下で指定されていないフィールドの場合、広告ネットワークのデフォルト値が使用されます。
>* [!UICONTROL Download Bulksheet] ダイアログで使用可能なバルクシート行のリストについては、「[&#x200B; 広告ネットワークによるバルクシート行 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network)」を参照してください。

| フィールド | 説明 |
| ---- | ---- |
| [!UICONTROL Platform] | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンの 1 日あたりの支出制限（金銭記号および句読点の有無は問わない）。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | <p>キャンペーンの広告を毎日表示する速度：</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日に配分します。</p></li><li><p><i>[!UICONTROL Accelerated]:</i> （2019 年 10 月に非推奨）予算に達するまでできるだけ頻繁に広告を表示します。 その結果、広告がその日の後半に表示されない場合があります。</p></li></ul> |
| [!UICONTROL Channel Type] | <p>広告を配置するチャネル。 1 つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Search]</i> （新しいキャンペーンのデフォルト）：広告を [!DNL Google Ads] 検索ネットワーク（[!DNL Google Ads] 検索および検索パートナーの web サイトを含む）およびオプションで [!DNL Google Ads] ディスプレイネットワークに配置します。 <b> 注意：</b> 検索ネットワークとディスプレイネットワークの両方をターゲットとするキャンペーンは、入札最適化のためにポートフォリオに追加することはできません。</p></li><li><p><i>[!UICONTROL Display]</i>：広告を [!DNL Google Ads] ディスプレイネットワークにのみ配置する場合。</p></li><li><p><i>[!UICONTROL Shopping]</i>: ショッピング広告を [!DNL Google Ads] のショッピング・ネットワーク（一部の国）および [!DNL Google Ads] の検索ネットワーク（[!DNL Google Ads] の検索および検索パートナー Web サイトを含む）に配置します。 買い物広告を作成するには、[!DNL Google Merchant Center] アカウントに商品があり、[&#x200B; 検索、ソーシャル、Commerceがアカウントからデータをダウンロードできるようにする &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md) 必要があります。 ショッピング広告を作成するプロセスについて詳しくは [&#x200B; 「 [!DNL Google Ads]  ショッピングキャンペーンの実装 &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)」を参照してください。</p></li></ul> |
| [!UICONTROL Networks] | <p>広告の配置場所。 1 つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Google Search]</i>:Google Search Network 専用のスポンサー付き検索リスト。</p></li><li><p><i>[!UICONTROL Search Partners]</i>:Googleの検索パートナーのスポンサー付き検索リスト。</p></li><li><p><i>[!UICONTROL Content]</i>: ネットワーク一覧を表示する入札を配置します。</p></li><li><p><i>[!UICONTROL All]</i> （新しいキャンペーンのデフォルト）:Google検索、検索パートナーおよびコンテンツをターゲットにします。</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>（検索ネットワークのみ。拡張された動的検索広告にのみ適用されます）。広告ネットワークが動的検索広告のターゲットとして使用するコンテンツの Web サイトのルートドメイン（example.comなど）またはサブドメイン（shoes.example.comなど）。<br><br><b> 注：</b></p><ul><li><p>動的検索広告をキーワードではなく web サイトコンテンツをターゲットに拡張しました。</p></li><li><p>ターゲットにするドメインは、広告ネットワークのオーガニック検索インデックスでインデックス化する必要があります。</p></li><li><p>ドメインを指定しない場合は、動的な検索ターゲットを作成する必要があります。このターゲットは、広告グループごとに、すべての web サイトページまたはサブセットをターゲットにします。</p></li></ul> |
| [!UICONTROL DSA Domain Language] | （検索ネットワークのみ。展開された動的検索広告にのみ適用）指定した web サイトドメインの言語。 <b> メモ：</b> ドメインに複数の言語のページが含まれ、すべてのページをターゲットにする場合は、言語ごとに個別のキャンペーンを作成します。 |
| [!UICONTROL GDN Custom Bid Level] | （ディスプレイネットワークをターゲットにするキャンペーンのみ）入札方法：<i>[!UICONTROL Ad Group]</i> （デフォルト）、<i>[!UICONTROL Keyword]</i>、<i>[!UICONTROL Placement]</i> （web サイト）、<i>[!UICONTROL None]</i> （既存の値をリセットする場合）。 その他のディメンション（<i> 年齢 </i>、<i> 性別 </i>、<i> 興味とリスト </i>、<i> トピック </i>、<i> 垂直方向 </i>）は、[!DNL Google Ads] インターフェイスから使用できます。 [!DNL Google Ads] インターフェイスを使用して別のディメンションによる入札を設定した場合、その値は表示されますが、ここではそのディメンションを選択または入力できません。</p><p><b> メモ：</b></p><ul><li><p>キーワードで入札する場合、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメント別に入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他のすべてのディメンションでは、広告レベルでトラッキングテンプレートを作成します。</p></li><li><p>サポートされていないディメンション（年齢、性別、興味とリスト、トピック）で入札を行った場合、検索、ソーシャルおよびCommerceでは、そのディメンションの入札が最適化されず、すべてのアトリビューションが広告グループに適用されます。</p></li><li><p>検索ネットワーク上の広告は、常にキーワード入札を使用します。</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>（ショッピングキャンペーンのみ）複数のキャンペーンが同じ製品を広告する場合に使用されるキャンペーンの優先度。<i>[!UICONTROL Low]</i> （新しいキャンペーンのデフォルト）、<i>[!UICONTROL Medium]</i> または <i>[!UICONTROL High]</i> です。</p><p>同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークは最初にキャンペーンの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Merchant ID] | （マーチャントフィードにリンクされたショッピングキャンペーンおよびオーディエンスキャンペーンのみ）商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。 |
| [!UICONTROL Sales Country] | （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）キャンペーンの商品が販売される国。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （[!DNL Google Ads] ショッピングネットワークを使用したキャンペーンのみ）キャンペーン用にショッピング広告を作成できる、[!DNL Google Merchant Center] アカウント内の製品。 dimension=attribute のフォーマットを使用して、製品をフィルタする製品次元と属性の組合せを最大 7 つ入力できます。 複数のフィルターを「>>」区切り文字で区切ります。 使用可能な製品ディメンションのリストについては、「[&#x200B; ショッピングキャンペーン製品フィルター &#x200B;](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。</p><p>例：「CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies」</p><p>既存の値を削除するには、値 <code>[delete] を使用します</code> （角括弧を含む）。</p> |
| [!UICONTROL Languages] | <p>（ネットワークの検索と表示のみ） キャンペーンの広告のターゲット言語。</p><p>新しいキャンペーンでこのフィールドにも [!UICONTROL Geo Targeting] フィールドにも値を入力しない場合、特定の言語（EUR など）にマッピングされていない通貨を使用したキャンペーンはすべての言語をターゲットにすることを除いて、アカウントに指定された通貨がデフォルトの言語を決定します。 このフィールドに値を入力せずに、新しいキャンペーンの「[!UICONTROL Geo Targeting]」フィールドに値を入力した場合は、デフォルトで <i>[!UICONTROL All]</i> になります。 既存のキャンペーンに対してこのフィールドを空白のままにした場合、既存の値が保持されます。</p><p>すべての言語を対象にするには、<span style="font-style: italic;">&lt;i[!UICONTROL >All]</i></span> と入力します。 特定の言語を指定するには、<a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] の言語名 </a> 正しい数値コードに置き換えられる <i> 英語；日本語 </i> など）または数値コード （<i>1000;1005</i> など）を使用して、セミコロンで区切られた値を入力します。 値では、大文字と小文字が区別されません。</p> |
| [!UICONTROL Location] | キャンペーンの広告を配置する、または広告を除外する地理的な場所。 このフィールドまたは新しいキャンペーンの「言語」フィールドのいずれにも値を入力しない場合、特定の場所（例：EUR）にマッピングされていない通貨を使用したキャンペーンはすべての場所をターゲットにすることを除いて、アカウントに指定された通貨がデフォルトの場所を決定します。 このフィールドに値を入力せずに、新しいキャンペーンの「[!UICONTROL Languages]」フィールドに値を入力した場合、デフォルトは <i>[!UICONTROL All]</i> になります。 既存のキャンペーンに対してこのフィールドを空白のままにした場合、既存の値が保持されます。</p><p>特定の場所をターゲットにするには、次のいずれかの [[!DNL Google Ads]  場所名 &#x200B;](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （正しい数値コードに置き換えられています）または場所コードを使用します：</p><ul><li><p>国/地域：国/地域名（<i> 米国；日本 </i> など）または数値コード（<i>2840;2392</i> など）を入力します。</p></li><li><p>都道府県/地域：都道府県/地域名を、関連する国/地域の略称（<i> 東京、JP；ニューヨーク、US</i> など）または数値コード（<i>20636;21167</i> など）で入力します。</p></li><li><p>米国以外の都市：都市名、都道府県/地域名、国/地域の略称（<i> 足立、東京、JP；北、東京、JP</i> など）または数値コード（<i>1028850;1009293</i> など）を入力します</p></li><li><p>米国の都市圏：都市名、州名、国の略称（<i> バッファロー NY、US；ニューヨーク NY、US</i> など）または数値コード（<i>514;501</i> など）を入力します。</p></li></ul><p>場所を除外するには、場所の名前またはコードの前にマイナス記号（`-`）（<i>-Japan</i> など）を付けます。</p><p><b> メモ：</b> 値では大文字と小文字が区別されません。</p> |
| [!UICONTROL Location Type] | （場所を含める場合） [&#x200B; 場所タイプ &#x200B;](https://developers.google.com/google-ads/api/data/geotargets)。 |
| [!UICONTROL Device] | キャンペーンレベルまたは広告グループレベルで入札調整が行われるデバイスタイプ：<i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>、<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | <p>（[!UICONTROL Location]、[!UICONTROL Device] または [!UICONTROL RLSA] ターゲットを含める場合）特定の場所、特定のデバイスタイプ、特定のオーディエンスターゲットのいずれかで広告の入札を調整するかどうかを指定します。</p><ul><li><p>キーワードレベルの入札（0% 差）を使用するには、0 を入力します。 新しいターゲットの場合は、空白のままにすることもできます。</p></li><li><p>このターゲットに対して別の入札を使用するには、入札の増減率を入力します。</p></li><ul><li><p>ロケーションおよび RLSA ターゲットの場合、有効な割合は–90 から 900 です。</p></li><li><p>デバイスの入札調整の場合、有効な割合は次のとおりです。</p></li><ul><li><p>（キャンペーン）–100 （デバイスタイプの広告に入札しない場合）または–90～900。</p></li><li><p>（広告グループ）–100 （スマートフォンとタブレットの場合）（デバイスタイプに入札しない場合）、およびすべてのデバイスタイプに対して–90～900。</p></li></ul></ul><li><p>（既存のキャンペーンおよび広告グループ）既存の入札調整を使用するには、これを空白のままにします。</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | （情報提供のために生成されたバルクシートに含まれる） キャンペーンレベルの場所のターゲットまたは RLSA に対してAdobeが推奨する読み取り専用の入札調整。 これは、キャンペーンが（[!UICONTROL Maximize Clicks] の目標ではなく）加重コンバージョン指標を使用する目標を持つポートフォリオにあり、キャンペーンに少なくとも 2 つの場所ターゲットまたは過去 90 日間に少なくとも 5 クリックまたは 5 米ドルのコストの RLSA が含まれている場合にのみ計算されます。</p><p>推奨値を使用するようにロケーション ターゲットまたは RLSA を手動で編集する場合は、ロケーション ターゲットまたは RLSA を作成してから少なくとも 2 週間待ち、十分なデータ収集が行われるようにし、値を週に 1 回以上変更しないでください。 |
| [!UICONTROL Device Targets] | <p>（従来のキャンペーンタイプのみ）広告を表示できるデバイス：<i>[!UICONTROL All]</i>、<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Smartphones]</i>、<i>[!UICONTROL Tablets]</i>。 新規キャンペーンの場合、デフォルトは <i>[!UICONTROL All]</i> です。</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | （従来のキャンペーンタイプのみ。デバイスターゲットに「スマートフォン」または「タブレット」が含まれる場合に適用されます）広告が表示されるオペレーティングシステムには、<i>[!UICONTROL All]</i>、<i>[!UICONTROL Android]</i>、<i>[!UICONTROL iOS]</i> または <i>[!UICONTROL Palm]</i> があります。 新規キャンペーンの場合、デフォルトは <i>[!UICONTROL All]</i> です。</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>（従来のキャンペーンタイプのみ。「[!UICONTROL Device Targets]」または「[!UICONTROL All]」が [!UICONTROL Smartphones] に含まれる場合に適用されます） スマートフォンが接続される可能性のある携帯電話会社：<i>[!UICONTROL All]</i>、または &lt;c<i>carrier code</i>>、&lt;<i>country code</i>> で示される 1 つ以上の携帯電話会社（T-Mobile、US など） <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank"> 利用可能な携帯電話会社および [!DNL Google Ads]</a> 用コードのリストを使用しています。 複数のキャリアをセミコロンで区切ります（T-Mobile、US;T-Mobile、GB など）。 新規キャンペーンの場合、デフォルトは <i>[!UICONTROL All]</i> です。</p> |
| [!UICONTROL Ad Group Name] | <p>広告グループを識別する一意の名前。 最大長は 255 文字です。末尾の空白文字は保存されません（例えば、「広告グループ 1」は「広告グループ 1」として保存されます）。 このフィールドは、キャンペーンレベルのサイトリンクまたはキャンペーンレベルのデバイスターゲットには適用されません。</p> |
| [!UICONTROL Ad Group Type] | <p>広告グループタイプ：<i>[!UICONTROL Demand Gen]</i> （需要生成キャンペーンのみ）、<i>[!UICONTROL Display]</i> （ディスプレイキャンペーンの場合）、<i>[!UICONTROL Search Dynamic]</i> （展開された動的検索広告の場合）、<i>[!UICONTROL Search Standard]</i> （検索広告の場合）、<i>[!UICONTROL Shopping Product]</i> （ショッピング製品広告の場合）、<i>[!UICONTROL Shopping Showcase]</i> （作成および編集はサポートされていません）、<i>[!UICONTROL Unknown]</i>。</p> |
| [!UICONTROL Max CPC] | <p>（CPC キャンペーンのみ）最大クリック単価（CPC）。これは、金銭的記号や句読点の有無にかかわらず、広告ネットワーク上の広告クリックに対して支払う最高額です。 広告グループとキーワード、製品グループおよび動的検索ターゲットの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 製品グループの場合、製品グループの最下位層の値を設定できます。新規層のデフォルトは、親層から継承されます。</p><p>最適化されたポートフォリオ内の既存の製品グループと動的検索ターゲットの場合、更新は 1 日のみ有効であり、次の最適化サイクルで上書きされます。</p> |
| [!UICONTROL Max Content CPC] | <p>（CPC キャンペーンのみ） 1 クリックあたりの最大コンテンツコスト（CPC）。これは、金銭的な記号や句読点の有無にかかわらず、ディスプレイネットワークサイトから広告クリックに対して支払う最高額です。 プレースメントに基づいていないキャンペーンの広告グループレベルで、値を設定および編集できます。</p> |
| [!UICONTROL Audience Target Method] | <p>（検索ネットワーク上のみのキャンペーンおよび表示ネットワーク上の既存の読み取り専用 [!DNL Gmail] キャンペーン）次のようにします。</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>：ターゲットオーディエンスに関連付けられているユーザーで、その広告グループの他のターゲットも満たしているユーザーにのみ広告を表示します。</p></li><li><p><i>[!UICONTROL Bid Only]</i>：他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていない人物にも広告を表示します。</p><p>ただし、特定のオーディエンスに対してより高い入札を設定すると、それらのオーディエンスに広告が表示される可能性が高くなります。</p></li></ul> |
| [!UICONTROL Keyword] | キーワード文字列。 最大長は 80 文字、10 語以内で、文字、数字、次の特殊文字のみを含めることができます。スペース `# $ & _ - " [ ] ' + . / :`</p><p><b> メモ：</b></p><ul><li><p>広告グループレベルまたはキャンペーンレベルでキーワードを除外するには、[!UICONTROL Match Type] を <i>[!UICONTROL Negative]</i> に設定します。 行に広告グループ名が含まれている場合、キーワードはその広告グループから除外されます。 行に広告グループ名が含まれていない場合、キーワードはキャンペーン全体で除外されます。</p></li><li><p>[!DNL Google Ads] キーワードまたは一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。</p></li></ul> |
| [!UICONTROL Placement] | （コンテンツ一致を使用するキャンペーンのみ）広告を表示できるディスプレイネットワーク内のプレースメント。 次のいずれかを指定します。</p><ul><li><p>Web サイト：有効な URL を入力します。 最上位ドメイン、最上位サブドメイン、または単一のディレクトリ名を持つドメインを指定できます。 URL に疑問符（?）を含めることはできません。 例：<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>特定のページの広告の位置：形式 `<URL> >> <location,sublocation>` （`finance.google.com >> Company pages,Top right` など）を使用します。</p></li><li><p>トピックカテゴリ：構文 `<category::<category> > <subcategory>` などを使用します（`category::Industries > Energy & Utilities > Oil & Gas` など）。</p></li></ul><p><b> メモ：</b> 広告グループレベルまたはキャンペーンレベルでプレースメントを除外するには、[!UICONTROL Match Type] を <i>[!UICONTROL Negative]</i> に設定します。 行に広告グループ名が含まれている場合、広告グループのプレースメントは除外されます。 行に広告グループ名が含まれていない場合、キャンペーン全体でそのプレースメントは除外されます。</p> |
| [!UICONTROL Auto Target Expression] | <p>（キャンペーン設定を「[!UICONTROL Use my website contents to target my ads]」にしない場合は必須です。それ以外の場合はオプション）広告グループの動的検索ターゲット。</p><p>すべてのターゲットにアスタリスク（*）を使用します。</p><p>最大 3 つの動的検索条件をターゲットにするには、形式 `<category>=<target>` を使用します。`<category>` の場合、以下のいずれかのカテゴリを含めることができます。 個々のカテゴリの複数のターゲットを「\[ 空白スペース\] および\[ 空白スペース\]」で結合し、複数のカテゴリを「[ 空白スペース ] および [ 空白スペース ]」で結合します。</p><ul><li><p><i>[!UICONTROL Category]</i>：特定の [!DNL Google Ads] コンテンツカテゴリを持つインデックス付きページの拡張された動的検索広告を表示します。</p></li><li><p><i>[!UICONTROL URL]</i>：特定の URL を持つインデックス付きページに対して拡張された動的検索広告を表示します。この値は、URL 内の任意の場所に含めることができます。</p></li><li><p><i>[!UICONTROL Page Title]</i>: ページタイトルに特定のテキストを含むインデックス付きページの拡張された動的検索広告を表示する。</p></li><li><p><i>[!UICONTROL Page Content]</i>：特定のコンテンツを含むインデックス付きページの拡張された動的検索広告を表示します。</p></li></ul><p>例：url=shoes.example.com and page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | 親商品グループの階層。<br><br> 例：`All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>製品グループ（「brand=acme」や「すべての製品」など）。</p><p><b> メモ：</b></p><ul><li><p>指定した商品グループが [!UICONTROL Parent Product Groupings] 階層に存在しない場合、検索、ソーシャル、Commerceは、必要な階層の部分を作成します。</p></li><li><p>デフォルトの入札額を広告グループのデフォルトの入札額に設定して、[!UICONTROL All Products] Shopping キャンペーンで広告グループを作成すると、検索、ソーシャル、Commerceに「[!DNL Google Ads]」グループが自動的に作成されます。 検索、ソーシャル、Commerceでは、商品グループ階層の各レベルに、広告グループのデフォルト入札を使用して、自動的に「[!UICONTROL Everything Else]」グループが作成されます。 これらのデフォルトグループを明示的に作成して、除外するか、入札を変更することができます。</p></li><li><p>各広告グループには、「[!UICONTROL All Products]」と 7 つのその他の層を含む、最大 8 つの製品グループ層を含めることができます。</p></li></ul> |
| [!UICONTROL Partition Type] | 製品グループの区分タイプ：<i> 下位区分 </i> （子製品グループがある場合）または <i> 単位 </i> （子製品グループがない場合）。 |
| [!UICONTROL Match Type] | <p>動的検索ターゲットまたは製品グループ：動的検索ターゲットまたは製品グループのキーワード照合オプション：<i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索ターゲットのデフォルト）、<i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）、または <i>[!UICONTROL Negative Product Group]</i> （製品グループを除外する場合）。</p><p>キーワードの場合：キーワードのキーワードマッチングオプションである <i>[!UICONTROL Broad]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Exact]</i> または <i>[!UICONTROL Negative]</i> （キーワードまたは表示ネットワーク上のプレースメントを除外するため）。ショッピング広告で使用される製品グループの場合、一致タイプは <i>[!UICONTROL Product Group]</i> です。 <i>[!UICONTROL Negative]</i> を使用する場合は、除外する一致タイプも含める必要があります（「負のフレーズ」など）。</p><p>新しいキーワードの場合、デフォルトは <i>[!UICONTROL Broad]</i> です。 一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。</p><p><b> メモ：</b></p><ul><li><p>一致タイプは、キーワードを使用しない展開された動的検索広告には適用されません。</p></li><li><p>[!DNL Google Ads] キーワードの一致タイプを変更すると、既存のキーワードが削除され、新しいキーワードが作成されます。</p></li><li><p>「部分一致」修飾子の場合は、「部分一致」を選択し、近いバリアントが必要なキーワード内の単語の前に+を挿入します（「赤」と「靴」の両方の近いバリアントが必要な場合は「+赤+靴」など）。 <b> メモ：</b> 部分一致修飾子は、一部の言語でフレーズ一致と同じ一致動作を持つようになり、2021 年 7 月以降、新しい部分一致修飾子キーワードを作成できません。 詳しくは、[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/7042511) を参照してください。</p> |
| [!UICONTROL First Page Bid] | （情報提供のために生成されたバルクシートに含まれる）検索結果の最初のページに広告を配置するために必要な入札。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Quality Score] | （情報提供のために生成されたバルクシートに含まれる）検索エンジンがキーワードに割り当てた現在の品質スコア。 この値は広告ネットワークには投稿されません）。 |
| [!UICONTROL Creative Preferred Devices] | （テキスト広告、拡張された動的検索広告、拡張サイトリンク。オプション）広告を表示するデバイスタイプは、<i>[!UICONTROL All]</i> （デフォルト）または <i>[!UICONTROL Mobile]</i> です。 <i>[!UICONTROL Mobile]</i> を指定すると、ネットワークはデスクトップまたはタブレットユーザーではなく、モバイルデバイスユーザーに広告を表示しようとします。 それ以外の場合、ネットワークは任意のデバイスタイプで広告を表示します。</p><p><b> メモ：</b></p><ul><li><p>この設定を編集できるのは、管理者と [!DNL Adobe] アカウント管理者のユーザーのみです。</p></li><li><p>ネットワークでは、優先デバイスタイプで広告が表示されるとは保証されません。</p></li><li><p>新しい拡張サイトリンクは、既存の拡張サイトリンクがある、またはサイトリンクがないキャンペーンでのみ作成できます。</p></li></ul> |
| [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]-15 | （拡張されたテキスト広告とレスポンシブ検索広告のみ）広告のヘッドライン。各広告は縦棒（&vert;）で区切られます。 各広告タイトルフィールドの最大長は、30 文字または 15 個の 2 バイト文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。</p><p>レスポンシブ検索広告の場合、[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3] は必須で、その他の広告タイトルフィールドはすべてオプションです。 必須以外のフィールドの既存の値を削除するには、値 <code>[delete] を使用します</code> （角括弧を含む）。</p><p>レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイズ機能を挿入します。<code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code><code>{CUSTOMIZER.Discount:10%} など）</code></p><p>作成や編集はできませんが、2022 年 6 月に廃止された、拡張されたテキスト広告を削除 [!DNL Google Ads] きます。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>（レスポンシブ検索広告のみ。オプション）対応する広告タイトルをピン留めする位置：`[null]` （値なし。これは、広告タイトルをすべての位置に対して適格にします）、<i>1</i>、<i>2</i>、<i>3</i>。 例えば、値が 1 の [!UICONTROL Ad Title Position] 合、広告タイトルは位置 1 にのみ表示されます。 デフォルトでは、すべての広告タイトルが null です（値がありません）。</p><p>既存の値を削除するには、値 <code>[delete] を使用します</code> （角括弧を含む）。</p><p><b> メモ：</b> 複数の広告タイトルを同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた広告タイトルの 1 つを使用する。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>（拡張された動的検索広告、拡張されたテキスト広告およびレスポンシブ検索広告のみ）広告の本文。 各説明フィールドの最大長は、90 文字または 45 文字の 2 バイト文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。</p><p>レスポンシブ検索広告については、次の形式を使用して広告カスタマイズ機能を挿入します。`{CUSTOMIZER.AdCustomizerName:DefaultText}` （`{CUSTOMIZER.Discount:10%}` など）</p><p>拡張された動的検索広告には、[!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] のみを使用します。 <b> メモ：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</p><p>作成や編集はできませんが、2022 年 6 月に廃止された、拡張されたテキスト広告を削除 [!DNL Google Ads] きます。</p><p>レスポンシブ検索広告の場合、[!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] は必須で、[!UICONTROL Description Line 3] と [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、値 <code>[delete] を使用します</code> （角括弧を含む）。</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ。オプション）対応する説明をピン留めする位置：`[null]` （値なし。これにより、説明がすべての位置に対して適格になります）、<i>1</i>、<i>2</i>、<i>3</i>。 たとえば、[!UICONTROL Description 1 Position] の値が 1 の場合、[!UICONTROL Description 1] は位置 1 にのみ表示されます。 デフォルトでは、説明は位置にピン留めされません。</p><p>既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。</p><p><b> 注：</b> 複数の説明を同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた説明の 1 つを使用します。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれる URL。<br><br> 展開された動的検索広告の場合、[!DNL Google Ads] は、この値を web サイトドメインから動的に生成するので、値を入力する必要はありません。<br><br> レスポンシブ検索広告の場合は、値を入力する必要はありません。 最終的な URL のドメインから、表示 URL が自動的に抽出されます。 オプションで、「パス 1」および「パス 2」フィールドを使用して URL をカスタマイズできます。<br><br> 作成または編集することはできませんが、2022 年 6 月に非推奨（廃止予定）になった、拡張されたテキスト広告を削除 [!DNL Google Ads] きます。<br><br><b> 注意：</b> （最終的な URL を持つアカウント）表示 URL と最終的な URL のドメイン名は一致する必要があります。</p> |
| [!UICONTROL Display Path 1] | <p>（拡張されたテキスト広告 <span> レスポンシブ検索広告 </span> のみ）</p><p>（任意）最終的な URL から自動的に抽出された、表示 URL に追加されるテキスト。 URL 内では、先頭にスラッシュ（/）が付きます。 パスにスラッシュ （/）や改行（\n）を含めることはできません。 最大長は 15 文字または 7 つの 2 バイト文字です。</p><p>広告カスタマイズ機能を挿入するには、次の形式を使用します（`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です）。`{CUSTOMIZER.AdCustomizerName:Default text}` など &lt; `{CUSTOMIZER.Discount:10%}`</p><p>例えば、[!UICONTROL Display Path 1] が「deals」の場合、表示 URL は &lt;<i>display URL</i>>/deals （www.example.com/dealsなど）です。</p><p>作成や編集はできませんが、2022 年 6 月に廃止された、拡張されたテキスト広告を削除 [!DNL Google Ads] きます。</p> |
| [!UICONTROL Display Path 2] | 2 つ目の表示パス。[!UICONTROL Display Path 1] しくは、エントリを参照してください。<br><br> 例：[!UICONTROL Display Path 1] が「deals」で、[!UICONTROL Display Path 2] が「local」の場合、表示 URL は &lt;<i>display URL</i>>/deals/local （www.example.com/deals/localなど）になります。</p><p>作成や編集はできませんが、2022 年 6 月に廃止された、拡張されたテキスト広告を削除 [!DNL Google Ads] きます。</p> |
| [!UICONTROL Promotion Line] | （商品リスト広告のみ）検索結果の商品リストに含めるオプションのプロモーションライン。 最大長は 45 文字です。</p><p>プロモーションラインは、広告がページ上のどこに表示されるかに応じて、広告に対して異なる場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Link Name] | <p>サイトリンクテキスト。 最大 25 文字を使用できます。</p><p>新しいサイトリンクの場合は、サイトリンク行にキャンペーン名を含める必要があります。 広告グループレベルのサイトリンクの場合は、広告グループ名も含める必要があります。</p><p><b> 注意：</b> 既存の 35 文字のテキストは、デスクトップやタブレットの広告には引き続き表示されますが、モバイルデバイスには表示されません。</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | （既存のアプリのインストール広告のみ） モバイルアプリケーションが実行されるオペレーティングシステム：<i>Android™</i> または <i>ios</i>。 |
| [!UICONTROL Mobile App ID (Google Adwords)] | （既存のアプリインストール広告のみ） <p>アプリケーション ID またはパッケージ名。 |
| [!UICONTROL Mobile App Name (Google Adwords)] | （既存のアプリのインストール広告のみ）アプリケーションの名前。 |
| [!UICONTROL Start Date] | <p>（強化されたサイトリンクのみ）サイトリンクの入札に使用できる最初の日付。広告主のタイムゾーンおよび次のいずれかの形式です。<i>m/d/yyyy</i>、<i>m/d/yy</i>、<i>m-d-yyyy</i> または <i>m-d-yy</i>。 新しい拡張サイトリンクのデフォルトは現在の日付です。</p><p><b> 注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクがあるキャンペーンにのみ作成するか、サイトリンクを作成しないキャンペーンに作成できます。</p> |
| [!UICONTROL End Date] | <p>（サイトのリンクの強化機能のみ）広告主のタイムゾーンおよび次のいずれかの形式で、サイトのリンクに入札を配置できる最後の日付。  <i>m/d/yyyy</i>、<i>m/d/yy</i>、<i>m-d-yyyy</i> または <i>m-d-yy</i> デフォルトは「なし」（終了日なし）です。</p><p><b> 注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクがあるキャンペーンにのみ作成するか、サイトリンクを作成しないキャンペーンに作成できます。</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | （既存のアプリインストール広告のみ）</p><p>（任意） [!DNL Google Ads] タブレットユーザーに広告を表示できないようにします。 値には、<i> はい </i> と <i> いいえ </i> を含めることができます。 |
| [!UICONTROL Landing Page Suffix] | 情報を追跡するために最終的な URL の末尾に追加するパラメーター。 例：`param2=value1&param3=value2`<br><br> 「[&#x200B; のクリック追跡形式  [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) を参照。<br><br> 下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下にサフィックスを設定するには、[!DNL Google Ads] エディターを使用します。 |
| [!UICONTROL Tracking Template] | トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL を [!DNL ValueTrack] パラメーターに埋め込みます。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、それより上のすべてのレベルの値を上書きします。<br><br> キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキングの場合、レコードを保存すると、検索、ソーシャルおよびCommerceによって独自のリダイレクトおよびトラッキングコードが自動的に追加されます。<br><br> サードパーティのリダイレクトおよびトラッキングの場合は、値を入力します。 トラッキングテンプレートで最終的な URL を示す [!DNL ValueTrack] パラメーターのリストについては、「ドキュメント」の「使用できる [!DNL ValueTrack] パラメーター」に関する節の「トラッキングテンプレートのみ [[!DNL Google Ads]  パラメーターを参照してください &#x200B;](https://support.google.com/google-ads/answer/2375447)。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Base URL/Final URL] | 広告をクリックした際に検索エンジンユーザーが取得されるランディングページの URL （キャンペーンまたはアカウントに設定されている追加パラメーターを含む）。 キーワードレベルのベース URL/最終 URL が、広告レベル以降の URL を上書きします。<br><br> 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Destination URL] | （情報目的で生成されたバルクシートに含まれ、検索エンジンに投稿されない）宛先 URL を持つアカウントの場合、これは、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 検索エンジン固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br> 最終 URL を持つアカウントの場合、この列には「ベース URL/最終 URL」列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | 検索アカウントまたはキャンペーン設定のトラッキングパラメーターに変数が含まれる場合、`{custom_code}` の動的変数に置き換わるデータです。 トラッキング URL にカスタム値を挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式：<i>[!UICONTROL Text ad]</i>、<i>[!UICONTROL Expanded text ad]</i>、<i>[!UICONTROL Demand Gen Carousel Ad]</i> （マルチ画像カルーセル広告）、<i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>、<i>[!UICONTROL Demand Gen Product Ad]</i>、<i>[!UICONTROL Demand Gen Video Ad]</i>、<i>[!UICONTROL Dynamic search ad]</i> （非推奨の広告タイプ）、<i>[!UICONTROL Expanded Dynamic Search ad]</i>、&lt;[!UICONTROL i>Display ad]</i>、<i>[!UICONTROL App Install ad]</i> （非推奨）、<i>[!UICONTROL Image]</i>、<i>[!UICONTROL Product ad<]/i> （ショッピング広告）、<i>[!UICONTROL Responsive search ad]</i>。 新規広告のデフォルトは <i>[!UICONTROL Text ad]</i> です。<br><br> 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Param1] | <p>`{param1}` 広告パラメーターの数値。バルクシートファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます。 最大長は 25 文字で、次のヌン数字を含めることができます。</p><ul><li><p>値の先頭または末尾に通貨記号またはコードを付けることができます。 例えば、`£2.000,00` と `2000GBP` は有効です。</p></li><li><p>値には、区切り文字としてコンマ（`,`）またはピリオド（`.`）を使用でき、オプションとしてピリオド（`.`）または分数値のコンマ（`,`）を使用できます。 例えば、`1,000.00` と `2.000,10` は有効です。</p></li><li><p>値の前には、パーセント記号（`%`）、プラス記号（`+`）、マイナス記号（`- `）を付けることができます。 例えば、`20%`、`208+` および `-42.32` は有効です。</p></li><li><p>2 つの数値をスラッシュで埋め込むことができます。 例えば、`4/1` と `0.95/0.45` は有効です。</p></li></ul><p>既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。</p> |
| [!UICONTROL Param2] | `{param2}` 広告パラメーターの数値。バルクシートファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます。 詳しくは、Param1 のエントリを参照してください。 |
| [!UICONTROL Audience] | 検索広告（RLSA）のリマーケティングリストは、キャンペーンまたは広告グループのターゲットオーディエンスまたは除外オーディエンスをターゲットにします。 「ターゲットタイプ」フィールドで、ターゲットか除外かを指定します。 |
| [!UICONTROL Target Type] | （オーディエンスが指定された場合）指定されたオーディエンスが <i> 含める </i> （ターゲット）か <i> 除外 </i> か。 |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Ended]</i> （編集不可）または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブまたは一時停止されたキャンペーンを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止されている広告グループを削除するには、値 `Deleted` を入力します。 |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止したキーワードを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Ad Status] | 広告の表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告のみ）、<i>[!UICONTROL Disapproved]</i> （編集不可）、<i>[!UICONTROL Paused]</i>。 新規広告のデフォルトは [!UICONTROL Active] です。 アクティブまたは一時停止された広告を削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Placement Status] | Web サイトプレースメントのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告のみ）。 新しい Web サイトのデフォルトは <i> アクティブです。</i> アクティブまたは一時停止したプレースメントを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i> または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットのデフォルトは <i> アクティブです。</i> アクティブまたは一時停止されたターゲットを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス：<i>[!UICONTROL Active]</i> <span> または </span> <i>[!UICONTROL Deleted]</i> （既存の製品グループのみ）。 新製品グループのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブな製品グループを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス：<i> アクティブまたは削除済み </i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブなサイトリンクを削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Location Status] | 場所ターゲットのステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトは [!UICONTROL Active] です。 アクティブな位置を削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL RLSA Target Status] | キャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外のステータス：<i>[!UICONTROL Active]</i> または [!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは <i>[!UICONTROL Active]</i> です。 アクティブなターゲットまたは除外を削除するには、値 <i>[!UICONTROL Deleted]</i> を入力します。 |
| [!UICONTROL Device Target Status] | <p>キャンペーンレベルまたは広告グループレベルデバイスターゲットのステータス：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i>。 新規キャンペーンおよび広告グループの場合、デフォルトは <i>[!UICONTROL Active]</i> です。</p> |
| \[ 広告主固有のラベル分類\] | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 製品グループのラベル分類は、単位（最も詳細な単位）レベルで適用されます。<br><br> 分類名も分類値も、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><b>> 制約は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に広告グループの「[!UICONTROL AMO ID]」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） キーワードを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、キーワードを変更する場合にのみ必要です。 |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには広告 ID または AMO ID が必要です。 その他のすべてのエンティティタイプでは、広告 ID が必要になるのは広告ステータスを変更した場合のみです。ただし、行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。</p><p><b> メモ：</b> 編集する場合、a）既存の広告のステータスを除く広告プロパティ列、または b）レスポンシブ検索広告のデータが含まれ、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も指定されていない場合、新しい広告が作成され、既存の広告は変更されません。</p> |
| [!UICONTROL Placement ID] | Web サイトプレースメントを識別する一意の ID。 行に（a）プレースメントを識別するのに十分なプロパティ列が含まれている場合、または（b）「[!UICONTROL AMO ID]」が含まれている場合を除き、プレースメントを変更または削除する場合にのみ必要です。 |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意の ID。 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL Product Group ID] | 既存の商品グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 製品グループを変更または削除する場合にのみ必要です。ただし、行に a）製品グループを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] サイトリンクを変更または削除した場合にのみ必要です。ただし、行に a） サイトリンクを識別するのに十分なプロパティ列、または b） 「[!UICONTROL AMO ID]」が含まれる場合を除きます。 ただし、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含まれず、プロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。</p><p><b> 注意：</b> 既存のサイトリンクの [ 状態 ] 以外のサイトリンク プロパティの列を編集し、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含めない場合は、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットまたは除外を変更または削除する場合にのみ必要です。 |
| [!UICONTROL Device Target ID] | <p>既存のキャンペーンレベルまたは広告グループレベルのデバイスのターゲットまたは除外を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です。</p> |
| [!UICONTROL AMO ID] | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意の ID。 レスポンシブ検索広告の場合、広告 ID を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |
| [!UICONTROL EF Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは [!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報提供のために生成されたバルクシートに含まれる）広告が違反した [!DNL Google Ads] の広告ポリシーの名前とテキストを表示するプレースホルダー。 |
| [!UICONTROL Retail Hash] | （詳細キャンペーン管理を使用して生成されたバルクシートに含まれる、情報提供の目的で）項目が詳細（ACM）ビューを使用して生成されたことを示す英数字のハッシュコード（f9639f40cdf56524b541e5dacf55a991 など）。 |

[^1]:[!DNL Excel] は、ファイルを開いたときに、大きな数値を指数表記（2115585666 の場合は 2.12E+09 など）に変換します。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

## 各アカウントコンポーネントを作成、編集または削除するために必要なフィールド {#bulksheet-fields-per-component-google}

以下の節には、特定のアカウントエンティティに関連するフィールドが含まれます。

>[!NOTE]
>
>フィールドがアクションに適用できない場合、フィールドに入力された値は無視されます。

### キャンペーンフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Campaign Budget] | キャンペーンの作成に必要です。 |
| [!UICONTROL Delivery Method] | キャンペーンの作成に必要です。 |
| [!UICONTROL Channel Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Networks] | キャンペーンの作成に必要です。 |
| [!UICONTROL DSA Domain Name] | 検索ネットワーク上に動的検索広告を含むキャンペーンを作成する際に必要です。 |
| [!UICONTROL DSA Domain Language] | 検索ネットワーク上に動的検索広告を含むキャンペーンを作成する際に必要です。 |
| [!UICONTROL Campaign Priority] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Merchant ID] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Sales Country] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Product Scope Filter] | （ショッピングキャンペーン）任意 |
| [!UICONTROL Languages] | オプション |
| [!UICONTROL Device Targets] | オプション |
| [!UICONTROL Device Targets (Google Adwords)] | オプション |
| [!UICONTROL Mobile Carriers (Google Adwords)] | オプション |
| [!UICONTROL Audience Target Method] | 該当なし |
| [!UICONTROL Landing Page Suffix] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Campaign Status] | キャンペーンを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | キャンペーン名を変更した場合にのみ必要です。ただし、行にキャンペーンの「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 広告グループフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Networks] | 該当なし |
| [!UICONTROL GDN Custom Bid Level] | オプション |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Group Type] | 広告グループを作成するために必要です。 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Max Content CPC] | オプション |
| [!UICONTROL Audience Target Method] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Group Status] | 広告グループを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Ad Group ID] | 広告グループ名を変更した場合にのみ必要です。ただし、行に広告グループの「[!UICONTROL AMO ID]」が含まれている場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キーワードフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Keyword] | 必須 |
| [!UICONTROL Match Type] | 複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード ID の値が必要です。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Param1] | オプション |
| [!UICONTROL Param2] | オプション |
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必須です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | 行に a） キーワードを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、キーワードを編集または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### プレースメントフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
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
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Placement ID] | 行に（a）プレースメントを識別するのに十分なプロパティ列が含まれている場合、または（b）「[!UICONTROL AMO ID]」が含まれている場合を除き、プレースメントを編集または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 動的検索広告を拡張しました

この広告タイプは、[!DNL Google Ads] では「動的検索広告」と呼ばれるようになりました。 動的検索広告の作成について詳しくは、「[&#x200B; 動的検索広告の実装  [!DNL Google Ads]  を参照してください &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-dynamic-search-ads.html)。

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 広告の作成または説明の編集に必要。 <b> メモ：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 商品リスト / ショッピング広告フィールド

ショッピング広告の作成の詳細は、「[&#x200B; ショッピング・キャンペーン  [!DNL Google Ads]  実装 &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/google-shopping-campaigns.html)」を参照してください。

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Promotion Line] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列、または（b）「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### レスポンシブ検索広告フィールド

この広告タイプの場合は、[!UICONTROL Responsive Search Ad] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]-15 | レスポンシブ検索広告の場合、広告を作成するには [!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3] が必要で、その他の広告タイトルフィールドはオプションです。 必須以外のフィールドに既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、広告を作成するには [!UICONTROL Description Line 1] と [!UICONTROL Description Line 2] が必要で、[!UICONTROL Description Line 3] と [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、値 `[delete]` （角括弧を含む）を使用します。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告の作成に必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない場合、広告を編集または削除する必要があります。 |
| [!UICONTROL AMO ID] | 広告 ID を含めない場合、広告を編集または削除する必要があります。 |

### テキストとフィールド

この広告タイプの場合は、[!UICONTROL Creative (except RSA)] ダイアログの「[!UICONTROL Download Bulksheet]」行を使用します。

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

>[!NOTE]
>
>拡張テキスト広告は、2022 年 6 月に非推奨（廃止予定）となりました。 既存のテキスト広告のみを削除できます。

| フィールド | 必須？ |
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
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告ステータスを変更した場合にのみ必要です。ただし、行に a&amp;rpar；広告を識別するのに十分な広告プロパティ列または b&rpar;「[!UICONTROL AMO ID]」が含まれている場合は除きます。 ただし、[!UICONTROL Ad ID] も [!UICONTROL AMO ID] も含まれず、広告プロパティ列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 動的検索のターゲット（自動ターゲット）フィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Auto Target Expression] | キャンペーン設定が「[!UICONTROL Use my website contents to target my ads]」に対して有効になっていない場合にのみ必要です。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Target Status] | ターゲットの削除が必要です |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### ショッピング製品グループ フィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | 製品グループを作成するために必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Product Group Status] | 製品グループを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 製品グループを変更または削除した場合にのみ必要です。ただし、行に a）製品グループを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれる場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのサイトリンクフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのサイトリンクに必要です。 キャンペーンレベルのサイトリンクには適用されません。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Link Name] | 必須 |
| [!UICONTROL Start Date] | オプション |
| [!UICONTROL End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Sitelink Status] | サイトリンクを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Sitelink ID] | 行に a） サイトリンクを識別するのに十分なプロパティ列、または b）「[!UICONTROL AMO ID]」が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。 ただし、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含まれず、プロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。<br><br><b> 注意：</b> 既存のサイトリンクの [!UICONTROL Status] を除くサイトリンクプロパティの列を編集し、[!UICONTROL Sitelink ID] も [!UICONTROL AMO ID] も含めない場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### 場所のターゲット

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | 場所のターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | [!UICONTROL Campaign ID] を含めない限り、データを編集または削除するために必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスのターゲットフィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを作成または編集するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必要。 キャンペーンレベルのデバイスターゲットには適用されません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのデバイスターゲットにのみ適用できます。 |
| [!UICONTROL Device Target ID] | 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | デバイスターゲット ID を含めない限り、データの編集または削除に必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

### キャンペーンレベルおよび広告グループレベルの RLSA ターゲット/除外フィールド

各データ・フィールドの説明は、「[&#x200B; 使用可能なすべてのデータ・フィールド &#x200B;](#bulksheet-fields-all-google)」を参照してください。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットおよび除外に必要。 キャンペーンレベルのターゲットおよび除外には適用されません。 |
| [!UICONTROL Audience] | 新しいターゲットまたは除外の作成に必要です。 |
| [!UICONTROL Target Type] | 新しいターゲットまたは除外の作成に必要です。 |
| [!UICONTROL RLSA Target Status] | ターゲットまたは除外を削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのターゲットと除外にのみ適用できます。 |
| [!UICONTROL RLSA Target ID] | 行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | RLSA ターゲット ID を含めない限り、データを編集または削除するために必要です。<br><br> 検索、ソーシャル、Commerceでは、値を使用して編集する正しい ID が判断されますが、ID は広告ネットワークに投稿されません。 |

>[!MORELIKETHIS]
>
>* [&#x200B; 付録 – バルクシート エラー &#x200B;](../bulksheet-errors.md)
>* [&#x200B; バルクシートで実行できる操作 &#x200B;](bulksheet-operations.md)
>* [&#x200B; サポートされるバルクシート ファイル形式 &#x200B;](bulksheet-file-formats.md)
>* [&#x200B; バルクシートファイルのダウンロード/作成 &#x200B;](../bulksheet-download.md)
>* [&#x200B; のクリック追跡形式  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [&#x200B; バルクシートファイルまたは修正されたエラーファイルのアップロード &#x200B;](../bulksheet-upload.md)
