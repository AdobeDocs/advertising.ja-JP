---
title: 基本レポートと詳細レポートのレポート列
description: 基本レポートと詳細レポートで使用できるデータ列について説明します。
exl-id: 649cdfa0-e6f2-4881-9f9d-8217e2547d99
feature: Search Reports, Search Basic Reports, Search Advanced Reports
TQID: https://experienceleague.adobe.com/6of-gBWNiXgwOxOoDFJ-idyaSFeP7wEi7GBfAoRxgyU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 3806
ht-degree: 0%

---

# 基本レポートと詳細レポートのレポート列

| 列 | 説明 |
| ---- | ---- |
| \[広告主固有のカスタム（派生）指標\] | 既存の指標から計算される、作成した[ カスタム指標](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md)の値。 |
| \[広告主固有ラベル分類\] | 現在エンティティに適用されているラベル分類（エンティティ レベル）。 複数のラベル分類は、コンマ（,）で区切ります。 |
| \[Advertiser-specific conversion metrics\] | 指定されたコンバージョン指標またはサイトエンゲージメント指標のコンバージョン数。 |
| \[Googleで追跡されたコンバージョン\] | 「GGL\*、GGL_CT\*、およびGGL_XD_CT\*」のエントリを参照してください。 |
| [!UICONTROL 7-Day Click Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない、過去7日間のクリック予測の平均精度（レポートで指定された日付範囲を含まない）。パーセントで表されます。 |
| [!UICONTROL 7-Day Cost Accuracy] | （[!UICONTROL Portfolio Report]）現在の日付を含まない、過去7日間のコスト予測の平均精度（レポートで指定された日付範囲を含まない）。パーセントで表されます。 |
| [!UICONTROL 7-Day Revenue Accuracy] | （[!UICONTROL Portfolio Report]）過去7日間の売上予測の平均精度で、現在の日付を含まない（レポートで指定された日付範囲を含まない）、パーセントで表されます。 |
| [!UICONTROL Account] | アカウント名。 |
| [!UICONTROL Account Status] | Search, Social, &amp; Commerce内のアカウントのステータス： <ul><li><i>[!UICONTROL Enabled]:</i> （デフォルト）同期された広告ネットワークの場合、Search、Social、およびCommerceは広告ネットワークアカウントにログインしてキャンペーンデータを取得でき、最適化やトラッキング生成などの他の適用機能が有効になります。<br><br>同期されていない広告ネットワークの場合、最適化やトラッキング生成などの適用可能な機能を利用できます。</li><li><i>[!UICONTROL Disabled]:</i>同期された広告ネットワークの場合、Search、Social、およびCommerceは広告ネットワークアカウントにログインしないため、キャンペーンデータを取得せず、最適化やトラッキング生成などの他の該当する機能は無効になっています。 アカウントが有効になっている間に収集されたデータは引き続き保存されますが、今後作成するすべてのキャンペーン管理ビューとレポートには、アカウントが無効になっている期間のデータは含まれません。<br><br>同期されていない広告ネットワークの場合、最適化やトラッキング生成などの該当する機能は使用できません。</li></ul> |
| [!UICONTROL Active Ad Groups] | アクティブな広告グループの数。 |
| [!UICONTROL Active Ads/Creatives] | アクティブな広告/クリエイターの数。 |
| [!UICONTROL Active Campaigns] | アクティブなキャンペーンの数。 |
| [!UICONTROL Active Keywords] | アクティブなキーワードの数。 |
| [!UICONTROL Ad Group] | 広告グループ。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意のID。 |
| [!UICONTROL Ad Group Status] | 広告グループの状態：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、または<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Ad Group Type] | 広告グループの種類（例：<i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ）、<i>[!UICONTROL Demand Gen]</i> （需要創出キャンペーンのみ）、<i>[!UICONTROL Display]</i> （ディスプレイキャンペーンのみ）、<i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、<i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告および既存の拡張テキスト広告のみ）、<i>[!UICONTROL Shopping Showcase]</i>、<i>[!UICONTROL Shopping Product]</i> （標準ショッピングキャンペーンのみ）、または<i>[!UICONTROL Shopping Smart]</i> （スマートショッピングキャンペーンのみ）など）。 キャンペーンの種類によっては、1つのキャンペーンに複数の広告タイプを含めることができるものもあります。 |
| [!UICONTROL Ad Groups] | ラベル値が割り当てられる広告グループの数。 |
| [!UICONTROL AD Name] | 広告グループ名。[!UICONTROL Ad Group]と同じ値。 |
| [!UICONTROL Ad Recall Lift] | （[!DNL Meta] キャンペーンのみ） 2日以内に広告を覚えている推定人数。 |
| [!UICONTROL Ad Recall Rate] | （[!DNL Meta] キャンペーンのみ） 2日以内に広告を覚えている推定人数を、リーチした人数で割った割合。 |
| [!UICONTROL Ad Size] | 広告のサイズ。 |
| [!UICONTROL AD Strength] | （[!DNL Google Ads] レスポンシブ検索広告）広告の有効性：<i>[!UICONTROL average]</i>、<i>[!UICONTROL excellent]</i>、<i>[!UICONTROL good]</i>、<i>[!UICONTROL no_ads]</i>、<i>[!UICONTROL pending]</i>、<i>[!UICONTROL poor]</i>、<i>[!UICONTROL unknown]</i>または<i>[!UICONTROL unspecified]</i>。 |
| [!UICONTROL Adgroup MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、および[!DNL Yahoo! Japan Ads] キャンペーン）現在の広告グループレベルのモバイル入札調整。この調整は、広告がモバイルデバイスに表示されたときに入札額がどのように調整されるかを決定します。 |
| [!UICONTROL AI Max Bundling Required] | （検索ネットワークのみをターゲットとするキャンペーン、AI最大機能が有効になっているキャンペーン、読み取り専用）バンドルが必要かどうか：*[!UICONTROL REQUIRED]*、*[!UICONTROL NOT_REQUIRED]*、*[!UICONTROL UNSPECIFIED]*、またはnull。 |
| [!UICONTROL AI Max Enabled] | [[!UICONTROL AI Max]機能](https://support.google.com/google-ads/answer/15910366)が有効かどうか：[!UICONTROL true]*、*[!UICONTROL false]*、またはnull。 |
| [!UICONTROL AI Max Search Term Matching] | （検索ネットワークをターゲットとし、[AI Max機能](https://support.google.com/google-ads/answer/15910366)とキャンペーンレベルの検索語句の照合機能が有効になっているキャンペーン。読み取り専用）広告グループレベルの検索語句の照合が有効かどうか：*[!UICONTROL true]*、*[!UICONTROL false]*、またはnull。 |
| [!UICONTROL Advertiser] | 広告主名。 |
| [!UICONTROL Advertiser ID] | 広告主のSearch, Social, &amp; Commerce アカウントの数値ID。 |
| [!UICONTROL Avg Position] | 指定された日付範囲内の広告の平均位置。<br><br>[!DNL Google Ads]および[!DNL Yahoo! Japan Ads] キャンペーンの場合、このデータは2019年9月までのみ利用できます。 [!DNL Microsoft Advertising]の場合、このデータは2021年1月22日までのみ利用できます。 |
| [!UICONTROL Base URL] | キャンペーンまたはアカウントに設定された追加パラメーターを含む、キーワードのベース URL。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれていません。 |
| [!UICONTROL Bid Strategy] | （ほとんどの広告ネットワーク）キャンペーンまたはキャンペーンコンポーネントの場合、これはキャンペーンの入札戦略です。 マネージャーアカウントにリンクされている広告ネットワークアカウントの場合、これはクロスアカウント入札戦略です。 使用可能な値は、広告ネットワークによって異なります。 |
| [!UICONTROL Business Name] | （[!DNL Microsoft Advertising]件のレスポンシブ広告） ビジネス名。 |
| [!UICONTROL Call to Action] | （[!DNL Microsoft Advertising]件のレスポンシブ広告とマルチメディア広告）広告に含まれるcall to action。 |
| [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Campaign Budget] | キャンペーン予算。 |
| [!UICONTROL Campaign MBA] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、および[!DNL Yahoo! Japan Ads] キャンペーン）現在のキャンペーンレベルのモバイル入札調整。この調整は、広告がモバイルデバイスに表示されたときに入札額がどのように調整されるかを決定します。 |
| [!UICONTROL Campaign Product Scope Filter] | （ショッピングネットワークを使用したキャンペーンのみ）キャンペーンに対して商品広告を作成できる加盟店アカウント内の商品。 |
| [!UICONTROL Campaign Start Date] | キャンペーンの入札が行われた/配置された最初の日。 |
| [!UICONTROL Campaign Status] | キャンペーンの状態：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Ended]</i>、または<i>[!UICONTROL Deleted]</i>。 |
| [!UICONTROL Campaign Type] | キャンペーンの種類（<i>[!UICONTROL Audience (Ctv Video)]</i><i>[!UICONTROL Audience (Feed)]</i>、<i>[!UICONTROL Audience (Image)]</i>、<i>[!UICONTROL Audience (Video)]</i>、<i>[!UICONTROL Brand Shopping]</i>、<i>[!UICONTROL Demand Gen]</i>、<i>[!UICONTROL Search and Display]</i>、<i>[!UICONTROL Standard Display]</i>、<i>[!UICONTROL Standard Performance Max]</i>、<i>[!UICONTROL Standard Search]</i>、<i>[!UICONTROL Standard Shopping]</i>、<i>[!UICONTROL Store Ad]</i>、<i>[!UICONTROL Video]</i>、または<i>[!UICONTROL Others]</i>など）。 |
| [!UICONTROL Channel Type] | マーケティングチャネルの種類：<i>[!UICONTROL Search]</i>または<i>[!UICONTROL Content]</i>。 この列は、レポート設定の[!UICONTROL Search/Content]設定が「[!UICONTROL Combined]」の場合は含まれません。 |
| [!UICONTROL City] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Transaction Report]） クリックが発生した都市。 それはユーザーのIP アドレスから決まります。 |
| [!UICONTROL Click Match Type] | クリックされた広告のキーワードマッチタイプ。 これは、複数の一致タイプを持つ[!UICONTROL Listing Match Type] キーワードを除き、[!DNL Microsoft Advertising]と同じです。 [!DNL Microsoft Advertising] キーワードの場合、これは実際にクリックされた一致タイプです。 |
| [!UICONTROL Click Value] | （[!UICONTROL Portfolio Report]） ポートフォリオの目的に指定されたクリック値。 |
| [!UICONTROL Click/Impression Time] | （[!UICONTROL Transaction Report]）コンバージョンの原因となったクリックまたはインプレッションが発生した時間。 |
| [!UICONTROL Clicks] | 指定された日付範囲内の広告のクリック数。 |
| [!UICONTROL Client ID1]、[!UICONTROL Client Id 1] | （[!UICONTROL Keyword Report]、[!UICONTROL Ad Variation Report]、および[!UICONTROL Transaction Report]; フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Id 2] | （[!UICONTROL Keyword Report]および[!UICONTROL Transaction Report]; フィードベースのトラッキング実装）フィードファイルで送信された、キーワードまたは広告のクライアント固有のトラッキング ID。 |
| [!UICONTROL Client Transaction ID] | （[!UICONTROL Transaction Report]）一意のトランザクション ID。 |
| [!UICONTROL Constraint End Date] | （[!UICONTROL Constraint Report]）制約がアクティブな最後の日。 |
| [!UICONTROL Constraint Name] | （[!UICONTROL Constraint Report]）制約の名前。 |
| [!UICONTROL Constraint Start Date] | （[!UICONTROL Constraint Report]）制約がアクティブになる最初の日。 |
| [!UICONTROL Constraint Status] | （[!UICONTROL Constraint Report]）制約の状態：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Paused]</i>。 |
| [!UICONTROL Constraint Type] | （[!UICONTROL Constraint Report]）制約の種類：<i>[!UICONTROL Bid/Pos Constraint]</i>、<i>[!UICONTROL Bid Shift]</i>、<i>[!UICONTROL Campaign Budget]</i>、<i>[!UICONTROL Context Sensitive Bid]</i>、<i>[!UICONTROL Incremental Bidding]</i>、<i>[!UICONTROL Max CPA]</i>、<i>[!UICONTROL Min Margin]</i>、<i>[!UICONTROL Variable Bid Position]</i>、<i>[!UICONTROL Search Engine Min Bid]</i>または<i>[!UICONTROL Variable Position]</i>。 |
| [!UICONTROL Constraints] | エンティティに適用できる制約の名前をコンマで区切ります。 |
| [!UICONTROL Content IS] | ディスプレイ/オーディエンスネットワーク上の広告に対して受け取ったインプレッション数を、受け取る資格のあるインプレッション数の推定値で割った値。 [!DNL Microsoft Advertising]では、これは「[!UICONTROL Audience IS]」と呼ばれます。 |
| [!UICONTROL Content IS Lost (budget)] | ディスプレイ/オーディエンスネットワーク上の広告が受け取らなかったインプレッションの推定パーセンテージ。1日または1か月の予算が低すぎたためです。 [!DNL Microsoft Advertising]では、これは「[!UICONTROL Audience lost IS (budget)]」と呼ばれます。 |
| [!UICONTROL Content IS Lost (rank)] | 広告ランクが低いため、ディスプレイ/オーディエンスネットワーク上の広告が表示されなかったインプレッションの推定パーセンテージ。 [!DNL Microsoft Advertising]では、これは「[!UICONTROL Audience lost IS (rank)]」と呼ばれます。 |
| [!UICONTROL Conversion Type] | （[!UICONTROL Transaction Report]）変換の前のアクション：<ul><li><i>[!UICONTROL Click:]</i> コンバージョンの前に、少なくとも1回の有料クリックが発生しました。</li><li><i>[!UICONTROL Impression:]</i> コンバージョンの前に有料クリックが発生しなかったため、コンバージョンはビュースルー（有料クリックのないインプレッション）に起因しました。</li></ul> |
| [!UICONTROL Cost] | 指定された日付範囲内の広告の合計費用。 |
| [!UICONTROL Country] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]） クリックが発生した国。 それはユーザーのIP アドレスから決まります。 |
| [!UICONTROL CPC] | 指定された日付範囲内の広告のクリック単価（CPC）。 |
| [!UICONTROL Creative Base URL] | 広告のベース URL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 検索、ソーシャル、Commerceのリダイレクトとトラッキングコードは含まれていません。 |
| [!UICONTROL Creative Destination URL] | 広告の最終URLまたは宛先URL （トラッキングパラメーターを含む）。 |
| [!UICONTROL Creative Name] | （[!DNL Yahoo! Japan]のみ）広告画像名。 |
| [!UICONTROL Creative Title]、[!UICONTROL Creative Title2] - [!UICONTROL Creative Title3] | 広告のタイトルや見出し。 クリエイティブタイプによって、必要なタイトル行とオプションのタイトル行の数が異なります。 [!UICONTROL Creative Title4]のレスポンシブ広告またはマルチメディア広告で[!DNL Microsoft Advertising]以降の列を表示するには、レポート設定に「[!UICONTROL Creative Titles]」列を含めます。 |
| [!UICONTROL Creative Titles] | （マルチメディアおよびレスポンシブ検索広告の場合のみ）広告の短い見出し（「[!UICONTROL Creative Title]」～「[!UICONTROL Creative Title15]」）ごとに列を追加します。 この列を含める場合、他の[!UICONTROL Creative Title]列を含める必要はありませんが、[!UICONTROL Order Results/Limit Rows By] セクションを編集して、[!UICONTROL Creative Titles]ではなく[!UICONTROL Creative Title]で並べ替えます。 |
| [!UICONTROL Creative Type] | 広告のフォーマット： 次の値が可能です：<i>[!UICONTROL App Install Ad]</i>、<i>[!UICONTROL Call Only Ad]</i>、<i>[!UICONTROL Demand Gen Carousel Ad]</i> （マルチイメージカルーセル広告）、<i>[!UICONTROL Demand Gen Image Ad (single-image ads)]</i>、<i>[!UICONTROL Demand Gen Product Ad]</i>、および<i>[!UICONTROL Demand Gen Video Ad]</i>、<i>[!UICONTROL Display Ad]</i>、<i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Legacy Text Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i>、<i>[!UICONTROL Responsive Ad]</i>、<i>[!UICONTROL Responsive Search Ad]</i>、または<i>[!UICONTROL Text Ad]</i>。 |
| [!UICONTROL CTR] | クリックスルー率：クリック数を、含まれている広告のインプレッション数で割った値です。 |
| [!UICONTROL Currency] | 該当する通貨タイプ（「USD」または「GBP」など）。<br><br><b>注：</b> レポートに異なる通貨を持つアカウントのデータが含まれる場合、「[!UICONTROL Total]」の金銭的価値は、通貨に関係なく、列のすべての数値の合計になります。 |
| [!UICONTROL Current Bid] | ターゲットの現在の入札額。 |
| [!UICONTROL Current First Page Bid] | （[!DNL Google Ads] キャンペーンのみ） [!DNL Google]検索クエリがキーワードと一致する場合に、検索結果の最初のページに広告を配置するために現在必要なクリック単価（CPC）の見積もり入札。<br><br>単一のキーワードと一致タイプの組み合わせの場合、この値は、現在その組み合わせに必要な最初のページ入札です。 同じキーワードと一致タイプの組み合わせを複数のキャンペーンで使用する場合、この値は、すべてのインスタンスで現在必要な最初のページ入札の最小値です。 |
| [!UICONTROL Current Quality Score] | （[!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンのみ）広告ネットワークによって指定された、キーワードまたは入札単位の現在の品質スコア。 範囲は1 （低）から10 （完全）です。 単一のキーワードと一致タイプの組み合わせの場合、この値はその組み合わせの現在のスコアです。 複数のキャンペーンで同じキーワードと一致タイプの組み合わせが使用されている場合、この値は、すべてのインスタンス間の最大の現在のスコアです。<br><br>広告ネットワークは、入札価格と広告掲載順位を決定するために品質スコアを使用します。 キーワードと関連する広告の関連性、利用者の検索クエリ、ランディングページの品質など、多くの要因にもとづいて計算されます。 [!DNL Google Ads]のキーワードの場合は、キーワードのクリック率も考慮され、[!DNL Microsoft Advertising]のキーワードの場合は、ランディングページが提供するユーザーエクスペリエンスも考慮されます。 |
| [!UICONTROL Custom Bid Level] | （ディスプレイネットワークのみをターゲットとするGoogle キャンペーン）どのレベルで入札が行われるか：<i>[!UICONTROL Ad Group]</i>、<i>[!UICONTROL Age]</i>、<i>[!UICONTROL Gender]</i>、<i>[!UICONTROL Interest and List]</i>、<i>[!UICONTROL Keyword]</i>、<i>[!UICONTROL Placement]</i>、<i>[!UICONTROL Vertical]</i>、<i>[!UICONTROL None]</i>、または<i>[!UICONTROL Unknown]</i>。 |
| [!UICONTROL Description1] - [!UICONTROL Description4] | 広告の本文。 クリエイティブタイプによって、必要な説明行とオプションの説明行の数が異なります。 [!UICONTROL Description3]のレスポンシブ広告またはマルチメディア広告の[!UICONTROL Description4]列と[!DNL Microsoft Advertising]列を表示するには、レポート設定に「[!UICONTROL Descriptions]」列を含めます。 |
| [!UICONTROL Descriptions] | （[!DNL Microsoft Advertising] レスポンシブ広告とマルチメディア広告）広告の説明行（「[!UICONTROL Description1]」～「[!UICONTROL Description4]」）ごとに列を追加します。 この列を含める場合、他の[!UICONTROL Description]列を含める必要はありません。 |
| [!UICONTROL Device] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、および[!DNL Yahoo Native] キャンペーン）広告が表示されたデバイスタイプ：<i>[!UICONTROL Computers]</i>、<i>[!UICONTROL Mobile]</i>、<i>[!UICONTROL Tablets]</i>、<i>[!UICONTROL Other]</i>、または<i>[!UICONTROL N/A]</i> （値なし）。 他の広告ネットワークの行の値はN/Aです。<br><br>検索キャンペーンでは、広告のクリック時に、キーワード、広告、および/または広告拡張機能のトラッキングテンプレートまたは宛先URLに、デバイス （`&ev_dvc={device}&ev_dvm={devicemodel}`）でデータを追跡するパラメーターが含まれている場合、コンバージョンデータも各デバイスタイプの行に含まれます。 それ以外の場合、コンバージョンデータをデバイスタイプに関連付けられない場合は、「[!UICONTROL Device]」値が[!UICONTROL N/A]の別の行に集計されます。 |
| [!UICONTROL Display Path 1] | （[!DNL Google Ads]個の拡張テキスト広告のみ）広告のベース URLの後の最初の表示パス。 |
| [!UICONTROL Display Path 2] | （[!DNL Google Ads]個の拡張テキスト広告のみ）広告のベース URLの後の2番目の表示パス。 |
| [!UICONTROL Display Type] | 廃止 |
| [!UICONTROL Display URL] | 広告の表示URL。エンドユーザーが広告に表示するものです。 |
| [!UICONTROL DMA] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]） クリックが発生した数値指定の市場地域（デンバーの場合は751など）。 それはユーザーのIP アドレスから決まります。 |
| [!UICONTROL Domain] | （[!UICONTROL Domain Referral Report], [!UICONTROL Keyword Report]） クリックが発生したドメイン名。 |
| [!UICONTROL eCPM] | 指定した日付範囲の1000 インプレッションあたりの平均コストです。 eCPM値は、CPMまたはCPC キャンペーンで計算されます。 |
| [!UICONTROL EF Campaign ID] | Search, Social, &amp; Commerceがキャンペーンに割り当てる数値ID。 |
| [!UICONTROL EF ID] | （[!UICONTROL Transaction Report]） （Adobe Advertising コンバージョン トラッキング サービスを使用する広告主と、トークンを使用する&quot;[!UICONTROL EF Redirect]&quot; トラッキング メソッド） クリックまたはコンバージョンのトークン。<ul><li>[!DNL Google Ads]件の検索広告のEF IDは`{gclid}:G:s`で、Google クリック ID （GCLID）とネットワークの種類（検索用に「s」）が含まれます。</li><li> [!DNL Microsoft Advertising]件の検索広告のEF IDは`{msclkid}:G:s`で、Microsoft クリック ID （MSCLKID）とネットワークの種類（検索用に「s」）が含まれます。</li><li>他の広告ネットワークでの検索広告の場合、EF IDには、サーファーID、クリック時間、ネットワークタイプが含まれます。</li><li>ディスプレイ広告の場合、EF IDには、サーファーID、クリックまたはインプレッション時間、ネットワークタイプが含まれます。</li></ul> |
| [!UICONTROL EF Pixel Location ID] | （[!UICONTROL Geo Distribution Report]；検索、ソーシャル、Commerceのみ）地理的位置の内部ID。データの正規化に使用されます。 |
| [!UICONTROL EF Portfolio Group ID] | ポートフォリオが属するポートフォリオグループの数値ID。 |
| [!UICONTROL EF Search Engine ID] | Search, Social, &amp; Commerceがアドネットワークに割り当てる数値ID: <i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], <i>[!UICONTROL 88]</i> for [!DNL Baidu], <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL Yahoo! Japan Ads] （非推奨）, <i>[!UICONTROL 105]</i> （非推奨）の[!DNL Yahoo Native]<i>[!UICONTROL 106]</i>[!DNL Pinterest] |
| [!UICONTROL End Date] | 最終日が報告されました。 |
| [!UICONTROL Engagement Rate] | （動画広告） エンゲージメントの数を、広告が表示された回数で割った値です。 |
| [!UICONTROL Engagements] | （動画広告） ユーザーが広告を少なくとも10秒間視聴した回数、または広告が10秒未満の場合に完全な広告の回数。 |
| [!UICONTROL Est. Clicks] | （[!UICONTROL Geo Distribution Report]；検索および表示キャンペーンのみ）広告グループ/キャンペーン/ポートフォリオの組み合わせのクリック数の推定値。 この値は、広告ネットワークによって提供される値とは異なる場合があります。 |
| [!UICONTROL Estimated Cost] | Search, Social, &amp; Commerceが追跡した関連する広告の見積もり費用の合計。 この値は、広告ネットワークによって提供される値とは異なる場合があります。 |
| [!UICONTROL Estimated Impressions] | （ディスプレイキャンペーンのみ） Search, Social, &amp; Commerceが追跡した広告インプレッションの推定数。 この値は、広告ネットワークによって提供される値を示す[!UICONTROL Impressions]列（使用可能な場合）の値とは異なる場合があります。 |
| [!UICONTROL Exclude (yes/no)] | 一致する製品の広告に対して、入札が除外されているか（<i>[!UICONTROL Yes]</i>）、または入札が許可されているか（<i>[!UICONTROL No]</i>）。 |
| [!UICONTROL First Page CPC] | （Google キャンペーンのみ）指定した日付範囲の検索結果の最初のページに表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Frequency] | （[!DNL Meta] キャンペーンのみ）ユーザーが広告を閲覧した平均回数。 |
| `GGL*`、`GGL_CT*`および`GGL_XD_CT*` [[!DNL Google Ads]件のトラッキング済みコンバージョン ] | （[!DNL Google Ads]件のキャンペーンが検索およびショッピングネットワーク上） [!DNL Google Ads]追跡されたコンバージョン。各コンバージョンに対して最大3つの個別の指標が含まれます：<ul><li>`GGL*` — （トラッキングする場合） 「GGL」プレフィックスで始まるキーワードのコンバージョン値（GGL Purchaseなど）。</li><li>`GGL_CT*` — 「GGL_CT」接頭辞（GGL_CT_Purchaseなど）で始まるコンバージョンの数（カウント）。</li><li>`GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合、トラッキングする場合）クロスデバイスコンバージョンの数（カウント）。「GGL_XD_CT_」接頭辞（GGL_XD_CT_Purchaseなど）で始まる[!DNL Google Ads]で測定されます。</li></ul><br>各コンバージョンは、入札単位とクリック日で記録されます。イベントレベルでは利用できません。 [!DNL Google Ads]件のトラッキングされたコンバージョンについて詳しくは、「[[!DNL Google Ads] Search, Social, &amp; Commerce](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」のコンバージョンデータを参照してください。 |
| [!UICONTROL Impr. (Abs. Top) %] | （[!DNL Google Ads]のみ）最初の広告としてオーガニック検索結果の上位に表示される広告インプレッションの割合。 |
| [!UICONTROL Impr. (Top) %] | （[!DNL Google Ads]のみ）オーガニック検索結果の上位に表示される広告インプレッションの割合。 |
| [!UICONTROL Impressions] | 指定された日付範囲内の広告インプレッション数。 |
| [!UICONTROL Interaction Rate] | （動画広告）インタラクションの数を広告（動画とサムネイルのインプレッション）が表示された回数で割った数。 |
| [!UICONTROL Interactions] | （動画広告）ユーザーが広告を視聴した回数。 |
| [!UICONTROL Is_Click_Objectives] | （[!UICONTROL Portfolio Report]） <i>true</i> （ポートフォリオに[!UICONTROL Maximize Clicks]入札戦略を持つキャンペーンが含まれる場合）、その他<i>false</i>。 |
| [!UICONTROL Keyword] | キーワード。<br><br><b>注：</b> レポートにコンテンツ対応の検索キャンペーンの広告グループからのデータが含まれる場合、この列には該当する広告グループ名（「広告グループ名」など）が含まれます。 検索キャンペーンでサイトをターゲットにしたプレースメントの場合、この列には値がありません。 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意のID。 |
| [!UICONTROL Keyword Status] | 検索語句が一致したキーワードのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>、<i>[!UICONTROL Deleted]</i>、または<i>[!UICONTROL Disapproved]</i>。 |
| [!UICONTROL Label Classification] | （[!UICONTROL Label Classification Report]および[!UICONTROL Label Value Report]） ラベル分類。 |
| [!UICONTROL Label Value] | （[!UICONTROL Label Classification Report]および[!UICONTROL Label Value Report]） ラベル分類の値。 |
| [!UICONTROL Language] | （ディスプレイキャンペーン）ターゲットオーディエンス言語。 |
| [!UICONTROL Link Type] | （[!UICONTROL Keyword Report]; [!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンのみ。データは、レポートに指定されたアトリビューションルールが「最後のイベント」の場合にのみ使用できます）行が、広告拡張機能（広告自体ではなく）または製品/ショッピング広告のクリックに起因するコンバージョンをレポートする場合、この列には、クリックされたリンクのタイプとタイトルが表示されます。<ul><li>`pla:*` – 製品広告は、「プラン `pla:<product ID>`」など、:8525822として表示されます。</li><li>`sl:*` — サイトリンクは、「sl`sl:<Sitelink text>` Current Offers」のように:Seeとして表示されます。</li></ul> |
| [!UICONTROL Listing Match Type] | 広告リストのキーワード一致タイプ、コンテンツ ターゲットキャンペーンの広告の<i>[!UICONTROL Content]</i>、サイト ターゲットキャンペーンのプレースメントのキーワード一致タイプ。<i>[!UICONTROL Sitecpc]</i> [!DNL Microsoft Advertising] キーワードの場合、これには複数の一致タイプ （「[!UICONTROL Broad],[!UICONTROL Exact]」など）が含まれる場合があります。 |
| [!UICONTROL Location] | （ディスプレイキャンペーン）ターゲットオーディエンスの場所。 |
| [!UICONTROL Long Creative Title1] - [!UICONTROL Long Creative Title5] | （レスポンシブ広告およびマルチメディア広告[!DNL Microsoft Advertising]件の完了したレポート行）広告の長い見出し。 これらの列を表示するには、レポート設定に「[!UICONTROL Long Creative Titles]」列を含めます。 |
| [!UICONTROL Long Creative Titles] | （レスポンシブ広告およびマルチメディア広告[!DNL Microsoft Advertising]の場合）各広告の長いタイトル（「[!UICONTROL Long Creative Title1]」から「[!UICONTROL Long Creative Title5]」）の列を追加します。 |
| [!UICONTROL Market Type] | 市場タイプ：<i>[!UICONTROL search]</i>または<i>[!UICONTROL social]</i> |
| [!UICONTROL Max Spend % Target] | （[!UICONTROL ROI]、[!UICONTROL CPT]、または[!UICONTROL Marginal Cost per Transaction]の予算戦略を使用するポートフォリオのキャンペーン）ポートフォリオの日次予算の最大目標。 |
| [!UICONTROL Max Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワーク用に構成されているポートフォリオの支出の最大割合。 制約タイプ「[!UICONTROL Min-Max]」を使用するポートフォリオの場合、これは[!UICONTROL Max %]値です。 制約タイプ「[!UICONTROL Target Spend]」を使用するポートフォリオの場合、これは[!UICONTROL Target Spend]値です。 |
| [!UICONTROL Method ID] | （[!UICONTROL Portfolio Report]） |
| [!UICONTROL Metro Code] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]） インプレッションまたはクリックが発生したメトロコード （Denverの場合はus-751など）。 検索ユーザーのIP アドレスから決定されます。 |
| [!UICONTROL Min Spend (%)] | （[!UICONTROL Network Constraint Report]）広告ネットワーク用に構成されているポートフォリオの支出の最小割合。 制約タイプ「[!UICONTROL Min-Max]」を使用するポートフォリオの場合、[!UICONTROL Min %]が設定されている場合、これは[!UICONTROL Min %]値です。 制約タイプ「[!UICONTROL Target Spend]」を使用するポートフォリオの場合、これは[!UICONTROL Target Spend]値です。 |
| [!UICONTROL Network Account ID] | ネットワークによって割り当てられたアカウント ID。 |
| [!UICONTROL Network Ad Group ID] | ネットワークによって割り当てられた広告グループ ID。 |
| [!UICONTROL Network Campaign ID] | ネットワークによって割り当てられたキャンペーン ID。 |
| [!UICONTROL Network Campaign Objective] | （[!DNL Meta] キャンペーンのみ）キャンペーンの目的。 |
| [!UICONTROL Objective Name] | ポートフォリオの目的。 |
| [!UICONTROL Objective Value] | ポートフォリオの現在の目標に従って計算された合計重み付けコンバージョン。 |
| [!UICONTROL Objective Value Calculation] | 目的の値を導き出すために使用される計算。 |
| [!UICONTROL Outbound Clicks] | （[!DNL Meta] キャンペーンのみ）広告内のリンクをクリックした回数で、[!DNL Meta]が所有するプロパティからユーザーを削除します。 |
| [!UICONTROL Parent Product Groupings] | 適用可能な場合、階層間に`>>`を持つ親製品グループの完全な階層（`All Products>>CategoryL1=Animals`など）。 |
| [!UICONTROL Partition Type] | 製品グループの種類：<i>[!UICONTROL Sub-Division]</i> （親製品グループ）または<i>[!UICONTROL Unit]</i> （入札済みの子製品グループの最下位レベル）。 |
| [!UICONTROL Path Position] | （[!UICONTROL Transaction Report]） コンバージョンパス内のイベントの位置。 |
| [!UICONTROL Path Total] | （[!UICONTROL Transaction Report]） パス位置のイベントの合計数。 |
| [!UICONTROL Portfolio] | ポートフォリオ。 |
| [!UICONTROL Portfolio Count] | （[!UICONTROL Portfolio Report]）目的に関連付けられているポートフォリオの数。<!-- This count is different than what I see within the Objectives view. --> |
| [!UICONTROL Portfolio Group Name] | ポートフォリオが属するポートフォリオグループの名前。 |
| [!UICONTROL Portfolio ID] | 数値ポートフォリオ ID。 |
| [!UICONTROL Portfolio Spend Strategy] | （[!UICONTROL Portfolio Report]） ポートフォリオの支出戦略：<i>[!UICONTROL Daily]</i>、<i>[!UICONTROL Weekly]</i>、<i>[!UICONTROL Monthly]</i>、<i>[!UICONTROL ROI]</i>、<i>[!UICONTROL Day of week]</i>、<i>[!UICONTROL Day of month]</i>、<i>[!UICONTROL CPT]</i>、<i>[!UICONTROL Marginal CPT]</i>、<i>[!UICONTROL Google Target CPA]</i>または<i>[!UICONTROL Google Target ROAS]</i>。 |
| [!UICONTROL Portfolio Status] | ポートフォリオステータス：<ul><li><i>[!UICONTROL Optimize]:</i>最適化機能では、関連するキャンペーンのクリック数と収益データを収集し、最適化に使用されたデータをモデリングして、入札、キャンペーン予算、キャンペーン入札戦略のターゲットを最適化しています（最適化の種類と入札戦略によって異なります）。</li><li><i>[!UICONTROL Active]:</i>最適化機能は、関連するキャンペーンのクリック数と収益データを収集し、データをモデリングしていますが、入札額やキャンペーン予算を最適化していません。</li><li><i>[!UICONTROL Inactive]:</i>最適化機能は、レポート用に関連するキャンペーンのクリック データを収集していますが、データのモデリングや、入札やキャンペーン予算の最適化を行っていません。</li></ul> |
| [!UICONTROL Portfolio Target] | （[!UICONTROL Portfolio Report]） ポートフォリオの支出戦略の日別目標。 日次/月次および日次/週次の戦略の場合、現在の目標が表示されます。 |
| [!UICONTROL Preferred Devices] | （[!DNL Google Ads]、[!DNL Microsoft Advertising]、および[!DNL Yahoo! Japan Ads] キャンペーン）広告設定で<i>[!UICONTROL Mobile ads]</i>または<i>[!UICONTROL All ads]</i>のどちらが優先されます。 |
| [!UICONTROL Product Group ID] | 広告ネットワークが製品グループに割り当てる数値ID。 |
| [!UICONTROL Product Group Name] | 製品グループの名前。 |
| [!UICONTROL Product Group Status] | 製品グループのステータス。 |
| [!UICONTROL Product Groupings] | 親製品グループ。 |
| [!UICONTROL Product ID] | （[!UICONTROL Keyword Report]; [!DNL Google Ads]個の製品リスト広告）広告と共に表示される製品の製品ID。<br><br><b>注：</b>IDは、製品リストにトラッキングパラメーター`ev_plx=<GMC product ID>`が含まれている場合にのみキャプチャされます。トラッキングパラメーターは[!DNL Google Merchant Center]以内に追加する必要があります。 |
| [!UICONTROL Raw Transaction Data] | （[!UICONTROL Transaction Report]） コンバージョン指標の収益（1件の登録では1件、12米ドルの注文では12件など）。 複数の入札単位が同じトランザクション IDを持つ場合、トラッキング IDの収益は、指定したクリック日のクリック数（クリックデータが使用可能な場合）に応じて分割されます。 |
| [!UICONTROL Reach] | （[!DNL Meta] キャンペーンのみ）少なくとも1回は広告を見たユーザーの数。 注意：[!DNL Meta]では、ユーザープロファイルのリーチが毎日重複しているため、[!DNL Meta]とSearch, Social, &amp; Commerceで報告される数値は異なる場合があります。 |
| [!UICONTROL Region] | （[!UICONTROL Geo Distribution Report], [!UICONTROL Keyword Report]） インプレッションまたはクリックが発生した地域または米国/カナダの州。 それはユーザーのIP アドレスから決まります。 |
| [!UICONTROL SE Creative ID] | ネットワークによって割り当てられた広告ID。 |
| [!UICONTROL Search (Abs. Top) IS] | （[!DNL Google Ads]と[!DNL Microsoft Advertising]）絶対上位の場所で受け取ったインプレッション （オーガニック検索結果の上位の最初の広告）を、上位の場所で受け取る資格のあるインプレッションの推定数で割った値。 10%未満の割合は、「`<10%`」または「`0.0999`」と表示されます。 |
| [!UICONTROL Search (Top) IS] | （[!DNL Google Ads]と[!DNL Microsoft Advertising]）上位の場所（オーガニック検索結果の上）で受け取ったインプレッションを、上位の場所で受け取る資格のあるインプレッションの推計数で割った値。 10%未満の割合は、「`<10%`」または「`0.0999`」と表示されます。 |
| [!UICONTROL Search Engine] | 広告ネットワーク。 |
| [!UICONTROL Search exact match IS] | キーワードと完全に一致した検索で受け取ったインプレッションの数を、受け取る資格のある完全一致インプレッションの推定数で割った値。 この数値が低い場合は、入札額が低すぎるか、広告の質や関連性が低いことが原因である可能性があります。 |
| [!UICONTROL Search impr. share] | （[!DNL Google Ads]のみ）受け取ったインプレッションを、受け取る資格のあるインプレッションの推定数で割った値。 10%未満の割合は「&lt;10%」、90%を超える割合は「`>90%`」と表示されます。 |
| [!UICONTROL Search lost abs. top IS (budget)] | （[!DNL Google Ads]と[!DNL Microsoft Advertising]）毎日または月々の予算が低すぎるため、広告がオーガニック検索結果を上回った最初の広告ではない時間の割合。 Google広告キャンペーンの場合、90%を超える割合は「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search lost abs. top IS (rank)] | （[!DNL Google Ads]と[!DNL Microsoft Advertising]）広告ランクが低いため、あなたの広告がオーガニック検索結果を上回った最初の広告ではない時間の割合。 Google広告キャンペーンの場合、90%を超える割合は「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search lost IS (budget)] | （[!DNL Google Ads]のみ）毎日または月々の予算が低すぎたため、広告が表示されなかった時間の割合。 この指標は、キャンペーンレベルでのみ使用できます。 90%を超える割合は、「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search lost IS (rank)] | （[!DNL Google Ads]のみ）広告ランクが低いため、広告が表示されなかった時間の割合。 90%を超える割合は、「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search lost top IS (budget)] | （[!DNL Google Ads]と[!DNL Microsoft Advertising]）毎日または月々の予算が低すぎたため、オーガニック検索結果の上位に広告が表示されなかった時間の割合。 [!DNL Google Ads] キャンペーンの場合、90%を超える割合は「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search lost top IS (rank)] | （[!DNL Google Ads]と[!DNL [!DNL Microsoft Advertising]]）広告ランクが低いため、あなたの広告がオーガニック検索結果より上位に表示されなかった時間の割合。 Google広告キャンペーンの場合、90%を超える割合は「`>90%`」または「`0.9001`」と表示されます。 |
| [!UICONTROL Search Term] | （[!UICONTROL Transaction Report]） ユーザーがクエリした検索語句。 |
| [!UICONTROL SETrackingOnly] | アカウントを追跡しているが入札を行っていない場合：<i>[!UICONTROL TRUE]</i>または<i>[!UICONTROL FALSE]</i>。 |
| [!UICONTROL Site] | （ドメイン紹介レポートと[!UICONTROL Keyword Report]; サイトのターゲット設定プレースメント） クリックが発生したサイト。 |
| [!UICONTROL Start Date] | 最初の日が報告されました。 |
| [!UICONTROL State] | （地域分布レポート、[!UICONTROL Keyword Report]）トランザクションの発生元の状態。 それはユーザーのIP アドレスから決まります。 |
| [!UICONTROL Surfer ID] | （[!UICONTROL Transaction Report]） トランザクションを完了したユーザーのID。 |
| [!UICONTROL Thru Plays] | （[!DNL Meta] キャンペーンのみ）広告全体を視聴したビューの数。 |
| [!UICONTROL Top of Page CPC] | （Google キャンペーンのみ）指定した日付範囲の検索結果ページの上部に表示される広告のクリック単価（CPC）。 |
| [!UICONTROL Tracking URL] | （検索対象キーワードのみ）検索、ソーシャル、およびCommerceのトラッキングコードに埋め込まれたトラッキングテンプレートまたは宛先URL （該当する場合）。 |
| [!UICONTROL Transaction Property Name] | （[!UICONTROL Transaction Report]） トランザクションがクレジットされる広告主固有のコンバージョン指標。 |
| [!UICONTROL Transaction Time] | （[!UICONTROL Transaction Report]）指定されたコンバージョン指標がクレジットされた時間。 |
| [!UICONTROL Two Second Continuous Video Plays] | （[!DNL Meta] キャンペーンのみ）ビデオが少なくとも2秒間連続して再生された回数。 |
| [!UICONTROL User Account Type] | 廃止 |
| [!UICONTROL User SE Account ID] | Search, Social, &amp; Commerceが広告ネットワークに割り当てる数値ID。 |
| [!UICONTROL Video Average Play Time] | （[!DNL Meta] キャンペーンのみ） 1回のインプレッションで、ビデオの再生に費やした時間を含む、ビデオの平均再生時間。 |
| [!UICONTROL Video Plays] | （[!DNL Meta] キャンペーンのみ）リプレイを除く、ビデオの再生を開始した回数。 |
| [!UICONTROL Video Played at 25 Percent Count]、[!UICONTROL Video Played at 50 Percent Count]、[!UICONTROL Video Played at 75 Percent Count]、[!UICONTROL Video Played at 100 Percent Count] | （動画広告）再生された動画数25%、50%、75%、または100%。 |
| [!UICONTROL VideoQuartile25Rate]、[!UICONTROL VideoQuartile50Rate]、[!UICONTROL VideoQuartile75Rate]、[!UICONTROL VideoQuartile100Rate] | （動画広告）再生された動画の割合。25%、50%、75%、または100% |
| [!UICONTROL View Rate] | （ビデオ広告）視聴回数またはエンゲージメントを、広告（ビデオおよびサムネールのインプレッション）が表示された回数で割った数。 |
| [!UICONTROL Views] | （動画広告）ユーザーが広告を視聴またはエンゲージした回数。 |
| [!UICONTROL ViewThroughConversions] | （オーディエンスネットワーク上の広告） 1つ以上のインプレッションに起因するが、クリックしなかったコンバージョンの数。 |

<!-- HOW IS MARKET TYPE DIFFERENT FROM CHANNEL TYPE? And what are all possible values for each? -->

>[!MORELIKETHIS]
>
>* [基本レポートと詳細レポートについて](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [基本レポートまたは詳細レポートを生成](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-generate.md)
>* [基本および詳細レポート設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
