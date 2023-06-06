---
title: カスタム指標設定
description: 標準の指標から計算されるカスタム指標の設定を参照します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '613'
ht-degree: 0%

---

# カスタム指標設定

カスタム指標設定は、インターフェイスの各部で少し異なります。

## キャンペーン管理ビューのカスタム指標設定

| パラメータ/セクション | 説明 |
|----|----|
| カスタム指標名 | 指標の名前。列名として表示されます。 <b>ヒント：</b> 意味のある指標名を使用しますが、長い名前を使用すると列の幅が広くなると考えます。 |
| 指標の挿入 | 新しい指標の計算に使用する数式 ( [コスト]/[登録]:<ul><li>トラフィック指標と売上高指標のリストから指標を挿入するには、指標を挿入する場所にカーソルを置き、リストから指標を選択するか、手動で指標を入力して角括弧で囲みます ( 例： `[CPC]`) をクリックします。</li><li>演算子を挿入するには、演算子を挿入する位置にカーソルを置き、ボタンをクリックするか、手動で記号を入力します。 使用可能な演算子は次のとおりです。 `+ - * / ( ) ()`</li></ul><b>注意：</b> 複雑なカスタム指標の計算に時間がかかり、それらを含むレポートと表示（特にクリックスルーとビュースルーのコンバージョン用に別々の列を含む場合）の生成に時間がかかります。 |
| 形式 | この指標のデータを表示する方法： *[!UICONTROL Currency]* （金額） *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*&#x200B;または *[!UICONTROL Percentage]* （小数点が 2 つある割合）。<br><br><b>注意：</b> の形式で派生指標を作成する場合 [!UICONTROL Number w/out Decimal Points] （データを整数で表示）を含め、重み付けされたコンバージョンアトリビューションルール ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]または [!UICONTROL Even Distribution]) の場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しいにもかかわらず、個々のデータフィールドが正しくない可能性があります。 例えば、ある注文が 3 つのイベント間で等しく分割されている場合、（0.33 順序ではなく）1 つの注文が 3 つのイベントのそれぞれに関連付けられます。 この問題を回避するには、指標の形式を使用します [!UICONTROL Number to 2 Decimal Points]. |

## レポートおよびレポートテンプレートと [!UICONTROL Portfolios] ビュー

| パラメータ/セクション | 説明 |
|----|----|
| カスタム指標名 | 指標の名前。列名として表示されます。 <b>ヒント：</b> 意味のある指標名を使用しますが、長い名前を使用すると列の幅が広くなると考えます。 |
| 形式 | この指標のデータを表示する方法： *[!UICONTROL Currency]* （金額） *[!UICONTROL Number to 2 Decimal Points]*, *[!UICONTROL Number to 3 Decimal Points]*, *[!UICONTROL Number w/out Decimal Points]*&#x200B;または *[!UICONTROL Percentage]* （小数点が 2 つある割合）。<br><br><b>注意：</b> の形式で派生指標を作成する場合 [!UICONTROL Number w/out Decimal Points] （データを整数で表示）を含め、重み付けされたコンバージョンアトリビューションルール ([!UICONTROL Weight First Event More], [!UICONTROL Weight Last Event More]または [!UICONTROL Even Distribution]) の場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しいにもかかわらず、個々のデータフィールドが正しくない可能性があります。 例えば、ある注文が 3 つのイベント間で等しく分割されている場合、（0.33 順序ではなく）1 つの注文が 3 つのイベントのそれぞれに関連付けられます。 この問題を回避するには、指標の形式を使用します [!UICONTROL Number to 2 Decimal Points]. |
| 指標の挿入 | 数式を作成できる既存の指標のリスト。<br><br>数式の入力フィールドに指標を挿入するには、指標を挿入する位置にカーソルを置き、リストから指標を選択するか、手動で指標を入力して角括弧で囲みます ( 例： `[CPC]`) をクリックします。 |
| 演算子の挿入 | 使用可能な演算子は次のとおりです。 `+ - x / ( )`<br><br>数式の入力フィールドに演算子を挿入するには、演算子を挿入する位置にカーソルを置き、ボタンをクリックするか、記号を手動で入力します。 |
| [指標の数式入力フィールド] | 1 つ以上の既存のプロパティまたは標準指標 ( `[Cost]/[Registrations]`. 指標と演算子の任意の組み合わせを含めることができます。<br><br><b>注意：</b> 複雑なカスタム指標の計算に時間がかかり、それらを含むレポートと表示（特にクリックスルーとビュースルーのコンバージョン用に別々の列を含む場合）の生成に時間がかかります。 |

>[!MORELIKETHIS]
>
>* [カスタム指標について](custom-metric-about.md)
>* [カスタム指標の作成](custom-metric-create.md)
>* [カスタム指標の編集](custom-metric-edit.md)
>* [カスタム指標の削除](custom-metric-delete.md)

