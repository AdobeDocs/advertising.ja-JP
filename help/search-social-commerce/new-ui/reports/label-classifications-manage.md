---
title: ラベル分類の管理
description: ラベル分類を使用してアカウントコンポーネントをグループ化する方法について説明します。
feature: Search Label Classifications
source-git-commit: 84eb5f060a696e057f706c0066c18c9afc1511e1
workflow-type: tm+mt
source-wordcount: '1515'
ht-degree: 0%

---

# ラベル分類の管理

ラベル分類は、アカウントコンポーネントを意味のあるセットにグループ化するのに役立ちます。 例えば、「Geo」という親ラベル分類を作成し、分類の中で地理的地域（「United Kingdom」や「Japan」など）ごとに異なるラベル値を作成し、そのラベル値を[入札ユニット ](/help/search-social-commerce/glossary.md#a-b)または親キャンペーンに割り当てることができます。 その後、任意のラベル値をビューやレポートに別の列として含め、様々な分類グループや値に関するレポートをサブピボットできます。

## ラベル分類の構成要素

### ラベルの分類

各広告主は、トップレベルのカテゴリである最大30個のラベル分類を持つことができます。 ラベル分類を作成したら、分類に特定のラベル値を作成できます。

### ラベル値

各ラベル分類には、最大2000個の値を指定できます。 分類の特定のラベル値を作成したら、キャンペーン管理ビュー](#classification-values-assign-campaign-management)または[から、バルクシート ](#classification-values-assign-bulksheets)を使用して、キャンペーン、広告グループ、キーワード、広告、プレースメント、製品グループ [にそれらを割り当てることができます。

対象となる各エンティティには、複数の分類のラベル値を設定できますが、分類ごとに1つのラベル値のみを設定できます。 ラベル値は子エンティティによって継承されますが、上書きできます。 最下位レベルで割り当てられた値は、常に親レベルで割り当てられた値よりも優先されます。

## ラベル分類ビュー

[!UICONTROL Reports] > [!UICONTROL Labels Classifications] ビューには、[!UICONTROL Classifications]および[!UICONTROL Label Values]件のサブビューが含まれています。 デフォルトでは、データはキーワードレベルのラベル分類と値に表示されますが、オプションで広告レベルの分類と値のデータを表示できます。

## 使用可能なアクション

* ラベル分類のデータを表示します。

* ラベル分類値のデータを表示します。

* [ ラベル分類を作成](#classification-create)。

* バルクシート ](#classification-values-assign-bulksheets)を使用して、キャンペーン管理ビュー](#classification-values-assign-campaign-management)または[からアカウントコンポーネント [に分類値を割り当てます。

* [ アカウントコンポーネント ](#classification-values-remove)からラベル分類値を削除します。

* [ ラベル分類値を削除](#classification-values-delete)。

* [ ラベル分類を削除](#classification-delete)。

## ラベル分類の作成 {#classification-create}

<!-- Update links to bulksheet columns once I have new files/paths -->

1. **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**&#x200B;をクリックします。

1. 右上の「**[!UICONTROL Create Classification]**」をクリックします。

1. 一意のラベル分類名を入力し、**[!UICONTROL Create]**&#x200B;をクリックします。

   名前は、広告主アカウントに対して一意である必要があり、[ASCII文字32 ～ 126](https://www.asciitable.com/)で構成され、最大長は27文字です。 名前は、既存のレポート列または既存のバルクシート列の名前と同じにすることはできません。 [Baidu](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-baidu.md)、[Google Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-google.md)、[Microsoft Advertising](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-microsoft.md)、[Naver](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)、[Yahoo！のバルクシート列の名前を参照してください。 Japan Ads](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-japan.md), [Yahoo! ネットワーク ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yahoo-display-network.md)および[Yandex](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-yandex.md)を表示します。

## キャンペーン管理ビューからアカウントコンポーネントに分類値を割り当て {#classification-values-assign-campaign-management}

キャンペーン管理ビューから、キャンペーン、広告グループ、キーワード、広告、プレースメント、ユニットレベルの製品グループ、動的検索ターゲットの次の検索エンティティの分類値を割り当てて削除できます。 必要に応じて、割り当てプロセス中に分類と分類値を作成できます。 各ラベル分類には、最大2000個の値を指定できます。

各エンティティは、分類ごとに1つのラベル値を持つことができます。 例えば、Shoes_Campaignでは、「Color」の値に「red」を、Geoの値に「Los Angeles」を指定できますが、「Color」または「Geo」に複数の値を指定することはできません。

ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは[変更不可](/help/search-social-commerce/campaign-management/faqs-campaigns.md)です。これは、編集すると既存のエンティティが削除され、新しいエンティティが作成されることを意味します。 この方法で既存のエンティティが削除された場合、ラベル分類は新しいエンティティに割り当てられません。

1. **[!UICONTROL Manage]**&#x200B;または&#x200B;**[!UICONTROL Target]** メニューからエンティティ ビューを開きます。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**+[!UICONTROL Assign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 適用できる各分類値について、次の操作を行います。

   1. **[!UICONTROL Classifications]**&#x200B;列で、分類を指定します。

      * 既存の分類を使用するには、分類名をクリックして展開します。

      * 分類を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに分類名を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして、分類をすぐに保存します。 新しい分類を使用するには、分類名をクリックして展開します。

        名前は[ASCII文字32 ～ 126](https://www.asciitable.com/)で、最大長は27文字です。

   1. **[!UICONTROL Value Name]**&#x200B;列で、選択した分類の値を指定します。

      * 既存の値を使用するには、値を選択します。

      * 値を作成するには、列見出しの[!UICONTROL +]をクリックします。 入力フィールドに値を入力し、![保存](/help/search-social-commerce/assets/save-checkmark.png "保存")をクリックして値をすばやく保存し、デフォルトで選択します。

        最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

1. **+[!UICONTROL Assign Now]**&#x200B;をクリックします。

## バルクシートを使用して、アカウントコンポーネントに分類値を割り当て {#classification-values-assign-bulksheets}

<!-- Update bulksheet references to ones in new UI -->

ラベル分類を、キャンペーン、広告グループ、キーワード、広告、プレースメント、単位レベルの製品グループ、動的検索ターゲットなどのバルクシートを使用して、次の検索エンティティの値に関連付けることができます。 各ラベル分類には、最大2000個の値を指定できます。

各エンティティは、分類ごとに1つのラベル値を持つことができます。 例えば、Shoes_Campaignでは、「Color」の値に「red」を、Geoの値に「Los Angeles」を指定できますが、「Color」または「Geo」に複数の値を指定することはできません。

ラベル値は子エンティティによって継承されるので、継承された値を上書きする場合を除き、子エンティティの値を入力しないでください。

>[!NOTE]
>
>一部の広告ネットワークおよびキャンペーンタイプのキーワードと広告コピーは[変更不可](/help/search-social-commerce/campaign-management/faqs-campaigns.md)です。これは、編集すると既存のエンティティが削除され、新しいエンティティが作成されることを意味します。 この方法で既存のエンティティが削除された場合、ラベル分類は新しいエンティティに割り当てられません。

1. [ ラベル分類値を割り当てるエンティティを含むバルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)をダウンロードします。

   * [!UICONTROL Rows and Columns] タブで、[!UICONTROL Bulksheet Columns] ペインの[!UICONTROL Campaign] リストを展開します。

   * [!UICONTROL Label Classification] リストを展開します。

   * バルクシート ファイルに列を含める各分類を選択します。

     例えば、「カラー」と「地域」のラベル分類を含める場合、バルクシートには「カラー」と「地域」の列が含まれます。

1. エディターでファイルを開き、関連付けるエンティティのラベル分類列にラベル値を追加します。 各値の最大長は100文字で、ASCII文字と非ASCII文字を含めることができます。

   次の節の値の例を参照してください。

   値を追加するだけでなく、関連する行から既存の値を削除することもできます。 親エンティティとその子エンティティの両方から値を削除するには、a）親エンティティ行のみを含めて既存の分類値を削除するか、b）親エンティティとその子エンティティの両方を含めて、すべての親行と子行から既存の分類値を削除します。

1. [ ファイル ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)をアップロードして、関連付けを作成します。<!-- Update once the new bulksheet UI is GA -->

アップロードされたラベル値は、関連するエンティティのビューに表示されます。

### バルクシートにアップロードするラベル分類値の例

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

## アカウントコンポーネントからのラベル分類値の削除 {#classification-values-remove}

分類値を削除すると、アカウントコンポーネントとそのすべての子コンポーネントとの関連付けが削除されます。 分類値のレポートデータは、これらのコンポーネントでは使用できなくなりました。 分類値を削除しても、値やアカウントコンポーネントは削除されません。

>[!NOTE]
>
>ラベル分類から値を削除するには、「[ ラベル分類値を削除](#classification-values-delete)」を参照してください。

1. **[!UICONTROL Manage]**&#x200B;または&#x200B;**[!UICONTROL Target]** メニューからエンティティ ビューを開きます。

1. 各関連行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**-[!UICONTROL Unassign]** > **[!UICONTROL Label Classification]**&#x200B;をクリックします。

1. 選択したエンティティから削除する各分類値の横にあるチェックボックスをオンにします。<!-- As of 2/24/26, no way to tell which entity each value is assigned to -->

   割り当てられたすべての値を選択するには、**[!UICONTROL Select All]**&#x200B;をクリックします。 割り当てられた値をすべて選択解除するには、**[!UICONTROL Deselect All]**&#x200B;をクリックします。

1. **[!UICONTROL Unassign Selected]**&#x200B;をクリックします。

## ラベル分類値の削除 {#classification-values-delete}

ラベル分類値を削除すると、後で使用できなくなり、レポート データは値に使用できなくなります。 値と親ラベル分類および特定のアカウントコンポーネントとの間のすべての割り当ては削除されますが、親ラベル分類とキャンペーンコンポーネントは削除されません。

>[!NOTE]
>
>アカウントコンポーネントから分類値を簡単に関連付け解除するには、「[ アカウントコンポーネントからラベル分類値を削除](#classification-values-remove)」を参照してください。

1. **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**&#x200B;をクリックします。

1. 「**[!UICONTROL Label Values]**」タブをクリックします。

1. （オプション）特定のラベル値を含めるようにリストをフィルタリングします。

1. 削除する各ラベル値の横にあるチェックボックスをオンにします。

   一度に最大200行まで削除できます。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## ラベル分類の削除

分類を削除すると、その子値とアカウントコンポーネント間のすべての関連付けが削除されます。 削除された分類とその値は、今後の使用に使用できません。 分類値のレポートデータが使用できるようになりました。

>[!NOTE]
>
>アカウントコンポーネントから分類値を簡単に関連付け解除するには、「[ アカウントコンポーネントからラベル分類値を削除](#classification-values-remove)」を参照してください。

1. **[!UICONTROL Reports]>[!UICONTROL Label Classifications]**&#x200B;をクリックします。

1. （オプション）特定のラベル分類を含めるようにリストをフィルタリングします。

1. 削除する各ラベル分類の横にあるチェックボックスをオンにします。

   一度に最大200行まで削除できます。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。
