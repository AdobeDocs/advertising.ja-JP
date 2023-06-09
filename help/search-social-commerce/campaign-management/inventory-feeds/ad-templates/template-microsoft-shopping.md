---
title: '"[!DNL Microsoft® Ads] 在庫フィード用のショッピング広告テンプレート設定»'
description: 次の設定を参照してください： [!DNL Microsoft® Ads] 在庫フィード用の買い物広告テンプレート。
source-git-commit: f8d17ba787496917f4011f9dcbcb5587fe5c83cb
workflow-type: tm+mt
source-wordcount: '499'
ht-degree: 0%

---

# [!DNL Microsoft® Ads] 在庫フィード用の買い物広告テンプレート設定

ショッピング広告テンプレートを使用して、ショッピング広告を設定します。

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名の指定用に予約されているため、すべての属性フィールドのテキストとして使用することはできません。  `[ ] < > `


## \[ すべてのタブの上\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[ 左パネル\]

<!-- **[!UICONTROL Feed &amp; Columns]:** -->

{{$include /help/_includes/inventory-feed-template-feed-and-columns.md}}

<!-- **[!UICONTROL Modifiers]:** -->

{{$include /help/_includes/inventory-feed-template-modifiers.md}}

## [!UICONTROL Campaigns]

<!-- **[!UICONTROL Campaign]:** -->

{{$include /help/_includes/inventory-feed-template-campaign.md}}

<!-- **[!UICONTROL Campaign Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-only.md}}

<!-- **[!UICONTROL Campaign Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-shopping-campaign-map-method.md}}

**[!UICONTROL Campaign Tracking Template]:** （クライアントフィードファイルのテンプレートのオプション）キャンペーンレベルのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終 URL をパラメーターに埋め込みます。 この値はアカウントレベルの設定より優先されますが、より詳細なレベル（最も詳細なキーワードを含む）でのトラッキングテンプレートは、この値よりも優先されます。

* Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、&quot;次のいずれかを実行します&quot;:

   * （推奨） [Microsoft®ショッピングキャンペーン用のトラッキングテンプレート形式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md). アカウント全体がショッピング広告専用の場合は、代わりにアカウントレベルでトラッキングテンプレートを定義できます。

   * 代わりに、「[!DNL bingads_redirect]&quot;列 ( [正しい形式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)) をクリックして、パラメーターを入力します `{lpurl}`. オプションで、サードパーティのリダイレクトとトラッキングを `{lpurl}` パラメーター。

* サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** 製品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。

**[!UICONTROL Sales Country]:** キャンペーンの製品が販売される国。 製品は対象国に関連付けられているので、この設定によってキャンペーンで広告される製品が決まります。

<!-- **[!UICONTROL Stock Level]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-stock-level.md}}

<!-- **[!UICONTROL This column has non-numeric values]:** -->

{{$include /help/_includes/inventory-feed-template-nonnumeric-values.md}}

### [!UICONTROL Campaign Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-campaign-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Campaigns]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Campaigns]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-manage-settings-new-campaigns.md}}

<!-- **[!UICONTROL Initial Budget]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-initial-budget.md}}

**[!UICONTROL Campaign Priority]:** 複数のキャンペーンが同じ製品を宣伝する場合に使用されるキャンペーンの優先度： *[!UICONTROL Low]* （新しいキャンペーンのデフォルト） *[!UICONTROL Medium]*&#x200B;または *[!UICONTROL High]*. 同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークは、まずキャンペーンの優先順位を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが実施要件を満たします。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL をパラメーターに埋め込む広告グループレベルのトラッキングテンプレート。 この値は、アカウントレベルとキャンペーンレベルの設定よりも優先されますが、より詳細なレベルでのトラッキングテンプレートは、この値よりも優先されます。

Adobe広告コンバージョントラッキングの場合、値を入力する必要はありません。 キャンペーンレベルの値で十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** デフォルトの包括的な製品グループ「[!UICONTROL All products].&quot; この親製品グループは削除できませんが、すべての下位層がフィードにない場合、自動的に削除されます。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** ( 子製品グループのない数量。（オプション）製品グループのトラッキングテンプレートです。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、ValueTrack パラメーターに最終的な URL を埋め込みます。 このテンプレートは、上位レベルのテンプレートを上書きします。

Adobe広告コンバージョントラッキングの場合、値を入力する必要はありません。 キャンペーンレベルの値で十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

**[!UICONTROL Initial Bid]:** 各広告の初期入札。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [在庫フィードを使用した広告管理の自動化について](../inventory-feeds-about.md)
>* [修飾子の管理](../modifiers-manage.md)
>* [在庫データフィードファイルの管理](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [テンプレートを通じてフィードデータを伝達](../feed-data-propagate.md)
>* [在庫フィードから広告ネットワークへのキャンペーンデータの投稿](../propagated-data-post.md)
