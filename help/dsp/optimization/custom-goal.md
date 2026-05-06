---
title: カスタム目標のベストプラクティス
description: 最小CPAまたは最大ROASに最適化されたパッケージのカスタム目標を定義するためのベストプラクティスについて説明します。
feature: DSP Optimization
exl-id: e40b82bc-2558-4e78-b269-9b9a3f0f5219
TQID: https://experienceleague.adobe.com/xSM4vyVErtNbVqF3eMDeHpgEWaMK6hBwQpvijHEs0dc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# カスタム目標のベストプラクティス

カスタム目標は、広告主がビジネス目標を達成するために必要な成功イベントを定義します。 最適化目標「[!UICONTROL Highest Return on Ad Spend (ROAS)"]」または「[!UICONTROL Lowest Cost per Acquisition (CPA)]」を使用する各パッケージには、全体的な最適化目標の達成に役立つカスタム目標が含まれている必要があります。 カスタム目標は&#x200B;*[カスタム目標](/help/dsp/admin/custom-objectives-manage.md)*&#x200B;として作成できます。

<!--
 update image or omit it

![custom goals](/help/dsp/assets/objective-goals.png)
 -->

各カスタム目標（目的）は、追跡および最適化される1つ以上のコンバージョン指標と、これらの指標の相対的な重みとで構成されます。 [!DNL Adobe AI]を使用して、レポートとアルゴリズムの最適化のために[&#x200B; カスタム目標をパッケージ &#x200B;](/help/dsp/campaign-management/packages/package-settings.md)に割り当てることができます。

カスタム目標を作成および管理するには、「[&#x200B; カスタム目標を管理](/help/dsp/admin/custom-objectives-manage.md)」を参照してください。

## 単一の指標でカスタム目標を設定

次の例は、単一のコンバージョン指標をターゲットとする目標を設定する方法を示しています。

### 「[!UICONTROL Highest Return on Ad Spend (ROAS)]」最適化目標を持つキャンペーンの例

キャンペーンの目標が収益（[!UICONTROL Highest Return on Ad Spend (ROAS)]）で、すべてのデバイスタイプからの収益が同じくらい重要な場合は、「[!UICONTROL Revenue]」指標を1の重みに含めます（1）。 指標タイプ *[!UICONTROL Goal]*&#x200B;を選択します。

<!--
 update image or delete 

![example of a ROAS custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 重みが1 （1）の場合、任意のデバイスのディスプレイ広告で追跡される収益の$1ごとに1 （1）の値に相当します。 例えば、重みが1の250 ドルのコンバージョンは、コンバージョンの場合250 ドルと報告されます。 コンバージョン指標に0.5の重みが割り当てられている場合、$250のコンバージョンは$125としてAdobe Advertisingで報告されます（$250 Conversion * 0.5 [!UICONTROL weight] = $125）。

### 「[!UICONTROL Lowest Cost per Acquisition (CPA)]」最適化目標を持つキャンペーンの例

キャンペーン目標が顧客獲得単価（CPA）が最も低く、成功イベントが1つだけ必要な場合（「アプリケーション送信」など）、その1つの指標を含め、指標の種類を&#x200B;*[!UICONTROL Goal]*&#x200B;として指定します。 ベストプラクティスは、重みを1 （1）に設定することです。

<!--
 update image or delete 

![example of a CPA custom goal with a single conversion metric](/help/dsp/assets/custom-goal-roas.png)

-->

>[!NOTE]
>
> 1の重み付けは、任意のデバイスのディスプレイ広告で追跡されるコンバージョンごとに1の値に相当します。 例えば、10件のアプリケーション送信コンバージョンが追跡された場合、10件のアプリケーション送信コンバージョンが報告されます。 ただし、コンバージョン指標に重みが0.5の場合、Adobe Advertisingでは10のコンバージョンは5 （5）と報告されます（10のコンバージョン * 0.5 [!UICONTROL weight] = 5）。

## 複数の指標を持つカスタム目標

カスタム目標で複数の指標を使用するには、次の2つのシナリオがあります。

* キャンペーンの目標には、複数の成功イベントがあります。 たとえば、複数のオンサイトアクション（PDFのダウンロード、お問い合わせ、メール登録）の広告を行っている場合、これらはすべてCPA目標に貢献するアクションです。 目的に3つの別々の指標が含まれ、それぞれ1つの重みがある場合、[!DNL Adobe AI]を活用したアルゴリズムは、各指標とユーザーデバイスタイプを同じ重要度で扱います。 異なる指標に様々なコストや重要度がある場合は、それに応じて相対的な重みづけを調整します。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties.png)

-->

* カスタム目標のひとつのコンバージョン指標では、パフォーマンスを最適化するために必要な1日あたり最低10回のコンバージョンを達成できません。 1日のパッケージ費用が少ない、または自然なコンバージョン数が限られているため、コンバージョン数が少ない可能性があります。 カスタム目標にさらに支援指標を追加することで、1日あたり10 コンバージョンの閾値を達成することができます。 10個のサポートイベントを使用すると、それぞれの重みが1個より小さい場合でも、パッケージが10個/日のしきい値を満たすことができます（1）。 しかし、そんなに多くのイベントを追加する必要はありません。

  サポート指標をカスタム目標に追加する際には、主要な成功イベントに対する相対的な重要度に従って重み付けをおこない、データポイントの量を考慮します。 これにより、[!DNL Adobe AI]を活用したアルゴリズムで、複数の指標のバランスを取り、目標に向かって最適化することができます。

  次の目標の例には、それぞれ異なる重みを持つ3つの指標が含まれています。Application Submit = 1、Application Start = 0.1、Advertiser Landing Page = 0.01。 つまり、アプリケーション送信の各コンバージョンは、平均10件のアプリケーション開始コンバージョンと100件の広告主ランディングページのコンバージョンと同じ値をビジネスに持ちます。

<!--
 update image or delete it and adjust the wording above

   ![example of a custom goal with multiple metrics](/help/dsp/assets/custom-goal-multiple-properties2.png)

-->

ランディングページへの訪問をアプリケーション送信に均等に重み付けした場合、ランディングページへの訪問の量が自然に多くなるため、目標を上回り、ランディングページへの訪問に向けて最適化を歪める可能性があります。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタム目標の管理](/help/dsp/admin/custom-objectives-manage.md)
>* [最適化の目標とその使用方法](optimization-goals.md)
>* [&#x200B; パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [DSPによるキャンペーンの最適化](optimization-how-dsp-optimizes-campaigns.md)
