---
title: '[!DNL Google Ads]広告グループの設定'
description: ' [!DNL Google Ads] 広告グループの設定を参照します。'
exl-id: def75630-19b9-4676-ad34-5d9041cc3680
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/pDFheVIM62XNCh2-7jbCscIqOrcTep7qnNg5S1tHYF8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 3111796b54e2e633ca734c7141efbc2d82f3087d
workflow-type: tm+mt
source-wordcount: 464
ht-degree: 0%

---

# [!DNL Google Ads]広告グループの設定

## [!UICONTROL Adgroup Details]

**[!UICONTROL Ad Group Name]:** キャンペーン内で一意の広告グループ名。 最大長は255個の2 バイト文字です。

**[!UICONTROL Status]:**&#x200B;広告グループの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新しい広告グループのデフォルトは&#x200B;*アクティブ*&#x200B;です。

**[!UICONTROL Ad Group Type]:** （拡張された動的検索広告キャンペーンのみ）広告グループの種類：

* *[!UICONTROL Search Standard]* （デフォルト）：標準の広告の場合。

* *[!UICONTROL Search Dynamic]:*&#x200B;動的な検索広告。

**[!UICONTROL Ad Rotation Mode]:**&#x200B;広告グループ内で[!DNL Google Ads]がアクティブな広告を相互に関連して配信する頻度：

* *[!UICONTROL Optimize]:* [!DNL Google Ads]は、広告グループ内の他の広告よりもパフォーマンスが高いと予想される広告を好みます。 これらの広告は、より頻繁に広告オークションに出稿され、時間の経過とともに1つの広告が支持されます。 これは、ビジネス目標や最適化目標と一致していない可能性があります。

* *[!UICONTROL Rotate forever]:*&#x200B;各広告は、広告オークションに偶数回参加します。これにより、Search, Social, &amp; Commerceでは、クリックスルー率だけでなく、コンバージョンでも広告をスコアリングできます。

* *[!UICONTROL Use campaign setting]* （新しい広告グループのデフォルト）：既存のキャンペーンレベルの広告ローテーション設定を使用します。 **注意：** キャンペーンレベルの設定は、検索、ソーシャル、およびCommerceでは表示されません。

キャンペーンでスマート入札戦略（[!UICONTROL Target CPA]、[!UICONTROL Target ROAS]など）を使用している場合、[!DNL Google Ads]は自動的にオプションを「[!UICONTROL Optimize]」に設定します。

**[!UICONTROL Custom Bid Level]:** （ディスプレイネットワークのみをターゲットとするキャンペーン）入札方法：*[!UICONTROL Ad Group]* （デフォルト）、*[!UICONTROL Age]*、*[!UICONTROL Gender]*、*[!UICONTROL Interest and List]* （Google Adsでの興味とリマーケティング）、*[!UICONTROL Keyword]*、*[!UICONTROL Placement]* （web サイト）、*[!UICONTROL Unknown]*、または&#x200B;*[!UICONTROL Vertical]*。

>[!NOTE]
>
>* キーワードで入札する場合は、キーワードレベルでトラッキングテンプレートを作成します。 同様に、プレースメントで入札する場合は、プレースメントレベルでトラッキングテンプレートを作成します。 その他のディメンションについては、広告レベルでトラッキングテンプレートを作成します。
>* 年齢、性別、興味とリスト、またはポートフォリオのキャンペーンの垂直方向で入札する場合、最適化機能はディメンションの入札を最適化しません。 また、すべてのアトリビューションは広告グループに適用されます。
>* 検索ネットワーク上の広告は、常にキーワード入札を使用します。

**[!UICONTROL AI Max Search Term Matching]:** （検索ネットワークをターゲットとし、[AI Max機能](https://support.google.com/google-ads/answer/15910366)およびキャンペーンレベルの検索語句の一致機能が有効になっているキャンペーン。読み取り専用）広告グループレベルの検索語句の一致が有効になっているかどうか：*[!UICONTROL Disabled]*&#x200B;または&#x200B;*[!UICONTROL Enabled]*。

## [!UICONTROL Budget Options]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-ad-group.md}}

**[!UICONTROL Target CPA]:** （入札が[!UICONTROL Target CPA]件のキャンペーン。オプション）広告グループの獲得単価（CPA）の目標値。 この値は、キャンペーンレベルのターゲットを上書きします。

**[!UICONTROL Target ROAS]:** （入札が[!UICONTROL Target ROAS]件のキャンペーン。オプション）広告グループの目標広告費用対効果（ROAS）をパーセンテージで示します。 この値は、キャンペーンレベルのターゲットを上書きします。

## [!UICONTROL Ad Group Targeting]

**[!UICONTROL Audience Target Method]:** （検索ネットワーク上のキャンペーン、およびディスプレイネットワーク上の既存の読み取り専用[!DNL Gmail] キャンペーン）次の項目を実行するかどうか：

* *[!UICONTROL Target and Bid]:*&#x200B;広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーにのみ広告を表示します。

* *[!UICONTROL Bid Only]:*&#x200B;他の広告グループレベルのターゲットを満たしている限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示します。 ただし、特定のオーディエンスに対して高い入札額を設定することで、広告が表示される可能性を高めることができます。

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
