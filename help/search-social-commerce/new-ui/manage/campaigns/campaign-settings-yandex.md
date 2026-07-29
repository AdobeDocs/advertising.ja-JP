---
title: '[!DNL Yandex] キャンペーン設定'
description: ' [!DNL Yandex]  キャンペーンの設定を参照します。'
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: d45eb490f9dbb7da89bd1270582e5548b70cbd31
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# [!DNL Yandex] キャンペーン設定

## \[ ページの先頭]

**[!UICONTROL Campaign Name]:** アカウント内で一意のキャンペーン名。

**[!UICONTROL Status]:** キャンペーンの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新規広告キャンペーンのデフォルトは&#x200B;*アクティブ*&#x200B;です。

## [!UICONTROL Basic Settings] タブ

*新しいキャンペーンのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign Type]:**&#x200B;広告を配置する場所：

* *[!UICONTROL Search Network Only]:*&#x200B;検索ネットワークにテキスト広告を表示します。 広告グループごとにキーワードを指定する必要があります。

* *[!UICONTROL Search and Display Network]:*&#x200B;検索ネットワークと[!DNL Yandex Advertising Network]にテキスト広告を表示します。 検索広告の場合は、広告グループごとに検索キーワードを指定する必要があります。 ディスプレイ広告の場合は、広告グループごとに広告を掲載するweb サイトのキーワードを指定する必要があります。

* *[!UICONTROL Display Network Only]:* [!DNL Yandex Advertising Network]にテキスト広告を表示します。 広告グループごとに、広告を掲載するweb サイトのキーワードを指定する必要があります。

## [!UICONTROL Campaign Details] タブ

<!-- **[!UICONTROL Start date]:** -->

{{$include /help/_includes/start-date.md}}

## [!UICONTROL Budget Options] タブ

**[!UICONTROL Budget]:**&#x200B;予算。アカウントの予算タイプに応じて、毎日（平均）またはキャンペーン期間中に費やしたい金額です。 最低予算は6,300円、10 ユーロ、10米ドルです。

**メモ：**

* 新しいキャンペーンには、入札管理戦略に「利用可能な最高のポジション」があります。

* 検索条件に応じて、キャンペーンの予算制限を自動的に調整できるように設定されたポートフォリオにこのキャンペーンを割り当てる場合、特定の日、月、またはライフタイムに指定された予算以上の予算を実際に費やすことができます。

<!-- **[!UICONTROL Delivery Method]:** -->

{{$include /help/_includes/delivery-method.md}}

## [!UICONTROL Additional Campaign Information] タブ

### [!UICONTROL Campaign Tracking]

<!-- **[!UICONTROL Override Account Tracking]:** -->

<!-- **[!UICONTROL Override Account Tracking]:** -->

{{$include /help/_includes/override-account-tracking.md}}

<!-- **[!UICONTROL Tracking Type]:** -->

{{$include /help/_includes/tracking-type.md}}

<!-- **[!UICONTROL Redirect Type]:** -->

{{$include /help/_includes/redirect-type.md}}

**[!UICONTROL Tracking Level]:** （[!UICONTROL EF Redirect]のみ。読み取り専用）クリックと収益を追跡するレベル。 *[!UICONTROL Creative]*&#x200B;のみが[!DNL Yandex]で利用できます。データは広告（クリエイティブ）レベルでのみ追跡されます。

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
>* [ キャンペーンの管理](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)
