---
title: カスタム指標設定
description: 標準指標から計算される、カスタム指標の設定を参照します。
exl-id: b9e8434d-5ea2-47cd-9d63-705a6337c34c
feature: Search Common Tasks, Search Custom Metrics
source-git-commit: a89a6513dfe468b98513b2d47c086a3107e63d47
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# カスタム指標設定

カスタム指標設定は、インターフェイスの様々な部分で若干異なります。

## ほとんどの管理ビューでのカスタム指標設定

| パラメーター/セクション | 説明 |
|----|----|
| カスタム指標名 | 列の名前として表示される指標の名前。 <b> ヒント：</b> 意味のある指標名を使用しますが、名前が長いと列が広くなると考えてください。 |
| 指標の挿入 | 新しい指標の計算に使用する数式（[ コスト ]/[ 登録など ]:<ul><li>トラフィック指標および売上高指標のリストから指標を挿入するには、指標を挿入する場所にカーソルを置き、リストから指標を選択するか、手動で指標を角括弧で囲んで入力します（例：`[CPC]`）。</li><li>演算子を挿入するには、演算子を挿入する位置にカーソルを置き、ボタンをクリックするか、記号を手動で入力します。 使用可能な数学演算子：`+ - * / ( ) ()`</li></ul><b> メモ：</b> 複雑なカスタム指標は、計算に時間がかかり、それらを含むレポートとビュー（特に、クリックスルーおよびビュースルーコンバージョン用に別々の列が含まれている場合）の生成にも時間がかかります。 |
| 書式設定 | この指標のデータを表示する方法：*[!UICONTROL Currency]* （金額）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]* または *[!UICONTROL Percentage]* （小数点 2 つ分のパーセンテージ）。<br><br><b> 注意：</b> 形式 [!UICONTROL Number w/out Decimal Points] （データを整数として表示）で派生指標を作成し、重み付けコンバージョンアトリビューションルール（[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More] または [!UICONTROL Even Distribution]）を使用するビューまたはレポートに含めた場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しくても、個々のデータフィールドが正しくない場合があります。 例えば、1 つの注文が 3 つのイベント間で均等に分割されている場合、3 つのイベントのそれぞれに 0.33 の注文ではなく 1 つの注文が関連付けられます。 この問題を回避するには、指標形式 [!UICONTROL Number to 2 Decimal Points] を使用します。 |

## レポートおよびレポートテンプレートと従来の [!UICONTROL Portfolios] ビューのカスタム指標設定

| パラメーター/セクション | 説明 |
|----|----|
| カスタム指標名 | 列の名前として表示される指標の名前。 <b> ヒント：</b> 意味のある指標名を使用しますが、名前が長いと列が広くなると考えてください。 |
| 書式設定 | この指標のデータを表示する方法：*[!UICONTROL Currency]* （金額）、*[!UICONTROL Number to 2 Decimal Points]*、*[!UICONTROL Number to 3 Decimal Points]*、*[!UICONTROL Number w/out Decimal Points]* または *[!UICONTROL Percentage]* （小数点 2 つ分のパーセンテージ）。<br><br><b> 注意：</b> 形式 [!UICONTROL Number w/out Decimal Points] （データを整数として表示）で派生指標を作成し、重み付けコンバージョンアトリビューションルール（[!UICONTROL Weight First Event More]、[!UICONTROL Weight Last Event More] または [!UICONTROL Even Distribution]）を使用するビューまたはレポートに含めた場合、出力は小数ではなく整数で表示されます。 その結果、合計が正しくても、個々のデータフィールドが正しくない場合があります。 例えば、1 つの注文が 3 つのイベント間で均等に分割されている場合、3 つのイベントのそれぞれに 0.33 の注文ではなく 1 つの注文が関連付けられます。 この問題を回避するには、指標形式 [!UICONTROL Number to 2 Decimal Points] を使用します。 |
| 指標の挿入 | 式を作成できる既存の指標のリスト。<br><br> 数式入力フィールドに指標を挿入するには、指標を挿入する位置にカーソルを置き、リストから指標を選択するか、手動で指標を角括弧で囲んで入力します（例：`[CPC]`）。 |
| 演算子を挿入 | 使用可能な数学演算子：`+ - x / ( )`<br><br> 数式入力フィールドに演算子を挿入するには、演算子を挿入する位置にカーソルを置き、ボタンをクリックするか、記号を手動で入力します。 |
| [ 指標の数式入力フィールド ] | 1 つ以上の既存のプロパティまたは標準指標（`[Cost]/[Registrations]` など）に基づいて新しい指標を計算するために使用される数式。 指標と演算子を任意に組み合わせることができます。<br><br><b> メモ：</b> 複雑なカスタム指標は、計算に時間がかかり、それらを含むレポートとビュー（特に、クリックスルーおよびビュースルーコンバージョン用に別々の列が含まれている場合）の生成にも時間がかかります。 |

>[!MORELIKETHIS]
>
>* [ カスタム指標について ](custom-metric-about.md)
>* [ カスタム指標の作成 ](custom-metric-create.md)
>* [ カスタム指標の編集 ](custom-metric-edit.md)
>* [ カスタム指標の削除 ](custom-metric-delete.md)
