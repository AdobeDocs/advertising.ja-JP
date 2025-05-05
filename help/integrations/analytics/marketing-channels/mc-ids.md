---
title: Adobe Advertising ID を使用したルール  [!DNL Marketing Channels]  作成
description: Adobe Advertising ID を使用して、 [!DNL Analytics Marketing Channels] の処理ルールを作成する方法を説明します。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 96a0add168c7fb7a6d80cf1b81ef4b315fbba89f
workflow-type: tm+mt
source-wordcount: '757'
ht-degree: 0%

---

# Adobe Advertising ID を使用した処理ルール [!DNL Marketing Channels] 作成

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

Adobe AdvertisingID （[AMO ID および EF ID](../ids.md)）を使用して、Adobe Analyticsで [!DNL Marketing Channels] 処理ルールを設定できます。 Adobe Advertisingキャンペーンに固有のルールには、Adobe AdvertisingID を使用します。

## 処理ルールの AMO ID

AMO ID は、[!DNL Analytics] 内でAdobe Advertisingデータのレポートに使用されるプライマリトラッキングコードです。 AMO ID は、Adobeが管理する動的な値を連結したもので、[!DNL Analytics] 内で詳細なレポートを提供します。 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=ja) または rVar ディメンション（AMO ID）に保存されます。 AMO ID は、次の 2 つの方法で [!DNL Analytics] で設定できます。

* クリックスルーのトラッキング：Adobe Advertisingは、リンクに `s_kwcid` のクエリ文字列パラメーターを設定 [!DNL Analytics]、クリックスルーが発生するとランディングページ URL からパラメーターを取得します。
* ビュースルートラッキング （[!DNL DSP] のみ）: Last Event Service は、サーバーサイドでビュースルーを検出し、AMO ID を [!DNL Analytics] に送信します。 この場合、URL には `s_kwcid` パラメーターは含まれません。

AMO ID 内の動的な値は、トラッキングされたマーケティングチャネルを示します。

* AMO ID のプレフィックスを使用して、[!DNL Marketing Channels] 内の最上位チャネルを識別できます。

* AMO ID の本文に含まれる文字フレーズは、より具体的なキャンペーンタイプを示します。

* 「vt」というサフィックスは、ビュースルートラフィック [!DNL DSP] 対して存在し、クリックスルーおよびビュースルーの別の [!DNL DSP] チャネルを作成するために使用できます。

残りの AMO ID は無視できます。

| [!UICONTROL AMO ID] | チャネル | ルールロジック |
|--------|---------|--------------------|
| !ctv （サフィックス） | [!UICONTROL DSP Connected TV View-through] | 次で終わる |
| !d! （本文） | [!UICONTROL Display Network] | 次を含む |
| !g! （本文） | [!UICONTROL Google Search] | 次を含む |
| !s! （本文） | [!UICONTROL Search Partner] | 次を含む |
| !u! （本文） | [!UICONTROL Smart Shopping Campaign] | 次を含む |
| !ytv! （本文） | [!UICONTROL YouTube Video Ad] | 次を含む |
| ！はい！ （本文） | [!UICONTROL YouTube Search Ad] | 次を含む |
| !vp! （本文） | [!UICONTROL Google Video Partners] | 次を含む |
| !vt （サフィックス） | [!UICONTROL DSP View-through] | 次で終わる |
| アル！ （プレフィックス） | [!UICONTROL Paid Search] | 次で始まる |
| AC! （プレフィックス） | [!UICONTROL DSP] | 次で始まる |

### AMO ID を使用する処理ルールの例

[!UICONTROL Paid Search] チャネルの [!DNL Marketing Channels] の処理ルールは、次のようになります。

![[!UICONTROL Paid Search] ルールの例 ](/help/integrations/assets/a4adc-mc-rule-paidsearch.png)

[!UICONTROL YouTube Video Ads] チャネルの [!DNL Marketing Channels] の処理ルールは、次のようになります。

![[!UICONTROL YouTube Video Ads] ルールの例 ](/help/integrations/assets/a4adc-mc-rule-youtube-video.png)

>[!IMPORTANT]
>
> 特定の順序でルールを実行するようにしてください。 上記の 2 つのルールが順番に実行された場合、AMO ID がどちらも「AL!」で始まるので、[!DNL YouTube] ビデオ広告トラフィックはすべて [!UICONTROL Paid Search] チャネルに分類されます。 また、「!ytv!」が含まれます。

## 処理ルールの EF ID

AMO EF ID （EF ID）は、[!DNL Analytics for Advertising] 統合で使用される 2 番目のトラッキングコードです。 主な目的は、イベントデータをトラッキングし [!DNL Analytics]Adobe Advertisingに渡すことです。 クリックスルーまたはビュースルーが発生するたびに、同じ訪問者に対して完全に同じ広告であっても、一意の EF ID が生成されます。 EF ID は、通常、[!DNL Analytics] の変数制限あたり 500,000 個の一意の値を超え、レポートに使用できなくなるので、[!DNL Analytics] レポートのユーザーインターフェイスでは使用されません。 Adobe Advertising指標とメタデータは EF ID には適用されず、AMO ID にのみ適用されます。 Adobe Advertisingでのキャンペーンの最適化には、さらに精度の高いトラッキングが必要なので、両方の ID が必要です。

EF ID ディメンションは、[!DNL Analytics] のレポートでは直接使用されませんが、マーケティングチャネルの作成に役立つ場合があります。 EF ID サフィックスは、チャネル（表示または検索）と、訪問がクリックスルーとビュースルーのどちらによって行われたかを示します。 EF ID の区切り文字は、AMO ID の感嘆符ではなくコロンです。

| EF ID サフィックス | チャネル |
|-------|---------|
| :s | [!UICONTROL Paid Search] |
| :d | [!UICONTROL Display Click-through] |
| :i | [!UICONTROL Display View-through] |

### EF ID を使用する処理ルールの例

#### クリックスルー規則の表示

クリックスルーのみをキャプチャして、ディスプレイのクリックスルーのマーケティングチャネルを作成します。 AMO ID はクリックスルーとビュースルーの両方で同じであるため、このルールでは EF ID 変数と `ef_id` クエリ文字列パラメーターが使用されます。

クリックスルーが URL 全体でトラッキングされる場合があります（デフォルト）。 また、クリックスルーは、サーバーサイドで Last Event Service を介して追跡されるので、URL には `ef_id` パラメーターは含まれません。 したがって、ルールは、EF ID 変数または `ef_id` クエリ文字列パラメータが「:d」で終わる条件をチェックします。 このルールをどちらの条件に対してもトリガーする場合は、「`Any`」演算子を使用します。

![ 表示のクリックスルーのルールの例 ](/help/integrations/assets/a4adc-mc-rule-display-ct.png)

#### ビュースルールールを表示

表示ビュースルーチャネルを作成するには、EF ID が「:i」で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングには URL に `ef_id` や `s_kwcid` は含まれず、ルールに必要な条件は 1 つだけです。

![ ビュースルールールの表示例 ](/help/integrations/assets/a4adc-mc-rule-display-vt.png)

>[!MORELIKETHIS]
>
>* [ の基本  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [ チャネルデータがAdobe Advertisingによって異なる理由  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Adobe Advertisingデ  [!DNL Analytics Marketing Channels]  タの使用 ](mc-ac-data.md)
>* [ ビデオ：Adobe Advertisingレポート  [!DNL Marketing Channels]  使用 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=ja)
>* [ 使用Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
