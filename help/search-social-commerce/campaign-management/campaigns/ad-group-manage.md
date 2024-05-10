---
title: 広告グループの管理
description: 広告グループを作成および管理する方法について説明します。
exl-id: 66900a1f-f915-497d-9053-9d393845af08
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 広告グループの管理

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]、および既存 [!DNL Baidu] アカウントのみ*

広告グループには、広告とその関連キーワードのセットが含まれます。 ディスプレイネットワークをターゲットとするキャンペーンの広告グループには、プレースメントも含めることができます。プレースメントは、広告が表示されるディスプレイネットワーク上の場所です。 広告グループの設定は、広告グループのすべてのコンポーネントに適用され、広告ネットワークによって異なります。

検索、ソーシャル、Commerce内から広告グループを作成できます [サポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md) within a [同期済み広告ネットワーク アカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md). 広告グループのステータスを編集および変更することもできます。

## 広告グループの作成

>[!TIP]
>
>一度に大量の広告グループデータを追加するには、 [機能をコピー&amp;ペースト](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [campaign バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. データ テーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーンを選択し、 **[!UICONTROL Continue]**.

1. を入力 [バイドゥ](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md), [Google広告](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md), [Yahoo! 日本広告](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)、または [ヤンデックス](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md) 広告グループ設定。

   広告ネットワークに応じて、設定はにグループ化できます [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]. の設定を指定するには [!UICONTROL Adgroup Frequency Cap Settings], [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites]使用可能な場合は、 **[!UICONTROL Add Frequency Cap Settings]**, **[!UICONTROL Add Negative Keywords]**、または **[!UICONTROL Add Negative Websites]**、それぞれ。

1. クリック **[!UICONTROL Post]**.

後でオプションで、広告グループ内の個々のキーワードまたはプレースメントに入札を設定することで、広告グループレベルの入札を上書きできます。

## 広告グループ設定の編集

個々の広告グループの設定を編集できます。 また、選択したすべてのキャンペーンに共通する広告グループの詳細、予算オプション、URL オプションなど、複数の広告グループの一部のフィールドを一度に編集することもできます。

>[!TIP]
>
>大量のデータを一度に編集するには、 [機能をコピー&amp;ペースト](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [バルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. 次のいずれかの操作をおこないます。

   1. （単一の広告グループの設定を編集するには）図形名の上にカーソルを置き、クリックします ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択してから、 **[!UICONTROL Edit]**.

   1. （1 つ以上の広告グループの設定を編集するには）次の手順を実行します。

      * 各広告グループの横にあるチェックボックスを選択します。

        複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

      * データ テーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集する [バイドゥ](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md), [Google広告](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md), [Yahoo! 日本広告](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)、または [ヤンデックス](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md) 広告グループ設定。

   複数の広告グループの場合、設定はにグループ化できます [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]（広告ネットワークによって異なります）。 編集できるのは、選択したすべての広告グループに共通のフィールドのみで、変更は選択したすべての広告グループに適用されます。 一部の英数字フィールドでは、既存の値を指定の値に変更する、既存の文字列を指定の文字列に置き換える、各値の先頭に指定のプレフィックスを追加する、各値の末尾にサフィックスを追加する、などのオプションがあります。 一部の通貨フィールドでは、既存の値を指定の値に変更するか、制限を設けて、指定の割合または金額で金額を増減するオプションがあります。

   単一の広告グループの場合、設定はにグループ化できます [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]. の設定を指定するには [!UICONTROL Negative Keywords] または [!UICONTROL Negative Websites]使用可能な場合は、 **[!UICONTROL Add Negative Keywords]** または **[!UICONTROL Add Negative Websites]**、それぞれ。

1. データを保存します。

   * （単一の広告グループ）クリック **[!UICONTROL Post]**.

   * （複数の広告グループ）クリック **[!UICONTROL Post Now]**.

## 広告グループのステータスの変更

アクティブな検索広告グループを一時停止して、そのグループへの入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブまたは一時停止されている検索広告グループを削除することもできます。 削除された広告グループは広告ネットワークから削除されます。 これらは引き続き表示されますが、変更することはできません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. （任意）特定の広告グループを含めるようにリストをフィルタリングします。

1. ステータスを変更する各広告グループの横にあるチェックボックスを選択します。

   複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

1. ツールバーの「ステータス」ボタンをクリックします。
   * 行をアクティブにするには、をクリックします ![Activate](/help/search-social-commerce/assets/activate.png "Activate").

   * 行を一時停止するには、をクリックします。 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、をクリックします ![詳細](/help/search-social-commerce/assets/more.png "詳細") を選択して、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md)
>* [[!DNL Microsoft Advertising] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md)
>* [[!DNL Yahoo! Japan Ads] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)
>* [[!DNL Yandex] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md)
