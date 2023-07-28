---
title: 一括送信シートを使用して、勘定科目コンポーネントに分類値を割り当てます。
description: バルクシートを使用して分類値をアカウントコンポーネントに割り当てる方法を説明します。
exl-id: 9bb38f28-d6bc-41f4-9c28-b391d9b9e412
feature: Search Label Classifications
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 7%

---

# 一括送信シートを使用して、勘定科目コンポーネントに分類値を割り当てます。

一括送信シートを使用して、ラベル分類を次の検索エンティティの値に関連付けることができます。キャンペーン、広告グループ、キーワード、広告、配置、単位レベルの製品グループ、動的検索ターゲット。 各ラベル分類には、最大 2,000 個の値を含めることができます。

各エンティティは、分類ごとに 1 つのラベル値を持つことができます。 例えば、Shoes_Campaign のカラー値は「red」、地域値は「Los Angeles」にできますが、カラーまたは地域に複数の値を含めることはできません。

ラベル値は子エンティティに継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードおよび広告コピーは、次のとおりです [不変](/help/search-social-commerce/campaign-management/faqs-campaigns.md)を編集すると、既存のエンティティが削除され、新しいエンティティが作成されます。 この方法で既存のエンティティを削除した場合、ラベルの分類は新しいエンティティに割り当てられません。

1. [バルクシートのダウンロード](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) ラベル分類値を割り当てるエンティティが含まれる

   * 次の日： [!UICONTROL Rows and Columns] タブ、展開 [!UICONTROL Campaign] リスト [!UICONTROL Bulksheet Columns] ウィンドウ

   * を展開します。 [!UICONTROL Label Classification] リスト。

   * バルクシートファイルに列を含める各分類を選択します。

     例えば、ラベル分類に「色」と「地域」を含めると、バルクシートに「色」と「地域」の列が含まれます。

1. ファイルをエディターで開き、関連付けるエンティティのラベル分類列にラベル値を追加します。 各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

   次の節の値の例を参照してください。

   値を追加する以外に、関連する行から既存の値を削除して、既存の値を削除することもできます。 親エンティティとその子エンティティの両方から値を削除するには、a) 親エンティティ行のみを含め、既存の分類値を削除する、b) 親エンティティと子エンティティの両方を含め、すべての親行と子行から既存の分類値を削除します。

1. [ファイルをアップロード](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) 関連付けを作成します。

アップロードされたラベル値は、関連するエンティティビューに表示されます。

## バルクシートにアップロードするラベル分類値の例

この例には、ラベル分類の列として、「Color」および「Geo」が含まれます。 独自のバルクシートの場合は、独自のラベル分類名を列に置き換えます。

| アカウント | Campaign | 広告グループ | キーワード | 広告 | プレースメント | ラベル | カラー | 地域 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | 緑 | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | 英国 |
| Acct1 | C1 | AG1 | K2 | | | | 赤 | AU |
| Acct1 | C1 | AG1 | K3 | | | | 青 | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | 赤 | |
| Acct1 | C1 | AG1 | | | P1 | | 赤 | AU |
| Acct1 | C1 | AG1 | | | P2 | | 青 | DE |

>[!MORELIKETHIS]
>
>* [ラベルの分類について](classification-about.md)
>* [ラベルの分類の作成](classification-create.md)
>* [分類値をキャンペーン管理ビューからアカウントコンポーネントに割り当てる](classification-values-assign-campaign-management.md)
>* [顧客コンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [ラベル分類値の削除](classification-values-delete.md)
>* [ラベルの分類を削除](classification-delete.md)
