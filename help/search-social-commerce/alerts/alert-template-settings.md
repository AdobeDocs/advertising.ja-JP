---
title: カスタムアラートテンプレートの設定
description: カスタムアラートテンプレートの設定について説明します。
exl-id: c9cff26b-e6be-4dad-ac3a-b5a53387c4e6
feature: Search Alerts
source-git-commit: 3ab2e38f6a2f70c03504363575b13dc0dc730282
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 0%

---

# カスタムアラートテンプレートの設定

| タブ | パラメーター | 説明 |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | アラートの条件を評価する日付範囲。 指標は、日付範囲全体にわたって集計で評価されます。 オプションの範囲は *[!UICONTROL Yesterday]* ～ *[!UICONTROL Last 180 Days]* です。 |
| [!UICONTROL Filters] |  | 「[!UICONTROL Scheduling and Delivery]」タブで指定された時刻にアラートをトリガーする条件。 使用可能な列は、エンティティタイプ（キャンペーンやキーワードなど）によって異なります。 すべてのフィルターは、ブール関数 AND を使用して結合されます。つまり、指定されたすべての条件を満たす必要があります。<ul><li><p>フィルターを追加するには、「![ 追加 ](/help/search-social-commerce/assets/arrow-down-expand.png " 追加 ")」 ![ ックスの横にある ](/help/search-social-commerce/assets/add.png " 下向き矢印 ") 下向き矢印 **[!UICONTROL ADD FILTER]** をクリックし、次の操作を実行します。</p></li><ol><li><p>（オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]** 入力フィールドに検索文字列を入力します。</p></li><li><p>列メニューから列名を選択します。</p></li><li><p>列のフィルターを定義：</p></li><ul><li><p>（入力フィールドのないフィルタ） 2 番目のメニューの横にある ![ 下矢印 ](/help/search-social-commerce/assets/arrow-down-expand.png " 下矢印 ") をクリックし、含める値の横のチェック ボックスをオンにします。</p></li><li><p>（指定した日付範囲と前の期間の値の増減を追跡する指標列）演算子の場合は、「*次の値の増加* または *次の値の減少* を選択してしきい値を入力します。</p><p>例えば、「[!UICONTROL Cost]」列を選択し、キャンペーンのコストが 21% 増加したときにアラートを表示したい場合は、「[!UICONTROL increases by]」を選択して、入力フィールドに「21」と入力します。 「[!UICONTROL Date Comparison Format]」フィールドで、（通貨単位の変更ではなく）パーセンテージの変更に関心があることを示します。</p><p>このオプションを選択すると、通常のデータ列ごとに 2 つの列が追加されます。 例えば、「クリック数」に 1 列のみを含めるのではなく、指定された [!UICONTROL Date Comparison Format] に応じて、「クリック数 R1」（範囲 1 の場合）「クリック数 R2」（範囲 2 の場合）、および「クリック数の差分」または「クリック数の差分（%）」のいずれかを含むレポートを作成できます（以下を参照）。</p><p>**注：**</p><ul><li><p>差分列に派生指標が入力されていません。<p></li><li><p>この機能は、コンバージョン指標、ID、ラベルの分類列には使用できません。</p></li><li><p>大きな日付範囲を比較するレポートは、生成に時間がかかる場合があります。</p></li></ul></ul><li><p>（入力フィールドを持つその他すべてのフィルター） 2 番目のメニューから演算子を選択し、適切な値を入力します。</p><p>例えば、「クリック数」列を選択し、クリック数が 100 を超える行のみを返したい場合、「次よりも大きい」を選択して、入力フィールドに「100」と入力します。</p><p>データ型に応じて、使用可能な演算子には <i> 次より大きい </i>、<i> 次より小さい </i>、<i> 次に等しい </i>、<i> 次を含む </i>、<i> 次を含まない </i>、<i> 次で始まる </i>、<i> 次で終わる </i>、<i> 値なし </i>、<i> 値を持つ </i>、<i> 前 </i>、<i></i> <i> </i> 後の日付または次が含まれます。</p><p>**メモ：** テキスト値では、大文字と小文字が区別されません。 例えば、名前に「loan」が含まれるキャンペーンでフィルタリングした場合、結果には「Consumer Loans」と「loan applications」が含まれる可能性があります。</p></li></ol><li><p>フィルターを削除するには、フィルター定義の横にある ![ 削除 ](/help/search-social-commerce/assets/delete.png " 削除 ") をクリックします。</p></li></ul> |
|  | [!UICONTROL Comparing] | （アラートが 1 つ以上の指標列で増加または減少を追跡する場合に使用できます。読み取り専用）データを比較する 2 つの日付範囲。 |
|  | [!UICONTROL Date Comparison Format] | （アラートが 1 つ以上の指標列で増加または減少を追跡している場合に使用可能） 2 つの日付範囲のデータ間の違いを表す方法：<ul><li><p><i>[!UICONTROL Variance]</i> （デフォルト） – 差異を数値で表示します。</p></li><li><p><i>[!UICONTROL % Change]</i>  – 差異をパーセンテージで表示します。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | アラート名。 少なくとも 5 文字を含める必要があります。 |
|  | [!UICONTROL Trigger this Alert] [when] | 指定した条件フィルターをアラートがチェックし、すべての条件を満たした場合にメール通知を送信する頻度：<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*曜日*> の &lt;*NN*>`[AM\|PM]`]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> &lt;*NN*>`[AM\|PM]`]</p></li></ul>**注意：** この値は評価期間には影響しません。 |
|  | [!UICONTROL Email Recipients] | （アラートテンプレートの作成者のみが編集できます。その他のすべてのユーザーは読み取り専用です） アラートが生成されたときに通知を送信するメールアドレス。 デフォルトでは、テンプレート作成者のアドレスが入力されます。<br><br> アドレスを追加するには、アドレスを入力し、[**[!UICONTROL Add]**] をクリックします。 複数のアドレスを指定する場合は、コンマまたはスペースで区切るか、別々に追加します。<br><br> アラートに最大 1000 件のレコードが含まれる場合、アラートの CSV バージョンがメールメッセージに添付されます。 |

>[!MORELIKETHIS]
>
>* [ カスタムアラートについて ](alert-about.md)
>* [ カスタムアラートテンプレートの作成 ](alert-template-create.md)
>* [ カスタムアラートテンプレートの編集 ](alert-template-edit.md)
>* [ カスタムアラートテンプレートの一時停止 ](alert-template-pause.md)
>* [ カスタムアラートテンプレートのアクティブ化 ](alert-template-activate.md)
>* [ カスタムアラートテンプレートの削除 ](alert-template-delete.md)
>* [ カスタムアラートの表示 ](alert-view.md)
>* [ カスタムアラートのデータのエクスポート ](alert-export-data.md)
