---
title: '[!DNL Google Analytics] データソース設定'
description: ' [!DNL Google Analytics]  データソースに必要な設定を参照してください。'
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
TQID: https://experienceleague.adobe.com/EvCJTrEFxRU87kUlKCZ-rN3jtNVjSkVGmrHCNsPMElw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 799
ht-degree: 0%

---

# [!DNL Google Analytics] データソース設定

| セクション | パラメーター | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | データの取得元となる[!DNL Google Analytics] アカウントのID。 データを引き出すためのすべてのAPI使用は、指定したアカウントに請求されます。 アカウントは、指定された電子メールアドレスに「読み取りと分析」権限を付与する必要があります。<br><br>自分のIDを見つけるには、[!DNL Google Analytics]にログインしてください。 左上の「**[!DNL All accounts]**」をクリックして、アカウントのリストを開きます。 各アカウントのIDは、アカウント名の下にあります。 |
| | [!UICONTROL Google Analytics Login] | このデータソースのデータへのアクセスに使用するログイン/電子メールアドレスを指定します。 ログインは[!DNL Google] アカウントに登録し、[!DNL Google Analytics] アカウントに「読み取りと分析」権限を持っている必要があります。 [ [!DNL Google Analytics]でユーザー権限を割り当てる方法については、](https://support.google.com/analytics/answer/9305587)の手順を参照してください。<br><br><b> メモ：</b>このログインアカウントのパスワードを変更すると、アカウントに対して開いているすべての接続が閉じられます。 データの同期を再開するには、このページに戻り、[再認証](data-source-reauthenticate.md)してください。 |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （読み取り専用、接続されたアカウントのみ） アカウント名。 |
| | [!UICONTROL Google Analytics Property] | [!DNL Google Analytics] アカウントのデータを収集するプロパティ （web サイト、モバイルアプリケーション、またはデバイス）。<br><br>複数のプロパティの指標を統合するには、各プロパティに個別のデータソースを設定します。 |
| | [!UICONTROL Google Analytics View] | アクセスするデータセットを含むビュー。 プロパティに複数のビューがある場合は、すべてのデータを含む、フィルタリングされていないビューを最上位レベルで引き出すことを検討してください。<br><br>同じプロパティの複数のビューの指標を統合するには、各ビューに個別のデータソースを設定します。 ビューに重複データが含まれていないことを確認します。 |
| | [!UICONTROL Google Analytics Dimension] | Adobe Advertisingの「ef_id」クエリ文字列パラメーターの値が入力された[!DNL Google Analytics] カスタムディメンション。 正しいディメンションが表示されない場合は、[!DNL Google Analytics]実装チームにお問い合わせください。<br><br> 「ef_id」は、[!DNL Google Analytics]からAdobe Advertisingにデータを渡すプライマリキーとして使用されます。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | 指定された[!DNL Google Analytics] プロパティおよびデータソースにインポートされていないビューの使用可能なすべての指標（カテゴリ別）。 リストには、読み込まれたフレンドリ名とバックエンド名（「ga」で始まる）が含まれます。 個別のダイアログを作成できます。 [!UICONTROL Refresh] ボタンは、[!DNL Google Analytics]の新しい指標を使用してリストを更新します。<br><br>使用可能な指標を読み込むには、[!UICONTROL Selected Metrics] セクションにドラッグします。<br><br>Advertising Cloud[の「 [!DNL Google Analytics] 利用可能](data-source-ga-metrics.md)指標」を参照してください。」 |
| | 選択した指標 | データソースにインポートされる指定された[!DNL Google Analytics] プロパティとビューのすべての指標、および各指標の検証ステータス。 リストには、各指標のインポートされたフレンドリ名とバックエンド名（「`ga.`」で始まる）が含まれます。 各データソースには、削除できない4つのデフォルトのトラフィック指標（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]、および[!UICONTROL Session Duration]）と、データを含まない追加の有効な指標または指標を最大16個まで含めることができます。 指標リストはいつでも編集できます。<br><br>指標を読み込むには、[!UICONTROL Available Metrics] ペインで指標を選択し、ここにドラッグします。<br><br><b>注意：</b> [!DNL Google Analytics]は、1つのデータフィードで最大10個の指標を許可します。 Search, Social, &amp; Commerceの各データソースには、合計20個の指標を含む最大2つのフィードを含めることができますが、2番目のフィードを使用すると、API呼び出しが[!DNL Google Analytics]に2倍になります。 多数の指標がある場合は、目的で最適化に使用する指標のみを選択します。 このプロジェクトの割り当てを[the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas)で表示できます。 [ [!DNL Google Analytics]へのAPI リクエストの](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)割り当てと呼び出し制限について詳しく説明します。<br><br><b> メモ：</b><br><ul><li>フレンドリ名は、[!UICONTROL Admin] > [!UICONTROL Transactions Properties] ビューで指標の表示名として読み込まれ、「<code>_ga:&lt;指標タグ フィールドで設定された指標タグ >」が追加されます</code>&quot;（&quot;Pageviews_ga:UK&quot;など）。 必要に応じて、カスタム目標とカスタム指標の表示名を編集できますが、すべての一般的な指標の表示名は、指定されたタグが付いた[!DNL Google Analytics]のわかりやすい名前で毎日上書きされます。</li><li>ページビュー、セッション、バウンス率（バウンス/セッションとして計算）、セッション時間は、自動的にポートフォリオ入札アルゴリズムに組み込まれます。 他の指標を手動でポートフォリオ目標に追加できます。</li><li>データソースから指標を削除すると、Adobe Advertisingは通常の[ データ保持ポリシー](/help/search-social-commerce/reports/data-used-for-reports.md)に従って履歴データを保持します。</li></ul> |
| 指標タグ | 指標タグ | Adobe Advertisingで選択した各指標[!DNL Google Analytics]に追加するタグ。その前に「<code>_ga:</code>「（&quot;Pageviews_ga:&lt;metric_tag>&quot;など）。 タグは2 ～ 5文字の英数字で指定でき、広告主に対して一意である必要があります。<br><br>このタグは、各指標のデータソースを特定するのに役立ちます。 このタグは、複数のデータソースを設定する場合に特に重要です。各データソースには、同じ指標名（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]、[!UICONTROL Session Duration]、その他の可能性のある指標など）が含まれているからです。 異なる指標タグを追加すると、指標の名前が重複しなくなります。<br><br>例えば、英国のプロパティとJP プロパティに対して個別の統合を設定する場合、指標タグとして「UK」と「JP」を使用できます。 2つのプロパティの[!UICONTROL Pageviews]指標は、Adobe Advertisingでは「Pageviews_ga:UK」および「Pageviews_ga:JP」として適切に表示されます。 |

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics]  コンバージョン指標](data-source-about.md)
>* [ データソースを設定するための前提条件 [!DNL Google Analytics] ](data-source-prerequisites.md)
>* [ データソースとして [!DNL Google Analytics]  ビューを設定](data-source-configure.md)
>* [ データソースの編集 [!DNL Google Analytics] ](data-source-edit.md)
>* [ データソースの同期を一時停止](data-source-pause.md)
>* [ データソースを再認証 [!DNL Google Analytics] します](data-source-reauthenticate.md)
>* [付録 – 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
