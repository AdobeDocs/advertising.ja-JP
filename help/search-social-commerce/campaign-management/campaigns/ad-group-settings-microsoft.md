---
title: '''[!DNL Microsoft® Advertising] 広告グループ設定'
description: の設定を参照します [!DNL Microsoft® Advertising] 広告グループ。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 7339af39250f0328bc6e8d530a2d7f04286132e5
workflow-type: tm+mt
source-wordcount: '667'
ht-degree: 0%

---

# [!DNL Microsoft® Advertising] 広告グループ設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は 128 文字です。

**[!UICONTROL Status]:** 広告グループの表示ステータス： *アクティブ* または *一時停止*. 新しい広告グループのデフォルトはです。 *アクティブ*.

**[!UICONTROL Ad Language]:** （検索キャンペーン）広告のターゲット言語。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** （広告を検索）広告グループ内に広告を配置する方法と場所：

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! websites]* （デフォルト）：広告の入札を検索ネットワークに配置します。

* *[!UICONTROL Only Microsoft® Advertising and Yahoo! syndicated search partners]:* 同時配信されるパートナーサイトに広告の入札を行う。

* *[!UICONTROL Content network]:* 非推奨

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** 非推奨

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （オーディエンス広告グループ）次のようにします。

* *[!UICONTROL Target and Bid]:* ターゲットオーディエンスに関連付けられているユーザーで、その広告グループに対する他のターゲットも満たしているユーザーにのみ広告を表示する。

* *[!UICONTROL Bid Only]:* ターゲットオーディエンスに関連付けられていない人物であっても、他の広告グループレベルのターゲットを満たす限り、広告を表示する。 ただし、特定のオーディエンスに対してより高い入札を設定することで、それらのオーディエンスに広告が表示される可能性を高めることができます。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

の場合 [!DNL Microsoft® Advertising] オーディエンスネットワークの広告グループ、ロケーションターゲットの入札修飾子は、「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定です。

**[!UICONTROL Genre]:** （の広告グループ [!UICONTROL Audience CTV Video] キャンペーン：米国、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY および TH で使用可能<!-- should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->）ターゲットジャンル。広告を表示する番組とチャネルを決定します。

* *[!UICONTROL All genres]:* （既定値）すべてのジャンルをターゲットにします。

* *[!UICONTROL Select From Below List]:* ターゲットは選択したジャンル。 使用可能なすべてのジャンルのリストから選択します。

接続された TV （CTV）広告の配置は、ビデオの品質と入札額に応じて異なります。 を参照してください。 [ctv 広告の技術的要件](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements).

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** （オーディエンス広告グループ。オプション）ターゲットとして含める、または除外する特定のヘッダー： *[!UICONTROL Male]*, *[!UICONTROL Female]*、および *[!UICONTROL Unknown]*. デフォルトでは、すべての性別がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、その値の横にある円を 1 回クリックし、青いチェックマーク（![次を含める](/help/search-social-commerce/assets/include.png "次を含める")）が表示されます。 オプションで、ターゲットとなる性別ごとに指定した割合で入札を増減できます。

* 値を除外するには、その値の横にある円を 2 回クリックして、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されます。

**[!UICONTROL Age]:** （オーディエンス広告グループ。オプション）ターゲットとして含める、または除外する特定の年齢カテゴリ： *[!UICONTROL 18-24]*, *[!UICONTROL 25-34]*, *[!UICONTROL 35-49]*, *[!UICONTROL 50-64]*, *[!UICONTROL 65+]*、および *[!UICONTROL Unknown]*. デフォルトでは、すべてのページがターゲットになっています。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、その値の横にある円を 1 回クリックし、青いチェックマーク（![次を含める](/help/search-social-commerce/assets/include.png "次を含める")）が表示されます。 必要に応じて、ターゲットとする各年齢に指定の割合で入札を増減できます。

* 値を除外するには、その値の横にある円を 2 回クリックして、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されます。

**[!UICONTROL Industry]:** （オーディエンス広告グループ。任意）ターゲットとして含める、または除外する特定の業界。 デフォルトでは、すべての業界がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、その値の横にある円を 1 回クリックし、青いチェックマーク（![次を含める](/help/search-social-commerce/assets/include.png "次を含める")）が表示されます。 オプションで、ターゲットとする業界ごとに指定した割合で入札を増減できます。

* 値を除外するには、その値の横にある円を 2 回クリックして、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されます。

**[!UICONTROL Job Function Targets]:** （オーディエンス広告グループ。オプション）ターゲットとして含めたり除外したりする特定の職種。 デフォルトでは、すべてのジョブ機能がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、その値の横にある円を 1 回クリックし、青いチェックマーク（![次を含める](/help/search-social-commerce/assets/include.png "次を含める")）が表示されます。 必要に応じて、ターゲットとする各役職機能に対して指定したパーセントで入札を増減できます。

* 値を除外するには、その値の横にある円を 2 回クリックして、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されます。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** （任意）顧客が広告グループから広告を提供される回数。 値を入力して時間単位を選択します（*[!UICONTROL Hour]*, *[!UICONTROL Day]*、または *[!UICONTROL Week]*）に設定します。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。オプション）広告を表示しないディスプレイネットワーク上のサイト。 www.example.comのように、有効な URL を入力します。 複数の文字列を指定する場合は、コンマで区切るか、別の行に入力します。

可用性の詳細については、を参照してください [!DNL Microsoft® Advertising] ヘルプ対象&#39;&#39;[特定の web サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0).」と入力します。

>[!MORELIKETHIS]
>
>* [広告グループの管理](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
