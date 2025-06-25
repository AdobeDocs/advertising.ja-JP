---
title: Manage [!DNL Google Ads] placements
description: 広告グループの入札可能なプレースメントを作成および管理する方法  [!DNL Google Ads]  ついて説明します。
exl-id: 80cb6fc6-e778-4b19-9e52-e0b57bde0d73
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 0%

---

# プレースメント [!DNL Google Ads] 管理

*[!DNL Google Ads]アカウントのみ*

[ 同期広告ネットワークアカウント内の表示ネットワークをターゲットとする [ サポートされているキャンペーンタイプ ](/help/search-social-commerce/introduction/supported-inventory.md) 広告グループのプレースメントを作成および編集 ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md) きます。

## プレースメント [!DNL Google Ads] 作成

>[!TIP]
>
>一度に多くのプレースメントを作成するには、[campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]** をクリックします。

1. 
   1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、「**[!UICONTROL Continue]**」をクリックします。

1. [ プレースメント設定 ](#placement-settings) を設定します。

1. 「**[!UICONTROL Post]**」をクリックします。

## プレースメント [!DNL Google Ads] 編集

>[!TIP]
>
>一度に多くのプレースメントを編集するには、[campaign bulksheets](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]** をクリックします。

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. データ テーブルの上にあるツールバーで、![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ") をクリックします。

1. [ プレースメント設定 ](#placement-settings) を編集します。

   複数のプレースメントの場合、変更は選択したすべてのプレースメントに適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の通貨フィールドでは、既存の値を指定の値に変更したり、制限を設けて、指定の割合または金額で金額を増減させることができます。

1. データを保存します。

   * （単一のプレースメント） **[!UICONTROL Post]** クリックします。

   * （複数のプレースメント） **[!UICONTROL Post Now]** クリックします。

## プレースメント設定 {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** 広告を表示できるコンテンツ ネットワーク上のサイト。 www.example.com、example.com、www.example.com/shoes/kidsなど、有効な URL を入力します。 複数の文字列を指定する場合は、コンマで区切るか、別の行に入力します。 URL に疑問符（`?`）を含めることはできません。 **メモ：**[!UICONTROL Placements]/[!UICONTROL Negatives] 表示、広告グループおよびキャンペーン設定から [web サイトのプレースメントを除外 ](placement-negative-create.md) できます。

**[!UICONTROL Status]:** プレースメントの表示ステータス：*アクティブ* （入札を有効にする場合）、*一時停止* （入札を無効にする場合）、*削除済み* （プレースメントを削除する場合）、既存のプレースメントのみ）。

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** （任意）プレースメントベース広告の最大クリック単価（CPC）または 1000 件あたりのビューアブルインプレッション単価（vCPM）は、キャンペーン入札戦略に応じて異なります。 この値は、広告グループレベルの入札を上書きします。

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
>* [ プレースメントについて ](placement-about.md)
>* [ ネガティブプレースメントの作成 ](placement-negative-create.md)
>* [ プレースメントとネガティブプレースメントのステータスの変更 ](placement-status-edit.md)
