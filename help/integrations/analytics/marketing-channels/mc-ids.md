---
title: Adobe Advertising ID を使用したルール  [!DNL Marketing Channels]  作成
description: Adobe Advertising ID を使用して、 [!DNL Analytics Marketing Channels] の処理ルールを作成する方法を説明します。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
source-git-commit: 0813a8bddc1ecf238f4a62c4fcefd8584f32e152
workflow-type: tm+mt
source-wordcount: '1448'
ht-degree: 0%

---

# Adobe Advertising ID を使用した処理ルール [!DNL Marketing Channels] 作成

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

Adobe Advertising ID （[AMO ID および EF ID](../ids.md)）を使用して、Adobe Analyticsで [!DNL Marketing Channels] 処理ルールを設定できます。 Adobe Advertising キャンペーンに固有のルールには、Adobe Advertising ID を使用します。 ルールを処理する順序によって、可能なすべてのデータが正しく取得されるかどうかが決まります。

## 処理ルールの AMO ID

AMO ID は、[!DNL Analytics] 内でAdobe Advertising データのレポートに使用されるプライマリトラッキングコードです。 AMO ID は、Adobeによって管理される動的な値を連結したもので、[!DNL Analytics] 内で詳細なレポートを提供します。 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html) または rVar ディメンション（AMO ID）に保存されます。 AMO ID は、次の 2 つの方法で [!DNL Analytics] で設定できます。

* クリックスルーのトラッキング：Adobe Advertisingは、`s_kwcid` のクエリ文字列パラメーターをリンクに設定 [!DNL Analytics]、クリックスルーが発生するとランディングページ URL からパラメーターを取得します。

* ビュースルートラッキング （[!DNL DSP] のみ）: [!DNL Last Event Service] は、サーバーサイドでビュースルーを検出し、AMO ID を [!DNL Analytics] に送信します。 この場合、URL には `s_kwcid` パラメーターは含まれません。

AMO ID 内の動的な値は、トラッキングされたマーケティングチャネルを示します。

* AMO ID のプレフィックスを使用して、[!DNL Marketing Channels] 内の最上位チャネルを識別できます。

* AMO ID の本文に含まれる文字フレーズは、より具体的なキャンペーンタイプを示します。

* 「vt」というサフィックスは、ビュースルートラフィック [!DNL DSP] 対して存在し、クリックスルーおよびビュースルーの別の [!DNL DSP] チャネルを作成するために使用できます。

残りの AMO ID は無視できます。

| [!UICONTROL AMO ID] | チャネル | ルールロジック |
|--------|---------|--------------------|
| !ctv （サフィックス） | [!UICONTROL DSP Connected TV ViewThrough] | 次で終わる |
| !d! （本文） | [!UICONTROL Display Network] | 次を含む |
| !g! （本文） | [!UICONTROL Google Search] | 次を含む |
| !s! （本文） | [!UICONTROL Search Partner] | 次を含む |
| !u! （本文） | [!UICONTROL Smart Shopping Campaign] | 次を含む |
| !ytv! （本文） | [!UICONTROL YouTube Video Ad] | 次を含む |
| ！はい！ （本文） | [!UICONTROL YouTube Search Ad] | 次を含む |
| !vp! （本文） | [!UICONTROL Google Video Partners] | 次を含む |
| !vt （サフィックス） | [!UICONTROL DSP ViewThrough] | 次で終わる |
| アル！ （プレフィックス） | [!UICONTROL Paid Search] | 次で始まる |
| AC! （プレフィックス） | [!UICONTROL DSP Display] | 次で始まる |

## 処理ルールの EF ID

AMO EF ID （EF ID）は、[!DNL Analytics for Advertising] 統合で使用される 2 番目のトラッキングコードです。 主な目的は、イベントデータをトラッキングし [!DNL Analytics]Adobe Advertisingに渡すことです。 クリックスルーまたはビュースルーが発生するたびに、同じ訪問者に対して完全に同じ広告であっても、一意の EF ID が生成されます。 EF ID は、通常、[!DNL Analytics] の変数制限あたり 500,000 個の一意の値を超え、レポートに使用できなくなるので、[!DNL Analytics] レポートのユーザーインターフェイスでは使用されません。 Adobe Advertising指標とメタデータは EF ID には適用されず、AMO ID にのみ適用されます。 Adobe Advertisingのキャンペーン最適化には、さらに精度を高めたトラッキングが必要なので、両方の ID が必要です。

EF ID ディメンションは、[!DNL Analytics] のレポートでは直接使用されませんが、マーケティングチャネルの作成に役立つ場合があります。 EF ID サフィックスは、チャネル（表示または検索）と、訪問がクリックスルーとビュースルーのどちらによって行われたかを示します。 EF ID の区切り文字は、AMO ID の感嘆符ではなくコロンです。

| EF ID サフィックス | チャネル |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Adobe Advertisingの処理ルールの例

次のルールセットの例では、広告チャネル（有料検索、表示クリックスルーおよび表示ビュースルー）のルールに焦点を当てています。 有料検索検出の推奨ルール（そのルールと自然検索マーケティングチャネルロジックとのやり取りを含む）と、自然参照ドメイン ルールのオプション更新についても説明します。

**メモ：** ディスプレイは、広告主の好みに基づいて、2 つのチャネルに分割したり、単一のチャネルに結合したりできます。

このスクリーンショットの例には、他のチャネルが含まれており、一般的な実装における広告チャネルと他のチャネルの比較において、推奨される操作順序を示しています。

>[!IMPORTANT]
>
>ルールの処理順序については、「[ ルールの操作の順序  [!DNL Marketing Channels] 」を参照してください ](#rule-order)

![ 一連の処理ルールの例 ](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### 有料検索ルール

ベストプラクティスは、[!UICONTROL Paid Search] ルールの「Any」演算子に 2 つの条件を含めることです。

* コスト、クリック数、インプレッション数のデータには AMO ID が含まれているので、AMO ID を含めます。 AMO ID は、「AL!」で始める必要があります クリック/コスト/インプレッションのデータを [!UICONTROL Paid Search].<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? --> に正しく配分する

* [!UICONTROL Paid Search] クリックスルーの URL には常に `s_kwcid` クエリ文字列パラメーターが含まれているので、訪問者がランディングページに戻った場合に適切な重複排除が発生するように含めます。 「AL!」を含める クリック/コスト/インプレッションのデータを `s_kwcid` に正しく割り当てる [!UICONTROL Paid Search] 前。

チャネルの値を AMO ID に設定しないでください。 代わりに、参照ドメイン、検索エンジン + キーワード、ページなどに設定します。 （これは、すべての [!DNL Marketing Channels] に関連します）。

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![ 有料検索ルールの例 ](/help/integrations/assets/a4adc-mc-rule-paid-search.png " 有料検索ルールの例 ")

### 自然検索ルール

[!UICONTROL Natural Search] しくは、[[!UICONTROL Paid Search] 検出ルールに ](https://experienceleague.adobe.com/en/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection)`ef_id` および `s_kwcid` のクエリ文字列パラメーターが含まれていることを確認してください。 （通常、これは、Advertisingの検索、ソーシャルおよびCommerceが [!DNL Analytics] に統合されると自動的に設定されますが、統合が設定された後に、[!DNL Analytics] 管理者がロジックを変更した場合は検証されます）。

ルールを「自然検索検出ルールに一致」に設定します（通常、このチャネルのデフォルト設定です）。

![ 自然検索ルールの例 ](/help/integrations/assets/a4adc-mc-rule-natural-search.png " 自然検索ルールの例 ")

### クリックスルールールの#1 を表示

クリックスルーのみをキャプチャして、ディスプレイのクリックスルーのマーケティングチャネルを作成します。 AMO ID はクリックスルーとビュースルーの両方で同じであるため、このルールでは EF ID 変数と `ef_id` クエリ文字列パラメーターが使用されます。

クリックスルーが URL 全体でトラッキングされる場合があります（デフォルト）。 また、クリックスルーは、サーバーサイドで Last Event Service を介して追跡されるので、URL には `ef_id` パラメーターは含まれません。 したがって、ルールは、EF ID 変数または `ef_id` クエリ文字列パラメーターが「:d」で終わる条件をチェックします。 このルールをどちらの条件に対してもトリガーする場合は、「`Any`」演算子を使用します。

![ 最初のディスプレイのクリックスルー規則の例 ](/help/integrations/assets/a4adc-mc-rule-display-ct.png " 最初のディスプレイのクリックスルー規則の例 ")

### 自然参照ドメインルール

（オプション）「訪問の最初のページ」条件と「任意」演算子を標準の [!UICONTROL Natural Referring Domains] ルールに追加することをお勧めします。 このルールはオプションですが、ユーザーが「戻る」ボタンをクリックしてランディングページに戻った場合に、自然なリファラーのエッジケースが設定されるのを防ぐのに役立ちます。

![ 自然参照ドメインのルールの例 ](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png " 自然参照ドメインのルールの例 ")

### CTV ビュースルールールの表示

接続され [!DNL DSP] テレビ（CTV）のビュースルーを追跡するには、AMO ID が `"!ctv"` で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングには URL に `ef_id` や `s_kwcid` は含まれず、ルールに必要な条件は 1 つだけです。

![ ディスプレイ CTV ビュースルー規則の例 ](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png " ディスプレイ CTV ビュースルー規則の例 ")

### ビュースルールールを表示

Display ViewThrough チャネルを作成するには、EF ID が「:i」で終わるルールを作成します。 訪問者が広告をクリックしなかったので、ビュースルートラッキングには URL に `ef_id` や `s_kwcid` は含まれず、ルールに必要な条件は 1 つだけです。

![ ビュースルー表示ルールの例 ](/help/integrations/assets/a4adc-mc-rule-display-vt.png " ビュースルー表示ルールの例 ")

### クリックスルールールの#2 を表示

2 番目のディスプレイのクリックスルー **ールについては、「AMO ID は「AC！で始まる」と設定します**。 2 つ目のルールは、Adobe Advertisingから [!DNL Analytics] に直接取り込まれる表示チャネルのクリック/コスト/インプレッション データをキャプチャするためのものです。 このデータは AMO ID に関連付けられていますが、`ef_id` クエリ文字列を含む URL が含まれていないので、これらのヒットは、最初のディスプレイのクリックスルー規則がキャプチャする AMO EF ID に接続されません。

![2 番目のディスプレイのクリックスルー規則の例 ](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "2 番目のディスプレイのクリックスルー規則の例 ")

## [!DNL Marketing Channels] 則の運用の順序 {#rule-order}

![Adobe Advertising関連規程の理想的な順序 ](/help/integrations/assets/a4adc-mc-rule-order.png "Adobe Advertising関連規程の理想的な順序 ")

* [!UICONTROL Paid Search] を *前* に置 [!UICONTROL Natural Search] ます。 そうしないと、自然検索に有料検索データが割り当てられてしまいます。

* **first**[!UICONTROL Display ClickThrough]*before*[!UICONTROL Natural Referring Domains] と [!UICONTROL Natural Social] を入れます。

* [!UICONTROL CTV view-throughs] を使うときは *前* に置き [!UICONTROL Display ViewThroughs] さい。 そうでない場合、CTV ビュースルーは Display ViewThrough としてキャプチャされます。

* 同じランディングイベントでビュースルーと非 [!UICONTROL Display ViewThroughs] ーザークリックスルーが発生する可能性があるので、*および* の前に [!UICONTROL Internal][!UICONTROL Direct] 後 [!DNL Advertising] 他のチャネルを配置します。 例えば、訪問者がAdobe Advertising広告を表示してインプレッションを取得し、[!UICONTROL Natural Search] を通じてサイトに移動する場合があります。

  ベストプラクティスは、ビュースルーよりも他のチャネル（[!UICONTROL Internal] と [!UICONTROL Direct] を除く）を優先することです。

* 一部の広告主は、[!UICONTROL Display ViewThroughs] よりも [!UICONTROL Natural Referring Domains] を優先することを選択する場合があります。 それには、2 つのルールの処理順序を入れ替えます。

* **2 番目** のルールは [!UICONTROL Display ClickThrough]Adobe Advertisingから [!DNL Analytics] に直接入ってくるクリック/コスト/インプレッションのデータをキャッチするためのものです。 このデータは AMO ID のみに関連付けられているので、これらのヒットは AMO EF ID に接続されていません。 このルールを設定しない場合、すべてのクリック/コスト/インプレッションのデータは [!UICONTROL Direct] チャネルに分類されます。これは、[!DNL Marketing Channel] に一致しないデータのデフォルトチャネルです。 このルールは、ビュースルー規則の *後* に指定する必要があります。指定しない場合、ビュースルーが適用されます。

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [ の基本  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertisingとでチャネルデータが異なる可能性がある理由  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Adobe Advertising データ  [!DNL Analytics Marketing Channels]  使用 ](mc-ac-data.md)
>* [ ビデオ：Adobe Advertising レポート  [!DNL Marketing Channels]  使用 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ 使用するAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md)