---
title: '[!DNL Microsoft Advertising]広告グループの設定'
description: ' [!DNL Microsoft Advertising] 広告グループの設定を参照します。'
exl-id: 5d788e5b-ddf3-4f4e-8e8d-98e3235cb187
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/f-mac9RGzF4qVr7P65-9AuhWKf22tdND5XSJ1YvLWyc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 75e264e213f60ae45c4f51f0a21352f690d6d699
workflow-type: tm+mt
source-wordcount: 756
ht-degree: 0%

---

# [!DNL Microsoft Advertising]広告グループの設定

## \[ ページの先頭]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新規広告キャンペーンのデフォルトは&#x200B;*アクティブ*&#x200B;です。

## [!UICONTROL Basic Settings] タブ

*新しいキャンペーンのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。

## [!UICONTROL Ad Group Details] タブ

**[!UICONTROL Ad Language]:** （キャンペーンの検索）広告のターゲット言語。

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

## [!UICONTROL Networks] タブ

**[!UICONTROL Networks]:** （検索広告）広告グループ内で広告を配置する方法と場所：

* *[!UICONTROL Only Bing and Yahoo websites]* （既定値）：検索ネットワークに広告の入札を配置します。

* *[!UICONTROL Only Bing and Yahoo syndicated search partners]:* シンジケート パートナーのサイトで広告の入札を行います。

* *[!UICONTROL Content Network]:*&#x200B;は非推奨です

## [!UICONTROL Budget Options] タブ

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Content Bid]:**&#x200B;は非推奨です

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （オーディエンス広告グループ）次の操作を実行するかどうか：

* *[!UICONTROL Bid Only]:*&#x200B;他の広告グループレベルのターゲットを満たしている限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示します。 ただし、特定のオーディエンスに対して高い入札額を設定することで、広告が表示される可能性を高めることができます。

* *[!UICONTROL Target and Bid]:*&#x200B;広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーにのみ広告を表示します。

<!-- **[!UICONTROL Location Target]:** -->

{{$include /help/_includes/location-targets.md}}

オーディエンスネットワーク内の[!DNL Microsoft Advertising]広告グループの場合、場所ターゲットの入札修飾子は、「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定の標準ポートフォリオでは最適化されません。

**[!UICONTROL Genre]:** （キャンペーン [!UICONTROL Audience CTV Video]件の広告グループ。US、CA、BR、MX、UK、DE、ES、FR、IT、AU、MY、TH<!-- Should that go in the campaign sub-type description instead, or is this applicable for this feature only? -->で利用可能）広告が表示される番組とチャネルを決定するターゲットジャンル：

* *[!UICONTROL All genres]:* （既定値）すべてのジャンルをターゲットにします。

* *[!UICONTROL Select From Below List]:*&#x200B;選択したジャンルをターゲットにします。 利用可能なすべてのジャンルのリストから選択します。

コネクテッド TV （CTV）の広告の配置は、動画の質と入札額によって異なります。 CTV広告の[技術要件](https://help.ads.microsoft.com/#apex/ads/en/60102/0/#TechnicalRequirements)を参照してください。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

**[!UICONTROL Gender]:** （オプション）ターゲットとして含めるまたは除外する特定の性別：*[!UICONTROL Male]*、*[!UICONTROL Female]*、および&#x200B;*[!UICONTROL Unknown]*。 デフォルトでは、すべての性別がターゲットになっています。 除外は常にインクルージョンを上書きします。

* すべての値をターゲットにするには、値を選択しないでください。

* 値を含めるには、青いチェックマーク（![Include](/help/search-social-commerce/assets/include.png "Include")）が表示されるように、隣接する円を1回クリックします。 オプションで、ターゲットとなる性別ごとに指定した割合で入札を増減できます。

* 値を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

**[!UICONTROL Age]:** （オプション）ターゲットとして含めるまたは除外する特定の年齢カテゴリ：*[!UICONTROL 18-24]*、*[!UICONTROL 25-34]*、*[!UICONTROL 35-49]*、*[!UICONTROL 50-64]*、*[!UICONTROL 65+]*、および&#x200B;*[!UICONTROL Unknown]*。 デフォルトでは、すべての年齢がターゲットになっています。 除外は常にインクルージョンを上書きします。

* すべての値をターゲットにするには、値を選択しないでください。

* 値を含めるには、青いチェックマーク（![Include](/help/search-social-commerce/assets/include.png "Include")）が表示されるように、隣接する円を1回クリックします。 オプションで、ターゲットとする各年齢に対して指定した割合で入札を増減できます。

* 値を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

**[!UICONTROL Company targets]:** （オプション） ユーザー[!DNL LinkedIn] プロファイルの特定の企業が、ターゲットとして含めるか除外します。 デフォルトでは、すべての企業がターゲットになっています。 ターゲティングを絞り込むには、個々の企業および中堅企業を検索して選択します。 除外は常にインクルージョンを上書きします。

* すべての値をターゲットにするには、値を選択しないでください。

* 値を含めるには、青いチェックマーク（![Include](/help/search-social-commerce/assets/include.png "Include")）が表示されるように、隣接する円を1回クリックします。 オプションで、ターゲット企業ごとに指定した割合で入札を増減できます。

* 値を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

**[!UICONTROL Industry]:** （オプション） ユーザー[!DNL LinkedIn] プロファイルの特定の業界をターゲットとして含めるか、除外します。 デフォルトでは、すべての業界がターゲットになっています。 除外は常にインクルージョンを上書きします。

* すべての値をターゲットにするには、値を選択しないでください。

* 値を含めるには、青いチェックマーク（![Include](/help/search-social-commerce/assets/include.png "Include")）が表示されるように、隣接する円を1回クリックします。 必要に応じて、ターゲットとする業界ごとに指定した割合で入札を増減できます。

* 値を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

**[!UICONTROL Job Function Targets]:** （オプション） ユーザー[!DNL LinkedIn] プロファイルの特定のジョブ関数をターゲットとして含めるか除外します。 デフォルトでは、すべてのジョブ関数がターゲットになっています。 除外は常にインクルージョンを上書きします。

* すべての値をターゲットにするには、値を選択しないでください。

* 値を含めるには、青いチェックマーク（![Include](/help/search-social-commerce/assets/include.png "Include")）が表示されるように、隣接する円を1回クリックします。 オプションで、ターゲットとなる各担当業務に対して、指定した割合で入札額を増減できます。

* 値を除外するには、赤いチェックマーク（![除外](/help/search-social-commerce/assets/exclude.png "除外")）が表示されるように、隣接する円を2回クリックします。

## [!UICONTROL URL Options] タブ

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-microsoft.md}}

<!-- **[!UICONTROL Custom Parameters]:** -->

{{$include /help/_includes/custom-parameters.md}}

## [!UICONTROL Additional Ad Group Information] タブ

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-microsoft.md}}

### [!UICONTROL Negative Websites]

**[!UICONTROL Negative Websites]:** （ディスプレイ/ネイティブネットワーク上のキャンペーンのみ。オプション）広告を表示しないディスプレイネットワーク上のサイト。 www.example.comなどの有効なURLを入力します。 複数の文字列を指定するには、それらをコンマで区切るか、別々の行に入力します。

利用可能性について詳しくは、「[特定のweb サイトに広告が表示されないようにする](https://help.ads.microsoft.com/#apex/bae/en/14061/0)」の[!DNL Microsoft Advertising] ヘルプを参照してください。

### [!UICONTROL Ad Group Frequency Cap Settings]

（オプション）顧客が広告グループから広告を配信できる回数。 値を入力し、時間単位（*[!UICONTROL Hour]*、*[!UICONTROL Day]*、*[!UICONTROL Week]*）または&#x200B;*[!UICONTROL Month]*）を選択します。

>[!MORELIKETHIS]
>
>* [広告グループの管理](/help/search-social-commerce/new-ui/manage/ad-groups/ad-group-manage.md)
