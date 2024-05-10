---
title: のクリック追跡形式 [!DNL Microsoft Advertising]
description: のクリック追跡形式について説明します [!DNL Microsoft Advertising] アカウント。
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# のクリック追跡形式 [!DNL Microsoft Advertising]

検索、ソーシャル、Commerceで必要となる、基本トラッキングテンプレートとランディングページのサフィックス（最終的な URL サフィックス）の形式は次のとおりです [!DNL Microsoft Advertising].

## トラッキングテンプレート形式

### 検索とオーディエンスネットワーク（サイトリンクを除く）

次の形式は、検索およびオーディエンスネットワーク上のすべての追跡可能な広告タイプに適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、を置き換える `cq?` 後 `<advertiser_ID>` （を使用） `c?`.
>
>* `{TargetId}` a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス） （例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、を置き換える `cq?` 後 `<advertiser_ID>` （を使用） `c?`.
>
>* `{TargetId}` a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス） （例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。
>
>* `{adextensionid}` が未使用である。
>
>* （サイトリンク）サイトリンクをクリックした結果のコンバージョンを、次のコードを生成することで確認できます。 [!UICONTROL Transaction Report]. この [!UICONTROL Link Type] サイトリンクの列の値は `sl:<Sitelink text>`（例：） `sl:See Current Offers`.

### ショッピングネットワーク

ショッピングネットワークのショッピング広告には、次の形式が適用されます。 追跡テンプレートは、アカウント、キャンペーン、広告グループまたは製品グループのレベルで指定できます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、を置き換える `cq?` 後 `<advertiser_ID>` （を使用） `c?`.
>
>* `{TargetId}` a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス） （例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。
>
>* （任意）アカウント、キャンペーン、広告グループ、製品グループの各レベルでトラッキングテンプレートを入力する代わりに、内の製品データにトラッキング URL を追加できます。 [!DNL Microsoft Merchant Center] アカウント。 これをおこなうには、トラッキング URL を値とともに「」に含めます`link`「または」`mobile_link`「フィールド（必要に応じて、カスタム列で）」[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)製品フィード内。 「」の値`bingads_redirect`「」フィールドは「」の値を置き換えます`link`「」と「」に対して検査する値`mobile_link`」フィールドに入力します。 この方法で生成される URL には、検索、ソーシャル、Commerceの各アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

## ランディングページのサフィックス（最終的な URL のサフィックス）の形式

>[!NOTE]
>
>下位レベルのランディングページのサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

### 検索とオーディエンスネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別情報（`msclkid` （用） [!DNL Microsoft Advertising]）を使用する必要があります。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスには次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 広告主がAdobe Analytics統合を持っていない場合、サフィックスには次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

### ショッピングネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別情報（`msclkid` （用） [!DNL Microsoft Advertising]）を使用する必要があります。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスには次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 広告主がAdobe Analytics統合を持っていない場合、サフィックスには次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について](formats-click-tracking-about.md)
>* [AMO ID 形式](/help/integrations/analytics/ids.md#amo-id-formats)
