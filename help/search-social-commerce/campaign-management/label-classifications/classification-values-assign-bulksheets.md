---
title: バルクシートを使用して、アカウントコンポーネントに分類値を割り当て
description: バルクシートを使用して、アカウントコンポーネントに分類値を割り当てる方法を説明します。
exl-id: b2dfd487-097c-45f8-a6a5-24395fdb2b85
feature: Search Label Classifications
TQID: https://experienceleague.adobe.com/zLEy6MglSGlf6WnoO2oEgSdPLwlp-5cBdmxi-XXiv5g
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 479
ht-degree: 0%

---

# バルクシートを使用して、アカウントコンポーネントに分類値を割り当て

ラベル分類を、キャンペーン、広告グループ、キーワード、広告、プレースメント、単位レベルの製品グループ、動的検索ターゲットなどのバルクシートを使用して、次の検索エンティティの値に関連付けることができます。 各ラベル分類には、最大2000個の値を指定できます。

各エンティティは、分類ごとに1つのラベル値を持つことができます。 例えば、Shoes_Campaignでは、「Color」の値に「red」を、Geoの値に「Los Angeles」を指定できますが、「Color」または「Geo」に複数の値を指定することはできません。

ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは[変更不可](/help/search-social-commerce/campaign-management/faqs-campaigns.md)です。これは、編集すると既存のエンティティが削除され、新しいエンティティが作成されることを意味します。 この方法で既存のエンティティが削除された場合、ラベル分類は新しいエンティティに割り当てられません。

1. [&#x200B; ラベル分類値を割り当てるエンティティを含むバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)をダウンロードします。

   * [!UICONTROL Rows and Columns] タブで、[!UICONTROL Campaign] ペインの[!UICONTROL Bulksheet Columns] リストを展開します。

   * [!UICONTROL Label Classification] リストを展開します。

   * バルクシート ファイルに列を含める各分類を選択します。

     例えば、「カラー」と「地域」のラベル分類を含める場合、バルクシートには「カラー」と「地域」の列が含まれます。

1. エディターでファイルを開き、関連付けるエンティティのラベル分類列にラベル値を追加します。 各値の最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

   次の節の値の例を参照してください。

   値を追加するだけでなく、関連する行から既存の値を削除することもできます。 親エンティティとその子エンティティの両方から値を削除するには、a）親エンティティ行のみを含めて既存の分類値を削除するか、b）親エンティティとその子エンティティの両方を含めて、すべての親行と子行から既存の分類値を削除します。

1. [&#x200B; ファイル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)をアップロードして、関連付けを作成します。<!-- Update once the new bulksheet UI is GA -->

アップロードされたラベル値は、関連するエンティティのビューに表示されます。

## バルクシートにアップロードするラベル分類値の例

この例には、「カラー」と「地域」のラベル分類の列が含まれます。 独自のバルクシートの場合は、独自のラベル分類名の代わりに列を使用します。

| アカウント | キャンペーン | 広告グループ | キーワード | 広告 | プレースメント | ラベル | カラー | 地域 |
|---|---|---|---|---|---|---|---|---|
| Acct1 | C1 | | | | | | 緑 | |
| Acct1 | C1 | AG1 | | | | | | |
| Acct1 | C1 | AG1 | K1 | | | | | UK |
| Acct1 | C1 | AG1 | K2 | | | | 赤 | AU |
| Acct1 | C1 | AG1 | K3 | | | | 青 | DE |
| Acct1 | C1 | AG1 | | A1 | | | | |
| Acct1 | C1 | AG1 | | A1 | | | 赤 | |
| Acct1 | C1 | AG1 | | | P1 | | 赤 | AU |
| Acct1 | C1 | AG1 | | | P2 | | 青 | DE |

>[!MORELIKETHIS]
>
>* [&#x200B; ラベル分類について](classification-about.md)
>* [&#x200B; ラベル分類を作成](classification-create.md)
>* [&#x200B; キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当てる](classification-values-assign-campaign-management.md)
>* [&#x200B; アカウントコンポーネントからラベル分類値を削除](classification-values-remove.md)
>* [&#x200B; ラベル分類値を削除](classification-values-delete.md)
>* [&#x200B; ラベル分類を削除](classification-delete.md)
