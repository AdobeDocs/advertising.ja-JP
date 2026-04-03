---
title: Adobe Advertising Creativeについて
description: ' [!DNL Creative]について説明します。'
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
TQID: https://experienceleague.adobe.com/UfaLj12BFBAxCDvtb6cUtVxlcuOSYgnZPTAn7494APk
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3did: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 493
ht-degree: 0%

---

# Adobe Advertising Creative 2.0について

<!-- verify all and rewrite to include new stuff -->

Adobe Advertisingに含まれるAdvertising Creativeは、リアルタイムのパーソナライズされた広告体験を自動化し、必要に応じてクリエイティブ要素レベルで広告を最適化するためのセルフサービスプラットフォームです。<!-- Verify --> Adobe Advertising DSPを含む任意のDSPで、広告エクスペリエンスを広告として実装できます。

## 再利用可能なクリエイティブのカスタムクリエイティブライブラリ

Creativeライブラリでは、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成できます。各ライブラリには、個々のクリエイターとクリエイティブグループ（*バンドル*&#x200B;と呼ばれ、エクスペリエンスに添付します）を含めます。

### [!DNL Adobe]個のアセット統合

[!DNL Creative]は次の[!DNL Adobe]製品と直接統合されているため、アセットをクリエイティブライブラリに読み込むことができます。

* **Adobe Experience Manager:** デザインチームが作成し、標準の画像アセットの承認を行う[!DNL Adobe]個の画像アセットをアップロードします。

* **Adobe GenStudio for Performance Marketing:** ディスプレイ広告エクスペリエンスからすべての広告バリエーションをHTML5のクリエイティブとして読み込みます。

## ルールベースの体験とターゲティングされていない体験を両方とも

* **ターゲットを絞ったルールベースのエクスペリエンス：** ルールベースの意思決定ツリーモデルを使用してストーリーを構築します。オーディエンスについて把握している内容に基づいて、リアルタイムでカスタマイズされる広告の振り付け文字列を展開します。 例えば、顧客の行動、位置情報、デモグラフィック、リターゲティング、カスタマージャーニー内のどこにいるかなどにもとづいて、ストーリーを変えることができます。

* **ターゲットを絞らないエクスペリエンス：** オーディエンスを絞り込むことなく、広告要素をスケジュールおよび最適化します。

### [!DNL Adobe]個のデータ統合

Adobe Audience ManagerとAdobe Analyticsの1st パーティオーディエンスセグメントと、Advertising DSPで作成したカスタムオーディエンスセグメント、および[!DNL Creative]を使用して作成したリターゲティングピクセルを広告エクスペリエンスの特定のクリエイターのターゲットとして使用します。<!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### 広告としての体験の導入

エクスペリエンスを作成したら、エクスペリエンス用にJavaScriptまたはiframe タグを生成し、そのタグをAdvertising DSP キャンペーンまたはその他のDSPにサードパーティ広告として実装できます。

### 広告要素の最適化

オプションで、[!DNL Creative]に対して、パフォーマンスに基づいて、特定のオーディエンスターゲットを定義するかどうかに関係なく、最適化された重み付けされた広告ローテーションを使用して、任意のエクスペリエンスの広告要素を最適化することを許可できます。これは、[!DNL Adobe AI]によって実現されます。

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## リターゲティングピクセル

リターゲティングピクセルを作成し、広告体験の中でクリエイターのターゲットとして使用することができます。 ターゲットは、以前に特定のweb ページにアクセスしたことがある、特定の属性を持つユーザーにのみ広告を表示します。

## インプレッション、クリック、コンバージョンの追跡

[!DNL Creative]は、エクスペリエンスから配信された広告のすべてのインプレッション数とクリック数を自動的に追跡します。 また、オプションで、Creative ライブラリのクリエイティブにサードパーティのインプレッション追跡URLとクリックトラッキング URLを追加したり、エクスペリエンスのカスタム追跡URLを追加したりすることもできます。

[!DNL Creative]は、広告エクスペリエンスから作成された、配信された広告からのコンバージョンも追跡します。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## パフォーマンスレポート

クリエイティブ/エクスペリエンス内で、エクスペリエンスレベルの詳細なパフォーマンスレポートを表示できます。

また、レポート/カスタムレポートでカスタム Creative レポートを作成して、エクスペリエンス全体のエクスペリエンスレベルのパフォーマンスをモニターすることもできます。 [!DNL Creative] エクスペリエンスをDSP キャンペーン内の広告として使用する場合、他のDSP広告のデータと同様に、これらの広告のパフォーマンスデータは、その他のカスタムレポートで使用できます。<!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

必要に応じて、指定した[ レポート宛先](/help/dsp/reports/report-destinations/report-destination-about.md)にカスタムレポートを配信できます。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリについて](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Advertising Creativeでの体験について](/help/creative/experiences/experience-about.md)
