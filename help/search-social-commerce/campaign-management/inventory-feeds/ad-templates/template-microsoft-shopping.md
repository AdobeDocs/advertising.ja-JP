---
title: '在庫フィードの買い物かご広告テンプレート設定を [!DNL Microsoft Ads] 定'
description: 在庫フィードの買い物  [!DNL Microsoft Ads]  広告テンプレートの設定を参照します。
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '498'
ht-degree: 0%

---

# 在庫フィードの買い物かごへのテンプレート設定の [!DNL Microsoft Ads] 定

ショッピング広告テンプレートを使用すると、ショッピング広告を設定できます。

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名を指定するために予約されているので、すべての属性フィールドでテキストとして使用することはできません。`[ ] < > `


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

**[!UICONTROL Campaign Tracking Template]:** （クライアントフィードファイルのテンプレートではオプション）キャンペーンレベルのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL をパラメーターに埋め込みます。 この値はアカウントレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレート（キーワードを最も詳細なレベルとして）はこの値を上書きします。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingのコンバージョントラッキングの場合は、次のいずれかを行います。

   * （推奨） [Microsoft ショッピングキャンペーン用のトラッキングテンプレートフォーマット ](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md) を使用します。 アカウント全体がショッピング広告専用の場合は、代わりにアカウントレベルでトラッキングテンプレートを定義できます。

   * 代わりに、「[!DNL bingads_redirect]」列を使用してフィードに各製品の値を含める場合（[ 正しい形式 ](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)）は、パラメーター `{lpurl}` を入力します。 オプションで、`{lpurl}` パラメーターへのサードパーティリダイレクトおよびトラッキングを追加できます。

* サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:** 商品がキャンペーンに使用されるマーチャントアカウントの顧客 ID。

**[!UICONTROL Sales Country]:** キャンペーンの商品が販売される国。 製品は関連付けられているためです
ターゲット国では、この設定によって、キャンペーンで広告する製品が決まります。

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

**[!UICONTROL Campaign Priority]:** 複数のキャンペーンで広告が行われる場合に、キャンペーンが使用される優先度
同じ製品：*[!UICONTROL Low]* （新規キャンペーンのデフォルト）、*[!UICONTROL Medium]* または *[!UICONTROL High]*。 同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークはを使用します
最初にキャンペーンの優先度を指定して、広告オークションに適格なキャンペーン（および関連入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （任意）広告グループレベルのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL をパラメーターに埋め込みます。 この値はアカウントレベルおよびキャンペーンレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレートはこの値を上書きします。

Adobe Advertisingコンバージョントラッキングの場合は、値を入力する必要はありません。 キャンペーンレベルの値で十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** デフォルトの全てを含む製品グループ「[!UICONTROL All products]」 この親製品グループは削除できませんが、下位のすべての層がフィードにない場合は自動的に削除されます。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** （子製品グループを持たない単位。オプション）製品の追跡テンプレート
すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的な URL を [!DNL ValueTrack] パラメーターに埋め込むグループ。 このテンプレートは、上位レベルのテンプレートを上書きします。

Adobe Advertisingコンバージョントラッキングの場合は、値を入力する必要はありません。 キャンペーンレベルの値で十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

**[!UICONTROL Initial Bid]:** 各広告の初期入札額。

## [!UICONTROL Feed Filters]

<!-- **\[Feed Filter\]:** -->

{{$include /help/_includes/inventory-feed-template-feed-filter.md}}

## [!UICONTROL Label Classifications]

<!-- **\[Component\] [!UICONTROL Label Classifications] &gt; `[Label Classification and Value`]:** -->

{{$include /help/_includes/inventory-feed-template-label-classifications.md}}

>[!MORELIKETHIS]
>
>* [ 在庫フィードを使用した広告管理の自動化について ](../inventory-feeds-about.md)
>* [ 修飾子の管理 ](../modifiers-manage.md)
>* [ 在庫データフィードファイルの管理 ](/help/search-social-commerce/campaign-management/inventory-feeds/feed-files-manage.md)
>* [ テンプレートを使用したフィードデータの伝播 ](../feed-data-propagate.md)
>* [ 在庫フィードから広告ネットワークへのキャンペーンデータの投稿 ](../propagated-data-post.md)
