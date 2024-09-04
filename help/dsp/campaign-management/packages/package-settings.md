---
title: パッケージ設定
description: 使用可能なパッケージ設定の説明を参照してください。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
source-git-commit: c1967636a762379f1daafb52cfe57dd0122b0748
workflow-type: tm+mt
source-wordcount: '1088'
ht-degree: 0%

---

# パッケージ設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** パッケージ名。 最大長は 60 文字です。

**[!UICONTROL Description]:** （オプション）パッケージの説明。

**[!UICONTROL 3rd Party Billed Fees]:** （任意）請求不可コストとして追跡される静的なサードパーティ料金。

* **[!UICONTROL CPM]:** 1000 インプレッション数（CPM）あたりのコスト。

* **[!UICONTROL Description]:** CPM 料金の説明。

>[!NOTE]
>
>請求可能な料金は、[!UICONTROL Net CPM] の指標に反映されます。

[ プレースメントレベル ](/help/dsp/campaign-management/placements/placement-settings.md) でパッケージレベルの設定を上書きできます。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （既存のパッケージの場合は読み取り専用） パッケージ内のプレースメントを調整およびキャップするレベル：

* **[!UICONTROL Package level pacing]:** このペーシング戦略は、含まれているすべてのプレースメントを *グループ* としてペーシングおよびキャッピングすることで機能します。 この戦略は、特定のパッケージ内のすべてのプレースメントが総合的に最適化され、パフォーマンスとスケールに基づいて、選択した主要業績評価指標（KPI）に支出が配分されるようにします。

* **[!UICONTROL Placement level pacing]:** このペーシング戦略は、含まれているすべてのプレースメントを（個別に *ペーシングおよびキャッピングすることで機能* ます。 ベストプラクティスは、この戦略を、保証された非公開のマーケットプレイス取引の実行にのみ使用することです。

**[!UICONTROL Flight Dates]:** パッケージの全体的な開始日と終了日。 フライト日は、キャンペーンフライト日の範囲内に含める必要があります。

>[!NOTE]
>
>* このパッケージに割り当てられているすべてのプレースメントのフライト日付は、これらの日付内に含める必要があります。
> * カスタム光源が有効な場合、パッケージの開始日は編集できません。

**[!UICONTROL Activate Custom Flighting]:** 以下の [!UICONTROL Flighting] のセクションのパッケージに対して、均等でないペーシングフライトを作成できます。 カスタムライティングを有効にしてパッケージを保存すると、カスタムライティングを無効にしたり、パッケージの開始日を編集したりできなくなります。

**[!UICONTROL Budget]:** （パッケージレベルのペーシングを使用したパッケージのみ）総予算の上限と予算間隔。

カスタム照明を使用するパッケージの場合、予算間隔は常に *[!UICONTROL All time]* です。 カスタム照明を使用しないパッケージの場合は、予算間隔 *[!UICONTROL All time]、*、*[!UICONTROL Daily]、*、*[!UICONTROL Monthly]、*、*[!UICONTROL Weekly]* を指定します。

**[!UICONTROL Gross Budget]:** （パッケージレベルのペーシングと動的マージン管理のみを使用するパッケージ）パッケージの期間に対する総予算上限値。

**[!UICONTROL Optimization Goal]:** （パッケージレベルのペーシングを使用したパッケージのみ） パッケージの最適化目標。 [ 最適化目標とその使用方法 ](/help/dsp/optimization/optimization-goals.md) で、各最適化目標の説明を参照してください。


**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** （パッケージレベルのペーシングを使用し、「[!UICONTROL Always Max Bid & Maximize Reach]」および「[!UICONTROL Lowest Cost per Reach]」の最適化目標を設定したパッケージのみ）キャンペーンでプログラムで保証されたすべてのプレースメントの世帯リーチデータを使用して、増分リーチを最適化します。

**[!UICONTROL Custom Goal for Model Learning]:** （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ） [ カスタム目標 ](/help/dsp/optimization/custom-goal.md) CPA または ROAS 指標の計算に使用される収益またはコンバージョンイベントを含む）。 カスタム目標には、パッケージ最適化の CPA または ROAS 指標に加えて、追加の重み付けされた上位ファネルイベント（ページ訪問数や買い物かごへの追加など）をオプションで含めることができます。 カスタム目標とそれを使用するキャンペーンを作成する際のベストプラクティスなど、カスタム目標の詳細については、「[ カスタム目標 ](/help/dsp/optimization/custom-goal.md)」および「[ パフォーマンスキャンペーンの設定のベストプラクティス ](/help/dsp/optimization/campaign-best-practices-performance.md)」を参照してください <!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** （オプション。「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ）クリックベースのコンバージョンからのみ学習するように最適化モデルに指示します。 そうでない場合、最適化モデルは、クリックベースおよびインプレッションベースのコンバージョンの両方から学習します。

**[!UICONTROL Conversion Metric]:** （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ）広告費用対効果または獲得あたりのコストを計算するために使用する最終コンバージョンイベント （サインアップなど）または収益イベント/販売額（購入および購入値など）。 選択したカスタム目標にマッピングされたすべてのプライマリイベント（「目標指標」）のリストから選択します。 リストに何も表示されない場合は、カスタム目標を編集して、基になるイベントの少なくとも 1 つを目標指標として含めます。

**[!UICONTROL Package Goal Type]:** （カスタム最適化目標を持つパッケージのみ） パッケージの目的。 この設定は、パッケージの最適化方法を決定するのに役立ちます。

* *[!UICONTROL Prospecting]:* 見込み客パッケージは、新規顧客の獲得に重点を置いています。

* *[!UICONTROL Retargeting]:* リターゲティングパッケージは、以前の訪問者または顧客を再公開することに重点を置いています。

* *[!UICONTROL Other]:* その他すべての目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （カスタム最適化目標を持つパッケージのみ）パッケージを最適化するための入力として履歴データが使用される別のパッケージ。

**[!UICONTROL Target]:** （パッケージレベルのペーシングのみを使用するパッケージ）パフォーマンスを追跡するために使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Frequency Cap]:** （パッケージレベルのペーシングを使用したパッケージのみ）一意のデバイス、ユニバーサル ID またはユーザー（キャンペーンに指定された [!UICONTROL Cross Device Level] とプレースメントの [!UICONTROL Targeting] 設定による）がパッケージから広告を提供できる回数。 オプションには、1 日、1 週間または 1 か月あたりの *[!UICONTROL Unlimited]* 数または特定の金額が含まれます。

>[!NOTE]
>
>* フリークエンシーキャップは、キャンペーン、パッケージ、プレースメントの各レベルで設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。
>* ベストプラクティスは、予測とリターゲティングの両方に対して、パッケージレベルでフリークエンシーキャップを設定することです。
> * フリークエンシーキャップが高いほど、支出とインプレッションは高くなりますが、リーチは低くなります。 フリークエンシーキャップが低いと、支出とインプレッションは低くなりますが、リーチは高くなります。

**[!UICONTROL Pace on]:** （パッケージレベルのペーシングのみを使用するパッケージ）ペーシングのベースとなるもの：

* *[!UICONTROL Budget]:* （デフォルト）このオプションは、割り当てられたパッケージ予算内でできるだけ多くのインプレッションを配信します。

* *[!UICONTROL Impressions]:* このオプションは、指定された期間内に指定された数に達するまでインプレッションを配信します。 このオプションを選択した場合は、インプレッションの数と間隔を *すべての時間、*、*[!UICONTROL Daily]、*、*[!UICONTROL Monthly]、* または *[!UICONTROL Weekly]* から指定します。

**[!UICONTROL Flight pacing]:** （パッケージレベルのペーシングのみを使用するパッケージ）フライト全体を通して広告の配信を調整する方法：

* *[!UICONTROL Even]:* フライトの前半で配信の 50% をターゲットとして、各フライト全体を通して均等に配信をペースします。

* *[!UICONTROL Slightly Ahead]:* （デフォルト）配信が加速されるので、フライト期間の半ばで 55～65% 完了します。

* *[!UICONTROL Frontload]:* 配信を高速化して、投入途中で 65～75% 完了するようにします。

* *[!UICONTROL Aggressive Frontload]:* 配信を高速化して、投入途中で 75～85% 完了するようにします。

**[!UICONTROL Intraday pacing]:** （パッケージレベルのペーシングのみを使用したパッケージ）フライト内で毎日広告の配信をペース調整する方法：

* *[!UICONTROL Even]:* （デフォルト）在庫の可用性に基づいて配信のスケールを設定します。 通常、オークションの量が多い昼間は 1 時間あたりにより多くの広告が配信され、朝と夜にはより少ない広告が配信されます。

* *[!UICONTROL ASAP]:* 配信を 2 倍の速度 *偶数* に高速化します。

  >[!CAUTION]
  >
  >このオプションは、パフォーマンスに悪影響を与える可能性があります。 配信の優先順位を完全に設定し、パフォーマンスの最適化よりも費用がかかる場合にのみ使用します。

## [!UICONTROL Flighting]

（パッケージレベルのペーシングを使用したパッケージ） パッケージのフライト期間（パッケージの全体 [!UICONTROL Flight Dates] 内のカスタムフライト期間を含む）。 カスタム フライトを設定できるのは、[!UICONTROL Goals & Budget] のセクションで [!UICONTROL Activate Custom Flighting] オプションが有効になっている場合だけです。

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** （「[!UICONTROL Activate Custom Flighting]」オプションが有効な場合のみ使用可能）前のフライトの残りの予算を、次のフライトの既存の予算に自動的に追加します。

[!UICONTROL Packages] ビューと [!DNL Package Name] > [!UICONTROL Flights] ビューでは、現在のフライト目標を示す [!UICONTROL Interval Goal] フィールドにロールオーバー予算が含まれています。

**[!DNL Flight N]:** （「[!UICONTROL Activate Custom Flighting]」オプションが有効な場合にのみ使用可能）各フライトに対して、開始日、終了日および目標支出目標を指定します。 別のフライトを追加するには、[**[!UICONTROL Add Flight]**] をクリックします。

「[!UICONTROL Automatically rollover remaining flight budget to next flight]」オプションが有効になっていない既存のパッケージの場合、オプションで設定を再度開き、任意のフライトの **[!UICONTROL Rollover]** 列に値を入力して、潜在的な未使用予算を次のフライトに追加できます。

>[!MORELIKETHIS]
>
>* [ パッケージ管理について ](package-about.md)
>* [ パッケージの作成 ](package-create.md)
>* [ パッケージの編集 ](package-edit.md)
>* [ パッケージへのプレースメントの添付 ](package-attach-placement.md)
>* [ パッケージの変更ログを表示する ](package-change-log.md)
>* [Campaign Managementに関する FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
