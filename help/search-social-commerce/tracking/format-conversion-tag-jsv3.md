---
title: JavaScript コンバージョントラッキングタグバージョン 3 の形式
description: JavaScript コンバージョントラッキングタグバージョン 3 の形式を参照してください。
exl-id: 1e177c52-f93c-4800-afb5-28f2336117b9
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 0%

---

# JavaScript コンバージョントラッキングタグバージョン 3 の形式

次の形式は、HTTPS を使用するサイト向けです。 HTTP を使用するサイトの場合、URL は「http」で始まる必要があります。

>[!NOTE]
>
>バージョン 2 とバージョン 3 の使用について詳しくは、 [トラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md).

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

場所：

* `<ef-userid>` は、Search、Social および Commerce が広告主に割り当てる一意の数値ユーザー ID です。

* `<propertyname>` は、追跡されるコンバージョンです。 例えば、「登録」と呼ばれるコンバージョンを追跡している場合、タグにはパラメーターが含まれます `ev_registration=<registration>`を渡す場合は、各トランザクションの実際の売上高 ( `ev_registration=1`) をクリックします。 複数のプロパティを追跡する場合、それらのプロパティはアンパサンド (`&`など ) `ev_registration=<registration>&ev_sale=<sale>` ( 例： `ev_registration=1&ev_sale=12.99`) をクリックします。 **注意：**  プロパティ名に特殊文字を含めることはできません。

* `<transid>` は、トランザクションを識別するために広告主が生成して渡す一意のトランザクション ID（実際の注文 ID など）です。 これは、「[!UICONTROL Include unique transaction IDs]」オプションが選択されています。

  検索、ソーシャル、コマースでは、トランザクション ID を使用して、同じトランザクション ID とプロパティ値を持つ重複トランザクションを排除します。 トランザクション ID は [!UICONTROL Transaction Report]：広告主のデータとのAdobe Advertising内でデータを検証するために使用できます。 **注意：** 広告主のデータにトランザクションごとの一意の ID が含まれていない場合、検索、ソーシャル、コマースは引き続きトランザクション時間に基づいて ID を生成します。

<!-- add more links -->

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのコンバージョントラッキングタグについて](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)
>* [Adobe Advertisingコンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [コンバージョンおよびページビューのトラッキングタグに関する FAQ](/help/search-social-commerce/tracking/faqs-conversion-page-view-tracking-tags.md)
>* [JavaScript コンバージョントラッキングタグバージョン 2 の形式](format-conversion-tag-jsv2.md)
>* [画像コンバージョントラッキングタグの形式](format-conversion-tag-image.md)
