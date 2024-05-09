---
title: JavaScript コンバージョントラッキングタグバージョン 2 の形式
description: JavaScript 変換トラッキングタグバージョン 2 の形式を参照します。
exl-id: 75e96f97-a3f0-4f5b-8bbb-4b1e8986f01a
feature: Search Tracking
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# JavaScript コンバージョントラッキングタグバージョン 2 の形式

HTTPS を使用するサイトの場合は、次の形式になります。 HTTP を使用するサイトの場合、URL は「http」で始める必要があります。

>[!NOTE]
>
>バージョン 2 とバージョン 3 のどちらを使用するかについては、を参照してください。 [トラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
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

* `<ef-userid>` は、検索、ソーシャルおよびCommerceによって広告主に割り当てられる一意の数値ユーザー ID です。

* `<propertyname>` は、追跡するコンバージョンです。 例えば、「registration」というコンバージョンをトラッキングする場合、タグにはパラメーターが含まれます `ev_registration=<registration>`を選択し、取引ごとに実収益を渡す必要があります（例： `ev_registration=1`）に設定します。 複数のプロパティがトラッキングされる場合、それらのプロパティはアンパサンド（`&`）など `ev_registration=<registration>&ev_sale=<sale>` （例： `ev_registration=1&ev_sale=12.99`）に設定します。 **注意：**  プロパティ名に特殊文字を含めることはできません。

* `<transid>` は、広告主がトランザクションを識別するために生成して渡す一意のトランザクション ID （実際の注文 ID など）です。 が「」の場合にのみ含まれます[!UICONTROL Include unique transaction IDs]」オプションが選択されています。

  検索、ソーシャル、Commerceでは、トランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 トランザクション ID はに含まれます [!UICONTROL Transaction Report]を使用して、Adobe Advertising内のデータを広告主のデータで検証できます。 **注意：** 広告主のデータにトランザクションごとの一意の ID が含まれていない場合、検索、ソーシャルおよびCommerceでは、トランザクション時間に基づいて引き続き ID が生成されます。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグを生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](format-conversion-tag-jsv2.md)
>* [JavaScript コンバージョントラッキングタグバージョン 3 の形式](format-conversion-tag-jsv3.md)
>* [画像変換トラッキングタグの形式](format-conversion-tag-image.md)
