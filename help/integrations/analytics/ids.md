---
title: Adobe AdvertisingID 使用者 [!DNL Analytics]
description: Adobe AdvertisingID 使用者 [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: 73cdb171523b55f48b5ae5c5b2b4843f542336a6
workflow-type: tm+mt
source-wordcount: '1180'
ht-degree: 0%

---

# Adobe AdvertisingID 使用者 [!DNL Analytics]

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*

Adobe Advertisingでは、オンサイトパフォーマンストラッキングに 2 つの ID( *EF ID* そして *AMO ID*.

広告インプレッションが発生すると、Adobe Advertisingは AMO ID と EF ID の値を作成して保存します。 広告を閲覧した訪問者が広告をクリックせずにサイトに入ったとき、 [!DNL Analytics] は、を通じてこれらの値をAdobe Advertisingから呼び出します [!DNL Analytics for Advertising] JavaScript コード。 ビュースルートラフィックの場合、 [!DNL Analytics] は追加の ID(`SDID`) で始まり、EF ID と AMO ID をステッチするために使用されます。 [!DNL Analytics]. クリックスルートラフィックの場合、これらの ID は `s_kwcid` および `ef_id` クエリー文字列パラメーター。

Adobe Advertisingは、次の条件を使用して、Web サイトへのクリックスルーエントリとビュースルーエントリを区別します。

* ビュースルーエントリは、広告を表示した後、広告をクリックせずにユーザーがサイトを訪問した場合に取り込まれます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。
   * 訪問者には、 [!DNL DSP] または [!DNL Search, Social, & Commerce] 次の期間の広告 [ルックバックウィンドウをクリック](#lookback-a4adc).
   * 訪問者が少なくとも 1 つを閲覧しました [!DNL DSP] 次の期間の広告 [インプレッションのルックバックウィンドウ](#lookback-a4adc). 最後のインプレッションは、ビュースルーとして渡されます。
* クリックスルーエントリは、サイト訪問者がサイトに入る前に広告をクリックするとキャプチャされます。 [!DNL Analytics] は、次のいずれかの条件が発生した場合にクリックスルーをキャプチャします。
   * URL には、Adobe Advertising別のランディングページ URL に追加された EF ID と AMO ID が含まれます。
   * URL にトラッキングコードは含まれていませんが、Adobe Advertisingの JavaScript コードが過去 2 分以内にクリックを検出しました。

![Adobe Advertisingビューベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Adobe Advertisingビューベース [!DNL Analytics] 統合*

![Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe Advertisingクリックの URL ベース [!DNL Analytics] 統合*

## Adobe AdvertisingEF ID

EF ID は、アクティビティをオンラインクリックまたは広告露出に関連付けるためにAdobe Advertisingが使用する一意のトークンです。 EF ID は、に格納されます。 [an [!DNL Analytics] [!DNL eVar]](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または [!DNL rVar] （予約済み） [!DNL eVar]) ディメンション (Adobe AdvertisingEF ID) を使用して、個々のブラウザーまたはデバイスレベルでの各広告のクリックまたは露出を追跡します。 EF ID は主に送信のキーとして機能します [!DNL Analytics] データをAdobe Advertisingに送信し、Adobe Advertising内でのレポートおよび入札の最適化を行います。

### EF ID 形式

>[!NOTE]
>
>EF ID では大文字と小文字が区別されます。 次の場合、 [!DNL Analytics] 実装により、URL トラッキングが強制的に小文字に変換され、Adobe Advertisingは EF ID を認識しません。 これはAdobe Advertisingの入札とレポートに影響しますが、内のAdobe Advertisingレポートには影響しません。 [!DNL Analytics].

#### [!DNL Google Ads] 広告を検索

```
{gclid}:G:s
```

場所：

* `gclid` が [!DNL Google Click ID] (GCLID) を使用します。
* `s` はネットワークタイプです（「s」は検索用）。

#### Microsoft Advertising 検索広告

```
{msclkid}:G:s
```

場所：

* `msclkid` が [!DNL Microsoft Click ID] (MSCLKID)。
* `s` はネットワークタイプです（「s」は検索用）。

#### 他の検索エンジンでの広告と検索広告の表示

```
<Adobe Advertising visitor ID>:<timestamp>:<channel type>
```

場所：

* &lt;*Adobe Advertising訪問者 ID*> は、訪問者ごとの一意の ID です（UhKVaAABCkJ0mDt など）。 また、 *サーファー ID*.

* &lt;*timestamp*> は、YYYYMMDDHHMMSS という形式の時刻です (2019 年の場合は20190821192533、08 月の場合は 21 日、19 時など )。:25:33).

* &lt;*チャネルタイプ*> は、クリックまたは露出の原因となるチャネルタイプです。

   * `d` DSPディスプレイ広告のクリック（クリックスルーを表示）
   * `i` DSPディスプレイ広告のインプレッション（表示ビュースルー）の場合
   * `s` 検索広告のクリック（検索クリックスルー）。

例 `EF ID: WcmibgAAAHJK1RyY:1551968087687:d`

### の EF IDDimension [!DNL Analytics]

In [!DNL Analytics] レポートでは、EF ID データを検索するには、 [!UICONTROL EF ID] ディメンションと使用 [!UICONTROL EF ID Instance] 指標。

EF ID には、Analysis Workspaceでの 500,000 個の一意の ID 制限が適用されます。 500,000 個の値に達すると、すべての新しいトラッキングコードが 1 行項目のタイトル「[!UICONTROL Low Traffic].&quot; レポートの正確性が欠落する可能性があるので、EF ID は分類されず、でのセグメントやレポートに使用しないでください [!DNL Analytics].

## Adobe AdvertisingAMO ID

AMO ID は、より詳細なレベルで一意の広告の組み合わせを追跡し、 [!DNL Analytics] 広告指標（インプレッション数、クリック数、コストなど）のデータ分類とAdobe Advertisingからの取り込み AMO ID は、 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション (AMO ID)。でのレポートにのみ使用されます。 [!DNL Analytics].

AMO ID は、 `s_kwcid`(「[!DNL the squid].&quot;

### の AMO ID フォーマット [!DNL DSP]

```
<Channel ID>!<Ad ID>!<Placement ID>
```

場所：

* &lt;*チャネル ID*> は次のいずれかになります。

   * `AC` = Advertising DSP
   * `AL` 対象： [!DNL Advertising Search, Social, & Commerce]

* &lt;*広告 ID*> は、広告に対してAdobe Advertising生成の一意の識別子を使用します。 Adobe Advertisingエンティティのメタデータを読み取り可能にするキーとして機能します [!DNL Analytics] ディメンション。

* &lt;*プレースメント ID*> は、配置のAdobe Advertising生成の一意の識別子です。 Adobe Advertisingエンティティのメタデータを読み取り可能にするキーとして機能します [!DNL Analytics] ディメンション。

AMO ID の例： AC!iIMvXqlOa6Nia2lDvtgw!GrV6o2oV2qQLjQiXLC7

### の AMO ID フォーマット [!DNL Search, Social, & Commerce]

の AMO ID [!DNL Search, Social, & Commerce] 各検索エンジンで異なる形式に従います。 すべての検索エンジンの形式は、次のように始まります。

```
AL!{userid}!{sid}
```

場所：

* `AL` は、広告ネットワークのチャネル ID です。
* `{userid}` は、広告主に割り当てる一意の数値Adobe AdvertisingID です。
* `{sid}` は、指定した広告ネットワークにAdobe Advertisingが使用する数値 ID です（例： ）。 `3` 対象： [!DNL Google Ads] または `10` 対象： [!DNL Microsoft Advertising].

以下は、いくつかの広告ネットワークの完全な AMO ID 形式です。 その他の広告ネットワーク向けの AMO ID の形式については、担当のAdobeアカウントチームにお問い合わせください。

の AMO ID フォーマット [!DNL Google Ads]:

```
AL!{userid}!{sid}!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

場所：

* `{creative}` が [!DNL Google Ads] クリエイティブの一意の数値 ID。
* `{matchtype}` は、広告をトリガーしたキーワードの一致タイプです。 `e` 正確には `p` ( フレーズの場合は、 `b` 幅の広い
* `{placement}` は、広告がクリックされた Web サイトのドメイン名です。 値は、配置ターゲットキャンペーンの広告と、コンテンツサイトに表示されるキーワードターゲットキャンペーンの広告で使用できます。
* `{network}` クリックが発生したネットワークを示します。  `g` 対象： [!DNL Google] 検索（キーワードターゲット広告のみ） `s` 検索パートナー（キーワードターゲット広告のみ）の場合、または `d` ディスプレイネットワーク用（キーワードターゲット広告またはプレースメントターゲット広告用）。
* `{keyword}` は、（検索サイトで）広告をトリガーした特定のキーワードか、（コンテンツサイトで）最適なキーワードのどちらかです。

の AMO ID フォーマット [!DNL Microsoft Advertising]:

```
AL!{userid}!{sid}!{AdId}!{OrderItemId}
```

場所：

* `{AdId}` が [!DNL Microsoft Advertising] クリエイティブの一意の数値 ID。
* `{OrderItemId}` が [!DNL Microsoft Advertising] キーワードの数値 ID。

### AMO IDDimension（内） [!DNL Analytics]

Analytics レポートでは、 [!UICONTROL AMO ID] ディメンションと使用 [!UICONTROL AMO ID Instance] 指標。 The [!UICONTROL AMO ID] ディメンションには、取得されたすべての AMO ID 値が格納されますが、 [!UICONTROL AMO ID Instance] 指標は、AMO ID 値がサイトによってキャプチャされた頻度を示します。 例えば、同じ検索広告が 4 回クリックされたが、Analytics が 7 つのサイトエントリを追跡した場合、 [!UICONTROL AMO ID Instance] 7(7) で [!UICONTROL Clicks] は 4(4) です。

内の任意のレポートまたは監査 [!DNL Analytics]を使用する場合、ベストプラクティスは、AMO ID を対応するインスタンスと共に使用することです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising]](data-variances.md#data-validation)」(「 [!DNL Analytics] そしてAdobe Advertising」

## Analytics 分類について

In [!DNL Analytics], a [分類](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html) は、アカウント、キャンペーン、広告など、特定のトラッキングコードのメタデータの一部です。 Adobe Advertisingは、レポートを生成する際に様々な方法（広告タイプやキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe Advertisingデータを分類します。 分類は、 [!DNL Analytics] とは、AMO 指標と共に使用できます。例： [!UICONTROL AMO Cost], [!UICONTROL AMO Impressions]、および [!UICONTROL AMO Clicks]、およびのようなカスタムおよび標準のオンサイトイベント [!UICONTROL Visits], [!UICONTROL Leads], [!UICONTROL Orders]、および [!UICONTROL Revenue].

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe Advertising](data-variances.md)
