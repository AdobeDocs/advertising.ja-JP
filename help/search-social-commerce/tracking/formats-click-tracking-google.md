---
title: のクリック追跡形式 [!DNL Google Ads]
description: のクリック追跡形式について説明します。 [!DNL Google Ads] アカウント。
exl-id: 68f6da43-3430-4c0a-9369-937fa52c071a
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '539'
ht-degree: 0%

---

# のクリック追跡形式 [!DNL Google Ads]

以下に、Search、Social および Commerce で必要となる基本トラッキングテンプレートおよびランディングページサフィックス（最終 URL サフィックス）の形式を示します。 [!DNL Google Ads].

## トラッキングテンプレート形式

### サイトリンクを含む検索/表示ネットワーク

次の形式は、検索およびディスプレイネットワーク上のすべての追跡可能な広告タイプ、およびサイトリンクに適用されます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_ln={keyword}&ev_lx={targetid}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={_evltx}&ev_pl={placement}&ev_pos={adposition}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* The [!DNL ValueTrack] トラッキングテンプレートの最終 URL を示すパラメーターは、次のいずれかである必要があります。 `{lpurl}` または `!{unescapedurl}`.
>
>* （テキスト広告）キーワードで入札する場合、 `ev_pl` （配置の場合）に値がありません。 配置で入札する場合、 `ev_ln` （キーワードの場合）に値がありません。 広告グループまたは他のディメンションで入札する場合、 `ev_ln` および `ev_pl` 値がありません。
>
>* （動的検索広告） `{keyword}` 動的検索ターゲット式を示します。例： `_cat:[VALUE]` または `_url:[VALUE]`.
>
>* （動的検索広告） [!DNL Google Ads] によって最終 URL が動的に決定されるので、URL を入力する必要はありません。
>
>* （サイトリンク）サイトリンクを生成することで、サイトリンクのクリックによって生じたコンバージョンを確認できます。 [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] サイトリンクの列の値は `sl:<Sitelink text>`、例： `sl:See Current Offers`.

### 買い物ネットワーク

次の形式は、ショッピングネットワークのショッピング広告および製品グループに適用されます。 トラッキングテンプレートは、アカウント、キャンペーン、広告グループまたは製品グループレベルで指定できます。

`https://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url={<Google ValueTrack parameter for the final URL>}`

例：

`https://pixel.everesttech.net/1234/cq?ev_sid=3&ev_lx={targetid}&ev_ln={keyword}&ev_pl={placement}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx={adtype}&ev_plx={product_id}&ev_ptid={product_partition_id}&ev_mid={merchant_id}&ev_cty={product_country}&ev_lan={product_language}&ev_dvc={device}&ev_dvm={devicemodel}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={campaignid}&ev_ax={adgroupid}&ev_efid={gclid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* The [!DNL ValueTrack] トラッキングテンプレートの最終 URL を示すパラメーターは、次のいずれかである必要があります。 `{lpurl}` または `!{unescapedurl}`.
>
>* [!DNL Google Ads] は、Google Merchant Center フィードの製品 URL を最終 URL として使用するので、製品データや製品グループの最終 URL を入力する必要はありません。
>
>* どのコンバージョンが、買い物広告のクリックによって生じたかを、 [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] 製品広告の列の値が pla の場合：`<product ID>`、例： `pla:8525822`.

## ランディングページのサフィックス（最終 URL サフィックス）の形式

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別子 (`gclid` 対象： [!DNL Google Ads]) を次のサフィックスに追加します。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスに次のいずれかを含める必要があります。

   * [!DNL Google Ads] 最新の `s_kwcid` 形式：最大パフォーマンスキャンペーンおよびドラフト&amp;実験キャンペーンのキャンペーンおよび広告グループレベルのレポートをサポートします。

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}`

     アカウントにサーバー側の s_kwcid 実装があり、アカウントまたはキャンペーン設定がある場合は、「[!UICONTROL Auto Upload]」が有効な場合、パラメーターは自動的に追加されます。 それ以外の場合は、手動で追加する必要があります。

   * その他すべて [!DNL Google Ads] アカウント：

     `ef_id={gclid}:G:s&s_kwcid=AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}`

* 広告主がAdobe Analytics統合を持たない場合、サフィックスに次を含める必要があります。

  `&ev_efid={gclid}:G:s`

>[!NOTE]
>
>* 下位レベルでのランディングページのサフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。
>
>* ( 動的検索広告、Adobe Analyticsを使用し、サーバーサイドトラッキングを使用しない広告主 )Adobe Advertisingから Analytics への逆フィードのトラッキングを含める場合、 `s_kwcid` トラッキングコードをアカウントレベルのランディングページサフィックスの最後に追加します。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [s\_kwcid トラッキングコードの形式](skwcid-tracking-parameter.md)
