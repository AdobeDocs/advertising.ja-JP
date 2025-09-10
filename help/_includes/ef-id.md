---
source-git-commit: dede10acca1540a10699be3c14564a6f9360edd2
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---
# ADOBE ADVERTISING EF ID

## ADOBE ADVERTISING EF ID

EF ID は、Adobe Advertisingがアクティビティをオンラインクリックや個々のブラウザーまたはデバイスレベルでの広告表示に関連付けるために使用する一意のトークンです。 EF ID は、主に、Adobe Advertising内のレポートと入札最適化のために、[!DNL Analytics] データとCustomer Journey Analytics データをAdobe Advertisingに送信するためのキーとして機能します。

[!DNL Analytics] の場合、EF ID は [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約 [!DNL eVar]）ディメンション（Adobe Advertising EF ID）に保存されます。

Customer Journey Analyticsの場合、EF ID は、`trackingIdentities` の一部である `conversionDetails` オブジェクトの [!UICONTROL Adobe Advertising Cloud ExperienceEvent Full Extension] プロパティに格納されます。

### EF ID 形式 {#ef-id-formats}

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
