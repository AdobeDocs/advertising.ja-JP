---
title: '''[!DNL Google Ads] 広告グループ設定'
description: 次の設定を参照してください： [!DNL Google Ads] 広告グループ。
exl-id: 00aaa936-796f-4e22-9bee-4bb5121cd887
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '419'
ht-degree: 0%

---

# [!DNL Google Ads] 広告グループ設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は 255 文字です。

**[!UICONTROL Status]:** 広告グループの表示ステータス： *アクティブ* または *一時停止*. 新しい広告グループのデフォルトはです。 *アクティブ*.

**[!UICONTROL Ad Group Type]:** （動的検索広告キャンペーンのみ）広告グループのタイプ。

* *[!UICONTROL Search Standard]* （デフォルト）：標準の広告の場合。

* *[!UICONTROL Search Dynamic]:* 動的検索広告の場合。

**[!UICONTROL Ad Rotation Mode]:** 頻度 [!DNL Google Ads] は、アクティブな広告を広告グループ内で相互に関連付けて配信します。

* *[!UICONTROL Optimize]:* Google Ads は、広告グループ内の他の広告よりもパフォーマンスが高いと予想される広告を優先します。 これらの広告は、より頻繁に広告オークションに入り、時間の経過と共に単一の広告が優先されます。 これは、ビジネス目標や最適化目標と一致しない場合があります。

* *[!UICONTROL Rotate forever]:*   各広告が広告オークションにより偶数回入力され、Search、Social、および Commerce は、クリックスルー率だけでなくコンバージョンでも広告にスコアを付けることができます。

* *[!UICONTROL Use campaign setting]*（新しい広告グループのデフォルト）：既存のキャンペーンレベルの広告ローテーション設定を使用します。 **注意：** キャンペーンレベルの設定は、検索、ソーシャル、コマースでは表示されません。

キャンペーンがスマート入札入札戦略 ( [!UICONTROL Target CPA], [!UICONTROL Target ROAS]または [!UICONTROL Enhanced CPC])、 [!DNL Google Ads] オプションを自動的に&quot;に設定します[!UICONTROL Optimize].&quot;

**[!UICONTROL Custom Bid Level]:** （ディスプレイネットワークのみをターゲットにするキャンペーン）入札方法： by *[!UICONTROL Ad Group]* （デフォルト）、 *[!UICONTROL Age]*, *[!UICONTROL Gender]*, *[!UICONTROL Interest and List]* (Google Ads の興味とリマーケティング ) *[!UICONTROL Keyword]*, *[!UICONTROL Placement]* （Web サイト）、 *[!UICONTROL Unknown]*&#x200B;または *[!UICONTROL Vertical]*.

>[!NOTE]
>
>* キーワードで入札する場合は、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメントで入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他すべてのディメンションについては、広告レベルでトラッキングテンプレートを作成します。
>* ポートフォリオ内のキャンペーンに対して、年齢、性別、興味、リスト、または垂直で入札する場合、最適化機能では、ディメンションの入札が最適化されません。 また、すべてのアトリビューションは広告グループに適用されます。
>* 検索ネットワーク上の広告は、常にキーワード入札を使用します。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** ( 次を含むキャンペーン： [!UICONTROL Target CPA] 入札（オプション）広告グループの獲得あたりのターゲットコスト (CPA)。 この値は、キャンペーンレベルのターゲットよりも優先されます。

**[!UICONTROL Target ROAS]:** ( 次を含むキャンペーン： [!UICONTROL Target ROAS] 入札；オプション ) 広告グループの広告費用対効果 (ROAS)（パーセンテージ）。 この値は、キャンペーンレベルのターゲットよりも優先されます。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** ( 検索ネットワーク上のキャンペーンと、既存の読み取り専用 [!DNL Gmail] ディスプレイネットワーク上のキャンペーン ) 次のどちらを実行するかを指定します。

* *[!UICONTROL Target and Bid]:* 広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーに対してのみ広告を表示する。

* *[!UICONTROL Bid Only]:* ターゲットオーディエンスに関連付けられていないユーザーが他の広告グループレベルのターゲットを満たしている限り、広告を表示する。 ただし、特定のオーディエンスに対して広告が表示される可能性を高めるには、それらのオーディエンスの入札額を高く設定します。

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
>* [広告グループの管理](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)
