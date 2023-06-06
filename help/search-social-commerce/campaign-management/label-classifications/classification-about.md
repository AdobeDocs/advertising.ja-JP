---
title: ラベルの分類について
description: ラベル分類を使用してアカウントコンポーネントをグループ化する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 0%

---

# ラベルの分類について

ラベルの分類は、アカウントコンポーネントを意味のあるセットにグループ化するのに役立ちます。 例えば、「地域」という親ラベル分類を作成し、分類内の地理的地域ごとに異なるラベル値（「英国」や「日本」など）を作成して、ラベル値を [入札単位](/help/search-social-commerce/glossary.md#a-b) または親キャンペーン。 その後、任意のラベル値をビューとレポートの個別の列として含め、様々な分類グループと値に関するレポートをサブピボットできます。

## ラベルの分類

各広告主は、最上位レベルのカテゴリである、最大 30 個のラベル分類を持つことができます。

## ラベル値

各ラベル分類には、最大 2,000 個の値を含めることができます。 分類に特定のラベル値を作成したら、キャンペーン、広告グループ、キーワード、広告、プレースメントおよび製品グループに割り当てることができます [キャンペーン管理ビューから](classification-values-assign-campaign-management.md) または [bulksheets の使用](classification-values-assign-bulksheets.md).

各適格なエンティティは、複数の分類に対してラベル値を持つことができますが、分類ごとに 1 つのラベル値のみを持つことができます。 ラベル値は子エンティティに継承されますが、上書きできます。 最下位レベルで割り当てられた値は、常に親レベルで割り当てられた値より優先されます。

## ラベルの分類ビュー

この [!UICONTROL Labels Classifications] 内の [!UICONTROL Search] > [!UICONTROL Campaigns] メニューの含まれる [!UICONTROL Classifications] および [!UICONTROL Label Values] サブビュー。 ラベル分類のデータを表示できます。 [作成](classification-create.md) および [削除](classification-delete.md) ラベルの分類を作成し、ラベル分類値のデータを表示します。 デフォルトでは、キーワードレベルのラベルの分類と値に関するデータが表示されますが、オプションで広告レベルの分類と値に関するデータを表示することもできます。

>[!MORELIKETHIS]
>
>* [ラベルの分類の作成](classification-create.md)
>* [分類値をキャンペーン管理ビューからアカウントコンポーネントに割り当てる](classification-values-assign-campaign-management.md)
>* [一括送信シートを使用して、勘定科目コンポーネントに分類値を割り当てます。](classification-values-assign-bulksheets.md)
>* [顧客コンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [ラベル分類値の削除](classification-values-delete.md)
>* [ラベルの分類を削除](classification-delete.md)

