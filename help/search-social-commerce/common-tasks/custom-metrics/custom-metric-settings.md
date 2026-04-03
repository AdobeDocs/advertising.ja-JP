---
title: カスタム指標の設定
description: 標準指標から計算されるカスタム指標の設定を参照します。
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
TQID: https://experienceleague.adobe.com/yyXHbc4ll8-Y4v3v0p3zMKi6zQVYXQr3bYApBEGGN-s
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 616
ht-degree: 0%

---

# カスタム指標の設定

カスタム指標の設定は、インターフェイスの各部分で若干異なります。

## ほとんどの管理ビューでのカスタム指標設定

| パラメーター/セクション | 説明 |
|----|----|
| カスタム指標名 | 列名として表示される指標の名前。 <b> ヒント：</b>意味のあるメトリック名を使用しますが、名前が長いほど列が広くなると考えてください。 |
| 挿入指標 | 新しい指標の計算に使用される数式（[ コスト ]/[登録]など）:<ul><li>トラフィックと収益指標のリストから指標を挿入するには、指標を挿入する場所にカーソルを置き、リストから指標を選択するか、手動で入力して括弧で囲みます（例：`[CPC]`）。</li><li>演算子を挿入するには、演算子を挿入する位置にカーソルを置き、ボタンをクリックするか、記号を手動で入力します。 使用可能な数学演算子：`+ - * / ( ) ()`</li></ul><b>注：</b>複雑なカスタム指標の計算に時間がかかり、それを含むレポートやビュー（特にクリックスルーとビュースルーコンバージョン用の別々の列が含まれる場合）の生成に時間がかかります。 |
| 書式設定 | この指標のデータの表示方法：*[!UICONTROL Currency]* （金額）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]*、または&#x200B;*[!UICONTROL Percentage]* （小数点2点を含む割合）。<br><br><b>注意：</b>形式が[!UICONTROL Number w/out Decimal Points]の派生指標（データを整数として表示）を作成し、重み付けされたコンバージョン属性ルール （[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More]または[!UICONTROL Even Distribution]）を使用するビューまたはレポートに含める場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しいとしても、個々のデータフィールドが正しくない可能性があります。 例えば、注文が3つのイベント間で均等に分割されている場合、1つの注文（0.33の注文ではなく）は3つのイベントのそれぞれに関連付けられます。 この問題を回避するには、メトリック形式[!UICONTROL Number to 2 Decimal Points]を使用します。 |

## レポートとレポートテンプレートおよび従来の[!UICONTROL Portfolios] ビューのカスタム指標設定

| パラメーター/セクション | 説明 |
|----|----|
| カスタム指標名 | 列名として表示される指標の名前。 <b> ヒント：</b>意味のあるメトリック名を使用しますが、名前が長いほど列が広くなると考えてください。 |
| 書式設定 | この指標のデータの表示方法：*[!UICONTROL Currency]* （金額）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]*、または&#x200B;*[!UICONTROL Percentage]* （小数点2点を含む割合）。<br><br><b>注意：</b>形式が[!UICONTROL Number w/out Decimal Points]の派生指標（データを整数として表示）を作成し、重み付けされたコンバージョン属性ルール （[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More]または[!UICONTROL Even Distribution]）を使用するビューまたはレポートに含める場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しいとしても、個々のデータフィールドが正しくない可能性があります。 例えば、注文が3つのイベント間で均等に分割されている場合、1つの注文（0.33の注文ではなく）は3つのイベントのそれぞれに関連付けられます。 この問題を回避するには、メトリック形式[!UICONTROL Number to 2 Decimal Points]を使用します。 |
| 挿入指標 | 数式を作成できる既存の指標のリスト。<br><br>数式入力フィールドに指標を挿入するには、指標を挿入する場所にカーソルを置き、リストから指標を選択するか、手動で入力して角括弧で囲みます（例：`[CPC]`）。 |
| 挿入演算子 | 使用可能な数学演算子：`+ - x / ( )`<br><br>数式入力フィールドに演算子を挿入するには、演算子を挿入する場所にカーソルを置き、ボタンをクリックするか、記号を手動で入力します。 |
| [指標]の数式入力フィールド | 1つ以上の既存のプロパティまたは標準指標（`[Cost]/[Registrations]`など）に基づいて新しい指標を計算するために使用される数式。 指標と演算子の任意の組み合わせを含めることができます。<br><br><b>注：</b>複雑なカスタム指標の計算に時間がかかり、それを含むレポートやビュー（特にクリックスルーとビュースルーコンバージョン用の別々の列が含まれる場合）の生成に時間がかかります。 |

>[!MORELIKETHIS]
>
>* [ カスタム指標について](custom-metric-about.md)
>* [ カスタム指標を作成](custom-metric-create.md)
>* [ カスタム指標を編集](custom-metric-edit.md)
>* [ カスタム指標を削除](custom-metric-delete.md)
