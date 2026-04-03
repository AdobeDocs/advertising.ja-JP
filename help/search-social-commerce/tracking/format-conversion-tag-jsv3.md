---
title: JavaScript コンバージョントラッキングタグバージョン 3のフォーマット
description: JavaScript コンバージョントラッキングタグバージョン 3のフォーマットを参照してください。
exl-id: 9fc6bb15-d880-4353-a8c5-260b7932ab34
feature: Search Tracking
TQID: https://experienceleague.adobe.com/IjPpsTp5GGaG6SM2k1UC0Q0J3QCF-jIR7-ug3yigW3U
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 297
ht-degree: 0%

---

# JavaScript コンバージョントラッキングタグバージョン 3のフォーマット

HTTPSを使用するサイトの形式は次のとおりです。 HTTPを使用するサイトの場合、URLは「http」で始まる必要があります。

>[!NOTE]
>
>バージョン 2とバージョン 3を使用するタイミングについて詳しくは、トラッキングタグに関する[FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)を参照してください。

```
<script type='text/javascript'>
    (function() {
        var f = function() {
              EF.init({ eventType: "transaction",
                        transactionProperties : "ev_property=<property name>&ev_transid=<transid>",
                        segment : "",
                        searchSegment : "",
                        sku : "",
                        userid : "ef-userid",
                        pixelHost : "pixel.everesttech.net"
                        
                        , allow3rdPartyPixels: 1});
              EF.main();
        };
        window.id5PartnerId=<ID5_PartnerID>
        window.EF = window.EF || {};
        if (window.EF.main) {
            f();
            return;
        }
        window.EF.onloadCallbacks = window.EF.onloadCallbacks || [];
        window.EF.onloadCallbacks[window.EF.onloadCallbacks.length] = f;
        if (!window.EF.jsTagAdded) {
            var efjs = document.createElement('script'); efjs.type = 'text/javascript'; efjs.async = true;
            efjs.src = 'https://www.everestjs.net/static/st.v3.js';
            var s = document.getElementsByTagName('script')[0]; s.parentNode.insertBefore(efjs, s);
            window.EF.jsTagAdded=1;
        }
    })();
</script>
<noscript><img src="https://pixel.everesttech.net/<ef-userid>/t?ev_property=<property name>&ev_transid=<transid>" width="1" height="1"/></noscript>
```

どこで：

* `<ef-userid>`は、Search、Social、およびCommerceが広告主に割り当てる一意の数値ユーザーIDです。

* `<ID5_PartnerID>`は組織のID5 パートナーIDで、組織は[!DNL ID5]との契約書に署名した後に受信します。 この変数は、組織がDSPを使用しており、ID5のユニバーサル ID[に関連付けられたユーザーを追跡する](/help/dsp/audiences/universal-ids.md) カスタムセグメントがある場合にのみ含めます。

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
>* [画像コンバージョントラッキングタグの形式](format-conversion-tag-image.md)
