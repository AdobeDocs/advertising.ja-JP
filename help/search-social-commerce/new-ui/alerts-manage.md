---
title: （新しいUI）カスタムアラートの管理
description: カスタムアラートとアラートテンプレートを作成、設定、一時停止、アクティベート、削除、表示、エクスポートする方法について説明します。
feature: Search Alerts
source-git-commit: 0fddeb8f01bd7c310544973ae2aff78339eb2144
workflow-type: tm+mt
source-wordcount: '1065'
ht-degree: 0%

---

# （新しいUI）カスタムアラートの管理

ポートフォリオ、キャンペーン、広告グループが、指定された期間内にパフォーマンス指標などの特定の条件を満たしたかどうかを特定するためのアラートテンプレートを作成し、アラートを生成します。 アラートは、1人の広告主に対して使用できます。 アラートには、関連するデフォルトビューのすべての列が含まれます。 例えば、キャンペーンレベルのアラートでは、デフォルトの[!UICONTROL Campaigns] ビューにすべての列が含まれます。

アラートテンプレートは、[!UICONTROL Custom Alerts] パネルの[!UICONTROL Alert Templates] タブまたは任意のページの上部から作成できます。

アラートテンプレートに対してアラートインスタンスがトリガーされる場合：

* 指定した受信者にメール通知が送信されます。 アラートに最大1000件のレコードが含まれる場合、メール通知には、アラートをトリガーしたすべてのエンティティのデータを含む、アラートデータを含む[CSV](/help/search-social-commerce/glossary.md#c-d) ファイルが含まれます。

* アラートは、[!UICONTROL Custom Alert Templates] パネルの[!UICONTROL Triggered Alerts] タブに表示されます。<!-- Not available as of 5/22 for alerts triggered the day before:  A downloadable report is available for ten days after the alert is triggered. -->

<!-- This doesn't seem to be true as of 5/22 -- check on this behavior:    * The alert is listed in the [!UICONTROL Notifications] center in the applicable entity view, which is available from the right toolbar. Notifications remain in the [!UICONTROL Notifications] center unless you delete them or mark them as read. -->

## [!UICONTROL Custom Alerts] ビュー

[!UICONTROL Custom Alerts] パネルを開くには、右上の![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ")をクリックします。

[!UICONTROL Custom Alerts] パネルには、[!UICONTROL Alert Templates] ビューが含まれています。このビューには、アカウント用に作成されたすべてのアラートテンプレートが一覧表示され、そこからアラートテンプレートを作成、編集、一時停止、再アクティブ化および削除できます。 [!UICONTROL Triggered Alerts] ビューには、生成されたアラート インスタンスが一覧表示されます。

## 使用可能なアクション

* [トリガーされたアラートの表示](#alert-view)

* [カスタムアラートテンプレートの表示](#alert-template-view)

* [カスタムアラートテンプレートの作成](#alert-template-create)

* [カスタムアラートテンプレートの編集](#alert-template-edit)

* [カスタムアラートテンプレートの一時停止](#alert-template-pause)

* [カスタムアラートテンプレートのアクティベーション](#alert-template-activate)

* [カスタムアラートテンプレートの削除](#alert-template-delete)

<!-- Not available as of 5/22:  * [Export data for triggered alerts](#alert-export-data) -->

## トリガーされたアラートの表示 {#alert-view}

1. 任意のページの右上にある「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ")」をクリックします。

1. 「**[!UICONTROL Triggered Alerts]**」タブをクリックします。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

## カスタムアラートテンプレートの表示 {#alert-template-view}

1. 任意のページの右上にある「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ")」をクリックすると、[!UICONTROL Alert Templates] タブが開きます。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

1. （オプション）アラートテンプレートのすべての条件を表示するには、条件の数をクリックします（![ カスタムアラート条件の例ボタン ](/help/search-social-commerce/assets/custom-alert-criteria.png " カスタムアラート条件の例ボタン ")など）。

## カスタムアラートテンプレートの作成 {#alert-template-create}

新しいアラートテンプレートのステータスは「[!UICONTROL Active]」です。

1. 次のいずれかの操作を行います。

   * 任意のページの右上で、![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL Create Custom Alert]**&#x200B;をクリックします。

   任意のページの右上にある「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL View Custom Alerts]**」をクリックすると、「[!UICONTROL Alert Templates]」タブが開きます。 **[!UICONTROL Create Alert]**&#x200B;をクリックします。

1. [ アラート設定](#alert-template-settings)を&#x200B;**[!UICONTROL Entity]**、**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**&#x200B;および&#x200B;**[!UICONTROL Scheduling and Delivery]** タブで指定します。

   タブ間を移動するには、タブ名（「フィルター」など）をクリックするか、右下の&#x200B;**[!UICONTROL Next]**&#x200B;をクリックします。

1. 「[!UICONTROL Summary]」タブで、「**[!UICONTROL Create Alert]**」をクリックします。

## カスタムアラートテンプレートの編集 {#alert-template-edit}

1. 右上の「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL View Custom Alerts]**」をクリックすると、「[!UICONTROL Alert Templates]」タブが開きます。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

1. テンプレート名の横にある「![編集](/help/search-social-commerce/assets/edit-new.png "編集")」をクリックします。

1. [!UICONTROL Edit Custom Alert] ウィンドウで、**[!UICONTROL Date Range]**、**[!UICONTROL Filters]**、および&#x200B;**[!UICONTROL Scheduling and Delivery]** タブの[ アラート設定](#alert-template-settings)を編集します。

   タブ間を移動するには、タブ名（「フィルター」など）をクリックするか、右下の&#x200B;**[!UICONTROL Next]**&#x200B;をクリックします。

1. 「[!UICONTROL Summary]」タブで、「**[!UICONTROL Update Alert]**」をクリックします。

## カスタムアラートテンプレートの一時停止 {#alert-template-pause}

1. 右上の「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL View Custom Alerts]**」をクリックすると、「[!UICONTROL Alert Templates]」タブが開きます。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

1. テンプレート行で、*[!UICONTROL Paused]*&#x200B;を選択します。

## カスタムアラートテンプレートのアクティベーション {#alert-template-activate}

1. 右上の「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL View Custom Alerts]**」をクリックすると、「[!UICONTROL Alert Templates]」タブが開きます。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

1. テンプレート行で、*[!UICONTROL Active]*&#x200B;を選択します。

## カスタムアラートテンプレートの削除 {#alert-template-delete}

削除できるのは、作成したアラートテンプレートのみです。

1. 右上の「![ カスタムアラート ](/help/search-social-commerce/assets/custom-alert.png " カスタムアラート ") > **[!UICONTROL View Custom Alerts]**」をクリックすると、「[!UICONTROL Alert Templates]」タブが開きます。

1. （オプション）リストをフィルタリングして、特定のエンティティタイプのアラートを含めるか、テンプレート名内のテキスト文字列を検索します。 検索クエリでは、大文字と小文字は区別されません。

1. テンプレート行で、![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

1. 確認メッセージ ボックスで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## カスタムアラートテンプレート設定 {#alert-template-settings}

| Tab | パラメーター | 説明 |
|--- |--- |--- |
|  | [!UICONTROL Name] | アラート名。 5文字以上を含める必要があります。 |
| [!UICONTROL Date Range] | [!UICONTROL Select Entity] | 評価するエンティティの種類：<i>[!UICONTROL Portfolio]</i>、<i>[!UICONTROL Campaign]</i>、または<i>[!UICONTROL Ad Group]</i>。 |
| [!UICONTROL Date Range] | [!UICONTROL Period] | アラートの条件を評価する日付範囲。 指標は、日付範囲をまたいで集計して評価されます。 オプションの範囲は&#x200B;*[!UICONTROL Yesterday]*&#x200B;から&#x200B;*[!UICONTROL Last 180 Days]*&#x200B;です。 |
| [!UICONTROL Filters] | \[定義されたフィルター\] | [!UICONTROL Scheduling and Delivery] タブで指定された時点でアラートをトリガーするための条件。 使用可能な列は、エンティティタイプによって異なります。 すべてのフィルターはブール関数ANDを使用して結合されます。つまり、指定したすべての条件を満たす必要があります。<ul><li><p>フィルターを追加するには、次の操作を行います。<p><ol><li><p>（オプション）列名をテキスト文字列でフィルタリングするには、[!UICONTROL ADD FILTER]入力フィールドに検索文字列を入力します。</p></li><li><p>列リストで、列名を選択します。</p></li><li><p>列にフィルターを定義します。</p></li><ul><li><p>（入力フィールドのないフィルター） 2番目のメニューの横にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、含める各値の横にあるチェックボックスを選択します。</p></li><li><p>（入力フィールドを持つその他のすべてのフィルター） 2番目のメニューから演算子を選択し、該当する値を入力します。</p><p>例えば、「クリック数」列を選択し、100回を超えるクリック数の行のみを返す場合は、「より大きい」を選択し、入力フィールドに100と入力します。</p><p>データ型に応じて、使用可能な演算子には、<i>1}より大きい、<i>より小さい</i>、<i>等しい</i>、<i>含む</i>、<i>含まない</i>、<i>から始まる</i>、<i>値なし</i>、<i>値なし</i>、</i>前</i>後<i>または<i>日付3}が含まれます。</i><i></i><i></i></p><p>**注意：** テキスト値では、大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンで絞り込むと、「消費者ローン」や「ローン申し込み」などの結果が得られます。</p></li></ol><li><p>フィルターを削除するには、フィルター定義の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Trigger this Alert] \[when\] | アラートが指定された条件フィルターをチェックする頻度と、すべての条件が満たされると、メール通知を送信する頻度：<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*週の日*> （&lt;*NN*> `[AM\|PM]`]）</p></li><li><p>[!UICONTROL Every month on <*日NN*> （&lt;*NN*> `[AM\|PM]`]）</p></li></ul>**注：**&#x200B;この値は、評価期間には影響しません。 |
|  | [!UICONTROL Email Recipients] | （アラートテンプレートの作成者のみが編集できます。他のユーザーは読み取り専用）登録済み検索、ソーシャル、およびCommerce ユーザーがアラートがトリガーされたときに通知を送信する。 デフォルトでは、ユーザーアカウントの名前が選択されています。 オプションで、広告主のデータへのアクセス権を持つユーザーを追加または削除します。<br><br> アラートに最大1000件のレコードが含まれる場合、アラートのCSV バージョンがメールメッセージに添付されます。 |

<!--

Not available as of 5/22:

## Export data for triggered alerts {#alert-export-data}

You can export data for a triggered alert or data for the most recently triggered alert for an alert template as a [!DNL Microsoft Excel] workbook ([XLS](/help/search-social-commerce/glossary.md#w-x) file), a tab-separated values ([TSV](/help/search-social-commerce/glossary.md#s-t)) file, or a comma-separated values ([CSV](/help/search-social-commerce/glossary.md#c-d)) file. Downloadable reports are available for ten days after the alert is triggered and are then automatically deleted.

1. Do either of the following:

   * (To export data for the most recently triggered alert for an alert template) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert") > **[!UICONTROL View Custom Alerts]**, which opens to the [!UICONTROL Alert Templates] tab.

   * (To export data for a specific triggered alert) In the upper right, click ![Custom Alert](/help/search-social-commerce/assets/custom-alert.png "Custom Alert"). Click **[!UICONTROL Triggered Alerts]**.

1. In the [!UICONTROL Export] column next to the template or report name, click the name of a format, and then open or save the file according to your browser's normal procedure:

   * **[!UICONTROL XLS]:** For an [!DNL Excel] workbook with a single worksheet (XLS). The report includes one worksheet, labeled at the top with the parameters, with one row for each included component when data for the component is available. Rows with no data are omitted. Basic reports include a total for each numeric column.

   * **[!UICONTROL TSV]:** For a TSV file. The report includes the parameters and one row for each included component.

   * **[!UICONTROL CSV]:** For a CSV file. The report includes the parameters and one row for each included component.

-->
