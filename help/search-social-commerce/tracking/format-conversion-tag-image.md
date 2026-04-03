---
title: 画像変換トラッキングタグの形式
description: 画像変換トラッキングタグの形式を参照します。
exl-id: e23107e1-b719-4572-a471-13e51387465d
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TQMACo5-LkbCU2SiMmUE-ZDBRTb8NERQPQ9ISzU0DdU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 249
ht-degree: 0%

---

# 画像変換トラッキングタグの形式

>[!NOTE]
>
>画像タグとJavaScript タグの使用状況について詳しくは、「[&#x200B; トラッキングタグに関するFAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)」を参照してください。

* HTTPを使用するサイトの安全でないタグ：

  `<img src="http://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

* HTTPSを使用したサイトの安全なタグ：

  `<img src="https://pixel.everesttech.net/px2/<ef-userid>?px_evt=s&s=<segmentid>&px_evt=t&ev_propertyname=<propertyname>&ev_transid=<transid>" width="1" height="1"/>`

どこで：

* `<ef-userid>`は、Search、Social、およびCommerceが広告主に割り当てる一意の数値ユーザーIDです。

* `<propertyname>`は追跡するコンバージョンです。 例えば、「登録」というコンバージョンをトラッキングする場合、タグにはパラメーター`ev_registration=<registration>`が含まれ、各トランザクションの実際の収益（`ev_registration=1`など）を渡す必要があります。 複数のプロパティがトラッキングされると、アンパサンド （`&`）が結合されます（例：`ev_registration=<registration>&ev_sale=<sale>`）（例：`ev_registration=1&ev_sale=12.99`）。 **注意：** プロパティ名に特殊文字を含めることはできません。

* `<transid>`は、広告主が生成し、トランザクションを識別するために渡す一意のトランザクション ID （実際の注文IDなど）です。 「[!UICONTROL Include unique transaction IDs]」オプションが選択されている場合にのみ含まれます。

  Search, Social, &amp; Commerceでは、トランザクション IDを使用して、同じトランザクション IDとプロパティ値を持つ重複するトランザクションを除外します。 トランザクション IDは[!UICONTROL Transaction Report]に含まれており、広告主のデータでAdobe Advertising内のデータを検証するために使用できます。 **メモ：**&#x200B;広告主のデータにトランザクションごとに一意のIDが含まれていない場合、Search, Social, &amp; Commerceはトランザクション時間に基づいて1つを生成します。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertising コンバージョンタグを生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* コンバージョンとページビューのトラッキングタグに関する[FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2](format-conversion-tag-jsv2.md)の形式
>* [JavaScript コンバージョントラッキングタグバージョン 3](format-conversion-tag-jsv3.md)の形式
