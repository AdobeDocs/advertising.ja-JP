---
title: Advertising DSP マクロ
description: 一般的なトラッキングと、サードパーティのディスプレイ広告でのクリックの追跡に使用できるマクロを参照します。
feature: DSP Ads
exl-id: 7058c988-c544-4a61-84dd-eec4ce88ceba
source-git-commit: 195e75386e64c3659d3f4db3c2508ac903e9e311
workflow-type: tm+mt
source-wordcount: '940'
ht-degree: 0%

---

# Advertising DSP マクロ

マクロは、命令の短いコマンドまたは略記法で、通常は書式 `${MACRO_NAME}` に従います。 クリエイティブコードまたはクリックスルー URL に含まれるマクロは、広告サーバーが理解できる長いコード文字列に展開されます。 DSP広告サーバーは、広告が提供またはクリックされるとマクロを実行します。

広告サーバーマクロは、DSPまたはサードパーティの広告サーバーに重要な情報を渡す場合に役立ちます。 マクロは、サードパーティおよびカスタムクリエイティブコードやメタデータ（サードパーティのピクセルなど）のトラフィック処理時に最も一般的に使用されます。

マクロは、VAST タグ、URL、DSPまたはサードパーティのイベントピクセルなど、任意の場所に手動で挿入できます。 ただし、DSP クライアントとパートナーによって広告タグの形式が異なるので、それに応じてマクロをタグの異なる場所に挿入する必要があります。 新しいクライアントまたはパートナーと仕事をするたびに、DSP トラフィックを実行する広告タグにマクロを挿入する場所に関するドキュメントを求めます。

## 一般的なトラッキングマクロ

必要に応じて、すべての広告タイプおよびタグタイプで一般的なトラッキングマクロを使用して、特定のデータを返します。

| マクロ | 置き換えの説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_ACCOUNT_ID}` | アカウント ID。 | 整数 |
| `${TM_AD_ID}` | 広告キー（adKey）。 | string |
| `${TM_AD_ID_NUM}` | 広告 ID。 | 整数 |
| `${TM_ADVERTISER_ID}` | 広告主 ID。 | 整数 |
| `${TM_CAMPAIGN_ID}` | キャンペーンキー | string |
| `${TM_CAMPAIGN_ID_NUM}` | キャンペーン ID。 | 整数 |
| ` ${TM_CLICK_URL}` | リダイレクト URL は、広告サーバーが広告クリックを追跡およびカウントできるようにします。 広告が配信されると、ユーザーがクリックすると、マクロがアクティブ化され、クリックが記録され、レポート目的でカウントされます。 | string |
| ` ${TM_CLICK_URL_URLENC}` | エンコードされたリダイレクト URL により、広告サーバーは広告の追跡およびクリック数のカウントが可能になります。 広告が配信されると、ユーザーがクリックすると、マクロがアクティブ化され、クリックが記録され、レポート目的でカウントされます。 サードパーティの広告を作成し、ベンダーが URL エンコーディングを必要とする場合以外は、このマクロを使用しないでください。 | string |
| `${TM_FEED_ID}` | メディアプレースメントのキー（feedKey）。 | string |
| `${TM_FEED_ID_NUM}` | メディアプレースメントの ID。 | 整数 |
| ` ${TM_MACRO_PLACEMENT_SITE_KEY` | プレースメントのサイトキー。 モバイルアプリインストール広告の [!DNL AppsFlyer] クリックトラッカーに必要です。<!-- should map to placement_site_key column of placement_site table --> | string |
| `${TM_PLACEMENT_ID}` | 配置キー（cpKey）。 | string |
| `${TM_PLACEMENT_ID_NUM}` | プレースメント ID。 | 整数 |
| `${TM_RANDOM}` | Cachebuster: 1 から 1000000 の間の乱数。 | long |
| `${TM_SESSION_ID}` | セッションの ID。広告タグの 1 回の取得に対応します。 | string |
| `${TM_SITE_DOMAIN_URLENC}` | 入札要求内の URL から解析されるページサブドメイン。URL はエンコードされます。 バナー内、クリックして再生する広告には対応していません。 | string |
| ` ${TM_SITE_NAME}` | プレースメントのサイト名。 | string |
| `${TM_SITE_URL_URLENC}` | 入札要求で渡される URL。URL はエンコードされます。 バナー内、クリックして再生する広告には対応していません。 | string |
| `${TM_SITE_ID_NUM}` | プレースメントのサイト ID。 | 整数 |
| `${TM_TIMESTAMP}` | 1970 年 1 月 1 日の午前 0 時（00:00 UTC）からの経過秒数を示す Unix タイムスタンプ。 | long |
| ` ${TM_VIDEO_DURATION}` | 広告ビデオのデュレーション （秒）。 | 整数 |

{style="table-layout:auto"}

<!-- Removed because not found in code base:
|` ${TM_MACRO_PROMOTED_AD_KEY}` | The promoted ad key for the placement. Required for [!DNL AppsFlyer] click trackers for mobile app install ads. | string |
 -->

## モバイル固有のマクロ

| マクロ | 置き換えの説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${CS_PLATFORM_ID}` | （[!DNL ComScore]） プラットフォーム ID。これは、デバイスのオペレーティングシステムに対応します。<ul><li>`ios` = [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>プラットフォームが上記のいずれでもない場合に `other` 行</li></ul> | varchar （50） |
| `${CS_DEVICE_MODEL}` | （[!DNL ComScore]）デバイスモデル名（URL エンコード）。 | string |
| `${CS_IMPLEMENTATION_TYPE}` | [!DNL ComScore] 広告の提供を受けた環境<ul><li>`a` = モバイルアプリケーション</li><li>`b` = モバイル web サイト</li></ul> | 文字列（`a` または `b`） |
| `${NS_PLATFORM_ID}` | （[!DNL Nielsen]） プラットフォーム ID。これは、デバイスのオペレーティングシステムに対応します。<ul><li>`ios`= [!DNL Apple iOS]</li><li>`android` = [!DNL Google Android]</li><li>`windows` = [!DNL Windows Mobile]</li><li>`blackberry` = [!DNL Blackberry]</li> <li>プラットフォームが上記のいずれでもない場合に `other` 行</li></ul> | string |
| `${NS_DEVICE_GROUPING}` | （[!DNL Nielsen]）広告が閲覧者だったデバイスの種類：<ul><li>`TAB` = タブレット</li><li>`PHN` = モバイル</li><li>`computer` = コンピュータ</li></ul> | string |
| `${UOO}` | （[!DNL Nielsen]）ユーザーが広告トラッキングをオプトアウトしたかどうか：<ul><li>`1` （DNT flag = 1） = ユーザーは広告トラッキングをオプトアウトしました</li><li>`0` （DNT flag = 0） = ユーザーが広告トラッキングをオプトインしました</li></ul> | 整数（`0` または `1`） |
| `${TM_BUNDLE}` | [!DNL iOS] または [!DNL Android] App Store バンドル ID。 例：com.zynga.wwf2.free または id804379658 | string |
| `gdpr=${GDPR_ENFORCED}&gdpr_consent=${GDPR_CONSENT}` | `gdpr=${GDPR_ENFORCED}` は、入札者が入札要求が欧州連合（EU）の起源からのものであると判断し、GDPR の実施を必要とするかどうかを示します。<ul><li>`1` = GDPR を適用する必要があります</li><li>`0` = GDPR は適用されない</li></ul>`gdpr_consent=${GDPR_CONSENT}` は、インバウンド入札要求でサプライ・パートナーから渡される同意値です。<ul><li>ほとんどの場合、これは base64url エンコードされた同意文字列、つまり daisybit です（例：BN5lERiOMYEdiAKAWXEND1HoSBE6CAFAApAMgBkIDIgM0AgOJxAnQA）</li><li>`0` =同意なし</li><li>`1` =同意</li></ul> | デイジー・ビットまたは整数 |

{style="table-layout:auto"}

## サードパーティのディスプレイ広告用のマクロをクリックします

サードパーティのディスプレイタグを使用した広告のクリックを正確に追跡するために、DSPでは表示クリックマクロが必要です。 必要なマクロのバージョンは 1 つだけです。関連するマクロは、タグのタイプによって異なります。

| マクロ | 置き換えの説明 | タイプ |
| ----- | ----------------------- | ---- |
| `${TM_CLICK_URL}` | 広告サーバーがプラットフォームで広告クリックを追跡およびカウントできるようにするリダイレクト URL。 | string |
| `${TM_CLICK_URL_URLENC}` | URL エンコーディングを必要とする広告サーバーが、プラットフォームで広告クリックを追跡およびカウントできるリダイレクト URL です。 | string |

{style="table-layout:auto"}

DSPは、次の場合に、表示クリックマクロをサードパーティの表示タグに自動的に挿入します。

* 広告サーバーのパートナーインスタンスからの広告タ <!-- [Needs PM confirmation.] --> の書き出し
* DSPで直接 [!DNL Flashtalking] または [!DNL Google DoubleClick for Advertisers] の広告タグを一括アップロード

ディスプレイ広告を作成する際にクリックマクロが見つからない場合、DSPは警告メッセージを表示し、タグの適切な領域に適切な表示クリックマクロを手動で挿入するよう求められます。

## [!DNL Analytics for Advertising] マクロ

[[!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) のユーザー専用の追加マクロについては、「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Flashtalking]  広告タグに ](/help/integrations/analytics/macros-flashtalking.md)」および「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Google Campaign Manager 360]  広告タグに ](/help/integrations/analytics/macros-google-campaign-manager.md)」を参照してください。

## マクロエラーのトラブルシューティング

コードにマクロを追加する場合は、マクロの正確な構文を使用してください。 マクロを検証する場合、DSPはマクロが有効なマクロの 1 つと完全に一致することを確認します。

マクロ名の先頭または末尾に文字がない場合は、エラーが発生します。 例えば、次の場合にエラーメッセージが表示されます。

* マクロ名の先頭の文字（`${` など）を 1 つ以上忘れた場合。 完全な構文が含まれていない場合、そのエントリは有効なマクロとして認識されません。
* マクロの末尾が有効な文字セット （`}` など）になっていません。

>[!MORELIKETHIS]
>
>* [ オーディオ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-audio.md)
>* [ 接続されたテレビ広告の設定 ](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)
>* [ 広告設定を表示 ](/help/dsp/campaign-management/ads/ad-settings-display.md)
>* [ モバイル広告設定 ](/help/dsp/campaign-management/ads/ad-settings-mobile.md)
>* [ ネイティブ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-native.md)
>* [ プリロール広告設定 ](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)
>* [ ユニバーサルビデオ広告設定 ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)
