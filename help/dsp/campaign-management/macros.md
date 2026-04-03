---
title: Advertising DSP マクロ
description: 一般的なトラッキングに使用できるマクロを参照し、サードパーティのディスプレイ広告のクリックをトラッキングします。
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
TQID: https://experienceleague.adobe.com/4jT3XQq555z7FwlwIj0wkCps3D3Dg-dWD0He3FnlLiQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 940
ht-degree: 0%

---

# Advertising DSP マクロ

マクロは、命令の短いコマンドまたは略語であり、通常は`${MACRO_NAME}`形式に従います。 クリエイティブコードまたはクリックスルーURLに含まれるマクロは、広告サーバーが理解できる長いコード文字列に展開されます。 DSP広告サーバーは、広告が配信またはクリックされたときにマクロを実行します。

Ad server マクロは、重要な情報をDSPまたはサードパーティのAd サーバーに渡すのに便利です。 マクロは、サードパーティおよびカスタムのクリエイティブコードまたはメタデータ（サードパーティピクセルなど）の不正取引で最も一般的に使用されます。

VAST タグ、任意のURL、DSPまたはサードパーティのイベントピクセルなど、任意の場所にマクロを手動で挿入できます。 ただし、DSPのクライアントとパートナーはそれぞれ異なる広告タグフォーマットを持っており、それに応じてマクロをタグ内の異なる場所に挿入する必要があります。 新しいクライアントやパートナーと作業するたびに、DSPが送信する広告タグにマクロをどこに挿入するかについてドキュメントを求めます。

## 一般的なトラッキングマクロ

必要に応じて、あらゆる広告タイプとタグタイプで一般的なトラッキングマクロを使用し、特定のデータを渡します。

| マクロ | 置き換え説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | アカウント ID。 | 整数 |
| `${TM_AD_ID}` | 広告キー（adKey）。 | 文字列 |
| `${TM_AD_ID_NUM}` | 広告ID。 | 整数 |
| `${TM_ADVERTISER_ID}` | 広告主ID。 | 整数 |
| `${TM_CAMPAIGN_ID}` | キャンペーンキー。 | 文字列 |
| `${TM_CAMPAIGN_ID_NUM}` | キャンペーン ID。 | 整数 |
| ` ${TM_CLICK_URL}` | 広告サーバーが広告クリックを追跡およびカウントできるようにするリダイレクト URL。 広告が配信されると、ユーザーがクリックすると、マクロがアクティブになり、クリックはレポート用に記録され、カウントされます。 | 文字列 |
| ` ${TM_CLICK_URL_URLENC}` | エンコードされたリダイレクト URL。広告サーバーは広告クリックを追跡およびカウントできます。 広告が配信されると、ユーザーがクリックすると、マクロがアクティブになり、クリックはレポート用に記録され、カウントされます。 サードパーティ広告を作成し、ベンダーがURL エンコーディングを必要とする場合を除き、このマクロを使用しないでください。 | 文字列 |
| `${TM_FEED_ID}` | メディア配置のキー（feedKey）。 | 文字列 |
| `${TM_FEED_ID_NUM}` | メディア配置のID。 | 整数 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | プレースメントのサイトキー。 モバイルアプリのインストール広告の[!DNL AppsFlyer] クリックトラッカーに必要です。<!-- should map to placement_site_key column of placement_site table --> | 文字列 |
| `${TM_PLACEMENT_ID}` | 配置キー（cpKey）。 | 文字列 |
| `${TM_PLACEMENT_ID_NUM}` | プレースメント ID。 | 整数 |
| `${TM_RANDOM}` | Cachebuster: 1 ～ 1000000の間の乱数。 | 長い |
| `${TM_SESSION_ID}` | 広告タグの1回の取得に対応するセッションのID。 | 文字列 |
| `${TM_SITE_DOMAIN_URLENC}` | 入札リクエストのURLから解析されたページサブドメイン。URLがエンコードされています。 バナー内でクリックして再生する広告ではサポートされていません。 | 文字列 |
| ` ${TM_SITE_NAME}` | プレースメントのサイト名。 | 文字列 |
| `${TM_SITE_URL_URLENC}` | 入札リクエストで渡されたURL。URL エンコードです。 バナー内でクリックして再生する広告ではサポートされていません。 | 文字列 |
| `${TM_SITE_ID_NUM}` | プレースメントのサイト ID。 | 整数 |
| `${TM_TIMESTAMP}` | 1970年1月1日の深夜（00:00 UTC）からの経過秒数を示すUnix タイムスタンプ。 | 長い |
| ` ${TM_VIDEO_DURATION}` | 広告動画のデュレーション（秒単位）。 | 整数 |

{style="table-layout:auto"}

<!--
 Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## モバイル固有のマクロ

| マクロ | 置き換え説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | （[!DNL ComScore]） デバイスのオペレーティング システムに対応するプラットフォーム ID:<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` プラットフォームが上記のいずれでもない場合</li></ul> | varchar （50） |
| `${CS_DEVICE_MODEL}` | （[!DNL ComScore]） デバイスモデル名は、URL エンコードされています。 | 文字列 |
| `${CS_IMPLEMENTATION_TYPE}` | （[!DNL ComScore]）広告が配信された環境：<ul><li>`a` = モバイルアプリケーション</li><li>`b` = モバイル web サイト</li></ul> | 文字列（`a`または`b`） |
| `${NS_PLATFORM_ID}` | （[!DNL Nielsen]） デバイスのオペレーティング システムに対応するプラットフォーム ID:<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>`other` プラットフォームが上記のいずれでもない場合</li></ul> | 文字列 |
| `${NS_DEVICE_GROUPING}` | （[!DNL Nielsen]）広告がビューアーだったデバイスの種類：<ul><li>`TAB` = タブレット</li><li>`PHN` = モバイル</li><li>`computer` = コンピューター</li></ul> | 文字列 |
| `${UOO}` | （[!DNL Nielsen]） ユーザーが広告トラッキングをオプトアウトしたかどうかを示します：<ul><li>`1` （DNT フラグ = 1） = ユーザーは広告トラッキングをオプトアウトしました</li><li>`0` （DNT フラグ = 0） = ユーザーが広告トラッキングにオプトインしました</li></ul> | 整数（`0`または`1`） |
| `${TM_BUNDLE}` | [!DNL iOS]または[!DNL Android] アプリストア バンドル ID。 例：com.zynga.wwf2.freeまたはid804379658 | 文字列 |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}`は、入札者が入札依頼が欧州連合（EU）の出所によるものであると判断し、GDPRの適用を必要とするかどうかを示します。<ul><li>`1` = GDPRを適用する必要があります</li><li>`0` = GDPRは適用できません</li></ul>`gdpr_consent=${GDPR_CONSENT}`は、インバウンド入札要求でサプライパートナーから渡された同意値です。<ul><li>ほとんどの場合、これはbase64url エンコードされた同意文字列、またはdaisybitです（例：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA）</li><li>`0` =同意なし</li><li>`1` =同意</li></ul> | daisybitまたは整数 |

{style="table-layout:auto"}

## サードパーティのディスプレイ広告のクリックマクロ

サードパーティのディスプレイタグを使用して広告のクリックを正確に追跡するには、DSPにディスプレイクリックマクロが必要です。 必要なマクロのバージョンは1つのみです。関連するマクロは、タグのタイプによって異なります。

| マクロ | 置き換え説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 広告サーバーがプラットフォームでの広告クリックを追跡およびカウントできるようにするリダイレクト URL。 | 文字列 |
| `${TM_CLICK_URL_URLENC}` | URL エンコーディングを必要とする広告サーバーが、プラットフォームでの広告クリックを追跡およびカウントできるようにするリダイレクト URL。 | 文字列 |

{style="table-layout:auto"}

DSPでは、次の操作を行うと、サードパーティの表示タグに表示クリックマクロが自動的に挿入されます。

* 広告サーバーパートナー<!-- [Needs PM confirmation.] -->からの広告タグのエクスポート
* [!DNL Flashtalking]または[!DNL Google DoubleClick for Advertisers]個の広告タグをDSPに直接アップロードできます

ディスプレイ広告の作成時にクリックマクロが見つからない場合、DSPに警告メッセージが表示され、タグの正しい領域に適切な表示クリックマクロを手動で挿入するように求められます。

## [!DNL Analytics for Advertising]個のマクロ

[[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)のお客様向けに特別に使用できる追加のマクロについては、「[追加 [!DNL Analytics for Advertising]  マクロを [!DNL Flashtalking] 広告タグ &#x200B;](/help/integrations/analytics/macros-flashtalking.md)」および「[追加 [!DNL Analytics for Advertising]  マクロを [!DNL Google Campaign Manager 360] 広告タグ &#x200B;](/help/integrations/analytics/macros-google-campaign-manager.md)」を参照してください。

## マクロエラーのトラブルシューティング

コードにマクロを追加する場合は、必ずマクロの正確な構文を使用してください。 マクロを検証する際、DSPは、マクロが有効なマクロの1つと正確に一致することを確認します。

マクロ名の先頭または末尾に文字がない場合は、エラーが生成されます。 例えば、次のような場合にエラーメッセージが表示されます。

* マクロ名の先頭にある文字（`${`など）を1つ以上忘れた場合。 完全な構文を含まない場合、エントリは有効なマクロとして認識されません。
* マクロの末尾に`}`などの有効な文字セットが含まれていません。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディオ広告設定](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [&#x200B; コネクテッド TV広告の設定](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [広告設定の表示](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [&#x200B; モバイル広告設定](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [&#x200B; ネイティブ広告設定](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [広告設定のプレロール &#x200B;](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [&#x200B; ユニバーサル動画広告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
