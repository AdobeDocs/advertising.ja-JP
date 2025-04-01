---
title: ' [!DNL Google Ads] のクリック追跡形式'
description: アカウントのクリック追跡形式について説明  [!DNL Google Ads]  ます。
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 70629247a18a78b12a7fc8b166a0272764bb20b8
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%

---

# [!DNL Google Ads] のクリック追跡形式

検索、ソーシャル、Commerceでア [!DNL Google Ads] ットに必要な基本トラッキングテンプレートとランディングページのサフィックス（最終的な URL のサフィックス）の形式は次のとおりです。

## トラッキングテンプレート形式

### ネットワークの検索/表示（サイトリンクを含む）

次の形式は、検索および表示ネットワーク上のすべての追跡可能な広告タイプと、サイトリンクに適用されます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内での広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* トラッキングテンプレート内の最終 URL を示す [!DNL ValueTrack] のパラメーターは、`{lpurl}` または `!{unescapedurl}` にする必要があります。
>
>* （テキスト広告）キーワードで入札する場合、（プレースメントの）パラメーター `ev_pl` には値がありません。 プレースメントで入札する場合、`ev_ln` （キーワードの場合）には値がありません。 広告グループまたは他のディメンションで入札する場合、`ev_ln` と `ev_pl` の両方に値がありません。
>
>* （動的検索広告） `{keyword}` 動的検索ターゲット式（`_cat:[VALUE]`、`_url:[VALUE]` など）を示します。
>
>* （動的検索広告）最終的 [!DNL Google Ads]URL は動的に決定されるので、入力する必要はありません。
>
>* （サイトリンク） [!UICONTROL Transaction Report] ータを生成することで、サイトリンクのクリックによって生じたコンバージョンを確認できます。 サイトリンクの [!UICONTROL Link Type] 列の値は `sl:<Sitelink text>` です（例：`sl:See Current Offers`）。

### ショッピングネットワーク

次の形式は、ショッピングネットワークのショッピング広告および商品グループに適用されます。 追跡テンプレートは、アカウント、キャンペーン、広告グループまたは製品グループのレベルで指定できます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内での広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* トラッキングテンプレート内の最終 URL を示す [!DNL ValueTrack] のパラメーターは、`{lpurl}` または `!{unescapedurl}` にする必要があります。
>
>* [!DNL Google Ads] は、Google マーチャントセンターフィードの商品 URL を最終的な URL として使用するので、商品データや商品グループの最終的な URL を入力する必要はありません。
>
>* [!UICONTROL Transaction Report] ールを生成することで、買い物かごの広告をクリックした結果、どのコンバージョンが生じたかを確認できます。 製品広告の [!UICONTROL Link Type] 列の値は pla:`<product ID>` です（例：`pla:8525822`）。

## ランディングページのサフィックス（最終的な URL のサフィックス）の形式

Adobe Advertising コンバージョントラッキングを使用するアカウントの場合は、アドネットワークのクリック識別子（[!DNL Google Ads] の `gclid`）をサフィックスに含める必要があります。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスには次のいずれかを含める必要があります。

   * 最新の [AMO ID 形式 ](/help/integrations/analytics/ids.md#amo-id-formats) （`s_kwcid` で始まる）を使用する [!DNL Google Ads] アカウントで、パフォーマンス最大化キャンペーンおよびドラフト/実験キャンペーンに関するキャンペーンおよび広告グループレベルのレポートをサポートします。

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     アカウントにサーバーサイド AMO ID 実装があり、アカウントまたはキャンペーン設定の「[!UICONTROL Auto Upload]」が有効になっている場合、パラメーターは自動的に追加されます。 そうでない場合は、手動で追加する必要があります。 「[ ユーザーのAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md#amo-id-implement)」を参照してください。

   * その他すべての [!DNL Google Ads] アカウント：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* 広告主がAdobe Analytics統合を持っていない場合、サフィックスには次を含める必要があります。

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* 下位レベルのランディングページのサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
>
>* （動的検索広告、Adobe Analyticsを使用しサーバーサイドトラッキングを使用しない広告主）Adobe Advertisingから Analytics へのリバースフィードのトラッキングを含める場合は、アカウントレベルのランディングページサフィックスの末尾に AMO ID トラッキングコードを追加します。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL 形式について ](formats-click-tracking-about.md)
>* [AMO ID 形式 ](/help/integrations/analytics/ids.md#amo-id-formats)
