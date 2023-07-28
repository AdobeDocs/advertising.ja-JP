---
title: バルクシートで実行できる操作
description: バルクシートを使用したキャンペーンデータの追加、編集、削除に関する一般情報を参照してください。
exl-id: 82969bb8-dff8-48e7-b37d-1446a2a90072
feature: Search Bulksheets
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# バルクシートで実行できる操作

一括送信シートでキャンペーンデータの追加、編集および削除を行えます。 [サポートされる広告ネットワーク](../bulksheet-about.md#bulksheet-functionality-by-network).

追加、編集または削除するキャンペーンコンポーネント（キャンペーン、広告グループ、キーワード、テキスト広告）、またはプロパティを追加、編集または削除するキャンペーンコンポーネント（キャンペーン、広告グループ、キーワード、テキスト広告）ごとに別々のデータ行を含めます。 例えば、1 つの広告グループ、1 つのキーワード、1 つの広告（合計 4 つのコンポーネント）を含むキャンペーンを作成する場合は、4 つの異なるデータ行が必要です。 次の手順で [!UICONTROL Ad Group Name] ただし、広告グループ（1 つのコンポーネント）の場合は、1 行だけで済みます。 同様に、1 つの広告グループ（1 つのコンポーネント）に対して 4 つの異なるプロパティを編集するには、1 行だけで済みます。

以下のルールは、キャンペーンのコンポーネントとそのプロパティの操作に適用されます。

* 追加中：

   * コンポーネントを追加するには、そのコンポーネントの追加に必要なすべてのフィールドを含め、オプションで、コンポーネントのプロパティのフィールドを含めます。

   * 既存のコンポーネントのプロパティを追加するには、次の手順を実行します。 [!UICONTROL Ad Group End Date] 広告グループの場合、そのコンポーネント（広告グループ）の編集に必要なすべてのフィールドと、プロパティのフィールド ([!UICONTROL Ad Group End Date]) をクリックします。

* 既存のコンポーネントのプロパティを編集するには、そのコンポーネントの編集に必要なすべてのフィールドと、そのプロパティのフィールドを含めます。

  プロパティフィールドを空白のままにした場合、既存の値が保持されます。

* 削除中：

   * 既存のコンポーネントを削除するには、そのコンポーネントの編集に必要なすべてのフィールドを含め、ステータスを「 [!UICONTROL Deleted]. 例えば、 [!DNL Google Ads] 広告グループに含めるには、 [!UICONTROL Campaign Name], [!UICONTROL Ad Group Name], [!UICONTROL Ad Group Status] 値を持つ <i>[!UICONTROL Deleted]</i>、および [!UICONTROL Ad Group ID].

   * ([!UICONTROL Param1], [!UICONTROL Param2]、および [!UICONTROL Param3] 値のみ ) 既存の [!DNL paramN] キーワードの値、キーワードの編集に必要なすべてのフィールドを含め、既存の [!DNL paramN] 値を入力して `[delete]` （括弧を含む）を含む ) を含めます。

   * （許可されているプロパティフィールド）コンポーネントの既存のプロパティ値を削除するには、そのコンポーネントの編集に必要なすべてのフィールドを含め、値を入力してプロパティ値も削除します。 `[delete]` （括弧を含む）。 使用できるフィールドは次のとおりです。

      * ([!UICONTROL Google Ads] のみ ) [!UICONTROL Description Line 1], [!UICONTROL Description Line 2]

      * ([!DNL Google Ads] および [!DNL Microsoft® Advertising] のみ ) [!UICONTROL Product Scope Filter], [!UICONTROL Base URL/Final URL], [!UICONTROL Tracking Template]

>[!NOTE]
>
>アクションに適用できないフィールドに値を含めた場合、そのフィールドに入力された値は無視されます。

>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](../bulksheet-about.md)
>* [サポートされるバルクシートファイル形式](bulksheet-file-formats.md)
>* [付録 — バルクシートエラー](../bulksheet-errors.md)
>* [バルクシートファイルをダウンロード/作成する](../bulksheet-download.md)
