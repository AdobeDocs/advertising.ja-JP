---
title: カスタムアラートテンプレート設定
description: カスタムアラートテンプレートの設定の詳細を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# カスタムアラートテンプレート設定

| タブ | パラメータ | 説明 |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | アラートの条件を評価する日付範囲。 指標は、日付範囲をまたいで集計で評価されます。 オプションの範囲は次のとおりです。 *[!UICONTROL Yesterday]* から *[!UICONTROL Last 180 Days]*. |
| [!UICONTROL Filters] |  | アラートのトリガー条件 ( [!UICONTROL Scheduling and Delivery] タブをクリックします。 使用可能な列は、エンティティのタイプ（キャンペーンやキーワードなど）によって異なります。 すべてのフィルターは、ブール関数 AND を使用して結合されます。つまり、指定したすべての条件を満たす必要があります。<ul><li><p>フィルターを追加するには、 ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 次の ![追加](/help/search-social-commerce/assets/add.png "追加") **[!UICONTROL ADD FILTER]**&#x200B;をクリックし、次の操作を実行します。</p></li><ol><li><p>（オプション）列名をテキスト文字列でフィルターするには、 **[!UICONTROL ADD FILTER]** 入力フィールド。</p></li><li><p>列メニューから列名を選択します。</p></li><li><p>列でフィルターを定義します。</p></li><ul><li><p>（入力フィールドを含まないフィルター）クリック ![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印") 2 番目のメニューの横にあるをクリックし、含める各値の横にあるチェックボックスをオンにします。</p></li><li><p>（指定した日付範囲と前の期間の間の値の増減を追跡する指標列）演算子に対して、 *増加* または *次のように減少*」、「しきい値」を入力します。</p><p>例えば、[!UICONTROL Cost]」列を開き、キャンペーンのコストが 21%増加した場合にアラートを受け取り、「[!UICONTROL increases by]」と入力し、入力フィールドに 21 と入力します。 内 [!UICONTROL Date Comparison Format] フィールドに、（通貨単位の変更ではなく）割合の変更に関心があることを示します。</p><p>このオプションを選択すると、通常のデータ列ごとに 2 つの列が追加されます。 例えば、「クリック数」に 1 列だけを含める代わりに、「Clicks R1」（範囲 1 の場合）「Clicks R2」（範囲 2 の場合）、「Clicks Diff」または「ClicksDiff (%)」の列が指定した内容に応じてレポートに表示されます [!UICONTROL Date Comparison Format] （以下を参照）。</p><p>**メモ：**</p><ul><li><p>派生指標の差異列が入力されない。<p></li><li><p>この機能は、プロパティ名、ID、ラベル分類列には使用できません。</p></li><li><p>大きな日付範囲を比較するレポートの生成には、時間がかかる場合があります。</p></li></ul></ul><li><p>（入力フィールドを含むその他すべてのフィルター）2 番目のメニューから演算子を選択し、適切な値を入力します。</p><p>例えば、「クリック数」列を選択し、100 回を超えるクリック数の行のみを返す場合は、「次より大きい」を選択して、入力フィールドに 100 と入力します。</p><p>データタイプに応じて、使用可能な演算子は次のとおりです。 <i>より大きい</i>, <i>より小さい</i>, <i>次と等しい</i>, <i>次を含む</i>, <i>次を含まない</i>, <i>次で始まる</i>, <i>次で終わる</i>, <i>値なし</i>, <i>値を含む</i>, <i>前</i>, <i>後</i>または <i>日付なし</i>.</p><p>**注意：** テキスト値では大文字と小文字が区別されません。 例えば、名前に「loan」を含むキャンペーンでフィルターする場合、結果には「Consumer Loans」と「loan applications」が含まれます。</p></li></ol><li><p>フィルターを削除するには、 ![削除](/help/search-social-commerce/assets/delete.png "削除") をクリックします。</p></li></ul> |
|  | [!UICONTROL Comparing] | ( アラートが 1 つ以上の指標列で増加または減少を追跡する場合に使用できます。読み取り専用 ) データの比較対象となる 2 つの日付範囲。 |
|  | [!UICONTROL Date Comparison Format] | （1 つ以上の指標列でアラートが追跡の対象となる場合に使用可能）2 つの日付範囲でのデータ間の違いを表す方法は、次のとおりです。<ul><li><p><i>[!UICONTROL Variance]</i> （デフォルト）：差異を数値として表示します。</p></li><li><p><i>[!UICONTROL % Change]</i>  — 差異をパーセンテージで表示します。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | アラート名。 5 文字以上含める必要があります。 |
|  | [!UICONTROL Trigger this Alert] [when] | アラートが指定した条件フィルターをチェックする頻度、およびすべての条件を満たした場合に電子メール通知を送信する頻度。<ul><li><p>[!UICONTROL Daily at <*NN*> [AMPM]]</p></li><li><p>[!UICONTROL Weekly on <*Day of Week*> at <*NN*> [AMPM]]</p></li><li><p>[!UICONTROL Every month on <*Day NN*> at <*NN*> [AMPM]]</p></li></ul>**注意：** この値は評価期間には影響しません。 |
|  | [!UICONTROL Email Recipients] | （アラートテンプレートの作成者のみが編集可能）読み取り専用 ) アラートの生成時に通知を送信する電子メールアドレス。 デフォルトでは、テンプレート作成者のアドレスが入力されます。<br><br>アドレスを追加するには、アドレスを入力し、 **[!UICONTROL Add]**. 複数のアドレスを指定する場合は、コンマまたはスペースで区切るか、個別に追加します。<br><br>アラートに最大 1000 件のレコードが含まれる場合、アラートの CSV バージョンが電子メールメッセージに添付されます。 |

>[!MORELIKETHIS]
>
>* [Custom Alerts について](alert-about.md)
>* [カスタムアラートテンプレートの作成](alert-template-create.md)
>* [カスタムアラートテンプレートの編集](alert-template-edit.md)
>* [カスタムアラートテンプレートの一時停止](alert-template-pause.md)
>* [カスタムアラートテンプレートのアクティブ化](alert-template-activate.md)
>* [カスタムアラートテンプレートの削除](alert-template-delete.md)
>* [カスタムアラートの表示](alert-view.md)
>* [カスタムアラート用のデータのエクスポート](alert-export-data.md)

