---
source-git-commit: 56c27461cf0e1d7111de9d35d9e38fa980af4c52
workflow-type: tm+mt
source-wordcount: '164'
ht-degree: 0%

---
# EF ID 形式

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 [!DNL Analytics] またはCustomer Journey Analyticsの実装によって URL トラッキングが強制的に小文字に変換される場合、Adobe Advertisingは EF ID を認識しません。 これは、Adobe Advertisingの入札とレポートに影響しますが、[!DNL Analytics] またはCustomer Journey Analytics内のAdobe Advertising レポートには影響しません。

#### [!DNL Google Ads] 検索広告

```
{gclid}:G:s
```

ここで、

* `gclid` は [!DNL Google Click ID] （GCLID）です。
* `s` はネットワークの種類（検索用は&quot;s&quot;）です。

#### [!DNL Microsoft Advertising] 検索広告

```
{msclkid}:G:s
```

ここで、

* `msclkid` は [!DNL Microsoft Click ID] （MSCLKID）です。
* `s` はネットワークの種類（検索用は&quot;s&quot;）です。

#### 他の検索エンジンでの広告および検索広告の表示

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

ここで、

* &lt;*Adobe Advertising訪問者 ID*> は、訪問者ごとの一意の ID です（UhKVaAABCkJ0mDt など）。 「*surfer ID*」とも呼ばれる。

* &lt;*timestamp*> は、YYYYMMDDHHMMSS 形式の時刻（2019 年、08 月、21 日、19:25:33 日の 20190821192533 など）です。

* &lt;*channel type*> は、クリックまたは露出を行うチャネルのタイプです。

   * DSP ディスプレイ広告のクリックを `d` す（表示のクリックスルー）
   * DSP ディスプレイ広告のインプレッションの `i` ール（ビュースルーの表示）
   * 検索広告を `s` リックします（検索クリックスルー）。

例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`
