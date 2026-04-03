---
title: カスタムアラートテンプレート設定
description: カスタムアラートテンプレートの設定について説明します。
exl-id: c9cff26b-e6be-4dad-ac3a-b5a53387c4e6
feature: Search Alerts
TQID: https://experienceleague.adobe.com/zPTijDSnrxMys8g0qByEvfh1XyvnAzwwqpVmBHUDdLk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 676
ht-degree: 0%

---

# カスタムアラートテンプレート設定

| Tab | パラメーター | 説明 |
|--- |--- |--- |
| [!UICONTROL Date Range] | [!UICONTROL Date] | アラートの条件を評価する日付範囲。 指標は、日付範囲をまたいで集計して評価されます。 オプションの範囲は&#x200B;*[!UICONTROL Yesterday]*&#x200B;から&#x200B;*[!UICONTROL Last 180 Days]*&#x200B;です。 |
| [!UICONTROL Filters] |  | [!UICONTROL Scheduling and Delivery] タブで指定された時点でアラートをトリガーするための条件。 使用可能な列は、エンティティタイプ（キャンペーンやキーワードなど）によって異なります。 すべてのフィルターはブール関数ANDを使用して結合されます。つまり、指定したすべての条件を満たす必要があります。<ul><li><p>フィルターを追加するには、![追加](/help/search-social-commerce/assets/arrow-down-expand.png "追加") ![の横にある](/help/search-social-commerce/assets/add.png "下向き矢印")下向き矢印&#x200B;**[!UICONTROL ADD FILTER]**&#x200B;をクリックし、次の操作を行います。</p></li><ol><li><p>（オプション）列名をテキスト文字列でフィルタリングするには、**[!UICONTROL ADD FILTER]**&#x200B;入力フィールドに検索文字列を入力します。</p></li><li><p>列メニューから列名を選択します。</p></li><li><p>列にフィルターを定義します。</p></li><ul><li><p>（入力フィールドのないフィルター） 2番目のメニューの横にある![下向き矢印](/help/search-social-commerce/assets/arrow-down-expand.png "下向き矢印")をクリックし、含める各値の横にあるチェックボックスを選択します。</p></li><li><p>（指定した日付範囲と前の期間の値の増減を追跡する指標の列）演算子の場合、「*増減*」または「*減減*」を選択し、しきい値を入力します。</p><p>例えば、「[!UICONTROL Cost]」列を選択し、キャンペーンのコストが21%増加したときにアラートを受け取りたい場合は、「[!UICONTROL increases by]」を選択して入力フィールドに21と入力します。 「[!UICONTROL Date Comparison Format]」フィールドで、（通貨単位の変更ではなく）割合の変更に関心があることを示します。</p><p>このオプションを選択すると、通常のデータ列ごとに2つの追加の列が追加されます。 例えば、レポートには「クリック数」の列を1つだけ含める代わりに、指定された[!UICONTROL Date Comparison Format]に応じて、「クリック数R1」（範囲1）の列と「クリック数R2」（範囲2）の列、および「クリック数の差分」または「クリック数の差分（%）」の列が含まれます（以下を参照）。</p><p>**メモ：**</p><ul><li><p>差分カラムは派生指標に入力されません。<p></li><li><p>この機能は、コンバージョン指標、ID、ラベル分類列では使用できません。</p></li><li><p>大規模な日付範囲を比較するレポートの生成に時間がかかる場合があります。</p></li></ul></ul><li><p>（入力フィールドを持つその他のすべてのフィルター） 2番目のメニューから演算子を選択し、該当する値を入力します。</p><p>例えば、「クリック数」列を選択し、100回を超えるクリック数の行のみを返す場合は、「より大きい」を選択し、入力フィールドに100と入力します。</p><p>データ型に応じて、使用可能な演算子には、<i>1&rbrace;より大きい、</i>より小さい<i>、</i>等しい<i>、</i>含む<i>、</i>含まない<i>、</i>から始まる<i>、</i>値なし<i>、</i>値なし<i>、</i>前<i>後</i>または<i>日付3&rbrace;が含まれます。</i><i></i><i></i></p><p>**注意：** テキスト値では、大文字と小文字は区別されません。 例えば、名前に「ローン」が付いたキャンペーンで絞り込むと、「消費者ローン」や「ローン申し込み」などの結果が得られます。</p></li></ol><li><p>フィルターを削除するには、フィルター定義の横にある![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。</p></li></ul> |
|  | [!UICONTROL Comparing] | （アラートトラックが1つ以上の指標カラムで増減する場合に使用できます。読み取り専用） データを比較する2つの日付範囲。 |
|  | [!UICONTROL Date Comparison Format] | （アラートトラックが1つ以上のメトリック列で増減する場合に使用可能） 2つの日付範囲のデータの違いを表現する方法：<ul><li><p><i>[!UICONTROL Variance]</i> （既定値） – 差分を数値として表示します。</p></li><li><p><i>[!UICONTROL % Change]</i>  – 差分をパーセントで表示します。</p></li></ul> |
| [!UICONTROL Scheduling and Delivery] | [!UICONTROL Name] | アラート名。 5文字以上を含める必要があります。 |
|  | [!UICONTROL Trigger this Alert] [いつ] | アラートが指定された条件フィルターをチェックする頻度と、すべての条件が満たされると、メール通知を送信する頻度：<ul><li><p>[!UICONTROL Daily at <*NN*> `[AM\|PM]`]</p></li><li><p>[!UICONTROL Weekly on <*週の日*> （&lt;*NN*> `[AM\|PM]`]）</p></li><li><p>[!UICONTROL Every month on <*日NN*> （&lt;*NN*> `[AM\|PM]`]）</p></li></ul>**注：**&#x200B;この値は、評価期間には影響しません。 |
|  | [!UICONTROL Email Recipients] | （アラートテンプレートの作成者のみが編集できます。他のユーザーは読み取り専用） アラートが生成されたときに通知を送信するメールアドレス。 デフォルトでは、テンプレート作成者のアドレスが入力されます。<br><br> アドレスを追加するには、アドレスを入力し、**[!UICONTROL Add]**&#x200B;をクリックします。 複数のアドレスを指定するには、コンマまたはスペースで区切るか、別々に追加します。<br><br> アラートに最大1000件のレコードが含まれる場合、アラートのCSV バージョンがメールメッセージに添付されます。 |

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムアラートについて](alert-about.md)
>* [&#x200B; カスタムアラートテンプレートを作成](alert-template-create.md)
>* [&#x200B; カスタムアラートテンプレートの編集](alert-template-edit.md)
>* [&#x200B; カスタムアラートテンプレートを一時停止](alert-template-pause.md)
>* [&#x200B; カスタムアラートテンプレートをアクティブ化](alert-template-activate.md)
>* [&#x200B; カスタムアラートテンプレートを削除](alert-template-delete.md)
>* [&#x200B; カスタムアラートの表示](alert-view.md)
>* [&#x200B; カスタムアラート用にデータを書き出し](alert-export-data.md)
