---
title: パッケージ設定
description: 使用可能なパッケージ設定の説明を参照してください。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: 81415330017ee207fa1aa43ffdf2fe3205d88e9a
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 0%

---

# パッケージ設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** パッケージ名。 最大長は 60 文字です。

**[!UICONTROL Description]:** （オプション）パッケージの説明。

**[!UICONTROL 3rd Party Billed Fees]:** （任意）請求不可コストとして追跡される静的なサードパーティ料金：

>[!NOTE]
>
>請求可能な料金は次に反映されます [!UICONTROL Net CPM] 指標。
>
* **[!UICONTROL CPM]:** 1000 インプレッション数（CPM）あたりのコスト。

* **[!UICONTROL CPM Description]:** CPM 料金の説明。

パッケージレベルの設定は、 [プレースメントレベル](/help/dsp/campaign-management/placements/placement-settings.md).

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （既存のパッケージの場合は読み取り専用） パッケージ内のプレースメントを調整およびキャップするレベル：

* **[!UICONTROL Package level pacing]:** このペーシング戦略は、含まれているすべてのプレースメントを a としてペーシングおよびキャッピングすることで機能します *グループ*. この戦略は、特定のパッケージ内のすべてのプレースメントが総合的に最適化され、パフォーマンスとスケールに基づいて、選択した主要業績評価指標（KPI）に支出が配分されるようにします。

* **[!UICONTROL Placement level pacing]:**  このペーシング戦略は、含まれているすべてのプレースメントをペーシングおよびキャッピングすることで機能します *個別に*. ベストプラクティスは、この戦略を、保証された非公開のマーケットプレイス取引の実行にのみ使用することです。

**[!UICONTROL Flight Dates]:** パッケージの全体的な開始日と終了日。 フライト日は、キャンペーンフライト日の範囲内に含める必要があります。

>[!NOTE]
>
>* このパッケージに割り当てられているすべてのプレースメントのフライト日付は、これらの日付内に含める必要があります。
> * カスタム光源が有効な場合、パッケージの開始日は編集できません。

**[!UICONTROL *Activate Custom Flighting]:** でパッケージの偶数でないペーシングフライトを作成できます。 [!UICONTROL Flighting] セクションを下にします。 カスタムライティングを有効にしてパッケージを保存すると、カスタムライティングを無効にしたり、パッケージの開始日を編集したりできなくなります。

**[!UICONTROL Budget]:** （パッケージレベルのペーシングを使用したパッケージのみ）総予算の上限と予算間隔。

カスタムライティングを使用するパッケージの場合、予算間隔は常に指定します *[!UICONTROL All time]*. カスタム照明を使用しないパッケージの場合は、予算間隔を指定します。 *[!UICONTROL All time],* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Gross Budget]:** （パッケージレベルのペーシングと動的マージン管理を使用したパッケージのみ） パッケージの期間の総予算の上限。

**[!UICONTROL Optimization Goal]:** （パッケージレベルのペーシングを使用したパッケージのみ） パッケージの最適化目標。 で各最適化目標の説明を参照してください [最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md).

**[!UICONTROL Custom Goal for Model Learning]:** （「」を含むパッケージ[!UICONTROL Highest Return on Ad Spend]「」と「」に対して検査する値[!UICONTROL Lowest Cost per Acquisition]「最適化目標のみ） A [カスタム目標](/help/dsp/optimization/custom-goal.md) これには、CPA または ROAS 指標の計算に使用される売上高またはコンバージョンイベントが含まれます。 カスタム目標には、パッケージ最適化の CPA または ROAS 指標に加えて、追加の重み付けされた上位ファネルイベント（ページ訪問数や買い物かごへの追加など）をオプションで含めることができます。 カスタム目標およびカスタム目標を使用するキャンペーンのベストプラクティスについて詳しくは、を参照してください。 [カスタム目標を作成するためのベストプラクティス](/help/dsp/optimization/custom-goal.md#custom-goal-best-practices) および [パフォーマンスキャンペーンの設定のベストプラクティス](/help/dsp/optimization/campaign-best-practices-performance.md).<!-- At some point, all of the objectives will be prefixed with "ADSP " -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** （オプション、「」を含むパッケージ[!UICONTROL Highest Return on Ad Spend]「」と「」に対して検査する値[!UICONTROL Lowest Cost per Acquisition]「最適化目標のみ）クリックベースのコンバージョンからのみ学習するように最適化モデルに指示します。 そうでない場合、最適化モデルは、クリックベースおよびインプレッションベースのコンバージョンの両方から学習します。

**[!UICONTROL Conversion Metric]:** （オプション、「」を含むパッケージ[!UICONTROL Highest Return on Ad Spend]「」と「」に対して検査する値[!UICONTROL Lowest Cost per Acquisition]「最適化目標のみ）広告費用対効果または獲得あたりのコストの計算に使用する、最終的なコンバージョンイベント（サインアップなど）または収益イベント/販売額（購入や購入値など）。 選択したカスタム目標にマッピングされたすべてのプライマリイベント（「目標指標」）のリストから選択します。 リストに何も表示されない場合は、カスタム目標を編集して、基になるイベントの少なくとも 1 つを目標指標として含めます。

**[!UICONTROL Package Goal Type]:** （カスタム最適化目標を持つパッケージのみ） パッケージの目的。 この設定は、パッケージの最適化方法を決定するのに役立ちます。

* *[!UICONTROL Prospecting]:* 見込み客パッケージは、新規顧客の獲得に重点を置いています。

* *[!UICONTROL Retargeting]:* リターゲティングパッケージは、以前の訪問者または顧客を再公開することに重点を置いています。

* *[!UICONTROL Other]:* 他のすべての目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （カスタム最適化目標を持つパッケージのみ）パッケージを最適化するための入力として履歴データが使用される別のパッケージ。

**[!UICONTROL Target]:** （パッケージレベルのペーシングを使用したパッケージのみ）パフォーマンスを追跡するために使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Frequency Cap]:** （パッケージレベルのペーシングのみを使用するパッケージ）一意のデバイス、ユニバーサル ID またはユーザーの回数（指定によって異なります） [!UICONTROL Cross Device Level] キャンペーンとプレースメントの [!UICONTROL Targeting] 設定）を使用して、パッケージから広告を提供できます。 次のようなオプションがあります *[!UICONTROL Unlimited]* または、1 日、1 週間または 1 か月あたりの特定の金額。

>[!NOTE]
>
>* フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。
>* ベストプラクティスは、予測とリターゲティングの両方に対して、パッケージレベルでフリークエンシーキャップを設定することです。
> * フリークエンシーキャップが高いほど、支出とインプレッションは高くなりますが、リーチは低くなります。 フリークエンシーキャップが低いと、支出とインプレッションは低くなりますが、リーチは高くなります。

**[!UICONTROL Pace on]:** （パッケージレベルのペーシングのみを使用するパッケージ）ペーシングのベースとなるもの：

* *[!UICONTROL Budget]:* （デフォルト）このオプションは、割り当てられたパッケージ予算内でできるだけ多くのインプレッションを配信します。

* *[!UICONTROL Impressions]:* このオプションは、指定された期間内に指定された数に達するまでインプレッションを配信します。 このオプションを選択した場合は、インプレッションの数と間隔を指定します。 *すべての時間、* *[!UICONTROL Daily],* *[!UICONTROL Monthly],* または *[!UICONTROL Weekly]*.

**[!UICONTROL Flight pacing]:** （パッケージレベルのペーシングのみを使用するパッケージ）フライト全体を通して広告の配信を調整する方法：

* *[!UICONTROL Even]:* フライトの前半で配信の 50% をターゲットに、各フライト全体で配信を均一にペースで進めます。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）配信が加速されるので、投入期間の半ばで 55～65% 完了します。

* *[!UICONTROL Frontload]:* 配信を高速化することで、投入期間の半ばで 65～75% 完了します。

* *[!UICONTROL Aggressive Frontload]:* 配信を高速化することで、投入期間の半ばで 75～85% 完了します。

**[!UICONTROL Intraday pacing]:** （パッケージレベルのペーシングのみを使用するパッケージ）フライト内で毎日広告を配信する方法：

* *[!UICONTROL Even]:* （デフォルト）在庫の可用性に基づいて配信をスケーリングします。 通常、オークションの量が多い昼間は 1 時間あたりにより多くの広告が配信され、朝と夜にはより少ない広告が配信されます。

* *[!UICONTROL ASAP]:* の 2 倍の速度で配信を高速化 *偶数*.

  >[!CAUTION]
  >
  >このオプションは、パフォーマンスに悪影響を与える可能性があります。 配信の優先順位を完全に設定し、パフォーマンスの最適化よりも費用がかかる場合にのみ使用します。

## [!UICONTROL Flighting]

（パッケージレベルのペーシングが適用されたパッケージ）パッケージのフライト期間（全体的なカスタムフライト期間を含む）。 [!UICONTROL Flight Dates] パッケージ用。 カスタム便を設定できるのは、 [!UICONTROL Activate Custom Flighting] オプションは、 [!UICONTROL Goals & Budget] セクション。

**[!DNL Flight N]:** （次の場合にのみ使用可能： [!UICONTROL Activate Custom Flighting] オプションを有効にする）フライトごとに、開始日、終了日、ターゲットの支出目標を指定します。 別のフライトを追加するには、をクリックします **[!UICONTROL Add Flight]**.

既存のパッケージの場合、オプションで、に値を入力できます [!UICONTROL Rollover] 潜在的な未支出予算を次のフライトに追加するためのすべてのフライトの列。 の見込み値 [!UICONTROL Adjusted Goal (Goal + Rollover)] それに応じて列が変更されます。<!-- clarify usage -->

>[!MORELIKETHIS]
>
>* [パッケージ管理について](package-about.md)
>* [パッケージを作成](package-create.md)
>* [パッケージを編集](package-edit.md)
>* [パッケージへのプレースメントの添付](package-attach-placement.md)
>* [パッケージの変更ログの表示](package-change-log.md)
>* [Campaign Managementに関する FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
