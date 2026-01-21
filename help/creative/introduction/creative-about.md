---
title: Adobe Systems広告Creativeについて
description: について学ぶ [!DNL Creative]。
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 1394b988828f5400b858f1a40b1b6382431a62b0
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# Adobe Systems Advertising Creative 2.0 について

<!-- verify all and rewrite to include new stuff -->

Adobe Systems広告の一環として、Advertising Creativeは、リアルタイムでパーソナライズされた広告エクスペリエンスを自動化し、オプションでクリエイティブエレメントレベルで広告を最適化するためのセルフサービスプラットフォームです。<!-- Verify --> 広告エクスペリエンスは、Adobe Systems Advertising DSPを含むあらゆるDSPの広告として実装するできます。

## 再利用可能なクリエイティブの特例文字クリエイティブライブラリ

Creative ライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成し、それぞれに個人クリエイティブとクリエイティブグループ( *バンドル*&#x200B;と呼ばれ、エクスペリエンスに添付します)を含めることができます。

### [!DNL Adobe] アセット統合

[!DNL Creative] は以下の [!DNL Adobe] 製品と直接統合されており、アセットクリエイティブ ライブラリ読み込むことができます。

* **Adobe Experience Manager:** デザインチームで作成され、標準のイメージ広告用に承認される [!DNL Adobe] 画像アセットをアップロードします。

* **パフォーマンスマーケティング用 GenStudio Adobe Systems:** ディスプレイ広告エクスペリエンスのすべての広告バリエーションを HTML5 クリエイティブとしてインポートします。

## ルールベースのエクスペリエンスとターゲット設定されていないエクスペリエンスの両方

* **ターゲットを絞ったルールベースのエクスペリエンス:ルールベースのデシジョンツリーモデルを使用してストーリービルド** 、オーディエンスについて知っていることに基づいてリアルタイムでカスタマイズされた一連の広告を展開します。 たとえば、ストーリーは、顧客行動、地理、人口統計、リターゲティング、カスタマージャーニー内の位置などに基づいて変更できます。

* **ターゲット設定されていないエクスペリエンス:** オーディエンスを絞り込まずに、広告要素スケジュールおよび最適化します。

### [!DNL Adobe] データ統合

Adobe Audience ManagerとAdobe Analyticsのファーストパーティオーディエンスセグメント、および広告DSPで作成したカスタムオーディエンスセグメントと、 [!DNL Creative] を使用して作成したリターゲティングピクセルを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用します。 <!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### エクスペリエンスの広告としての実装

エクスペリエンスを作成したら、エクスペリエンスのJavaScriptまたはiframeタグを生成し、広告DSPキャンペーンまたはその他のDSPのサードパーティ広告としてタグ実装するできます。

### 広告要素の最適化

必要に応じて、[!DNL Creative]を利用した最適化された加重広告の循環を使用して、特定のオーディエンスターゲットを定義するかどうかに関係なく、パフォーマンスに基づいて[!DNL Adobe AI]エクスペリエンスの広告要素を最適化できます。

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## ピクセルの再ターゲット化

リターゲティングピクセルを作成して、広告エクスペリエンス内のクリエイティブのターゲットとして使用できます。 ターゲットでは、以前に特定のウェブページにアクセスした、指定された属性を持つユーザーにのみ広告が表示されます。

## インプレッション、クリック、コンバージョントラッキング

[!DNL Creative] エクスペリエンスから配信された広告のすべてのインプレッションとクリックを自動的にトラッキングします。 必要に応じて、サードパーティインプレッショントラッキング URL とクリックトラッキング URL を Creative ライブラリ内のクリエイティブに追加したり、カスタム トラッキング URL をエクスペリエンスに追加したりすることもできます。

[!DNL Creative] 広告エクスペリエンスから作成された配信広告のコンバージョンもトラッキングします。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## パフォーマンスレポート

クリエイティブ>エクスペリエンス内で詳細なエクスペリエンスレベルのパフォーマンスレポート表示できます。

また、レポート>特例文字レポートで特例文字Creativeレポートを作成して、エクスペリエンス全体でエクスペリエンスレベルのパフォーマンス監視することもできます。 [!DNL Creative]エクスペリエンスをDSPキャンペーン内の広告として使用する場合、それらの広告の掲載結果は、他のDSP広告のデータと同様に、追加のカスタム レポートで使用できます。<!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

オプションで、カスタムレポートを指定した [レポートの送信先](/help/dsp/reports/report-destinations/report-destination-about.md)に配信できます。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [クリエイティブライブラリについて](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Advertising Creative のエクスペリエンスについて](/help/creative/experiences/experience-about.md)
