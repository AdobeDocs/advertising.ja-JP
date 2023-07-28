---
title: キャンペーンの管理
description: 広告キャンペーンの作成および管理方法について説明します。
exl-id: 9406e4bd-d5a2-4744-ab71-fc52428e3af6
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '751'
ht-degree: 0%

---

# キャンペーンの管理

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]、および [!DNL Yandex] アカウントのみ*

キャンペーンは、広告ネットワークアカウントの主要なコンポーネントです。 ほとんどのキャンペーンタイプでは、一連の広告グループまたは広告セットで構成されます。 キャンペーン設定には、キャンペーン予算パラメーター、広告ターゲット、キャンペーン内のすべての広告のオプションのトラッキングパラメーターが含まれます。 キャンペーンレベルのトラッキングパラメーターは、アカウントレベルのパラメーターより優先されますが、それ自体は低いレベルで上書きされる場合があります。

一度 [広告ネットワークアカウントをアクセス可能にする](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) 検索、ソーシャル、コマースがアカウントデータを広告ネットワークと同期しました。 [サポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md). また、キャンペーンのステータスを編集および変更することもできます。

## キャンペーンの作成

>[!NOTE]
>
>* キャンペーンを作成する前に、 [コンバージョントラッキングタグの実装](/help/search-social-commerce/tracking/conversion-tracking-about.md) 広告主の Web ページ内に表示されます。
>* 一度に多数のキャンペーンを作成するには、 [コピーおよび貼り付け機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、およびキャンペーンのタイプを選択し、 **[!UICONTROL Continue]**.

   各キャンペーンタイプについて詳しくは、 [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)または [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) キャンペーンの設定。

1. 次を入力します。 [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)または [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) キャンペーンの設定。

   広告ネットワークに応じて、設定は次のようにグループ化されます。 [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Shopping Settings], [!UICONTROL Campaign Targeting], [!UICONTROL Conversion Goals], [!UICONTROL Advanced Device Options], [!UICONTROL URL Options]、および [!UICONTROL (Google) DSA Options]. の設定を構成するには [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites], [!UICONTROL Campaign Tracking]または [!UICONTROL Asset Groups] （利用可能な場合）、 **[!UICONTROL Add Negative Keywords]**, **[!UICONTROL Add Negative Websites]**, **[!UICONTROL Set Campaign Tracking]**, **[!UICONTROL Set Campaign Goals]**&#x200B;または **[!UICONTROL Manage Asset Groups]**、それぞれ。

1. クリック **[!UICONTROL Post]**.

キャンペーンが作成された広告ネットワークに応じて、キャンペーンが広告ネットワークにプッシュされる前に、関連する広告グループと広告を作成する必要が生じる場合があります。

## キャンペーン設定を編集

個々のキャンペーンの設定を編集できます。 また、選択したすべてのキャンペーンに共通するキャンペーンの詳細、予算オプション、URL オプションなど、複数のキャンペーンのフィールドを一度に編集することもできます。

>[!TIP]
>
>コピー&amp;ペースト機能またはキャンペーン一括送信シートを使用して、データを一括編集することもできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. 次のいずれかの操作を行います。

   1. （1 つのキャンペーンの設定を編集する場合）エンティティ名の上にカーソルを置いたまま、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Edit]**.

   1. （1 つ以上のキャンペーンの設定を編集するには）次の操作を行います。

      * 各キャンペーンの横にあるチェックボックスをオンにします。

        複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      * データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [Baidu](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md), [Google Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md), [Microsoft Advertising](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md), [Yahoo! Japan Ads](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)または [Yandex](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md) キャンペーンの設定。

   複数のキャンペーンの場合、設定は [!UICONTROL Campaign Details], [!UICONTROL Budget Options]、および [!UICONTROL URL Options]（広告ネットワークに応じて）。 選択したすべてのキャンペーンに共通するフィールドのみを編集でき、選択したすべてのキャンペーンに変更が適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の金額フィールドでは、既存の値を指定した値に変更するか、指定した割合または金額で金額を上限に従って増減するかを選択できます。

   単一のキャンペーンの場合、設定は [!UICONTROL Campaign Details], [!UICONTROL Budget Options], [!UICONTROL Shopping Settings], [!UICONTROL Campaign Targeting], [!UICONTROL Conversion Goals], [!UICONTROL Advanced Device Options], [!UICONTROL URL Options]、および [!UICONTROL (Google) DSA Options]. の設定を構成するには [!UICONTROL Negative Keywords], [!UICONTROL Negative Websites], [!UICONTROL Campaign Tracking]または [!UICONTROL Asset Groups] （利用可能な場合）、 **[!UICONTROL Add Negative Keywords]**, **[!UICONTROL Add Negative Websites]**, **[!UICONTROL Set Campaign Tracking]**, **[!UICONTROL Set Campaign Goals]**&#x200B;または **[!UICONTROL Manage Asset Groups]**、それぞれ。

1. データを保存します。

   * （単一キャンペーン）クリック **[!UICONTROL Post]**.

   * （複数のキャンペーン）クリック **[!UICONTROL Post Now]**.

キャンペーンが作成された広告ネットワークによっては、広告が広告ネットワークにプッシュされる前に、キャンペーンに広告グループと広告が含まれる必要が生じる場合があります。

## キャンペーンのステータスの変更

サポートされている広告ネットワーク上の任意のアクティブな検索キャンペーンを一時停止して、そのキャンペーンでの入札を無効にすることができます。 ステータスを「アクティブ」に戻すと、後で入札を再開できます。

アクティブまたは一時停止した任意の検索キャンペーンも削除できます。 削除されたキャンペーンは広告ネットワークから削除されます。 データフィルターに含めると、これらは引き続き表示されますが、変更することはできません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

1. （オプション）リストをフィルタリングして、特定のキャンペーンを含めます。

1. ステータスを変更する各キャンペーンの横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. ツールバーで、ステータスボタンをクリックします。

   * 行をアクティブにするには、 ![有効化](/help/search-social-commerce/assets/activate.png "有効化").

   * 行を一時停止するには、 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、 ![その他](/help/search-social-commerce/assets/more.png "その他") を選択し、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [Baidu キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-baidu.md)
>* [Google Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [Microsoft Advertising キャンペーンの設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
>* [Yahoo! Japan Ads キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yahoo-japan.md)
>* [Yandex キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-yandex.md)
