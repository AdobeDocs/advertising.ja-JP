---
title: '''[!DNL Microsoft® Advertising] 広告グループ設定'
description: 次の設定を参照してください： [!DNL Microsoft® Advertising] 広告グループ。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 29401370d18a5d1c7d5c28cb90a109ea5134ac00
workflow-type: tm+mt
source-wordcount: '597'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] 広告グループ設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は 128 文字です。

**[!UICONTROL Status]:** 広告グループの表示ステータス： *アクティブ* または *一時停止*. 新しい広告グループのデフォルトはです。 *アクティブ*.

**[!UICONTROL Ad Language]:** （キャンペーン検索）広告のターゲット言語。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** （広告の検索）広告グループ内の広告を配置する方法と場所：

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* （デフォルト）：検索ネットワーク上で広告の入札を配置します。

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* シンジケートパートナーサイトに広告の入札を配置する。

* *[!UICONTROL Content network]:* 非推奨

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** 非推奨

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （オーディエンス広告グループ）次のいずれを実行するか。

* *[!UICONTROL Target and Bid]:* 広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーに対してのみ広告を表示する。

* *[!UICONTROL Bid Only]:* ターゲットオーディエンスに関連付けられていないユーザーが他の広告グループレベルのターゲットを満たしている限り、広告を表示する。 ただし、特定のオーディエンスに対して広告が表示される可能性を高めるには、それらのオーディエンスの入札額を高く設定します。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

の場合 [!DNL Microsoft® Advertising] オーディエンスネットワークの広告グループで、場所のターゲットの入札修飾子が、標準のポートフォリオで「[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;設定中です。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** （オーディエンス広告グループ、オプション）ターゲットとして含める、または除外する特定のジェンダー： *[!UICONTROL Male]*, *[!UICONTROL Female]*、および *[!UICONTROL Unknown]*. デフォルトでは、すべてのジェンダーがターゲットになります。 除外は、常に含めるものを上書きします。

* すべての値をターゲットにする場合は、値を選択しないでください。

* 値を含めるには、値の横の円を 1 回クリックして、青いチェックマーク (![次を含む](/help/search-social-commerce/assets/include.png "次を含む")) が表示されます。 オプションで、ターゲットとする性別ごとに、指定した割合で入札を増減できます。

* 値を除外するには、値の横の円を 2 回クリックして、赤いチェックマーク (![除外](/help/search-social-commerce/assets/exclude.png "除外")) が表示されます。

**[!UICONTROL Age]:** （オーディエンス広告グループ、オプション）ターゲットとして含めるまたは除外する特定の年齢カテゴリ： *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*、および *[!UICONTROL Unknown]*. デフォルトでは、すべての年齢がターゲットになっています。 除外は、常に含めるものを上書きします。

* すべての値をターゲットにする場合は、値を選択しないでください。

* 値を含めるには、値の横の円を 1 回クリックして、青いチェックマーク (![次を含む](/help/search-social-commerce/assets/include.png "次を含む")) が表示されます。 オプションで、ターゲットとする各年齢に対して、指定した割合で入札を増減できます。

* 値を除外するには、値の横の円を 2 回クリックして、赤いチェックマーク (![除外](/help/search-social-commerce/assets/exclude.png "除外")) が表示されます。

**[!UICONTROL Industry]:** （オーディエンス広告グループ、オプション）ターゲットとして含めるまたは除外する特定の業種。 デフォルトでは、すべての業界がターゲットになっています。 除外は、常に含めるものを上書きします。

* すべての値をターゲットにする場合は、値を選択しないでください。

* 値を含めるには、値の横の円を 1 回クリックして、青いチェックマーク (![次を含む](/help/search-social-commerce/assets/include.png "次を含む")) が表示されます。 オプションで、対象となる各業界に対して、指定した割合で入札を増減できます。

* 値を除外するには、値の横の円を 2 回クリックして、赤いチェックマーク (![除外](/help/search-social-commerce/assets/exclude.png "除外")) が表示されます。

**[!UICONTROL Job Function Targets]:** （オーディエンス広告グループ、オプション）ターゲットとして含めるまたは除外する特定のジョブ機能。 デフォルトでは、すべてのジョブ関数がターゲットになっています。 除外は、常に含めるものを上書きします。

* すべての値をターゲットにする場合は、値を選択しないでください。

* 値を含めるには、値の横の円を 1 回クリックして、青いチェックマーク (![次を含む](/help/search-social-commerce/assets/include.png "次を含む")) が表示されます。 オプションで、対象となる各ジョブ関数に対して、指定した割合で入札を増減できます。

* 値を除外するには、値の横の円を 2 回クリックして、赤いチェックマーク (![除外](/help/search-social-commerce/assets/exclude.png "除外")) が表示されます。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** （オプション）顧客が広告グループから広告を提供する回数。 値を入力し、時間単位 (*[!UICONTROL Hour]*, *[!UICONTROL Day]*&#x200B;または *[!UICONTROL Week]*) をクリックします。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ、オプション）広告を表示したくないディスプレイネットワーク上のサイト。 有効な URL( 例： www.example.com ) を入力します。 複数の文字列を指定するには、コンマで区切るか、複数の文字列を別々の行に入力します。

可用性について詳しくは、 [!DNL Microsoft® Advertising] 」をクリックします。[特定の Web サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0).&quot;

>[!MORELIKETHIS]
>
>* [広告グループの管理](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
