---
title: Adobe Advertising IDを使用した [!DNL Marketing Channels]  ルールの作成
description: Adobe Advertising IDを使用して [!DNL Analytics Marketing Channels]の処理ルールを作成する方法を説明します。
feature: Integration with Adobe Analytics
exl-id: 525761b4-607f-4b03-9020-8051009a13c6
TQID: https://experienceleague.adobe.com/mBjU1jKifWk35v43sGsBO5aHDQA5ftmyI9GJ4Xujz9A
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1448
ht-degree: 0%

---

# Adobe Advertising IDを使用して[!DNL Marketing Channels]処理ルールを作成する

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

Adobe Advertising ID （[AMO IDおよびEF ID](../ids.md)）を使用して、Adobe Analyticsで[!DNL Marketing Channels]処理ルールを設定できます。 Adobe Advertising キャンペーンに固有のルールには、Adobe Advertising IDを使用します。 ルールを処理する順序によって、可能なすべてのデータが正しくキャプチャされるかどうかが決まります。

## 処理ルールのAMO ID

AMO IDは、[!DNL Analytics]内のAdobe Advertising データのレポートに使用される主要なトラッキングコードです。 AMO IDは、[!DNL Analytics]内で詳細なレポートを提供するためにAdobeによって管理される動的値の連結です。 [!DNL Analytics] [eVar](https://experienceleague.adobe.com/docs/analytics/components/dimensions/evar.html?lang=ja)またはrVar ディメンション （AMO ID）に保存されています。 AMO IDは、[!DNL Analytics]で次の2つの方法で設定できます。

* クリックスルー追跡：Adobe Advertisingは`s_kwcid` クエリ文字列パラメーターをリンクに設定し、[!DNL Analytics]はクリックスルーが発生したときにランディングページ URLからパラメーターを取得します。

* ビュースルー追跡（[!DNL DSP]のみ）: [!DNL Last Event Service]はサーバーサイドのビュースルーを検出し、AMO IDを[!DNL Analytics]に送信します。 この場合、URLに`s_kwcid` パラメーターが含まれていません。

AMO ID内の動的な値は、追跡されたマーケティングチャネルを示します。

* AMO IDのプレフィックスを使用して、[!DNL Marketing Channels]内のトップレベル チャネルを識別できます。

* AMO IDの本文の文字フレーズは、より特定のキャンペーンタイプを示します。

* 接尾辞「vt」は[!DNL DSP] ビュースルーのトラフィックに存在し、[!DNL DSP] チャネルのクリックスルーとビュースルーを個別に作成するために使用できます。

AMO IDの残りの部分は無視できます。

| [!UICONTROL AMO ID] | チャネル | ルール論理 |
|--------|---------|--------------------|
| !ctv （接尾辞） | [!UICONTROL DSP Connected TV ViewThrough] | 次で終わる |
| !d! （本文） | [!UICONTROL Display Network] | 次を含む |
| !g! （本文） | [!UICONTROL Google Search] | 次を含む |
| !s! （本文） | [!UICONTROL Search Partner] | 次を含む |
| !u! （本文） | [!UICONTROL Smart Shopping Campaign] | 次を含む |
| !ytv! （本文） | [!UICONTROL YouTube Video Ad] | 次を含む |
| !yts! （本文） | [!UICONTROL YouTube Search Ad] | 次を含む |
| !vp! （本文） | [!UICONTROL Google Video Partners] | 次を含む |
| !vt （接尾辞） | [!UICONTROL DSP ViewThrough] | 次で終わる |
| アル！ （接頭辞） | [!UICONTROL Paid Search] | 次で始まる |
| AC! （接頭辞） | [!UICONTROL DSP Display] | 次で始まる |

## 処理ルールのEF ID

AMO EF ID （EF ID）は、[!DNL Analytics for Advertising]統合で使用される2番目のトラッキングコードです。 主な目的は、[!DNL Analytics] イベントデータを追跡してAdobe Advertisingに渡すことです。 クリックスルーまたはビュースルーが発生するたびに、同じ訪問者に対してまったく同じ広告であっても、一意のEF IDが生成されます。 EF IDは、[!DNL Analytics] レポート ユーザーインターフェイスでは使用されません。これは、通常、[!DNL Analytics]の変数当たりの一意の値が500 kを超えるため、レポートに使用できません。 Adobe Advertisingの指標とメタデータは、EF IDには適用されません。AMO IDにのみ適用されます。 Adobe Advertisingのキャンペーンの最適化には、トラッキングの詳細な設定が必要なため、両方のIDが必要です。

EF ID ディメンションは、[!DNL Analytics] レポートでは直接使用されませんが、EF IDはマーケティングチャネルの作成に役立ちます。 EF ID サフィックスは、チャネル（表示または検索）と、訪問がクリックスルーまたはビュースルーによって推進されたかどうかを示します。 EF IDの区切り文字は、AMO IDの感嘆符ではなくコロンです。

| EF ID サフィックス | チャネル |
|-------|---------|
| :s | [!UICONTROL Paid Search Click-through] |
| :d | [!UICONTROL Display ClickThrough] |
| :i | [!UICONTROL Display ViewThrough] |

## Adobe Advertisingの処理ルールの例

次のルールセットの例では、広告チャネル（有料検索、表示クリックスルー、表示ビュースルー）のルールに焦点を当てます。 有料検索検出の推奨ルール（そのルールが自然検索マーケティングチャネルロジックとどのように相互作用するかを含む）と、自然参照ドメインルールに対するオプションの更新も示されます。

**注意：**&#x200B;表示は、広告主の環境設定に基づいて2つのチャネルとして分離するか、1つのチャネルに統合することができます。

その他のチャネルは、一般的な実装における広告チャネルと他のチャネルの推奨される運用順序を示すために、サンプルのスクリーンショットに含まれます。

>[!IMPORTANT]
>
>ルールを処理する順序について詳しくは、「[&#x200B; ルール  [!DNL Marketing Channels] 」の「](#rule-order)操作順序」を参照してください。

![処理ルールのセットの例](/help/integrations/assets/a4adc-mc-rule-set-example.png)

### 有料検索ルール

ベストプラクティスは、[!UICONTROL Paid Search] ルールの「Any」演算子に2つの条件を含めることです。

* コスト/クリック/インプレッションデータにはAMO IDが含まれているので、AMO IDを含めます。 AMO IDは「AL!」で始まる必要があります。 クリック/コスト/インプレッションのデータを[!UICONTROL Paid Search]に正しく割り当てる。<!-- Is this just called AMO ID there, not s_kwcid=XXX? What's the difference? -->

* [!UICONTROL Paid Search] クリックスルーのURLには、常に`s_kwcid` クエリ文字列パラメーターが含まれるため、訪問者がランディングページに戻る場合に適切な重複排除が行われるように、URLを含めます。 「AL!」を含める クリック/コスト/インプレッション データを`s_kwcid`に正しく割り当てるために[!UICONTROL Paid Search]の前に行います。

チャネルの値をAMO IDに設定しないでください。 代わりに、「参照ドメイン」、「検索エンジン + キーワード」、「ページ」などに設定します。 （これは、すべての[!DNL Marketing Channels]に関連しています）。

<!-- Explain that comment about relevancy -- do I need to repeat this for each rule example?  -->

![有料検索ルールの例](/help/integrations/assets/a4adc-mc-rule-paid-search.png "有料検索ルールの例")

### 自然検索ルール

[!UICONTROL Natural Search]の場合、[[!UICONTROL Paid Search]検出ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/t-paid-search-detection)に`ef_id`と`s_kwcid`のクエリ文字列パラメーターが含まれていることを確認してください。 （通常、これはAdvertising Search、Social、およびCommerceが[!DNL Analytics]に統合されている場合に自動的に設定されますが、統合が設定された後に[!DNL Analytics]管理者がロジックを変更した場合は検証します）。

ルールを「自然検索検出ルールに一致」に設定します（通常、このチャネルのデフォルト設定です）。

![自然検索ルールの例](/help/integrations/assets/a4adc-mc-rule-natural-search.png "自然検索ルールの例")

### クリックスルー規則#1の表示

クリックスルーのみをキャプチャして、ディスプレイのクリックスルーマーケティングチャネルを作成します。 AMO IDはクリックスルーとビュースルーの両方で同じであるため、このルールではEF ID変数と`ef_id` クエリ文字列パラメーターを使用します。

クリックスルーは、URL （デフォルト）を通じて追跡されることがあります。 それ以外の場合、クリックスルーはサーバーサイドの最後のイベントサービスを通じて追跡されるため、URLに`ef_id` パラメーターが含まれていません。 したがって、ルールは、EF ID変数または`ef_id` クエリ文字列パラメーターが「:d」で終わる条件をチェックします。 このルールをいずれかの条件に対してトリガーする必要があるので、「`Any`」演算子を使用します。

![最初の表示クリックスルー規則の例](/help/integrations/assets/a4adc-mc-rule-display-ct.png "最初の表示クリックスルー規則の例")

### 自然参照ドメインのルール

（オプション）ベストプラクティスは、「任意」演算子を使用して「訪問の最初のページです」条件を標準の[!UICONTROL Natural Referring Domains] ルールに追加することです。 このルールはオプションですが、ユーザーが「戻る」ボタンをクリックしてランディングページに戻ったときに、自然参照のエッジケースが設定されるのを防ぐのに役立ちます。

![自然参照ドメイン ルールの例](/help/integrations/assets/a4adc-mc-rule-natural-referring-domains.png "自然参照ドメイン ルールの例")

### CTV ビュースルールールの表示

[!DNL DSP]個のコネクテッド TV （CTV） ビュースルーを追跡するには、AMO IDが`"!ctv"`で終わるルールを作成します。 訪問者が広告をクリックしていないため、ビュースルートラッキングにはURLに`ef_id`または`s_kwcid`が含まれず、ルールには1つの条件のみが必要です。

![&#x200B; ディスプレイ CTV ビュースルー規則の例](/help/integrations/assets/a4adc-mc-rule-display-ctv-vt.png " ディスプレイ CTV ビュースルー規則の例")

### ビュースルー規則の表示

表示ViewThrough チャネルを作成するには、EF IDが「:i」で終わるルールを作成します。 訪問者が広告をクリックしていないため、ビュースルートラッキングにはURLに`ef_id`または`s_kwcid`が含まれず、ルールには1つの条件のみが必要です。

![表示ビュースルー規則の例](/help/integrations/assets/a4adc-mc-rule-display-vt.png "表示ビュースルー規則の例")

### クリックスルー規則#2の表示

2つ目のクリックスルー表示ルールの場合、**AMO IDは「AC!」で始まります。**。 この2つ目のルールは、Adobe Advertisingから[!DNL Analytics]に直接送られる表示チャネルのクリック/コスト/インプレッションデータを取得するために存在します。 このデータはAMO IDに関連付けられていますが、`ef_id` クエリ文字列を持つURLが含まれていないため、これらのヒットはAMO EF IDに接続されません。これは、最初の表示クリックスルールールでキャプチャしたものです。

![2番目の表示クリックスルー規則の例](/help/integrations/assets/a4adc-mc-rule-display-ct2.png "2番目の表示クリックスルー規則の例")

## [!DNL Marketing Channels] ルールの操作順序 {#rule-order}

![Adobe Advertising関連の規則に対する理想的な作業順序](/help/integrations/assets/a4adc-mc-rule-order.png "Adobe Advertising関連の規則に対する理想的な作業順序")

* [!UICONTROL Paid Search] *before* [!UICONTROL Natural Search]を配置します。 そうでなければ、有料検索データは自然検索に割り当てられる可能性があります。

* **first** [!UICONTROL Display ClickThrough] *before* [!UICONTROL Natural Referring Domains]と[!UICONTROL Natural Social]を配置します。

* [!UICONTROL CTV view-throughs]を使用する場合は、*before* [!UICONTROL Display ViewThroughs]と入力します。 それ以外の場合、CTV ビュースルーはディスプレイビュースルーとしてキャプチャされます。

* ビュースルーと[!UICONTROL Display ViewThroughs]以外のクリックスルーが同じランディングイベントで発生する可能性があるので、**&#x200B;後[!UICONTROL Internal]の他のチャネルを[!UICONTROL Direct]および[!DNL Advertising]前に配置します。 例えば、訪問者がAdobe Advertisingの広告を見てインプレッションを受け取り、[!UICONTROL Natural Search]経由でサイトに移動する場合があります。

  ベストプラクティスは、ビュースルーよりも他のチャネル（[!UICONTROL Internal]と[!UICONTROL Direct]を除く）を優先することです。

* 一部の広告主は、[!UICONTROL Display ViewThroughs]よりも[!UICONTROL Natural Referring Domains]を優先する場合があります。 これは、2つのルールの処理順序を入れ替えて行います。

* **second** [!UICONTROL Display ClickThrough] ルールは、Adobe Advertisingから[!DNL Analytics]に直接送られてくるクリック/コスト/インプレッションのデータを取得するためのものです。 このデータはAMO IDにのみ関連付けられているため、これらのヒットはAMO EF IDに接続されません。 このルールを設定しない場合、すべてのクリック/コスト/インプレッション データは[!UICONTROL Direct] チャネルに属します。これは、[!DNL Marketing Channel]と一致しないデータのデフォルト チャネルです。 このルールは、ビュースルー規則の&#x200B;*後*&#x200B;に来る必要があります。そうしないと、ビュースルー規則が取得されます。

<!-- WORDING!!!!  Check on this, and if it's necessary still with the other info about order:  If you include additional marketing channels, be sure to run your rules in order of specificity. For example, say you create a processing rule for [!DNL YouTube] video ad traffic tracked by Advertising Search, Social, & Commerce. The AMO ID for video traffic starts with with "AL!" and contain "!ytv!". If you run the rule for Paid Search (for which the AMO ID starts with "AL!") and then run the rule for video traffic, the YouTube video ad traffic would all fall under the Paid Search channel. -->

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertisingと [!DNL Marketing Channels]](mc-data-variances.md)でチャネルデータが異なる理由
>* [Adobe Advertising data [!DNL Analytics Marketing Channels] での](mc-ac-data.md)の使用
>* [&#x200B; ビデオ： [!DNL Marketing Channels] をAdobe Advertising レポートに使用](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=ja)
>* [様が使用している [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID