---
title: Adobe Advertisingコンバージョンマッピングタグ
description: ITP 2.2 の JavaScript ベースのコンバージョンマッピングタグについて説明します。このタグを使用すると、Adobe Advertisingは、ランディングページ以外のページで発生するコンバージョンイベントを追跡できます。
exl-id: 6e2515da-2552-4f19-8344-1dee96cbf706
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '632'
ht-degree: 0%

---

# Adobe Advertisingの JavaScript コンバージョンマッピングタグ

*コンバージョントラッキングのAdobe Advertisingを持つ広告主のみ*

Adobe Advertisingの JavaScript ベースのコンバージョンマッピングタグは、Adobe Advertisingの JavaScript v2 または v3 コンバージョントラッキングタグと共に使用すると、Adobe Advertisingは、ランディングページ以外のページで発生するコンバージョンイベントを追跡できます。 ITP 2.2 ソリューションは、ユーザーの Cookie を広告主が所有する iFrame のローカルストレージに保存します。 その後、ローカルストレージは、クリック後のダウンストリームからコンバージョンページまで Cookie の値を保持できます。

Adobe AdvertisingがApple Safari および Mozilla Firefox ブラウザー内で発生したすべてのコンバージョンを確実に追跡できるように、ファーストパーティ cookie の持続性が制限されるようにするには、コンバージョンマッピングタグを使用します。 <!-- For all requirements to track conversions from Safari, see "Track Conversions from Apple Safari Browsers." -->

コンバージョンマッピングタグを使用するには：

1. [コンバージョンマッピングタグのデプロイ](#deploy-conversion-mapping-tag).

1. 組織が複数のAdobe Experience Cloud Identity Service 組織 ID（旧称 IMS Org ID）を使用している場合、 [コンバージョンタグを更新する](#update-conversion-tags) を追加して、組織 ID を含めます。

1. [タグのデプロイメントを検証する](#validate-conversion-mapping).

## ITP 2.2 の JavaScript コンバージョンマッピングタグをデプロイします {#deploy-conversion-mapping-tag}

>[!NOTE]
>
>ITP 2.0 の JavaScript コンバージョンマッピングタグを使用している場合は、すべてのコンバージョンページの既存のタグを次のタグのいずれかに置き換えます。<!-- any other instructions, too? Point them to the other page on Track Conversions from Safari...." -->

* 組織が単一の組織 ID を使用していて、その ID が Search、Social、&amp;Commerce のアカウントに使用されている場合は、次のタグを使用します。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" userid="{AMO User ID}"></script>`

  置き換える場所 `{AMO User ID}` を検索、ソーシャル、コマースの各アカウントの一意のユーザー ID に置き換えます。

* 組織が複数の組織 ID を使用している場合は、次のタグを使用します。

  `<script src="//www.everestjs.net/static/amo-conversion-mapper.js" imsorgid="{xxxxxx@AdobeOrg}" userid="{AMO User ID}"></script>`

  場所：

   * 値を置き換えます `{xxxxxx@AdobeOrg}` を、ページのコンバージョンを追跡する組織 ID に置き換えます。 すべてのコンバージョンページで同じ組織 ID を使用します。

   * 置き換える `{AMO User ID}` を検索、ソーシャル、コマースの各アカウントの一意のユーザー ID に置き換えます。

* を追加できないタグ管理システムを使用している場合、 `imsorgid` 変数をスクリプトタグに追加し、代わりに次のコードを使用します。

  *組織が単一の組織 ID を使用している場合：

  ```
  <script>
  window.ad_cloud = window.ad_cloud || {};
  window.ad_cloud.userid = "{AMO User ID}"
  </script>
  <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
  ```

  置き換える場所 `{AMO User ID}` を検索、ソーシャル、コマースの各アカウントの一意のユーザー ID に置き換えます。

   * 組織が複数の組織 ID を使用している場合：

     ```
     <script>
     window.ad_cloud = window.ad_cloud || {};
     window.ad_cloud.imsorgid = "{xxxxxx@AdobeOrg}"
     window.ad_cloud.userid = "{AMO User ID}"
     </script>
     <script src="//www.everestjs.net/static/amo-conversionmapper.js"></script>
     ```

     場所：

      * 値を置き換えます `{xxxxxx@AdobeOrg}` を、ページのコンバージョンを追跡する組織 ID に置き換えます。 すべてのコンバージョンページで同じ組織 ID を使用します。

      * 置き換える `{AMO User ID}` を検索、ソーシャル、コマースの各アカウントの一意のユーザー ID に置き換えます。

組織 ID または検索、Social、およびコマースのユーザー ID の値がわからない場合は、Adobeのアカウントマネージャーにお問い合わせください。

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

検索クリックからランディングページになる可能性のある任意のページにタグを追加します（ランディングページは時間の経過と共に変化する可能性があるので、すべてのページで理想的です）。 JavaScript v3 コンバージョントラッキングタグの前にAdobe Advertisingする必要があります。

iframe またはコンテナタグ内に配置されている場合は、次のようになります。

* iframe は、トップレベルドメインと同じレベルにある必要があります。

* コンバージョンマッピングタグは、トップレベルドメインの 1 レベル下にのみ配置する必要があります。

## JavaScript コンバージョンタグを更新する {#update-conversion-tags}

組織が複数の組織 ID を使用している場合、ページのコンバージョンを追跡する組織 ID を既存の JavaScript コンバージョンタグに追加します。

組織が 1 つの組織 ID を使用している場合、この手順は必要ありません。

### JavaScript V2 タグ

変換スクリプトタグの先頭に次の文字列を追加します。

`ef_imsorgid="{xxxxxx@AdobeOrg}";`

値を置き換える場所 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンを追跡する組織 ID に置き換えます。

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

後 `window.EF` が定義されている場合は、次の文字列を追加します。

`window.EF.imsorgid = "{xxxxxx@AdobeOrg}";`

値を置き換える場所 `{xxxxxx@AdobeOrg}` を、ページのコンバージョンを追跡する組織 ID に置き換えます。

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

## タグのデプロイメントを検証する {#validate-conversion-mapping}

Adobeアカウントチームに問い合わせて、コンバージョンマッピングタグと通常のコンバージョンタグ（更新済みの場合）の検証をお手伝いします。
