---
title: 管理 [!DNL Google Ads] 配置
description: の入札可能な配置の作成および管理方法を説明します。 [!DNL Google Ads] 広告グループ。
source-git-commit: a24b51405bef1e73ed57b1cb9d012bdfbda9cdec
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 配置

*[!DNL Google Ads]アカウントのみ*

で広告グループのプレースメントを作成および編集できます [サポートされるキャンペーンタイプ](/help/search-social-commerce/introduction/supported-inventory.md) が [同期済み広告ネットワークアカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-about.md)

## 作成 [!DNL Google Ads] 配置

>[!TIP]
>
>一度に多数の配置を作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Placements] >[!UICONTROL Placements]**.

1. 
   1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーンおよび広告グループを選択し、 **[!UICONTROL Continue]**.

1. の設定 [配置設定](#placement-settings).

1. クリック **[!UICONTROL Post]**.

## 編集 [!DNL Google Ads] 配置

>[!TIP]
>
>複数の配置を一度に編集するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Keywords]**.

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集") .

1. を編集します。 [配置設定](#placement-settings).

   複数の配置の場合、変更は選択したすべての配置に適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の金額フィールドでは、既存の値を指定した値に変更するか、制限を持つ指定した割合または金額で金額を増減させることができます。

1. データを保存します。

   * （単一の配置）クリック **[!UICONTROL Post]**.

   * （複数の配置）クリック **[!UICONTROL Post Now]**.

## 配置設定 {#placement-settings}

### [!UICONTROL Placement Details]

**[!UICONTROL Placements]:** 広告を表示できるコンテンツネットワーク上のサイト。 有効な URL(www.example.com、example.com、www.example.com/shoes/kidsなど ) を入力します。 複数の文字列を指定するには、コンマで区切るか、複数の文字列を別々の行に入力します。 URL に疑問符 (`?`) をクリックします。 **注意：** 以下が可能です。 [web サイト配置の除外](placement-negative-create.md) から [!UICONTROL Placements] > [!UICONTROL Negatives] 広告グループとキャンペーンの設定で「 」と「 」を表示します。

**[!UICONTROL Status]:** 配置の表示ステータス： *アクティブ* （入札を有効にする）。デフォルト )、 *一時停止* （入札を無効にする）、または *削除済み* （配置を削除する場合）既存の配置のみ )。

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** （オプション）プレースメントベースの広告のクリック単価 (CPC) またはビューアブルインプレッション数 1,000 回あたりの最大コスト (vCPM)。キャンペーン入札戦略に応じて異なります。 この値は、広告グループレベルの入札を上書きします。

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
>* [配置について](placement-about.md)
>* [ネガティブな配置の作成](placement-negative-create.md)
>* [配置と負の配置のステータスの変更](placement-status-edit.md)
