---
title: ' [!DNL Microsoft Advertising] のクリック追跡形式'
description: アカウントのクリック追跡形式について説明  [!DNL Microsoft Advertising]  ます。
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] のクリック追跡形式

検索、ソーシャル、Commerceでア [!DNL Microsoft Advertising] ットに必要な基本トラッキングテンプレートとランディングページのサフィックス（最終的な URL のサフィックス）の形式は次のとおりです。

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
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `{TargetId}` は、a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `{TargetId}` は、a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。
>
>* `{adextensionid}` は未使用です。
>
>* （サイトリンク） [!UICONTROL Transaction Report] ータを生成することで、サイトリンクのクリックによって生じたコンバージョンを確認できます。 サイトリンクの [!UICONTROL Link Type] 列の値は `sl:<Sitelink text>` です（例：`sl:See Current Offers`）。

### ショッピングネットワーク

ショッピングネットワークのショッピング広告には、次の形式が適用されます。 追跡テンプレートは、アカウント、キャンペーン、広告グループまたは製品グループのレベルで指定できます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンに対してトークン受け渡しが有効になっている（デフォルト）ことを示します。 トークン受け渡しが無効な場合、`<advertiser_ID>` の後に `cq?` を `c?` で置き換えます。
>
>* `{TargetId}` は、a）キーワードまたは b）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方で「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」）の ID を表します。
>
>* （任意）アカウントレベル、キャンペーンレベル、広告グループレベルまたは製品グループレベルでトラッキングテンプレートを入力する代わりに、トラッキング URL を [!DNL Microsoft Merchant Center] アカウント内の製品データに追加できます。 これを行うには、トラッキング URL を、必要に応じて「`link`」または「`mobile_link`」フィールドの値と共に、製品フィード内のカスタム列「[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)」に含めます。 「`bingads_redirect`」フィールドの値は、「`link`」および「`mobile_link`」フィールドの値を置き換えます。 この方法で生成される URL には、検索、ソーシャル、Commerceの各アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

## ランディングページのサフィックス（最終的な URL のサフィックス）の形式

>[!NOTE]
>
>下位レベルのランディングページのサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要な場合を除き、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

### 検索とオーディエンスネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントの場合は、アドネットワークのクリック識別子（[!DNL Microsoft Advertising] の `msclkid`）をサフィックスに含める必要があります。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスには次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 広告主がAdobe Analytics統合を持っていない場合、サフィックスには次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

### ショッピングネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントの場合は、アドネットワークのクリック識別子（[!DNL Microsoft Advertising] の `msclkid`）をサフィックスに含める必要があります。

* 広告主がAdobe Analytics統合を使用する場合、サフィックスには次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 広告主がAdobe Analytics統合を持っていない場合、サフィックスには次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について ](formats-click-tracking-about.md)
>* [AMO ID 形式 ](/help/integrations/analytics/ids.md#amo-id-formats)
