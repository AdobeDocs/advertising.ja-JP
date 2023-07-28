---
title: 基本レポートと高度なレポートのレポート列
description: 基本レポートと高度なレポートで使用できるデータ列について説明します。
exl-id: 20ce9519-4a13-4175-bf7c-26f1dc4c9bd1
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: 7ffdd97387815098994f85c4368e60b2b44838dd
workflow-type: tm+mt
source-wordcount: '3603'
ht-degree: 0%

---

# 基本レポートと高度なレポートのレポート列

| 列 | 説明 |
| ---- | ---- |
| \[ 広告主固有のカスタム（派生）指標\] | の値 [作成したカスタム指標](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) これは既存の指標から計算されます。 |
| \[ 広告主固有のラベルの分類\] | エンティティに現在適用されている、エンティティレベルのラベル分類。 複数のラベル分類はコンマ (,) で区切ります。 |
| \[ 広告主固有のトランザクションプロパティ\] | 指定したトランザクションプロパティまたはサイトエンゲージメント指標に対するコンバージョンの数。 |
| \[Google-tracked conversions/transaction properties\] | 「GGL\*、GGL_CT\*および GGL_XD_CT\*」のエントリを参照してください。 |
| [!UICONTROL 7-Day Click Accuracy] | ([!UICONTROL Portfolio Report]) 過去 7 日間の予測クリック数の平均精度（現在の日付を含まず、レポートの指定した日付範囲を含まない）をパーセンテージで表したもの。 |
| [!UICONTROL 7-Day Cost Accuracy] | ([!UICONTROL Portfolio Report]) 過去 7 日間のコスト予測の平均精度 ( 現在の日付を含まない（レポートの指定した日付範囲を含まない）。パーセンテージで表されます。 |
| [!UICONTROL 7-Day Revenue Accuracy] | ([!UICONTROL Portfolio Report]) 過去 7 日間の売上高予測の平均精度 ( 現在の日付を含まない（レポートの指定した日付範囲を含まない）。パーセンテージで表されます。 |
| [!UICONTROL Account] | アカウント名。 |
| [!UICONTROL Account Status] | 検索、ソーシャル、コマース内のアカウントのステータス： <ul><li><i>[!UICONTROL Enabled]:</i> （デフォルト）同期された広告ネットワークの場合、Search、Social、&amp; Commerce は、広告ネットワークアカウントにログインしてキャンペーンデータを取得でき、最適化やトラッキング生成などのその他の適用可能な機能が有効になっています。<br><br>非同期広告ネットワークの場合は、最適化やトラッキング生成などの適用可能な機能を使用できます。</li><li><i>[!UICONTROL Disabled]:</i> 同期された広告ネットワークの場合、Search、Social、&amp; Commerce は広告ネットワークアカウントにログインしないので、キャンペーンデータを取得しません。また、最適化やトラッキング生成など、適用可能な機能は無効になります。 アカウントが有効な間に収集されたデータは保存されますが、今後作成するすべてのキャンペーン管理ビューとすべてのレポートには、アカウントが無効になる期間のデータは含まれません。<br><br>非同期広告ネットワークの場合、最適化やトラッキング生成などの適用可能な機能は使用できません。</li></ul> |
| [!UICONTROL Active Ad Groups] | アクティブな広告グループの数。 |
| [!UICONTROL Active Ads/Creatives] | アクティブな広告/クリエイティブの数。 |
| [!UICONTROL Active Campaigns] | アクティブなキャンペーンの数。 |
| [!UICONTROL Active Keywords] | アクティブなキーワードの数。 |
| [!UICONTROL Ad Group] | 広告グループ。 |
| [!UICONTROL Ad Group ID] | Search、Social および Commerce が広告グループに割り当てる数値 ID。 |
| [!UICONTROL Ad Group Status] | 広告グループのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Type] | 広告グループのタイプ（例： ） <i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ） <i>[!UICONTROL Discovery]</i> （検出キャンペーンのみ） <i>[!UICONTROL Display]</i> （ディスプレイキャンペーンのみ） <i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、 <i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ） <i>[!UICONTROL Shopping Showcase]</i>, <i>[!UICONTROL Shopping Product]</i> （標準の買い物キャンペーンのみ）または <i>[!UICONTROL Shopping Smart]</i> （スマートショッピングキャンペーン用）。 キャンペーンタイプによっては、1 つのキャンペーンに複数の広告タイプを含めることができます。 |
| [!UICONTROL Ad Groups] | ラベル値が割り当てられる広告グループの数。 |
| [!UICONTROL AD Name] | 広告グループ名。 [!UICONTROL Ad Group]. |
| [!UICONTROL Ad Size] | 広告のディメンション。 |
| [!UICONTROL AD Strength] | ([!DNL Google Ads] レスポンシブ検索広告 ) 広告の効果： <i>[!UICONTROL average]</i>, <i>[!UICONTROL excellent]</i>, <i>[!UICONTROL good]</i>, <i>[!UICONTROL no_ads]</i>, <i>[!UICONTROL pending]</i>, <i>[!UICONTROL poor]</i>, <i>[!UICONTROL unknown]</i>または <i>[!UICONTROL unspecified]</i>. |
| [!UICONTROL Adgroup MBA] | ([!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン ) 現在の広告グループレベルのモバイル入札の調整。広告がモバイルデバイスに表示されたときの入札の調整方法を決定します。 |
| [!UICONTROL Advertiser] | 広告主の名前。 |
| [!UICONTROL Advertiser ID] | 広告主の検索、ソーシャル、コマースアカウントの数値 ID。 |
| [!UICONTROL Avg Position] | 指定した日付範囲における広告の平均順位。<br><br>の場合 [!DNL Google Ads] および [!DNL Yahoo! Japan Ads] キャンペーンの場合、このデータは 2019 年 9 月までのみ利用できます。 の場合 [!DNL Microsoft Advertising]の場合、このデータは 2021 年 1 月 22 日までのみ利用できます。 |
| [!UICONTROL Base URL] | キーワードのベース URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 検索、ソーシャル、コマースのリダイレクトおよびトラッキングコードは含まれません。 |
| [!UICONTROL Bid Strategy] | （ほとんどの広告ネットワーク）キャンペーンまたはキャンペーンコンポーネントの場合、これはキャンペーンの入札戦略です。 マネージャーアカウントにリンクされている広告ネットワークアカウントの場合、これはアカウント間の入札戦略です。 使用可能な値は、広告ネットワークによって異なります。 |
| [!UICONTROL Business Name] | ([!DNL Microsoft Advertising] レスポンシブ広告 ) ビジネス名。 |
| [!UICONTROL Call to Action] | ([!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告 ) 広告に含まれるコールトゥアクション。 |
| [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Campaign Budget] | キャンペーンの予算。 |
| [!UICONTROL Campaign MBA] | ([!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン ) 現在のキャンペーンレベルのモバイル入札の調整。広告がモバイルデバイスに表示されたときの入札の調整方法を決定します。 |
| [!UICONTROL Campaign Start Date] | キャンペーンの入札が行われた最初の日。 |
| [!UICONTROL Campaign Status] | キャンペーンステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i>または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Campaign Type] | キャンペーンのタイプ（例： ） <i>[!UICONTROL Audience (Image)]</i>, <i>[!UICONTROL Audience (Feed)]</i>, <i>[!UICONTROL Discovery]</i>, <i>[!UICONTROL Search and Display]</i>, <i>[!UICONTROL Standard Display]</i>, <i>[!UICONTROL Standard Performance Max]</i>, <i>[!UICONTROL Standard Search]</i>, <i>[!UICONTROL Standard Shopping]</i>, <i>[!UICONTROL Video]</i>または <i>[!UICONTROL Others]</i>. |
| [!UICONTROL Channel Type] | マーケティングチャネルのタイプ： <i>[!UICONTROL Search]</i> または <i>[!UICONTROL Content]</i>. この列は、レポートの [!UICONTROL Search/Content] レポート設定では、「[!UICONTROL Combined].&quot; |
| [!UICONTROL City] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Transaction Report]) クリックの発生元となった市区町村。 ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL Click Match Type] | クリックされた広告のキーワード一致タイプ。 これは、 [!UICONTROL Listing Match Type] ただし [!DNL Microsoft Advertising] 複数の一致タイプを持つキーワード。 の場合 [!DNL Microsoft Advertising] キーワード。実際にクリックされた一致タイプです。 |
| [!UICONTROL Click Value] | ([!UICONTROL Portfolio Report]) ポートフォリオの目的に指定したクリック値。 |
| [!UICONTROL Click/Impression Time] | ([!UICONTROL Transaction Report]) コンバージョンが発生したクリックまたはインプレッションの時間。 |
| [!UICONTROL Clicks] | 指定した日付範囲での広告のクリック数。 |
| [!UICONTROL Client ID1], [!UICONTROL Client Id 1] | ([!UICONTROL Keyword Report], [!UICONTROL Ad Variation Report]、および [!UICONTROL Transaction Report]；フィードベースのトラッキング実装 ) フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Id 2] | ([!UICONTROL Keyword Report] および [!UICONTROL Transaction Report]；フィードベースのトラッキング実装 ) フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Transaction ID] | ([!UICONTROL Transaction Report]) 一意のトランザクション ID。 |
| [!UICONTROL Constraint End Date] | ([!UICONTROL Constraint Report]) 制約がアクティブになった最終日。 |
| [!UICONTROL Constraint Name] | ([!UICONTROL Constraint Report]) 制約名。 |
| [!UICONTROL Constraint Start Date] | ([!UICONTROL Constraint Report]) 制約が有効な最初の日。 |
| [!UICONTROL Constraint Status] | ([!UICONTROL Constraint Report]) 制約のステータス：  <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Paused]</i>. |
| [!UICONTROL Constraint Type] | ([!UICONTROL Constraint Report]) 制約のタイプ。  <i>[!UICONTROL Bid/Pos Constraint]</i>, <i>[!UICONTROL Bid Shift]</i>, <i>[!UICONTROL Campaign Budget]</i>, <i>[!UICONTROL Context Sensitive Bid]</i>, <i>[!UICONTROL Incremental Bidding]</i>, <i>[!UICONTROL Max CPA]</i>, <i>[!UICONTROL Min Margin]</i>, <i>[!UICONTROL Variable Bid Position]</i>, <i>[!UICONTROL Search Engine Min Bid]</i>または <i>[!UICONTROL Variable Position]</i>. |
| [!UICONTROL Constraints] | エンティティに適用できる制約の名前（コンマ区切り）。 |
| [!UICONTROL Content IS] | ディスプレイ/オーディエンスネットワーク上の広告に対して受け取ったインプレッション数を、受け取る資格のあった推定インプレッション数で割った値です。 In [!DNL Microsoft Advertising]を呼び出します。これは、[!UICONTROL Audience IS].&quot; |
| [!UICONTROL Content IS Lost (budget)] | 1 日あたりの予算または月別の予算が少なすぎるので、ディスプレイ/オーディエンスネットワーク上の広告が受け取らなかったインプレッションの推定割合。 In [!DNL Microsoft Advertising]を呼び出します。これは、[!UICONTROL Audience lost IS (budget)].&quot; |
| [!UICONTROL Content IS Lost (rank)] | 広告のランクが低いので、ディスプレイ/オーディエンスネットワークに広告が表示されなかったインプレッションの推定割合。 In [!DNL Microsoft Advertising]を呼び出します。これは、[!UICONTROL Audience lost IS (rank)].&quot; |
| [!UICONTROL Conversion Type] | ([!UICONTROL Transaction Report]) コンバージョンの前に実行されたアクション：<ul><li><i>[!UICONTROL Click:]</i> コンバージョンの前に 1 回以上のペイドクリックが発生した。</li><li><i>[!UICONTROL Impression:]</i> コンバージョン前に有料クリックが発生しなかったので、コンバージョンはビュースルー（有料クリックなしのインプレッション）から発生していました。</li></ul> |
| [!UICONTROL Cost] | 指定した日付範囲での広告の合計コストです。 |
| [!UICONTROL Country] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) クリックの発生元となった国。 ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL CPC] | 指定した日付範囲の広告のクリック単価 (CPC)。 |
| [!UICONTROL Creative Base URL] | 広告のベース URL。キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 検索、ソーシャル、コマースのリダイレクトおよびトラッキングコードは含まれません。 |
| [!UICONTROL Creative Destination URL] | 広告の最終的な URL またはリンク先 URL （任意のトラッキングパラメーターを含む）。 |
| [!UICONTROL Creative Name] | ([!DNL Yahoo! Japan] のみ ) 広告画像名。 |
| [!UICONTROL Creative Title], [!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 広告のタイトルまたはヘッドライン。 クリエイティブタイプごとに、必須行とオプションのタイトル行の数が異なります。 参照： [!UICONTROL Creative Title4] およびより高い列 [!DNL Microsoft Advertising] レスポンシブ広告またはマルチメディア広告には、「[!UICONTROL Creative Titles]」列に表示されます。 |
| [!UICONTROL Creative Titles] | （マルチメディアおよびレスポンシブ検索広告のみ）広告の短いヘッドライン ([!UICONTROL Creative Title]&quot;から&quot;[!UICONTROL Creative Title15]」) をクリックします。 この列を含める場合、他の [!UICONTROL Creative Title] 列のみ、編集する [!UICONTROL Order Results/Limit Rows By] 並べ替えに使用するセクション [!UICONTROL Creative Titles] の代わりに [!UICONTROL Creative Title]. |
| [!UICONTROL Creative Type] | 広告の形式。 次の値を指定できます。 <i>[!UICONTROL App Install Ad]</i>, <i>[!UICONTROL Call Only Ad]</i>, <i>[!UICONTROL Discovery Ad (single-image ads)]</i>, <i>[!UICONTROL Discovery Carousel Ad]</i> （マルチ画像カルーセル広告）、 <i>[!UICONTROL Display Ad]</i>, <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Legacy Text Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i>, <i>[!UICONTROL Responsive Ad]</i>, <i>[!UICONTROL Responsive Search Ad]</i>または <i>[!UICONTROL Text Ad]</i>. |
| [!UICONTROL CTR] | クリックスルー率。クリック数を、含まれる広告のインプレッション数で割った値です。 |
| [!UICONTROL Currency] | 該当する通貨のタイプ（「USD」や「GBP」など）。<br><br><b>注意：</b> 異なる通貨のアカウントのデータがレポートに含まれる場合は、[!UICONTROL Total]「通貨の値は、通貨に関係なく、列内のすべての数値の合計に過ぎません。 |
| [!UICONTROL Current Bid] | ターゲットの現在の入札額。 |
| [!UICONTROL Current First Page Bid] | ([!DNL Google Ads] キャンペーンのみ ) 現在、広告を検索結果の最初のページに配置するために必要な推定クリック単価 (CPC) 入札。 [!DNL Google] 検索クエリがキーワードと一致する。<br><br>単一のキーワードと一致タイプの組み合わせの場合、この値は、その組み合わせで現在必要な最初のページ入札です。 同じキーワードと一致タイプの組み合わせが複数のキャンペーンで使用される場合、この値は、現在すべてのインスタンスで必要とされる最初のページ入札の最小値になります。 |
| [!UICONTROL Current Quality Score] | ([!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ ) 広告ネットワークで指定された、キーワードまたは入札単位の現在の品質スコア。 1（低）～ 10（完全）の範囲です。 単一のキーワードと一致タイプの組み合わせの場合、この値はその組み合わせの現在のスコアです。 同じキーワードと一致タイプの組み合わせが複数のキャンペーンで使用される場合、この値はすべてのインスタンスでの最大現在のスコアになります。<br><br>広告ネットワークは、品質スコアを使用して入札価格と広告の位置を決定します。 キーワードは、関連する広告に対するキーワードの関連性、ユーザーの検索クエリ、ランディングページの質など、様々な要因に従って計算されます。 のキーワードの場合 [!DNL Google Ads]の場合、キーワードのクリックスルー率も考慮され、 [!DNL Microsoft Advertising]の場合、ランディングページで提供されるユーザーエクスペリエンスも考慮されます。 |
| [!UICONTROL Custom Bid Level] | ( ディスプレイネットワークをターゲットにするGoogleキャンペーンのみ ) 入札のレベル： <i>[!UICONTROL Ad Group]</i>, <i>[!UICONTROL Age]</i>, <i>[!UICONTROL Gender]</i>, <i>[!UICONTROL Interest and List]</i>, <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i>, <i>[!UICONTROL Vertical]</i>, <i>[!UICONTROL None]</i>または <i>[!UICONTROL Unknown]</i>. |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 広告の本文。 クリエイティブタイプが異なれば、必須とオプションの説明行の数も異なります。 参照： [!UICONTROL Description3] および [!UICONTROL Description4] 列 [!DNL Microsoft Advertising] レスポンシブ広告またはマルチメディア広告には、「[!UICONTROL Descriptions]」列に表示されます。 |
| [!UICONTROL Descriptions] | ([!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告 ) 広告の説明行ごとに列を追加します (&quot;[!UICONTROL Description1]&quot;から&quot;[!UICONTROL Description4]」) をクリックします。 この列を含める場合、他の [!UICONTROL Description] 列。 |
| [!UICONTROL Device] | ([!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads]、および [!DNL Yahoo Native] キャンペーン ) 広告が表示されたデバイスタイプ。 <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>または <i>[!UICONTROL N/A]</i> （値なし）。 その他の広告ネットワークの行には、値 N/A が含まれます。<br><br>検索キャンペーンで、キーワード、広告、広告拡張のトラッキングテンプレートまたはリンク先 URL に、デバイス別にデータを追跡するためのパラメーターが含まれている場合 (`&ev_dvc={device}&ev_dvm={devicemodel}`) をクリックした時点で、コンバージョンデータも各デバイスタイプの行に含まれます。 それ以外の場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、別の行で「[!UICONTROL Device]」の値 [!UICONTROL N/A]. |
| [!UICONTROL Display Path 1] | ([!DNL Google Ads] 拡張テキスト広告のみ ) 広告のベース URL の後の最初の表示パス。 |
| [!UICONTROL Display Path 2] | ([!DNL Google Ads] 拡張テキスト広告のみ ) 広告のベース URL の後の 2 番目の表示パス。 |
| [!UICONTROL Display Type] | 廃止 |
| [!UICONTROL Display URL] | 広告の表示 URL。エンドユーザーが広告で表示する内容です。 |
| [!UICONTROL DMA] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) クリックの発生元となった数値的な指定された市場領域（Denver の 751 など）。 ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL Domain] | ([!UICONTROL Domain Referral Report], [!UICONTROL Keyword Report]) クリックの発生元となったドメイン名。 |
| [!UICONTROL eCPM] | 効果的な CPM、または指定した日付範囲での 1,000 件のインプレッションあたりの平均支払額。 eCPM の値は CPM キャンペーンまたは CPC キャンペーンで計算されます。 |
| [!UICONTROL EF Campaign ID] | Search、Social および Commerce がキャンペーンに割り当てる数値 ID。 |
| [!UICONTROL EF ID] | ([!UICONTROL Transaction Report])(Adobe Advertisingコンバージョントラッキングサービスを持つ広告主、および[!UICONTROL EF Redirect]」トークンを使用したトラッキングメソッド ) クリックまたはコンバージョンのトークン。<ul><li>の場合 [!DNL Google Ads] 広告を検索する場合、EF ID は `{gclid}:G:s`:Googleクリック ID(GCLID) とネットワークタイプ（検索の場合は「s」）が含まれます。</li><li> の場合 [!DNL Microsoft Advertising] 広告を検索する場合、EF ID は `{msclkid}:G:s`:Microsoftクリック ID(MSCLKID) とネットワークタイプ（検索の場合は「s」）が含まれます。</li><li>他の広告ネットワーク上の検索広告の場合、EF ID にはサーファー ID、クリック時間、ネットワークタイプが含まれます。</li><li>ディスプレイ広告の場合、EF ID には、サーファー ID、クリックまたはインプレッション時間、ネットワークタイプが含まれます。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | ([!UICONTROL Geo Distribution Report]；検索、ソーシャル、コマースの場合のみ ) 地理的な場所の内部 ID。データの標準化に使用されます。 |
| [!UICONTROL EF Portfolio Group ID] | ポートフォリオが属するポートフォリオグループの数値 ID。 |
| [!UICONTROL EF Search Engine ID] | Search、Social および Commerce が広告ネットワークに割り当てる数値 ID。  <i>[!UICONTROL 3]</i> 対象： [!DNL Google Ads], <i>[!UICONTROL 10]</i> 対象： [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> 対象： [!DNL Meta], <i>[!UICONTROL 86]</i> 対象： [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> 対象： [!DNL Naver], <i>[!UICONTROL 88]</i> 対象： [!DNL Baidu], <i>[!UICONTROL 90]</i> 対象： [!DNL Yandex], <i>[!UICONTROL 94]</i> 対象： [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> 対象： [!DNL Yahoo Native] （非推奨）、または <i>[!UICONTROL 106]</i> 対象： [!DNL Pinterest] （非推奨）。 |
| [!UICONTROL End Date] | 最終日が報告されました。 |
| [!UICONTROL Engagement Rate] | （ビデオ広告）アクション数を、広告が表示された回数で割った値です。 |
| [!UICONTROL Engagements] | （ビデオ広告）ユーザーが 10 秒以上広告を視聴した回数、または 10 秒未満の場合は完了広告を視聴した回数です。 |
| [!UICONTROL Est. Clicks] | ([!UICONTROL Geo Distribution Report]；検索および表示キャンペーンのみ ) 広告グループ/キャンペーン/ポートフォリオの組み合わせに対する推定クリック数。 この値は、広告ネットワークによって提供される値とは異なる場合があります。 |
| [!UICONTROL Estimated Cost] | 検索、ソーシャル、コマースで追跡した、関連する広告の推定コストの合計です。 この値は、広告ネットワークによって提供される値とは異なる場合があります。 |
| [!UICONTROL Estimated Impressions] | （キャンペーンのみを表示）検索、ソーシャル、コマースで追跡された広告インプレッション数の推定値。 この値は、 [!UICONTROL Impressions] 列（使用可能な場合）：広告ネットワークによって提供される値を表示します。 |
| [!UICONTROL Exclude (yes/no)] | 入札が除外されるかどうか (<i>[!UICONTROL Yes]</i>) または入札が許可されます (<i>[!UICONTROL No]</i>) を参照してください。 |
| [!UICONTROL First Page CPC] | (Googleキャンペーンのみ ) 指定した日付範囲で検索結果の最初のページに表示される広告のクリック単価 (CPC)。 |
| `GGL*`, `GGL_CT*`、および `GGL_XD_CT*` [[!DNL Google Ads] — 追跡されたコンバージョン/トランザクションのプロパティ。 | ([!DNL Google Ads] 検索およびショッピングネットワーク上のキャンペーン ) [!DNL Google Ads] — トラッキングされたコンバージョン。各コンバージョンに最大 3 つの異なるトランザクションプロパティを持ちます。<ul><li>`GGL*` — （追跡する場合）キーワードのコンバージョン値で、「GGL」プレフィックスで始まる値（GGL Purchase など）。</li><li>`GGL_CT*` — 「GGL_CT」プレフィックス（GGL_CT_Purchase など）で始まるコンバージョンの数（カウント）。</li><li>`GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合、コンバージョンを追跡する際）クロスデバイスコンバージョンの数（数）。 [!DNL Google Ads] 「GGL_XD_CT_」プレフィックスで始まる (GGL_XD_CT_Purchase など )。</li></ul><br>各コンバージョンは、入札単位およびクリック日別に記録されます。イベントレベルでは使用できません。 詳しくは、 [!DNL Google Ads] — トラッキングされたコンバージョン：[[!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).&quot; |
| [!UICONTROL Impr. (Abs. Top) %] | ([!DNL Google Ads] （のみ）オーガニック検索結果の上の最初の広告として表示される広告インプレッションの割合。 |
| [!UICONTROL Impr. (Top) %] | ([!DNL Google Ads] （のみ）オーガニック検索結果の上に表示される広告インプレッションの割合。 |
| [!UICONTROL Impressions] | 指定した日付範囲での広告インプレッション数。 |
| [!UICONTROL Interaction Rate] | （ビデオ広告）インタラクション数を広告の回数（ビデオおよびサムネールのインプレッション）で割った数です。 |
| [!UICONTROL Interactions] | （ビデオ広告）ユーザーが広告を視聴した回数です。 |
| [!UICONTROL Is_Click_Objectives] | ([!UICONTROL Portfolio Report]) <i>true</i> ( ポートフォリオに [!UICONTROL Maximize Clicks] 入札戦略および <i>false</i> それ以外の場合は |
| [!UICONTROL Keyword] | キーワード。<br><br><b>注意：</b> レポートにコンテンツ対応検索キャンペーンの広告グループのデータが含まれる場合、この列には、該当する広告グループ名 (「(adgroup content) 広告グループ名」など ) が含まれます。 検索キャンペーンでのサイトターゲット配置の場合、この列に値は含まれません。 |
| [!UICONTROL Keyword ID] | Search、Social および Commerce がキーワードに割り当てる数値 ID。 |
| [!UICONTROL Keyword Status] | 検索語句が一致したキーワードのステータス。 <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Deleted]</i>または <i>[!UICONTROL Disapproved]</i>. |
| [!UICONTROL Label Classification] | ([!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]) ラベルの分類。 |
| [!UICONTROL Label Value] | ([!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]) ラベル分類の値。 |
| [!UICONTROL Language] | （ディスプレイキャンペーン）ターゲットオーディエンスの言語。 |
| [!UICONTROL Link Type] | ([!UICONTROL Keyword Report]; [!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ。データは、レポートに指定された属性ルールが「最後のイベント」の場合にのみ使用可能です ) 行が（広告自体ではなく）広告拡張または製品/ショッピング広告のクリックによるコンバージョンをレポートする場合、クリックされたリンクのタイプとタイトルを表示します。<ul><li>`pla:*`  — 製品広告は、 `pla:<product ID>`例えば、「pla:8525822」などです。</li><li>`sl:*`  — サイトリンクは、 `sl:<Sitelink text>`例えば、「sl:See Current Offers」など。</li></ul> |
| [!UICONTROL Listing Match Type] | 広告リストのキーワード一致タイプ。 <i>[!UICONTROL Content]</i> コンテンツターゲットキャンペーン内の広告の場合、または <i>[!UICONTROL Sitecpc]</i> サイトターゲットキャンペーン内のプレースメントの場合。 の場合 [!DNL Microsoft Advertising] キーワードは、複数の一致タイプ (「[!UICONTROL Broad],[!UICONTROL Exact]」) をクリックします。 |
| [!UICONTROL Location] | （ディスプレイキャンペーン）ターゲットオーディエンスの場所。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | ( の完了したレポート行で [!DNL Microsoft Advertising] レスポンシブおよびマルチメディア広告 ) 広告の長いヘッドライン。 これらの列を表示するには、[!UICONTROL Long Creative Titles]」列に表示されます。 |
| [!UICONTROL Long Creative Titles] | ( の [!DNL Microsoft Advertising] レスポンシブおよびマルチメディア広告 ) 広告の長いタイトル ([!UICONTROL Long Creative Title1]&quot;から&quot;[!UICONTROL Long Creative Title5]」) をクリックします。 |
| [!UICONTROL Market Type] | 市場タイプ：  <i>[!UICONTROL search]</i> または <i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | ( ポートフォリオ内の Campaign と [!UICONTROL ROI], [!UICONTROL CPT]または [!UICONTROL Marginal Cost per Transaction] 支出戦略 ) ポートフォリオの 1 日の最大予算ターゲットです。 |
| [!UICONTROL Max Spend (%)] | ([!UICONTROL Network Constraint Report]) 広告ネットワークに対して設定された、ポートフォリオの支出の最大割合。 制約タイプ「 」を使用するポートフォリオの場合[!UICONTROL Min-Max]、これは [!UICONTROL Max %] の値です。 制約タイプ「 」を使用するポートフォリオの場合[!UICONTROL Target Spend]、これは [!UICONTROL Target Spend] の値です。 |
| [!UICONTROL Method ID] | ([!UICONTROL Portfolio Report])  <!-- ???????? Insert value --> |
| [!UICONTROL Metro Code] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) インプレッション数またはクリック数の発生元となった数値のメトロコード（Denver の us-751 など）。 検索ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL Min Spend (%)] | ([!UICONTROL Network Constraint Report]) 広告ネットワーク用に設定された、ポートフォリオの支出の最小割合。 制約タイプ「 」を使用するポートフォリオの場合[!UICONTROL Min-Max]、これは [!UICONTROL Min %] 値 ( [!UICONTROL Min %] が設定されている。 制約タイプ「 」を使用するポートフォリオの場合[!UICONTROL Target Spend]、これは [!UICONTROL Target Spend] の値です。 |
| [!UICONTROL Network Account ID] | ネットワークによって割り当てられたアカウント ID。 |
| [!UICONTROL Network Ad Group ID] | ネットワークによって割り当てられた広告グループ ID。 |
| [!UICONTROL Network Campaign ID] | ネットワークによって割り当てられたキャンペーン ID。 |
| [!UICONTROL Objective Name] | ポートフォリオの目的。 |
| [!UICONTROL Objective Value] | ポートフォリオの現在の目標に従って計算された、合計加重コンバージョン。 |
| [!UICONTROL Objective Value Calculation] | 目標値の導き出しに使用される計算。 |
| [!UICONTROL Outbound Clicks] | ([!DNL Meta] 広告 ) ユーザーを離脱させる広告内のリンクのクリック数 [!DNL Meta]-owned プロパティ。 |
| [!UICONTROL Parent Product Groupings] | 親製品グループの完全な階層。 `>>` 層間 ( `All Products>>CategoryL1=Animals`) に書き込まれます。 |
| [!UICONTROL Partition Type] | 製品グループのタイプ： <i>[!UICONTROL Sub-Division]</i> （親製品グループ）または <i>[!UICONTROL Unit]</i> （入札を持つ子製品グループの最下位レベル）。 |
| [!UICONTROL Path Position] | ([!UICONTROL Transaction Report]) コンバージョンパス内でのイベントの位置。 |
| [!UICONTROL Path Total] | ([!UICONTROL Transaction Report]) パスの位置のイベントの合計数。 |
| [!UICONTROL Portfolio] | ポートフォリオ。 |
| [!UICONTROL Portfolio Count] | ([!UICONTROL Portfolio Report]) 目標に関連付けられたポートフォリオの数。 <!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | 数値のポートフォリオ ID。 |
| [!UICONTROL Portfolio Spend Strategy] | ([!UICONTROL Portfolio Report]) ポートフォリオの支出戦略： <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly]</i>, <i>[!UICONTROL Monthly]</i>, <i>[!UICONTROL ROI]</i>, <i>[!UICONTROL Day of week]</i>, <i>[!UICONTROL Day of month]</i>, <i>[!UICONTROL CPT]</i>, <i>[!UICONTROL Marginal CPT]</i>, <i>[!UICONTROL Google Target CPA]</i>または <i>[!UICONTROL Google Target ROAS]</i>. |
| [!UICONTROL Portfolio Status] | ポートフォリオのステータス：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリックおよび売上高データを収集し、入札を最適化するデータをモデリングし、入札およびキャンペーン予算（最適化タイプおよびキャンペーン入札戦略に応じて）を最適化します。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数および売上高データを収集し、データをモデリングしていますが、入札やキャンペーン予算は最適化されていません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポートを作成する目的で、関連するキャンペーンのクリックデータを収集しますが、データのモデリングや入札やキャンペーン予算の最適化はおこないません。</li></ul> |
| [!UICONTROL Portfolio Target] | ([!UICONTROL Portfolio Report]) ポートフォリオの支出戦略の日別ターゲット。 日別/月別および曜日/月別の戦略の場合は、現在の日のターゲットが表示されます。 |
| [!UICONTROL Preferred Devices] | ([!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン ) 広告設定が <i>[!UICONTROL Mobile ads]</i> または <i>[!UICONTROL All ads]</i>. |
| [!UICONTROL Product Group ID] | 広告ネットワークが製品グループに割り当てる数値 ID。 |
| [!UICONTROL Product Groupings] | 親製品グループ。 |
| [!UICONTROL Product ID] | ([!UICONTROL Keyword Report]; [!DNL Google Ads] 製品リスト広告 ) 広告と共に表示される製品の製品 ID。<br><br><b>注意：</b> この ID は、製品リストにトラッキングパラメーターが含まれている場合にのみ取り込まれます `ev_plx=<GMC product ID>`（内に追加する必要があります） [!DNL Google Merchant Center]. |
| [!UICONTROL Raw Transaction Data] | ([!UICONTROL Transaction Report]) トランザクションプロパティの売上高（1 件の登録の場合は 1、12 米ドルの注文の場合は 12 など）。 複数の入札単位に同じトランザクション ID がある場合、トラッキング ID の売上高は、指定したクリック日（クリックデータが使用可能な場合）のクリック数に応じて分割されます。 |
| [!UICONTROL Reach] | ([!DNL Meta] 広告 ) 少なくとも 1 回広告を閲覧した人の数です。 注意： [!DNL Meta] ユーザープロファイルのリーチの重複を毎日排除し、 [!DNL Meta] 検索、Social、および Commerce では異なる場合があります。 |
| [!UICONTROL Region] | ([!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]) インプレッションまたはクリックが発生した地域または米国/カナダの州。 ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL SE Creative ID] | ネットワークによって割り当てられた広告 ID。 |
| [!UICONTROL Search (Abs. Top) IS] | ([!DNL Google Ads] および [!DNL Microsoft Advertising]) 絶対的なトップの場所（オーガニック検索結果の最初の広告）で受け取ったインプレッション数を、トップの場所で受け取る資格のある推定インプレッション数で割った値です。 10%未満の割合は、「`<10%`&quot;または&quot;`0.0999`.&quot; |
| [!UICONTROL Search (Top) IS] | ([!DNL Google Ads] および [!DNL Microsoft Advertising]) 上位の場所（オーガニック検索結果の上）で受け取ったインプレッション数を、上位の場所で受け取る資格のある推定インプレッション数で割った値です。 10%未満の割合は、「`<10%`&quot;または&quot;`0.0999`.&quot; |
| [!UICONTROL Search Engine] | 広告ネットワーク。 |
| [!UICONTROL Search exact match IS] | キーワードと完全に一致する検索に対して受け取ったインプレッション数を、受け取る資格のある推定完全一致インプレッション数で割った値です。 この数が少ない場合は、入札額が少なすぎるか、広告の質や関連性が低いことが原因の可能性があります。 |
| [!UICONTROL Search impr. share] | ([!DNL Google Ads] のみ ) 受け取ったインプレッション数を、受け取る資格のある推定インプレッション数で割った値です。 10%未満の割合は「&lt;10%」、90%を超える割合は「`>90%`.&quot; |
| [!UICONTROL Search lost abs. top IS (budget)] | ([!DNL Google Ads] および [!DNL Microsoft Advertising]) 日次または月次の予算が少なすぎるので、広告がオーガニック検索結果を上回る最初の広告ではなかった時間の割合。 Google広告キャンペーンの場合、90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search lost abs. top IS (rank)] | ([!DNL Google Ads] および [!DNL Microsoft Advertising]) 広告のランクが低いので、広告がオーガニック検索結果を上回る最初の広告ではなかった時間の割合。 Google広告キャンペーンの場合、90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search lost IS (budget)] | ([!DNL Google Ads] （のみ）日次または月次の予算が少なすぎるので、広告が表示されなかった時間の割合。 この指標は、キャンペーンレベルでのみ使用できます。 90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search lost IS (rank)] | ([!DNL Google Ads] （ただし）広告のランクが低いために広告が表示されなかった時間の割合。 90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search lost top IS (budget)] | ([!DNL Google Ads] および [!DNL Microsoft Advertising]) 日次予算または月次予算が少なすぎるので、広告がオーガニック検索結果を上回らなかった時間の割合。 の場合 [!DNL Google Ads] キャンペーンの場合、90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search lost top IS (rank)] | ([!DNL Google Ads] と [!DNL [!DNL Microsoft Advertising]]) 広告のランクが低いので、広告がオーガニック検索結果を上回らなかった時間の割合。 Google広告キャンペーンの場合、90%を超える割合は、「`>90%`&quot;または&quot;`0.9001`.&quot; |
| [!UICONTROL Search Term] | ([!UICONTROL Transaction Report]) ユーザーが照会した検索語句。 |
| [!UICONTROL SETrackingOnly] | アカウントを追跡しているが、入札を行っていないかどうか： <i>[!UICONTROL TRUE]</i> または <i>[!UICONTROL FALSE]</i>. |
| [!UICONTROL Site] | ( ドメイン紹介レポート及び [!UICONTROL Keyword Report]；サイトターゲット配置 ) クリックの発生元となるサイト。 |
| [!UICONTROL Start Date] | 最初の日が報告されました。 |
| [!UICONTROL State] | ( 地域配分レポート、 [!UICONTROL Keyword Report]) トランザクションの開始元の状態。 ユーザーの IP アドレスから判断されます。 |
| [!UICONTROL Surfer ID] | ([!UICONTROL Transaction Report]) トランザクションを完了したユーザーの ID。 |
| [!UICONTROL Through Plays] | ([!DNL Meta] ads) 広告全体を視聴した視聴回数。 |
| [!UICONTROL Top of Page CPC] | (Googleキャンペーンのみ ) 指定した日付範囲で検索結果ページの先頭に表示される広告のクリック単価 (CPC)。 |
| [!UICONTROL Tracking URL] | （検索ターゲットキーワードのみ）（該当する場合）検索、ソーシャル、コマースのトラッキングコードに埋め込まれた、トラッキングテンプレートまたはリンク先 URL。 |
| [!UICONTROL Transaction Property Name] | ([!UICONTROL Transaction Report]) トランザクションのクレジットが付与される広告主固有のトランザクションプロパティ。 |
| [!UICONTROL Transaction Time] | ([!UICONTROL Transaction Report]) 指定したトランザクションプロパティがクレジットされた時刻。 |
| [!UICONTROL User Account Type] | 廃止 |
| [!UICONTROL User SE Account ID] | Search、Social および Commerce が広告ネットワークに割り当てる数値 ID。 |
| [!UICONTROL Video Average Play Time] | ([!DNL Meta] ads) 単一のインプレッションに対する、ビデオの再生に費やされた時間を含む、ビデオが再生された平均時間。 |
| [!UICONTROL Video Plays] | ([!DNL Meta] ads) ビデオの再生が開始された回数（再生を除く）。 |
| [!UICONTROL VideoQuartile25Rate], [!UICONTROL VideoQuartile50Rate], [!UICONTROL VideoQuartile75Rate]、および [!UICONTROL VideoQuartile100Rate] | （ビデオ広告）再生回数の 25%、50%、75%または 100%であったビデオの割合。 |
| [!UICONTROL View Rate] | （ビデオ広告）視聴回数またはアクション数を、広告（ビデオおよびサムネールのインプレッション）が表示された回数で割った値です。 |
| [!UICONTROL Views] | （ビデオ広告）ユーザーが広告を視聴した、または関与した回数です。 |
| [!UICONTROL ViewThroughConversions] | (Ads on the audience network)1 つ以上のインプレッションに起因し、クリックは発生しなかったコンバージョンの数。 |

<table style="table-layout:auto">

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [基本レポートと高度なレポートについて](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本レポートまたは高度なレポートの生成](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [基本レポート設定と詳細レポート設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
