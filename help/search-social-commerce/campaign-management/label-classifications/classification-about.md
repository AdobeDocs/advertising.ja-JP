---
title: ラベルの分類について
description: ラベル分類を使用したアカウントコンポーネントのグループ化について説明します。
exl-id: 3ec4b111-225e-4272-b3dc-4f6f9c711779
feature: Search Label Classifications
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# ラベルの分類について

ラベル分類は、アカウントコンポーネントを意味のあるセットにグループ化するのに役立ちます。 例えば、「地域」という親ラベル分類を作成し、分類内の各地理的地域（「英国」や「日本」など）に異なるラベル値を作成して、[ 入札単位 ](/help/search-social-commerce/glossary.md#a-b) または親キャンペーンにラベル値を割り当てることができます。 その後、任意のラベル値を個別の列としてビューやレポートに含め、異なる分類グループや値に基づいてレポートをサブピボットできます。

## ラベルの分類

各広告主には、最大 30 個のラベル分類を指定できます。これは最上位レベルのカテゴリです。

## ラベルの値

各ラベル分類には、最大 2000 個の値を設定できます。 分類に特定のラベル値を作成したら、それらをキャンペーン、広告グループ、キーワード、広告、配置、製品グループに [&#128279;](classification-values-assign-bulksheets.md) キャンペーン管理ビューまたは [ バルクシートの使用 ](classification-values-assign-campaign-management.md) から  割り当てることができます。

各適格エンティティは、複数の分類のラベル値を持つことができますが、分類ごとに 1 つのラベル値のみを持つことができます。 ラベル値は、子エンティティに継承されますが、上書きできます。 最下位レベルで割り当てられた値は、常に親レベルで割り当てられた値を上書きします。

## ラベルの分類ビュー

[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] メニュー内の [!UICONTROL Labels Classifications] ビューには、[!UICONTROL Classifications] と [!UICONTROL Label Values] のサブビューが含まれます。 ラベル分類のデータを表示したり、ラベル分類を [ 作成 ](classification-create.md) および [ 削除 ](classification-delete.md) したり、ラベル分類値のデータを表示することができます。 デフォルトでは、キーワードレベルのラベルの分類と値のデータが表示されますが、オプションで、広告レベルの分類と値のデータを表示することもできます。

>[!MORELIKETHIS]
>
>* [ ラベル分類の作成 ](classification-create.md)
>* [ キャンペーン管理ビューからアカウントコンポーネントへの分類値の割り当て ](classification-values-assign-campaign-management.md)
>* [ バルクシートを使用した勘定科目コンポーネントへの分類値の割当て ](classification-values-assign-bulksheets.md)
>* [ アカウントコンポーネントからラベル分類値を削除する ](classification-values-remove.md)
>* [ ラベル分類値を削除 ](classification-values-delete.md)
>* [ ラベル分類を削除 ](classification-delete.md)
