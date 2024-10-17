---
title: 基本レポートと高度なレポートのレポート列
description: 基本レポートと高度なレポートで使用可能なデータ列について説明します。
exl-id: 649cdfa0-e6f2-4881-9f9d-8217e2547d99
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '3743'
ht-degree: 0%

---

# 基本レポートと高度なレポートのレポート列

| 列 | 説明 |
| ---- | ---- |
| \[ 広告主固有のカスタム （派生）指標\] | 既存の指標から計算された [ 作成したカスタム指標 ](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) の値。 |
| \[ 広告主固有のラベル分類\] | エンティティ レベルでエンティティに現在適用されているラベル分類。 複数のラベルの分類は、コンマ（,）で区切ります。 |
| \[ 広告主固有のコンバージョン指標\] | 指定したコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| \[Googleでトラッキングされたコンバージョン\] | 「GGL\*、GGL_CT\*、GGL_XD_CT\*」のエントリを参照してください。 |
| [!UICONTROL 7-Day Click Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない過去 7 日間（レポートで指定された日付範囲を除く）のクリック数予測の平均精度をパーセントで表したもの。 |
| [!UICONTROL 7-Day Cost Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない過去 7 日間（レポートで指定した日付範囲を除く）の原価予測の平均精度をパーセントで表したもの。 |
| [!UICONTROL 7-Day Revenue Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない過去 7 日間（レポートで指定された日付範囲を除く）の収益予測の平均精度をパーセントで表したもの。 |
| [!UICONTROL Account] | アカウント名。 |
| [!UICONTROL Account Status] | 検索、ソーシャル、Commerce内でのアカウントのステータス： <ul><li><i>[!UICONTROL Enabled]:</i> （デフォルト）同期された広告ネットワークの場合、検索、ソーシャルおよびCommerceは広告ネットワークアカウントにログインして、キャンペーンデータを取得できます。また、最適化やトラッキング生成などのその他の該当する機能も有効になります。<br><br> 同期されていない広告ネットワークの場合は、最適化やトラッキング生成など、該当する機能を使用できます。</li><li><i>[!UICONTROL Disabled]:</i> 同期された広告ネットワークの場合、検索、ソーシャル、Commerceは広告ネットワークアカウントにログインしないため、キャンペーンデータは取得されません。また、最適化やトラッキング生成など、その他の該当する機能は無効になっています。 アカウントが有効になっている間に収集されたデータは、引き続き保存されますが、すべてのキャンペーン管理ビューおよび今後作成するすべてのレポートには、アカウントが無効になっている期間のデータは含まれません。<br><br> 同期されていない広告ネットワークでは、最適化やトラッキングの生成など、該当する機能を使用できません。</li></ul> |
| [!UICONTROL Active Ad Groups] | アクティブな広告グループの数。 |
| [!UICONTROL Active Ads/Creatives] | アクティブな広告/クリエイティブの数。 |
| [!UICONTROL Active Campaigns] | アクティブなキャンペーンの数。 |
| [!UICONTROL Active Keywords] | アクティブなキーワードの数。 |
| [!UICONTROL Ad Group] | 広告グループ。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意の ID。 |
| [!UICONTROL Ad Group Status] | 広告グループのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Type] | 広告グループタイプ。<i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ）、<i>[!UICONTROL Discovery]</i> （ディスカバリーキャンペーンのみ）、<i>[!UICONTROL Display]</i> （ディスプレイキャンペーンのみ）、<i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、<i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ）、<i>[!UICONTROL Shopping Showcase]</i>、<i>[!UICONTROL Shopping Product]</i> （標準ショッピングキャンペーンのみ）、<i>[!UICONTROL Shopping Smart]</i> （スマートショッピングキャンペーンのみ）などがあります。 一部のキャンペーンタイプでは、1 つのキャンペーンに複数の広告タイプを含めることができます。 |
| [!UICONTROL Ad Groups] | ラベル値が割り当てられる広告グループの数。 |
| [!UICONTROL AD Name] | 広告グループ名。[!UICONTROL Ad Group] と同じ値。 |
| [!UICONTROL Ad Recall Lift] | （[!DNL Meta] キャンペーンのみ） 2 日以内に広告を覚えている推定ユーザー数。 |
| [!UICONTROL Ad Recall Rate] | （[!DNL Meta] キャンペーンのみ） 2 日以内に広告を覚えている推定ユーザー数を、到達したユーザー数で割ったパーセンテージ。 |
| [!UICONTROL Ad Size] | 広告のディメンション。 |
| [!UICONTROL AD Strength] | （レスポンシブ検索広告に [!DNL Google Ads]）広告の有効性：<i>[!UICONTROL average]</i>、<i>[!UICONTROL excellent]</i>、<i>[!UICONTROL good]</i>、<i>[!UICONTROL no_ads]</i>、<i>[!UICONTROL pending]</i>、<i>[!UICONTROL poor]</i>、<i>[!UICONTROL unknown]</i> または <i>[!UICONTROL unspecified]</i>。 |
| [!UICONTROL Adgroup MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] キャンペーン）現在の広告グループレベルのモバイル入札調整。モバイルデバイスに広告を表示する際の入札調整方法を決定します。 |
| [!UICONTROL Advertiser] | 広告主名。 |
| [!UICONTROL Advertiser ID] | 広告主の検索、ソーシャル、Commerce アカウントの数値 ID。 |
| [!UICONTROL Avg Position] | 指定した日付範囲での広告の平均位置。<br><br>[!DNL Google Ads] および [!DNL Yahoo! Japan Ads] キャンペーンの場合、このデータは 2019 年 9 月までのみ利用できます。 [!DNL Microsoft Advertising] の場合、このデータは 2021 年 1 月 22 日（PT）までのみ使用できます。 |
| [!UICONTROL Base URL] | キャンペーンまたはアカウントに設定された追加パラメーターを含む、キーワードのベース URL。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれません。 |
| [!UICONTROL Bid Strategy] | （ほとんどの広告ネットワーク）キャンペーンまたはキャンペーンコンポーネントの場合、これはキャンペーンの入札戦略です。 管理者アカウントにリンクされている広告ネットワークアカウントの場合、これはクロスアカウント入札戦略です。 使用可能な値は、広告ネットワークによって異なります。 |
| [!UICONTROL Business Name] | （[!DNL Microsoft Advertising] レスポンシブ広告） ビジネス名。 |
| [!UICONTROL Call to Action] | （レスポンシブ広告とマルチメディア広告の [!DNL Microsoft Advertising]）広告に含まれるコールトゥアクション。 |
| [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Campaign Budget] | キャンペーン予算。 |
| [!UICONTROL Campaign MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] のキャンペーン）現在のキャンペーンレベルのモバイル入札調整。モバイルデバイスに広告を表示する際の入札調整方法を決定します。 |
| [!UICONTROL Campaign Product Scope Filter] | （ショッピングネットワークを使用したキャンペーンのみ）キャンペーンに対して商品広告を作成できる、マーチャントアカウント内の商品。 |
| [!UICONTROL Campaign Start Date] | キャンペーンの入札が行われた/または行われた最初の日。 |
| [!UICONTROL Campaign Status] | キャンペーンステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Ended]</i>、<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Campaign Type] | キャンペーンのタイプ（<i>[!UICONTROL Audience (Ctv Video)]</i><i>[!UICONTROL Audience (Feed)]</i>、<i>[!UICONTROL Audience (Image)]</i>、<i>[!UICONTROL Audience (Video)]</i>、<i>[!UICONTROL Brand Shopping]</i>、<i>[!UICONTROL Discovery]</i>、<i>[!UICONTROL Search and Display]</i>、<i>[!UICONTROL Standard Display]</i>、<i>[!UICONTROL Standard Performance Max]</i>、<i>[!UICONTROL Standard Search]</i>、<i>[!UICONTROL Standard Shopping]</i>、<i>[!UICONTROL Store Ad]</i>、<i>[!UICONTROL Video]</i>、<i>[!UICONTROL Others]</i> など）。 |
| [!UICONTROL Channel Type] | マーケティングチャネルのタイプ：<i>[!UICONTROL Search]</i> または <i>[!UICONTROL Content]</i>。 レポート設定のレポート [!UICONTROL Search/Content] 設定が「[!UICONTROL Combined]」の場合、この列は含まれません。 |
| [!UICONTROL City] | （[!UICONTROL Geo Distribution Report]、[!UICONTROL Transaction Report]） クリックが発生した都市。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Click Match Type] | クリックされた広告のキーワード一致タイプ。 これは、複数の一致タイプを持つ [!DNL Microsoft Advertising] キーワードを除き、[!UICONTROL Listing Match Type] と同じです。 [!DNL Microsoft Advertising] のキーワードの場合、これは、実際にクリックされた一致タイプです。 |
| [!UICONTROL Click Value] | （[!UICONTROL Portfolio Report]） ポートフォリオの目的に指定されたクリックの値。 |
| [!UICONTROL Click/Impression Time] | （[!UICONTROL Transaction Report]）変換の原因となったクリックまたはインプレッションが発生した時間。 |
| [!UICONTROL Clicks] | 指定した日付範囲内での広告のクリック数。 |
| [!UICONTROL Client ID1], [!UICONTROL Client Id 1] | （[!UICONTROL Keyword Report]、[!UICONTROL Ad Variation Report] および [!UICONTROL Transaction Report]、フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Id 2] | （[!UICONTROL Keyword Report] および [!UICONTROL Transaction Report]、フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Transaction ID] | （[!UICONTROL Transaction Report]）一意のトランザクション ID。 |
| [!UICONTROL Constraint End Date] | （[!UICONTROL Constraint Report]）制約がアクティブである最終日。 |
| [!UICONTROL Constraint Name] | （[!UICONTROL Constraint Report]）制約名。 |
| [!UICONTROL Constraint Start Date] | （[!UICONTROL Constraint Report]）制約が有効になる最初の日。 |
| [!UICONTROL Constraint Status] | （[!UICONTROL Constraint Report]）制約の状態：<i>[!UICONTROL Active]</i> または <i>[!UICONTROL Paused]</i>。 |
| [!UICONTROL Constraint Type] | （[!UICONTROL Constraint Report]）制約のタイプ：<i>[!UICONTROL Bid/Pos Constraint]</i>、<i>[!UICONTROL Bid Shift]</i>、<i>[!UICONTROL Campaign Budget]</i>、<i>[!UICONTROL Context Sensitive Bid]</i>、<i>[!UICONTROL Incremental Bidding]</i>、<i>[!UICONTROL Max CPA]</i>、<i>[!UICONTROL Min Margin]</i>、<i>[!UICONTROL Variable Bid Position]</i>、<i>[!UICONTROL Search Engine Min Bid]</i> または <i>[!UICONTROL Variable Position]</i>。 |
| [!UICONTROL Constraints] | エンティティに適用可能な制約の名前（コンマで区切る）。 |
| [!UICONTROL Content IS] | ディスプレイ/オーディエンスネットワークの広告で獲得したインプレッション数を、インプレッション数の推定値で割った値です。 [!DNL Microsoft Advertising] では、これは「[!UICONTROL Audience IS]」と呼ばれます。 |
| [!UICONTROL Content IS Lost (budget)] | 1 日または 1 か月の予算が低すぎたので、ディスプレイ/オーディエンスネットワークの広告で獲得できなかった推定インプレッション数の割合です。 [!DNL Microsoft Advertising] では、これは「[!UICONTROL Audience lost IS (budget)]」と呼ばれます。 |
| [!UICONTROL Content IS Lost (rank)] | 広告ランクが低いので、ディスプレイ/オーディエンスネットワークの広告で獲得した推定インプレッション数の割合は表示されませんでした。 [!DNL Microsoft Advertising] では、これは「[!UICONTROL Audience lost IS (rank)]」と呼ばれます。 |
| [!UICONTROL Conversion Type] | （[!UICONTROL Transaction Report]）変換の前に行った操作：<ul><li><i>[!UICONTROL Click:]</i> コンバージョン前に少なくとも 1 回の有料クリックが発生しました。</li><li><i>[!UICONTROL Impression:]</i> コンバージョン前に有料クリックが発生していなかったので、コンバージョンはビュースルー（有料クリックのないインプレッション）の結果となりました。</li></ul> |
| [!UICONTROL Cost] | 指定した日付範囲の広告の合計コスト。 |
| [!UICONTROL Country] | （[!UICONTROL Geo Distribution Report]、[!UICONTROL Keyword Report]） クリックが発生した国。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL CPC] | 指定した日付範囲内の広告に関するクリック単価（CPC）。 |
| [!UICONTROL Creative Base URL] | キャンペーンまたはアカウント用に設定された追加パラメーターを含む、広告のベース URL。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれません。 |
| [!UICONTROL Creative Destination URL] | 広告の最終的な URL または宛先 URL （トラッキングパラメーターを含む）。 |
| [!UICONTROL Creative Name] | （[!DNL Yahoo! Japan] のみ）広告イメージ名。 |
| [!UICONTROL Creative Title]、[!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 広告のタイトルまたはヘッドライン。 必須タイトル行とオプションタイトル行の数はクリエイティブタイプによって異なります。 [!DNL Microsoft Advertising] のレスポンシブ広告またはマルチメディア広告で [!UICONTROL Creative Title4] 以上の列を表示するには、レポート設定に「[!UICONTROL Creative Titles]」列を含めます。 |
| [!UICONTROL Creative Titles] | （マルチメディアおよびレスポンシブ検索広告のみ）広告の短いヘッドラインごとに列を追加します（「[!UICONTROL Creative Title]」から「[!UICONTROL Creative Title15]」）。 この列を含める場合、他の [!UICONTROL Creative Title] の列を含める必要はありませんが、[!UICONTROL Creative Title] ではなく [!UICONTROL Creative Titles] で並べ替えるように [!UICONTROL Order Results/Limit Rows By] セクションを編集します。 |
| [!UICONTROL Creative Type] | 広告の形式。 <i>[!UICONTROL App Install Ad]</i>、<i>[!UICONTROL Call Only Ad]</i>、<i>[!UICONTROL Discovery Ad (single-image ads)]</i>、<i>[!UICONTROL Discovery Carousel Ad]</i> （マルチ画像カルーセル広告）、<i>[!UICONTROL Display Ad]</i>、<i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Legacy Text Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i>、<i>[!UICONTROL Responsive Ad]</i>、<i>[!UICONTROL Responsive Search Ad]</i>、<i>[!UICONTROL Text Ad]</i> のいずれかの値を使用できます。 |
| [!UICONTROL CTR] | クリックスルー率（クリック数を、含まれる広告のインプレッション数で割った値）。 |
| [!UICONTROL Currency] | 該当する通貨タイプ（「USD」や「GBP」など）。<br><br><b> 注意：</b> 異なる通貨を使用する勘定科目のデータがレポートに含まれる場合、通貨に関係なく、金額の「[!UICONTROL Total]」値は単に列のすべての数値の合計になります。 |
| [!UICONTROL Current Bid] | ターゲットに対する現在の入札。 |
| [!UICONTROL Current First Page Bid] | （[!DNL Google Ads] キャンペーンのみ） [!DNL Google] しい検索クエリがキーワードと一致する場合に、検索結果の最初のページに広告を表示するために現在必要な推定クリック単価（CPC）入札。<br><br> 単一のキーワードと一致タイプの組み合わせの場合、この値は、その組み合わせに現在必要な最初のページの入札です。 複数のキャンペーンで同じキーワードと一致タイプの組み合わせを使用する場合、この値は、現在すべてのインスタンスで必要な最初のページの最小入札額になります。 |
| [!UICONTROL Current Quality Score] | （[!DNL Google Ads] キャンペーンおよび [!DNL Microsoft Advertising] キャンペーンのみ）広告ネットワークで指定された、キーワードまたは入札単位の現在の品質スコア。 範囲は 1 （低）から 10 （完全）です。 単一のキーワードと一致タイプの組み合わせの場合、この値はその組み合わせの現在のスコアです。 複数のキャンペーンで同じキーワードと一致タイプの組み合わせを使用する場合、この値は、すべてのインスタンス間の現在の最大スコアです。<br><br> 広告ネットワークでは、品質スコアを使用して入札価格と広告ポジションを判断します。 これは、関連する広告やユーザーの検索クエリ、ランディングページの品質に対するキーワードの関連性など、多くの要因に従って計算されます。 [!DNL Google Ads] のキーワードについては、キーワードのクリックスルー率も考慮され、[!DNL Microsoft Advertising] のキーワードについては、ランディングページから提供されるユーザーエクスペリエンスも考慮されます。 |
| [!UICONTROL Custom Bid Level] | （ディスプレイネットワークを対象とするGoogle キャンペーンのみ）入札のレベルは、<i>[!UICONTROL Ad Group]</i>、<i>[!UICONTROL Age]</i>、<i>[!UICONTROL Gender]</i>、<i>[!UICONTROL Interest and List]</i>、<i>[!UICONTROL Keyword]</i>、<i>[!UICONTROL Placement]</i>、<i>[!UICONTROL Vertical]</i>、<i>[!UICONTROL None]</i> または <i>[!UICONTROL Unknown]</i> です。 |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 広告の本文。 必須の説明行とオプションの説明行の数は、クリエイティブタイプによって異なります。 レスポンシブ広告またはマルチメディア広告で [!UICONTROL Description3] 列および [!UICONTROL Description4] 列 [!DNL Microsoft Advertising] 表示するには、レポート設定に「[!UICONTROL Descriptions]」列を含めます。 |
| [!UICONTROL Descriptions] | （レスポンシブ広告とマルチメディア広告の [!DNL Microsoft Advertising]）広告の説明行ごとに列を追加します（「[!UICONTROL Description1]」から「[!UICONTROL Description4]」）。 この列を含める場合、他の [!UICONTROL Description] の列を含める必要はありません。 |
| [!UICONTROL Device] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads] および [!DNL Yahoo Native] キャンペーン）広告が表示されたデバイスタイプ：<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i> または <i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値は N/A です。<br><br> 検索キャンペーンでは、広告がクリックされた時点で、キーワード、広告、広告拡張機能のトラッキングテンプレートまたは宛先 URL にデバイス別データを追跡するパラメーター（`&ev_dvc={device}&ev_dvm={devicemodel}`）が含まれている場合、各デバイスタイプの行にもコンバージョンデータが含まれます。 そうでない場合、コンバージョンデータをデバイスタイプに関連付けることができない場合は、「[!UICONTROL Device]」の値が [!UICONTROL N/A] の別の行に集計されます。 |
| [!UICONTROL Display Path 1] | （拡張テキスト広告の [!DNL Google Ads] み）広告のベース URL の後の最初の表示パス。 |
| [!UICONTROL Display Path 2] | （拡張テキスト広告の [!DNL Google Ads] み）広告のベース URL の後の 2 番目の表示パス。 |
| [!UICONTROL Display Type] | 廃止 |
| [!UICONTROL Display URL] | 広告の表示 URL （エンドユーザーに表示される URL）。 |
| [!UICONTROL DMA] | （[!UICONTROL Geo Distribution Report]、[!UICONTROL Keyword Report]）クリックが発生した、数値で指定されたマーケットエリア（Denver の場合は 751 など）。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Domain] | （[!UICONTROL Domain Referral Report]、[!UICONTROL Keyword Report]）クリックが発生したドメイン名。 |
| [!UICONTROL eCPM] | 有効 CPM、つまり指定した日付範囲内の 1000 インプレッションあたり支払われた平均費用。 eCPM の値は、CPM または CPC キャンペーンに対して計算されます。 |
| [!UICONTROL EF Campaign ID] | 検索、ソーシャルおよびCommerceがキャンペーンに割り当てる数値 ID。 |
| [!UICONTROL EF ID] | （[!UICONTROL Transaction Report]）（Adobe Advertisingコンバージョントラッキングサービスを利用する広告主及びトークンを利用する「[!UICONTROL EF Redirect]」トラッキング方式） クリック又はコンバージョンのトークン。<ul><li>[!DNL Google Ads] 検索広告の場合、EF ID は `{gclid}:G:s` です。これには、Googleのクリック ID （GCLID）とネットワークタイプ（検索用の「s」）が含まれます。</li><li> [!DNL Microsoft Advertising] 検索広告の場合、EF ID は `{msclkid}:G:s` です。これには、Microsoftのクリック ID （MSCLKID）とネットワークタイプ（検索用は「s」）が含まれます。</li><li>他の広告ネットワークでの検索広告の場合、EF ID にはサーファー ID、クリック時間、ネットワークタイプが含まれます。</li><li>ディスプレイ広告の場合、EF ID にはサーファー ID、クリックまたはインプレッション時間、ネットワークタイプが含まれます。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | （[!UICONTROL Geo Distribution Report]：検索、ソーシャル、Commerceでの使用のみ）地理的な場所の内部 ID。データの正規化に使用されます。 |
| [!UICONTROL EF Portfolio Group ID] | ポートフォリオが属しているポートフォリオグループの数値 ID。 |
| [!UICONTROL EF Search Engine ID] | 検索、ソーシャル、およびCommerceによって広告ネットワークに割り当てられる数値 ID。[!DNL Google Ads] の場合は <i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising] の場合は <i>[!UICONTROL 10]</i>、[!DNL Meta] の場合は <i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]<i>[!UICONTROL 87]</i> の場合は <i>[!UICONTROL 86]</i>、[!DNL Naver] の場合は <i>[!UICONTROL 88]</i>、[!DNL Baidu] の場合は <i>[!UICONTROL 90]</i> [!DNL Yandex]、[!DNL Yahoo! Japan Ads] の場合は <i>[!UICONTROL 94]</i>、[!DNL Yahoo Native] の場合は <i>[!UICONTROL 105]</i>、[!DNL Pinterest] の場合は <i>[!UICONTROL 106]</i> （非推奨）です。 |
| [!UICONTROL End Date] | 最後に報告された日。 |
| [!UICONTROL Engagement Rate] | （ビデオ広告）エンゲージメント数を、広告の表示回数で割った値。 |
| [!UICONTROL Engagements] | （ビデオ広告）ユーザーが広告を 10 秒以上視聴した回数、または広告が 10 秒未満の場合は広告全体を視聴した回数。 |
| [!UICONTROL Est. Clicks] | （[!UICONTROL Geo Distribution Report]：検索および表示キャンペーンのみ）広告グループ/キャンペーン/ポートフォリオの組み合わせの推定クリック数。 この値は、広告ネットワークで指定される値とは異なる場合があります。 |
| [!UICONTROL Estimated Cost] | 検索、ソーシャルおよびCommerceで追跡した関連広告の推定コストの合計。 この値は、広告ネットワークで指定される値とは異なる場合があります。 |
| [!UICONTROL Estimated Impressions] | （キャンペーンの表示のみ）検索、ソーシャル、Commerceでトラッキングした広告インプレッションの推定数。 この値は、広告ネットワークによって提供された値を示す「[!UICONTROL Impressions]」列（使用可能な場合）の値とは異なる場合があります。 |
| [!UICONTROL Exclude (yes/no)] | 一致する製品の広告に入札を除外するか（<i>[!UICONTROL Yes]</i>）、または入札を許可するか（<i>[!UICONTROL No]</i>）を指定します。 |
| [!UICONTROL First Page CPC] | （Google キャンペーンのみ）指定した日付範囲に検索結果の最初のページに表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Frequency] | （[!DNL Meta] キャンペーンのみ）訪問者が広告を表示した平均回数。 |
| `GGL*`、`GGL_CT*`、`GGL_XD_CT*` [[!DNL Google Ads]-tracked conversions] | （検索およびショッピングネットワーク上のキャンペーンを [!DNL Google Ads] 照） [!DNL Google Ads] 追跡コンバージョンと、各コンバージョンに対する最大 3 つの個別の指標：<ul><li>`GGL*` — （追跡する場合）「GGL」プレフィックスで始まるキーワードのコンバージョン値（GGL 購入など）。</li><li>`GGL_CT*` — 「GGL_CT」プレフィックス（GGL_CT_Purchase など）で始まるコンバージョンの数（カウント）。</li><li>`GGL_XD_CT*` — （コンバージョンタイプに使用可能な場合は、追跡時） クロスデバイスコンバージョンの数（カウント）。「GGL_XD_CT_」プレフィックス （GGL_XD_CT_Purchase など）で始ま [!DNL Google Ads] て測定されます。</li></ul><br> 各コンバージョンは入札単位とクリック日で記録されます。イベントレベルでは使用できません。 [!DNL Google Ads] でトラッキングされるコンバージョンについて詳しくは、「[[!DNL Google Ads]  検索、ソーシャル、Commerceのコンバージョンデータ ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」を参照してください。 |
| [!UICONTROL Impr. (Abs. Top) %] | （[!DNL Google Ads] のみ）オーガニック検索結果の上に最初の広告として表示される広告インプレッションの割合。 |
| [!UICONTROL Impr. (Top) %] | （[!DNL Google Ads] のみ）オーガニック検索結果の上に表示される広告インプレッションの割合。 |
| [!UICONTROL Impressions] | 指定した日付範囲内の広告インプレッション数。 |
| [!UICONTROL Interaction Rate] | （ビデオ広告）インタラクション数を広告の表示回数（ビデオおよびサムネールのインプレッション数）で割った値です。 |
| [!UICONTROL Interactions] | （ビデオ広告）訪問者が広告を視聴した回数。 |
| [!UICONTROL Is_Click_Objectives] | （[!UICONTROL Portfolio Report]） <i>true</i>[!UICONTROL Maximize Clicks] に設定した入札戦略を持つキャンペーンがポートフォリオに含まれている場合）、および <i>false</i> に設定されていない場合。 |
| [!UICONTROL Keyword] | キーワード。<br><br><b> メモ：</b> レポートにコンテンツ対応の検索キャンペーンの広告グループのデータが含まれる場合、この列には「（広告グループコンテンツ）広告グループ名」などの該当する広告グループ名が含まれます。 検索キャンペーンでサイトをターゲットにしたプレースメントの場合、この列には値がありません。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意の ID。 |
| [!UICONTROL Keyword Status] | 検索語句が一致したキーワードのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>、<i>[!UICONTROL Disapproved]</i>。 |
| [!UICONTROL Label Classification] | （[!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]） ラベルの分類。 |
| [!UICONTROL Label Value] | （[!UICONTROL Label Classification Report] および [!UICONTROL Label Value Report]） ラベル分類の値。 |
| [!UICONTROL Language] | （キャンペーンを表示）ターゲットオーディエンスの言語。 |
| [!UICONTROL Link Type] | （[!UICONTROL Keyword Report]、[!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンのみ。データを使用できるのは、レポートに指定したアトリビューションルールが「最終イベント」の場合のみです）行が（広告自体ではなく）広告拡張機能または製品/ショッピング広告のクリックによるコンバージョンをレポートする場合、この列には、クリックされたリンクのタイプとタイトルが表示されます。<ul><li>`pla:*` – 製品広告は、「pla:8525822」のように `pla:<product ID>` のように表示されます。</li><li>`sl:*` - 「sl:See Current Offers」のように、サイトリンクは `sl:<Sitelink text>` として表示されます。</li></ul> |
| [!UICONTROL Listing Match Type] | 広告リストのキーワード一致タイプ、コンテンツターゲットキャンペーンの広告の <i>[!UICONTROL Content]</i>、サイトターゲットキャンペーンのプレースメントの <i>[!UICONTROL Sitecpc]</i>。 [!DNL Microsoft Advertising] のキーワードには、複数の一致タイプ（「[!UICONTROL Broad],[!UICONTROL Exact]」など）が含まれる場合があります。 |
| [!UICONTROL Location] | （ディスプレイキャンペーン）ターゲットオーディエンスの場所。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | （レスポンシブ広告とマルチメディア広告 [!DNL Microsoft Advertising] 完了したレポート行で）広告の長いヘッドライン。 これらの列を表示するには、レポート設定に「[!UICONTROL Long Creative Titles]」列を含めます。 |
| [!UICONTROL Long Creative Titles] | （レスポンシブ広告 [!DNL Microsoft Advertising] マルチメディア広告の場合）広告の長いタイトルごとに列を追加します（「[!UICONTROL Long Creative Title1]」から「[!UICONTROL Long Creative Title5]」）。 |
| [!UICONTROL Market Type] | マーケットタイプ：<i>[!UICONTROL search]</i> または <i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | （[!UICONTROL ROI]、[!UICONTROL CPT] または [!UICONTROL Marginal Cost per Transaction] の支出戦略を持つポートフォリオ内のキャンペーン）ポートフォリオの 1 日の最大予算目標。 |
| [!UICONTROL Max Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワークに対して設定されているポートフォリオの支出の最大割合。 制約タイプ「[!UICONTROL Min-Max]」を使用するポートフォリオの場合、これは [!UICONTROL Max %] 値です。 制約タイプ「[!UICONTROL Target Spend]」を使用するポートフォリオの場合、これは [!UICONTROL Target Spend] 値です。 |
| [!UICONTROL Method ID] | （[!UICONTROL Portfolio Report]） |
| [!UICONTROL Metro Code] | （[!UICONTROL Geo Distribution Report]、[!UICONTROL Keyword Report]）インプレッション数またはクリック数の発生元となった数値のメトロコード（Denver の場合は us-751 など）。 これは、検索ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Min Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワークに対して設定されているポートフォリオ支出の最小割合。 制約タイプ「[!UICONTROL Min-Max]」を使用するポートフォリオの場合、[!UICONTROL Min %] が設定されている場合、これは [!UICONTROL Min %] 値です。 制約タイプ「[!UICONTROL Target Spend]」を使用するポートフォリオの場合、これは [!UICONTROL Target Spend] 値です。 |
| [!UICONTROL Network Account ID] | ネットワークによって割り当てられたアカウント ID。 |
| [!UICONTROL Network Ad Group ID] | ネットワークによって割り当てられた広告グループ ID。 |
| [!UICONTROL Network Campaign ID] | ネットワークによって割り当てられたキャンペーン ID。 |
| [!UICONTROL Network Campaign Objective] | （[!DNL Meta] キャンペーンのみ）キャンペーンの目的。 |
| [!UICONTROL Objective Name] | ポートフォリオの目的。 |
| [!UICONTROL Objective Value] | ポートフォリオの現在の目標に従って計算された、重み付けされたコンバージョンの合計。 |
| [!UICONTROL Objective Value Calculation] | 目標値を導き出すために使用される計算。 |
| [!UICONTROL Outbound Clicks] | （[!DNL Meta] キャンペーンのみ） [!DNL Meta] 所有プロパティからユーザーを離す広告内のリンクのクリック数。 |
| [!UICONTROL Parent Product Groupings] | 該当する場合は、階層間の `>>` を含む親製品グループの完全な階層（`All Products>>CategoryL1=Animals` など）。 |
| [!UICONTROL Partition Type] | 商品グループのタイプ：<i>[!UICONTROL Sub-Division]</i> （親商品グループ）または <i>[!UICONTROL Unit]</i> （入札がある子商品グループの最下位レベル）。 |
| [!UICONTROL Path Position] | （[!UICONTROL Transaction Report]）コンバージョンパス内のイベントの位置。 |
| [!UICONTROL Path Total] | （[!UICONTROL Transaction Report]） パス位置のイベントの合計数。 |
| [!UICONTROL Portfolio] | ポートフォリオ。 |
| [!UICONTROL Portfolio Count] | （[!UICONTROL Portfolio Report]）目的に関連付けられているポートフォリオの数。<!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | ポートフォリオが属しているポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | 数値ポートフォリオ ID。 |
| [!UICONTROL Portfolio Spend Strategy] | （[!UICONTROL Portfolio Report]） ポートフォリオの支出戦略：<i>[!UICONTROL Daily]</i>、<i>[!UICONTROL Weekly]</i>、<i>[!UICONTROL Monthly]</i>、<i>[!UICONTROL ROI]</i>、<i>[!UICONTROL Day of week]</i>、<i>[!UICONTROL Day of month]</i>、<i>[!UICONTROL CPT]</i>、<i>[!UICONTROL Marginal CPT]</i>、<i>[!UICONTROL Google Target CPA]</i> または <i>[!UICONTROL Google Target ROAS]</i>。 |
| [!UICONTROL Portfolio Status] | ポートフォリオの状態：<ul><li><i>[!UICONTROL Optimize]:</i> 最適化機能は、関連するキャンペーンのクリック数および売上高データを収集し、最適化に使用されるデータをモデリングして、最適化のタイプと入札戦略に応じて、入札、キャンペーン予算およびキャンペーン入札戦略のターゲットを最適化します。</li><li><i>[!UICONTROL Active]:</i> 最適化機能は、関連するキャンペーンのクリック数と売上高のデータを収集しており、データをモデリングしていますが、入札やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i> 最適化機能は、レポート目的で関連するキャンペーンのクリックデータを収集していますが、データのモデリングや、入札またはキャンペーン予算の最適化は行っていません。</li></ul> |
| [!UICONTROL Portfolio Target] | （[!UICONTROL Portfolio Report]）ポートフォリオの支出戦略の日別目標。 毎日/毎月および曜日/月の戦略の場合、現在の日付のターゲットが表示されます。 |
| [!UICONTROL Preferred Devices] | （[!DNL Google Ads]、[!DNL Microsoft Advertising] および [!DNL Yahoo! Japan Ads] キャンペーン）広告設定で <i>[!UICONTROL Mobile ads]</i> が優先されるか、<i>[!UICONTROL All ads]</i> が優先されるか。 |
| [!UICONTROL Product Group ID] | 広告ネットワークが製品グループに割り当てる数値 ID。 |
| [!UICONTROL Product Group Name] | 商品グループの名前。 |
| [!UICONTROL Product Group Status] | 商品グループのステータス。 |
| [!UICONTROL Product Groupings] | 親製品グループ。 |
| [!UICONTROL Product ID] | （[!UICONTROL Keyword Report]：広告 [!DNL Google Ads] 表示する製品）広告と共に表示される製品の製品 ID。<br><br><b> メモ：</b> ID は、製品リストにトラッキングパラメーター `ev_plx=<GMC product ID>` が含まれている場合にのみ取得され、[!DNL Google Merchant Center] 内で追加する必要があります。 |
| [!UICONTROL Raw Transaction Data] | （[!UICONTROL Transaction Report]）コンバージョン指標の売上高（1 つの登録に対して 1 件、12 米ドルの注文に対して 12 件など）。 複数の入札単位に同じ取引 ID がある場合、指定したクリック日（クリックデータが使用可能な場合）のクリック数に従ってトラッキング ID の売上高が分割されます。 |
| [!UICONTROL Reach] | （[!DNL Meta] キャンペーンのみ）広告を少なくとも 1 回表示したユーザーの数。 メモ：[!DNL Meta] はユーザープロファイルのリーチの重複を毎日排除するので、[!DNL Meta] でレポートされる数や検索、ソーシャル、Commerceでレポートされる数は異なる場合があります。 |
| [!UICONTROL Region] | （[!UICONTROL Geo Distribution Report]、[!UICONTROL Keyword Report]）インプレッション数またはクリック数の発生源となる地域または米国/カナダの州。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL SE Creative ID] | ネットワークによって割り当てられた広告 ID。 |
| [!UICONTROL Search (Abs. Top) IS] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）最上位の絶対位置（オーガニック検索結果よりも上位にある最初の広告）で獲得したインプレッション数を、最上位の位置で獲得できる推定インプレッション数で割った値。 10% 未満の割合は、「`<10%`」または「`0.0999`」と示されます。 |
| [!UICONTROL Search (Top) IS] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）上位の場所（オーガニック検索結果の上）で受け取ったインプレッション数を、上位の場所で受け取る資格のある推定インプレッション数で割った値。 10% 未満の割合は、「`<10%`」または「`0.0999`」と示されます。 |
| [!UICONTROL Search Engine] | 広告ネットワーク。 |
| [!UICONTROL Search exact match IS] | キーワードと完全に一致する検索で獲得したインプレッション数を、獲得資格のある完全一致の推定インプレッション数で割った値です。 この数値が低い場合は、入札が低すぎるか、広告の品質または関連性が低いことが原因である可能性があります。 |
| [!UICONTROL Search impr. share] | （[!DNL Google Ads] のみ）受け取ったインプレッション数を、受け取る資格のあるインプレッションの推定数で割った値です。 10% 未満は「&lt;10%」と表示され、90% を超える割合は「`>90%`」と表示されます。 |
| [!UICONTROL Search lost abs. top IS (budget)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]） 1 日または 1 か月の予算が低すぎたので、オーガニック検索結果を上回る最初の広告が広告でなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search lost abs. top IS (rank)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]）広告ランクが低いので、広告がオーガニック検索結果を上回る最初の広告ではなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search lost IS (budget)] | （[!DNL Google Ads] のみ） 1 日または 1 か月の予算が低すぎたので広告が表示されなかった時間の割合。 この指標は、キャンペーンレベルでのみ使用できます。 90% を超える割合は、「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search lost IS (rank)] | （[!DNL Google Ads] のみ）広告ランクが低いので広告が表示されなかった時間の割合。 90% を超える割合は、「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search lost top IS (budget)] | （[!DNL Google Ads] および [!DNL Microsoft Advertising]） 1 日または 1 か月の予算が低すぎたので、オーガニック検索結果を超えて広告が表示されなかった時間の割合。 [!DNL Google Ads] キャンペーンの場合、90% を超える割合は「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search lost top IS (rank)] | （[!DNL Google Ads] および [!DNL [!DNL Microsoft Advertising]]）広告ランクが低いので、オーガニック検索結果を超えて広告が表示されなかった時間の割合。 Google広告キャンペーンの場合、90% を超える割合は「`>90%`」または「`0.9001`」と示されます。 |
| [!UICONTROL Search Term] | （[!UICONTROL Transaction Report]） ユーザーがクエリを実行した検索語句。 |
| [!UICONTROL SETrackingOnly] | アカウントをトラッキングしているが入札を行っていないかどうか：<i>[!UICONTROL TRUE]</i> または <i>[!UICONTROL FALSE]</i>。 |
| [!UICONTROL Site] | （Domain Referral Report and [!UICONTROL Keyword Report]; site-targeted placements） クリックの元となったサイト。 |
| [!UICONTROL Start Date] | 報告された最初の日。 |
| [!UICONTROL State] | （地域配布レポート、[!UICONTROL Keyword Report]）トランザクションが開始された状態。 これは、ユーザーの IP アドレスから決定されます。 |
| [!UICONTROL Surfer ID] | [!UICONTROL Transaction Report] 取引をした利用者の ID |
| [!UICONTROL Thru Plays] | （[!DNL Meta] キャンペーンのみ）広告全体を視聴したビューの数。 |
| [!UICONTROL Top of Page CPC] | （Google キャンペーンのみ）指定した日付範囲で検索結果ページの上部に表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Tracking URL] | （検索ターゲットキーワードのみ）トラッキングテンプレート、または（該当する場合）検索、ソーシャル、Commerceのトラッキングコードが埋め込まれた宛先 URL。 |
| [!UICONTROL Transaction Property Name] | （[!UICONTROL Transaction Report]）取引のクレジットを付与する広告主固有のコンバージョン指標。 |
| [!UICONTROL Transaction Time] | （[!UICONTROL Transaction Report]）特定のコンバージョン指標がクレジットされた時間。 |
| [!UICONTROL Two Second Continuous Video Plays] | （[!DNL Meta] キャンペーンのみ）ビデオが連続した 2 秒以上再生された回数。 |
| [!UICONTROL User Account Type] | 廃止 |
| [!UICONTROL User SE Account ID] | 検索、ソーシャルおよびCommerceが広告ネットワークに割り当てる数値 ID。 |
| [!UICONTROL Video Average Play Time] | （[!DNL Meta] キャンペーンのみ） 1 つのインプレッションに対してビデオが再生された平均時間（ビデオの再生に費やした時間を含む）。 |
| [!UICONTROL Video Plays] | （[!DNL Meta] キャンペーンのみ）再生を除く、ビデオの再生が開始された回数。 |
| [!UICONTROL Video Played at 25 Percent Count]、[!UICONTROL Video Played at 50 Percent Count]、[!UICONTROL Video Played at 75 Percent Count]、[!UICONTROL Video Played at 100 Percent Count] | （ビデオ広告）再生されたビデオの数です。再生されたビデオの数は、全体の 25%、50%、75% または 100% です。 |
| [!UICONTROL VideoQuartile25Rate]、[!UICONTROL VideoQuartile50Rate]、[!UICONTROL VideoQuartile75Rate]、[!UICONTROL VideoQuartile100Rate] | （ビデオ広告）再生されたビデオの割合は、25%、50%、75% または 100% です。 |
| [!UICONTROL View Rate] | （ビデオ広告）ビューまたはエンゲージメントの数を、広告の表示回数（ビデオおよびサムネールのインプレッション数）で割った値です。 |
| [!UICONTROL Views] | （ビデオ広告）訪問者が広告を視聴した回数、または広告にエンゲージした回数。 |
| [!UICONTROL ViewThroughConversions] | （オーディエンスネットワーク上の広告） 1 つ以上のインプレッションに起因したが、クリックに起因しないコンバージョンの数。 |

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [ 基本レポートと高度なレポートについて ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [ 基本レポートまたは詳細レポートの生成 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [ 基本および詳細レポートの設定 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
