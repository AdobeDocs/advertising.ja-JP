---
title: バルクシートで実行できる操作
description: バルクシートを使用したキャンペーンデータの追加、編集、削除に関する一般情報を参照します。
exl-id: 17ec9307-6dfd-45cb-b8bd-d0d7fcbf2d41
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 0%

---

# バルクシートで実行できる操作

[ サポートされている広告ネットワーク ](../bulksheet-about.md#bulksheet-functionality-by-network) のバルクシートを使用して、キャンペーンデータを追加、編集、削除できます。

追加、編集、削除するキャンペーンコンポーネント（キャンペーン、広告グループ、キーワード、テキスト広告）、またはプロパティを追加、編集、削除するキャンペーンコンポーネントごとに個別のデータ行を含めます。 例えば、1 つの広告グループ、1 つのキーワードおよび 1 つの広告（合計 4 つのコンポーネント）でキャンペーンを作成する場合、4 つの異なるデータラインが必要です。 ただし、広告グループの [!UICONTROL Ad Group Name] を編集する場合（1 つのコンポーネント）は、1 行で済みます。 同様に、1 つの広告グループ（1 つのコンポーネント）に対して 4 つの異なるプロパティを編集する場合は、必要なプロパティは 1 行だけです。

キャンペーンコンポーネントとそのプロパティの操作には、次のルールが適用されます。

* 追加中：

   * コンポーネントを追加するには、そのコンポーネントの追加に必要なすべてのフィールドを含め、オプションで、コンポーネントのプロパティのフィールドを含めます。

   * 広告グループの [!UICONTROL Ad Group End Date] など、既存のコンポーネントのプロパティを追加するには、そのコンポーネント（広告グループ）を編集するために必要なすべてのフィールドと、プロパティのフィールド（[!UICONTROL Ad Group End Date]）を含めます。

* 既存のコンポーネントのプロパティを編集するには、そのコンポーネントの編集に必要なすべてのフィールドと、プロパティのフィールドを含めます。

  このプロパティフィールドを空白のままにすると、既存の値が保持されます。

* 削除中：

   * 既存のコンポーネントを削除するには、そのコンポーネントの編集に必要なすべてのフィールドを含めて、ステータスを [!UICONTROL Deleted] に変更します。 例えば、[!DNL Google Ads] の広告グループを削除するには、[!UICONTROL Campaign Name]、[!UICONTROL Ad Group Name]、[!UICONTROL Ad Group Status] （値が <i>[!UICONTROL Deleted]</i>、[!UICONTROL Ad Group ID]）を含める必要があります。

   * （[!UICONTROL Param1]、[!UICONTROL Param2]、[!UICONTROL Param3] 値のみ）キーワードの既存の [!DNL paramN] 値を削除するには、キーワードの編集に必要なすべてのフィールドを含め、対応するフィールドに値 `[delete]` （角括弧を含めて）を入力して既存の [!DNL paramN] 値を削除します。

   * （許可されたプロパティフィールド）コンポーネントの既存のプロパティ値を削除するには、そのコンポーネントの編集に必要なすべてのフィールドを含め、値 `[delete]` （角括弧を含む）を入力してプロパティ値を削除します。 使用できるフィールドは次のとおりです。

      * （[!UICONTROL Google Ads] のみ） [!UICONTROL Description Line 1]、[!UICONTROL Description Line 2]

      * （[!DNL Google Ads] および [!DNL Microsoft Advertising] のみ） [!UICONTROL Product Scope Filter]、[!UICONTROL Base URL/Final URL]、[!UICONTROL Tracking Template]

>[!NOTE]
>
>アクションに適用されない値をフィールドに含めた場合、そのフィールドに入力された値は無視されます。

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign データの管理について ](../bulksheet-about.md)
>* [ サポートされるバルクシート ファイル形式 ](bulksheet-file-formats.md)
>* [ 付録 – バルクシート エラー ](../bulksheet-errors.md)
>* [ バルクシートファイルのダウンロード/作成 ](../bulksheet-download.md)
