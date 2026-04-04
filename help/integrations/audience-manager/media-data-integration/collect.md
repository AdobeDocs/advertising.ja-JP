---
title: Advertising DSPのキャンペーンからクリック&インプレッションデータを収集できます
description: Audience Manager pixelsを使用してAdvertising DSP広告からCookie ベースのインプレッションをキャプチャし、クリックイベントをキャプチャする方法を説明します
feature: Integration with Adobe Audience Manager
exl-id: d827fbb8-b61a-4601-a42a-1ea60e4f36b7
TQID: https://experienceleague.adobe.com/UXP1gmCmLCHH-l7a1WYxlmYfSRIgJPLpxWHyHujIdX0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 3b9845e85cd91cdece195593b43cbaf851368f9e
workflow-type: tm+mt
source-wordcount: 991
ht-degree: 0%

---

# Advertising DSPのキャンペーンからメディア露出データを収集します

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを使用する広告主*

このドキュメントでは、Audience Manager ピクセルを使用してAdvertising DSP広告をタグ付けし、cookie ベースのインプレッションとクリックイベントをキャプチャする方法と、データを使用するために必要な追加のタスクについて説明します。

イベントピクセルは、モバイルアプリやコネクテッド TV （CTV）など、Cookieのない環境で発生するイベントを捉えることはできません。

## 手順1: Audience Managerでのデータソースの設定 {#set-up-data-source}

Audience Managerで、DSP インプレッション用の[&#x200B; データソース &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/data-sources/datasources-list-and-settings.html?lang=ja)を作成し、「データ」をクリックします。 追跡されたすべてのイベントがデータソースに関連付けられるように、各イベントタグ [にデータソース ID &#x200B;](#implement-dsp-pixels)を含めます。

>[!NOTE]
> 単一のデータソース内で、複数のDSPで実行されている広告キャンペーンのインプレッションとクリックのデータをすべて収集することができます。

## ステップ 2:web ページにインプレッションを実装し、イベントピクセルをクリックする {#implement-dsp-pixels}

広告主は、自社ブランドのイベントタグを作成し、実装することができます。 必要に応じて、Adobe Audience Manager コンサルタントまたはAdobe アカウントチームにお問い合わせください。

>[!NOTE]
>
>お客様の組織で[!DNL Analytics] トラッキングを使用している場合は、Audience Manager クリック トラッキングが不要になる可能性があります。 Adobe Analyticsはクリックのシグナルをキャプチャし、[&#x200B; サーバーサイド転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html?lang=ja)を通じてAudience Managerに送信できます。

### ピクセル構文

イベントピクセルには、次のパラメーターを含める必要があります。

**インプレッション追跡ピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=imp&d_src=[source id]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[&#x200B; オプションの追加パラメーター](#parameters)が`&`で始まる

**クリックトラッキングピクセル：**

`[Audience Manager customer domain].demdex.net/event?d_event=click&d_src=[source id]&d_rd=[redirect URL]&d_campaign=${TM_CAMPAIGN_ID_NUM}`

[&#x200B; オプションの追加パラメーター](#parameters)が`&`で始まる

どこで：

* `[Audience Manager customer domain]`は、インプレッションまたはクリック イベントを[!DNL Adobe]に送信するドメイン名です。

* `[source id]`は、[&#x200B; データソース &#x200B;](#set-up-data-source)のIDで、DSP インプレッションとクリックデータを追跡します。

* `[redirect URL]`は二重エンコードされたリダイレクト URLです。 www.urlencoder.orgなどのオンラインエンコーディングツールを使用している場合は、エンコーダーを通して文字列を実行し、結果を再エンコードします。

* `${TM_CAMPAIGN_ID_NUM}`はDSPのキャンペーン IDの数値です。 DSP マクロを使用せずに個々のキャンペーン IDをハードコーディングする場合は、キャンペーン設定でIDを見つけます。

* 各[&#x200B; パラメーター](#key-value-pairs)には`&`というプレフィックスが付けられ、`d_parameter=parameter_id`という形式で指定されます。この形式では、`parameter`は新しいフィールドのキーと値のペアに置き換えられます。 例：`&d_placement=${TM_PLACEMENT_ID_NUM}`

### キーと値のペアとしてのパラメーター {#parameters}

**形式：** `d_parameter=parameter_id`

どこで：

* パラメーターの先頭には`&`が付きます

* `parameter`は、新しいフィールドのキーと値のペアに置き換えられます

*例：* `&d_placement=${TM_PLACEMENT_ID_NUM}`

両方のタイプのピクセルには、特性を収集したり、他のレポートにキャンペーンメタデータ（プレースメント名やキャンペーン名など）を提供したりするために、*キーと値のペア*&#x200B;という追加のパラメーターを含めることができます。 キーと値のペアは、データセットを定義する定数である&#x200B;*キー*&#x200B;と、セットに属する変数である&#x200B;*値*&#x200B;の2つの関連要素で構成されます。

キーと値のペアでは、値変数はハードコードされたIDか、*マクロ*&#x200B;のいずれかになります。これは、広告タグがキャンペーンとユーザー追跡のために読み込まれたときに、対応する値に動的に置き換えられる自己完結型コードの小単位です。 キャンペーン関連のパラメーターの場合は、Audience Manager マクロの代わりに[DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)を使用して、キャンペーン属性を対応するインプレッションと一緒に送信したり、クリックデータをAudience Managerに送信したりして、すべての広告で1 ピクセルを使用したりできます。 イベントピクセルに挿入するDSP マクロは、ピクセル内に含めるキーと値のペアに適した値である必要があります。 例えば、`d_placement` キーの場合、Adobe Advertising マクロ `${TM_PLACEMENT_ID_NUM}`を値として使用して、DSP マクロによって生成されたプレースメント IDを取得します。

Audience Managerがインプレッションイベントピクセルに対してサポートするマクロの一覧については、「[Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/impression-data-pixels.html?lang=ja#supported-key-value-pairs)を使用したキャンペーンインプレッションデータのキャプチャ」を参照してください。

Audience Managerがクリックイベントピクセルに対応しているマクロの一覧については、「[Pixel Calls](https://experienceleague.adobe.com/docs/audience-manager/user-guide/implementation-integration-guides/media-data-integration/click-data-pixels.html?lang=ja)を使用したCampaign クリックデータのキャプチャ」を参照してください。

>[!TIP]
>
>* ベストプラクティスは、キャンペーン、プレースメント、クリエイティブ（広告）、およびサイト IDを含めることです。これにより、キャンペーン属性を使用してAudience Manager特性を作成できます。
>* Audience Optimization レポートを作成するには、追加のパラメーターが必要です。
>* キーと値のペアで、値を関連する[DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)に置き換えて、すべてのキャンペーンのすべての広告で1つのピクセルを使用できるようにします。 例えば、`d_campaign=[%campaignID%]`を`d_campaign=${TM_CAMPAIGN_ID_NUM}`に変更して、Adobe Advertising マクロによって生成されたキャンペーン IDをキャプチャします。
>* 必要に応じて、ハードコードされた値を使用して独自のパラメーターを作成できます。 例：`d_DSP=AdCloud`

インプレッションイベントピクセルの例：

`http://acme.demdex.net/event?d_event=imp&d_src=1052880&d_site=${TM_SITE_ID_NUM}&d_creative=${TM_AD_ID_NUM}&d_placement=${TM_FEED_ID_NUM}&d_campaign=${TM_CAMPAIGN_ID_NUM}&d_DSP=AdCloud&d_bust=${TM_RANDOM}`

### ピクセルの追加場所

#### インプレッション追跡ピクセル

インプレッションイベント追跡ピクセルを、[!DNL DSP] キャンペーンのすべての広告に添付します。 次のいずれかの場所で行うことができます。

* プレースメントレベルで、プレースメント内のすべての広告にデフォルトでピクセルを適用します。 プレースメント設定の「トラッキング」セクションで、[[!UICONTROL Event pixels] フィールド &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)にピクセルを追加します。

* 広告レベルでアセットを配信し、広告配信レベルのイベントピクセルを。 広告設定で、[&#x200B; 「[!UICONTROL Pixel]」タブにイベントピクセルを作成](/help/dsp/campaign-management/ads/ad-edit.md)。

* （サードパーティ広告サーバーの広告の場合）広告サーバー内の広告レベル。

#### クリックトラッキングピクセル

広告サーバー内で、通常は広告のクリックスルーURLを挿入する場所に、（エンコードされたURLが付加された）クリックイベントピクセルを挿入します。

## 手順3：実装後のタスク

イベントタグが実装されると、データはAudience Manager Data Collection Serverに取り込まれます。 レポートでデータを使用する前に、次のタスクを完了します。

### [!DNL Amazon S3] バケットとデータソースの作成

データがAudience Manager サーバーに取り込まれたら、[!DNL Amazon Simple Storage Service] （[!DNL Amazon S3]） バケットを作成してから、すべてのピクセルデータが送信されるデータソースを作成する必要があります。 サポートが必要な場合は、Audience Manager コンサルタントまたは[&#x200B; カスタマーケア &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/help-and-legal/help-legal-contact.html?lang=ja)にお問い合わせください。

### Adobe Audience Managerの特性とセグメントの構築

イベントデータは、[未使用のシグナル &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/interactive-and-overlap-reports/unused-signals.html?lang=ja)としてAudience Managerに取り込まれます。 取り込んだデータから[&#x200B; ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=ja)を手動で作成し、レポートでデータを使用する前に、これらの特性を使用して[&#x200B; セグメント &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/segments-purpose.html?lang=ja)を作成します。

DSPで特定のクリエイティブにアクセスしたユーザーのユーザーレベルのデータを入力する特性の例：

1. イベントを`d_event = imp`として識別します。
1. DSP キャンペーン内のクリエイティブ IDを特定し、それを`d_creative=[Creative ID]`として特性にマッピングします。

![特性の作成画面](/help/dsp/assets/aa-trait.png)

>[!MORELIKETHIS]
>
>* [DSP マクロ &#x200B;](/help/dsp/campaign-management/macros.md)
>* [Adobe Audience ManagerへのDSP メディア露出データの送信の概要](overview.md)
>* [&#x200B; ユースケース &#x200B;](use-cases.md)
