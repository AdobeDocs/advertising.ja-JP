---
title: ' [!DNL Microsoft Advertising]のクリックトラッキング形式'
description: ' [!DNL Microsoft Advertising]  アカウントのクリックトラッキング形式について説明します。'
exl-id: 4970ac33-4978-4768-8701-6fdd3252bbd1
feature: Search Tracking
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 0%

---

# [!DNL Microsoft Advertising]のクリックトラッキング形式

次に、Search、Social、およびCommerceで[!DNL Microsoft Advertising]に必要な基本トラッキングテンプレートとランディングページのサフィックス（最終URL サフィックス）形式を示します。

## テンプレート形式のトラッキング

### 検索およびオーディエンスネットワーク （サイトリンクを除く）

次の形式は、検索およびオーディエンスネットワーク上で追跡可能なすべての広告タイプに適用されます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `{TargetId}`は、a）キーワードまたはb）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）のIDを表します（例えば、キーワードとリマーケティングリストの両方に「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」など）。

### Sitelinks

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_ln={keyword}&ev_ltx={_evltx}&ev_lx={TargetId}&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_cx={CampaignId}&ev_ax={AdGroupId}&ev_ex={adextensionid}&ev_efid={msclkid}:G:s&url={lpurl}`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `{TargetId}`は、a）キーワードまたはb）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）のIDを表します（例えば、キーワードとリマーケティングリストの両方に「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」など）。
>
>* `{adextensionid}`は未使用です。
>
>* （サイトリンク） [!UICONTROL Transaction Report]を生成すると、サイトリンクをクリックした結果のコンバージョンを確認できます。 サイトリンクの[!UICONTROL Link Type]列の値は`sl:<Sitelink text>`など`sl:See Current Offers`です。

### ショッピングネットワーク

次の形式は、ショッピングネットワークでのショッピング広告に適用されます。 トラッキングテンプレートは、アカウントレベル、キャンペーンレベル、広告グループレベル、製品グループレベルで指定できます。

`http://pixel.everesttech.net/<advertiser_ID>/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url={lpurl}`

例：

`http://pixel.everesttech.net/1234/cq?ev_sid=10&ev_crx={AdId}&ev_mt={MatchType}&ev_dvc={device}&ev_plx={ProductId}&ev_ptid={CriterionId}&ev_phy={loc_physical_ms}&ev_loc={loc_interest_ms}&ev_ex={feeditemid}&ev_efid={msclkid}:G:s&url=http%3A//www.example.com`

>[!NOTE]
>
>* `<advertiser_ID>`は、Adobe Advertising内の広告主の一意のIDの変数です。
>
>* この形式は、キャンペーンに対してトークン渡しが有効になっていることを示します（デフォルト）。 トークンの渡しが無効な場合は、`cq?`の後の`<advertiser_ID>`を`c?`に置き換えます。
>
>* `{TargetId}`は、a）キーワードまたはb）広告をトリガーしたキーワードおよびリマーケティングリスト（オーディエンス）のIDを表します（例えば、キーワードとリマーケティングリストの両方に「kwd-123:aud-456」、キーワードのみの場合は「kwd-123」など）。
>
>* （オプション）アカウント、キャンペーン、広告グループ、または製品グループレベルでトラッキングテンプレートを入力する代わりに、[!DNL Microsoft Merchant Center] アカウント内の製品データにトラッキング URLを追加できます。 これを行うには、トラッキング URLを、必要に応じて製品フィード内のカスタム列「`link`bingads_redirect`mobile_link`」に「[」または「](https://help.bingads.microsoft.com/#apex/3/en/51084/0)」フィールドの値と共に含めます。 「`bingads_redirect`」フィールドの値は、「`link`」および「`mobile_link`」フィールドの値に置き換わります。 この方法で生成されたURLには、Search, Social, &amp; Commerce アカウントまたはキャンペーン設定で指定されたトラッキングパラメーターが含まれていません。

## ランディングページサフィックス（最終URL サフィックス）形式

>[!NOTE]
>
>下位レベルのランディングページサフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、広告ネットワークのエディターを使用します。

### 検索およびオーディエンスネットワーク

Adobe Advertising コンバージョントラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック ID （`msclkid`の[!DNL Microsoft Advertising]）を含める必要があります。

* 広告主がAdobe Analytics統合を持っている場合、接尾辞には次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{OrderItemId}`

* 広告主がAdobe Analyticsとの統合を持っていない場合、接尾辞には次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

### ショッピングネットワーク

Adobe Advertising コンバージョントラッキングを使用するアカウントでは、サフィックスに広告ネットワークのクリック ID （`msclkid`の[!DNL Microsoft Advertising]）を含める必要があります。

* 広告主がAdobe Analytics統合を持っている場合、接尾辞には次を含める必要があります。

  `ef_id={msclkid}:G:s&s_kwcid=AL!{userid}!10!{AdId}!{CriterionId}`

* 広告主がAdobe Analyticsとの統合を持っていない場合、接尾辞には次を含める必要があります。

  `&ev_efid={msclkid}:G:s`

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](formats-click-tracking-about.md)
>* [AMO ID形式](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id#dimension-items)
