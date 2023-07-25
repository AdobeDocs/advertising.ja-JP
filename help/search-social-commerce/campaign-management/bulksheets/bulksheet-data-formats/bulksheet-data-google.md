---
title: 次に必要なバルクシートデータ： [!DNL Google Ads] アカウント
description: 次のバルクシートで、必須ヘッダーフィールドとデータフィールドを参照します： [!DNL Google Ads] アカウント。
exl-id: 1e35f503-c2fe-459c-ad13-6b8cf65be67e
source-git-commit: 16e7a310571000fc5b584eb67c832df1e12cea72
workflow-type: tm+mt
source-wordcount: '7729'
ht-degree: 0%

---

# 付録 — の必須バルクシートデータ [!DNL Google Ads] アカウント

作成および更新するには [!DNL Google Ads] キャンペーンデータを一括で使用する場合は、専用の形式の検索、ソーシャル、コマースのバルクシートファイルを使用できます。 [!DNL Google Ads] アカウント。 次のいずれかを実行できます。a) [既存のアカウントに対してバルクシートファイルを生成](../bulksheet-download.md) 必要なファイル形式で、または b) 手動で作成する ([サポートされるバルクシートファイル形式](bulksheet-file-formats.md)」を参照してください )。

各バルクシートには、ヘッダーフィールドと、 [実行する特定の操作](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md) （広告の作成など）。 フィールドが必須でない場合は、ヘッダー行とデータ行から省略できます。 バルクシートファイルをアップロードすると、すべてのカスタム列が削除されます。

以下に、使用可能なすべてのデータフィールドの表と、個々のエンティティ（キャンペーン、キーワードなど）のデータの追加、編集、削除に必要なフィールドを示す追加テーブルを示します。

## すべての使用可能なデータフィールド {#bulksheet-fields-all-google}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、[各アカウントコンポーネントの作成、編集または削除に必要なフィールド](#bulksheet-fields-per-component-google).

>[!NOTE]
>
>* すべてのテキスト列の値では、大文字と小文字が区別されます。
>* 新しいレコードを作成し、すべての必須データフィールドの値を含めない場合、これらのフィールドの一部には指定されたデフォルト値が割り当てられます。
>* 以下に指定されていないフィールドの場合は、広告ネットワークのデフォルト値が使用されます。
>* で使用可能な一括シート行のリスト [!UICONTROL Download Bulksheet] ダイアログは、[広告ネットワーク別のバルクシート行](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md#bulksheet-rows-by-ad-network).&quot;

| フィールド | 説明 |
| ---- | ---- |
| [!UICONTROL Platform] | （情報を提供するために生成された一括送信シートに含まれます）広告プラットフォーム。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンに対する 1 日の支出制限。通貨記号や句読点の有無は問いません。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | <p>キャンペーンの広告を 1 日に表示する速度：</p><ul><li><p><i>[!UICONTROL Standard (Distributed)]</i> （新規キャンペーンのデフォルト）:広告インプレッションを 1 日にわたって広める。</p></li><li><p><i>[!UICONTROL Accelerated]:</i> （2019 年 10 月に廃止）予算に達するまで、可能な限り頻繁に広告を表示します。 その結果、広告が 1 日後に表示されない場合があります。</p></li></ul> |
| [!UICONTROL Channel Type] | <p>広告を配置するチャネル。 1 つ以上のオプションを指定します。</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Search]</i></span> （新規キャンペーンのデフォルト）:広告を [!DNL Google Ads] 検索ネットワーク ( [!DNL Google Ads] 検索と検索のパートナー Web サイトを参照 )、およびオプションで [!DNL Google Ads] ディスプレイネットワーク。 <b>注意：</b> 検索ネットワークとディスプレイネットワークの両方をターゲットにするキャンペーンを、入札の最適化のためにポートフォリオに追加することはできません。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Display]</i></span>:広告を [!DNL Google Ads] ディスプレイネットワーク。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Shopping]</i></span>:ショッピング広告を配置するには [!DNL Google Ads] ショッピングネットワーク（一部の国）と [!DNL Google Ads] 検索ネットワーク ( [!DNL Google Ads] 検索と検索のパートナー web サイトを参照 )。 ショッピング広告を作成するには、 [!DNL Google Merchant Center] アカウントと [検索、ソーシャル、コマースがアカウントからデータをダウンロードすることを許可](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md). 参照：[実装方法 [!DNL Google Ads] ショッピングキャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」を参照してください。</p></li></ul> |
| [!UICONTROL Networks] | <p>広告の配置場所。 1 つ以上のオプションを指定します。</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Google Search]</i></span>:Google Search Network のみのスポンサー付き検索リスト。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Search Partners]</i></span>:Googleの検索パートナーに関するスポンサー付き検索リスト。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Content]</i></span>:ネットワークリストを表示する入札を行う。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL All]</i></span> （新規キャンペーンのデフォルト）:Google検索、検索パートナー、コンテンツをターゲットに設定します。</p></li></ul> |
| [!UICONTROL DSA Domain Name] | <p>( 検索ネットワークのみ、拡張された動的検索広告のみに適用可能 ) 広告ネットワークが動的検索広告をターゲットにしてコンテンツを使用する Web サイトのルートドメイン（example.com など）またはサブドメイン（shoes.example.com など）。<br><br><b>メモ：</b></p><ul><li><p>動的検索広告の拡張により、キーワードではなく Web サイトのコンテンツがターゲットになります。</p></li><li><p>ターゲットにするドメインは、広告ネットワークのオーガニック検索インデックスによってインデックス付けされる必要があります。</p></li><li><p>ドメインを指定しない場合、各広告グループに対して、すべての Web サイトページまたはそのサブセットをターゲットにする動的検索ターゲットを作成する必要があります。</p></li></ul> |
| [!UICONTROL DSA Domain Language] | ( 検索ネットワークのみ、拡張された動的検索広告のみに適用 ) 指定された Web サイトドメインの言語。 <b>注意：</b> ドメインに複数の言語のページが含まれ、それらすべてをターゲットにする場合は、言語ごとに個別のキャンペーンを作成します。 |
| [!UICONTROL GDN Custom Bid Level] | （ディスプレイネットワークのみをターゲットにするキャンペーン）入札方法：作成者 <span style="font-style: italic;"><i>[!UICONTROL Ad Group]</i></span> （デフォルト） <span style="font-style: italic;"><i>[!UICONTROL Keyword]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Placement]</i></span> （Web サイト）、または <span style="font-style: italic;"><i>[!UICONTROL None]</i></span> （既存の値をリセット）。 その他のディメンション (<span style="font-style: italic;"><i>年齢</i></span>, <span style="font-style: italic;"><i>性別</i></span>, <span style="font-style: italic;"><i>関心とリスト</i></span>, <span style="font-style: italic;"><i>トピック</i></span>、および <span style="font-style: italic;"><i>垂直方向</i></span>) は、 [!DNL Google Ads] インターフェイス。 以前に [!DNL Google Ads] 別のディメンションによる入札を設定するインターフェイスでは、その値が表示されますが、ここでは、これらのディメンションを選択または入力できません。</p><p><b>注意：</b></p><ul><li><p>キーワードで入札する場合は、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメントで入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他すべてのディメンションについては、広告レベルでトラッキングテンプレートを作成します。</p></li><li><p>サポートされていないディメンション（年齢、性別、興味、リスト、トピック）で入札した場合、検索、ソーシャル、コマースではディメンションの入札が最適化されず、すべてのアトリビューションが広告グループに適用されます。</p></li><li><p>検索ネットワーク上の広告は、常にキーワード入札を使用します。</p></li></ul> |
| [!UICONTROL Campaign Priority] | <p>（買い物キャンペーンのみ）複数のキャンペーンが同じ製品を宣伝する場合に使用される優先順位：  <span style="font-style: italic;"><i>[!UICONTROL Low]</i></span> （新しいキャンペーンのデフォルト） <span style="font-style: italic;"><i>[!UICONTROL Medium]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL High]</i></span>.</p><p>同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークは、まずキャンペーンの優先順位を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Merchant ID] | （マーチャントフィードにリンクされたショッピングキャンペーンおよびオーディエンスキャンペーンのみ）商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。 |  |
| [!UICONTROL Sales Country] | ( 買い物キャンペーンのみ、既存のキャンペーンの読み取り専用 ) キャンペーンの製品が販売された国。 製品は対象国に関連付けられているので、この設定によってキャンペーンで広告される製品が決まります。 |
| [!UICONTROL Product Scope Filter] | ( [!DNL Google Ads] （買い物ネットワークのみ） [!DNL Google Merchant Center] キャンペーン用にショッピング広告を作成できるアカウント。 dimension=attribute の形式を使用して、製品をフィルタリングする製品次元と属性の組み合わせを 7 つまで入力できます。 複数のフィルターは「>>」区切り文字で区切ります。 使用可能な製品ディメンションのリストについては、[買い物キャンペーンの製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md).&quot;</p><p>例：&quot;CategoryL1=animals>>CategoryL2=pet supplies>>Brand=Acme Pet Supplies&quot;</p><p>既存の値を削除するには、 <span class="Code">[削除]</span> （括弧を含む）</p> |
| [!UICONTROL Languages] | <p>（検索および表示ネットワークのみ）キャンペーンの広告のターゲット言語。</p><p>このフィールドまたは [!UICONTROL Geo Targeting] 新しいキャンペーンのフィールドで、アカウントに対して指定された通貨によってデフォルト言語が決まります。ただし、特定の言語にマッピングされていない通貨（EUR など）のキャンペーンはすべての言語をターゲットにします。 このフィールドに値を入力しない場合は、 [!UICONTROL Geo Targeting] 新しいキャンペーンのフィールド。デフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>. 既存のキャンペーンでこのフィールドを空白にした場合、既存の値が保持されます。</p><p>すべての言語をターゲットにするには、 <span style="font-style: italic;">&lt;i span=&quot;&quot; id=&quot;1&quot; translate=&quot;no&quot; />. [!UICONTROL >All]</i></span>特定の言語をターゲットにするには、次のいずれかを使用して、セミコロンで区切った値を入力します。 <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#languages" target="_blank">[!DNL Google Ads] 言語名</a> ( <span style="font-style: italic;"><i>英語；日本語</i></span>（正しい数値コードで置き換えられる）または数値コード ( <span style="font-style: italic;"><i>1000;1005</i></span>) をクリックします。 値では大文字と小文字が区別されません。</p> |
| [!UICONTROL Location] | キャンペーンの広告を配置する、または広告を除外する地理的な場所。 このフィールドまたは新しいキャンペーンの「言語」フィールドに値を入力しない場合、特定の場所（EUR など）にマッピングされていない通貨を持つキャンペーンがすべての場所をターゲットにする点を除き、アカウントで指定された通貨がデフォルトの場所です。 このフィールドに値を入力しない場合は、 [!UICONTROL Languages] 新しいキャンペーンのフィールドを選択すると、デフォルトはになります。 <i>[!UICONTROL All]</i>. 既存のキャンペーンでこのフィールドを空白のままにした場合、既存の値が保持されます。</p><p>特定の場所をターゲットにするには、次のいずれかを使用します。 [[!DNL Google Ads] 場所名](https://developers.google.com/adwords/api/docs/appendix/geotargeting) （正しい数値コードで置き換えられる）または場所コード：</p><ul><li><p>国/地域：国名または地域名 ( 例： <span style="font-style: italic;"><i>米国；日本</i></span>) または数値コード ( <span style="font-style: italic;"><i>2840;2392</i></span>) をクリックします。</p></li><li><p>都道府県/地域：州/都道府県/地域の名前を、関連する国/地域の略語 ( <span style="font-style: italic;"><i>東京、JP；ニューヨーク、米国</i></span>) または数値コード ( <span style="font-style: italic;"><i>20636;21167</i></span>) をクリックします。</p></li><li><p>米国以外の都市：市区町村名、都道府県/地域名、国/地域の略語 ( 例： <span style="font-style: italic;"><i>足立，東京， JP；北，東京， JP</i></span>) または数値コード ( <span style="font-style: italic;"><i>1028850;1009293</i></span>)</p></li><li><p>米国の主要都市：市区町村名、都道府県名、国の略語 ( <span style="font-style: italic;"><i>バッファロー NY, US；ニューヨーク NY, US</i></span>) または数値コード ( <span style="font-style: italic;"><i>514;501</i></span>) をクリックします。</p></li></ul><p>場所を除外するには、場所名またはコードの前にマイナス記号 (`-`など ) <span style="font-style: italic;"><i> — 日本</i></span>.</p><p><b>注意：</b> 値では大文字と小文字が区別されません。</p> |
| [!UICONTROL Location Type] | （場所を含める場合） [場所の種類](https://developers.google.com/google-ads/api/data/geotargets). |
| [!UICONTROL Device] | キャンペーンまたは広告グループレベルで入札調整がおこなわれるデバイスタイプ。 <i>[!UICONTROL smartphone]</i>, <i>[!UICONTROL tablet]</i>または <i>[!UICONTROL desktop]</i>. |
| [!UICONTROL Bid Adjustment] | <p>( [!UICONTROL Location], [!UICONTROL Device]または [!UICONTROL RLSA] （ターゲット）特定の場所、特定のデバイスタイプ、または特定のオーディエンスターゲットのどちらで広告の入札を調整するかを指定します。</p><ul><li><p>キーワードレベルの入札（0%の差異）を使用するには、0 を入力します。 新しいターゲットの場合は、空白のままにすることもできます。</p></li><li><p>このターゲットに異なる入札を使用するには、入札を増減する割合を入力します。</p></li><ul><li><p>ロケーションおよび RLSA ターゲットの場合、有効な割合は —90 ～ 900 です。</p></li><li><p>デバイスの入札調整の場合、有効な割合は次のとおりです。</p></li><ul><li><p>（キャンペーン） —100（デバイスタイプで広告を入札しない）または —90～900。</p></li><li><p>（広告グループ） -100 （デバイスタイプに対して入札しない）、-90 ～ 900 （すべてのデバイスタイプに対して）。</p></li></ul></ul><li><p>（既存のキャンペーンおよび広告グループ）既存の入札調整を使用する場合は、これを空白のままにします。</p></li></ul> |
| [!UICONTROL Adobe Rec Bid Adjustment] | （情報提供のために生成された一括送信シートに含まれます）Adobeがキャンペーンレベルのロケーションターゲットまたは RLSA に推奨する読み取り専用の入札調整。 キャンペーンが重み付けされた収益の目標 ( [!UICONTROL Maximize Clicks] 目的として )、およびキャンペーンに 2 つ以上のロケーションターゲットまたは RLSA が含まれている（過去 90 日間に 5 回以上のクリックまたは 5 USD のコストがかかる）場合。</p><p>ロケーションターゲットまたは RLSA を手動で編集して推奨値を使用する場合は、ロケーションターゲットまたは RLSA を作成して十分なデータ収集を可能にしてから 2 週間以上待ち、値を週に 1 回以上変更しないでください。 |
| [!UICONTROL Device Targets] | <p>（従来のキャンペーンタイプのみ）広告が表示されるデバイス： <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Computers]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Smartphones]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL Tablets]</i></span>. 新規キャンペーンの場合、デフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Device OS Targets (Google Adwords)] | ( 従来のキャンペーンタイプのみ、デバイスターゲットに「スマートフォン」または「タブレット」が含まれる場合に適用 ) 広告が表示されるオペレーティングシステム： <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Android]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL iOS]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL Palm]</i></span>. 新規キャンペーンの場合、デフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Mobile Carriers (Google Adwords)] | <p>( 従来のキャンペーンタイプのみ、該当する場合 [!UICONTROL Device Targets] &quot;[!UICONTROL All]&quot;または&quot;[!UICONTROL Smartphones]（イ）スマートフォンが接続される携帯電話会社 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>または 1 つ以上の通信事業者で、 &lt;c span=&quot;&quot; id=&quot;4&quot; translate=&quot;no&quot; />キャリアコード</i></span>>,&lt;<span style="font-style: italic;"><i>国コード</i></span>>（T-Mobile、US など） <a href="https://developers.google.com/adwords/api/docs/appendix/codes-formats?csw=1#mobile-carriers" target="_blank">使用可能な通信事業者およびコード [!DNL Google Ads]</a>. <span style="font-style: italic;"><i>複数の通信事業者をセミコロンで区切ります（T-Mobile、US、T-Mobile、GB など）。 新規キャンペーンの場合、デフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span>.</p> |
| [!UICONTROL Ad Group Name] | <p>広告グループを識別する一意の名前。 最大長は 255 文字です。末尾の空白文字は保存されません（例えば、「Ad Group 1」は「Ad Group 1」として保存されます）。 このフィールドは、キャンペーンレベルのサイトリンクや、キャンペーンレベルのデバイスターゲットには適用されません。</p> |
| [!UICONTROL Ad Group Type] | <p>広告グループのタイプ： <i>[!UICONTROL Discovery]</i> （検出キャンペーンのみ） <i>[!UICONTROL Display]</i> （ディスプレイキャンペーンの場合） <i>[!UICONTROL Search Dynamic]</i> （拡張された動的検索広告の場合） <i>[!UICONTROL Search Standard]</i> （検索広告の場合）、 <i>[!UICONTROL Shopping Product]</i> （買い物製品広告の場合） <i>[!UICONTROL Shopping Showcase]</i> （作成と編集はサポートされていません）、または <i>[!UICONTROL Unknown]</i>.</p> |
| [!UICONTROL Max CPC] | <p>（CPC キャンペーンのみ）最大クリック単価 (CPC)。広告ネットワーク上での広告クリックに対して支払われる最高の金額で、通貨記号や句読点の有無は問いません。 広告グループとキーワード、製品グループ、動的検索ターゲットの値を設定できます。 新しいキーワードのデフォルトは、広告グループレベルから継承されます。 製品グループの場合は、最も低い製品グループ層の値を設定できます。新しい層のデフォルトは親層から継承されます。</p><p>最適化されたポートフォリオ内の既存の製品グループと動的検索ターゲットの場合、更新は 1 日のみ有効で、次の最適化サイクルで上書きされます。</p> |
| [!UICONTROL Max Content CPC] | <p>（CPC キャンペーンのみ）最大コンテンツコストパークリック (CPC)。ディスプレイネットワークサイトから広告クリックに支払う最も高い金額で、通貨記号や句読点の有無は問いません。 プレースメントターゲット設定されていないキャンペーンの広告グループレベルで値を設定および編集できます。</p> |
| [!UICONTROL Audience Target Method] | <p>( 検索ネットワーク上のキャンペーンと、既存の読み取り専用 [!DNL Gmail] ディスプレイネットワーク上のキャンペーン ) 次のどちらを実行するかを指定します。</p><ul><li><p><span style="font-style: italic;"><i>[!UICONTROL Target and Bid]</i></span>:広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーに対してのみ広告を表示する。</p></li><li><p><span style="font-style: italic;"><i>[!UICONTROL Bid Only]</i></span>:ターゲットオーディエンスに関連付けられていないユーザーが他の広告グループレベルのターゲットを満たしている限り、広告を表示する。</p><p>ただし、特定のオーディエンスに対して広告が表示される可能性を高めるには、それらのオーディエンスの入札額を高く設定します。</p></li></ul> |
| [!UICONTROL Keyword] | キーワード文字列。 最大長は 80 文字で 10 語以下で、文字、数字、次の特殊文字のみを含めることができます。space `# $ & _ - " [ ] ' + . / :`</p><p><b>注意：</b></p><ul><li><p>広告グループまたはキャンペーンレベルでキーワードを除外するには、 [!UICONTROL Match Type] から <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>. 行に広告グループ名が含まれる場合、そのキーワードは広告グループに対して除外されます。 行に広告グループ名が含まれていない場合、このキーワードはキャンペーン全体に対して除外されます。</p></li><li><p>の変更 [!DNL Google Ads] キーワードまたは一致タイプは、既存のキーワードを削除し、新しいキーワードを作成します。</p></li></ul> |
| [!UICONTROL Placement] | （コンテンツの一致のみを使用するキャンペーン）広告が表示されるディスプレイネットワーク内の配置。 次のいずれかを指定します。</p><ul><li class="p"><p>Web サイト：有効な URL を入力してください。 最上位ドメイン、第 1 レベルサブドメイン、または単一のディレクトリ名を持つドメインにすることができます。 URL に疑問符 (?) を含めることはできません。 例：<span class="Code"><br />www.example.com<br />example.com<br />autos.example.com<br />example.com/widgets</span></p></li><li class="p"><p>特定のページ上の広告の位置：形式を使用 `<URL> >> <location,sublocation>` ( `finance.google.com >> Company pages,Top right`) をクリックします。</p></li><li class="p"><p>トピックカテゴリ：構文を使用します。 `<category::<category> > <subcategory>` その他 ( `category::Industries > Energy & Utilities > Oil & Gas`) をクリックします。</p></li></ul><p><b>注意：</b> 広告グループまたはキャンペーンレベルでプレースメントを除外するには、 [!UICONTROL Match Type] から <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>. 行に広告グループ名が含まれる場合、プレースメントは広告グループに対して除外されます。 行に広告グループ名が含まれていない場合、配置はキャンペーン全体に対して除外されます。</p> |
| [!UICONTROL Auto Target Expression] | <p>( キャンペーンを「[!UICONTROL Use my website contents to target my ads]「」が有効になっていません。それ以外の場合はオプション ) 広告グループの動的検索ターゲット。</p><p>すべてのターゲットに対して、アスタリスク (*) を使用します。</p><p>最大 3 つの動的検索条件をターゲットにするには、という形式を使用します。 `<category>=<target>`で、 `<category>` には、以下の任意のカテゴリを含めることができます。 個々のカテゴリの複数のターゲットを「\[ 空白スペース\]」および「\[ 空白スペース\]」で結合し、複数のカテゴリを「[空白] および [空白]&quot;.</p><ul><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Category]</i></span>:特定の [!DNL Google Ads] コンテンツカテゴリ。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL URL]</i></span>:特定の URL を持つインデックス付きページで、拡張された動的検索広告を表示します。URL 内の任意の場所に値を含めることができます。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Page Title]</i></span>:ページタイトルに特定のテキストを含むインデックス付きページに対して、拡張された動的検索広告を表示する。</p></li><li class="p"><p><span style="font-style: italic;"><i>[!UICONTROL Page Content]</i></span>:特定のコンテンツを含むインデックス付きページに対して、拡張された動的検索広告を表示する。</p></li></ul><p>例：url=shoes.example.com および page title=footwear</p> |
| [!UICONTROL Parent Product Groupings] | 親製品グループの階層。<br><br>例： `All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | <p>製品グループ（「brand=acme」や「All Products」など）。</p><p><b>注意：</b></p><ul><li><p>指定した製品グループが [!UICONTROL Parent Product Groupings] 階層、検索、Social、およびコマースは、必要な階層の任意の部分を作成します。</p></li><li><p>検索、ソーシャル、コマースでは、「[!UICONTROL All Products]」グループとして表示されます。 [!DNL Google Ads] 広告グループのデフォルト入札に設定されたデフォルト入札を持つショッピングキャンペーン。 検索、ソーシャル、コマースでは、「[!UICONTROL Everything Else]「広告グループ階層の各レベルでの広告グループのデフォルト入札額を持つグループ。 これらのデフォルトグループを明示的に作成し、それらを除外したり、入札を変更したりできます。</p></li><li><p>各広告グループは、最大 8 層の製品グループ (「[!UICONTROL All Products]「それから他の七段。</p></li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティションタイプ： <i>小分け</i> （子製品グループがある場合）または <i>単位</i> （子製品グループがない場合）。 |
| [!UICONTROL Match Type] | <p>動的検索のターゲットまたは製品グループの場合：動的検索ターゲットまたは製品グループのキーワード一致オプション： <i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索ターゲットのデフォルト） <i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）または <i>[!UICONTROL Negative Product Group]</i> （製品グループを除外する場合）。</p><p>キーワードの場合：キーワードのキーワード一致オプション： <span style="font-style: italic;"><i>[!UICONTROL Broad]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Phrase]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Exact]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span> （ディスプレイネットワーク上のキーワードまたは配置を除外する場合）ショッピング広告で使用される製品グループは、 <span style="font-style: italic;"><i>[!UICONTROL Product Group]</i></span>. 次を使用する場合、 <span style="font-style: italic;"><i>[!UICONTROL Negative]</i></span>除外する一致タイプも含める必要があります（例：「除外するフレーズ」）。</p><p>新しいキーワードの場合、デフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL Broad]</i></span>. 一致タイプまたはキーワード ID の値は、複数の一致タイプを持つキーワードを編集する場合にのみ必要です。</p><p><b>注意：</b></p><ul><li><p>一致タイプは、キーワードを使用しない拡張動的検索広告には適用できません。</p></li><li><p>の一致タイプの変更 [!DNL Google Ads] キーワードは、既存のキーワードを削除し、新しいキーワードを作成します。</p></li><li><p>ブロード一致修飾子の場合は、「ブロード」を選択し、クローズバリアントが必要なキーワード内の任意の単語の前に+を挿入します（例：「+red +shoes」は、「red」と「shoes」の両方のクローズバリアントを必要とします）。 <b>注意：</b> 一部の言語でのフレーズ一致と同じ一致動作がブロード一致修飾子になり、2021 年 7 月以降、新しいブロード一致修飾子キーワードを作成できなくなりました。 詳しくは、 [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/7042511) を参照してください。</p> |
| [!UICONTROL First Page Bid] | （情報を提供するために生成された一括送信シートに含まれます）検索結果の最初のページに広告を配置するために必要な入札。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Quality Score] | （情報を得るために生成された一括送信シートに含まれます）検索エンジンによってキーワードに割り当てられた現在の品質スコア。 この値は広告ネットワークに投稿されません。) |
| [!UICONTROL Creative Preferred Devices] | ( テキスト広告、動的検索広告の拡張、サイトリンクの拡張。（オプション）広告を表示するデバイスタイプ。 <span style="font-style: italic;"><i>[!UICONTROL All]</i></span> （デフォルト）または <i>[!UICONTROL Mobile]</i>. 条件 <i>[!UICONTROL Mobile]</i> を指定すると、ネットワークはデスクトップユーザーやタブレットユーザーではなく、広告をモバイルデバイスユーザーに表示しようとします。 そうしないと、任意のデバイスタイプで広告が表示されます。</p><p><b>注意：</b></p><ul><li><p>管理者および [!DNL Adobe] アカウントマネージャーユーザーは、この設定を編集できます。</p></li><li><p>ネットワークでは、広告が優先デバイスタイプで表示されるとは限りません。</p></li><li><p>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンでのみ作成できます。また、サイトリンクを含まないキャンペーンでも作成できます。</p></li></ul> |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | （拡張テキスト広告およびレスポンシブ検索広告のみ）広告のヘッドライン ( 各広告が縦のパイプ ( | ) をクリックします。 各広告タイトルフィールドの最大の長さは、任意の動的テキスト（キーワードや広告のカスタマイザの値など）を含む 30 文字または 15 文字の 2 バイト文字です。</p><p>レスポンシブ検索広告の場合、 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] は必須で、その他の広告タイトルフィールドはすべてオプションです。 必須でないフィールドの既存の値を削除するには、 <code>[削除]</code> （括弧を含む）</p><p>レスポンシブ検索広告の場合、次の形式を使用して広告のカスタマイズを挿入します。 `{CUSTOMIZER.AdCustomizerName:DefaultText}`例： `{CUSTOMIZER.Discount:10%}`</p><p>拡張テキスト広告は、作成や編集はできませんが、削除や編集はできます。 [!DNL Google Ads] は 2022 年 6 月に非推奨（廃止予定）となりました。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | <p>（レスポンシブ検索広告のみ）（オプション）対応する広告タイトルを固定する位置： `[null]` （値なし。これにより、広告タイトルはすべての位置の資格を得ることができます）、 <i>1</i>, <i>2</i>または <i>3</i>. 例えば、 [!UICONTROL Ad Title Position] の値が 1 の場合、広告タイトルは位置 1 にのみ表示されます。 デフォルトでは、すべての広告タイトルは null です（値はありません）。</p><p>既存の値を削除するには、 <code>[削除]</code> （括弧を含む）</p><p><b>注意：</b> 複数の広告タイトルを同じ位置にピン留めできます。 広告ネットワークは、位置に固定された広告タイトルの 1 つを使用します。 位置 3 にピン留めされたタイトルは、広告と共に表示されない場合があります。</p> |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | <p>（拡張された動的検索広告、拡張テキスト広告、レスポンシブ検索広告のみ）広告の本文。 各説明フィールドの最大の長さは、任意の動的テキスト（キーワードや広告のカスタマイズ子の値など）を含む 90 文字または 45 文字の 2 バイト文字です。</p><p>レスポンシブ検索広告の場合、次の形式を使用して広告のカスタマイズを挿入します。 `{CUSTOMIZER.AdCustomizerName:DefaultText}`例： `{CUSTOMIZER.Discount:10%}`</p><p>拡張された動的検索広告に対して、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] のみ。 <b>注意：</b> この広告タイプで広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</p><p>拡張テキスト広告は、作成や編集はできませんが、削除や編集はできます。 [!DNL Google Ads] は 2022 年 6 月に非推奨（廃止予定）となりました。</p><p>レスポンシブ検索広告の場合、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] が必要で、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、 <code>[削除]</code> （括弧を含む）</p> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ）（オプション）対応する説明を固定する位置： `[null]` （値なし。すべての職階に対する適格な説明になります）。 <i>1</i>, <i>2</i>または <i>3</i>. 例えば、 [!UICONTROL Description 1 Position] の値が 1 の場合、 [!UICONTROL Description 1] は、位置 1 にのみ表示されます。 デフォルトでは、説明は位置にピン留めされません。</p><p>既存の値を削除するには、 `[delete]` （括弧を含む）</p><p><b>注意：</b> 複数の説明を同じ位置にピン留めできます。 広告ネットワークは、位置に固定された説明の 1 つを使用します。 位置 2 に固定された説明は、広告と共に表示されない場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれる URL。<br><br>拡張された動的検索広告の場合、 [!DNL Google Ads] は web サイトドメインから動的にこの値を生成するので、値を入力する必要はありません。<br><br>レスポンシブ検索広告の場合、値を入力する必要はありません。 表示 URL は、最終的な URL のドメインから自動的に抽出されます。 オプションで、「パス 1」フィールドと「パス 2」フィールドを使用して URL をカスタマイズできます。<br><br>拡張テキスト広告は、作成や編集はできませんが、削除や編集はできます。 [!DNL Google Ads] は 2022 年 6 月に非推奨（廃止予定）となりました。<br><br><b>注意：</b> （最終 URL を持つアカウント）表示 URL と最終 URL のドメイン名が一致する必要があります。</p> |
| [!UICONTROL Display Path 1] | <p>（拡張テキスト広告）<span> レスポンシブ検索広告</span> のみ )</p><p>（オプション）最終的な URL から自動的に抽出される、表示 URL に追加されるテキスト。 URL の前にスラッシュ (/) が付いています。 パスには、スラッシュ (/) や改行 (\n) 文字を含めることはできません。 最大長は 15 文字または 2 バイト文字 7 文字です。</p><p>広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。&lt; `{CUSTOMIZER.AdCustomizerName:Default text}`例： `{CUSTOMIZER.Discount:10%}`</p><p>例えば、 [!UICONTROL Display Path 1] が「契約」の場合、表示 URL は &lt;<i>表示 URL</i>>/deals(www.example.com/dealsなど )。</p><p>拡張テキスト広告は、作成や編集はできませんが、削除や編集はできます。 [!DNL Google Ads] は 2022 年 6 月に非推奨（廃止予定）となりました。</p> |
| [!UICONTROL Display Path 2] | 2 番目の表示パスエントリを見る [!UICONTROL Display Path 1].<br><br>例：If [!UICONTROL Display Path 1] は「契約」で、 [!UICONTROL Display Path 2] が「local」の場合、表示 URL は &lt;<i>表示 URL</i>>/deals/local(www.example.com/deals/localなど )</p><p>拡張テキスト広告は、作成や編集はできませんが、削除や編集はできます。 [!DNL Google Ads] は 2022 年 6 月に非推奨（廃止予定）となりました。</p> |
| [!UICONTROL Promotion Line] | （製品リスト広告のみ）検索結果の製品リストに含めるオプションのプロモーション行。 最大長は 45 文字です。</p><p>プロモーション行は、ページ上で広告が表示される場所に応じて、広告に関連した様々な場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Link Name] | <p>サイトリンクのテキスト。 最大 25 文字まで含めることができます。</p><p>新しいサイトリンクの場合は、サイトリンク行内にキャンペーン名を含める必要があります。 広告グループレベルのサイトリンクの場合は、広告グループ名も含める必要があります。</p><p><b>注意：</b> 35 文字の既存のテキストは、デスクトップおよびタブレットの広告には表示されますが、モバイルデバイスには表示されません。</p> |
| [!UICONTROL Mobile App Platform (Google Adwords)] | （既存のアプリインストール広告のみ）モバイルアプリケーションが実行されるオペレーティングシステム： <i>Android™</i> または <i>ios</i>. |
| [!UICONTROL Mobile App ID (Google Adwords)] | （既存のアプリインストール広告のみ） <p>アプリケーション ID またはパッケージ名。 |
| [!UICONTROL Mobile App Name (Google Adwords)] | （既存のアプリインストール広告のみ）アプリケーションの名前。 |
| [!UICONTROL Start Date] | <p>（拡張サイトリンクのみ）広告主のタイムゾーンと次のいずれかの形式で、サイトリンクに入札を配置できる最初の日付。 <span style="font-style: italic;"><i>m/d/yyyy</i></span>, <span style="font-style: italic;"><i>m/d/yy</i></span>, <span style="font-style: italic;"><i>m-d-yyyy</i></span>または <span style="font-style: italic;"><i>m-d-yy</i></span>. 新しい拡張サイトリンクのデフォルトは現在の日です。</p><p><b>注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンでのみ作成できます。また、サイトリンクを含まないキャンペーンでも作成できます。</p> |
| [!UICONTROL End Date] | <p>（拡張サイトリンクのみ）広告主のタイムゾーンと次のいずれかの形式で、サイトリンクに入札を配置できる最後の日付。  <span style="font-style: italic;"><i>m/d/yyyy</i></span>, <span style="font-style: italic;"><i>m/d/yy</i></span>, <span style="font-style: italic;"><i>m-d-yyyy</i></span>または <span style="font-style: italic;"><i>m-d-yy</i></span>. デフォルトは「なし」（終了日なし）です。</p><p><b>注意：</b> 新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーンでのみ作成できます。また、サイトリンクを含まないキャンペーンでも作成できます。</p> |
| [!UICONTROL Exclude Tablet (Google Adwords)] | （既存のアプリインストール広告のみ）</p><p>（オプション）を防ぎます。 [!DNL Google Ads] 広告の表示からタブレットユーザーへ。 値には、 <i>はい</i> および <i>いいえ</i>. |
| [!UICONTROL Landing Page Suffix] | 情報を追跡するために、最終 URL の末尾に追加するパラメーター。 例： `param2=value1&param3=value2`<br><br>参照：[のクリック追跡形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md).&quot;<br><br>下位レベルでの最終的な URL サフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、 [!DNL Google Ads] 編集者。 |
| [!UICONTROL Tracking Template] | トラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL を [!DNL ValueTrack] パラメーター。 最も詳細なレベル（最も詳細なキーワードを含む）のトラッキングテンプレートは、より高いレベルのすべての値を上書きします。<br><br>Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「検索、ソーシャル、コマースは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードを自動的に追加します。<br><br>サードパーティのリダイレクトとトラッキングの場合は、値を入力します。 のリスト [!DNL ValueTrack] トラッキングテンプレートの最終 URL を示すパラメーターについては、「使用可能」の節の「トラッキングテンプレートのみ」パラメーターを参照してください。 [!DNL ValueTrack] パラメーター」( [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/2375447).<br><br>既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Base URL/Final URL] | 広告のクリック時に検索エンジンユーザーが使用するランディングページの URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 キーワードレベルのベース URL と最終 URL は、広告レベル以上の URL よりも優先されます。<br><br>既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Destination URL] | ( 情報を提供するために、生成された一括送信シートに含まれます。検索エンジンに投稿されない ) リンク先 URL のアカウントの場合、広告を広告主の Web サイト上のベース URL/ランディングページにリンクする URL です（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを経由する場合もあります）。 検索、ソーシャル、コマースのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URL を生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づいています。 検索エンジン固有のパラメーターを追加した場合は、Search、Social、および Commerce の同等のパラメーターに置き換えることができます。<br><br>最終 URL を持つアカウントの場合、この列には、ベース URL/最終 URL 列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | に代わるデータ `{custom_code}` 動的変数を設定できます。 トラッキング URL にカスタム値を挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式は次のとおりです。 <i>[!UICONTROL Text ad]</i>, <i>[!UICONTROL Expanded text ad]</i>, <i>[!UICONTROL Dynamic search ad]</i> （非推奨の広告タイプ）、 <i>[!UICONTROL Expanded Dynamic Search ad]</i>, &lt;[!UICONTROL i>Display ad]</i>, <i>[!UICONTROL App Install ad]</i> （非推奨）、 <i>[!UICONTROL Image]</i>, <i>[!UICONTROL Product ad<]/i> （買い物広告）または <i>[!UICONTROL Responsive search ad]</i>. 新しい広告のデフォルトは、 <i>[!UICONTROL Text ad]</i>.<br><br>製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Param1] | <p>の数値 `{param1}` 広告パラメーター。bulksheet ファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます。 最大長は 25 文字で、以下の nun-numeric 文字を含めることができます。</p><ul><li><p>値の前後に通貨記号やコードを付けることができます。 例： `£2.000,00` および `2000GBP` は有効です。</p></li><li><p>値にはコンマ (`,`) またはピリオド (`.`) を区切り文字として使用し、オプションのピリオド (`.`) またはコンマ (`,`) を使用します。 例： `1,000.00` および `2.000,10` は有効です。</p></li><li><p>値の前にはパーセント記号 (`%`)，プラス記号 (`+`) またはマイナス記号 (`- `) をクリックします。 例： `20%`, `208+`、および `-42.32` は有効です。</p></li><li><p>2 つの数字をフォワードスラッシュで埋め込むことができます。 例： `4/1` および `0.95/0.45` は有効です。</p></li></ul><p>既存の値を削除するには、 `[delete]` （括弧を含む）</p> |
| [!UICONTROL Param2] | の数値 `{param2}` 広告パラメーター。bulksheet ファイル内の任意の広告の広告コピーまたは表示 URL に含めることができます。 詳しくは、 Param1 のエントリを参照してください。 |
| [!UICONTROL Audience] | 検索広告 (RLSA) のリマーケティングリストは、キャンペーンまたは広告グループのターゲットオーディエンスまたは除外オーディエンスをターゲットにします。 「ターゲットタイプ」フィールドにターゲットか除外かを指定します。 |
| [!UICONTROL Target Type] | （オーディエンスが指定されている場合）指定されたオーディエンスが <i>含める</i> （ターゲット）または <i>除外</i>. |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i> （編集不可）または <i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新しいキャンペーンのデフォルトはです。 <i>[!UICONTROL Active]</i>. アクティブまたは一時停止したキャンペーンを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新しい広告グループのデフォルトはです。 [!UICONTROL Active]. アクティブな広告または一時停止した広告グループを削除するには、値を入力します `Deleted`. |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトはです。 [!UICONTROL Active]. アクティブまたは一時停止したキーワードを削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Status] | 広告の表示ステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Deleted]</i> （既存の広告のみ）、 <i>[!UICONTROL Disapproved]</i> （編集不可）または <i>[!UICONTROL Paused]</i>. 新しい広告のデフォルトは、 [!UICONTROL Active]. アクティブな広告または一時停止した広告を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Placement Status] | Web サイト配置のステータス： <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Paused]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> （既存の広告のみ）。 新しい Web サイトのデフォルトはです。 <span style="font-style: italic;"><i>アクティブ。</i></span> アクティブなプレースメントまたは一時停止したプレースメントを削除するには、値を入力します <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス： <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>, <span style="font-style: italic;"><i>[!UICONTROL Paused]</i></span>または <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> （既存のターゲットのみ）。 新しいターゲットのデフォルトはです。 <span style="font-style: italic;"><i>アクティブ。</i></span> アクティブなターゲットまたは一時停止したターゲットを削除するには、値を入力します <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス： <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span> <span>または</span> <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span> （既存の製品グループのみ）。 新しい製品グループのデフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. アクティブな製品グループを削除するには、値を入力します <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス： <span style="font-style: italic;"><i>アクティブまたは削除済み</i></span> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトはです。 <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. アクティブなサイトリンクを削除するには、値を入力します。 <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Location Status] | ロケーションターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトはです。 [!UICONTROL Active]. アクティブな場所を削除するには、値を入力します <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL RLSA Target Status] | キャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外のステータス。 <span style="font-style: italic;"><i>[!UICONTROL Active]</i> または [!UICONTROL Deleted]</i></span> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは、 <span style="font-style: italic;"><i>[!UICONTROL Active]</i></span>. アクティブなターゲットまたは除外を削除するには、値を入力します <span style="font-style: italic;"><i>[!UICONTROL Deleted]</i></span>. |
| [!UICONTROL Device Target Status] | <p>キャンペーンまたは広告グループレベルのデバイスターゲットのステータス： <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Deleted]</i>. 新しいキャンペーンおよび広告グループの場合、デフォルトはです。 <i>[!UICONTROL Active]</i>.</p> |
| \[ 広告主固有のラベル分類\] | （広告主固有のラベル分類用に名前付けされます。例えば、Color というラベル分類用の「色」）エンティティに関連付けられている、指定した分類の値です。 エンティティごとに 1 つの分類のみを含めることができます（キャンペーン A の「色」ラベル分類の「赤」など）。 最大長は 100 文字で、値には ASCII 文字と非 ASCII 文字を含めることができます。<br><br>ラベルの分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も精度の高い）レベルに適用されます。<br><br>分類名も分類値も、大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられる制約。 エンティティごとに 1 つの制約のみを割り当てることができます。<br><b>> 制約は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に「[!UICONTROL AMO ID]」と呼ばれます。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に「[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] キーワードを変更した場合にのみ必須です（行に a が含まれている場合を除く）キーワードを識別するのに十分なプロパティ列、または b)a &quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには、広告 ID または AMO ID が必要です。 その他すべてのエンティティタイプの場合、広告 ID は、行に a) 広告を識別するのに十分な広告プロパティ列、または b) または b)[!UICONTROL AMO ID]&quot;.&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。</p><p><b>注意：</b> a) 広告プロパティの列（既存の広告のステータスを除く）または b) レスポンシブ検索広告のデータを編集する場合、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]をクリックした場合、新しい広告が作成され、既存の広告は変更されません。</p> |
| [!UICONTROL Placement ID] | Web サイトの配置を識別する一意の ID。 配置を変更または削除する場合にのみ必須です（行に a を含む場合を除く）配置を識別するのに十分なプロパティ列、または b)「[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意の ID。 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Product Group ID] | 既存の製品グループを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] 行に a が含まれている場合を除き、製品グループを変更または削除する場合にのみ必須です。a) 製品グループを識別するのに十分なプロパティ列、または b) および&quot;[!UICONTROL AMO ID]&quot;.&quot; |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] サイトリンクを識別するのに十分なプロパティ列（a を含む場合を除く）または b) および&quot;[!UICONTROL AMO ID]&quot;.&quot; ただし、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]、およびプロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。</p><p><b>注意：</b> 既存のサイトリンクの「ステータス」以外のサイトリンクプロパティ列を編集し、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]をクリックした場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルの RLSA ターゲットまたは除外を識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] ターゲットまたは除外を変更または削除する場合にのみ必須です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Device Target ID] | <p>既存のキャンペーンレベルまたは広告グループレベルのデバイスターゲットまたは除外を識別する一意の ID。 CSV ファイルおよび TSV ファイルでは、前に一重引用符 (&#39;) を付ける必要があります。[^1] ターゲットを変更または削除する場合にのみ必要です ( 行に「[!UICONTROL AMO ID]」と入力します。</p> |
| [!UICONTROL AMO ID] | （生成された一括送信シート内）同期されたAdobeに対してエンティティが生成した一意の識別子。 レスポンシブ検索広告の場合、広告 ID を含めない限り、広告を編集または削除するには AMO ID が必要です。 AMO ID を持つ他のすべてのエンティティタイプのデータを編集するには、エンティティ ID と親エンティティ ID を含めない限り、AMO ID はデータの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |
| [!UICONTROL EF Error Message] | （情報を提供するために、生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL EF Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報を提供するために、生成された一括送信シートに含まれます）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは、 [!UICONTROL SE Errors] ファイル。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報を提供するために生成された一括送信シートに含まれます）任意の [!DNL Google Ads] 広告が違反する広告ポリシー。 |
| [!UICONTROL Retail Hash] | (Advanced Campaign Managementを使用して生成されたバルクシートの情報用に含まれます )Advanced (ACM) ビューを使用してアイテムが生成されたことを示す英数字のハッシュコード (f9639f40cdf56524b541e5dacf55a991 など )。 |

<table style="table-layout:auto">

[^1]: [!DNL Excel] は、ファイルを開くときに大きな数を科学的表記 (2115585666の 2.12E+09 など ) に変換します。 標準の表記で数字を表示するには、列内の任意のセルを選択し、数式バーの内側をクリックします。

## 各アカウントコンポーネントの作成、編集または削除に必要なフィールド {#bulksheet-fields-per-component-google}

以下のセクションでは、特定のアカウントエンティティに関連するフィールドについて説明します。

各データフィールドの説明については、[すべての使用可能なデータフィールド](#bulksheet-fields-all-google).&quot;

>[!NOTE]
>
>1 つのフィールドをアクションに適用できない場合、そのフィールドに入力された値は無視されます。

### Campaign フィールド

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 | アカウントのキャンペーンを識別する一意の名前。 |
| [!UICONTROL Campaign Budget] | キャンペーンを作成するために必要です。 | キャンペーンに対する 1 日の支出制限。通貨記号や句読点の有無は問いません。 この値は上書きされますが、アカウント予算を超えることはできません。 |
| [!UICONTROL Delivery Method] | キャンペーンを作成するために必要です。 |
| [!UICONTROL Channel Type] | キャンペーンを作成するために必要です。 |
| [!UICONTROL Networks] | キャンペーンを作成するために必要です。 |
| [!UICONTROL DSA Domain Name] | 動的な検索広告を含む検索ネットワーク上でキャンペーンを作成するために必要です。 |
| [!UICONTROL DSA Domain Language] | 動的な検索広告を含む検索ネットワーク上でキャンペーンを作成するために必要です。 |
| [!UICONTROL Campaign Priority] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Merchant ID] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Sales Country] | 買い物キャンペーンを作成するために必要です。 |
| [!UICONTROL Product Scope Filter] | （買い物キャンペーン）オプション |
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
| [!UICONTROL Campaign ID] | 行に「[!UICONTROL AMO ID]」と呼ばれます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 広告グループフィールド

| フィールド | 必須？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
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
| [!UICONTROL Ad Group ID] | 行に「[!UICONTROL AMO ID]」と表示されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キーワードフィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
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
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | キーワードを編集または削除する場合にのみ必須です（ただし、行に a が含まれている場合を除く）。キーワードを識別するのに十分なプロパティ列、または b)a &quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 配置フィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max Placement CPC (Google Adwords)] | オプション |
| [!UICONTROL Max Placement CPM (Google Adwords)] | オプション |
| [!UICONTROL Placement] | 必須 |
| [!UICONTROL Match Type] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Placement Status] | 配置を削除する場合にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Placement ID] | 配置を編集または削除する場合にのみ必要です（行に a を含む場合を除く）配置を識別するのに十分なプロパティ列、または b)「[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 拡張された動的検索広告

この広告タイプは、現在、では「動的検索広告」と呼ばれています。 [!DNL Google Ads]. 動的検索広告の作成について詳しくは、[実装方法 [!DNL Google Ads] 動的検索広告](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-dynamic-search-ads.html).&quot;

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 広告の作成や説明の編集に必要です。 <b>注意：</b> この広告タイプで広告のコピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 製品リスト/ショッピング広告フィールド

ショッピング広告の作成について詳しくは、[実装方法 [!DNL Google Ads] ショッピングキャンペーン](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-campaign-types/google-shopping-campaigns.html).&quot;

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
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
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### レスポンシブ検索広告フィールド

この広告タイプでは、[!UICONTROL Responsive Search Ad]」行を [!UICONTROL Download Bulksheet] ダイアログ。

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 | |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-15 | レスポンシブ検索広告の場合、 [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]、および [!UICONTROL Ad Title 3] 広告を作成するにはが必要です。その他の広告タイトルフィールドはすべてオプションです。 必須でないフィールドの既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、 [!UICONTROL Description Line 1] および [!UICONTROL Description Line 2] 広告を作成するにはが必要で、 [!UICONTROL Description Line 3] および [!UICONTROL Description Line 4] はオプションです。 既存の値を削除するには、 `[delete]` （括弧を含む） |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告を作成するために必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Ad Status] | 広告を削除するために必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | 広告 ID を含めない限り、広告の編集または削除に必要です。 |

### テキスト広告フィールド

この広告タイプでは、[!UICONTROL Creative (except RSA)]」行を [!UICONTROL Download Bulksheet] ダイアログ。

>[!NOTE]
>
>拡張テキスト広告は、2022 年 6 月に非推奨（廃止予定）となりました。 既存のテキスト広告のみを削除できます。

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Creative Preferred Devices] | 読み取り専用 |
| [!UICONTROL Ad Title]，広告タイトル 2-3 | 読み取り専用 |
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
| [!UICONTROL Ad ID] | 行に広告を識別するのに十分な広告プロパティ列が含まれている場合を除き、広告のステータスを変更した場合にのみ必須です。b) または b)[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Ad ID] nor [!UICONTROL AMO ID]を検索し、広告プロパティの列が複数の広告に一致する場合、1 つの広告のステータスのみが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 動的検索ターゲット（自動ターゲット）フィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Auto Target Expression] | キャンペーンの設定が「[!UICONTROL Use my website contents to target my ads]」が有効になっていません。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Target Status] | ターゲットの削除に必要 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 買い物製品グループのフィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Max CPC] | 製品グループを作成するために必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループを作成するために必要です。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Product Group Status] | 製品グループの削除にのみ必要です。 |
| \[ 広告主固有のラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 行に a が含まれている場合を除き、製品グループを変更または削除する場合にのみ必須です。a) 製品グループを識別するのに十分なプロパティ列、または b) および&quot;[!UICONTROL AMO ID].&quot; |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのサイトリンクフィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのサイトリンクの場合は必須です。 キャンペーンレベルのサイトリンクには適用されません。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Link Name] | 必須 |
| [!UICONTROL Start Date] | オプション |
| [!UICONTROL End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Sitelink Status] | サイトリンクを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Sitelink ID] | サイトリンクを識別するのに十分なプロパティ列（a を含む場合を除く）または b) および&quot;[!UICONTROL AMO ID].&quot; ただし、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]  およびプロパティ列が複数のサイトリンクに一致する場合、1 つのサイトリンクのステータスのみが変更されます。<br><br><b>注意：</b> サイトリンクプロパティの列を編集する場合、次の項目を除く [!UICONTROL Status] 既存のサイトリンクの場合、 [!UICONTROL Sitelink ID] nor [!UICONTROL AMO ID]をクリックした場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ ID と親エンティティ ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### 場所のターゲットフィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | ロケーションターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | を含めない限り、データを編集または削除するために必要 [!UICONTROL Campaign ID].<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスターゲットフィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを作成または編集するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必須です。 キャンペーンレベルのデバイスターゲットには適用されません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション広告グループレベルのデバイスターゲットにのみ適用できます。 |
| [!UICONTROL Device Target ID] | ターゲットを変更または削除する場合にのみ必要です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | デバイスターゲット ID を含めない限り、データの編集または削除に必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

### キャンペーンレベルおよび広告グループレベルの RLSA ターゲット/除外フィールド

| フィールド | 必須？ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Acct Name] | 各行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットと除外に必須です。 キャンペーンレベルのターゲットおよび除外には適用されません。 |
| [!UICONTROL Audience] | 新しいターゲットまたは除外を作成するために必要です。 |
| [!UICONTROL Target Type] | 新しいターゲットまたは除外を作成するために必要です。 |
| [!UICONTROL RLSA Target Status] | ターゲットまたは除外を削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション広告グループレベルのターゲットおよび除外にのみ適用できます。 |
| [!UICONTROL RLSA Target ID] | ターゲットを変更または削除する場合にのみ必要です ( 行に「[!UICONTROL AMO ID]」と入力します。 |
| [!UICONTROL AMO ID] | RLSA ターゲット ID を含めない限り、データを編集または削除するために必要です。<br><br>検索、ソーシャル、コマースは、値を使用して、編集する正しい ID を判断しますが、広告ネットワークには ID が投稿されません。 |

>[!MORELIKETHIS]
>
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートで実行できる操作](bulksheet-operations.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [バルクシートファイルのダウンロード/作成](../bulksheet-download.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](../bulksheet-upload.md)
