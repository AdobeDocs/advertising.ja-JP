---
title: Adobe Advertising Creativeについて
description: 詳細情報  [!DNL Creative].
feature: Creative Introduction
source-git-commit: 1ab83cfe82bde4a7b1a32cf3773cdce4738af497
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 0%

---

# Adobe Advertising Creative 2.0 について

*クローズドベータ版*

<!-- verify all and rewrite to include new stuff -->

Adobe Advertisingの一部であるAdvertising Creativeは、パーソナライズされたリアルタイムの広告エクスペリエンスを自動化し、オプションでクリエイティブ要素レベルで広告を最適化するためのセルフサービスプラットフォームです。

## 再利用可能なクリエイティブのカスタムクリエイティブライブラリ

Creative ライブラリを使用すると、広告エクスペリエンスで使用するクリエイティブを管理できます。 複数のライブラリを作成でき、それぞれに個別のクリエイティブとクリエイティブグループ（*バンドル* と呼ばれます）を含めることができます。 広告エクスペリエンスにクリエイティブバンドルを追加します。

## ルールベースのエクスペリエンス

[!DNL Creative] を使用すると、ルールベースのデシジョンツリーモデルを使用してストーリーを構築できます。オーディエンスに関する知識に基づいてリアルタイムにカスタマイズされ、異なる web サイトに移動した場合でも顧客に従う、振り付けられた広告の文字列を展開しま <!-- verify if that's true without Adobe CDP -->。 例えば、ストーリーは、顧客の行動、地域、人口統計、リターゲティング、カスタマージャーニーでの位置などに基づいて変更されます。

<!-- Add when available:

## [!DNL Adobe] content and data integrations

[!DNL Creative] has direct integrations with Adobe Experience Manager, allowing you to easily upload the [!DNL Adobe] assets that your design team creates and use them for real-time storyboarding and editing of ad experiences.

You also can use your first-party audience segments from Adobe Audience Manager and Adobe Analytics &mdash; as well as audience segments you create in Advertising Cloud DSP
or retargeting pixels you create using [!DNL Creative] &mdash; as targets for specific creatives in an ad experience.
-->

### 広告としてのエクスペリエンスの実装

エクスペリエンスを作成したら、エクスペリエンス用のJavaScriptまたは iframe タグを生成し、そのタグをAdvertising DSPまたは他のDSPのサードパーティ広告として実装できます。<!-- Add any more info about integration with DSP? -->

<!-- Maybe add a subsection "Audience targeting options" with info about types of creative-level Retargeting and placement-level targeting within your DSP.  Need to clarify if any placement-level targeting might contradict/override creative-level targeting, or if they're completely different.

Advertiser should be able to target all segments which are available in DSP for targeting
-->

### 広告要素の最適化

オプションで、Adobe Senseiを活用し [!DNL Creative]、最適化された重み付けされた広告ローテーションを使用して、特定のオーディエンス目標を定義しているかどうかに関係なく、パフォーマンスに基づいて任意のエクスペリエンスの広告要素を最適化することもできます。

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

レポート/カスタムレポートでカスタム Creative レポートを作成し、エクスペリエンスをまたいでエクスペリエンスレベルのパフォーマンスを監視することもできます。 DSP キャンペーン内の広告として [!DNL Creative] エクスペリエンスを使用する場合、他のDSP広告のデータと同様に、それらの広告のパフォーマンスデータは、追加のカスタムレポートで利用できます。<!-- Verify that [!DNL Creative] users have access to ALL other reports, and if I can completely duplicate the report help for both help sets. -->

オプションで、指定した [ レポートの宛先 ](/help/dsp/reports/report-destinations/report-destination-about.md) にカスタムレポートを配信できます。

<!--
>* [Overview of implementing Adobe Advertising Creative](/help/creative/introduction/implementation-overview.md)
>* [How the user interface is organized](/help/creative/introduction/ui.md)
-->

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md)
>* [Advertising Creativeでのエクスペリエンスについて ](/help/creative/experiences/experience-about.md)
