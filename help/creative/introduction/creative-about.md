---
title: Adobe Advertising Creativeについて
description: 詳細情報  [!DNL Creative].
feature: Creative Introduction
exl-id: 2cc12119-5924-4fcd-a54b-30f7887ae6a7
source-git-commit: 9082d9f455a0d26ca027dc699df29737b9042457
workflow-type: tm+mt
source-wordcount: '472'
ht-degree: 0%

---

# Adobe Advertising Creative 2.0 について

<!-- verify all and rewrite to include new stuff -->

Adobe Advertisingの一部であるAdvertising Creativeは、パーソナライズされたリアルタイムの広告エクスペリエンスを自動化し、オプションでクリエイティブ要素レベルで広告を最適化するためのセルフサービスプラットフォームです。<!-- Verify --> 広告エクスペリエンスは、Adobe Advertising DSPを含む任意のDSPの広告として実装できます。

## 再利用可能なクリエイティブのカスタムクリエイティブライブラリ

Creative ライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成して、それぞれに個別のクリエイティブとクリエイティブグループ（エクスペリエンスに添付する *バンドル* と呼ばれます）を含めることができます。

### [!DNL Adobe] アセット統合

[!DNL Creative] はAdobe Experience Managerと直接統合されているので、デザインチームが作成して標準の画像広告に対して承認する [!DNL Adobe] しい画像アセットを簡単にアップロードできます。

## ルールベースのエクスペリエンスとターゲットに設定されていないエクスペリエンスの両方

* **ターゲットを絞ったルールベースのエクスペリエンス：** ルールベースのデシジョンツリーモデルを使用してストーリーを構築します。オーディエンスに関する知識に基づいてリアルタイムにカスタマイズされる、振り付けされた広告の文字列を展開します。 例えば、ストーリーは、顧客の行動、地域、人口統計、リターゲティング、カスタマージャーニーでの位置などに基づいて変更されます。

* **ターゲット以外のエクスペリエンス：** オーディエンスを絞り込まずに、広告要素をスケジュールおよび最適化します。

### [!DNL Adobe] データ統合

Adobe Audience ManagerとAdobe Analyticsのファーストパーティオーディエンスセグメントに加えて、Advertising DSPで作成したカスタムオーディエンスセグメントを使用し、[!DNL Creative] を使用して作成したピクセルをリターゲティングし、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用できます。<!-- Advertiser should be able to target all segments that are available in DSP for targeting -->

### 広告としてのエクスペリエンスの実装

エクスペリエンスを作成したら、エクスペリエンス用のJavaScriptまたは iframe タグを生成し、そのタグをサードパーティ広告としてAdvertising DSP キャンペーンまたはその他のDSPに実装できます。

### 広告要素の最適化

オプションで、Adobe Senseiを活用し [!DNL Creative]、最適化された重み付けされた広告ローテーションを使用して、特定のオーディエンス目標を定義しているかどうかに関係なく、パフォーマンスに基づいて任意のエクスペリエンスの広告要素を最適化することもできます。

<!--
[!DNL Creative] serves first-party ads and triggers third-party ads for the experience based on the specified targeting (when applicable), scheduling, ad rotation, and optimization goal options 
-->

## リターゲティングピクセル

リターゲティングピクセルを作成して、広告エクスペリエンス内のクリエイティブのターゲットとして使用できます。 ターゲットは、特定の web ページを以前に訪問した、指定した属性を持つユーザーにのみ広告を表示します。

## インプレッション、クリックおよびコンバージョントラッキング

[!DNL Creative] は、エクスペリエンスから提供される広告のすべてのインプレッション数およびクリック数を自動的に追跡します。 また、オプションで、Creative ライブラリのクリエイティブやエクスペリエンスのカスタムトラッキング URL にサードパーティのインプレッショントラッキング URL やクリックトラッキング URL を追加できます。

[!DNL Creative] た、広告エクスペリエンスから作成された提供済み広告からのコンバージョンも追跡します。<!-- Verify wording; anything important to add here? We do track them for all users, right? Or is it optional?  -->

<!--
 [Don't need to mention] When an ad is served, the DSP that buys the ad first tracks the impression, and then passes the impression information to [!DNL Creative]. [!DNL Creative] first tracks a click on an ad, and it then passes the click information
to the DSP.
-->

## パフォーマンスレポート

クリエイティブ / エクスペリエンスで、詳細なエクスペリエンスレベルのパフォーマンスレポートを表示できます。

レポート/カスタムレポートでカスタム Creative レポートを作成し、エクスペリエンスをまたいでエクスペリエンスレベルのパフォーマンスを監視することもできます。 DSP キャンペーン内の広告として [!DNL Creative] エクスペリエンスを使用する場合、他のDSP広告のデータと同様に、それらの広告のパフォーマンスデータは、追加のカスタムレポートで利用できます。<!-- Verify that [!DNL Creative] users have access to ALL other reports. -->

オプションで、指定した [&#x200B; レポートの宛先 &#x200B;](/help/dsp/reports/report-destinations/report-destination-about.md) にカスタムレポートを配信できます。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [&#x200B; クリエイティブライブラリについて &#x200B;](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Advertising Creativeでのエクスペリエンスについて &#x200B;](/help/creative/experiences/experience-about.md)
