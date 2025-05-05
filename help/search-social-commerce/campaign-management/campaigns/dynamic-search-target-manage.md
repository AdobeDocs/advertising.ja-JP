---
title: 動的検索タ  [!DNL Google Ads]  ゲットの管理
description: 動的検索ターゲットを作成および管理する方法  [!DNL Google Ads]  ついて説明します。
exl-id: 5ea68cab-677f-4c7e-8776-24d6546f0b15
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# 動的検索タ [!DNL Google Ads] ゲットの管理

*[!DNL Google Ads]アカウントのみ*

検索ネットワークを使用するキャンペーンの動的検索ターゲットのステータスを作成、編集および変更できます。

>[!NOTE]
>
>[ バルクシート ファイル ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) をアップロードして広告ネットワークに投稿することで、大量のターゲットデータを一度に作成および編集できます。

## [!DNL Google Ads] の動的検索ターゲットの作成

動的検索ターゲットを作成して、同じ広告グループ内の動的検索広告をターゲットするためにコンテンツが使用される web サイトのページ（つまり、広告のディスプレイ URL で使用されるドメイン）を定義できます。

すべての条件、または最大 3 つの個別の条件をターゲットにすることができます。

>[!NOTE]
>
>パフォーマンスを最適に追跡するには、キャンペーンあたり 1 つの広告グループに対してのみ「[!UICONTROL All Targets]」ターゲットを作成します。

>[!TIP]
>
>一度に多くのアカウントコンポーネントを作成するには、[campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Auto Targets]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループを選択し、「**[!UICONTROL Continue]**」をクリックします。

1. [ 動的検索ターゲット設定 ](#dynamic-search-target-settings) を指定します。

1. 「**[!UICONTROL Post]**」をクリックします。

## 動的検索ターゲット設定 [!DNL Google Ads] 編集

[!DNL Google Ads] の動的検索ターゲットのステータスまたは最大入札額を編集できます。 対象となる条件は変更できません。

>[!TIP]
>
>一度に大量のデータを編集するには、[campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Auto Targets]** をクリックします。

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. [ 動的検索ターゲット設定 ](#dynamic-search-target-settings) を指定します。

   複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。 [!UICONTROL Bid field] の場合は、既存の値を指定の値に変更するか、制限を設けて、指定の割合または金額で金額を増減するオプションがあります。

1. データを保存します。

   * （単一ターゲット） **[!UICONTROL Post]** をクリックします。

   * （複数の広告グループ）「**[!UICONTROL Post Now]**」をクリックします。

## 動的検索ターゲット [!DNL Google Ads] ステータスの変更

サポートされているキャンペーンタイプでアクティブな動的検索ターゲットを一時停止して、同じ広告グループ内の動的検索広告に対するアクティブな動的検索ターゲットの使用を停止できます。 後で広告のステータスをアクティブに戻すことで、これらをターゲットとして使用できます。

また、任意の動的ターゲットを削除することもできます。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Auto Targets]** をクリックします。

1. （任意）特定の動的ターゲットを含めるようにリストをフィルタリングします。

1. 次のいずれかの操作をおこないます。

   * 1 つの動的ターゲットのステータスを変更するには、**[!UICONTROL Status]** 列内をクリックしてステータスを変更します。

   * 1 つ以上の動的ターゲットを削除するには、次の手順を実行します。

      1. 削除する各動的ターゲットの横にあるチェックボックスをオンにします。

     複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. ツールバーの ![ その他 ") をクリックし ] (/help/search-social-commerce/assets/more.png " 選択 **[!UICONTROL Delete]** ます。

      1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

## 動的検索のターゲット設定の [!DNL Google Ads] 定 {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** （キャンペーンの「[!UICONTROL DSA Options]」セクションで web サイトのドメインと言語を指定しない場合に必要。既存のターゲットの場合は読み取り専用）広告グループの動的検索ターゲット：

* *[!UICONTROL All Targets]* （デフォルト）：すべてのインデックス付きページをターゲットにします。

* *\[Specific Targets\]:* インデックス付きページに対して最大 3 つの条件をターゲットにします。 これを選択する場合は、広告のターゲットとなる情報カテゴリと特定の値を指定して条件を指定する必要があります（「URL contains shoes.example.com」など）。 複数の条件を指定するには、[**[!UICONTROL + And]**] をクリックします。 ターゲット条件は次のとおりです。

   * *[!UICONTROL Category]:* 特定の [!DNL Google Ads] コンテンツカテゴリでインデックス付けされたページの広告を表示します。

   * *[!UICONTROL URL]:* 特定の URL を持つインデックス付きページの広告を表示します。この場合、値は URL 内の任意の場所に含めることができます。

   * *[!UICONTROL Page Title]:* ページタイトルに特定のテキストを含む、インデックス付きのページの広告を表示します。

   * *[!UICONTROL Page Content]:* 特定のコンテンツを含むインデックス付きページの広告を表示します。

**ステータス：** ターゲット設定のステータス：

* *[!UICONTROL Active]* （デフォルト）：入札を有効にします。

* *[!UICONTROL Paused]:* 入札を無効にします。

* *[!UICONTROL Deleted]* （既存のターゲットのみ）：ターゲット設定を削除します。

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** 広告の最大クリック単価（CPC）または広告の 1000 インプレッション単価（CPM）は、広告ネットワークおよびキャンペーン価格モデルの場合に適用されます。 この値は、広告グループレベルの値を上書きします。

>[!NOTE]
>
>ターゲットが最適化されたポートフォリオ内にある場合、指定された CPC 入札は 1 日適用されます。 その後、最適化機能は独自の計算に従って入札を行います。

>[!MORELIKETHIS]
>
>* [ 動的検索ターゲット  [!DNL Google Ads]  ついて ](dynamic-search-target-about.md)
