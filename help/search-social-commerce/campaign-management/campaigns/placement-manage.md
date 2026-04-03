---
title: ' [!DNL Google Ads]  プレースメントを管理'
description: ' [!DNL Google Ads] 広告グループの入札可能なプレースメントを作成および管理する方法について説明します。'
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/rvRv9LNnt-HX4u3hCsdhqbcl3XdNRvhLCqlVrX-tbm8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 367
ht-degree: 0%

---

# [!DNL Google Ads]件のプレースメントを管理

*[!DNL Google Ads]アカウントのみ*

[同期広告ネットワークアカウント &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)内の表示ネットワークをターゲットとする[&#x200B; サポートされているキャンペーンタイプ &#x200B;](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)の広告グループのプレースメントを作成および編集できます

## [!DNL Google Ads]個のプレースメントを作成

>[!TIP]
>
>一度に多くのプレースメントを作成するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**&#x200B;をクリックします。

1. &#x200B;
   1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. [&#x200B; プレースメント設定](#placement-settings)を構成します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## [!DNL Google Ads]件のプレースメントを編集

>[!TIP]
>
>一度に多くのプレースメントを編集するには、[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**&#x200B;をクリックします。

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. [&#x200B; プレースメント設定](#placement-settings)を編集します。

   複数のプレースメントの場合、変更は選択したすべてのプレースメントに適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、指定した接頭辞を各値の先頭に追加したり、各値の末尾に接尾辞を追加したりできます。 一部の金銭的なフィールドでは、既存の値を指定した値に変更したり、指定した割合または金額を増減したり、制限を設けることができます。

1. データを保存します。

   * （1つのプレースメント）「**[!UICONTROL Post]**」をクリックします。

   * （複数のプレースメント）「**[!UICONTROL Post Now]**」をクリックします。

## 配置の設定 {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:**：広告を表示できるコンテンツネットワーク上のサイト。 www.example.com、example.com、www.example.com/shoes/kidsなどの有効なURLを入力します。 複数の文字列を指定するには、それらをコンマで区切るか、別々の行に入力します。 URLに疑問符（`?`）を含めることはできません。 **メモ：** Web サイトのプレースメント [を](placement-negative-create.md) > [!UICONTROL Placements] ビューから除外し、広告グループおよびキャンペーン設定で除外できます。[!UICONTROL Negatives]

**[!UICONTROL Status]:** プレースメントの表示ステータス：*アクティブ* （入札を有効にする場合、デフォルト）、*一時停止* （入札を無効にする場合）、または&#x200B;*削除* （プレースメントを削除する場合、既存のプレースメントのみ）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** （オプション） キャンペーン入札戦略に応じて、プレースメントベースの広告のクリック単価（CPC）または表示可能インプレッション数（vCPM）の千単位あたりのコストを指定します。 この値は、広告グループレベルの入札を上書きします。

<!-- If the placement is in a standard optimized portfolio, then the specified bid is applied for one day. Afterward, the optimization capability places bids according to its own calculations. -->

### [!UICONTROL Tracking URLs]

<!-- **[!UICONTROL Base URL]:** -->

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

<!-- note -->

{{$include /help/_includes/base-url-google-note.md}}

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

>[!MORELIKETHIS]
>
>* [&#x200B; プレースメントについて](placement-about.md)
>* [負のプレースメントを作成](placement-negative-create.md)
>* [&#x200B; プレースメントとネガティブプレースメントのステータスを変更](placement-status-edit.md)
