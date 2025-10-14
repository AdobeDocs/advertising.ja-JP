---
title: '[!DNL Google Analytics] データソース設定'
description: データソースに必要な設定  [!DNL Google Analytics]  参照します。
role: User, Admin
exl-id: 78422c2c-ed58-410e-8996-882759ed5556
feature: Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '802'
ht-degree: 0%

---

# [!DNL Google Analytics] データソース設定

| セクション | パラメーター | 説明 |
| ---- | ---- | ---- |
| [!UICONTROL Connect to Google Analytics] | [!UICONTROL Google Analytics Account ID] | データの取得元である [!DNL Google Analytics] アカウントの ID。 データを取り込むための API の使用はすべて、指定されたアカウントに請求されます。 アカウントは、指定されたメールアドレスに「読み取りと分析」権限を付与する必要があります。<br><br>ID を見つけるには、[!DNL Google Analytics] にログインします。 左上で、「**[!DNL All accounts]**」をクリックして、アカウントのリストを開きます。 各アカウントの ID は、アカウント名の下に表示されます。 |
| | [!UICONTROL Google Analytics Login] | このデータソースのデータへのアクセスに使用するログイン / メールアドレスを指定します。 ログインは、[!DNL Google] アカウントに登録され、[!DNL Google Analytics] アカウントの「読み取りと分析」権限を持っている必要があります。 [&#x200B; のユーザー権限の割り当て手順  [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587) を参照してください。<br><br><b> 注意：</b> このログインアカウントのパスワードを変更すると、そのアカウントへの開いているすべての接続が閉じられます。 データの同期を再開するには、このページに戻って [&#x200B; 再認証 &#x200B;](data-source-reauthenticate.md) してください。 |
| [!UICONTROL Account Details] | [!UICONTROL Google Analytics Account Name] | （読み取り専用。接続されたアカウントのみ）アカウント名。 |
| | [!UICONTROL Google Analytics Property] | [!DNL Google Analytics] アカウントのデータを収集するプロパティ（web サイト、モバイルアプリケーション、またはデバイス）。<br><br> 複数のプロパティの指標を統合するには、プロパティごとに個別のデータソースを設定します。 |
| | [!UICONTROL Google Analytics View] | アクセスするデータセットを含むビュー。 プロパティに複数のビューがある場合は、フィルタリングされていないビューをすべてのデータを含む最上位レベルに取り込むことを検討します。<br><br> 同じプロパティの複数ビューの指標を統合するには、ビューごとに個別のデータソースを設定します。 ビューに重複するデータが含まれていないことを確認します。 |
| | [!UICONTROL Google Analytics Dimension] | Adobe Advertising「ef_id」クエリ文字列パラメーターの値が入力された [!DNL Google Analytics] カスタムディメンション。 正しいディメンションがリストに表示されない場合は、[!DNL Google Analytics] 実装チームにお問い合わせください。<br><br> 「ef_id」は、[!DNL Google Analytics] からAdobe Advertisingにデータを渡すためのプライマリキーとして使用されます。 |
| [!UICONTROL Import Metrics] | [!UICONTROL Available Metrics] | データ ソース用にインポートされていない、指定した [!DNL Google Analytics] プロパティおよびビューで利用可能なすべての指標を、カテゴリ別に整理します。 リストには、読み込んだわかりやすい名前とバックエンド名（「ga」で始まる）が含まれています。 各指標の。 「[!UICONTROL Refresh]」ボタンをクリックすると、[!DNL Google Analytics] 内の新しい指標でリストが更新されます。<br><br> 使用可能な指標をインポートするには、指標を「[!UICONTROL Selected Metrics]」セクションにドラッグします。<br><br> 「Advertising Cloudで利用可能  [!DNL Google Analytics]  指標 [&#x200B; を参照 &#x200B;](data-source-ga-metrics.md)。 |
| | 選択された指標 | データソースにインポートされた、指定した [!DNL Google Analytics] プロパティおよびビューのすべての指標、各指標の検証ステータス。 リストには、読み込んだ各指標のわかりやすい名前とバックエンド名（「`ga.`」で始まる）が含まれます。 各データソースには、削除できない 4 つのデフォルトのトラフィック指標（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces] および [!UICONTROL Session Duration]）と、データがない最大 16 の追加の有効な指標または指標を含めることができます。 指標リストはいつでも編集できます。<br><br> 指標をインポートするには、[!UICONTROL Available Metrics] ウィンドウ枠で指標を選択し、ここにドラッグします。<br><br><b> 注意：</b> [!DNL Google Analytics] では、1 つのデータフィードに最大 10 個の指標を使用できます。 検索、ソーシャル、Commerceの各データソースには、合計 20 個の指標を持つ最大 2 つのフィードを含めることができますが、2 番目のフィードを使用すると、[!DNL Google Analytics] への API 呼び出しが 2 倍になります。 指標が多数ある場合は、最適化の目標で使用する指標のみを選択します。 このプロジェクトの割り当て量は、[the [!DNL Google API Console]](https://console.developers.google.com/apis/api/analytics-json.googleapis.com/quotas) で確認できます。 [&#x200B; への API リクエストの割り当て量と呼び出し制限  [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) の詳細を参照してください。<br><br><b> 注：</b><br><ul><li>わかりやすい名前が、[!UICONTROL Admin] > [!UICONTROL Transactions Properties] ビューで指標の表示名として読み込まれ、「<code>_ga:&lt;metric_tag が指標タグフィールドに設定されています ></code>&quot;（「Pageviews_ga:UK」など）。 必要に応じて、カスタム目標とカスタム指標の表示名を編集できますが、すべての一般的な指標の表示名は毎日、[!DNL Google Analytics] のわかりやすい名前に指定されたタグを付けて上書きされます。</li><li>ページビュー、セッション、バウンス率（バウンス/セッションとして計算）、セッション時間は、ポートフォリオ入札アルゴリズムに自動的に組み込まれます。 その他の指標は、ポートフォリオ目標に手動で追加できます。</li><li>データソースから指標を削除すると、Adobe Advertisingでは、通常の [&#x200B; データ保持ポリシー &#x200B;](/help/search-social-commerce/reports/data-used-for-reports.md) に従って履歴データが保持されます。</li></ul> |
| 指標タグ | 指標タグ | Adobe Advertisingで選択された各 [!DNL Google Analytics] 指標に追加するタグ。先頭に「<code>_ga:</code>&quot;（「Pageviews_ga:&lt;metric_tag>」など）。 タグは 2～5 文字の英数字で、広告主にとって一意である必要があります。<br><br> このタグを使用すると、各指標のデータソースを特定できます。 複数のデータソースを設定する場合、このタグが特に重要になります。各データソースには、一部の同じ指標名（[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces] および [!UICONTROL Session Duration] のほか、場合によってはその他の指標も含む）が含まれるからです。 異なる指標タグを追加すると、指標名が重複するのを防ぐことができます。<br><br> 例えば、UK プロパティと JP プロパティに別々の統合を設定した場合、指標のタグとして「UK」と「JP」を使用することができます。 2 つのプロパティの [!UICONTROL Pageviews] の指標は、Adobe Advertisingでは「Pageviews_ga:UK」および「Pageviews_ga:JP」として適切に表示されます。 |

>[!MORELIKETHIS]
>
>* [&#x200B; 同期  [!DNL Google Analytics]  コンバージョン指標について &#x200B;](data-source-about.md)
>* [&#x200B; データソースを設定するため  [!DNL Google Analytics]  前提条件 &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースとして  [!DNL Google Analytics]  ビューを設定する &#x200B;](data-source-configure.md)
>* [&#x200B; データソース  [!DNL Google Analytics]  編集 &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期の一時停止 &#x200B;](data-source-pause.md)
>* [&#x200B; データソース  [!DNL Google Analytics]  再認証 &#x200B;](data-source-reauthenticate.md)
>* [&#x200B; 付録 – 利用可能  [!DNL Google Analytics]  指標 &#x200B;](data-source-ga-metrics.md)
