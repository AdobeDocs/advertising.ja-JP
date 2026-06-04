---
title: 検索入札単位の制約の管理
description: 従来のキーワードレベルのポートフォリオで、CPC キャンペーンの入札単位の入札を制限する制約について説明します。
feature: Search Campaign Management, Search Optimization
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2:
  - id: c800239a-06eb-4249-9aef-771973d24d35
source-git-commit: 9cc395a6b0fe25435ca6ed022f8da767d525d68e
workflow-type: tm+mt
source-wordcount: 2660
ht-degree: 0%

---

# 検索入札単位の制約の管理

*従来のキーワードレベルのポートフォリオのCPC キャンペーンの入札単位にのみ適用*

入札単位の制約は、制約に関連付けられたコストと収益モデルを使用して、すべての[入札単位](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/glossary.html)に対して最適化された入札を制限するルールです。

## 制約について

各制約は特定の通貨に適用され、オプションで、ルールを適用するために指定されたデータ評価期間中に満たす必要があるトリガー条件を含みます。 評価するデータには、チャネルタイプ、一致タイプ、クリックデータ、コンバージョンデータ、派生指標などを含めることができます。 例えば、入札を特定の金銭範囲に制限したり、指定された金額だけ入札を継続的に増減したり、ポートフォリオの平均入札に応じて入札したりできます。 各制約には適用可能な開始日があり、特定の日付に有効期限が切れるか、無期限に適用されます。

制約を設定したら、特定の入札単位または特定の広告グループまたはキャンペーン内のすべての入札単位に割り当てることができます。 各入札ユニットには、1つの制約を設定できます。 制約は子エンティティによって継承されますが、上書きできます。 最下位レベルで割り当てられた制約は、常に親レベルで割り当てられた制約を上書きします。 入札単位に制約を割り当てると、入札単位にコストと収益モデルがある場合、入札単位が生成する収益の量に関係なく、入札単位に指定された制約の範囲内で入札が実行されます。

>[!CAUTION]
>
>入札単位に制約を割り当てる場合、入札最適化システムの決定を上書きし、その入札単位のROIに対して自分で責任を負います。

>[!NOTE]
>
>* アクティブな制約は、最適化された従来のキーワードレベルのポートフォリオで、割り当てられた入札単位のみに対して入札を制限します。 ハイブリッドポートフォリオ内の入札単位やアクティブなポートフォリオ内の入札単位、またはポートフォリオ内にない入札単位では無視されます。 **ヒント：** ポートフォリオ設定で、「キャンペーンの予算制限を自動調整」に対するポートフォリオオプションをオンにします。 推奨される「複数」の値は「1」です。
>* 入札制限は、コストと収益モデルを生成するのに十分なデータがない入札単位では無視されます。
>* （CPCまたはeCPC入札戦略を使用したキャンペーン）入札制約がポートフォリオレベルの入札制限と競合する場合、その制約はポートフォリオレベルの入札制限を上書きします。 例えば、ポートフォリオの最低入札額が5 USDであるが、ポートフォリオの入札単位を3 USDの最低入札額に制限する場合、入札単位は3 USD以上に入札されます。 ただし、制限付き入札単位の全体的な支出は、ポートフォリオの[&#x200B; 「制約を中心に支出」パラメーター](#spend-around-constraints)によって決定されます。
>* 制約はベース入札で動作します。 基本入札に対する入札調整（モバイルデバイス上のエンドユーザーの入札の引き上げなど）は、入札を制約の許容範囲から外すことができます。 たとえば、制約で最大CPCが6 USDである場合、基本入札はすでに6 USDで、ポートフォリオはモバイルデバイスの入札調整を50%～60%に自動最適化しているため、最大CPCは6 USDではなく9.00～9.60 USDです。

### 制約タイプ {#constraint-types}

* **[!UICONTROL Bid]:**&#x200B;は、入札を金銭的範囲に制限します。

* **[!UICONTROL Bid Shift]:**&#x200B;関連するすべての入札単位の最適化入札を、入札範囲内で指定した金額だけ継続的に変更します。 入札シフトは、ポートフォリオの「支出の制約」の設定に関係なく、入札シフトによって引き起こされた合計金額で、関連するポートフォリオを過小支出または過小支出にします。 注意：現在のCPC入札が既に最大入札額と同じかそれ以上、または最小入札額と同じかそれ以下の場合、制約は無視され、入札は変更されません。 また、入札シフトの制約は、コストや収益モデルを生成するのに十分なデータがない入札単位には適用されません。

* **[!UICONTROL Incremental Bidding]:** （インプレッションのないキーワードにのみ適用）入札が指定されたターゲットに達するまで、指定された割合で入札を増分または減額します。

* **[!UICONTROL Search Engine Min Bid]:** （[!DNL Google Ads] アカウントのみ）検索エンジンによって決定された最小CPC入札額を最小入札額として使用します。 検索エンジンが最低入札額を変更すると、それに応じて入札額が変更されます。 必要に応じて、関連するすべての入札単位に追加の入札制限を指定できます。

* **[!UICONTROL Impression Share]:** （[!DNL Google Ads]および[!DNL Microsoft Advertising]件のCPC キャンペーンと完全一致のみ）広告がインプレッション シェアの最小値と最大値の間にある場合、入札を金銭的な範囲に制限します。 **注意：**&#x200B;制約がコスト効率に優れていない場合、最適化機能によって上書きされる可能性があります。

### 制約を適用するタイミング

入札単位を制限する理由には、次のようなものがあります。

* 未検証のキーワードや広告を迅速に公開する。

* 新しいポートフォリオ、アカウント、キャンペーン、広告グループのリスクを軽減します。 例えば、ポートフォリオを立ち上げる前に、トラフィックの多い入札単位に最大入札を設定し、その後、毎日徐々に値を上げることができます。 これにより、入札モデルは、大きな入札のリスクを伴うことなく、毎日調整することができます。

* コンバージョン率の高いテールキーワードを落札しないようにします。

* ブランドの中心となる特定の用語や、プロモーションの際に使用する用語を。

### UI内の制約に関する情報の表示場所

[[!UICONTROL Constraints] ビュー](#constraints-view)を開くだけでなく、次の方法で制約に関連する情報を確認することもできます。

* すべての制約は、「[!UICONTROL Constraints]」と呼ばれる単一の[&#x200B; ラベル分類](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/label-classifications/classification-about.html)のラベル値です。

   * 「[!UICONTROL Constraints]」は、デフォルトおよびカスタムビュー設定とスケジュール済みレポートの「[!UICONTROL Classifications]」リストに含まれています。 関連エンティティに割り当てられた制約を表示する場所に列を追加できます。

   * バルクシートをダウンロードすると、[!UICONTROL Download Bulksheet] ダイアログの該当するエンティティの「[!UICONTROL Classifications]」列の下に「[!UICONTROL Constraints]」が表示されます。 列を含めると、ダウンロードされたバルクシートには、関連するエンティティに割り当てられた制約が含まれます。

  [!UICONTROL Constraints]分類は[!UICONTROL Label Classifications] ビューに含まれていません。[!UICONTROL Constraints] ビューは別のビューです。 [!UICONTROL Constraints]分類も30 ラベルの分類制限に含まれていません。

* [[!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)には、ラベル分類アーキテクチャを使用する制約のコスト、クリック、および（オプションで）コンバージョンデータが含まれます。

### [!UICONTROL Constraints] ビュー {#constraints-view}

[!UICONTROL Goals] > [!UICONTROL Constraints] ビューには、すべての制約が一覧表示されます。 使用可能な列には、制約ステータス、制約タイプ、開始日および終了日、制約が関連付けられているキャンペーン、広告グループ、キーワード、広告、プレースメント、自動ターゲットおよび製品グループの数、インプレッション数、クリック数およびコストデータ、表示されているすべてのコンバージョン指標の収益データが含まれます。<!-- Clarify why "Ads" is listed, unless it's to identify the relevant ads -->

>[!IMPORTANT]
>
>[!UICONTROL Constraints] ビューの行のパフォーマンス データが、制約が割り当てられている最上位のエンティティのパフォーマンス データと一致しない場合があります。 最も低いレベルで割り当てられた制約は、常に親レベルで割り当てられた制約を上書きするため、キャンペーンまたは広告グループに割り当てられた制約は、子広告グループおよびキーワードに割り当てられたままにならない場合があります。 例えば、キャンペーン Aに制約Aが割り当てられている場合、キャンペーン Aのすべての広告グループとキーワードは、制約Aを自動的に継承します。ただし、これらの広告グループとキーワードは、後で制約Bなどの他の制約に割り当てられ、その後、制約Aとの関連付けが失われる可能性があります。

>[!NOTE]
>
>入札単位に制約を割り当て、関連するエンティティ管理ビュー（キャンペーンレベルの制約の[!UICONTROL Campaigns] ビューなど）から制約を割り当て解除します。

#### 使用可能なアクション

* [制約を作成](#constraint-create)。

* [制約の設定を編集](#constraint-edit)。

* [制約のステータスを変更](#constraint-change-status)。

## 制約の作成 {#constraint-create}

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Constraints]**&#x200B;をクリックします。

1. データテーブルの上にある右上のツールバーで、**[!UICONTROL Create Constraint]**&#x200B;をクリックします。

1. [制約の設定](#constraint-settings)を入力します。

   「[!UICONTROL Constraint Type]」タブと「[!UICONTROL Conditions]」タブの間を移動するには、開くタブをクリックするか、「[!UICONTROL Next]」ボタンと「[!UICONTROL Back]」ボタンをクリックします。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

制約を作成したら、キャンペーン、広告グループ、キーワード、プレースメント、および単位レベルの製品グループに[割り当て](#constraint-assign)できます。

## 制約の設定を編集 {#constraint-edit}

一度に1つの制約の設定を編集できます。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Constraints]**&#x200B;をクリックします。

1. （オプション）ツールバー[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)または[列の見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からリスト をフィルタリングします。

1. 編集する制約の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、![編集](/help/search-social-commerce/assets/edit-new.png "編集")をクリックします。

1. [制約の設定](#constraint-settings)を編集します。

   「[!UICONTROL Constraint Type]」タブと「[!UICONTROL Conditions]」タブの間を移動するには、開くタブをクリックするか、「[!UICONTROL Next]」ボタンと「[!UICONTROL Back]」ボタンをクリックします。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 制約のステータスの変更 {#constraint-change-status}

アクティブなコンストレインを一時停止して無効にすることができます。 後でステータスを&#x200B;*アクティブ*&#x200B;に戻して有効にすることができます。

また、制約を削除して、アカウントコンポーネントとの関連付けをすべて削除し、後で使用できないようにすることもできます。 制約のレポートデータは使用できなくなります。 **メモ：**&#x200B;単にアカウント コンポーネントから制約を解除するには、「[検索入札単位からの制約の割り当て解除](#constraints-unassign)」を参照してください。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Constraints]**&#x200B;をクリックします。

1. （オプション）ツールバー[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)または[列の見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からリスト をフィルタリングします。

1. ステータスを変更する各制約の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、ステータスボタンをクリックします。

   * 選択したすべての行をアクティブ化するには、![&#x200B; アクティブ化](/help/search-social-commerce/assets/activate-new.png " アクティブ化")をクリックします。

   * 選択したすべての行を一時停止するには、![一時停止](/help/search-social-commerce/assets/pause-new.png "一時停止")をクリックします。

   * 選択したすべての行を削除するには、![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 制約の設定 {#constraint-settings}

| Tab | パラメーター | 説明 |
|---|---|---|
| \[基本情報\] | [!UICONTROL Constraint Name] | 制約の一意の名前。 |
| | [!UICONTROL Currency] | 適用可能な入札単位が入札される通貨。 別の通貨が使用されている入札単位は無視されます。 |
| | [!UICONTROL Status] | 制約のステータス：<ul><li>**アクティブ：** （既定値）制約は、指定された条件と日付範囲に適用されます。</li><li>**一時停止：**&#x200B;制約が適用されていません。</li></ul> |
| [!UICONTROL Constraint Type] | [!UICONTROL Constraint Type] | 制約のタイプ。 制約の種類と各対象となる広告ネットワークについて詳しくは、「[制約の種類](#constraint-types)」を参照してください。 |
| | [!UICONTROL Start Date] | 制約が有効になる最初の日。 デフォルトは現在の日付です。 日付を変更するには、日付を入力するか、![&#x200B; カレンダー](/help/search-social-commerce/assets/calendar-new.png " カレンダー")をクリックしてカレンダーを開き、日付を選択します。 |
| | [終了日] | 制約が特定の日付に無効になるかどうかを確認します。 入札単位が会社のブランドの中心となる場合など、制約を無期限に適用するには、フィールドを空のままにします。 特定の日付で制約を終了するには、日付を入力するか、![&#x200B; カレンダー](/help/search-social-commerce/assets/calendar-new.png " カレンダー")をクリックしてカレンダーを開き、日付を選択します。 **メモ：**&#x200B;制約は明日までに期限切れにすることはできません。 |
| | [!UICONTROL Set constraint options for Bid] | （[!UICONTROL Bid]個の制約のみ）設定には、次のものが含まれます。<ul><li>**[!UICONTROL Min Bid]:**&#x200B;関連付けられた入札単位の最低基本入札額。</li><li>**[!UICONTROL Max Bid]:**&#x200B;関連付けられた入札単位の最大基本入札額。</li></ul> |
| | [!UICONTROL Set constraint options for Bid Shift] | （[!UICONTROL Bid Shift]個の制約のみ）入札の種類と金額は、基本入札に継続的に適用されるように変更されます。<ul><li>*[!UICONTROL Increases]:*&#x200B;指定した割合または通貨値で入札額を増やします。 変更する金額を入力し、*$*&#x200B;または&#x200B;*%*&#x200B;のいずれかを選択します。 また、制約が適用されたときに可能な限り高い入札（上限）である&#x200B;**[!UICONTROL Max Limit]**&#x200B;を入力します。 **注：**&#x200B;現在のCPC入札額が[!UICONTROL Max Limit]以上の場合、制約は無視され、入札額は変更されません。</li><li>*[!UICONTROL Decreases]:*&#x200B;指定した割合または通貨値で入札額を減らします。 変更する金額を入力し、*$または%*&#x200B;のいずれかを選択します。 また、制約が適用されたときに、可能な限り低い入札（フロア）である&#x200B;**[!UICONTROL Min Limit]**&#x200B;を入力します。 **注：**&#x200B;現在のCPC入札額が[!UICONTROL Min Limit]と同じかそれ以下の場合、制約は無視され、入札額は変更されません。</li></ul>**メモ：**<ul><li>入札シフトは、ポートフォリオの「[!UICONTROL Spend Around Constraints]」の設定に関係なく、入札シフトによって引き起こされる合計金額で、関連するポートフォリオを過小支出または過小支出にします。</li><li>制約に終了日を指定し、最適化機能がポートフォリオ内のキャンペーンの支出制限を自動的に調整している場合、入札は終了日以降に元の金額に戻るだけでなく、最適に調整されます。</li><li>入札シフトは、コストと収益モデルを生成するのに十分なデータがない入札単位には適用されません。</li></ul> |
| | [!UICONTROL Set constraint options for Incremental Bidding] | （[!UICONTROL Incremental Bidding]個の制約のみ）入札ターゲット、および入札が目標に達するまで入札を増分に増減する量と頻度：<ul><li>**[!UICONTROL Bid target]:** ターゲット入札金額。</li><li>**[!UICONTROL Incrementally change bids by]**&#x200B;と&#x200B;**[種類]:**&#x200B;入札を増減する金額、および入札を通貨値（**$**）または割合（*%*）で変更するかどうか。</li><li>**[!UICONTROL Every __ days]:**&#x200B;入札を増やす頻度。</li></ul>例えば、キーワードの1つに対する現在の入札額が100 セントで、500 セントの入札目標に達するまで、毎日10%ずつ入札額を変更したいとします。 制約が設定された後の1日目に、そのキーワードの入札は110 セント（現在の入札+ 10%）になります。 2日目の入札は120 セント（1日目の現在の入札+ 20%）です。 ただし、入札目標が50 セントで、他のパラメーターが同じ場合、入札が50 セントに達するまで入札は徐々に減少します。 |
| | [!UICONTROL Set constraint options for Search Engine Min Bid] | （[!UICONTROL Search Engine Min Bid]個の制約）Google （[!UICONTROL Google First Page CPC]）の検索結果の最初のページに入札単位を表示するために必要な最小入札額を使用します。 必要に応じて、**[!UICONTROL Min Bid]**&#x200B;値または&#x200B;**[!UICONTROL Max Bid]**&#x200B;値を入力して、制約の対象となる入札範囲を定義します。 例えば、2.50 USDの[!UICONTROL Min Bid]と4 USDの[!UICONTROL Max Bid]を指定した場合、[!DNL Google Ads]の最初のページ入札が2.50 USD未満または4 USD以上の場合、入札単位に入札することはありません。 |
| | [!UICONTROL Set constraint options for Impression Share] | （[!UICONTROL Impression Share]個の制約のみ）設定には、次のものが含まれます。<ul><li>**[!UICONTROL Min Bid]** （オプション）関連付けられた入札単位の最低基本入札額。</li><li>**[!UICONTROL Max Bid]:** （オプション）関連付けられた入札単位の最大基本入札額。</li><li>**[!UICONTROL Min Impression Share]:**&#x200B;適用可能な入札単位の制約をトリガーするインプレッションの最小シェアの割合（パーセント）。 10から90の間である必要があります。 **注意：**&#x200B;制約がコスト効率に優れていない場合、最適化機能によって上書きされる可能性があります。</li><li>**[!UICONTROL Max Impression Share]:**&#x200B;適用可能な入札単位の制約をトリガーする最も高いインプレッションの割合（パーセント）。 10 ～ 90の範囲である必要があります。**注：**&#x200B;制約がコスト効率に優れていない場合、最適化機能によって上書きされる可能性があります。</li></ul>> |
| [!UICONTROL Conditions] | [!UICONTROL Condition Type] | 制約に条件を適用するかどうか：<ul><li>*[!UICONTROL No Condition]:* （既定値）制約は、指定された日付範囲内に無条件で適用されます。</li><li>*[!UICONTROL Satisfy]:*&#x200B;制約は、指定されたデータ評価期間に指定された条件が満たされた場合にのみ適用されます。</li></ul> |
| | [!UICONTROL Data Evaluation Period] | （条件が設定されている場合）指定された基準のデータを評価する期間。 *[!UICONTROL Custom date range],**を選択した場合は、形式`MM-DD-YYYY`で各日付を入力するか、![&#x200B; カレンダーボタン &#x200B;](/help/search-social-commerce/assets/calendar-new.png " カレンダーボタン ")をクリックしてカレンダーを開き、各日付を選択して&#x200B;**&#x200B;[!UICONTROL Start Date]&#x200B;**&#x200B;と&#x200B;**&#x200B;[!UICONTROL End Date]**&#x200B;を指定します（2026年3月29日など）。 |
| | [!UICONTROL When to Apply Constraints] | （条件が設定されている場合）条件を適用するために満たす必要があるフィルター条件の数：<ul><li>*[!UICONTROL Match All Filters]:*&#x200B;指定したすべてのフィルター条件に一致すると、制約が適用されます。</li><li>*[!UICONTROL Match Any Filters]:*&#x200B;指定されたフィルター条件の少なくとも1つが満たされたときに制約を適用します。</li></ul> |
| | [!UICONTROL Filters] | （条件が設定されている場合）満たす必要がある1つ以上の基準。 フィルターを作成するには、リストからプロパティまたは指標を選択します。 プロパティ（[!UICONTROL Channel Type]など）の場合は、リスト内の該当する値を選択します。 指標（[!UICONTROL Clicks]など）の場合は、演算子を選択し、該当する値を入力します。 例えば、100 クリックを超える入札単位のみを返すには、「**クリック**」を選択し、「**より大きい**」を選択して、入力フィールドに「`100`」と入力します。</li></ul> |

## 検索入札単位への制約の割り当て {#constraint-assign}

入札単位の制約は、キャンペーン、広告グループ、キーワード、プレースメント、または動的検索ターゲット（自動ターゲット）に適用できます。

各エンティティには1つの制約しか設定できません。 1つの拘束を1つまたは複数のエンティティに同時に割り当てることができます。

>[!NOTE]
>
>* 後で広告のキーワードまたは広告コピーを編集して、新しいキーワードまたは広告を作成した場合、制約は新しいエンティティに割り当てられません。
>* [[!UICONTROL Campaigns] ビュー](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)、[[!UICONTROL Ad Groups] ビュー](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)、[[!UICONTROL Keywords] ビュー](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)、または[[!UICONTROL Placements] ビュー](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)で同じ手順を参照してください。<!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. メインメニューから、関連する管理ビューを開きます。

   例えば、キャンペーンレベルで制約を割り当てるには、[!UICONTROL Manage] > [!UICONTROL Campaigns]に移動します。

1. （オプション）ツールバー[&#128279;](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)または[列の見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からリスト をフィルタリングします。

1. 1つの拘束を割り当てる各エンティティの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. 制約を選択します。

1. **[!UICONTROL Assign Now]**&#x200B;をクリックします。

## 検索入札単位からの制約の割り当て解除 {#constraints-unassign}

>[!NOTE]
>
>* 制約を削除して後で使用できないようにするには、「[制約のステータスを変更](#constraint-change-status)」を参照してください。
>* [[!UICONTROL Campaigns] ビュー](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)、[[!UICONTROL Ad Groups] ビュー](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)、[[!UICONTROL Keywords] ビュー](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)、または[[!UICONTROL Placements] ビュー](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)で同じ手順を参照してください。<!-- ADD LINK WHEN AVAILABLE for dynamic search targets (auto targets). -->

1. メインメニューで、関連する管理ビューを開きます。

   例えば、キャンペーンレベルの制約の割り当てを解除するには、[!UICONTROL Manage] > [!UICONTROL Campaigns]に移動します。

1. 制約の割り当てを解除する各エンティティの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Constraint]**&#x200B;をクリックします。

1. **[!UICONTROL Confirm]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンの制約の割り当ての管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-constraint-assignments-manage.md)
>* [広告グループの制約の割り当てを管理](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-constraint-assignments-manage.md)
>* [&#x200B; キーワードの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/keywords/keyword-assignments-manage.md)
>* [&#x200B; プレースメントの制約の割り当てを管理](/help/search-social-commerce/new-ui/target/placements/placement-assignments-manage.md)
>* [The [!UICONTROL Constraint Report]](/help/search-social-commerce/new-ui/reports/management/basic-advanced/constraint-report.md)
