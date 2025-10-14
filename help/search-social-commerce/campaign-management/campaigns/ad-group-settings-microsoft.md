---
title: '[!DNL Microsoft Advertising] 広告グループの設定'
description: 広告グループの設定  [!DNL Microsoft Advertising]  参照します。
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '651'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 広告グループ設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は 128 文字です。

**[!UICONTROL Status]:** 広告グループの表示ステータス：*アクティブ* または *一時停止*。 新しい広告グループのデフォルトは *アクティブ* です。

**[!UICONTROL Ad Language]:** （検索キャンペーン）広告のターゲット言語。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks]

**[!UICONTROL Networks]:** （広告を検索）広告グループ内に広告を配置する方法と場所：

* *[!UICONTROL Only Microsoft Advertising and Yahoo! websites]* （デフォルト）：検索ネットワークに広告の入札を配置します。

* *[!UICONTROL Only Microsoft Advertising and Yahoo! syndicated search partners]:* 同時配信されるパートナーサイトに広告の入札を行います。

* *[!UICONTROL Content network]:* 非推奨（廃止予定）

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:** 非推奨（廃止予定）

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （オーディエンス広告グループ）次の操作を行うかどうか：

* *[!UICONTROL Target and Bid]:* ターゲットオーディエンスに関連付けられているユーザーで、その広告グループの他のターゲットも満たしているユーザーにのみ広告を表示します。

* *[!UICONTROL Bid Only]:* 他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていない人物にも広告を表示する場合。 ただし、特定のオーディエンスに対してより高い入札を設定することで、それらのオーディエンスに広告が表示される可能性を高めることができます。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

オーディエンスネットワークの [!DNL Microsoft Advertising] の広告グループの場合、ロケーションターゲットの入札修飾子は、「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定の標準ポートフォリオでは最適化されません。

**[!UICONTROL Genre]:** （[!UICONTROL Audience CTV Video] キャンペーンの広告グループ。米国、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY、TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? --> で利用可能）広告が表示される番組とチャネルを決定するターゲットジャンル。

* *[!UICONTROL All genres]:* （デフォルト）すべてのジャンルをターゲットにします。

* *[!UICONTROL Select From Below List]:* 選択したジャンルのターゲット。 使用可能なすべてのジャンルのリストから選択します。

接続された TV （CTV）広告の配置は、ビデオの品質と入札額に応じて異なります。 詳しくは、[CTV 広告の技術要件 &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements) を参照してください。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** （オーディエンス広告グループ、オプション）ターゲットとして含める、または除外する特定の性別：*[!UICONTROL Male]*、*[!UICONTROL Female]* および *[!UICONTROL Unknown]*。 デフォルトでは、すべての性別がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、隣の円を 1 回クリックして、青いチェックマーク（![&#x200B; 含める &#x200B;](/help/search-social-commerce/assets/include.png " 含める ")）を表示します。 オプションで、ターゲットとなる性別ごとに指定した割合で入札を増減できます。

* 値を除外するには、隣の円を 2 回クリックして、赤いチェックマーク（![&#x200B; 除外 &#x200B;](/help/search-social-commerce/assets/exclude.png " 除外 ")）を表示します。

**[!UICONTROL Age]:** （オーディエンス広告グループ、オプション）ターゲットとして含める、または除外する特定の年齢カテゴリ：*[!UICONTROL 18-24]*、*[!UICONTROL 25-34]*、*[!UICONTROL 35-49]*、*[!UICONTROL 50-64]*、*[!UICONTROL 65+]* および *[!UICONTROL Unknown]*。 デフォルトでは、すべてのページがターゲットになっています。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、隣の円を 1 回クリックして、青いチェックマーク（![&#x200B; 含める &#x200B;](/help/search-social-commerce/assets/include.png " 含める ")）を表示します。 必要に応じて、ターゲットとする各年齢に指定の割合で入札を増減できます。

* 値を除外するには、隣の円を 2 回クリックして、赤いチェックマーク（![&#x200B; 除外 &#x200B;](/help/search-social-commerce/assets/exclude.png " 除外 ")）を表示します。

**[!UICONTROL Industry]:** （オーディエンス広告グループ、オプション）ターゲットとして含めるか除外する特定の業界。 デフォルトでは、すべての業界がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、隣の円を 1 回クリックして、青いチェックマーク（![&#x200B; 含める &#x200B;](/help/search-social-commerce/assets/include.png " 含める ")）を表示します。 オプションで、ターゲットとする業界ごとに指定した割合で入札を増減できます。

* 値を除外するには、隣の円を 2 回クリックして、赤いチェックマーク（![&#x200B; 除外 &#x200B;](/help/search-social-commerce/assets/exclude.png " 除外 ")）を表示します。

**[!UICONTROL Job Function Targets]:** （オーディエンス広告グループ、オプション）ターゲットとして含めたり除外したりする特定の職種。 デフォルトでは、すべてのジョブ機能がターゲットになります。 除外は、常に包含を上書きします。

* すべての値をターゲットにするには、どの値も選択しません。

* 値を含めるには、隣の円を 1 回クリックして、青いチェックマーク（![&#x200B; 含める &#x200B;](/help/search-social-commerce/assets/include.png " 含める ")）を表示します。 必要に応じて、ターゲットとする各役職機能に対して指定したパーセントで入札を増減できます。

* 値を除外するには、隣の円を 2 回クリックして、赤いチェックマーク（![&#x200B; 除外 &#x200B;](/help/search-social-commerce/assets/exclude.png " 除外 ")）を表示します。

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

**[!UICONTROL Adgroup Frequency Cap Settings]:** （任意）顧客が広告グループから広告を提供できる回数。 値を入力して、時間単位（*[!UICONTROL Hour]*、*[!UICONTROL Day]*、*[!UICONTROL Week]*）を選択します。

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

## [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。オプション）広告を表示しないディスプレイネットワーク上のサイト。 www.example.comのように、有効な URL を入力します。 複数の文字列を指定する場合は、コンマで区切るか、別の行に入力します。

利用可能なサイトについて詳しくは、「[&#x200B; 特定の Web サイトに広告が表示されないようにする &#x200B;](https://help.ads.microsoft.com/#apex/bae/en/14061/0)」のヘルプを [!DNL Microsoft Advertising] 照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; 広告グループの管理 &#x200B;](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
