---
title: バルクシートを使用したアカウントコンポーネントへの分類値の割り当て
description: バルクシートを使用して、分類値をアカウントコンポーネントに割り当てる方法を説明します。
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
source-git-commit: d68107b04762ea149dd74fb30ab7ea9d8850915f
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 0%

---

# バルクシートを使用したアカウントコンポーネントへの分類値の割り当て

バルクシートを使用して、キャンペーン、広告グループ、キーワード、広告、配置、単位レベルの製品グループ、動的検索ターゲットの検索エンティティの値にラベル分類を関連付けることができます。 各ラベル分類には、最大 2000 個の値を設定できます。

各エンティティには、分類ごとに 1 つのラベル値を設定できます。 例えば、Shoes_Campaign では、カラー値が「red」、地域値が「Los Angeles」に設定できますが、カラーと地域に複数の値を設定することはできません。

ラベル値は子エンティティによって継承されるため、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは [&#x200B; 不変 &#x200B;](/help/search-social-commerce/campaign-management/faqs-campaigns.md) です。つまり、それらを編集すると、既存のエンティティが削除され、新しいエンティティが作成されます。 この方法で既存の図形を削除すると、ラベル分類は新しい図形に割り当てられません。

1. ラベル分類値を割り当てるエンティティを含む [&#x200B; バルクシートをダウンロードします &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)。

   * 「[!UICONTROL Rows and Columns]」タブで、[!UICONTROL Campaign] ペインの [!UICONTROL Bulksheet Columns] リストを展開します。

   * [!UICONTROL Label Classification] リストを展開します。

   * バルクシートファイルに列を含める各分類を選択します。

     例えば、ラベル分類「色」および「地域」を含める場合、バルクシートには「色」列と「地域」列が含まれます。

1. ファイルをエディターで開き、関連付けるエンティティのラベル分類列にラベル値を追加します。 各値の最大長は 100 文字で、ASCII 文字と非 ASCII 文字を含めることができます。

   次の節の値の例を参照してください。

   値を追加する以外にも、関連する行から既存の値を削除することで、既存の値を削除することもできます。 親エンティティとその子エンティティの両方から値を削除するには、a）親エンティティ行のみを含めて既存の分類値を削除するか、b）親エンティティと子エンティティの両方を含めて、すべての親行と子行から既存の分類値を削除します。

1. [&#x200B; ファイルをアップロード &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) して、関連付けを作成します。<!-- Update once the new bulksheet UI is GA -->

アップロードされたラベル値は、関連するエンティティビューに表示されます。

## バルクシートにアップロードするラベル分類値の例

この例には、ラベル分類「Color」および「Geo」の列が含まれます。 独自のバルクシートの場合、独自のラベル分類名を列に置き換えます。

| アカウント | キャンペーン | 広告グループ | キーワード | 広告 | プレースメント | ラベル | カラー | 地域 |
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
>* [&#x200B; ラベル分類について &#x200B;](classification-about.md)
>* [&#x200B; ラベル分類の作成 &#x200B;](classification-create.md)
>* [&#x200B; キャンペーン管理ビューからアカウントコンポーネントへの分類値の割り当て &#x200B;](classification-values-assign-campaign-management.md)
>* [&#x200B; アカウントコンポーネントからラベル分類値を削除する &#x200B;](classification-values-remove.md)
>* [&#x200B; ラベル分類値を削除 &#x200B;](classification-values-delete.md)
>* [&#x200B; ラベル分類を削除 &#x200B;](classification-delete.md)
