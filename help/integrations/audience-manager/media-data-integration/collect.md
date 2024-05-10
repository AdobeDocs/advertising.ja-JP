---
title: Advertising DSP キャンペーンからクリックとインプレッションのデータを収集
description: Audience Managerピクセルを使用して Advertising DSP広告から cookie ベースのインプレッションとクリックイベントをキャプチャする方法を説明します
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Advertising DSP キャンペーンからメディア露出データを収集

*Advertising DSPのみを使用する広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを持つ広告主*

このドキュメントでは、Audience Managerピクセルを使用して cookie ベースのインプレッションとクリックイベントをキャプチャするための Advertising DSP広告にタグ付けする方法と、データを使用するために必要な追加のタスクについて説明します。

イベントピクセルでは、モバイルアプリやコネクテッド テレビ（CTV）など、cookie のない環境で発生するイベントはキャプチャされません。

## 手順 1:Audience Managerでのデータソースの設定 {#set-up-data-source}

Audience Managerーで、 [データソース](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) をDSP インプレッションに設定し、「データ」をクリックします。 データソース ID を含める [各イベントタグ内](#implement-dsp-pixels) そのため、トラッキングされるすべてのイベントはデータソースに関連付けられます。

>[!NOTE]
> 1 つのデータソース内の複数のDSPで実行されている広告キャンペーンに対して、すべてのインプレッションおよびクリックデータを収集できます。

## 手順 2:Web ページへのインプレッションの実装とクリックイベントピクセル {#implement-dsp-pixels}

広告主は、独自のブランドのイベントタグを作成および実装できます。 必要に応じて、Adobe Audience Manager コンサルタントまたはAdobeアカウントチームに連絡し、サポートを受けてください。

>[!NOTE]
>
>組織がを使用している場合 [!DNL Analytics] トラッキングの場合、Audience Managerのクリックのトラッキングは不要な場合があります。 Adobe Analyticsは、クリック信号をキャプチャし、次の経路でAudience Managerに送信できます [サーバーサイド転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html).

### ピクセル構文

イベントピクセルには、次のパラメーターを含める必要があります。

**インプレッショントラッキングのピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

（を使用） [オプションの追加パラメーター](#parameters) 先頭にが付いている `&`

**クリック追跡ピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

（を使用） [オプションの追加パラメーター](#parameters) 先頭にが付いている `&`

ここで、

* `[Audience Manager customer domain]` は、インプレッションまたはクリックイベントを送信するドメイン名です。 [!DNL Adobe].

* `[source id]` は、の ID です。 [データソース](#set-up-data-source) でDSP インプレッションをトラッキングし、データをクリックします。

* `[redirect URL]` はダブルエンコードされたリダイレクト URL です。 www.urlencoder.orgなどのオンラインエンコーディングツールを使用している場合は、エンコーダーを介して文字列を実行し、結果を再エンコードします。

* `${TM_CAMPAIGN_ID_NUM}` は、DSPの数値キャンペーン ID です。 DSP マクロを使用する代わりに個々のキャンペーン ID をハードコードする場合は、キャンペーン設定で ID を見つけます。

* Each [パラメーター](#key-value-pairs) というプレフィックスが付いた `&` とは形式です `d_parameter=parameter_id`、ここで `parameter` は、新しいフィールドのキーと値のペアに置き換えられます。 例： `&d_placement=${TM_PLACEMENT_ID_NUM}`

### キーと値のペアとしてのパラメーター {#parameters}

**形式：**  `d_parameter=parameter_id`

    ここで、
    
    * パラメーターの先頭には「&amp;」が付きます
    
    * 「パラメーター」は、新しいフィールドのキーと値のペアに置き換えられます
    
    例：&#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

どちらのタイプのピクセルにも、次のような追加パラメーターを含めることができます。 *キーと値のペア* 特性を収集したり、他のレポートにキャンペーンメタデータ（プレースメント名やキャンペーン名など）を提供したりできます。 キーと値のペアは、関連する 2 つの要素、 *キー*（データセットを定義する定数）と *value*：セットに属する変数です。

このキーと値のペアでは、値変数は、ハードコーディングされた ID または *マクロ*&#x200B;これは、キャンペーンおよびユーザートラッキング用に広告タグが読み込まれるときに、対応する値に動的に置き換えられる、自己完結型コードの小さな単位です。 キャンペーン関連のパラメーターには、を使用できます [DSP マクロ](/help/dsp/campaign-management/macros.md) Audience Managerマクロの代わりに、キャンペーン属性を対応するインプレッションまたはクリックデータと共にAudience Managerに送信し、すべての広告にわたって 1 つのピクセルを使用します。 イベントピクセルに挿入するDSP マクロは、ピクセル内に含めるキーと値のペアに適した値である必要があります。 例えば、 `d_placement` キーを押すと、DSP マクロを使用します `${TM_PLACEMENT_ID_NUM}` を、Adobe Advertisingマクロで生成されたプレースメント ID を取得するための値として使用します。

Audience Managerがインプレッションイベントピクセルでサポートするマクロのリストについては、「」を参照してください[ピクセル呼び出しを使用したキャンペーンのインプレッションデータのキャプチャ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs).」と入力します。

Audience Managerがクリックイベントピクセルでサポートするマクロのリストについては、「」を参照してください[ピクセル呼び出しを使用したキャンペーンのクリックデータのキャプチャ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html).」と入力します。

>[!TIP]
>
>* ベストプラクティスは、キャンペーン、プレースメント、クリエイティブ（広告）およびサイト ID を含めて、キャンペーン属性を使用してAudience Manager特性を作成できるようにすることです。
>* Audience Optimizationレポートを作成するには、さらにパラメーターが必要です。
>* キーと値のペアで、値を関連する [DSP マクロ](/help/dsp/campaign-management/macros.md) したがって、すべてのキャンペーンのすべての広告で 1 つのピクセルを使用できます。 例えば、 `d_campaign=[%campaignID%]`対象： `d_campaign=${TM_CAMPAIGN_ID_NUM}` Adobe Advertisingマクロで生成されたキャンペーン ID を取得します。
>* 必要に応じて、ハードコードされた値を使用して独自のパラメーターを作成できます。 例： `d_DSP=AdCloud`

インプレッションイベントピクセルの例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### ピクセルの追加先

#### インプレッショントラッキングピクセル

すべての広告にインプレッションイベントトラッキングピクセルを添付 [!DNL DSP] キャンペーン。 次の場所のいずれかで実行できます。

* プレースメントレベル。デフォルトでは、プレースメント内のすべての広告にピクセルを適用します。 プレースメント設定の「トラッキング」セクションで、にピクセルを追加します [[!UICONTROL Event pixels] フィールド](/help/dsp/campaign-management/placements/placement-settings.md).

* 広告レベルで。これは、プレースメントレベルのイベントピクセルを上書きします。 広告設定で、 [でイベントピクセルを作成 [!UICONTROL Pixel] タブ](/help/dsp/campaign-management/ads/ad-edit.md).

* （サードパーティの広告サーバーでの広告の場合）広告サーバー内の広告レベル。

#### クリック追跡ピクセル

広告サーバー内で、通常広告のクリックスルー URL を挿入する場所には、クリックイベントピクセル（エンコードされた URL が追加されたもの）を挿入します。

## 手順 3：実装後のタスク

イベント・タグが実装されると、データはAudience Managerデータ収集サーバに送られます。 レポートでデータを使用する前に、次のタスクを完了してください。

### を作成 [!DNL Amazon S3] バケットとデータソース

データがAudience Managerサーバーに送信されたら、 [!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）バケットの後、すべてのピクセルのデータの送信先となるデータソースに移動します。 Audience Managerコンサルタントに問い合わせるか、 [カスタマーケア](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) サポートが必要な場合。

### Audience Managerの特性とセグメントの作成

イベントデータは、次のようにAudience Managerに送られます [未使用のシグナル](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html). 手動で作成 [ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) を作成します [セグメント](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) レポートでデータを使用する前に、これらの特性を使用します。

DSPで特定のクリエイティブに公開されたユーザーにユーザーレベルのデータを入力する特性の例は次のとおりです。

1. イベントをとして識別 `d_event = imp`.
1. DSP キャンペーン内でクリエイティブ ID を特定し、次のように特性にマッピングします `d_creative=[Creative ID]`.

![特性作成画面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP マクロ](/help/dsp/campaign-management/macros.md)
>* [DSP Media のAdobe Audience Managerへの公開データ送信の概要](overview.md)
>* [ユースケース](use-cases.md)
