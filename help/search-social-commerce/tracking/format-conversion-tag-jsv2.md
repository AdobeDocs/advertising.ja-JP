---
title: JavaScript コンバージョントラッキングタグバージョン 2 の形式
description: JavaScript コンバージョントラッキングタグバージョン 2 のフォーマットを参照します。
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: f73e91c54fb58cbd165ddf4ca652033435fbbede
workflow-type: tm+mt
source-wordcount: '305'
ht-degree: 0%

---

# JavaScript コンバージョントラッキングタグバージョン 2 の形式

HTTPS を使用するサイトの場合は、次の形式になります。 HTTP を使用するサイトの場合、URL は「http」で始める必要があります。

>[!NOTE]
>
>バージョン 2 とバージョン 3 のどちらを使用するかについては、[ トラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md) を参照してください。

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
window.id5PartnerId=<Your_ID5_PartnerID>
var ef_event_type="transaction";
var ef_transaction_properties = "ev_property name=<property name>&ev_transid=<transid>";
/*
 * Do not modify below this line
 */
var ef_segment = "";
var ef_search_segment = "";
var ef_userid="ef-userid";
var ef_pixel_host="pixel.everesttech.net";
var ef_fb_is_app = 0;
var ef_allow_3rd_party_pixels = 1;
effp();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property name=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

ここで、

* `<ef-userid>` は、検索、ソーシャルおよびCommerceが広告主に割り当てる一意の数値ユーザー ID です。

* `<Your_ID5_PartnerID>` は、組織が [!DNL ID5] と契約を締結した後に受け取る、組織の ID5 パートナー ID です。 組織がDSPを使用し、[ID5 ユニバーサル ID に関連付けられたユーザーを追跡するカスタムセグメント ](/help/dsp/audiences/universal-ids.md) を持つ場合にのみ、この変数を含めます。

* `<propertyname>` は、追跡するコンバージョンです。 例えば、「登録」と呼ばれるコンバージョンをトラッキングする場合、タグにはパラメーター `ev_registration=<registration>` が含まれ、各トランザクションの実際の売上高（`ev_registration=1` など）を渡す必要があります。 複数のプロパティがトラッキングされる場合、それらのプロパティは、`ev_registration=<registration>&ev_sale=<sale>` などのアンパサンド（`&`）で結合されます（例：`ev_registration=1&ev_sale=12.99`）。 **注意：** プロパティ名に特殊文字を含めることはできません。

* `<transid>` は、トランザクションを識別するために広告主が生成して渡す一意のトランザクション ID （実際の注文 ID など）です。 「[!UICONTROL Include unique transaction IDs]」オプションが選択されている場合にのみ含まれます。

  検索、ソーシャル、Commerceでは、トランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 取引 ID は [!UICONTROL Transaction Report] に含まれ、広告主のデータを使用してAdobe Advertising内のデータを検証するために使用できます。 **メモ：** 広告主のデータにトランザクションごとの一意の ID が含まれていない場合、検索、ソーシャルおよびCommerceでは、トランザクション時間に基づいて引き続き ID が生成されます。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて ](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグを生成 ](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [ コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式 ](format-conversion-tag-jsv2.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式 ](format-conversion-tag-jsv3.md)
>* [ 画像変換トラッキングタグの形式 ](format-conversion-tag-image.md)
