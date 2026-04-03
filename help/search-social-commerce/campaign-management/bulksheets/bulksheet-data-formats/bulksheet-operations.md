---
title: バルクシートで実行できる操作
description: バルクシートを使用したキャンペーンデータの追加、編集および削除に関する一般的な情報を参照します。
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/v0lNqlMXWFmw8O1Tr51d-WoHC-X2dxdSh-ZRKIPxGQY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 381
ht-degree: 0%

---

# バルクシートで実行できる操作

[&#x200B; サポートされている広告ネットワーク &#x200B;](../bulksheet-about.md#bulksheet-functionality-by-network)のバルクシートを使用して、キャンペーンデータを追加、編集、削除できます。

追加、編集、削除するキャンペーンコンポーネント（キャンペーン、広告グループ、キーワード、テキスト広告）または追加、編集、削除するプロパティごとに個別のデータ行を含めます。 たとえば、ひとつの広告グループ、ひとつのキーワード、ひとつの広告でキャンペーンを構成したい場合、合計4つのコンポーネントが必要になります。データラインは4つ別々に作成する必要があります。 ただし、広告グループ（1つのコンポーネント）の[!UICONTROL Ad Group Name]を編集するには、1行のみが必要です。 同様に、1つの広告グループ（1つのコンポーネント）に4つの異なるプロパティを編集するには、1行のみが必要です。

キャンペーンコンポーネントとそのプロパティの操作には、次のルールが適用されます。

* 追加：

   * コンポーネントを追加するには、そのコンポーネントの追加に必要なすべてのフィールドと、オプションでコンポーネントのプロパティのフィールドを含める必要があります。

   * 広告グループの[!UICONTROL Ad Group End Date]など、既存のコンポーネントのプロパティを追加するには、そのコンポーネント（広告グループ）の編集に必要なすべてのフィールドと、プロパティ（[!UICONTROL Ad Group End Date]）のフィールドを含めます。

* 既存のコンポーネントのプロパティを編集するには、そのコンポーネントの編集に必要なすべてのフィールドとプロパティのフィールドを含めます。

  プロパティフィールドを空白のままにすると、既存の値が保持されます。

* 削除：

   * 既存のコンポーネントを削除するには、そのコンポーネントを編集するために必要なすべてのフィールドを含め、そのステータスを[!UICONTROL Deleted]に変更します。 例えば、[!DNL Google Ads]広告グループを削除するには、[!UICONTROL Campaign Name]、[!UICONTROL Ad Group Name]、[!UICONTROL Ad Group Status]を値<i>[!UICONTROL Deleted]</i>および[!UICONTROL Ad Group ID]で含める必要があります。

   * （[!UICONTROL Param1]、[!UICONTROL Param2]、および[!UICONTROL Param3]値のみ）キーワードの既存の[!DNL paramN]値を削除するには、キーワードの編集に必要なすべてのフィールドを含め、対応するフィールドに値[!DNL paramN] （括弧を含む）を入力して既存の`[delete]`値も削除します。

   * （許可されるプロパティフィールド）コンポーネントの既存のプロパティ値を削除するには、そのコンポーネントを編集するために必要なすべてのフィールドを含め、値`[delete]` （括弧を含む）を入力してプロパティ値を削除します。 許可されるフィールドは次のとおりです。

      * （[!UICONTROL Google Ads]のみ） [!UICONTROL Description Line 1]、[!UICONTROL Description Line 2]

      * （[!DNL Google Ads]と[!DNL Microsoft Advertising]のみ） [!UICONTROL Product Scope Filter]、[!UICONTROL Base URL/Final URL]、[!UICONTROL Tracking Template]

>[!NOTE]
>
>アクションに適用できないフィールドに値を含めると、フィールドに入力された値は無視されます。

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用したキャンペーンデータの管理について](../bulksheet-about.md)
>* [&#x200B; サポートされているバルクシート ファイル形式](bulksheet-file-formats.md)
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
