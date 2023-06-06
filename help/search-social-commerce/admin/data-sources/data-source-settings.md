---
title: "[!DNL Google Analytics] データソース設定"
description: 次の必要な設定を参照してください： [!DNL Google Analytics] データソース。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '820'
ht-degree: 0%

---

# [!DNL Google Analytics] データソース設定

| セクション | パラメータ | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | の ID [!DNL Google Analytics] データの取り込み元となるアカウント。 データを取り込むための API 使用量は、すべて、指定したアカウントに請求されます。 アカウントは、指定された電子メールアドレスに対して「読み取りと分析」権限を付与する必要があります。<br><br>ID を見つけるには、にログインします。 [!DNL Google Analytics]. 左上で、 **[!DNL All accounts]** をクリックして、アカウントのリストを開きます。 各アカウントの ID は、アカウント名の下に表示されます。 |
|  | [!UICONTROL Google Analytics Login] | このデータソースのデータへのアクセスに使用するログイン/電子メールアドレスを指定します。 ログインは、 [!DNL Google] アカウントに追加し、 [!DNL Google Analytics] アカウント 詳しくは、 [でのユーザー権限の割り当て手順 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).<br><br><b>注意：</b> このログインアカウントのパスワードを変更すると、アカウントへのオープン接続はすべて閉じられます。 データの同期を再開するには、このページに戻り、 [再認証](data-source-reauthenticate.md). |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | ( 読み取り専用、接続されたアカウントのみ ) アカウント名。 |
|  | [!UICONTROL Google Analytics Property] | のデータを収集する元となるプロパティ（Web サイト、モバイルアプリケーションまたはデバイス） [!DNL Google Analytics] アカウント<br><br> 複数のプロパティの指標を統合するには、プロパティごとに個別のデータソースを設定します。 |
|  | [!UICONTROL Google Analytics View] | アクセスするデータセットを含むビュー。 プロパティに複数のビューがある場合は、すべてのデータを含む、フィルターを適用していないビューを最上位レベルで取り込むことを検討してください。<br><br>同じプロパティに対して複数のビューの指標を統合するには、ビューごとに個別のデータソースを設定します。 ビューに重複するデータが含まれていないことを確認します。 |
|  | [!UICONTROL Google Analytics Dimension] | この [!DNL Google Analytics] Adobe広告の「ef_id」クエリー文字列パラメーターの値が設定されたカスタムディメンション。 正しいディメンションが表示されない場合は、 [!DNL Google Analytics] 実装チーム。<br><br>「ef_id」は、データを渡す主キーとして使用されます。 [!DNL Google Analytics] をAdobe広告に追加します。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定した [!DNL Google Analytics] データソース用に読み込まれない、カテゴリ別に整理されたプロパティおよびビュー。 このリストには、インポートされたわかりやすい名前とバックエンド名が含まれます（「ga」で始まります）。 を設定します。 この [!UICONTROL Refresh] 「 」ボタンをクリックすると、リストが [!DNL Google Analytics].<br><br>使用可能な指標をインポートするには、 [!UICONTROL Selected Metrics] 」セクションに入力します。<br><br>参照：[利用可能 [!DNL Google Analytics] Advertising Cloudの指標](data-source-ga-metrics.md).&quot; |
|  | 選択した指標 | 指定した [!DNL Google Analytics] データソース用にインポートされるプロパティおよびビュー、および各指標の検証ステータス。 このリストには、インポートされたわかりやすい名前とバックエンド名 (「`ga.`」) を使用します。 各データソースには、削除できない 4 つのデフォルトのトラフィック指標 ([!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces]、および [!UICONTROL Session Duration]) と、データを含まない最大 16 個の追加の有効な指標または指標。 指標リストはいつでも編集できます。<br><br>指標をインポートするには、 [!UICONTROL Available Metrics] ウィンドウを開き、ここにドラッグします。<br><br><b>注意：</b> [!DNL Google Analytics] では、1 つのデータフィードで最大 10 個の指標を許可します。 Search、Social、および Commerce の各データソースには、合計 20 個の指標を持つ最大 2 つのフィードを含めることができますが、2 番目のフィードを使用すると、API 呼び出しを [!DNL Google Analytics]. 指標が多い場合は、最適化の目的で使用する指標のみを選択します。 このプロジェクトのクォータは、で表示できます。 [の [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas). 詳しくは、 [への API リクエストのクォータと呼び出し制限 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).<br><br><b>メモ：</b><br><ul><li>わかりやすい名前は、 [!UICONTROL Admin] > [!UICONTROL Transactions Properties] 表示され、「_ga」が付加されます。&lt;metric_tag configured=&quot;&quot; in=&quot;&quot; the=&quot;&quot; metric=&quot;&quot; tag=&quot;&quot; field=&quot;&quot;></code>&quot; （例： &quot;Pageviews_ga:UK&quot;）。 オプションで、カスタム目標とカスタム指標の表示名を編集できますが、一般的な指標の表示名はすべて、 [!DNL Google Analytics]指定したタグが付加された</li><li>ページビュー数、セッション数、直帰率（バウンス/セッションとして計算）、セッション期間は、ポートフォリオ入札アルゴリズムに自動的に考慮されます。 ポートフォリオの目標には、他の指標を手動で追加できます。</li><li>データソースから指標を削除すると、Adobe広告では、通常の [データ保持ポリシー](/help/search-social-commerce/reports/data-used-for-reports.md).</li></ul> |
| 指標タグ | 指標タグ | 選択した各項目に追加するタグ [!DNL Google Analytics] Adobe広告の指標。先頭に「_ga:</code>&quot; ( 例： &quot;Pageviews_ga:&lt;metric_tag>&quot;) です。 タグには 2 ～ 5 文字の英数字を使用でき、広告主で一意である必要があります。<br><br>このタグを使用すると、各指標のデータソースを識別できます。 各データソースには同じ指標名 ( [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces]、および [!UICONTROL Session Duration]、および潜在的に他の指標 )。 異なる指標タグを追加すると、指標名が重複するのを防ぎます。<br><br>例えば、UK プロパティと JP プロパティに対して個別の統合を設定する場合、指標タグとして「UK」と「JP」を使用できます。 この [!UICONTROL Pageviews] 次に、2 つのプロパティの指標が、Adobe広告で「Pageviews_ga:UK」および「Pageviews_ga:JP」として適切に表示されます。 |

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics] コンバージョン指標](data-source-about.md)
>* [の設定の前提条件 [!DNL Google Analytics] データソース](data-source-prerequisites.md)
>* [の設定 [!DNL Google Analytics] データソースとして表示](data-source-configure.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [の再認証 [!DNL Google Analytics] データソース](data-source-reauthenticate.md)
>* [付録 — 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)

