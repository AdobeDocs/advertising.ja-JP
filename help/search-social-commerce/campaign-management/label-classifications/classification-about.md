---
title: ラベルの分類について
description: ラベル分類を使用してアカウントコンポーネントをグループ化する方法について説明します。
exl-id: 3ec4b111-225e-4272-b3dc-4f6f9c711779
feature: Search Label Classifications
TQID: https://experienceleague.adobe.com/dZL-v9IRny6Q2rjXcEeFKicL8UHKhRofQS4bBEd0sX8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 304
ht-degree: 0%

---

# ラベルの分類について

ラベル分類は、アカウントコンポーネントを意味のあるセットにグループ化するのに役立ちます。 例えば、「Geo」という親ラベル分類を作成し、分類の中で地理的地域（「United Kingdom」や「Japan」など）ごとに異なるラベル値を作成し、そのラベル値を[入札ユニット ](/help/search-social-commerce/glossary.md#a-b)または親キャンペーンに割り当てることができます。 その後、任意のラベル値をビューやレポートに別の列として含め、様々な分類グループや値に関するレポートをサブピボットできます。

## ラベルの分類

各広告主は、トップレベルのカテゴリである最大30個のラベル分類を持つことができます。

## ラベル値

各ラベル分類には、最大2000個の値を指定できます。 分類の特定のラベル値を作成したら、キャンペーン管理ビュー[または](classification-values-assign-campaign-management.md)から、バルクシート [を使用して、キャンペーン、広告グループ、キーワード、広告、プレースメント、製品グループ ](classification-values-assign-bulksheets.md)にそれらを割り当てることができます。

対象となる各エンティティには、複数の分類のラベル値を設定できますが、分類ごとに1つのラベル値のみを設定できます。 ラベル値は子エンティティによって継承されますが、上書きできます。 最下位レベルで割り当てられた値は、常に親レベルで割り当てられた値よりも優先されます。

## ラベル分類ビュー

レガシーUIでは、[!UICONTROL Labels Classifications] ビューは[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Labels Classifications]にあります。 新しいUIでは、[!UICONTROL Labels Classifications] ビューは[!UICONTROL Reports] > [!UICONTROL Labels Classifications]にあります。

[!UICONTROL Labels Classifications] ビューには、[!UICONTROL Classifications]と[!UICONTROL Label Values]個のサブビューが含まれています。 ラベル分類のデータを表示し、[create](classification-create.md)および[delete](classification-delete.md)のラベル分類を作成し、ラベル分類値のデータを表示できます。 デフォルトでは、データはキーワードレベルのラベル分類と値に表示されますが、オプションで広告レベルの分類と値のデータを表示できます。

新しいUIでは，

>[!MORELIKETHIS]
>
>* [ ラベル分類を作成](classification-create.md)
>* [ キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当てる](classification-values-assign-campaign-management.md)
>* [ バルクシートを使用してアカウントコンポーネントに分類値を割り当てる](classification-values-assign-bulksheets.md)
>* [ アカウントコンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [ ラベル分類値を削除](classification-values-delete.md)
>* [ ラベル分類を削除](classification-delete.md)
