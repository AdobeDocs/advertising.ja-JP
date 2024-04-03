---
title: パッケージ設定
description: 使用可能なパッケージ設定の説明を参照してください。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 0606614cc4fca842b800c089afa0303b67ecba5f
workflow-type: tm+mt
source-wordcount: '933'
ht-degree: 0%

---

# パッケージ設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** パッケージ名。 最大長は 60 文字です。

**[!UICONTROL Description]:** （オプション）パッケージの説明。

**[!UICONTROL 3rd Party Billed Fees]:** （オプション）請求不可のコストとして追跡される静的なサードパーティ料金：

>[!NOTE]
>
>請求可能な料金は、 [!UICONTROL Net CPM] 指標。
>
* **[!UICONTROL CPM]:** 1,000 インプレッションあたりのコスト (CPM)。

* **[!UICONTROL CPM Description]:** CPM 費用の説明。

パッケージレベルの設定は、 [配置レベル](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （既存のパッケージの読み取り専用）パッケージ内の配置の配置と制限のレベル：

* **[!UICONTROL Package level pacing]:** このペーシング戦略は、含まれるすべての配置を as a としてペーシングし、制限することで動作します *グループ*. この戦略では、特定のパッケージ内のすべての配置を全体的に最適化し、パフォーマンスに基づく支出を選択した主要業績評価指標 (KPI) に配分し、規模を拡大します。

* **[!UICONTROL Placement level pacing]:**  このペーシング戦略は、含まれるすべての配置をペーシングし、制限することで機能します *個別に*. ベストプラクティスは、この戦略を使用して、保証された民間市場取引を実行することです。

**[!UICONTROL Flight Dates]:** パッケージの開始日と終了日です。

オプションで、パッケージに対して偶数でないフライトを作成するには、 *[!UICONTROL *Activate Custom Flighting]**を設定し、 [!UICONTROL Flighting] 」の節を参照してください。 カスタムフライティングを有効にしてパッケージを保存すると、カスタムフライティングを無効にすることはできません。

>[!NOTE]
>
>* フライト日は、キャンペーンのフライト日に含める必要があります。 さらに、このパッケージに割り当てられるすべての配置のフライト日をこれらの日付に含める必要があります。
> * カスタム照明が有効になっている場合、パッケージの開始日を編集することはできません。

**[!UICONTROL Budget]:** （パッケージレベルのペーシングのみのパッケージ）総予算額と予算間隔。

カスタム照明を含むパッケージの場合、予算間隔は常に *[!UICONTROL All time]*. カスタムフライティングのないパッケージの場合は、予算間隔を指定します。 *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** （パッケージレベルのペーシングと動的利益管理のみを含むパッケージ）パッケージの期間中の総予算額の上限。

**[!UICONTROL Optimization Goal]:** （パッケージレベルのペーシングのみのパッケージ）パッケージの最適化目標です。 各最適化目標の説明は、 [最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** (「[!UICONTROL Highest Return on Ad Spend]&quot;および&quot;[!UICONTROL Lowest Cost per Acquisition]&quot;最適化目標のみ ) A [カスタム目標](/help/dsp/optimization/custom-goal-about.md) これには、CPA または ROAS 指標の計算に使用される売上高またはコンバージョンイベントが含まれます。 カスタム目標では、オプションで、パッケージ最適化の CPA 指標や ROAS 指標に加えて、使用する追加の重み付けされた上位ファネルイベント（ページ訪問数、買い物かごへの追加など）を含めることができます。 カスタムの目標とそれを使用するキャンペーンのベストプラクティスについて詳しくは、  [カスタム目標を構築するためのベストプラクティス](/help/dsp/optimization/custom-goal-best-practices.md) および [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md).

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** ( オプション。「[!UICONTROL Highest Return on Ad Spend]&quot;および&quot;[!UICONTROL Lowest Cost per Acquisition]「最適化目標のみ ) 最適化モデルに対し、クリックベースのコンバージョンからのみ学習するよう指示します。 そうでない場合、最適化モデルはクリックベースとインプレッションベースの両方のコンバージョンから学習します。

**[!UICONTROL Conversion Metric]:** ( オプション。「[!UICONTROL Highest Return on Ad Spend]&quot;および&quot;[!UICONTROL Lowest Cost per Acquisition]「最適化目標のみ ) 広告費用対効果または 1 回あたりのコストの計算に使用する最終的なコンバージョンイベント（サインアップなど）または売上高イベント/販売額（購入値や購入値など）。 選択したカスタム目標にマッピングされているすべてのイベントのリストから選択します。

**[!UICONTROL Package Goal Type]:** （カスタム最適化目標を持つパッケージのみ）パッケージの目的。 この設定は、パッケージの最適化方法を決定する際に役立ちます。

* *[!UICONTROL Prospecting]:* パッケージの予測は、新しい顧客の獲得に重点を置いています。

* *[!UICONTROL Retargeting]:* パッケージのリターゲティングは、以前の訪問者または顧客を再公開することに重点を置いています。

* *[!UICONTROL Other]:* その他のすべての目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （カスタム最適化目標を持つパッケージのみ）パッケージの最適化のための入力として履歴データが使用される別のパッケージ。

**[!UICONTROL Target]:** （パッケージレベルのペーシングのみのパッケージ）パフォーマンスの追跡に使用されるターゲット目標。

>[!NOTE]
>
>このフィールドは、単なるベンチマークであり、決定には使用されません。

**[!UICONTROL Frequency Cap]:** （パッケージレベルのペーシングのみのパッケージ）一意のデバイスまたは人物の回数 ( 指定した [!UICONTROL Cross Device Level] キャンペーンの場合 ) は、パッケージから広告を提供できます。 次のオプションがあります *[!UICONTROL Unlimited]* または 1 日、1 週間、1 ヶ月あたりの特定の金額。

>[!NOTE]
>
>* 頻度キャップは、キャンペーン、パッケージ、配置の各レベルで設定できます。 DSPは、キャンペーン階層における最も厳しい頻度キャップに従います。
>* ベストプラクティスは、プロスペクティングとリターゲティングの両方に対して、パッケージレベルで頻度キャップを設定することです。
> * 頻度キャップが高いと、支出とインプレッションは高くなりますが、リーチは低くなります。 頻度キャップが低いと、支出とインプレッションは少なくなりますが、リーチは高くなります。

**[!UICONTROL Pace on]:** （パッケージレベルのペーシングのみのパッケージ）ペーシングの基盤は次のとおりです。

* *[!UICONTROL Budget]:* （デフォルト）このオプションでは、割り当てられたパッケージ予算内で、できるだけ多くのインプレッションを配信します。

* *[!UICONTROL Impressions]:* このオプションでは、指定された数量が指定された間隔内に達するまで、インプレッションを配信します。 このオプションを選択する場合は、インプレッション数と間隔を指定します。 *常に* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** （パッケージレベルでペーシングのみのパッケージ）フライト全体で広告配信を遅らせる方法は次のとおりです。

* *[!UICONTROL Even]:* フライトの前半の配信のターゲットの 50%を含む、各フライトを通して配信を均等に配置します。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）配信を加速し、飛行時間の途中で 55～65%完了するようにします。

* *[!UICONTROL Frontload]:* 配信を加速し、飛行中に 65～75%完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を加速し、飛行中に 75～85%完了するようにします。

**[!UICONTROL Intraday pacing]:** （パッケージレベルのペーシングのみのパッケージ）フライト内の毎日の広告配信を遅らせる方法は、次のとおりです。

* *[!UICONTROL Even]:* （デフォルト）在庫の可用性に基づいて配信の規模を拡大/縮小します。 一般に、オークション量が多いときは昼間に 1 時間あたりより多くの広告が配信され、朝晩に配信される広告は少なくなります。

* *[!UICONTROL ASAP]:* 配信を 2 倍の速度に高速化 *偶数*.

  >[!CAUTION]
  >
  >このオプションは、パフォーマンスに悪影響を与える可能性があります。 配信を完全に優先し、パフォーマンスの最適化よりも費用を優先する場合にのみ使用してください。

## [!UICONTROL Flighting]

( パッケージレベルでのペーシングと「[!UICONTROL Activate Custom Flighting]&quot;有効 ) 全体の [!UICONTROL Flight Dates] 次に示す [!UICONTROL Goals & Budget] 」セクションに入力します。

フライトごとに、開始日、終了日、インプレッションのターゲット数を入力します。 別のフライトを追加するには、 **[!UICONTROL Add Flight]**.

>[!MORELIKETHIS]
>
>* [パッケージ管理について](package-about.md)
>* [パッケージの作成](package-create.md)
>* [パッケージの編集](package-edit.md)
>* [パッケージに配置を添付する](package-attach-placement.md)
>* [パッケージの変更ログの表示](package-change-log.md)
>* [Campaign Managementに関する FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
