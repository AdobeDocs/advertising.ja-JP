---
title: '[!DNL Google Ads] 広告グループ設定'
description: 広告グループの設定  [!DNL Google Ads]  参照します。
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
source-git-commit: fb38bf6afa181b4560742d3649db68c8aef0e619
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] 広告グループ設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は 255 文字の 2 バイト文字です。

**[!UICONTROL Status]:** 広告グループの表示ステータス：*アクティブ* または *一時停止*。 新しい広告グループのデフォルトは *アクティブ* です。

**[!UICONTROL Ad Group Type]:** （拡張された動的検索広告キャンペーンのみ）広告グループのタイプ：

* *[!UICONTROL Search Standard]* （デフォルト）：標準広告の場合。

* *[!UICONTROL Search Dynamic]:* 動的検索広告。

**[!UICONTROL Ad Rotation Mode]:** 広告グループ内 [!DNL Google Ads] アクティブな広告を相互に関連させて配信する頻度：

* *[!UICONTROL Optimize]:* Google広告は、広告グループ内の他の広告よりも優れたパフォーマンスを期待している広告をお勧めします。 これらの広告はより頻繁に広告オークションに入り、時間の経過とともに単一の広告が好まれます。 これは、ビジネス目標や最適化目標と一致しない場合があります。

* *[!UICONTROL Rotate forever]:*   各広告はより偶数の回数で広告オークションにエントリします。これにより、検索、ソーシャル、Commerceで、クリックスルー率だけでなくコンバージョンでも広告をスコアリングできます。

* *[!UICONTROL Use campaign setting]* （新しい広告グループのデフォルト）：既存のキャンペーンレベルの広告ローテーション設定を使用します。 **メモ：** キャンペーンレベルの設定は、検索、ソーシャル、Commerceには表示されません。

キャンペーンでスマート入札入札戦略（[!UICONTROL Target CPA]、[!UICONTROL Target ROAS] など）を使用する場合、[!DNL Google Ads] はオプションを自動的に「[!UICONTROL Optimize]」に設定します。

**[!UICONTROL Custom Bid Level]:** （ディスプレイネットワークをターゲットとするキャンペーンのみ）入札方法：*[!UICONTROL Ad Group]* （デフォルト）、*[!UICONTROL Age]*、*[!UICONTROL Gender]*、*[!UICONTROL Interest and List]* （Google Ads の興味とリマーケティング）、*[!UICONTROL Keyword]*、*[!UICONTROL Placement]* （web サイト）、*[!UICONTROL Unknown]*、*[!UICONTROL Vertical]*。

>[!NOTE]
>
>* キーワードで入札する場合、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメント別に入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他のすべてのディメンションでは、広告レベルでトラッキングテンプレートを作成します。
>* ポートフォリオのキャンペーンを年齢、性別、興味とリスト、または垂直方向で入札する場合、最適化機能はディメンションの入札を最適化しません。 また、すべてのアトリビューションが広告グループに適用されます。
>* 検索ネットワーク上の広告は、常にキーワード入札を使用します。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** （[!UICONTROL Target CPA] 入札キャンペーン、オプション）広告グループの獲得あたりの目標コスト（CPA）。 この値は、キャンペーンレベルのターゲットを上書きします。

**[!UICONTROL Target ROAS]:** （[!UICONTROL Target ROAS] 入札キャンペーン、オプション）広告グループのターゲット広告費用対効果（ROAS）（パーセンテージ）。 この値は、キャンペーンレベルのターゲットを上書きします。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （検索ネットワーク上のキャンペーンおよび表示ネットワーク上の既存の読み取り専用 [!DNL Gmail] キャンペーン）次のどちらを実行するか：

* *[!UICONTROL Target and Bid]:* ターゲットオーディエンスに関連付けられているユーザーで、その広告グループの他のターゲットも満たしているユーザーにのみ広告を表示します。

* *[!UICONTROL Bid Only]:* 他の広告グループレベルのターゲットを満たす限り、ターゲットオーディエンスに関連付けられていない人物にも広告を表示する場合。 ただし、特定のオーディエンスに対してより高い入札を設定することで、それらのオーディエンスに広告が表示される可能性を高めることができます。

<!-- **[!UICONTROL Devices]:** -->

{{$include /help/_includes/devices.md}}

## [!UICONTROL URL Options]

<!-- **[!UICONTROL Tracking Template]:** -->

{{$include /help/_includes/tracking-template-google.md}}

## [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-google.md}}

## [!UICONTROL Negative Websites]

<!-- **[!UICONTROL Negative Websites]:** -->

{{$include /help/_includes/negative-websites-google.md}}

>[!MORELIKETHIS]
>
>* [ 広告グループの管理 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
