---
title: レポートに関する FAQ
description: データの問題のトラブルシューティングなど、パフォーマンスレポートに関するよくある質問への回答を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '3917'
ht-degree: 0%

---

# レポートに関する FAQ

## 一般的な質問

+++レポートの日付範囲がレポートデータが使用可能になる前に開始した場合はどうなりますか。
レポートは生成されますが、データが使用可能な日付のデータのみが含まれます。 各レポートタイプでデータを利用できるタイミングについて詳しくは、[レポートに使用するデータ](data-used-for-reports.md).&quot;
+++

+++クリック日レポートとトランザクション日ベースレポートの違いは何ですか。
トランザクション日別にコンバージョンをレポートする場合、データには、指定した期間にトランザクション日が発生したトランザクションが含まれます。 このオプションは、基本レポートおよび高度なレポートのデフォルト設定で、指定した期間内に獲得した売上高を示します。

クリック日別にコンバージョンをレポートする場合、データには、指定した期間に発生したクリックに起因するトランザクションが含まれます。 ポートフォリオでクリック数とトランザクション数の間に大きな遅延が生じた場合、このタイプのレポートは、ポートフォリオのクリックあたりの過去の売上高を示し、時間の経過と共に予想される売上高行動を把握できます。

![クリック日別のレポートとトランザクション日別のレポート](/help/search-social-commerce/assets/click-date-vs-txn-date.png "クリック日別のレポートとトランザクション日別のレポート")
+++

+++クリックのルックバックウィンドウまたはインプレッションのルックバックウィンドウを変更するとどうなりますか。
（広告ピクセルベースのコンバージョントラッキングサービスを持つ広告主のみ）最初のクリックによって生じたイベントのデータは、長い期間または短い期間収集されます。

広告主の [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j) 有料クリックまたは表示インプレッションが（それぞれ）発生してからの日数を判断し、その中でイベントがコンバージョンに関連付けられる可能性があります。 値を長い期間または短い期間に変更することは、特にクリックトゥ売上高が短い広告主や長い広告主や、インプレッションツー売上高の期間を表示する広告主にとって重要です。

**ベストプラクティス：** ルックバックウィンドウが売上高のクリックトゥリーよりも長いことを確認し、ほとんどのキーワードや広告でインプレッションから売上高までの時間を表示します。 短いコンバージョンの場合、一部のコンバージョンは、最初のクリックやインプレッションに関連付けられません。
+++

+++どのコンバージョンが [!DNL Google Ads] 広告の拡張または製品のリスト。
どのコンバージョンが、 [!DNL Google Ads] 広告の拡張（広告自体ではなく）、または [!UICONTROL Transaction Report]. この [!UICONTROL Link Type] 列の値は、クリックされたリンクのタイプとタイトルを示します。

* 製品リストは、次のように表示されます。 `pla:<product ID>`例： `pla:8525822`.

* サイトリンクは、 `sl:<Sitelink text>`例： `sl:See Current Offers`.

   また、 [!UICONTROL Tracking URL] 」列に表示されます。 この [!UICONTROL Tracking URL] サイトリンクの場合、属性 `&ev_ltx=sl:<link-name>`.

>[!NOTE]
>
>コンバージョン元 [!DNL Google Ads] 場所と電話の拡張は、それらが付随する広告のデータに含まれます。 別途報告されるわけではありません。

+++

+++[!UICONTROL Keyword]&quot;レポートの列に値&quot;(adgroup content) &lt;*広告グループ名*>」
行に、キーワードを含まないコンテンツ対応検索キャンペーン、ディスプレイキャンペーン、またはソーシャルキャンペーンのデータが含まれる場合、 [!UICONTROL Keyword] 列には、代わりに、該当する広告グループ名が表示されます。
+++

+++季節や市場の変化により、レポートに異常なデータが表示されます。 条件が変更されると、入札に影響を与えますか？
最適化機能は、トレンドを特定して即座に対応できるように、毎日入札単位ごとに売上高モデルを作成し、モデルに長期履歴データを組み込んで季節性の予測に役立てます。 ポートフォリオの収益モデルの半減期設定<!-- add link to glossary? --> また、最近の売上高データの重み付けの程度を決定します。 ベストプラクティスは、非定型的なパフォーマンスの期間中に半減期を減らし、収益モデルを調整した後に寿命を延ばすことです。 半減期の調整が必要かどうかについて質問がある場合は、担当のAdobeアカウントチームにお問い合わせください。

期間のデータが将来の入札にまったく影響を与えたくない場合は、モデルからそれらの日付を除外するように選択できます。 日付を除外するには、Adobeアカウントチームにお問い合わせください。
+++

+++特定のプロパティ指標 ( [!UICONTROL Device] または [!UICONTROL Objective Name]?
キャンペーンエンティティレポートの場合 ([!UICONTROL Campaign Report], [!UICONTROL Ad Group Report], [!UICONTROL Ad Variation Report], [!UICONTROL Keyword Report]、および [!UICONTROL Product Group Report]) の場合、指標データは、レポートに含めるプロパティ列によって動的に集計されます。 オプションで、レポートのキー列を削除し、データを集計するプロパティ列のみを含めることができます。

例えば、 [!UICONTROL Keyword Report] を含む [!UICONTROL Ad Group] および  次に、デフォルトでは、デバイス列は、広告グループおよびデバイスタイプごとに各キーワードの指標を集計します。 ただし、 [!UICONTROL Keyword] 」列を使用してレポートを生成すると、デバイスタイプ別に指定した広告グループの指標がレポートで動的に生成されます。

>[!NOTE]
>
>この機能を使用して、ラベルの分類でデータを集計することはできません。 レポート内のラベル分類列は省略されます。 代わりに、 [ラベル分類レポート](/help/search-social-commerce/reports/management/basic-advanced/label-classification-report.md).

+++

## 一般的なデータの問題

+++異なるアトリビューションルールを使用して生成されたレポートの合計は異なります。
同じレポートパラメーターを使用し、異なるアトリビューションルールを使用してレポートを複数回生成する場合、データは次のどちらかの理由で異なる可能性があります。

* クリック日ベースのデータは、指定した日付範囲外に含まれる場合があります。

   レポートパラメーター「[!UICONTROL Conversions based on click date]」と入力すると、指定した日付範囲が、トランザクションの日付ではなく、クリックの日付に適用されます。 レポートでアトリビューションルール「最初のイベント」または「最後のイベント」も使用している場合、コンバージョンにつながった最初または最後のイベントが指定した日付範囲外になる可能性があります。 例えば、ユーザーが 4 月 30 日に Keyword_1 をクリックし、5 月 20 日に Keyword_2 をクリックし、5 月 21 日に Keyword_2 を変換したとします。 レポートで[!UICONTROL First Event]「属性ルールおよび 5 月 1 日から 21 日までの日付範囲の場合、最初のイベント（4 月 30 日のキーワード 1 のクリック）はレポートに含まれません。 同じ日付範囲で、[!UICONTROL Last Event]」アトリビューションルールを指定した場合、最後のクリックが指定した日付範囲内で発生したので、コンバージョンがレポートに含まれます。

* ポートフォリオフィルターの選択では、コンバージョンにつながるイベントの一部が除外されます。

   ポートフォリオのサブセットについてレポートする場合、アトリビューションルールの 1 つでコンバージョンに関連付けられたイベントを含むキャンペーンが含まれていない可能性があります。 たとえば、ユーザーがPortfolio_1 から Keyword_1 をクリックし、Portfolio_2 から Keyword_2 をクリックして、変換を行うとします。 レポートで[!UICONTROL First Event]」アトリビューションルールを使用する場合は、Portfolio_1 を含めて、コンバージョンをレポートに含める必要があります。 ただし、レポートで「最後のイベント」属性ルールを使用する場合は、Portfolio_2 を含める必要があります。

>[!TIP]
>
>異なるアトリビューションルールでコンバージョンの合計を比較する場合は、レポートパラメーター「[!UICONTROL Conversions based on transaction date]「 」を選択し、すべての広告ネットワークまたはすべてのポートフォリオを選択します。 他のフィルターを設定しない場合は、コンバージョンの合計が一致する必要があります。

+++

+++個々のデータフィールドが正しくありませんが、合計は正しいです。
この状況は、指標の形式で整数が使用されている場合に発生する可能性があります。

* 次の場合、 [カスタム指標](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-about.md) を *小数点を含む数値* （データを整数で表示）を含め、重み付けされたコンバージョンアトリビューションルール ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]または [!UICONTROL Even Distribution]) の場合、出力は小数ではなく整数で表示されます。 この場合、個々のデータフィールドが正しくない可能性がありますが、合計は正しいです。 例えば、ある注文が 3 つのイベント間で等しく分割されている場合、（0.33 順序ではなく）1 つの注文が 3 つのイベントのそれぞれに関連付けられます。 問題を解決するには、 [指標の形式を変更する](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-edit.md) から *小数点第 2 位までの数値*.

* 同様に、売上高指標が整数で送信される場合も、同じ問題が発生します。 （売上高フォーマットは、データを送信するコンバージョンタグによって制御されます）。 問題を解決するには、 [カスタム指標の作成](/help/search-social-commerce/common-tasks/custom-metrics/custom-metric-create.md) 売上高指標のみから成り、形式を持つ *小数点第 2 位までの数値*を作成し、元の指標ではなく、ビューやレポートに含めます。
+++

+++クリックまたは売上高データが見つからない場合、将来の入札に影響を与えないようにする方法を教えてください。
Search、Social、および Commerce が広告ネットワークと同期していない場合、クリックデータの問題が発生します。 アカウントを手動で同期するには、Adobeアカウントチームにお問い合わせください。 1 日のクリックデータがない場合は、Adobeアカウントチームに連絡して、その日をコストモデルから除外するように依頼します。

売上高データの問題は、トラッキングまたはフィードファイルの問題が原因で発生する可能性があります。 問題を調査するには、Adobeアカウントチームにお問い合わせください。 1 日の売上高データがない場合は、Adobeアカウントチームに問い合わせて、その日を売上高モデルから除外するよう依頼します。
+++

+++金額データが誤った形式で表示されます。
デフォルトでは、レポート内のすべての金額データは、米ドルの形式（1,000.00 など）で表示されます。 値を正しい通貨形式で（ただし、CSV 形式と TSV 形式の通貨記号を含まない）表示するには、[!UICONTROL Currency]」列に表示されます。 異なる通貨のアカウントのデータがレポートに含まれる場合、[!UICONTROL Total]「通貨の値は、通貨に関係なく、列内のすべての数値の合計に過ぎません。
+++

+++トランザクションプロパティに、自然数（1、2 など）である必要がある 10 進数値が表示されるのはなぜですか？
次の場合、10 進数の値が表示されます。

* コンバージョン属性ルールのパラメーターで、 [!UICONTROL Last Event] または [!UICONTROL First Event]に値を指定すると、売上高がコンバージョンパス内の複数のイベントに分割される場合があります。

* 内 [!UICONTROL Transaction Report]複数の場合は [入札単位](/help/search-social-commerce/glossary.md#a-b) 一致タイプが異なる場合、同じトランザクション ID を持つので、トラッキング ID の売上高は、指定したクリック日のクリック数に応じて分割されます。
+++

## 標準的なパフォーマンス指標

+++クリックデータがレポートに表示されません。
クリックデータがない一般的な理由を次に示します。

| 原因 | 検出/分析 | 解決策 |
|---|---|---|
| 広告アカウントからクリックデータを取得するプロセスが失敗しました。 | この問題を検出する体系的な方法はありませんが、広告アカウントがお金を使った場合でも、キャンペーンにコストやクリック情報が表示されないことに気付くかもしれません。 | カスタマーサポート ( &lt; ) にお問い合わせください。*検索、ソーシャル、コマースの各ユーザーアカウント*>@support\.efrontier\.com.<!-- Escaped periods and using HTML code for angle brackets --><br><br>データが 24 時間以上欠落している場合は、データが取得されるまで、原価予測からこれらの日付が除外されます。 Adobeアカウントチームが日付を除外できます。 |
| 広告主と広告ネットワークの間の請求の問題により、広告アカウントが使用できなくなります。 | この問題を検出する体系的な方法はありませんが、キャンペーンにコストやクリック情報が表示されないことに気付くかもしれません。 | 請求の問題が原因で広告アカウントが支出できなかったことがわかっている場合は、コスト予測からこれらの日付を除外します。 Adobeアカウントチームが日付を除外できます。 |
+++

+++パフォーマンスデータは、広告ネットワークエディターのデータとは異なります。
広告ネットワークが以前のデータに更新を送信する場合（多くの場合、クリックの不正を一部のクリックに起因させているため）、検索、ソーシャル、コマースは、5%以上の相違があり、Adobeアカウントチームがリクエストを送信しない限り、データを更新しません。

また、日付範囲をまたいで集計されたインプレッション共有データを比較する場合、検索、ソーシャル、コマースの各レポートに表示されるデータと広告ネットワークのレポートに表示されるデータが異なる場合があります。 これは、データが広告ネットワークの API によってどのようにレポートされるかという点が異なります。広告ネットワークの API は、Search、Social および Commerce がデータを取り込む際に使用するものです。 例： [!DNL Google Ads] データ：

* ほとんどのインプレッション共有指標では、 [!DNL Google Ads] は、10%未満または 90%超の値に対してレポートされる値の下限または上限を指定します。 データは、10%未満は 0.0999、90%超は 0.9001 としてレポートされます。

* 日付範囲内に大文字と小文字の区別がないデータが混在している場合、検索、ソーシャル、およびコマースは、API で送信された値をそのまま使用してインプレッションデータを集計し、行に 0.0999 を 10%未満、90%を超える行に 0.9001 を使用します。 この集計により、 [!DNL Google Ads] 次の理由で事前に集計されたデータ [!DNL Google Ads] は、7%や 97%など、実際の割合の値を使用できます。
+++

+++レポート内のパフォーマンスデータは、 [!DNL Google Analytics].
2 つのシステムは異なるデータを測定するので、異なるデータを表示する必要があります。 例：

* Search、Social、&amp;Commerce( およびGoogle Ads) でクリックを追跡するのに対し、 [!DNL Google Analytics] は、30 分のブラウザーセッションごとに訪問を追跡します。 例えば、ユーザーが広告を 1 回クリックし、「戻る」ボタンをクリックしてから広告を再度クリックすると、Search、Social、&amp;Commerce は 2 回のクリックを記録しますが、 [!DNL Google Analytics] は 1 回の訪問を記録します。

* [!DNL Google Analytics] 検索、ソーシャル、コマース ( および [!DNL Google Ads]) は、無効なクリック（過剰な、繰り返しのクリックなど）をフィルターします。

* [!DNL Google Analytics] には、すべてのクリックのクリック数と売上高のデータが含まれます。 Search, Social, &amp; Commerce では、トラッキング URL が正しくないか、見つからない広告およびキーワードのクリック数および売上高データを追跡できません。
+++

## コンバージョン指標

+++レポートにコンバージョンデータが表示されない。
このレポートには、コンバージョンが発生したコンバージョン指標が含まれていない場合があります。
+++

+++レポートに売上高がありません。

### Adobe広告コンバージョンタグを使用する広告主

#### 考えられる原因

* 検索、ソーシャル、およびコマースのクリック追跡プレフィックスをトラッキングテンプレートまたはリンク先 URL の前に付けずにキーワードまたは広告が追加された、またはトラッキングプレフィックスが正しくありません。

* 該当するすべての Web ページまたはが編集された場合、コンバージョントラッキングタグが正しく実装されていません。

* 検索、ソーシャル、コマースの各トラッキング対象のトランザクションプロパティは、レポートから除外されるので、表示されません。

* クライアントの収益パーサーが実装されませんでした。

#### 考えられる解決策または回避策

1. レポートまたはデータビューに正しい列が含まれていることを確認します。 正しい列を追加できない場合は、自分またはAdobeアカウントチームが [トランザクションプロパティをレポートで使用できるようにする](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. 該当するすべての Web ページに正しいコンバージョントラッキングタグが実装されていることを確認します。 必要に応じて、Adobeアカウントチームに、該当する各コンバージョントラッキングタグに対してテストトランザクションを作成し、トランザクションの詳細 ( `transactionid` Cookie からの詳細 ( `trackingid`, `clickid`など )。

1. この [!UICONTROL Auto Upload] 「 」オプションはキャンペーンに対して無効になっており、キーワードや広告を追加している場合は、それぞれ検索、ソーシャル、コマースのクリックリダイレクト追跡を含むトラッキングテンプレートまたはリンク先 URL を生成していることを確認します。 Adobeアカウントチームが内部レポートを実行して、クリック追跡 URL（トラッキングテンプレートまたは宛先 URL）が見つからないか、正しくないかを確認できます。

   必要に応じて、正しい URL を持つバルクシートファイルを作成し、 **トラッキング URL の生成** オプション。

   リンク先 URL は、「http://pixel.everesttech.net」または「https://pixel.everesttech.net」で始まる必要があります。

1. これらの手順で問題が解決されない場合は、 [カスタマーケアにお問い合わせください](/help/search-social-commerce/get-help.md).

   クライアントが起動されていないか、新たに起動された場合、カスタマーケアは売上高パーサーが設定されているかどうかを確認します。 パーサーが設定されている場合、Search、Social、&amp;Commerce がピクセル変換を受け取っているかどうかを確認し、問題のトラブルシューティングをおこないます。

### コンバージョンデータフィードを送信する広告主

#### 考えられる原因

* フィードファイルが配信されなかったか、完全に解析されなかったか、フィードにオーファントランザクションが含まれていました。

* 関連するトランザクションプロパティはレポートから除外されるので、表示されません。

>[!NOTE]
>
>通常、データは、フィードを受け取ってから 2 ～ 4 時間が経過するまで、ユーザーインターフェイスに表示されません。

#### 考えられる解決策または回避策

1. レポートまたはデータビューに正しい列が含まれていることを確認します。 正しい列を追加できない場合は、自分またはAdobeアカウントチームが [トランザクションプロパティをレポートで使用できるようにする](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-available.md).

1. を実行します。 [!UICONTROL Portfolio Report]. 値が空の場合は、 [!UICONTROL Campaign Report] および [!UICONTROL Search Engine Report] をクリックして、これらのレポートに売上高が表示されるかどうかを確認します。 割り当てられている場合、キャンペーンが適切なポートフォリオに割り当てられていない可能性があります。

1. ファイルが売上高サーバーに送信され、ファイルが以前のファイルと同じ形式および命名規則に従っていることを確認します。

   形式またはファイル命名規則が変更された場合は、ファイルを修正し、再送信します。

1. ファイルが送信された場合、 [カスタマーケアにお問い合わせください](/help/search-social-commerce/get-help.md).

   カスタマーケアは、ファイルが受信され、解析されたかどうかを確認します。 ファイルがエラーなしで処理された場合は、孤立したトランザクションを確認します。
+++

+++一部の高度なレポートには、広告主フィードが提供するコンバージョンデータが含まれていません。
この [!UICONTROL Geo Distribution Report] および [!UICONTROL Domain Referral Report] 広告コンバージョントラッキングサービスでAdobeされたデータを使用して、サービスを持つ広告主のみに対して生成できます。 レポートには、Adobe広告コンバージョントラッキングシステムの外部で追跡されるコンバージョンデータは含まれません。
+++

+++売上高データは、広告主独自の売上高データとは異なります。

### Adobe広告コンバージョンタグを使用する広告主

#### 考えられる原因

* Search、Social、および Commerce は、cookie の有効期限が切れたり削除されたりした場合に売上高を無視しますが、広告主は売上高を有効と見なす可能性があります。

* 広告主のページへのトラフィックは、広告からではなく、ブックマークまたはオーガニック検索から来ています。

* 該当するすべての Web ページまたはが編集された場合、コンバージョントラッキングタグが正しく実装されていません。

#### 考えられる解決策または回避策

1. に移動します。 **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** および [!UICONTROL Transaction Report]. Search、Social、および Commerce が受け取ったトランザクションを広告主のデータと比較します。

1. 一部のトランザクションが正しくない場合や見つからない場合は、該当するすべての Web ページに関連するコンバージョントラッキングタグが実装され、編集されないようにしてください (Adobeアカウントチームから通知を受けた場合 )。 Web サイトが最近更新された場合、タグが見つからないか、変更される可能性があります。

   検索、Social、および Commerce では、 `ef_transaction_properties` 変数と `src` 要素 `img` タグを使用します。

1. 問題を特定して解決できない場合は、 [カスタマーケアにお問い合わせください](/help/search-social-commerce/get-help.md).

   カスタマーケアは、見つからないトランザクションを特定し、広告から得られない孤立トランザクションおよびトランザクションを確認しようとします（「相関のないコンバージョン」）。

### を使用してコンバージョンデータフィードを持つ広告主 `ef_id` 値

上記のピクセル実装で考えられる原因と解決策を参照してください。

### トランザクション ID を使用したコンバージョンデータフィードを持つ広告主

#### 考えられる原因

* 検索、ソーシャル、コマースは、cookie の有効期限が切れたり削除されたりした場合に売上高を無視しますが、広告主は売上高を有効と見なす場合があります。

* 広告主のページへのトラフィックは、広告からではなく、ブックマークまたはオーガニック検索から来ています。

* 同じトランザクション ID を持つオンライントランザクションが発生する前に、オフラインコンバージョンがレポートされていました。 オンライントランザクションが最初に発生する必要があります。

#### 考えられる解決策または回避策

1. に移動します。 **[!UICONTROL Insights & Reports]>[!UICONTROL Reports]** および [!UICONTROL Transaction Report]. Search、Social、および Commerce が受け取ったトランザクションを広告主のフィードデータと比較します。

1. フィードファイル内のトランザクションがレポートにない場合は、同じトランザクション ID（ピクセルを介して追跡）を持つオンライントランザクションが、オフラインコンバージョンの前に発生したかどうかを確認します。

1. 問題を特定して解決できない場合は、 [カスタマーケアにお問い合わせください](/help/search-social-commerce/get-help.md).

   カスタマーケアは、データ解析エラーおよび [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p).

### 他のタイプのコンバージョンデータフィードを持つ広告主

#### 考えられる原因

* Search、Social、および Commerce は、cookie の有効期限が切れたり削除されたりした場合に売上高を無視しますが、広告主は売上高を有効と見なす可能性があります。

* 広告主のページへのトラフィックは、広告からではなく、ブックマークまたはオーガニック検索から来ています。

* 次のものがあります。 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p)したがって、Search、Social、&amp;Commerce は、必要な売上高をすべて数えていません。

* 広告主は、フィードで送信されたデータとは異なるデータセットに対して、検索、ソーシャル、コマースのレポートを検証しました。

* トランザクション ID (`ev_transid` 値 ) は送信されなかったか、一意でないか、正しくありません。

* フィードファイルに、重複したトラッキング ID が含まれています。

* ファイルを解析する際にエラーが発生しました。

* 広告主の重複排除ロジックは、検索、ソーシャル、コマースのロジックとは異なります。

#### 考えられる解決策または回避策

1. に移動します。 **[!UICONTROL Insights]&amp;[!UICONTROL Reports > Reports]** および [!UICONTROL Transaction Report]. Search、Social、および Commerce が受け取ったトランザクションを広告主のデータと比較します。

1. 一部のトランザクションが正しくないか、見つからない場合は、a) 必要なトランザクション ID がすべてフィードファイルに含まれ、重複するトラッキング ID がないこと、b) トランザクション ID が一意で正しいことを確認します。

1. 問題を特定して解決できない場合は、 [カスタマーケアにお問い合わせください](/help/search-social-commerce/get-help.md).

   カスタマーケアは、データ解析エラーとオーファントランザクションがないかを確認します。
+++

+++売上高データがAdobe Analyticsのデータと異なる。詳しくは、 [https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/data/data-variances.html).<!-- change link URL to relative link -->
+++

## 特定のレポート

+++ [!UICONTROL Portfolio Report] ～と同じ数字を示す [!UICONTROL Portfolios] 表示
この [!UICONTROL Portfolio Report] そして [!UICONTROL Portfolios] ビューとレポートのすべてのフィルター、レポートパラメーター、およびビューとレポートのデータ列が同じ場合は、同じデータが表示されます。 例えば、 [!UICONTROL Portfolios] 表示は、「[!UICONTROL All but inactive]&quot; （日付範囲）[!UICONTROL Last 7 days]」が表示され、デフォルトのデータ列のみが表示され、 [!UICONTROL Portfolio Report] デフォルトのパラメーターを使用すると、同じデータが表示されます。 レポートのパラメーターを変更した場合、または [!UICONTROL Portfolios] 表示する場合、データ値は異なる可能性があります。
+++

+++ [!UICONTROL Portfolio Report] が [!UICONTROL Search Engine Report] または [!UICONTROL Search Engine Account Report].
この [!UICONTROL Portfolio Report] 指定したポートフォリオに割り当てられたキャンペーンのデータのみを表示しますが、 [!UICONTROL Search Engine Report] および [!UICONTROL Search Engine Account Report] また、ポートフォリオに割り当てられていないキャンペーンのデータを含めることもできます。
+++

+++機能 [!UICONTROL Model Accuracy] > [!UICONTROL Forecast Accuracy Report] ポートフォリオレベルとは異なる [!UICONTROL Model Accuracy Report]?
( 代理店のアカウントマネージャー、Adobeのアカウントマネージャー、管理者のユーザーのみ ) [!UICONTROL Forecast Accuracy Report] 次の場所から利用可能： [!UICONTROL Reports] > [!UICONTROL Model Accuracy] は、ポートフォリオレベルと同じデータを提供します [!UICONTROL Model Accuracy Report] ただし、複数のポートフォリオにまたがって実行でき、アトリビューションルールを変更できる点が異なります。 また、カスタムパラメーターを使用してレポートを実行し、スケジュールを設定したり、それを使用してスプレッドシートフィードを作成したりすることもできます。 また、 [!UICONTROL Forecast Accuracy Report] は、現在の目標ではなくポートフォリオの目標履歴を使用して売上高の精度を評価し、適用されるタイムゾーンのデータをより正確に表すので、従来のポートフォリオレベルのレポートよりも正確です。
+++

+++広告レベルのデータは [!DNL Google Ads] 動的検索広告 (DSA)、パフォーマンスの最大値、スマートショッピング、 [!DNL YouTube] キャンペーン。
広告ネットワークは、売上高をキャンペーンの個々の広告に関連付けるのに必要な識別子を提供しません。 その結果、 [!UICONTROL Ads] 表示または [!UICONTROL Ad Variation Report]. キャンペーンの広告レベルの合計データとキャンペーンの合計データの間に相違が生じることを想定しています。
+++

+++ [!UICONTROL Transaction Report]、データフィードのトランザクションプロパティと、AdobeAdvertising トラッキングピクセルによってトラッキングされているトランザクションプロパティを知るには、どうすればよいですか。
トランザクションレポートで、カスタム列「[!UICONTROL Tracking URL].&quot; Adobe広告トラッキングピクセルを使用した URL のトラッキングは、「`http://pixel.everesttech.net`.&quot;
+++

+++ [!UICONTROL Transaction Report] が [!UICONTROL Keyword Report].
ポートフォリオ別に両方のレポートを生成する場合、 [!UICONTROL Keyword Report] 現在のキャンペーンのデータを使用するのではなく、履歴データ（指定した日付のポートフォリオ設定に基づく）を使用します。 次の場合に [!UICONTROL Transaction Report] ポートフォリオ別に、ポートフォリオ内の現在のキャンペーンのデータが含まれます。
+++

## スプレッドシートフィード

+++レポート出力には、様々な日付範囲が含まれます。
フィードが「[!UICONTROL Daily].&quot;

この問題を解決するには、毎日集計したデータを含めるようにスプレッドシートフィードを更新します。 このタスクには、レポートテンプレートの更新、テンプレートを使用したレポートの生成、カスタムの作成が含まれます [!DNL Microsoft® Excel] テンプレートを作成し、フィード設定を更新して新しい Excel テンプレートを含めます。 詳しくは、[スプレッドシートレポートフィード設定の編集](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++スプレッドシートフィードは内部エラーを引き起こします。
このエラーは、レポートテンプレートの列を変更したが、 [!DNL Microsoft® Excel] 適切なテンプレート

この問題を解決するには、スプレッドシートフィードを更新して新しい列を含めます。 このタスクには、レポートテンプレートの更新、テンプレートを使用したレポートの生成、カスタムの作成が含まれます [!DNL Excel] テンプレートを作成し、フィード設定を更新して新しい Excel テンプレートを含めます。 詳しくは、[スプレッドシートレポートフィード設定の編集](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++

+++ [!DNL Excel], [!DNL Excel] は「読み取れないコンテンツ」エラーを報告し、復元されたコンテンツからデータが削除されます。
次の場合に [!DNL Microsoft® Excel] template は開始日を昇順で並べ替えません。スプレッドシートフィードに空白行が含まれている場合があります。 特に [!DNL Excel] 「Excel で読み取り不能なコンテンツが「&lt;」で見つかりました」というエラーを報告します&#x200B;*レポート名*>.xlsx&#39; ワークブックの内容を復元しますか？ このブックのソースを信頼できる場合は、[ はい ] をクリックします。 「はい」をクリックすると、次のメッセージが表示されます。&quot;削除されたレコード：/xl/worksheets/sheet1.xmlの部分のセル情報、「」、およびスプレッドシートフィードに空白の行が含まれている。

問題を解決するには、 [!DNL Excel] データの並べ替えに使用するフィードに関連付けられたテンプレート [!DNL Start date in Ascending (Oldest to Newest) order]」をクリックし、更新したテンプレートをスプレッドシートフィード設定からアップロードします。 詳しくは、[スプレッドシートレポートフィードの編集](/help/search-social-commerce/reports/automation/spreadsheet-feeds/spreadsheet-feed-edit.md).&quot;
+++