---
title: のクリック追跡形式 [!DNL Microsoft Advertising]
description: のクリック追跡形式について説明します。 [!DNL Microsoft Advertising] アカウント。
exl-id: 725981db-1b9a-4c89-b95d-98d07ec99756
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '584'
ht-degree: 0%

---

# のクリック追跡形式 [!DNL Microsoft Advertising]

以下に、Search、Social および Commerce で必要となる基本トラッキングテンプレートおよびランディングページサフィックス（最終 URL サフィックス）の形式を示します。 [!DNL Microsoft Advertising].

## トラッキングテンプレート形式

### 検索およびオーディエンスネットワーク（サイトリンクを除く）

次の形式は、検索およびオーディエンスネットワーク上のすべての追跡可能な広告タイプに適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* `{TargetId}` は、キーワードの ID または b) 広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方の場合は「kwd-123:aud-456」、キーワードの場合は「kwd-123」）を表します。

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* `{TargetId}` は、キーワードの ID または b) 広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方の場合は「kwd-123:aud-456」、キーワードの場合は「kwd-123」）を表します。
>
>* `{adextensionid}` が未使用です。
>
>* （サイトリンク）サイトリンクを生成することで、サイトリンクのクリックによって生じたコンバージョンを確認できます。 [!UICONTROL Transaction Report]. The [!UICONTROL Link Type] サイトリンクの列の値は `sl:<Sitelink text>`、例： `sl:See Current Offers`.

### 買い物ネットワーク

ショッピングネットワークのショッピング広告には、次の形式が適用されます。 トラッキングテンプレートは、アカウント、キャンペーン、広告グループまたは製品グループレベルで指定できます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>` は、Adobe Advertising内の広告主の一意の ID の変数です。
>
>* この形式は、キャンペーンでトークンの受け渡しが有効（デフォルト）になっていることを示します。 トークンの受け渡しが無効な場合は、 `cq?` 次より後 `<advertiser_ID>` 次を使用 `c?`.
>
>* `{TargetId}` は、キーワードの ID または b) 広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）（例えば、キーワードとリマーケティングリストの両方の場合は「kwd-123:aud-456」、キーワードの場合は「kwd-123」）を表します。
>
>* （オプション）アカウント、キャンペーン、広告グループまたは製品グループレベルでトラッキングテンプレートを入力する代わりに、トラッキング URL を [!DNL Microsoft Merchant Center] アカウント。 これをおこなうには、トラッキング URL を`link`&quot;または&quot;`mobile_link`&quot;フィールドは、必要に応じて、カスタム列&quot;[bingads_redirect](https://help.bingads.microsoft.com/#apex/3/en/51084/0)」と入力します。 「`bingads_redirect`&quot;フィールドは、`link`&quot;および&quot;`mobile_link`」フィールドに値を入力します。 このメソッドを使用して生成される URL には、検索、ソーシャル、コマースのアカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

## ランディングページのサフィックス（最終 URL サフィックス）の形式

>[!NOTE]
>
>下位レベルでのランディングページのサフィックスは、アカウントレベルのサフィックスよりも優先されます。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して別々の追跡が必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

### 検索とオーディエンスネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別子 (`msclkid` 対象： [!DNL Microsoft Advertising]) を次のサフィックスに追加します。

* 広告主がAdobe Analytics統合をおこなう場合、サフィックスに次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{OrderItemId}`

* 広告主がAdobe Analytics統合を持たない場合、サフィックスに次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

### 買い物ネットワーク

Adobe Advertisingコンバージョントラッキングを使用するアカウントには、広告ネットワークのクリック識別子 (`msclkid` 対象： [!DNL Microsoft Advertising]) を次のサフィックスに追加します。

* 広告主がAdobe Analytics統合をおこなう場合、サフィックスに次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!{sid}!{AdId}!{CriterionId}`

* 広告主がAdobe Analytics統合を持たない場合、サフィックスに次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリック追跡 URL の形式について](formats-click-tracking-about.md)
>* [s\_kwcid トラッキングコードの形式](skwcid-tracking-parameter.md)
