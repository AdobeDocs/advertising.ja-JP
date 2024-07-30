---
title: Adobe Advertisingコンバージョンマッピングタグ
description: ランディングページ以外のページで発生したコンバージョンイベントをAdobe Advertisingがトラッキングできる、ITP 2.2 のJavaScript ベースのコンバージョンマッピングタグについて説明します。
exl-id: cbeaf3cd-f1ab-419d-bba8-58a1c8215352
feature: Search Tracking
source-git-commit: 2c755eaa01f5bc7606074bb0fc276901c21ef807
workflow-type: tm+mt
source-wordcount: '637'
ht-degree: 0%

---

# Adobe Advertising JavaScript コンバージョンマッピングタグ

*Adobe Advertisingコンバージョントラッキングのみを使用する広告主*

JavaScript ベースのAdobe AdvertisingコンバージョンマッピングタグをAdobe AdvertisingのJavaScript v2 または v3 コンバージョントラッキングタグに加えて使用すると、Adobe Advertisingは、ランディングページ以外のページで発生するコンバージョンイベントをトラッキングできます。 ITP 2.2 ソリューションは、ユーザーの Cookie を広告主所有の iFrame のローカルストレージに保存します。 その後、ローカルストレージは、クリックダウンストリームからコンバージョンページまで、Cookie 値を保持できます。

コンバージョンマッピングタグを使用して、Apple Safari および Mozilla Firefox ブラウザー内で発生するすべてのコンバージョンをAdobe Advertisingでトラッキングできるようにします。これにより、ファーストパーティ cookie の永続性が制限されます。<!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

変換マッピングタグを使用するには：

1. [ コンバージョンマッピングタグをデプロイします ](#deploy-conversion-mapping-tag)。

1. 組織が複数のAdobe Experience Cloud ID サービス組織 ID （以前の IMS 組織 ID）を使用している場合は、[ コンバージョンタグを更新 ](#update-conversion-tags) して組織 ID を含めます。

1. [ タグのデプロイメントを検証 ](#validate-conversion-mapping) します。

## ITP 2.2 用のJavaScript コンバージョンマッピングタグのデプロイ {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>ITP 2.0 のJavaScript コンバージョンマッピングタグを使用している場合は、すべてのコンバージョンページの既存のタグを次のいずれかのタグに置き換えます。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 組織で 1 つの組織 ID を使用している場合は、この ID が検索、ソーシャル、Commerceのアカウントに使用されています。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  `{AMO User ID}` を検索、ソーシャル、Commerceの各アカウントの一意のユーザー ID に置き換える場所。

* 組織で複数の組織 ID を使用する場合は、次のタグを使用します。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  ここで、

   * 値 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンが追跡される組織 ID に置き換えます。 すべてのコンバージョンページで同じ組織 ID を使用します。

   * `{AMO User ID}` を検索、ソーシャル、Commerceの各アカウントの一意のユーザー ID に置き換えます。

* スクリプトタグへの `imsorgid` 変数の追加をサポートしていないタグ管理システムを使用している場合は、代わりに次のコードを使用します。

  *組織が 1 つの組織 ID を使用している場合：

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  `{AMO User ID}` を検索、ソーシャル、Commerceの各アカウントの一意のユーザー ID に置き換える場所。

   * 組織が複数の組織 ID を使用する場合：

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     ここで、

      * 値 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンが追跡される組織 ID に置き換えます。 すべてのコンバージョンページで同じ組織 ID を使用します。

      * `{AMO User ID}` を検索、ソーシャル、Commerceの各アカウントの一意のユーザー ID に置き換えます。

組織 ID や検索、ソーシャル、Commerceのユーザー ID の値が不明な場合は、Adobeアカウントチームにお問い合わせください。

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

### タグの追加場所

検索クリックからランディングページである可能性のある任意のページにタグを追加します（ランディングページは時間と共に変化する可能性があるので、すべてのページで行うのが理想的です）。 JavaScript v3 コンバージョントラッキングタグをAdobe Advertisingする前に読み込む必要があります。

iframe またはコンテナタグ内に配置されている場合は、次のようにします。

* iframe は、トップレベルドメインと同じレベルにある必要があります。

* コンバージョンマッピングタグは、最上位ドメインの 1 つ下のレベルのみにしてください。

## JavaScript コンバージョンタグを更新する {#update-conversion-tags}

組織が複数の組織 ID を使用している場合は、ページのコンバージョンが追跡される組織 ID を、既存のJavaScript コンバージョンタグに追加します。

組織で 1 つの組織 ID を使用している場合、この手順は必要ありません。

### JavaScript V2 タグ

変換スクリプトタグの先頭に次の文字列を追加します。

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

値 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンがトラッキングされる組織 ID に置き換えます。

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

`window.EF` を定義したら、次の文字列を追加します。

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

値 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンがトラッキングされる組織 ID に置き換えます。

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

## タグデプロイメントの検証 {#validate-conversion-mapping}

コンバージョンマッピングタグと通常のコンバージョンタグ（更新している場合）の検証については、Adobeアカウントチームにお問い合わせください。
