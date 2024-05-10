---
title: 基本レポートと高度なレポートのレポート列
description: 基本レポートと高度なレポートで使用可能なデータ列について説明します。
exl-id: 649cdfa0-e6f2-4881-9f9d-8217e2547d99
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '3747'
ht-degree: 0%

---

# 基本レポートと高度なレポートのレポート列

| 列 | 説明 |
| ---- | ---- |
| \[ 広告主固有のカスタム （派生）指標\] | の値 [作成したカスタム指標](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) これは、既存の指標から計算されています。 |
| \[ 広告主固有のラベル分類\] | エンティティ レベルでエンティティに現在適用されているラベル分類。 複数のラベルの分類は、コンマ（,）で区切ります。 |
| \[ 広告主固有のコンバージョン指標\] | 指定したコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| \[Googleでトラッキングされたコンバージョン\] | 「GGL\*、GGL_CT\*、GGL_XD_CT\*」のエントリを参照してください。 |
| [!UICONTROL 7-Day Click Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない過去 7 日間（レポートで指定された日付範囲を除く）のクリック数予測の平均精度を、パーセンテージで表したもの。 |
| [!UICONTROL 7-Day Cost Accuracy] | （[!UICONTROL Portfolio Report]）現在を含まない過去 7 日間（レポートで指定された日付範囲を除く）のコスト予測の平均精度をパーセントで表したもの。 |
| [!UICONTROL 7-Day Revenue Accuracy] | （[!UICONTROL Portfolio Report]）現在を含まない過去 7 日間（レポートで指定された日付範囲を除く）の収益予測の平均精度は、パーセンテージで表されます。 |
| [!UICONTROL Account] | アカウント名。 |
| [!UICONTROL Account Status] | 検索、ソーシャル、Commerce内でのアカウントのステータス： <ul><li><i>[!UICONTROL Enabled]:</i> （デフォルト）同期された広告ネットワークの場合、検索、ソーシャルおよびCommerceは広告ネットワークアカウントにログインしてキャンペーンデータを取得でき、最適化やトラッキング生成などのその他の該当する機能が有効になります。<br><br>非同期の広告ネットワークの場合は、最適化やトラッキング生成など、適用可能な機能を使用できます。</li><li><i>[!UICONTROL Disabled]:</i> 同期された広告ネットワークの場合、検索、ソーシャル、Commerceは広告ネットワークアカウントにログインしないので、キャンペーンデータは取得されません。また、最適化やトラッキングの生成など、その他の該当する機能は無効になります。 アカウントが有効になっている間に収集されたデータは、引き続き保存されますが、すべてのキャンペーン管理ビューおよび今後作成するすべてのレポートには、アカウントが無効になっている期間のデータは含まれません。<br><br>同期されていない広告ネットワークでは、最適化やトラッキングの生成など、適用可能な機能は使用できません。</li></ul> |
| [!UICONTROL Active Ad Groups] | アクティブな広告グループの数。 |
| [!UICONTROL Active Ads/Creatives] | アクティブな広告/クリエイティブの数。 |
| [!UICONTROL Active Campaigns] | アクティブなキャンペーンの数。 |
| [!UICONTROL Active Keywords] | アクティブなキーワードの数。 |
| [!UICONTROL Ad Group] | 広告グループ。 |
| [!UICONTROL Ad Group ID] | 検索、ソーシャルおよびCommerceが広告グループに割り当てる数値 ID。 |
| [!UICONTROL Ad Group Status] | 広告グループのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>、または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Ad Group Type] | 広告グループのタイプ（など） <i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ）、 <i>[!UICONTROL Discovery]</i> （ディスカバリーキャンペーンのみ）、 <i>[!UICONTROL Display]</i> （ディスプレイキャンペーンのみ）、 <i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、 <i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ）、 <i>[!UICONTROL Shopping Showcase]</i>, <i>[!UICONTROL Shopping Product]</i> （標準のショッピングキャンペーンのみ）、 <i>[!UICONTROL Shopping Smart]</i> （スマートショッピングキャンペーン用）。 一部のキャンペーンタイプでは、1 つのキャンペーンに複数の広告タイプを含めることができます。 |
| [!UICONTROL Ad Groups] | ラベル値が割り当てられる広告グループの数。 |
| [!UICONTROL AD Name] | 広告グループ名（と同じ値） [!UICONTROL Ad Group]. |
| [!UICONTROL Ad Recall Lift] | （[!DNL Meta] キャンペーンのみ） 2 日以内に広告を覚えている推定ユーザー数。 |
| [!UICONTROL Ad Recall Rate] | （[!DNL Meta] キャンペーンのみ） 2 日以内に広告を覚えている推定ユーザー数を、到達したユーザー数で割った割合。 |
| [!UICONTROL Ad Size] | 広告のディメンション。 |
| [!UICONTROL AD Strength] | （[!DNL Google Ads] レスポンシブ検索広告）広告の効果： <i>[!UICONTROL average]</i>, <i>[!UICONTROL excellent]</i>, <i>[!UICONTROL good]</i>, <i>[!UICONTROL no_ads]</i>, <i>[!UICONTROL pending]</i>, <i>[!UICONTROL poor]</i>, <i>[!UICONTROL unknown]</i>、または <i>[!UICONTROL unspecified]</i>. |
| [!UICONTROL Adgroup MBA] | （[!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン）現在の広告グループレベルのモバイル入札調整。モバイルデバイスに広告を表示する際に入札を調整する方法を決定します。 |
| [!UICONTROL Advertiser] | 広告主名。 |
| [!UICONTROL Advertiser ID] | 広告主の検索、ソーシャル、Commerce アカウントの数値 ID。 |
| [!UICONTROL Avg Position] | 指定した日付範囲での広告の平均位置。<br><br>の場合 [!DNL Google Ads] および [!DNL Yahoo! Japan Ads] キャンペーン、このデータは 2019 年 9 月までのみ利用できます。 の場合 [!DNL Microsoft Advertising]このデータは 2021 年 1 月 22 日までのみ利用できます。 |
| [!UICONTROL Base URL] | キャンペーンまたはアカウントに設定された追加パラメーターを含む、キーワードのベース URL。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれません。 |
| [!UICONTROL Bid Strategy] | （ほとんどの広告ネットワーク）キャンペーンまたはキャンペーンコンポーネントの場合、これはキャンペーンの入札戦略です。 管理者アカウントにリンクされている広告ネットワークアカウントの場合、これはクロスアカウント入札戦略です。 使用可能な値は、広告ネットワークによって異なります。 |
| [!UICONTROL Business Name] | （[!DNL Microsoft Advertising] レスポンシブ広告） ビジネス名。 |
| [!UICONTROL Call to Action] | （[!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告）広告に含まれるコールトゥアクション。 |
| [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Campaign Budget] | キャンペーン予算。 |
| [!UICONTROL Campaign MBA] | （[!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン）現在のキャンペーンレベルのモバイル入札調整。モバイルデバイスに広告を表示するときに入札を調整する方法を決定します。 |
| [!UICONTROL Campaign Product Scope Filter] | （ショッピングネットワークを使用したキャンペーンのみ）キャンペーンに対して商品広告を作成できる、マーチャントアカウント内の商品。 |
| [!UICONTROL Campaign Start Date] | キャンペーンの入札が行われた/または行われた最初の日。 |
| [!UICONTROL Campaign Status] | キャンペーンステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Ended]</i>、または <i>[!UICONTROL Deleted]</i>. |
| [!UICONTROL Campaign Type] | キャンペーンタイプ（など） <i>[!UICONTROL Audience (Ctv Video)]</i><i>[!UICONTROL Audience (Feed)]</i>, <i>[!UICONTROL Audience (Image)]</i>, <i>[!UICONTROL Audience (Video)]</i>, <i>[!UICONTROL Brand Shopping]</i>, <i>[!UICONTROL Discovery]</i>, <i>[!UICONTROL Search and Display]</i>, <i>[!UICONTROL Standard Display]</i>, <i>[!UICONTROL Standard Performance Max]</i>, <i>[!UICONTROL Standard Search]</i>, <i>[!UICONTROL Standard Shopping]</i>, <i>[!UICONTROL Store Ad]</i>, <i>[!UICONTROL Video]</i>、または <i>[!UICONTROL Others]</i>. |
| [!UICONTROL Channel Type] | マーケティングチャネルのタイプ。 <i>[!UICONTROL Search]</i> または <i>[!UICONTROL Content]</i>. この列は、レポートの [!UICONTROL Search/Content] レポート設定の設定は「」です[!UICONTROL Combined].」と入力します。 |
| [!UICONTROL City] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Transaction Report]）クリックが発生した都市。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Click Match Type] | クリックされた広告のキーワード一致タイプ。 これは [!UICONTROL Listing Match Type] 次を除く [!DNL Microsoft Advertising] 一致するタイプが複数あるキーワード。 の場合 [!DNL Microsoft Advertising] キーワード。実際にクリックされた一致のタイプです。 |
| [!UICONTROL Click Value] | （[!UICONTROL Portfolio Report]） ポートフォリオの目的に指定されたクリック値。 |
| [!UICONTROL Click/Impression Time] | （[!UICONTROL Transaction Report]）変換の原因となったクリックまたはインプレッションが発生した時間。 |
| [!UICONTROL Clicks] | 指定した日付範囲内での広告のクリック数。 |
| [!UICONTROL Client ID1], [!UICONTROL Client Id 1] | （[!UICONTROL Keyword Report], [!UICONTROL Ad Variation Report]、および [!UICONTROL Transaction Report]（フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Id 2] | （[!UICONTROL Keyword Report] および [!UICONTROL Transaction Report]（フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Transaction ID] | （[!UICONTROL Transaction Report]）一意のトランザクション ID。 |
| [!UICONTROL Constraint End Date] | （[!UICONTROL Constraint Report]）制約がアクティブである最終日。 |
| [!UICONTROL Constraint Name] | （[!UICONTROL Constraint Report]）制約の名前。 |
| [!UICONTROL Constraint Start Date] | （[!UICONTROL Constraint Report]）制約がアクティブになる最初の日。 |
| [!UICONTROL Constraint Status] | （[!UICONTROL Constraint Report]）制約のステータス：  <i>[!UICONTROL Active]</i> または <i>[!UICONTROL Paused]</i>. |
| [!UICONTROL Constraint Type] | （[!UICONTROL Constraint Report]）制約のタイプ。  <i>[!UICONTROL Bid/Pos Constraint]</i>, <i>[!UICONTROL Bid Shift]</i>, <i>[!UICONTROL Campaign Budget]</i>, <i>[!UICONTROL Context Sensitive Bid]</i>, <i>[!UICONTROL Incremental Bidding]</i>, <i>[!UICONTROL Max CPA]</i>, <i>[!UICONTROL Min Margin]</i>, <i>[!UICONTROL Variable Bid Position]</i>, <i>[!UICONTROL Search Engine Min Bid]</i>、または <i>[!UICONTROL Variable Position]</i>. |
| [!UICONTROL Constraints] | エンティティに適用可能な制約の名前（コンマで区切る）。 |
| [!UICONTROL Content IS] | ディスプレイ/オーディエンスネットワークの広告で獲得したインプレッション数を、インプレッション数の推定値で割った値です。 対象： [!DNL Microsoft Advertising]の場合、これは&quot; &quot;と呼ばれます[!UICONTROL Audience IS].」と入力します。 |
| [!UICONTROL Content IS Lost (budget)] | 1 日または 1 か月の予算が低すぎたので、ディスプレイ/オーディエンスネットワークの広告で獲得できなかった推定インプレッション数の割合です。 対象： [!DNL Microsoft Advertising]の場合、これは&quot; &quot;と呼ばれます[!UICONTROL Audience lost IS (budget)].」と入力します。 |
| [!UICONTROL Content IS Lost (rank)] | 広告ランクが低いので、ディスプレイ/オーディエンスネットワークの広告で獲得した推定インプレッション数の割合は表示されませんでした。 対象： [!DNL Microsoft Advertising]の場合、これは&quot; &quot;と呼ばれます[!UICONTROL Audience lost IS (rank)].」と入力します。 |
| [!UICONTROL Conversion Type] | （[!UICONTROL Transaction Report]）変換の前のアクション：<ul><li><i>[!UICONTROL Click:]</i> コンバージョンの前に少なくとも 1 回の有料クリックが発生しました。</li><li><i>[!UICONTROL Impression:]</i> コンバージョン前には有料クリックは発生していなかったので、コンバージョンはビュースルー（有料クリックのないインプレッション）の結果となりました。</li></ul> |
| [!UICONTROL Cost] | 指定した日付範囲の広告の合計コスト。 |
| [!UICONTROL Country] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]）クリックが発生した国。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL CPC] | 指定した日付範囲内の広告に関するクリック単価（CPC）。 |
| [!UICONTROL Creative Base URL] | キャンペーンまたはアカウント用に設定された追加パラメーターを含む、広告のベース URL。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれません。 |
| [!UICONTROL Creative Destination URL] | 広告の最終的な URL または宛先 URL （トラッキングパラメーターを含む）。 |
| [!UICONTROL Creative Name] | （[!DNL Yahoo! Japan] のみ）広告イメージ名。 |
| [!UICONTROL Creative Title], [!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 広告のタイトルまたはヘッドライン。 必須タイトル行とオプションタイトル行の数はクリエイティブタイプによって異なります。 を表示 [!UICONTROL Creative Title4] およびの上位の列 [!DNL Microsoft Advertising] レスポンシブ広告またはマルチメディア広告には、「[!UICONTROL Creative Titles]レポート設定の「」列。 |
| [!UICONTROL Creative Titles] | （マルチメディアおよびレスポンシブ検索広告のみ）広告の短いヘッドラインごとに列を追加します（&quot;[!UICONTROL Creative Title]&quot; ～ &quot;[!UICONTROL Creative Title15]``）に含まれます。 この列を含める場合、他の列を含める必要はありません [!UICONTROL Creative Title] 列。ただし、を編集します [!UICONTROL Order Results/Limit Rows By] 並べ替え基準にするセクション [!UICONTROL Creative Titles] の代わりに [!UICONTROL Creative Title]. |
| [!UICONTROL Creative Type] | 広告の形式。 使用可能な値は次のとおりです。 <i>[!UICONTROL App Install Ad]</i>, <i>[!UICONTROL Call Only Ad]</i>, <i>[!UICONTROL Discovery Ad (single-image ads)]</i>, <i>[!UICONTROL Discovery Carousel Ad]</i> （マルチ画像カルーセル広告）、 <i>[!UICONTROL Display Ad]</i>, <i>[!UICONTROL Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Dynamic Search Ad]</i>, <i>[!UICONTROL Expanded Text Ad]</i>, <i>[!UICONTROL Legacy Text Ad]</i>, <i>[!UICONTROL Multimedia Ad]</i>, <i>[!UICONTROL Product Ad]</i>, <i>[!UICONTROL Responsive Ad]</i>, <i>[!UICONTROL Responsive Search Ad]</i>、または <i>[!UICONTROL Text Ad]</i>. |
| [!UICONTROL CTR] | クリックスルー率（クリック数を、含まれる広告のインプレッション数で割った値）。 |
| [!UICONTROL Currency] | 該当する通貨タイプ（「USD」や「GBP」など）。<br><br><b>注意：</b> 異なる通貨を使用する勘定科目のデータがレポートに含まれる場合は、任意の勘定科目[!UICONTROL Total]「通貨値は、通貨に関係なく、単に列のすべての数値の合計です。 |
| [!UICONTROL Current Bid] | ターゲットに対する現在の入札。 |
| [!UICONTROL Current First Page Bid] | （[!DNL Google Ads] キャンペーンのみ）広告を検索結果の最初のページに配置するために現在必要な、推定クリック単価（CPC）入札 [!DNL Google] 検索クエリがキーワードに一致します。<br><br>単一のキーワードと一致タイプの組み合わせの場合、この値は、その組み合わせに現在必要な最初のページの入札です。 複数のキャンペーンで同じキーワードと一致タイプの組み合わせを使用する場合、この値は、現在すべてのインスタンスで必要な最初のページの最小入札額になります。 |
| [!UICONTROL Current Quality Score] | （[!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ）広告ネットワークで指定された、キーワードまたは入札単位の現在の品質スコア。 範囲は 1 （低）から 10 （完全）です。 単一のキーワードと一致タイプの組み合わせの場合、この値はその組み合わせの現在のスコアです。 複数のキャンペーンで同じキーワードと一致タイプの組み合わせを使用する場合、この値は、すべてのインスタンス間の現在の最大スコアです。<br><br>広告ネットワークは、品質スコアを使用して入札価格と広告ポジションを決定します。 これは、関連する広告やユーザーの検索クエリ、ランディングページの品質に対するキーワードの関連性など、多くの要因に従って計算されます。 のキーワード [!DNL Google Ads]では、キーワードのクリックスルー率も考慮され、のキーワードについても考慮されます [!DNL Microsoft Advertising]ランディングページが提供するユーザーエクスペリエンスも考慮されます。 |
| [!UICONTROL Custom Bid Level] | （ディスプレイネットワークをターゲットにするGoogle キャンペーンのみ）入札を配置するレベル： <i>[!UICONTROL Ad Group]</i>, <i>[!UICONTROL Age]</i>, <i>[!UICONTROL Gender]</i>, <i>[!UICONTROL Interest and List]</i>, <i>[!UICONTROL Keyword]</i>, <i>[!UICONTROL Placement]</i>, <i>[!UICONTROL Vertical]</i>, <i>[!UICONTROL None]</i>、または <i>[!UICONTROL Unknown]</i>. |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 広告の本文。 必須の説明行とオプションの説明行の数は、クリエイティブタイプによって異なります。 を表示 [!UICONTROL Description3] および [!UICONTROL Description4] の列 [!DNL Microsoft Advertising] レスポンシブ広告またはマルチメディア広告には、「[!UICONTROL Descriptions]レポート設定の「」列。 |
| [!UICONTROL Descriptions] | （[!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告）広告の説明行ごとに列を追加します（&quot;[!UICONTROL Description1]&quot; ～ &quot;[!UICONTROL Description4]``）に含まれます。 この列を含める場合、他の列を含める必要はありません [!UICONTROL Description] 列。 |
| [!UICONTROL Device] | （[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Display Network], [!DNL Yahoo! Japan Ads]、および [!DNL Yahoo Native] キャンペーン）広告が表示されたデバイスタイプ。 <i>[!UICONTROL Computers]</i>, <i>[!UICONTROL Mobile]</i>, <i>[!UICONTROL Tablets]</i>, <i>[!UICONTROL Other]</i>、または <i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は N/A です。<br><br>検索キャンペーンで、キーワード、広告または広告拡張機能のトラッキングテンプレートや宛先 URL に、デバイス別にデータを追跡するパラメーターが含まれている場合（`&ev_dvc={device}&ev_dvm={devicemodel}`）を選択した場合は、デバイスタイプごとの行にもコンバージョンデータが含まれます。 そうでない場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、「」を使用して別の行に集計されます[!UICONTROL Device]の値 [!UICONTROL N/A]. |
| [!UICONTROL Display Path 1] | （[!DNL Google Ads] （拡張テキスト広告のみ）広告のベース URL の後の最初の表示パス。 |
| [!UICONTROL Display Path 2] | （[!DNL Google Ads] （拡張テキスト広告のみ）広告のベース URL の後の 2 番目の表示パス。 |
| [!UICONTROL Display Type] | 廃止 |
| [!UICONTROL Display URL] | 広告の表示 URL （エンドユーザーに表示される URL）。 |
| [!UICONTROL DMA] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]）クリックが発生した、数値の指定されたマーケットエリア（Denver の場合は 751 など）。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Domain] | （[!UICONTROL Domain Referral Report], [!UICONTROL Keyword Report]）クリックが発生したドメイン名。 |
| [!UICONTROL eCPM] | 有効 CPM、つまり指定した日付範囲内の 1000 インプレッションあたり支払われた平均費用。 eCPM の値は、CPM または CPC キャンペーンに対して計算されます。 |
| [!UICONTROL EF Campaign ID] | 検索、ソーシャルおよびCommerceがキャンペーンに割り当てる数値 ID。 |
| [!UICONTROL EF ID] | （[!UICONTROL Transaction Report]）（Adobe Advertisingコンバージョントラッキングサービスを使用する広告主、「[!UICONTROL EF Redirect]「トークンによるトラッキングメソッド） クリックまたはコンバージョンのトークン。<ul><li>の場合 [!DNL Google Ads] 広告を検索、EF ID はです `{gclid}:G:s`。Google クリック ID （GCLID）とネットワークタイプ（検索用の「s」）が含まれます。</li><li> の場合 [!DNL Microsoft Advertising] 広告を検索、EF ID はです `{msclkid}:G:s`Microsoftのクリック ID （MSCLKID）とネットワークタイプ（検索用に「s」）が含まれます。</li><li>他の広告ネットワークでの検索広告の場合、EF ID にはサーファー ID、クリック時間、ネットワークタイプが含まれます。</li><li>ディスプレイ広告の場合、EF ID にはサーファー ID、クリックまたはインプレッション時間、ネットワークタイプが含まれます。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | （[!UICONTROL Geo Distribution Report]（検索、ソーシャル、Commerceでの使用のみ）地理的な場所の内部 ID。データの正規化に使用されます。 |
| [!UICONTROL EF Portfolio Group ID] | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL EF Search Engine ID] | 検索、ソーシャルおよびCommerceが広告ネットワークに割り当てる数値 ID:  <i>[!UICONTROL 3]</i> （用） [!DNL Google Ads], <i>[!UICONTROL 10]</i> （用） [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> （用） [!DNL Meta], <i>[!UICONTROL 86]</i> （用） [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> （用） [!DNL Naver], <i>[!UICONTROL 88]</i> （用） [!DNL Baidu], <i>[!UICONTROL 90]</i> （用） [!DNL Yandex], <i>[!UICONTROL 94]</i> （用） [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> （用） [!DNL Yahoo Native] （非推奨）、または <i>[!UICONTROL 106]</i> （用） [!DNL Pinterest] （非推奨）。 |
| [!UICONTROL End Date] | 最後に報告された日。 |
| [!UICONTROL Engagement Rate] | （ビデオ広告）エンゲージメント数を、広告の表示回数で割った値。 |
| [!UICONTROL Engagements] | （ビデオ広告）ユーザーが広告を 10 秒以上視聴した回数、または広告が 10 秒未満の場合は広告全体を視聴した回数。 |
| [!UICONTROL Est. Clicks] | （[!UICONTROL Geo Distribution Report]（キャンペーンの検索と表示のみ）広告グループ/キャンペーン/ポートフォリオの組み合わせの推定クリック数。 この値は、広告ネットワークで指定される値とは異なる場合があります。 |
| [!UICONTROL Estimated Cost] | 検索、ソーシャルおよびCommerceで追跡した関連広告の推定コストの合計。 この値は、広告ネットワークで指定される値とは異なる場合があります。 |
| [!UICONTROL Estimated Impressions] | （キャンペーンの表示のみ）検索、ソーシャル、Commerceでトラッキングした広告インプレッションの推定数。 この値は、の値とは異なる場合があります [!UICONTROL Impressions] 列（使用可能な場合）：広告ネットワークによって提供される値を示します。 |
| [!UICONTROL Exclude (yes/no)] | 入札が除外されているかどうか（<i>[!UICONTROL Yes]</i>）または入札できます（<i>[!UICONTROL No]</i>）に設定する必要があります。 |
| [!UICONTROL First Page CPC] | （Google キャンペーンのみ）指定した日付範囲に検索結果の最初のページに表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Frequency] | （[!DNL Meta] キャンペーンのみ）訪問者が広告を表示した平均回数。 |
| `GGL*`, `GGL_CT*`、および `GGL_XD_CT*` [[!DNL Google Ads] – トラッキングされたコンバージョン ] | （[!DNL Google Ads] 検索およびショッピングネットワーク上のキャンペーン） [!DNL Google Ads] – で追跡されるコンバージョン。各コンバージョンに対して最大 3 つの個別の指標を使用します。<ul><li>`GGL*` — （追跡する場合）「GGL」プレフィックスで始まるキーワードのコンバージョン値（GGL 購入など）。</li><li>`GGL_CT*` — 「GGL_CT」プレフィックスで始まるコンバージョンの数（カウント）（GGL_CT_Purchase など）。</li><li>`GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合は、トラッキング時）クロスデバイスコンバージョンの数（カウント）。で測定されます。 [!DNL Google Ads] 「GGL_XD_CT_」プレフィックス（GGL_XD_CT_Purchase など）で始まる。</li></ul><br>各コンバージョンは、入札単位とクリック日によって記録されます。イベントレベルでは使用できません。 詳しくは、 [!DNL Google Ads] – 追跡されたコンバージョン。を参照してください。[[!DNL Google Ads] 検索、ソーシャル、Commerceのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).」と入力します。 |
| [!UICONTROL Impr. (Abs. Top) %] | （[!DNL Google Ads] のみ）オーガニック検索結果の上に最初の広告として表示される広告インプレッションの割合。 |
| [!UICONTROL Impr. (Top) %] | （[!DNL Google Ads] のみ）オーガニック検索結果の上に表示される広告インプレッション数の割合。 |
| [!UICONTROL Impressions] | 指定した日付範囲内の広告インプレッション数。 |
| [!UICONTROL Interaction Rate] | （ビデオ広告）インタラクション数を広告の表示回数（ビデオおよびサムネールのインプレッション数）で割った値です。 |
| [!UICONTROL Interactions] | （ビデオ広告）訪問者が広告を視聴した回数。 |
| [!UICONTROL Is_Click_Objectives] | （[!UICONTROL Portfolio Report]） <i>true</i> ポートフォリオにを含むキャンペーンが含まれている場合 [!UICONTROL Maximize Clicks] 入札戦略 <i>偽</i> それ以外。 |
| [!UICONTROL Keyword] | キーワード。<br><br><b>注意：</b> レポートにコンテンツ対応の検索キャンペーンの広告グループのデータが含まれる場合、この列には「（広告グループコンテンツ）広告グループ名」など、該当する広告グループ名が含まれます。 検索キャンペーンでサイトをターゲットにしたプレースメントの場合、この列には値がありません。 |
| [!UICONTROL Keyword ID] | 検索、ソーシャルおよびCommerceがキーワードに割り当てる数値 ID。 |
| [!UICONTROL Keyword Status] | 検索語が一致したキーワードのステータス： <i>[!UICONTROL Active]</i>, <i>[!UICONTROL Paused]</i>, <i>[!UICONTROL Deleted]</i>、または <i>[!UICONTROL Disapproved]</i>. |
| [!UICONTROL Label Classification] | （[!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]） ラベルの分類。 |
| [!UICONTROL Label Value] | （[!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]） ラベル分類の値。 |
| [!UICONTROL Language] | （キャンペーンを表示）ターゲットオーディエンスの言語。 |
| [!UICONTROL Link Type] | （[!UICONTROL Keyword Report]; [!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ。データを使用できるのは、レポートに指定したアトリビューションルールが「最終イベント」の場合のみです）行が（広告自体ではなく）広告拡張機能または製品/ショッピング広告のクリックによるコンバージョンをレポートする場合、この列には、クリックされたリンクのタイプとタイトルが表示されます。<ul><li>`pla:*`  – 製品広告のリストは次のとおりです `pla:<product ID>`（「pla:8525822」など）。</li><li>`sl:*` — サイトリンクは次のようにリストされます `sl:<Sitelink text>`「sl:See Current Offers」など。</li></ul> |
| [!UICONTROL Listing Match Type] | 広告リストのキーワード一致タイプ。 <i>[!UICONTROL Content]</i> コンテンツターゲットキャンペーンの広告の場合、または <i>[!UICONTROL Sitecpc]</i> サイトターゲットキャンペーンのプレースメント。 の場合 [!DNL Microsoft Advertising] キーワード。複数の一致タイプが含まれる場合があります（「[!UICONTROL Broad],[!UICONTROL Exact]``）に含まれます。 |
| [!UICONTROL Location] | （ディスプレイキャンペーン）ターゲットオーディエンスの場所。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | （完了したレポート行内） [!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告）広告の長いヘッドライン。 これらの列を表示するには、「[!UICONTROL Long Creative Titles]レポート設定の「」列。 |
| [!UICONTROL Long Creative Titles] | （用 [!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告）広告の長いタイトルごとに列を追加します（&quot;[!UICONTROL Long Creative Title1]&quot; ～ &quot;[!UICONTROL Long Creative Title5]``）に含まれます。 |
| [!UICONTROL Market Type] | マーケットタイプ：  <i>[!UICONTROL search]</i> または <i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | （ポートフォリオでのキャンペーン [!UICONTROL ROI], [!UICONTROL CPT]、または [!UICONTROL Marginal Cost per Transaction] 支出戦略）ポートフォリオの 1 日の最大予算ターゲット。 |
| [!UICONTROL Max Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワーク用に設定されたポートフォリオの支出の最大割合。 制約タイプ「」を使用するポートフォリオの場合[!UICONTROL Min-Max]」といった具合です [!UICONTROL Max %] の値。 制約タイプ「」を使用するポートフォリオの場合[!UICONTROL Target Spend]」といった具合です [!UICONTROL Target Spend] の値。 |
| [!UICONTROL Method ID] | （[!UICONTROL Portfolio Report]） |
| [!UICONTROL Metro Code] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]）インプレッション数またはクリック数の発生元となった数値のメトロコード（Denver の場合の us-751 など）。 これは、検索ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Min Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワーク用に設定されたポートフォリオ支出の最小割合。 制約タイプ「」を使用するポートフォリオの場合[!UICONTROL Min-Max]」といった具合です [!UICONTROL Min %] 値（の場合） [!UICONTROL Min %] が設定されました。 制約タイプ「」を使用するポートフォリオの場合[!UICONTROL Target Spend]」といった具合です [!UICONTROL Target Spend] の値。 |
| [!UICONTROL Network Account ID] | ネットワークによって割り当てられたアカウント ID。 |
| [!UICONTROL Network Ad Group ID] | ネットワークによって割り当てられた広告グループ ID。 |
| [!UICONTROL Network Campaign ID] | ネットワークによって割り当てられたキャンペーン ID。 |
| [!UICONTROL Network Campaign Objective] | （[!DNL Meta] キャンペーンのみ）キャンペーンの目的。 |
| [!UICONTROL Objective Name] | ポートフォリオの目的。 |
| [!UICONTROL Objective Value] | ポートフォリオの現在の目標に従って計算された、重み付けされたコンバージョンの合計。 |
| [!UICONTROL Objective Value Calculation] | 目標値を導き出すために使用される計算。 |
| [!UICONTROL Outbound Clicks] | （[!DNL Meta] キャンペーンのみ）ユーザーが離脱した広告内のリンクのクリック数 [!DNL Meta]が所有するプロパティ。 |
| [!UICONTROL Parent Product Groupings] | 親製品グループの完全な階層（ `>>` 階層間（など） `All Products>>CategoryL1=Animals`）、該当する場合。 |
| [!UICONTROL Partition Type] | 製品グループのタイプ。 <i>[!UICONTROL Sub-Division]</i> （親製品グループ）または <i>[!UICONTROL Unit]</i> （入札がある子製品グループの最下位レベル）。 |
| [!UICONTROL Path Position] | （[!UICONTROL Transaction Report]）コンバージョンパス内のイベントの位置。 |
| [!UICONTROL Path Total] | （[!UICONTROL Transaction Report]）パス位置のイベントの合計数。 |
| [!UICONTROL Portfolio] | ポートフォリオ。 |
| [!UICONTROL Portfolio Count] | （[!UICONTROL Portfolio Report]）目標に関連付けられているポートフォリオの数。 <!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | ポートフォリオが属しているポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | 数値ポートフォリオ ID。 |
| [!UICONTROL Portfolio Spend Strategy] | （[!UICONTROL Portfolio Report]）ポートフォリオの支出戦略： <i>[!UICONTROL Daily]</i>, <i>[!UICONTROL Weekly]</i>, <i>[!UICONTROL Monthly]</i>, <i>[!UICONTROL ROI]</i>, <i>[!UICONTROL Day of week]</i>, <i>[!UICONTROL Day of month]</i>, <i>[!UICONTROL CPT]</i>, <i>[!UICONTROL Marginal CPT]</i>, <i>[!UICONTROL Google Target CPA]</i>、または <i>[!UICONTROL Google Target ROAS]</i>. |
| [!UICONTROL Portfolio Status] | ポートフォリオの状態：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集し、入札を最適化するためのデータをモデリングし、（最適化タイプとキャンペーン入札戦略に応じて）入札とキャンペーン予算の最適化を行います。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集しており、データをモデリングしていますが、入札やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポート目的で関連するキャンペーンのクリックデータを収集していますが、データのモデリングや、入札またはキャンペーン予算の最適化は行っていません。</li></ul> |
| [!UICONTROL Portfolio Target] | （[!UICONTROL Portfolio Report]）ポートフォリオの支出戦略の日別ターゲット。 毎日/毎月および曜日/月の戦略の場合、現在の日付のターゲットが表示されます。 |
| [!UICONTROL Preferred Devices] | （[!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yahoo! Japan Ads] キャンペーン）広告設定で優先するかどうか <i>[!UICONTROL Mobile ads]</i> または <i>[!UICONTROL All ads]</i>. |
| [!UICONTROL Product Group ID] | 広告ネットワークが製品グループに割り当てる数値 ID。 |
| [!UICONTROL Product Group Name] | 商品グループの名前。 |
| [!UICONTROL Product Group Status] | 商品グループのステータス。 |
| [!UICONTROL Product Groupings] | 親製品グループ。 |
| [!UICONTROL Product ID] | （[!UICONTROL Keyword Report]; [!DNL Google Ads] 製品リスト広告）広告と共に表示される製品の製品 ID。<br><br><b>注意：</b> ID は、製品リストにトラッキングパラメーターが含まれている場合にのみ取得されます `ev_plx=<GMC product ID>`（内で追加する必要があります） [!DNL Google Merchant Center]. |
| [!UICONTROL Raw Transaction Data] | （[!UICONTROL Transaction Report]） コンバージョン指標の売上高（1 件の登録に対して 1 件、12 米ドルの注文に対して 12 件など）。 複数の入札単位に同じ取引 ID がある場合、指定したクリック日（クリックデータが使用可能な場合）のクリック数に従ってトラッキング ID の売上高が分割されます。 |
| [!UICONTROL Reach] | （[!DNL Meta] キャンペーンのみ）広告を少なくとも 1 回表示したユーザーの数。 注意： [!DNL Meta] ユーザープロファイルのリーチを毎日重複排除するので、次の方法でレポートされる数になります。 [!DNL Meta] また、検索、ソーシャル、Commerceによって異なる場合があります。 |
| [!UICONTROL Region] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]）インプレッションまたはクリックが発生した地域または米国/カナダの州。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL SE Creative ID] | ネットワークによって割り当てられた広告 ID。 |
| [!UICONTROL Search (Abs. Top) IS] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）上位の絶対場所（オーガニック検索結果よりも上位の広告）で受け取ったインプレッション数を、上位の場所で受け取る資格のある推定インプレッション数で割った値。 10% 未満の割合は、「`<10%`「または」`0.0999`.」と入力します。 |
| [!UICONTROL Search (Top) IS] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）上位の場所（オーガニック検索結果の上）で受け取ったインプレッション数を、上位の場所で受け取る資格のある推定インプレッション数で割った値。 10% 未満の割合は、「`<10%`「または」`0.0999`.」と入力します。 |
| [!UICONTROL Search Engine] | 広告ネットワーク。 |
| [!UICONTROL Search exact match IS] | キーワードと完全に一致する検索で獲得したインプレッション数を、獲得資格のある完全一致の推定インプレッション数で割った値です。 この数値が低い場合は、入札が低すぎるか、広告の品質または関連性が低いことが原因である可能性があります。 |
| [!UICONTROL Search impr. share] | （[!DNL Google Ads] のみ）受信したインプレッション数を、インプレッションの推定数で割った値です。 10% 未満は「&lt;10%」と示され、90% を超える割合は「」と示されます`>90%`.」と入力します。 |
| [!UICONTROL Search lost abs. top IS (budget)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]） 1 日または 1 か月の予算が低すぎたので、オーガニック検索結果を超えて、広告が最初の広告ではなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「」と示されます`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search lost abs. top IS (rank)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）広告ランクが低いので、オーガニック検索結果を上回る、広告が最初の広告ではなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「」と示されます`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search lost IS (budget)] | （[!DNL Google Ads] のみ） 1 日または 1 か月の予算が低すぎたので広告が表示されなかった時間の割合。 この指標は、キャンペーンレベルでのみ使用できます。 90% を超える割合は、「`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search lost IS (rank)] | （[!DNL Google Ads] のみ）広告ランクが低いので広告が表示されなかった時間の割合。 90% を超える割合は、「`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search lost top IS (budget)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]） 1 日または 1 か月の予算が低すぎたので、広告がオーガニック検索結果の上に表示されなかった時間の割合。 の場合 [!DNL Google Ads] キャンペーン、90% を超える割合は「」と示されます`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search lost top IS (rank)] | （[!DNL Google Ads] および [!DNL [!DNL Microsoft Advertising]]）広告ランクが低いので、オーガニック検索結果から広告が表示されなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「」と示されます`>90%`「または」`0.9001`.」と入力します。 |
| [!UICONTROL Search Term] | （[!UICONTROL Transaction Report]） ユーザーがクエリを実行した検索語句。 |
| [!UICONTROL SETrackingOnly] | アカウントをトラッキングしているが入札を行っていないかどうか： <i>[!UICONTROL TRUE]</i> または <i>[!UICONTROL FALSE]</i>. |
| [!UICONTROL Site] | （ドメイン紹介報告書 [!UICONTROL Keyword Report]; site-targeted placements）クリックが発生したサイト。 |
| [!UICONTROL Start Date] | 報告された最初の日。 |
| [!UICONTROL State] | （地域配布レポート、 [!UICONTROL Keyword Report]）トランザクションが開始された状態。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Surfer ID] | （[!UICONTROL Transaction Report]）トランザクションを完了したユーザーの ID。 |
| [!UICONTROL Thru Plays] | （[!DNL Meta] キャンペーンのみ）広告全体を視聴したビューの数。 |
| [!UICONTROL Top of Page CPC] | （Google キャンペーンのみ）指定した日付範囲で検索結果ページの上部に表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Tracking URL] | （検索ターゲットキーワードのみ）トラッキングテンプレート、または（該当する場合）検索、ソーシャル、Commerceのトラッキングコードが埋め込まれた宛先 URL。 |
| [!UICONTROL Transaction Property Name] | （[!UICONTROL Transaction Report]）トランザクションのクレジット先となる、広告主固有のコンバージョン指標。 |
| [!UICONTROL Transaction Time] | （[!UICONTROL Transaction Report]）指定したコンバージョン指標がクレジットされた時間。 |
| [!UICONTROL Two Second Continuous Video Plays] | （[!DNL Meta] （キャンペーンのみ）ビデオが少なくとも 2 秒間連続して再生された回数。 |
| [!UICONTROL User Account Type] | 廃止 |
| [!UICONTROL User SE Account ID] | 検索、ソーシャルおよびCommerceが広告ネットワークに割り当てる数値 ID。 |
| [!UICONTROL Video Average Play Time] | （[!DNL Meta] キャンペーンのみ）単一のインプレッションに対してビデオが再生された平均時間（ビデオの再生に費やした時間を含む）。 |
| [!UICONTROL Video Plays] | （[!DNL Meta] キャンペーンのみ）再生を除く、ビデオの再生が開始された回数。 |
| [!UICONTROL Video Played at 25 Percent Count], [!UICONTROL Video Played at 50 Percent Count], [!UICONTROL Video Played at 75 Percent Count]、および [!UICONTROL Video Played at 100 Percent Count] | （ビデオ広告）再生されたビデオの数です。再生されたビデオの数は、全体の 25%、50%、75% または 100% です。 |
| [!UICONTROL VideoQuartile25Rate], [!UICONTROL VideoQuartile50Rate], [!UICONTROL VideoQuartile75Rate]、および [!UICONTROL VideoQuartile100Rate] | （ビデオ広告）再生されたビデオの割合は、25%、50%、75% または 100% です。 |
| [!UICONTROL View Rate] | （ビデオ広告）ビューまたはエンゲージメントの数を、広告の表示回数（ビデオおよびサムネールのインプレッション数）で割った値です。 |
| [!UICONTROL Views] | （ビデオ広告）訪問者が広告を視聴した回数、または広告にエンゲージした回数。 |
| [!UICONTROL ViewThroughConversions] | （オーディエンスネットワーク上の広告） 1 つ以上のインプレッションに起因したが、クリックに起因しないコンバージョンの数。 |

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [基本レポートと高度なレポートについて](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本レポートまたは詳細レポートの生成](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [基本的なレポート設定と高度なレポート設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
