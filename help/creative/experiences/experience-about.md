---
title: Advertising Creativeのエクスペリエンスについて
description: パーソナライズされた広告エクスペリエンスを設定し、パフォーマンスに基づいて広告要素を最適化する方法を説明します。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: e966058f5fe3fe9eb039f74bda8ea950f717e123
workflow-type: tm+mt
source-wordcount: '796'
ht-degree: 0%

---

# Advertising Creative 2.0 のエクスペリエンスについて

*クローズドベータ版*

<!-- Revisit Description metadata  -->

<!-- MORE -->

[!DNL Advertising Creative 2.0] は、クリエイティブライブラリの広告に対して、<!-- can use a single library only --> の 2 つの異なる広告エクスペリエンス構造を提供します。

* **意思決定ツリーターゲティングを使用したエクスペリエンス：** [!DNL Creative] では、意思決定ツリーモデルを使用して、カスタマージャーニー全体を通してパーソナライズされた広告エクスペリエンスを設定できます。 ターゲットオーディエンスに基づいて、すべての広告要素（画像、ヘッドライン、オファー、ランディングページ）をカスタマイズできます。

  例えば、シカゴとニューヨーク市のユーザーを対象に同じクリエイティブのバンドルを指定し、シカゴのユーザーをAdobe Analyticsとは異なるランディングページに送信できます。 また、シカゴとニューヨーク市以外に住んでいるセグメント内のユーザーには別のバンドルを指定し、セグメントに属していない他のユーザーには 3 番目のバンドルを指定することもできます。

  ターゲティングオプションは次のとおりです。

   * Adobe Audience Manager、Adobe Analyticsおよび Advertising Cloud DSP からのファーストパーティオーディエンスセグメント

   * 特定の地理的な場所（国、州、米国内の DMA、都市、郵便番号を含む）

   * 特定のキーと値のペア（データパスターゲット）がDSP、パブリッシャー、パートナーから渡されるビューア

   * [!DNL Creative] リターゲティングピクセルと指定された属性値

   * 特定のデバイスタイプ、オペレーティングシステムおよびブラウザー

  各エクスペリエンスにクリエイティブバンドルを割り当てることができます。 各エクスペリエンスで、クリエイティブバンドルの最適化とスケジュールをカスタマイズし、各バンドル内の個々のクリエイティブのデフォルトのランディングページとトラッキング URL<!-- and any flexible attributes --> を変更できます。

* **デシジョンツリーのターゲット設定を使用しないエクスペリエンス：** [!DNL Creative] は、オーディエンスを絞り込まずに、広告エクスペリエンスの広告要素を最適化します。<!-- For first-party creatives, [!DNL Creative] serves the ads. --> 各エクスペリエンスの開始日と終了日および一部のデフォルト設定を指定しますが、ワークフローの多くは、エクスペリエンス内に直接存在しません。 エクスペリエンスにクリエイティブを直接追加する代わりに、[!UICONTROL Tag Manager] を使用してエクスペリエンスの各広告サイズに広告タグを作成したあと、それにクリエイティブを追加し、クリエイティブの最適化とスケジュールを設定し、ランディングページとトラッキング URL をカスタマイズします。

## 広告の最適化

<!-- MORE -->
[!DNL Creative] では、パフォーマンスに基づいて任意のエクスペリエンス用に広告要素を最適化します。 特定のオーディエンスをターゲットにしたエクスペリエンスの場合、ターゲットオーディエンスセットの個々の広告要素のパフォーマンスに基づいて広告を最適化できます。 特定のオーディエンスターゲットのないエクスペリエンスの場合、広告要素は、個々の広告要素のパフォーマンスにのみ基づいて最適化されます。

## エクスペリエンスの実装と管理

ライブエクスペリエンス（必要なすべての広告要素を含む）を作成したら、[ エクスペリエンス全体のJavaScriptまたは iframe タグを生成 ](experience-tag-export.md) できます。 Experience tag を広告としてAdobe Advertising DSPのキャンペーンにアップロードしたり、サードパーティのDSPに広告として実装したりできます。 [!DNL Creative] は、ターゲティング、広告ローテーションのオプションおよび使用可能な広告インベントリに基づいて、エクスペリエンスの広告を提供します。

## エクスペリエンスのパフォーマンスデータ

[!UICONTROL Experiences] ビューで「[!UICONTROL Metrics]」オプションを有効にすると、各エクスペリエンスカードまたは行は、エクスペリエンスが受け取ったインプレッション数とクリック数を示します。

![ 指標オプション ](/help/creative/assets/metrics-option.png " 指標オプション ")

<!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

<!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

[!UICONTROL Creative]/[!UICONTROL Experiences] ビューから、任意のエクスペリエンスの詳細なパフォーマンスデータを表示できます。 エクスペリエンス全体のパフォーマンスを監視するには、[!UICONTROL Custom Creative Report] を作成します。

<!--
You can [view detailed performance data for any experience](experience-performance-details.md) from the Creative > Experiences view. To monitor performance across your experiences, [create custom reports](/help/dsp/reports/report-create.md).
-->

## エクスペリエンスのステータス {#experience-statuses}

<!-- verify that these are all still the same -->

エクスペリエンスのステータスは自動的に設定されます（手動で設定する *deleted* を除く）。

*ライブ：* エクスペリエンスには必要な要素がすべて含まれているので、エクスペリエンスタグを生成して、DSPの広告として実装できます。<!-- A live experience may be scheduled to start in the future -->

*ドラフト：* エクスペリエンスのすべてのブランチにクリエイティブが割り当てられていないので、エクスペリエンスは不完全で、エクスペリエンスタグを生成できません。

*処理中：* 以前ライブだったエクスペリエンスは編集されましたが、現在は不完全です。 そのためのエクスペリエンスタグは生成できません。 **注意：** エクスペリエンスにエクスペリエンスタグを既に実装している場合、以前にライブになっていたバージョンは引き続き提供できます。 後でエクスペリエンスを完了し、再度ライブにした場合は、既存のタグ実装を使用して新しいバージョンを提供できます。

*削除済み：* エクスペリエンスは [!DNL Creative] から削除され、[!UICONTROL Experiences] ビューには表示されなくなります。

>[!NOTE]
>
>[!DNL Creative] のエクスペリエンスステータスに影響を与えることなく、DSP内で広告のステータスを変更できます。

## [!UICONTROL Experiences] ビュー

[!UICONTROL Experiences] ビューには、ターゲット設定されたエクスペリエンスとターゲット設定されていないエクスペリエンスがすべて表示されます。 エクスペリエンスの名前、ステータス、開始日と終了日、割り当てられたクリエイティブまたはクリエイティブバンドルの数とディメンション、エクスペリエンスに動的広告が含まれているかどうかがわかります。 [!UICONTROL Experiences] ビューで「[!UICONTROL Metrics]」オプションを有効にすると、各エクスペリエンスカードまたは行は、エクスペリエンスが受け取ったインプレッション数とクリック数を示します。

エクスペリエンスの作成や管理（最適化や、エクスペリエンスへのクリエイティブおよびクリエイティブバンドルの割り当てなど）を行えます。 また、広告エクスペリエンスタグを作成および名前変更したり、タグをJavaScriptおよび iframe 形式で書き出して DSP に実装したりすることもできます。 Advertising DSPを使用する広告主は、オプションで、タグを広告としてAdvertising DSP キャンペーンに直接アップロードできます。

<!--
### Available actions

* [Download data within the view](experience-download-view.md)

        + [Assign and unassign creative bundles to a final node](/help/creative/experiences/experience-assign-creative-bundles.md)
* Experiences with decision tree targeting: [Create](/help/creative/experiences/experience-create-targeting.md) and [edit](/help/creative/experiences/experience-edit-targeting.md) experiences, [assign and unassign creative bundles](/help/creative/experiences/experience-assign-creative-bundles.md), [customize creative optimization and scheduling](/help/creative/experiences/experience-optimization-scheduling-targeting.md), and [customize the tracking URLs for creatives](/help/creative/experiences/experience-tracking-urls-targeting.md)

* Experiences without decision tree targeting: [Create](experience-create-no-targeting.md) and [edit](/help/creative/experiences/experience-edit-no-targeting.md)

* [Clone](experience-clone.md) an experience

* [Preview](experience-preview.md) an experience

* [Share a demo URL](experience-share-demo-url.md) for an experience

* [Export ad tags for an experience](experience-tag-export.md)

* [Delete](experience-delete.md) an experience

-->

<!-- You can add or remove labels for your experiences.-->

<!-- Add links to workflows once they're done -->

>[!MORELIKETHIS]
>
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ ターゲティングを使用しないエクスペリエンスの作成 ](experience-create-no-targeting.md)
