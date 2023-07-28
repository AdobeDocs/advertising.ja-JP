---
title: 管理 [!DNL Google Ads] 動的検索ターゲット
description: 作成および管理方法を学ぶ [!DNL Google Ads] 動的検索ターゲット。
exl-id: 85b1455a-dda1-4bb9-b4be-d6e0a837fd9d
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 動的検索ターゲット

*[!DNL Google Ads]アカウントのみ*

検索ネットワークを使用するキャンペーンの動的検索ターゲットのステータスを作成、編集および変更できます。

>[!NOTE]
>
>一度に大量のターゲットデータを作成および編集するには、 [bulksheet ファイル](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) 広告ネットワークに投稿します。

## の作成 [!DNL Google Ads] 動的検索ターゲット

動的検索ターゲットを作成して、同じ広告グループ内の動的検索広告をターゲットにするコンテンツが使用される Web サイト（つまり、広告の表示 URL で使用されるドメイン）のページを定義できます。

すべての条件をターゲットにするか、最大 3 つの個々の条件をターゲットにすることができます。

>[!NOTE]
>
>パフォーマンスを最も高く追跡するには、[!UICONTROL All Targets]&quot;キャンペーンごとに 1 つの広告グループのみのターゲット。

>[!TIP]
>
>一度に多数のアカウントコンポーネントを作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーンおよび広告グループを選択し、 **[!UICONTROL Continue]**.

1. 次を指定します。 [動的検索ターゲット設定](#dynamic-search-target-settings).

1. クリック **[!UICONTROL Post]**.

## 編集 [!DNL Google Ads] 動的検索ターゲット設定

のステータスまたは最大入札額を編集できます [!DNL Google Ads] 動的検索ターゲット。 ターゲットとなる条件は変更できません。

>[!TIP]
>
>大量のデータを一度に編集するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. 編集する各行の横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. 次を指定します。 [動的検索ターゲット設定](#dynamic-search-target-settings).

   複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。 の [!UICONTROL Bid field]に値を追加する場合は、既存の値を指定した値に変更するか、指定した割合または金額で金額を増減（制限あり）するかを選択できます。

1. データを保存します。

   * （単一のターゲット）クリック **[!UICONTROL Post]**.

   * （複数の広告グループ）クリック **[!UICONTROL Post Now]**.

## ステータスの変更 [!DNL Google Ads] 動的検索ターゲット

サポートされるキャンペーンタイプのアクティブな動的検索ターゲットを一時停止して、同じ広告グループ内の動的検索広告に対する使用を停止できます。 後で広告のステータスをアクティブに戻すことで、ターゲットとして使用できます。

また、任意の動的ターゲットを削除することもできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Auto Targets]**.

1. （オプション）リストをフィルタリングして、特定の動的ターゲットを含めます。

1. 次のいずれかの操作を行います。

   * 1 つの動的ターゲットのステータスを変更するには、 **[!UICONTROL Status]** 列を編集して、ステータスを変更します。

   * 1 つ以上の動的ターゲットを削除するには、次の手順を実行します。

      1. 削除する各動的ターゲットの横にあるチェックボックスをオンにします。

     複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. ツールバーで、 ![その他](/help/search-social-commerce/assets/more.png "その他") を選択し、 **[!UICONTROL Delete]**.

      1. 確認メッセージで、 **[!UICONTROL Delete]**.

## [!DNL Google Ads] 動的検索ターゲット設定 {#dynamic-search-target-settings}

### [!UICONTROL Auto-Target Details]

**[!UICONTROL Auto-targets]:** ( キャンペーンの [!UICONTROL DSA Options] セクション。既存のターゲットの場合は読み取り専用 ) 広告グループの動的検索ターゲット：

* *[!UICONTROL All Targets]* （デフォルト）：インデックスで指定されたすべてのページをターゲットにします。

* *\[ 特定のターゲット\]:* インデックスで指定されたページの最大 3 つの条件をターゲットに設定します。 これを選択する場合、広告をターゲットにする情報カテゴリと特定の値（例：「URL に shoes.example.com が含まれる」）を指定して、条件を指定する必要があります。 複数の条件を指定するには、 **[!UICONTROL + And]**. ターゲット条件には次のものが含まれます。

   * *[!UICONTROL Category]:* 特定の [!DNL Google Ads] コンテンツカテゴリ。

   * *[!UICONTROL URL]:* 特定の URL を持つインデックス付きページの広告を表示する場合。URL 内の任意の場所に値を含めることができます。

   * *[!UICONTROL Page Title]:* ページタイトルに特定のテキストを含むインデックス付きページの広告を表示する。

   * *[!UICONTROL Page Content]:* 特定のコンテンツを含むインデックス付きページの広告を表示する。

**ステータス：** ターゲット設定のステータス：

* *[!UICONTROL Active]* （デフォルト）：入札を有効にします。

* *[!UICONTROL Paused]:* 入札を無効にします。

* *[!UICONTROL Deleted]* （既存のターゲットのみ）：ターゲット設定を削除します。

### [!UICONTROL Bids]

**[!UICONTROL Bid]:** 広告の最大クリック単価 (CPC) または広告の 1,000 インプレッションあたりのコスト (CPM)。広告ネットワークとキャンペーンの価格モデルで使用できます。 この値は、広告グループレベルの値よりも優先されます。

>[!NOTE]
>
>ターゲットが最適化されたポートフォリオにある場合、指定された CPC 入札が 1 日に適用されます。 その後、最適化機能によって、入札は独自の計算に従って配置されます。

>[!MORELIKETHIS]
>
>* [について [!DNL Google Ads] 動的検索ターゲット](dynamic-search-target-about.md)
