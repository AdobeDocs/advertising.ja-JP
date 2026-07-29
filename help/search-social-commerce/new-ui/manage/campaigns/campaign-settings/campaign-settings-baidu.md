---
title: '[!DNL Baidu] キャンペーン設定'
description: ' [!DNL Baidu]  キャンペーンの設定を参照します。'
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 3a5c2507f3acb08419e143ba906cf55df2496d0f
workflow-type: tm+mt
source-wordcount: 309
ht-degree: 0%

---

# [!DNL Baidu] キャンペーン設定

## \[ ページの先頭]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新規広告キャンペーンのデフォルトは&#x200B;*アクティブ*&#x200B;です。

## [!UICONTROL Basic Settings] タブ

*新しいキャンペーンのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign Type]:**&#x200B;広告を配置する場所、およびキャンペーンに含めることができる広告タイプ。 唯一のオプションは&#x200B;*検索ネットワークのみ*&#x200B;です。

## [!UICONTROL Campaign Details] タブ

<!-- **[!UICONTROL Start Date]:** -->

{{$include /help/_includes/start-date.md}}

<!-- **[!UICONTROL End Date]:** -->

{{$include /help/_includes/end-date.md}}

**[!UICONTROL Contains EU Political Ads]:** （欧州連合（EU）のオーディエンスをターゲットとするキャンペーンに適用）キャンペーンに、EU規則2024/90に基づいて欧州連合で配信される広告の要件に従った政治的広告が含まれているかどうか：*[!UICONTROL Yes]*&#x200B;または&#x200B;*[!UICONTROL No]*。

## [!UICONTROL Budget Options] タブ

<!-- **[!UICONTROL Budget]:** -->

{{$include /help/_includes/budget.md}}

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

<!--VERIFY OPTIMIZATION BEHAVIOR -->**[!UICONTROL Bid strategy]:** キャンペーンの入札戦略：

* *[!UICONTROL Maximize Conversions]:*&#x200B;検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化してコンバージョンを最大化します。 必要に応じて、**[!UICONTROL Target CPA]** （獲得単価）を入力します。 **注：** キャンペーンレベルの最適化が適用されたポートフォリオのキャンペーンに対して、このオプションを使用します。 キャンペーンレベルの最適化が可能なポートフォリオでは、Search, Social, &amp; CommerceでTarget CPAを最適化します。

* *[!UICONTROL Maximize Conversion Value]:*&#x200B;検索、ソーシャル、Commerceではなく、広告ネットワークが入札を最適化し、コンバージョンの価値を最大化します。 オプションで&#x200B;**[!UICONTROL Target Return on Ad Spend]** （ROAS）をパーセントとして入力します。 **注：** キャンペーンレベルの最適化が適用されたポートフォリオのキャンペーンに対して、このオプションを使用します。 キャンペーンレベルの最適化が可能なポートフォリオでは、Search, Social, &amp; CommerceでTargetのROASを最適化します。

## [!UICONTROL Campaign Targeting] タブ

**[!UICONTROL Languages]:**&#x200B;広告の言語。広告を表示できるサイトの言語と一致する必要があります。 広告ネットワークは、ユーザーのクエリ、パブリッシャーの国、ユーザーの言語設定など、様々なシグナルからユーザーの言語を決定します。

<!-- **[!UICONTROL Location Targets]:** -->

{{$include /help/_includes/location-targets.md}}

## [!UICONTROL Additional Campaign Information] タブ

### [!UICONTROL Negative Keywords]

<!-- **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword.md}}

<!-- Note for **[!UICONTROL Campaign Negative Keywords]:** -->

{{$include /help/_includes/negative-keyword-note-baidu.md}}

### [!UICONTROL Campaign Tracking] タブ

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** （[!UICONTROL EF Redirect]の場合のみ）リダイレクトを追加し、関連URLにパラメーターを追加して、クリックと収益を追跡するレベル：

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡します。

* *[!UICONTROL Creative]:*&#x200B;広告（クリエイティブ）レベルでのみデータを追跡します。

* *[!UICONTROL Creative and Keyword]:*&#x200B;広告（クリエイティブ）レベルとキーワードレベルの両方でデータを追跡します。

**[!UICONTROL Enable conversion reporting in Adobe Analytics]:** アカウントまたはキャンペーンの広告にURL パラメーターを追加して、コンバージョンを追跡します。

<!-- **[!UICONTROL Encode Base URL]:** -->

{{$include /help/_includes/encode-base-url.md}}

<!-- **[!UICONTROL Append Parameters]:** -->

{{$include /help/_includes/append-parameters.md}}

<!--

Not there as of 7/22 -- what's going on here? If we're removing it, then I need to update many references throughout the whole doc:

[               **[!UICONTROL Auto Upload]:**      ]

{{$include /help/_includes/auto-upload.md}}

-->

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンの管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
