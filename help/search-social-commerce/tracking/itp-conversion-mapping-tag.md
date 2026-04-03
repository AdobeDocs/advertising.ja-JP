---
title: Adobe Advertising コンバージョンマッピングタグ
description: Adobe Advertisingがランディングページ以外のページで発生するコンバージョンイベントをトラッキングできるITP 2.2のJavaScript ベースのコンバージョンマッピングタグについて説明します。
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
TQID: https://experienceleague.adobe.com/gG9j9kbctKTam6mhevTy4jTf7f68iy26XQW5dDjd-ZA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 637
ht-degree: 0%

---

# Adobe Advertising JavaScriptのコンバージョンマッピングタグ

*Adobe Advertising コンバージョントラッキングのみを使用する広告主*

Adobe Advertising JavaScript ベースのコンバージョンマッピングタグを、Adobe Advertising JavaScript v2またはv3 コンバージョントラッキングタグに加えて使用すると、Adobe Advertisingは、ランディングページではないページで発生するコンバージョンイベントをトラッキングできます。 ITP 2.2 ソリューションは、ユーザーのCookieを広告主所有のiFrameのローカルストレージに保存します。 次に、ローカルストレージは、クリックのダウンストリームからコンバージョンページまでCookie値を保持できます。

コンバージョンマッピングタグを使用して、Adobe AdvertisingがApple SafariおよびMozilla Firefox ブラウザー内で発生するすべてのコンバージョンを追跡できるようにします。これにより、ファーストパーティ Cookieの永続性が制限されます。<!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

コンバージョンマッピングタグを使用するには：

1. [&#x200B; コンバージョンマッピングタグ &#x200B;](#deploy-conversion-mapping-tag)をデプロイします。

1. 組織で複数のAdobe Experience Cloud ID サービス組織ID （旧称IMS組織ID）を使用している場合は、[&#x200B; コンバージョンタグを更新して](#update-conversion-tags)組織IDを含めます。

1. [&#x200B; タグのデプロイメントを検証](#validate-conversion-mapping)。

## ITP 2.2用のJavaScript コンバージョンマッピングタグのデプロイ {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>ITP 2.0にJavaScript コンバージョンマッピングタグを使用している場合は、すべてのコンバージョンページの既存のタグを次のいずれかのタグに置き換えます。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 組織でSearch、Social、およびCommerce アカウントに使用される1つの組織IDを使用している場合は、次のタグを使用します。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  ここで、`{AMO User ID}`をSearch, Social, &amp; Commerce アカウントの一意のユーザーIDに置き換えます。

* 組織で複数の組織IDを使用する場合は、次のタグを使用します。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  どこで：

   * 値`{xxxxxx@AdobeOrg}`を、ページのコンバージョンが追跡される組織IDに置き換えます。 すべてのコンバージョンページに同じ組織IDを使用します。

   * `{AMO User ID}`は、Search、Social、およびCommerce アカウントの一意のユーザーIDに置き換えられます。

* スクリプトタグへの`imsorgid`変数の追加をサポートしていないタグ管理システムを使用している場合は、代わりに次のコードを使用してください。

  * 組織が単一の組織IDを使用している場合：

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  ここで、`{AMO User ID}`をSearch, Social, &amp; Commerce アカウントの一意のユーザーIDに置き換えます。

   * 組織が複数の組織IDを使用する場合：

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     どこで：

      * 値`{xxxxxx@AdobeOrg}`を、ページのコンバージョンが追跡される組織IDに置き換えます。 すべてのコンバージョンページに同じ組織IDを使用します。

      * `{AMO User ID}`は、Search、Social、およびCommerce アカウントの一意のユーザーIDに置き換えられます。

組織IDまたはSearch, Social, &amp; Commerce ユーザーIDの値がわからない場合は、Adobe アカウントチームにお問い合わせください。

### 例

```
<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="abc12345@AdobeOrg" userid="99999"></script>`
```

```
<script>
window.ad_cloud = window.ad_cloud || {};
window.ad_cloud.imsorgid = "abc12345@AdobeOrg"
window.ad_cloud.userid = "99999"
</script>
<script src="//www.everestjs.net/static/amo-conversion-mapper.js"></script>
```

### タグの追加先

検索クリックからランディングページになる可能性のあるページにタグを追加します（ランディングページは時間の経過とともに変化するため、すべてのページにタグを追加するのが理想的です）。 Adobe Advertising JavaScript v3 コンバージョントラッキングタグの前に読み込む必要があります。

iframeまたはコンテナタグ内に配置する場合は、次の操作を行います。

* iframeはトップレベルドメインと同じレベルである必要があります。

* コンバージョンマッピングタグは、トップレベルドメインの下の1 レベルのみにする必要があります。

## JavaScript コンバージョンタグの更新 {#update-conversion-tags}

組織で複数の組織IDを使用している場合は、ページのコンバージョンを追跡する組織IDを既存のJavaScript コンバージョンタグに追加します。

組織が1つの組織IDを使用する場合、この手順は必要ありません。

### JavaScript V2 tags

変換スクリプトタグの先頭に次の文字列を追加します。

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

ここでは、値`{xxxxxx@AdobeOrg}`を、ページのコンバージョンが追跡される組織IDに置き換えます。

例：

```
<script language="javascript" src="https://www.everestjs.net/static/st.v2.js"></script>
<script language="javascript">
ef_imsorgid = "abc12345@AdobeOrg";
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

### JavaScript V3 タグ

`window.EF`を定義したら、次の文字列を追加します。

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

ここでは、値`{xxxxxx@AdobeOrg}`を、ページのコンバージョンが追跡される組織IDに置き換えます。

例：

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
        window.EF.imsorgid ="abc12345@AdobeOrg";
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

## タグ展開の検証 {#validate-conversion-mapping}

コンバージョンマッピングタグと通常のコンバージョンタグの検証について、Adobe アカウントチームにお問い合わせください（更新した場合）。
