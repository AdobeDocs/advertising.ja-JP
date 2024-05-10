---
title: に必要なバルクシート データ [!DNL Google Ads] アカウント
description: のバルクシートの必須のヘッダーフィールドおよびデータフィールドを参照します。 [!DNL Google Ads] アカウント。
exl-id: 756b77fe-f95d-469f-9ae0-7424c2fad0b1
feature: Search Bulksheets
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '7855'
ht-degree: 0%

---

# 付録 – に必要なバルクシートデータ [!DNL Google Ads] アカウント

を作成および更新するには [!DNL Google Ads] campaign データを一括で使用すると、用に特別にフォーマットされた検索、ソーシャル、Commerceのバルクシートファイルを使用できます [!DNL Google Ads] アカウント。 次のいずれかを実行できます [既存のアカウントの一括シートファイルを生成](../bulksheet-download.md) 必要なファイル形式または b）で手動作成（「」を参照）。[サポートされるバルクシート ファイル形式](bulksheet-file-formats.md)サポートされるファイル形式の一般情報については、「」を参照してください。

各バルクシートには、ヘッダーフィールドと、に必要な対応するデータフィールドを含める必要があります [実行する特定の操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （広告の作成など）。 フィールドが不要な場合は、ヘッダー行とデータ行から省略できます。 バルクシートファイルをアップロードすると、すべてのカスタム列が削除されます。

次の表は、使用可能なすべてのデータフィールドと、個々のエンティティ（キャンペーンやキーワードなど）のデータを追加、編集または削除するために必要なフィールドを示す追加のテーブルです。

## すべての使用可能なデータフィールド {#bulksheet-fields-all-google}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、を参照してください[各アカウントコンポーネントを作成、編集または削除するために必要なフィールド](#bulksheet-fields-per-component-google).」と入力します。

>[!NOTE]
>
>* すべてのテキスト列の値は、大文字と小文字が区別されます。
>* 新しいレコードを作成するときに、すべての必須データフィールドに値を指定しなかった場合、それらのフィールドの一部に、指定したデフォルト値が割り当てられます。
>* 以下で指定されていないフィールドの場合、広告ネットワークのデフォルト値が使用されます。
>* で使用可能なバルクシート行のリストについては、 [!UICONTROL Download Bulksheet] ダイアログ、「」を参照[広告ネットワーク別バルクシート行](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).」と入力します。

| フィールド | 説明 |
| ---- | ---- |
| [!UICONTROL Platform] | （情報提供のために生成されたバルクシートに含まれる）広告プラットフォーム。 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンの 1 日あたりの支出制限（金銭記号および句読点の有無は問わない）。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | <p>キャンペーンの広告を毎日表示する速度：</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを 1 日に配分します。</p></li><li><p><i>[!UICONTROL Accelerated]:</i> （2019 年 10 月に非推奨）予算に達するまでできるだけ頻繁に広告を表示します。 その結果、広告がその日の後半に表示されない場合があります。</p></li></ul> |
| [!UICONTROL Channel Type] | <p>広告を配置するチャネル。 1 つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Search]</i> （新規キャンペーンのデフォルト）：に広告を配置します [!DNL Google Ads] ネットワークを検索（含む） [!DNL Google Ads] パートナー web サイトを検索および検索）、およびオプションで [!DNL Google Ads] ネットワークを表示します。 <b>注意：</b> 検索ネットワークとディスプレイネットワークの両方をターゲットとするキャンペーンは、入札最適化のためにポートフォリオに追加することはできません。</p></li><li><p><i>[!UICONTROL Display]</i>：広告をにのみ配置する [!DNL Google Ads] ネットワークを表示します。</p></li><li><p><i>[!UICONTROL Shopping]</i>：ショッピング広告を配置する [!DNL Google Ads] ショッピングネットワーク（一部の国のみ）と [!DNL Google Ads] ネットワークを検索（含む） [!DNL Google Ads] パートナー web サイトを検索および検索します）。 ショッピング広告を作成するには、に商品が必要です。 [!DNL Google Merchant Center] アカウントと [アカウントから検索、ソーシャル、Commerceにデータをダウンロードできるようにする](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 参照先」[実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)「ショッピング広告の作成プロセスの詳細については、を参照してください。</p></li></ul> |
| [!UICONTROL Networks] | <p>広告の配置場所。 1 つ以上のオプションを指定します。</p><ul><li><p><i>[!UICONTROL Google Search]</i>:Google Search Network 専用のスポンサー付き検索リスト。</p></li><li><p><i>[!UICONTROL Search Partners]</i>:Googleの検索パートナーのスポンサー付き検索リスト。</p></li><li><p><i>[!UICONTROL Content]</i>：ネットワーク一覧を表示する入札を配置します。</p></li><li><p><i>[!UICONTROL All]</i> （新しいキャンペーンのデフォルト）:Google検索、検索パートナーおよびコンテンツをターゲットにします。</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>（検索ネットワークのみ。拡張された動的検索広告にのみ適用されます）。広告ネットワークが動的検索広告のターゲットとして使用するコンテンツの Web サイトのルートドメイン（example.comなど）またはサブドメイン（shoes.example.comなど）。<br><br><b>メモ：</b></p><ul><li><p>動的検索広告をキーワードではなく web サイトコンテンツをターゲットに拡張しました。</p></li><li><p>ターゲットにするドメインは、広告ネットワークのオーガニック検索インデックスでインデックス化する必要があります。</p></li><li><p>ドメインを指定しない場合は、動的な検索ターゲットを作成する必要があります。このターゲットは、広告グループごとに、すべての web サイトページまたはサブセットをターゲットにします。</p></li></ul> |
| [!UICONTROL DSA Domain Language] | （検索ネットワークのみ。展開された動的検索広告にのみ適用）指定した web サイトドメインの言語。 <b>注意：</b> ドメインに複数の言語のページが含まれ、すべてのページをターゲットにする場合は、言語ごとに個別のキャンペーンを作成します。 |
| [!UICONTROL GDN Custom Bid Level] | （ディスプレイネットワークをターゲットにするキャンペーンのみ）入札方法：by <i>[!UICONTROL Ad Group]</i> （デフォルト）、 <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i> （web サイト）、 <i>[!UICONTROL None]</i> （既存の値をリセットする）。 その他のディメンション （<i>年齢</i>, <i>性別</i>, <i>興味とリスト</i>, <i>トピック</i>、および <i>垂直方向</i>）は、から使用できます [!DNL Google Ads] インターフェイス。 を使用したことがある場合 [!DNL Google Ads] 別のディメンションによる入札を設定するためのインターフェイス。この値は表示されますが、これらのディメンションをここで選択または入力することはできません。</p><p><b>注意：</b></p><ul><li><p>キーワードで入札する場合、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメント別に入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他のすべてのディメンションでは、広告レベルでトラッキングテンプレートを作成します。</p></li><li><p>サポートされていないディメンション（年齢、性別、興味とリスト、トピック）で入札を行った場合、検索、ソーシャルおよびCommerceでは、そのディメンションの入札が最適化されず、すべてのアトリビューションが広告グループに適用されます。</p></li><li><p>検索ネットワーク上の広告は、常にキーワード入札を使用します。</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>（ショッピングキャンペーンのみ）複数のキャンペーンで同じ製品が広告される場合に使用されるキャンペーンの優先度。  <i>[!UICONTROL Low]</i> （新規キャンペーンのデフォルト）、 <i>[!UICONTROL Medium]</i>、または <i>[!UICONTROL High]</i>.</p><p>同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークは最初にキャンペーンの優先度を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Merchant ID] | （マーチャントフィードにリンクされたショッピングキャンペーンおよびオーディエンスキャンペーンのみ）商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。 |  |
| [!UICONTROL Sales Country] | （ショッピングキャンペーンのみ。既存のキャンペーンの場合は読み取り専用）キャンペーンの商品が販売される国。 製品はターゲット国に関連付けられているので、この設定によってキャンペーンで広告する製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （を使用したキャンペーン [!DNL Google Ads] （買い物かご内の商品のみ） [!DNL Google Merchant Center] キャンペーン用にショッピング広告を作成できるアカウント。 dimension=attribute のフォーマットを使用して、製品をフィルタする製品次元と属性の組合せを最大 7 つ入力できます。 複数のフィルターを「>>」区切り文字で区切ります。 使用可能な製品ディメンションのリストについては、「」を参照してください[買い物キャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).」と入力します。</p><p>例：「CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies」</p><p>既存の値を削除するには、 <code>[削除]</code> （角括弧を含む）。</p> |
| [!UICONTROL Languages] | <p>（ネットワークの検索と表示のみ） キャンペーンの広告のターゲット言語。</p><p>このフィールドにも [!UICONTROL Geo Targeting] 新しいキャンペーンのフィールドでは、特定の言語（EUR など）にマッピングされていない通貨を使用したキャンペーンはすべての言語をターゲットにすることを除いて、アカウントに指定された通貨によってデフォルトの言語が決定されます。 このフィールドに値を入力せずに、 [!UICONTROL Geo Targeting] 新しいキャンペーン用のフィールド。デフォルトは <i>[!UICONTROL All]</i>. 既存のキャンペーンに対してこのフィールドを空白のままにした場合、既存の値が保持されます。</p><p>すべての言語を対象にするには、次のように入力します <span style="font-style: italic;">&lt;i span=&quot;&quot; id=&quot;1&quot; translate=&quot;no&quot; />. [!UICONTROL >All]</i></span>特定の言語をターゲットにするには、次のいずれかを使用して、セミコロンで区切られた値を入力します <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] 言語名</a> （例： <i>英語；日本語</i>：正しい数値コードに置き換えられる）または数値コード（例： <i>1000;1005</i>）に設定します。 値では、大文字と小文字が区別されません。</p> |
| [!UICONTROL Location] | キャンペーンの広告を配置する、または広告を除外する地理的な場所。 このフィールドまたは新しいキャンペーンの「言語」フィールドのいずれにも値を入力しない場合、特定の場所（例：EUR）にマッピングされていない通貨を使用したキャンペーンはすべての場所をターゲットにすることを除いて、アカウントに指定された通貨がデフォルトの場所を決定します。 このフィールドに値を入力せずに、 [!UICONTROL Languages] 新しいキャンペーン用の「」フィールド、デフォルトは <i>[!UICONTROL All]</i>. 既存のキャンペーンに対してこのフィールドを空白のままにした場合、既存の値が保持されます。</p><p>特定の場所をターゲットにするには、次のいずれかを使用します [[!DNL Google Ads] 場所名](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （正しい数値コードに置き換えられます）またはロケーション コード：</p><ul><li><p>国/地域：国/地域名を入力します（例：） <i>米国；日本</i>）または数値コード（など <i>2840;2392</i>）に設定します。</p></li><li><p>都道府県/地域：都道府県/地域名を、関連する国/地域の略語と共に入力します（例： <i>東京、JP；ニューヨーク、米国</i>）または数値コード（など <i>20636;21167</i>）に設定します。</p></li><li><p>米国以外の都市：都市名、都道府県/地域名、国/地域の略称（など）を入力します <i>東京都北区</i>）または数値コード（など <i>1028850;1009293</i>）</p></li><li><p>米国の都市圏：都市名、州名、国の略称（など）を入力します <i>バッファロー NY （米国）；ニューヨーク NY （米国）</i>）または数値コード（など <i>514;501</i>）に設定します。</p></li></ul><p>場所を除外するには、場所の名前またはコードの前にマイナス記号（`-`）など <i> – 日本</i>.</p><p><b>注意：</b> 値では、大文字と小文字が区別されません。</p> |
| [!UICONTROL Location Type] | （場所を含める場合） [場所タイプ](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | キャンペーンレベルまたは広告グループレベルで入札調整が行われるデバイスタイプ。 <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>、または <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>（以下を含める場合： [!UICONTROL Location], [!UICONTROL Device]、または [!UICONTROL RLSA] ターゲット）特定の場所、特定のデバイスタイプ、特定のオーディエンスターゲットのいずれかで広告の入札を調整するかどうかを指定します。</p><ul><li><p>キーワードレベルの入札（0% 差）を使用するには、0 を入力します。 新しいターゲットの場合は、空白のままにすることもできます。</p></li><li><p>このターゲットに対して別の入札を使用するには、入札の増減率を入力します。</p></li><ul><li><p>ロケーションおよび RLSA ターゲットの場合、有効な割合は–90 から 900 です。</p></li><li><p>デバイスの入札調整の場合、有効な割合は次のとおりです。</p></li><ul><li><p>（キャンペーン）–100 （デバイスタイプの広告に入札しない場合）または–90～900。</p></li><li><p>（広告グループ）–100 （スマートフォンとタブレットの場合）（デバイスタイプに入札しない場合）、およびすべてのデバイスタイプに対して–90～900。</p></li></ul></ul><li><p>（既存のキャンペーンおよび広告グループ）既存の入札調整を使用するには、これを空白のままにします。</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | （情報提供のために生成されたバルクシートに含まれる） キャンペーンレベルの場所のターゲットまたは RLSA に対してAdobeが推奨する読み取り専用の入札調整。 これは、キャンペーンが（ではなく）重み付けコンバージョン指標を使用する目標を持つポートフォリオにある場合にのみ計算されます [!UICONTROL Maximize Clicks] 目標）を選択し、キャンペーンに少なくとも 2 つの場所ターゲットまたは過去 90 日間に少なくとも 5 回のクリックまたは 5 米ドルのコストの RLSA が含まれている場合。</p><p>推奨値を使用するようにロケーション ターゲットまたは RLSA を手動で編集する場合は、ロケーション ターゲットまたは RLSA を作成してから少なくとも 2 週間待ち、十分なデータ収集が行われるようにし、値を週に 1 回以上変更しないでください。 |
| [!UICONTROL Device Targets] | <p>（従来のキャンペーンタイプのみ）広告を表示できるデバイスは次のとおりです。 <i>[!UICONTROL All]</i>, <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Smartphones]</i>、または <i>[!UICONTROL Tablets]</i>. 新規キャンペーンの場合、デフォルトはです。 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | （従来のキャンペーンタイプのみ。デバイスターゲットに「スマートフォン」または「タブレット」が含まれる場合に適用されます）広告を表示できるオペレーティングシステムは次のとおりです。 <i>[!UICONTROL All]</i>, <i>[!UICONTROL Android]</i>, <i>[!UICONTROL iOS]</i>、または <i>[!UICONTROL Palm]</i>. 新規キャンペーンの場合、デフォルトはです。 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>（従来のキャンペーンタイプのみ。次の場合に適用： [!UICONTROL Device Targets] include ``[!UICONTROL All]「または」[!UICONTROL Smartphones]（参考）スマートフォンが接続される可能性のある携帯電話会社 <i>[!UICONTROL All]</i>、または以下で示される 1 つ以上のキャリア &lt;c span=&quot;&quot; id=&quot;4&quot; translate=&quot;no&quot; />通信事業者コード</i>>,&lt;<i>国コード</i>> （T-Mobile、米国など）以下のリストを使用 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">使用可能な通信事業者およびコード [!DNL Google Ads]</a>. <i>複数のキャリアをセミコロンで区切ります（T-Mobile、US;T-Mobile、GB など）。 新規キャンペーンの場合、デフォルトはです。 <i>[!UICONTROL All]</i>.</p> |
| [!UICONTROL Ad Group Name] | <p>広告グループを識別する一意の名前。 最大長は 255 文字です。末尾の空白文字は保存されません（例えば、「広告グループ 1」は「広告グループ 1」として保存されます）。 このフィールドは、キャンペーンレベルのサイトリンクまたはキャンペーンレベルのデバイスターゲットには適用されません。</p> |
| [!UICONTROL Ad Group Type] | <p>広告グループのタイプ： <i>[!UICONTROL Discovery]</i> （ディスカバリーキャンペーンのみ）、 <i>[!UICONTROL Display]</i> （ディスプレイキャンペーンの場合） <i>[!UICONTROL Search Dynamic]</i> （拡張された動的検索広告の場合）、 <i>[!UICONTROL Search Standard]</i> （検索広告の場合） <i>[!UICONTROL Shopping Product]</i> （ショッピング製品広告の場合）、 <i>[!UICONTROL Shopping Showcase]</i> （作成と編集はサポートされていません）、 <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>（CPC キャンペーンのみ）最大クリック単価（CPC）。これは、金銭的記号や句読点の有無にかかわらず、広告ネットワーク上の広告クリックに対して支払う最高額です。 広告グループとキーワード、製品グループおよび動的検索ターゲットの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 製品グループの場合、製品グループの最下位層の値を設定できます。新規層のデフォルトは、親層から継承されます。</p><p>最適化されたポートフォリオ内の既存の製品グループと動的検索ターゲットの場合、更新は 1 日のみ有効であり、次の最適化サイクルで上書きされます。</p> |
| [!UICONTROL Max Content CPC] | <p>（CPC キャンペーンのみ） 1 クリックあたりの最大コンテンツコスト（CPC）。これは、金銭的な記号や句読点の有無にかかわらず、ディスプレイネットワークサイトから広告クリックに対して支払う最高額です。 プレースメントに基づいていないキャンペーンの広告グループレベルで、値を設定および編集できます。</p> |
| [!UICONTROL Audience Target Method] | <p>（検索ネットワークのみのキャンペーンと既存の読み取り専用キャンペーン [!DNL Gmail] ディスプレイネットワーク上のキャンペーン）次のようにします。</p><ul><li><p><i>[!UICONTROL Target and Bid]</i>：ターゲットオーディエンスに関連付けられているユーザーのうち、広告グループに対する他のターゲットも満たしているユーザーにのみ広告を表示します。</p></li><li><p><i>[!UICONTROL Bid Only]</i>：他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示します。</p><p>ただし、特定のオーディエンスに対してより高い入札を設定すると、それらのオーディエンスに広告が表示される可能性が高くなります。</p></li></ul> |
| [!UICONTROL Keyword] | キーワード文字列。 最大長は 80 文字、10 語以内で、文字、数字、次の特殊文字のみを含めることができます。スペース `# $ & _ - " [ ] ' + . / :`</p><p><b>注意：</b></p><ul><li><p>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] 対象： <i>[!UICONTROL Negative]</i>. 行に広告グループ名が含まれている場合、キーワードはその広告グループから除外されます。 行に広告グループ名が含まれていない場合、キーワードはキャンペーン全体で除外されます。</p></li><li><p>変更， [!DNL Google Ads] キーワードまたは一致タイプは、既存のキーワードを削除し、新しいキーワードを作成します。</p></li></ul> |
| [!UICONTROL Placement] | （コンテンツ一致を使用するキャンペーンのみ）広告を表示できるディスプレイネットワーク内のプレースメント。 次のいずれかを指定します。</p><ul><li><p>Web サイト：有効な URL を入力します。 最上位ドメイン、最上位サブドメイン、または単一のディレクトリ名を持つドメインを指定できます。 URL に疑問符（?）を含めることはできません。 例：<code><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</code></p></li><li><p>特定のページの広告の位置：形式を使用します `<URL> >> <location,sublocation>` （例： `finance.google.com >> Company pages,Top right`）に設定します。</p></li><li><p>トピックカテゴリ：構文を使用します `<category::<category> > <subcategory>` その他（など） `category::Industries > Energy & Utilities > Oil & Gas`）に設定します。</p></li></ul><p><b>注意：</b> 広告グループまたはキャンペーンレベルでプレースメントを除外するには、 [!UICONTROL Match Type] 対象： <i>[!UICONTROL Negative]</i>. 行に広告グループ名が含まれている場合、広告グループのプレースメントは除外されます。 行に広告グループ名が含まれていない場合、キャンペーン全体でそのプレースメントは除外されます。</p> |
| [!UICONTROL Auto Target Expression] | <p>（キャンペーン設定を「」にする場合は必須）[!UICONTROL Use my website contents to target my ads]」が有効になっていません。有効にしていない場合はオプションです）広告グループの動的検索ターゲット。</p><p>すべてのターゲットにアスタリスク（*）を使用します。</p><p>最大 3 つの動的検索条件をターゲットにするには、形式を使用します `<category>=<target>`、ここで `<category>` 以下のカテゴリのいずれかを含めることができます。 個々のカテゴリの複数のターゲットを「\[blank space\] および\[blank space\]」で結合し、複数のカテゴリを「」で結合する[空白スペース] および [空白スペース]」と入力します。</p><ul><li><p><i>[!UICONTROL Category]</i>：特定の値を持つインデックス付きページの拡張された動的検索広告を表示します [!DNL Google Ads] コンテンツのカテゴリ。</p></li><li><p><i>[!UICONTROL URL]</i>：特定の URL を持つインデックス付きページに対して拡張された動的検索広告を表示します。この値は、URL 内の任意の場所に含めることができます。</p></li><li><p><i>[!UICONTROL Page Title]</i>：ページタイトルに特定のテキストを含むインデックス付きページの拡張された動的検索広告を表示します。</p></li><li><p><i>[!UICONTROL Page Content]</i>：特定のコンテンツを含むインデックス付きページの拡張された動的検索広告を表示します。</p></li></ul><p>例：url=shoes.example.com and page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | 親商品グループの階層。<br><br>例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>製品グループ（「brand=acme」や「すべての製品」など）。</p><p><b>注意：</b></p><ul><li><p>指定した製品グループがに存在しない場合 [!UICONTROL Parent Product Groupings] 階層、検索、ソーシャル、Commerceでは、必要な階層の部分を作成します。</p></li><li><p>検索、ソーシャル、Commerceでは、「」が自動的に作成されます[!UICONTROL All Products]で広告グループを作成する場合の「グループ [!DNL Google Ads] 広告グループのデフォルト入札にデフォルト入札が設定されたショッピングキャンペーン。 検索、ソーシャル、Commerceでは、「」が自動的に作成されます[!UICONTROL Everything Else]製品グループ階層の各レベルで、広告グループのデフォルト入札を持つ「グループ。 これらのデフォルトグループを明示的に作成して、除外するか、入札を変更することができます。</p></li><li><p>各広告グループには、「」を含む最大 8 つの製品グループ層を含めることができます[!UICONTROL All Products]」と入力し、他の 7 つの層も選択します。</p></li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティションの種類： <i>下位区分</i> （子製品グループがある場合）、 <i>単位</i> （子製品グループがない場合）。 |
| [!UICONTROL Match Type] | <p>動的検索ターゲットまたは製品グループの場合：動的検索ターゲットまたは製品グループのキーワード照合オプション： <i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索ターゲットのデフォルト）、 <i>[!UICONTROL Product Group]</i> （新製品グループのデフォルト）または <i>[!UICONTROL Negative Product Group]</i> （製品グループを除外する場合）。</p><p>キーワードの場合：キーワードの「キーワード一致」オプション： <i>[!UICONTROL Broad]</i>, <i>[!UICONTROL Phrase]</i>, <i>[!UICONTROL Exact]</i>、または <i>[!UICONTROL Negative]</i> （表示ネットワーク上のキーワードまたはプレースメントを除外するため）。ショッピング広告で使用される製品グループには、次の一致タイプがあります。 <i>[!UICONTROL Product Group]</i>. を使用する場合 <i>[!UICONTROL Negative]</i>また、除外する一致タイプを含める必要があります（例：「負のフレーズ」）。</p><p>新しいキーワードの場合、デフォルトはです。 <i>[!UICONTROL Broad]</i>. 一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。</p><p><b>注意：</b></p><ul><li><p>一致タイプは、キーワードを使用しない展開された動的検索広告には適用されません。</p></li><li><p>の一致タイプの変更 [!DNL Google Ads] keyword 既存のキーワードを削除し、新しいキーワードを作成します。</p></li><li><p>「部分一致」修飾子の場合は、「部分一致」を選択し、近いバリアントが必要なキーワード内の単語の前に+を挿入します（「赤」と「靴」の両方の近いバリアントが必要な場合は「+赤+靴」など）。 <b>注意：</b> 部分一致修飾子は、一部の言語でフレーズ一致と同じ一致動作を持つようになり、2021 年 7 月以降、新しい部分一致修飾子のキーワードを作成できません。 参照： [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/7042511) を参照してください。</p> |
| [!UICONTROL First Page Bid] | （情報提供のために生成されたバルクシートに含まれる）検索結果の最初のページに広告を配置するために必要な入札。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Quality Score] | （情報提供のために生成されたバルクシートに含まれる）検索エンジンがキーワードに割り当てた現在の品質スコア。 この値は広告ネットワークには投稿されません）。 |
| [!UICONTROL Creative Preferred Devices] | （テキスト広告、拡張された動的検索広告、拡張サイトリンク。オプション）広告を表示するデバイスタイプ。 <i>[!UICONTROL All]</i> （デフォルト）または <i>[!UICONTROL Mobile]</i>. 条件 <i>[!UICONTROL Mobile]</i> を指定すると、ネットワークはデスクトップユーザーまたはタブレットユーザーではなく、モバイルデバイスユーザーに広告を表示しようと試みます。 それ以外の場合、ネットワークは任意のデバイスタイプで広告を表示します。</p><p><b>注意：</b></p><ul><li><p>Only administrator and [!DNL Adobe] アカウントマネージャーユーザーはこの設定を編集できます。</p></li><li><p>ネットワークでは、優先デバイスタイプで広告が表示されるとは保証されません。</p></li><li><p>新しい拡張サイトリンクは、既存の拡張サイトリンクがある、またはサイトリンクがないキャンペーンでのみ作成できます。</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | （拡張されたテキスト広告とレスポンシブ検索広告のみ）広告のヘッドライン。各広告は縦棒（&amp;vert;）で区切られます。 各広告タイトルフィールドの最大長は、30 文字または 15 個の 2 バイト文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。</p><p>レスポンシブ検索広告の場合、 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] は必須で、その他すべての広告タイトルフィールドはオプションです。 非必須フィールドの既存の値を削除するには、値を使用します <code>[削除]</code> （角括弧を含む）。</p><p>レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイズ機能を挿入します。 <code>{CUSTOMIZER.AdCustomizerName:DefaultText}</code>（例：） <code>{CUSTOMIZER.Discount:10%}</code></p><p>作成や編集はできませんが、展開されたテキスト広告を削除および編集することはできます。以下の操作を実行できます [!DNL Google Ads] 2022 年 6 月に非推奨（廃止予定）になりました。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>（レスポンシブ検索広告のみ。オプション）対応する広告タイトルをピン留めする位置。 `[null]` （値なし。これにより、すべてのポジションに対して広告タイトルが適格になります）、 <i>1</i>, <i>2</i>、または <i>3</i>. 例えば、 [!UICONTROL Ad Title Position] の値が 1 の場合、広告タイトルは位置 1 にのみ表示されます。 デフォルトでは、すべての広告タイトルが null です（値がありません）。</p><p>既存の値を削除するには、値 <code>[削除]</code> （角括弧を含む）。</p><p><b>注意：</b> 複数の広告タイトルを同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた広告タイトルの 1 つを使用する。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>（拡張された動的検索広告、拡張されたテキスト広告およびレスポンシブ検索広告のみ）広告の本文。 各説明フィールドの最大長は、90 文字または 45 文字の 2 バイト文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。</p><p>レスポンシブ検索広告の場合、次の形式を使用して広告カスタマイズ機能を挿入します。 `{CUSTOMIZER.AdCustomizerName:DefaultText}`（例：） `{CUSTOMIZER.Discount:10%}`</p><p>拡張された動的検索広告には、を使用します [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] のみ。 <b>注意：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</p><p>作成や編集はできませんが、展開されたテキスト広告を削除および編集することはできます。以下の操作を実行できます [!DNL Google Ads] 2022 年 6 月に非推奨（廃止予定）になりました。</p><p>レスポンシブ検索広告の場合、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] は必須で、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、値 <code>[削除]</code> （角括弧を含む）。</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ。オプション）対応する説明をピン留めする位置。 `[null]` （値を指定しないと、すべてのポジションについて説明が有効になります）、 <i>1</i>, <i>2</i>、または <i>3</i>. 例えば、 [!UICONTROL Description 1 Position] の値は 1 で、次の条件を満たす [!UICONTROL Description 1] 位置 1 にのみ表示されます。 デフォルトでは、説明は位置にピン留めされません。</p><p>既存の値を削除するには、値 `[delete]` （角括弧を含む）。</p><p><b>注意：</b> 複数の説明を同じ位置にピン留めできます。 広告ネットワークは、位置にピン留めされた説明の 1 つを使用します。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれる URL。<br><br>拡張された動的検索広告の場合、 [!DNL Google Ads] は、web サイトドメインから動的にこの値を生成するので、値を入力する必要はありません。<br><br>レスポンシブ検索広告では、値を入力する必要はありません。 最終的な URL のドメインから、表示 URL が自動的に抽出されます。 オプションで、「パス 1」および「パス 2」フィールドを使用して URL をカスタマイズできます。<br><br>作成や編集はできませんが、展開されたテキスト広告を削除および編集することはできます。以下の操作を実行できます [!DNL Google Ads] 2022 年 6 月に非推奨（廃止予定）になりました。<br><br><b>注意：</b> （最終的な URL を持つアカウント）表示 URL と最終的な URL のドメイン名は一致する必要があります。</p> |
| [!UICONTROL Display Path 1] | <p>（拡張テキスト広告<span> とレスポンシブ検索広告</span> のみ）</p><p>（任意）最終的な URL から自動的に抽出された、表示 URL に追加されるテキスト。 URL 内では、先頭にスラッシュ（/）が付きます。 パスにスラッシュ （/）や改行（\n）を含めることはできません。 最大長は 15 文字または 7 つの 2 バイト文字です。</p><p>広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`（例：） `{CUSTOMIZER.Discount:10%}`</p><p>例えば、 [!UICONTROL Display Path 1] は「取引」、表示 URL はです &lt;<i>url を表示</i>>/deals （www.example.com/dealsなど）。</p><p>作成や編集はできませんが、展開されたテキスト広告を削除および編集することはできます。以下の操作を実行できます [!DNL Google Ads] 2022 年 6 月に非推奨（廃止予定）になりました。</p> |
| [!UICONTROL Display Path 2] | 2 番目の表示パス。のエントリを参照してください。 [!UICONTROL Display Path 1].<br><br>例：If [!UICONTROL Display Path 1] は「deals」で、 [!UICONTROL Display Path 2] が「ローカル」の場合、表示 URL は &lt; です<i>url を表示</i>>/deals/local （www.example.com/deals/localなど）。</p><p>作成や編集はできませんが、展開されたテキスト広告を削除および編集することはできます。以下の操作を実行できます [!DNL Google Ads] 2022 年 6 月に非推奨（廃止予定）になりました。</p> |
| [!UICONTROL Promotion Line] | （商品リスト広告のみ）検索結果の商品リストに含めるオプションのプロモーションライン。 最大長は 45 文字です。</p><p>プロモーションラインは、広告がページ上のどこに表示されるかに応じて、広告に対して異なる場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Link Name] | <p>サイトリンクテキスト。 最大 25 文字を使用できます。</p><p>新しいサイトリンクの場合は、サイトリンク行にキャンペーン名を含める必要があります。 広告グループレベルのサイトリンクの場合は、広告グループ名も含める必要があります。</p><p><b>注意：</b> 35 文字の既存のテキストは、デスクトップやタブレットの広告には引き続き表示されますが、モバイルデバイスには表示されません。</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | （既存のアプリのインストール広告のみ） モバイルアプリケーションが実行されるオペレーティングシステム。 <i>Android™</i> または <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | （既存のアプリインストール広告のみ） <p>アプリケーション ID またはパッケージ名。 |
| [!UICONTROL Mobile App Name (Google Adwords)] | （既存のアプリのインストール広告のみ）アプリケーションの名前。 |
| [!UICONTROL Start Date] | <p>（強化されたサイトリンクのみ） サイトリンクの入札を行うことができる最初の日付。広告主のタイムゾーンおよび次のいずれかの形式です。 <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i>、または <i>m-d-yy</i>. 新しい拡張サイトリンクのデフォルトは現在の日付です。</p><p><b>注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクがある、またはサイトリンクがないキャンペーンでのみ作成できます。</p> |
| [!UICONTROL End Date] | <p>（サイトのリンクの強化機能のみ）広告主のタイムゾーンおよび次のいずれかの形式で、サイトのリンクに入札を配置できる最後の日付。  <i>m/d/yyyy</i>, <i>m/d/yy</i>, <i>m-d-yyyy</i>、または <i>m-d-yy</i>. デフォルトは「なし」（終了日なし）です。</p><p><b>注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクがある、またはサイトリンクがないキャンペーンでのみ作成できます。</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | （既存のアプリインストール広告のみ）</p><p>（オプション）防止 [!DNL Google Ads] 広告の表示からタブレットユーザーへ。 値には次のものがあります <i>はい</i> および <i>なし</i>. |
| [!UICONTROL Landing Page Suffix] | 情報を追跡するために最終的な URL の末尾に追加するパラメーター。 例： `param2=value1&param3=value2`<br><br>参照先」[のクリック追跡形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).」と入力します。<br><br>下位レベルの最終 URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、次を使用します [!DNL Google Ads] 編集者。 |
| [!UICONTROL Tracking Template] | トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL をに埋め込みます。 [!DNL ValueTrack] パラメーター。 最も詳細なレベルの追跡テンプレート（キーワードを最も詳細なレベルとして）は、それより上のすべてのレベルの値を上書きします。<br><br>キャンペーン設定に「」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキング[!UICONTROL EF Redirect]「」と「」に対して検査する値[!UICONTROL Auto Upload],」という文字列が表示される場合、レコードを保存すると、検索、ソーシャル、Commerce独自のリダイレクトおよびトラッキングコードが自動的に追加されます。<br><br>サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 のリスト用 [!DNL ValueTrack] トラッキングテンプレートで最終的な URL を示すパラメーターについては、「利用可能」の節の「トラッキングテンプレートのみ」のパラメーターを参照してください。 [!DNL ValueTrack] のパラメーター [[!DNL Google Ads] 詳細を見る](https://support.google.com/google-ads/answer/2375447).<br><br>既存の値を削除するには、値 `[delete]` （角括弧を含む）。 |
| [!UICONTROL Base URL/Final URL] | 広告をクリックした際に検索エンジンユーザーが取得されるランディングページの URL （キャンペーンまたはアカウントに設定されている追加パラメーターを含む）。 キーワードレベルのベース URL/最終 URL が、広告レベル以降の URL を上書きします。<br><br>既存の値を削除するには、値 `[delete]` （角括弧を含む）。 |
| [!UICONTROL Destination URL] | （情報目的で生成されたバルクシートに含まれ、検索エンジンに投稿されない）宛先 URL を持つアカウントの場合、これは、広告を広告主の web サイトのベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 検索エンジン固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には「ベース URL/最終 URL」列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | に置き換えるデータ `{custom_code}` 動的変数：変数が検索アカウントまたはキャンペーン設定のトラッキングパラメーターに含まれる場合。 トラッキング URL にカスタム値を挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告フォーマット： <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> （非推奨の広告タイプ）、 <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> （非推奨）、 <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> （ショッピング広告）、 <i>[!UICONTROL Responsive search ad]</i>. 新規広告のデフォルトはです。 <i>[!UICONTROL Text ad]</i>.<br><br>製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Param1] | <p>の数値 `{param1}` 広告パラメーター（バルクシートファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます）。 最大長は 25 文字で、次のヌン数字を含めることができます。</p><ul><li><p>値の先頭または末尾に通貨記号またはコードを付けることができます。 例： `£2.000,00` および `2000GBP` 有効です。</p></li><li><p>値にはコンマ（`,`）またはピリオド（`.`）を区切り文字として使用し、必要に応じてピリオド（`.`）またはコンマ （`,`）に設定する必要があります。 例： `1,000.00` および `2.000,10` 有効です。</p></li><li><p>値の前にはパーセント記号（`%`）、プラス記号（`+`）またはマイナス記号（`- `）に設定します。 例： `20%`, `208+`、および `-42.32` 有効です。</p></li><li><p>2 つの数値をスラッシュで埋め込むことができます。 例： `4/1` および `0.95/0.45` 有効です。</p></li></ul><p>既存の値を削除するには、値 `[delete]` （角括弧を含む）。</p> |
| [!UICONTROL Param2] | の数値 `{param2}` 広告パラメーター（バルクシートファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます）。 詳しくは、Param1 のエントリを参照してください。 |
| [!UICONTROL Audience] | 検索広告（RLSA）のリマーケティングリストは、キャンペーンまたは広告グループのターゲットオーディエンスまたは除外オーディエンスをターゲットにします。 「ターゲットタイプ」フィールドで、ターゲットか除外かを指定します。 |
| [!UICONTROL Target Type] | （オーディエンスが指定された場合）指定されたオーディエンスが <i>Inclusion</i> （ターゲット）または <i>除外</i>. |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> （編集不可）、 <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新規キャンペーンのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブまたは一時停止されたキャンペーンを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ） 新しい広告グループのデフォルトはです。 [!UICONTROL Active]. アクティブまたは一時停止されている広告グループを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは [!UICONTROL Active]. アクティブまたは一時停止したキーワードを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 広告の表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> （既存の広告のみ） <i>[!UICONTROL Disapproved]</i> （編集不可）、 <i>[!UICONTROL Paused]</i>. 新規広告のデフォルトはです。 [!UICONTROL Active]. アクティブまたは一時停止した広告を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | Web サイトプレースメントのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存の広告のみ） 新しい Web サイトのデフォルトはです。 <i>アクティブ。</i> アクティブなプレースメントまたは一時停止したプレースメントを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i> （既存のターゲットのみ） 新しいターゲットのデフォルトはです。 <i>アクティブ。</i> アクティブまたは一時停止したターゲットを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス： <i>[!UICONTROL Active]</i> <span>または</span> <i>[!UICONTROL Deleted]</i> （既存の製品グループのみ） 新製品グループのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブな製品グループを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス： <i>アクティブまたは削除済み</i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブなサイトリンクを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Location Status] | 場所ターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトはです [!UICONTROL Active]. アクティブな位置を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | キャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外のステータス： <i>[!UICONTROL Active]</i> または [!UICONTROL Deleted]</i> （既存のターゲットのみ） 新しいターゲットまたは除外のデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブなターゲットまたは除外を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Device Target Status] | <p>キャンペーンレベルまたは広告グループレベルのデバイスターゲットのステータス。 <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i>. 新規キャンペーンおよび広告グループの場合、デフォルトはです。 <i>[!UICONTROL Active]</i>.</p> |
| \[ 広告主固有のラベル分類\] | （広告主固有のラベル分類に対して名前が付けられます。例えば、色と呼ばれるラベル分類の「色」など） エンティティに関連付けられている、指定された分類の値。 エンティティごとに分類ごとに 1 つの値のみを含めることができます（キャンペーン A の「カラー」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加する新しいコンポーネントは、自動的にラベルに関連付けられます。 製品グループのラベル分類は、単位（最も詳細な単位）レベルで適用されます。<br><br>分類名と分類値では、大文字と小文字が区別されません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられている制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><b>> 制約は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に「」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に「」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） キーワードを識別するのに十分なプロパティ列、または b） &#39;&#39;が含まれていない限り、キーワードを変更する場合にのみ必要です。[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] レスポンシブ検索広告の場合、広告データの編集または削除には広告 ID または AMO ID が必要です。 その他のすべてのエンティティタイプでは、広告 ID が必要になるのは広告ステータスを変更した場合のみです。ただし、行に（a）広告を識別するのに十分な広告プロパティ列、または（b） ``[!UICONTROL AMO ID]&quot;.&quot; ただし、に加えて [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]の場合、広告プロパティ列が複数の広告に一致すると、1 つの広告のステータスのみが変更されます。</p><p><b>注意：</b> a）既存の広告のステータスを除く広告プロパティ列、または b） レスポンシブ検索広告のデータを編集し、どちらにも含めない場合 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を選択すると、新しい広告が作成されますが、既存の広告は変更されません。</p> |
| [!UICONTROL Placement ID] | Web サイトプレースメントを識別する一意の ID。 行に（a）プレースメントを識別するのに十分なプロパティ列が含まれている場合、または（b） &#39;&#39;が含まれていない限り、プレースメントを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意の ID。 行に「」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。 |
| [!UICONTROL Product Group ID] | 既存の商品グループを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 製品グループを変更または削除した場合にのみ必要です。ただし、行に（a）製品グループを識別するのに十分なプロパティ列、または（b） ``[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に a） サイトリンクを識別するのに十分なプロパティ列、または b） &#39;&#39;が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。[!UICONTROL AMO ID]&quot;.&quot; ただし、どちらも含めない場合は、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]の各プロパティ列が複数のサイトリンクと一致する場合、1 つのサイトリンクのステータスのみが変更されます。</p><p><b>注意：</b> 既存のサイトリンクのステータスを除くサイトリンクプロパティの列を編集する場合に、を含めることはできません [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]を選択すると、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に「」が含まれていない限り、ターゲットまたは除外を変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。 |
| [!UICONTROL Device Target ID] | <p>既存のキャンペーンレベルまたは広告グループレベルのデバイスのターゲットまたは除外を識別する一意の ID。 CSV および TSV ファイルでは、一重引用符（&#39;）で始める必要があります。[^1] 行に「」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。</p> |
| [!UICONTROL AMO ID] | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意の ID。 レスポンシブ検索広告の場合、広告 ID を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つその他すべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID でデータを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |
| [!UICONTROL EF Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは次に含まれます [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報提供のために生成されたバルクシートに含まれる）行内のデータに関する広告ネットワークのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは次に含まれます [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報提供のために生成されたバルクシートに含まれる）任意の項目の名前とテキストを表示するためのプレースホルダー [!DNL Google Ads] 広告が違反する広告ポリシー。 |
| [!UICONTROL Retail Hash] | （詳細Campaign Managementを使用して生成されたバルクシートに含まれる）項目が詳細（ACM）ビューを使用して生成されたことを示す英数字のハッシュコード（f9639f40cdf56524b541e5dacf55a991 など）。 |

[^1]: [!DNL Excel] ファイルを開いたときに、大きな数値を指数表記（2115585666 の場合は 2.12E+09 など）に変換します。 標準の表記で数字を表示するには、列の任意のセルを選択して、式バーの内側をクリックします。

## 各アカウントコンポーネントを作成、編集または削除するために必要なフィールド {#bulksheet-fields-per-component-google}

以下の節には、特定のアカウントエンティティに関連するフィールドが含まれます。

>[!NOTE]
>
>フィールドがアクションに適用できない場合、フィールドに入力された値は無視されます。

### キャンペーンフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Campaign ID] | 行に「」が含まれていない限り、キャンペーン名を変更する場合にのみ必要です[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### 広告グループフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Ad Group ID] | 行に「」が含まれていない限り、広告グループ名を変更する場合にのみ必要です[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### キーワードフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Keyword ID] | 行に a） キーワードを識別するのに十分なプロパティ列が含まれている場合、または b） ```が含まれている場合を除き、キーワードを編集または削除する場合にのみ必要です[!UICONTROL AMO ID].」と入力します。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### プレースメントフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Placement ID] | 行に（a）プレースメントを識別するのに十分なプロパティ列が含まれている場合、または（b） ```が含まれていない限り、プレースメントを編集または削除する場合にのみ必要です[!UICONTROL AMO ID].」と入力します。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### 動的検索広告を拡張しました

この広告タイプは、では「動的検索広告」と呼ばれるようになりました。 [!DNL Google Ads]. 動的検索広告の作成について詳しくは、「」を参照してください[実装方法 [!DNL Google Ads] 動的検索広告](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html).」と入力します。

この広告タイプには、「[!UICONTROL Creative (except RSA)]の``行 [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 広告の作成または説明の編集に必要。 <b>注意：</b> この広告タイプの場合、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列が含まれている場合、または（b） ``[!UICONTROL AMO ID].」と入力します。 ただし、に加えて [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]の場合、広告プロパティ列が複数の広告に一致すると、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### 商品リスト / ショッピング広告フィールド

ショッピング広告の作成について詳しくは、「」を参照してください[実装方法 [!DNL Google Ads] 買い物キャンペーン](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html).」と入力します。

この広告タイプには、「[!UICONTROL Creative (except RSA)]の``行 [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列が含まれている場合、または（b） ``[!UICONTROL AMO ID].」と入力します。 ただし、に加えて [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]の場合、広告プロパティ列が複数の広告に一致すると、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### レスポンシブ検索広告フィールド

この広告タイプには、「[!UICONTROL Responsive Search Ad]の``行 [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | レスポンシブ検索広告の場合、 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] 広告の作成には必須で、その他の広告タイトルフィールドはすべてオプションです。 非必須フィールドの既存の値を削除するには、値を使用します `[delete]` （角括弧を含む）。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] 広告の作成に必要な場合。 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、値 `[delete]` （角括弧を含む）。 |
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
| [!UICONTROL Ad ID] | 行に「」が含まれていない場合、広告を編集または削除する必要があります[!UICONTROL AMO ID].」と入力します。 |
| [!UICONTROL AMO ID] | 広告 ID を含めない場合、広告を編集または削除する必要があります。 |

### テキストとフィールド

この広告タイプには、「[!UICONTROL Creative (except RSA)]の``行 [!UICONTROL Download Bulksheet] ダイアログ。

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

>[!NOTE]
>
>拡張テキスト広告は、2022 年 6 月に非推奨（廃止予定）となりました。 既存のテキスト広告のみを削除できます。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | 読み取り専用 |
| [!UICONTROL Ad Title]、広告タイトル 2 ～ 3 | 読み取り専用 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] 読み取り専用 |
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
| [!UICONTROL Ad ID] | 行に（a）広告を識別するのに十分な広告プロパティ列が含まれている場合、または（b） ``[!UICONTROL AMO ID].」と入力します。 ただし、に加えて [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]の場合、広告プロパティ列が複数の広告に一致すると、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### 動的検索のターゲット（自動ターゲット）フィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Auto Target Expression] | キャンペーン設定が「」の場合にのみ必要です[!UICONTROL Use my website contents to target my ads]」が有効になっていません。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Target Status] | ターゲットの削除が必要です |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 行に「」が含まれていない限り、自動ターゲットを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### ショッピング製品グループ フィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Product Group ID] | 製品グループを変更または削除した場合にのみ必要です。ただし、行に（a）製品グループを識別するのに十分なプロパティ列、または（b） ``[!UICONTROL AMO ID].」と入力します。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのサイトリンクフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
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
| [!UICONTROL Sitelink ID] | 行に a） サイトリンクを識別するのに十分なプロパティ列、または b） &#39;&#39;が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。[!UICONTROL AMO ID].」と入力します。 ただし、どちらも含めない場合は、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  プロパティ列が複数のサイトリンクと一致する場合は、1 つのサイトリンクのステータスのみが変更されます。<br><br><b>注意：</b> 次の場合を除き、サイトリンクプロパティの列を編集します [!UICONTROL Status] 既存のサイトリンクに対して、にも含めない [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]を選択すると、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない場合は、データを編集または削除する必要があります。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### 場所のターゲット

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | 場所のターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | を含めない限り、データの編集または削除に必要です。 [!UICONTROL Campaign ID].<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスのターゲットフィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを作成または編集するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必要。 キャンペーンレベルのデバイスターゲットには適用されません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのデバイスターゲットにのみ適用できます。 |
| [!UICONTROL Device Target ID] | 行に「」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。 |
| [!UICONTROL AMO ID] | デバイスターゲット ID を含めない限り、データの編集または削除に必要です。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルの RLSA ターゲット/除外フィールド

各データフィールドの説明については、「」を参照してください[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).」と入力します。

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「」が含まれていない場合は必須[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットおよび除外に必要。 キャンペーンレベルのターゲットおよび除外には適用されません。 |
| [!UICONTROL Audience] | 新しいターゲットまたは除外の作成に必要です。 |
| [!UICONTROL Target Type] | 新しいターゲットまたは除外の作成に必要です。 |
| [!UICONTROL RLSA Target Status] | ターゲットまたは除外を削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのターゲットと除外にのみ適用できます。 |
| [!UICONTROL RLSA Target ID] | 行に「」が含まれていない限り、ターゲットを変更または削除する場合にのみ必要です[!UICONTROL AMO ID]」に設定する必要があります。 |
| [!UICONTROL AMO ID] | RLSA ターゲット ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、Commerceは、値を使用して編集する正しい ID を判断しますが、ID は広告ネットワークに投稿しません。 |

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルのダウンロードと作成](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正されたエラーファイルのアップロード](../bulksheet-upload.md)
