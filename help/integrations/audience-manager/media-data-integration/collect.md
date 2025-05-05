---
title: Advertising DSP キャンペーンからクリックおよびインプレッションデータを収集
description: Audience Managerピクセルを使用してAdvertising DSP広告から cookie ベースのインプレッションとクリックイベントをキャプチャする方法を説明します
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# Advertising DSP キャンペーンからメディア露出データを収集

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを行う広告主*

このドキュメントでは、Advertising DSP広告にタグを付けて cookie ベースのインプレッションとクリックイベントをAudience Managerピクセルでキャプチャする方法と、データを使用するために必要な追加のタスクについて説明します。

イベントピクセルでは、モバイルアプリやコネクテッド テレビ（CTV）など、cookie のない環境で発生するイベントはキャプチャされません。

## 手順 1:Audience Managerでの Data Sourceの設定 {#set-up-data-source}

Audience Managerで、DSP インプレッション用の [ データソース ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html) を作成し、「データ」をクリックします。 追跡されたすべてのイベントがデータソースに関連付けられるように [&#128279;](#implement-dsp-pixels) 各イベントタグにデータソース ID を含めます。

>[!NOTE]
> 1 つのデータソース内の複数のDSPで実行されている広告キャンペーンに対して、すべてのインプレッションおよびクリックデータを収集できます。

## 手順 2:Web ページへのインプレッションの実装とクリックイベントピクセル {#implement-dsp-pixels}

広告主は、独自のブランドのイベントタグを作成および実装できます。 必要に応じて、Adobe Audience Manager コンサルタントまたはAdobeアカウントチームに連絡し、サポートを受けてください。

>[!NOTE]
>
>組織で [!DNL Analytics] トラッキングを使用している場合は、Audience Managerのクリックのトラッキングは不要な場合があります。 Adobe Analyticsは、クリック信号をキャプチャし、[ サーバーサイド転送 ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) を介してAudience Managerに送信できます。

### ピクセル構文

イベントピクセルには、次のパラメーターを含める必要があります。

**インプレッショントラッキングのピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[ オプションの追加パラメーター ](#parameters) の前に `&` が付いたもの

**クリック追跡ピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[ オプションの追加パラメーター ](#parameters) の前に `&` が付いたもの

ここで、

* `[Audience Manager customer domain]` は、インプレッションまたはクリックイベントを [!DNL Adobe] に送信するドメイン名です。

* `[source id]` は、DSP インプレッションをトラッキングし、データをクリックする [ データソース ](#set-up-data-source) の ID です。

* `[redirect URL]` はダブルエンコードされたリダイレクト URL です。 www.urlencoder.orgなどのオンラインエンコーディングツールを使用している場合は、エンコーダーを介して文字列を実行し、結果を再エンコードします。

* `${TM_CAMPAIGN_ID_NUM}` はDSPの数値キャンペーン ID です。 DSP マクロを使用する代わりに個々のキャンペーン ID をハードコードする場合は、キャンペーン設定で ID を見つけます。

* 各 [ パラメーター ](#key-value-pairs) の先頭には `&` が付き、`d_parameter=parameter_id` の形式になります。`parameter` は、新しいフィールドのキーと値のペアに置き換えられます。 例：`&d_placement=${TM_PLACEMENT_ID_NUM}`

### キーと値のペアとしてのパラメーター {#parameters}

**形式：** `d_parameter=parameter_id`

    where:
    
    * パラメーターの先頭は&#39;&amp;&#39;
    
    * &#39;parameter&#39;で、新しいフィールドのキーと値のペアが置き換えられます 
    
     例：&#39;&amp;d_placement=${TM_PLACEMENT_ID_NUM}&#39;

どちらのタイプのピクセルにも、特性を収集したり、他のレポートにキャンペーンメタデータ *プレースメント名やキャンペーン名など）を提供したりするための追加のパラメーター* キー値ペア）を含めることができます。 キーと値のペアは、関連する 2 つの要素で構成されます。1 つ *キー* はデータセットを定義する定数、もう 1 つは *値* はセットに属する変数です。

このキーと値のペアでは、値変数は、ハードコードされた ID または *マクロ* のどちらかです。これは、キャンペーンおよびユーザートラッキングのために広告タグが読み込まれるときに、対応する値に動的に置き換えられる、自己完結型の小さなユニットです。 キャンペーン関連のパラメーターの場合、Audience Managerマクロの代わりに [DSP マクロを使用して ](/help/dsp/campaign-management/macros.md) キャンペーン属性を対応するインプレッションまたはクリックデータと共に、すべての広告にわたって 1 つのピクセルを使用してAudience Managerに送信できます。 イベントピクセルに挿入するDSP マクロは、ピクセル内に含めるキーと値のペアに適した値である必要があります。 例えば、`d_placement` キーの場合、DSP マクロ `${TM_PLACEMENT_ID_NUM}` を値として使用して、Adobe Advertisingマクロで生成されたプレースメント ID を取得します。

Audience Managerがインプレッションイベントピクセルでサポートするマクロのリストについては、「[ ピクセル呼び出しを使用したキャンペーンのインプレッションデータのキャプチャ ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html#supported-key-value-pairs)」を参照してください。

Audience Managerがクリックイベントピクセルでサポートするマクロのリストについては、「[ ピクセル呼び出しを使用したキャンペーンクリックデータのキャプチャ ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html)」を参照してください。

>[!TIP]
>
>* ベストプラクティスは、キャンペーン、プレースメント、クリエイティブ（広告）およびサイト ID を含めて、キャンペーン属性を使用してAudience Manager特性を作成できるようにすることです。
>* Audience Optimizationレポートを作成するには、さらにパラメーターが必要です。
>* キーと値のペアでは、値を関連する [DSP マクロに置き換えて ](/help/dsp/campaign-management/macros.md) すべてのキャンペーンのすべての広告で 1 つのピクセルを使用できるようにします。 例えば、`d_campaign=[%campaignID%]` を `d_campaign=${TM_CAMPAIGN_ID_NUM}` に変更すると、Adobe Advertisingマクロで生成されたキャンペーン ID を取り込むことができます。
>* 必要に応じて、ハードコードされた値を使用して独自のパラメーターを作成できます。 例：`d_DSP=AdCloud`

インプレッションイベントピクセルの例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### ピクセルの追加先

#### インプレッショントラッキングピクセル

[!DNL DSP] キャンペーン内のすべての広告にインプレッションイベントトラッキングピクセルを添付します。 次の場所のいずれかで実行できます。

* プレースメントレベル。デフォルトでは、プレースメント内のすべての広告にピクセルを適用します。 プレースメント設定の「トラッキング」セクションで、[[!UICONTROL Event pixels] フィールドにピクセルを追加します ](/help/dsp/campaign-management/placements/placement-settings.md)。

* 広告レベルで。これは、プレースメントレベルのイベントピクセルを上書きします。 広告設定で、[ 「[!UICONTROL Pixel]」タブにイベントピクセルを作成します ](/help/dsp/campaign-management/ads/ad-edit.md)。

* （サードパーティの広告サーバーでの広告の場合）広告サーバー内の広告レベル。

#### クリック追跡ピクセル

広告サーバー内で、通常広告のクリックスルー URL を挿入する場所には、クリックイベントピクセル（エンコードされた URL が追加されたもの）を挿入します。

## 手順 3：実装後のタスク

イベント・タグが実装されると、データはAudience Managerデータ収集サーバに送られます。 レポートでデータを使用する前に、次のタスクを完了してください。

### [!DNL Amazon S3] バケットとデータSourceの作成

データがAudience Managerサーバーに送信されたら、[!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]）バケットを作成した後、すべてのピクセルデータが送信されるデータソースを作成する必要があります。 サポートが必要な場合は、担当のAudience Managerコンサルタントまたは [ カスタマーケア ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html) にお問い合わせください。

### Audience Managerの特性とセグメントの作成

イベントデータは、[ 未使用のシグナル ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html) としてAudience Managerに送られます。 取り込んだデータから [ ルールベースの特性 ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html) を手動で作成し、その特性を使用して [ セグメント ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html) を作成してから、レポートでデータを使用できます。

DSPで特定のクリエイティブに公開されたユーザーにユーザーレベルのデータを入力する特性の例は次のとおりです。

1. イベントを `d_event = imp` として識別します。
1. DSP キャンペーン内でクリエイティブ ID を特定し、`d_creative=[Creative ID]` のように特性にマッピングします。

![ 特性作成画面 ](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP マクロ ](/help/dsp/campaign-management/macros.md)
>* [DSP Media のAdobe Audience Managerへの公開データ送信の概要 ](overview.md)
>* [ ユースケース ](use-cases.md)
