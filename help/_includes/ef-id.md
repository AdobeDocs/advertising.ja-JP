---
source-git-commit: 91610ee5e1741f19dde5567b806e05f1034397c0
workflow-type: tm+mt
source-wordcount: '230'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

EF ID は、Adobe Advertisingがアクティビティをオンラインクリックまたは広告漏洩に関連付けるために使用する一意のトークンです。 EF ID は、[an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約済み [!DNL eVar]）ディメンション（Adobe Advertising EF ID）に保存され、個々のブラウザーまたはデバイスレベルで各広告のクリックまたは露出をトラッキングします。 EF ID は、主にAdobe Advertising内のレポートおよび入札最適化のためにAdobe Advertisingに [!DNL Analytics] データを送信するためのキーとして機能します。

### EF ID フォーマット

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 [!DNL Analytics] 実装によって URL トラッキングが強制的に小文字に変換される場合、Adobe Advertisingは EF ID を認識しません。 これは、Adobe Advertisingの入札とレポートに影響しますが、[!DNL Analytics] 内のAdobe Advertising レポートには影響しません。

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
