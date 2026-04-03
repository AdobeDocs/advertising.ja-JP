---
title: 在庫フィードのショッピングとテンプレート設定[!DNL Microsoft Ads]
description: 在庫フィードの [!DNL Microsoft Ads]  ショッピング広告テンプレートの設定を参照します。
exl-id: a0dd6542-0516-406a-b8c5-2e102ec7ab3d
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/Q-TmSKd7yk8Infwx-Nyar61Bu-oqK8NUd2qgJbAOTDA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: f8667931-f646-4dd3-af2a-b9d0cb8098ad
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 535
ht-degree: 0%

---

# 在庫フィードのショッピングとテンプレート設定[!DNL Microsoft Ads]

ショッピング広告テンプレートを使用したショッピング広告の設定。

>[!NOTE]
>
>* 次の文字は、テンプレート内の列名と修飾子名を指定するために予約されているため、すべての属性フィールドのテキストとして使用できません：`[ ] < > `

## \[すべてのタブの上\]

<!-- **Template Name:** -->

{{$include /help/_includes/inventory-feed-template-name.md}}

<!-- **Status:** -->

{{$include /help/_includes/inventory-feed-template-status.md}}

<!-- **Account:** -->

{{$include /help/_includes/inventory-feed-template-account.md}}

## \[左パネル\]

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

**[!UICONTROL Campaign Tracking Template]:** （クライアントフィードファイルのテンプレートの場合はオプション） キャンペーンレベルのトラッキングテンプレート。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLをパラメーターに埋め込みます。 この値はアカウントレベルの設定よりも優先されますが、より詳細なレベル（キーワードが最も詳細なレベル）でテンプレートを追跡すると、この値よりも優先されます。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合は、次のいずれかの操作を行います。

   * （推奨）Microsoft ショッピングキャンペーンに[ トラッキングテンプレート形式を使用](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)。 アカウント全体がショッピング広告専用の場合は、代わりにアカウントレベルでトラッキングテンプレートを定義できます。

   * 代わりに、「[!DNL bingads_redirect]」列（[正しい形式](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)を使用）を使用してフィードに各製品の値を含める場合は、パラメーター`{lpurl}`を入力します。 オプションで、サードパーティのリダイレクトとトラッキングを`{lpurl}` パラメーターに追加できます。

* サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

<!-- **[!UICONTROL Campaign Final URL Suffix]:** -->

{{$include /help/_includes/final-url-suffix.md}}

**[!UICONTROL Merchant ID]:**&#x200B;製品がキャンペーンに使用されているマーチャント アカウントの顧客ID。

**[!UICONTROL Sales Country]:** キャンペーンの製品が販売される国。 製品が関連付けられているため
ターゲット国では、この設定により、キャンペーンで宣伝される製品が決まります。

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

**[!UICONTROL Campaign Priority]:**複数のキャンペーンが次のキャンペーンを宣伝する場合にキャンペーンが使用される優先度
同じ製品：*[!UICONTROL Low]* （新しいキャンペーンのデフォルト）、*[!UICONTROL Medium]*、または&#x200B;*[!UICONTROL High]*。 同じ商品が複数のキャンペーンに含まれる場合、広告ネットワークは
最初にキャンペーンの優先順位を指定して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを決定します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。

<!-- **[!UICONTROL Locations]:** -->

{{$include /help/_includes/inventory-feed-template-campaign-locations.md}}

**[!UICONTROL Has EU Political Ads]:** （[!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンのみ。欧州連合（EU）内のオーディエンスをターゲットとするキャンペーンに適用されます）このキャンペーンに、EU規則2024/90に基づいて欧州連合で配信される広告の要件に従った政治的広告が含まれているかどうか：*[!UICONTROL Yes]*&#x200B;または&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Ad Groups]

<!-- **[!UICONTROL Ad Group]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group.md}}

<!-- **[!UICONTROL Map Only]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-only.md}}

<!-- **[!UICONTROL Map Method]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-map-method.md }}

**[!UICONTROL Ad Group Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLをパラメーターに埋め込む、広告グループレベルのトラッキングテンプレート。 この値は、アカウントレベルとキャンペーンレベルの設定を上書きしますが、より詳細なレベルでのトラッキングテンプレートはこの値を上書きします。

Adobe Advertisingのコンバージョントラッキングでは、値を入力する必要はありません。 キャンペーンレベルの価値だけで十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

### [!UICONTROL Ad Group Level Negative Keywords]

{{$include /help/_includes/inventory-feed-template-ad-group-negative-keywords.md}}

### [!UICONTROL Manage Settings for NEW Ad Groups]

<!-- Flag/check box **[!UICONTROL Manage Settings for NEW Ad Groups]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-manage-settings-new-ad-groups.md}}

<!-- **[!UICONTROL Languages]:** -->

{{$include /help/_includes/inventory-feed-template-ad-group-language-microsoft.md}}

## [!UICONTROL Product Groups]

**[!UICONTROL Tier 1]:** デフォルトの包括的な製品グループ「[!UICONTROL All products]」。 この親製品グループを削除することはできませんが、フィードに下位の階層がすべて欠落している場合は、自動的に削除されます。

<!-- **[!UICONTROL Tier 2 - Tier 8]:** -->

{{$include /help/_includes/inventory-feed-template-tier2-8.md}}

<!-- **[!UICONTROL Row Level Value]:** -->

{{$include /help/_includes/inventory-feed-template-row-level-value.md}}

**[!UICONTROL Tracking Template]:** （子の製品グループのないユニット、オプション）製品のトラッキングテンプレート
すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLを[!DNL ValueTrack] パラメーターに埋め込むグループ。 このテンプレートは、より高いレベルのテンプレートを上書きします。

Adobe Advertisingのコンバージョントラッキングでは、値を入力する必要はありません。 キャンペーンレベルの価値だけで十分です。

サードパーティのリダイレクトとトラッキングの場合は、値を入力します。

**[!UICONTROL Initial Bid]:**&#x200B;各広告の初回入札。

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
>* [ テンプレートを通じてフィード データを伝達](../feed-data-propagate.md)
>* [在庫フィードのキャンペーンデータを広告ネットワークに投稿](../propagated-data-post.md)
