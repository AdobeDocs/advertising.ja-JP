---
title: ' [!DNL Google Ads]のクリックトラッキング形式'
description: ' [!DNL Google Ads]  アカウントのクリックトラッキング形式について説明します。'
exl-id: d09c3b4e-1274-45fb-abb6-dddfe60f1477
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# [!DNL Google Ads]のクリックトラッキング形式

次に、Search、Social、およびCommerceで[!DNL Google Ads]に必要な基本トラッキングテンプレートとランディングページのサフィックス（最終URL サフィックス）形式を示します。

## テンプレート形式のトラッキング

### サイトリンクを含む検索/表示ネットワーク

次の形式は、検索および表示ネットワーク上のすべての追跡可能な広告タイプ、およびサイトリンクに適用されます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* トラッキングテンプレートの最終的なURLを示す[!DNL ValueTrack] パラメーターは、`{lpurl}`または`!{unescapedurl}`である必要があります。
>
>* （テキスト広告）キーワードで入札する場合、パラメーター`ev_pl` （プレースメント用）に値がありません。 プレースメントで入札する場合、`ev_ln` （キーワード用）には値がありません。 広告グループまたは他のディメンションで入札すると、`ev_ln`と`ev_pl`の両方に値がありません。
>
>* （動的検索広告） `{keyword}`は、`_cat:[VALUE]`や`_url:[VALUE]`などの動的検索ターゲット式を示します。
>
>* （動的検索広告） [!DNL Google Ads]は最終的なURLを動的に決定するので、入力する必要はありません。
>
>* （サイトリンク） [!UICONTROL Transaction Report]を生成すると、サイトリンクをクリックした結果のコンバージョンを確認できます。 サイトリンクの[!UICONTROL Link Type]列の値は`sl:<Sitelink text>`など`sl:See Current Offers`です。

### ショッピングネットワーク

次の形式は、ショッピングネットワーク内のショッピング広告と商品グループに適用されます。 トラッキングテンプレートは、アカウントレベル、キャンペーンレベル、広告グループレベル、製品グループレベルで指定できます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* トラッキングテンプレートの最終的なURLを示す[!DNL ValueTrack] パラメーターは、`{lpurl}`または`!{unescapedurl}`である必要があります。
>
>* [!DNL Google Ads]は、Google Merchant Center フィードの商品URLを最終的なURLとして使用するので、商品データまたは商品グループの最終的なURLを入力する必要はありません。
>
>* [!UICONTROL Transaction Report]を生成すると、ショッピング広告をクリックした結果のコンバージョンを確認できます。 製品広告の[!UICONTROL Link Type]列の値は、`<product ID>`など、プラン：`pla:8525822`です。

## ランディングページサフィックス（最終URL サフィックス）形式

Adobe Advertising コンバージョントラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック ID （`gclid`の[!DNL Google Ads]）を含める必要があります。

* 広告主がAdobe Analytics統合を持っている場合、接尾辞には次のいずれかを含める必要があります。

   * パフォーマンスの最大キャンペーン、ドラフト、および実験キャンペーンのキャンペーンレベルおよび広告グループレベルのレポートをサポートする最新の[!DNL Google Ads]AMO ID形式[&#x200B; （](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)から始まる）を使用する`s_kwcid` アカウント：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     アカウントにサーバーサイド AMO ID実装があり、アカウントまたはキャンペーン設定「[!UICONTROL Auto Upload]」が有効になっている場合、パラメーターが自動的に追加されます。 それ以外は、手動で追加する必要があります。 「[&#x200B; [!DNL Analytics]様が使用するAdobe Advertising ID &#x200B;](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id-implement)を参照してください。」

   * その他[!DNL Google Ads] アカウントすべて：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* 広告主がAdobe Analyticsとの統合を持っていない場合、接尾辞には次を含める必要があります。

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* 下位レベルのランディングページサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
>
>* （動的検索広告、Adobe Analyticsを持つ広告主、サーバーサイドトラッキングを持たない広告主）Adobe AdvertisingからAnalyticsへのリバースフィードのトラッキングを含める場合は、アカウントレベルのランディングページサフィックスの最後にAMO ID トラッキングコードを追加します。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)
