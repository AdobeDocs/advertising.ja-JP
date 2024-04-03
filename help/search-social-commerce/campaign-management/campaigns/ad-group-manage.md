---
title: 広告グループの管理
description: 広告グループを作成および管理する方法について説明します。
exl-id: 66900a1f-f915-497d-9053-9d393845af08
feature: Search Campaign Management
source-git-commit: 3f9380076389d00c87efbcdbbb2112352cbe173c
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 広告グループの管理

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]、および既存 [!DNL Baidu] アカウントのみ*

広告グループには、一連の広告とその関連キーワードが含まれます。 ディスプレイネットワークをターゲットにするキャンペーンの広告グループには、プレースメント（ディスプレイネットワーク上で広告を表示できる場所）を含めることもできます。 広告グループ設定は、広告グループのすべてのコンポーネントに適用され、広告ネットワークによって異なります。

検索、ソーシャル、コマース内から、 [サポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md) 内 [同期済み広告ネットワークアカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md). また、広告グループのステータスを編集および変更することもできます。

## 広告グループの作成

>[!TIP]
>
>一度に大量の広告グループデータを追加するには、 [コピーおよび貼り付け機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーンを選択し、 **[!UICONTROL Continue]**.

1. 次を入力します。 [Baidu](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md), [Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)または [Yandex](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md) 広告グループの設定。

   広告ネットワークに応じて、設定は次のようにグループ化されます。 [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]. の設定を構成するには [!UICONTROL Adgroup Frequency Cap Settings], [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites]を使用できる場合は、「 **[!UICONTROL Add Frequency Cap Settings]**, **[!UICONTROL Add Negative Keywords]**&#x200B;または **[!UICONTROL Add Negative Websites]**、それぞれ。

1. クリック **[!UICONTROL Post]**.

後で、広告グループ内の個々のキーワードまたはプレースメントに入札を設定することで、広告グループレベルの入札をオプションで上書きできます。

## 広告グループ設定の編集

個々の広告グループの設定を編集できます。 また、選択したすべてのキャンペーンに共通する一部の広告グループの詳細、予算オプション、URL オプションなど、複数の広告グループの一部のフィールドを一度に編集することもできます。

>[!TIP]
>
>大量のデータを一度に編集するには、 [コピーおよび貼り付け機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. 次のいずれかの操作を行います。

   1. （単一の広告グループの設定を編集するには）エンティティ名の上にカーソルを置いたまま、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Edit]**.

   1. （1 つ以上の広告グループの設定を編集するには）次の操作を行います。

      * 各広告グループの横にあるチェックボックスを選択します。

        複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [Baidu](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md), [Microsoft® Advertising](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)または [Yandex](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md) 広告グループの設定。

   複数の広告グループの場合、設定は [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]（広告ネットワークに応じて） 選択したすべての広告グループに共通するフィールドのみを編集でき、変更は選択したすべての広告グループに適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の金額フィールドでは、既存の値を指定した値に変更するか、指定した割合または金額で金額を上限に従って増減するかを選択できます。

   単一の広告グループの場合、設定は [!UICONTROL Ad Group Details], [!UICONTROL Budget Options], [!UICONTROL Ad Group Targeting]、および [!UICONTROL URL Options]. の設定を構成するには [!UICONTROL Negative Keywords] または [!UICONTROL Negative Websites]を使用できる場合は、「 **[!UICONTROL Add Negative Keywords]** または **[!UICONTROL Add Negative Websites]**、それぞれ。

1. データを保存します。

   * （単一の広告グループ）クリック **[!UICONTROL Post]**.

   * （複数の広告グループ）クリック **[!UICONTROL Post Now]**.

## 広告グループのステータスの変更

任意のアクティブな検索広告グループを一時停止して、その広告グループに対する入札を無効にできます。 ステータスを「アクティブ」に戻すと、後で入札を再開できます。

また、アクティブな検索広告グループや一時停止した検索広告グループも削除できます。 削除された広告グループは広告ネットワークから削除されます。 まだ表示されますが、変更することはできません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ad Groups]**.

1. （オプション）リストをフィルタリングして、特定の広告グループを含めます。

1. ステータスを変更する各広告グループの横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. ツールバーで、ステータスボタンをクリックします。
   * 行をアクティブにするには、 ![有効化](/help/search-social-commerce/assets/activate.png "有効化").

   * 行を一時停止するには、 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、 ![その他](/help/search-social-commerce/assets/more.png "その他") を選択し、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [[!DNL Baidu] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-baidu.md)
>* [[!DNL Google Ads] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-google.md)
>* [[!DNL Microsoft® Advertising] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-microsoft.md)
>* [[!DNL Yahoo! Japan Ads] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yahoo-japan.md)
>* [[!DNL Yandex] 広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-settings-yandex.md)
