---
title: パッケージ設定
description: 使用可能なパッケージ設定の説明を参照してください。
feature: DSP Packages
exl-id: 20ec5e8e-4980-4fa0-80c9-531f5b02c0f9
TQID: https://experienceleague.adobe.com/--5v-30zFSwhdU1g0h9VXANZnIRNL-RgFYv-scnxRT0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1089
ht-degree: 0%

---

# パッケージ設定

## [!UICONTROL Basic Details]

**[!UICONTROL Name]:** パッケージ名。 最大長は60文字です。

**[!UICONTROL Description]:** （オプション） パッケージの説明。

**[!UICONTROL 3rd Party Billed Fees]:** （オプション）請求不可コストとして追跡される静的なサードパーティ料金：

* **[!UICONTROL CPM]:** インプレッション数1000あたりのコスト （CPM）。

* **[!UICONTROL Description]:** CPM料金の説明。

>[!NOTE]
>
>請求可能な手数料は、[!UICONTROL Net CPM]指標に反映されます。

パッケージレベルの設定は、[&#x200B; プレースメントレベル &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)で上書きできます。

## [!UICONTROL Goals & Budget]

**[!UICONTROL Pacing & Capping]:** （既存のパッケージの読み取り専用） パッケージ内のプレースメントをペースおよびキャップするレベル：

* **[!UICONTROL Package level pacing]:**&#x200B;このペーシング戦略は、含まれているすべてのプレースメントを&#x200B;*グループ*&#x200B;としてペーシングおよびキャップすることで動作します。 この戦略により、特定のパッケージ内のあらゆる配置が包括的に最適化され、パフォーマンスに基づいて支出が配分され、選択した主要業績評価指標（KPI）に拡大されます。

* **[!UICONTROL Placement level pacing]:**&#x200B;このペーシング戦略は、含まれているすべてのプレースメント *を個別に* ペーシングおよびキャッピングすることで動作します。 ベストプラクティスは、この戦略を、保証されたプライベート マーケットプレイス取引を実行するためにのみ使用することです。

**[!UICONTROL Flight Dates]:** パッケージ全体の開始日と終了日。 フライト日は、キャンペーンのフライト日に含める必要があります。

>[!NOTE]
>
>* このパッケージに割り当てられているすべてのプレースメントのフライト日は、これらの日付内に含める必要があります。
> * カスタムフライトがアクティブになっている場合、パッケージの開始日を編集することはできません。

**[!UICONTROL Activate Custom Flighting]:**&#x200B;以下の[!UICONTROL Flighting] セクションのパッケージに対して、均一でないペーシングのフライトを作成できます。 カスタムフライトを有効にしてパッケージを保存すると、カスタムフライトを無効にしたり、パッケージの開始日を編集したりすることはできません。

**[!UICONTROL Budget]:** （パッケージレベルのペーシングを含むパッケージのみ）総予算上限と予算間隔。

カスタムフライトを持つパッケージの場合、予算間隔は常に&#x200B;*[!UICONTROL All time]*&#x200B;です。 カスタムフライトのないパッケージの場合、予算間隔を指定します：*[!UICONTROL All time]、*、*[!UICONTROL Daily]、*、*[!UICONTROL Monthly]、*、または&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Gross Budget]:** （パッケージレベルのペーシングと動的マージン管理のみを含むパッケージ） パッケージの期間の総予算キャップ。

**[!UICONTROL Optimization Goal]:** （パッケージレベルのペーシングを含むパッケージのみ） パッケージの最適化目標。 各最適化目標の説明については、[最適化目標とその使用方法](/help/dsp/optimization/optimization-goals.md)を参照してください。

**[!UICONTROL Link PG Placements for Incremental Reach Optimization]:** （パッケージレベルのペーシングを持ち、「[!UICONTROL Always Max Bid & Maximize Reach]」および「[!UICONTROL Lowest Cost per Reach]」の最適化目標のみを持つパッケージ）は、キャンペーン内のすべてのプログラムで保証されたプレースメントからの世帯リーチデータを使用して、リーチを増やすように最適化します。

**[!UICONTROL Custom Goal for Model Learning]:** （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標のみを含むパッケージ）収益またはコンバージョンイベントを含む[&#x200B; カスタム目標](/help/dsp/optimization/custom-goal.md)は、CPAまたはROAS指標の計算に使用されます。 カスタム目標には、パッケージの最適化にCPAまたはROAS指標に加えて、使用する重み付けされた上funnelイベント（ページ訪問やショッピングカートの追加など）を含める必要があります。 カスタム目標とそれを使用するキャンペーンの作成に関するベストプラクティスなど、カスタム目標の詳細については、「[&#x200B; カスタム目標](/help/dsp/optimization/custom-goal.md)」および「[&#x200B; パフォーマンスキャンペーンの設定に関するベストプラクティス &#x200B;](/help/dsp/optimization/campaign-best-practices-performance.md)」を参照してください。「<!-- At some point, all of the objectives will be prefixed with "ADSP_," but probably that won't show up in the Custom Goal list in the DSP UI. -->」

**[!UICONTROL Consider Only Click Conversions for Model Learning]:** （オプション、「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標を持つパッケージのみ）最適化モデルに、クリックベースのコンバージョンからのみ学習するように指示します。 それ以外の場合、最適化モデルはクリックベースとインプレッションベースの両方のコンバージョンから学習します。

**[!UICONTROL Conversion Metric]:** （「[!UICONTROL Highest Return on Ad Spend]」および「[!UICONTROL Lowest Cost per Acquisition]」の最適化目標のみを含むパッケージ）最終的なコンバージョンイベント（サインアップなど）または収益イベント/販売金額（購入および購入金額など）は、広告費用対効果または獲得単価の計算に使用します。 選択したカスタム目標にマッピングされたすべてのプライマリイベント（「目標指標」）のリストから選択します。 リストが空の場合は、カスタム目標を編集して、少なくとも1つの基になるイベントを目標指標として含めます。

**[!UICONTROL Package Goal Type]:** （カスタム最適化目標を持つパッケージのみ） パッケージの目的。 この設定は、パッケージを最適化する方法を決定するのに役立ちます。

* *[!UICONTROL Prospecting]:*&#x200B;見込み客パッケージは、新規顧客の獲得に重点を置いています。

* *[!UICONTROL Retargeting]:* リターゲティングパッケージでは、以前の訪問者または顧客の再ターゲティングに焦点を当てています。

* *[!UICONTROL Other]:*&#x200B;他のすべての目的。

**[!UICONTROL Linked Package for Optimization Learnings Carryover]:** （カスタム最適化目標を持つパッケージのみ）履歴データがパッケージを最適化するための入力として使用される別のパッケージ。

**[!UICONTROL Target]:** （パッケージレベルのペーシングを含むパッケージのみ）パフォーマンスの追跡に使用されるターゲット目標。

>[!NOTE]
>
>このフィールドはベンチマークに過ぎず、意思決定には使用されません。

**[!UICONTROL Frequency Cap]:** （パッケージレベルのペーシングを含むパッケージのみ）一意のデバイス、ユニバーサル ID、またはユーザー（キャンペーン用に指定された[!UICONTROL Cross Device Level]とプレースメントの[!UICONTROL Targeting]設定に応じて）がパッケージから広告を配信できる回数。 オプションには、1日、週、または月あたりの特定の金額&#x200B;*[!UICONTROL Unlimited]*&#x200B;が含まれます。

>[!NOTE]
>
>* 広告の表示頻度の上限は、キャンペーン、パッケージ、プレースメントレベルで設定できます。 DSPは、キャンペーン階層で最も厳格な頻度キャップを尊重しています。
>* 最善の方法は、見込み顧客の発掘と再ターゲティングの両方の頻度の上限をパッケージレベルで設定することです。
> * 広告の表示頻度を上げることで、オーディエンスの支出とインプレッションは増加しますが、リーチは低下します。 広告の表示頻度の上限が低いと、支出とインプレッションは少なくなりますが、リーチは高くなります。

**[!UICONTROL Pace on]:** （パッケージレベルのペーシングを含むパッケージのみ）次に基づくペーシング：

* *[!UICONTROL Budget]:* （デフォルト）このオプションは、割り当てられたパッケージ予算内で可能な限り多くのインプレッションを提供します。

* *[!UICONTROL Impressions]:*&#x200B;このオプションは、指定した間隔で指定した数量に達するまでインプレッションを配信します。 このオプションを選択する場合、インプレッション数と間隔を指定します：*すべての時間、* *[!UICONTROL Daily]、* *[!UICONTROL Monthly]、*、または&#x200B;*[!UICONTROL Weekly]*。

**[!UICONTROL Flight pacing]:** （パッケージレベルのペーシングを含むパッケージのみ）フライト全体で広告配信をペーシングする方法：

* *[!UICONTROL Even]:*&#x200B;各フライト全体に一様に配信を配置し、フライトの前半の配信の50%を目標とします。

* *[!UICONTROL Slightly Ahead]:* （既定値）配信を高速化して、フライト期間の途中で55 ～ 65%が完了するようにします。

* *[!UICONTROL Frontload]:*&#x200B;は、フライトの途中で65 ～ 75%が完了するように配信を高速化します。

* *[!UICONTROL Aggressive Frontload]:*&#x200B;は、フライトの途中で75 ～ 85%が完了するように配信を高速化します。

**[!UICONTROL Intraday pacing]:** （パッケージレベルのペーシングを含むパッケージのみ）フライト内の各日に広告の配信をペース設定する方法：

* *[!UICONTROL Even]:* （既定値）在庫の空き状況に基づいて配信を拡大します。 一般的に、オークション数が多い日中に1時間あたりの広告が増え、朝や夕方に配信される広告が少なくなります。

* *[!UICONTROL ASAP]:*&#x200B;配信を&#x200B;*均等*&#x200B;の2倍の速度に高速化します。

  >[!CAUTION]
  >
  >このオプションはパフォーマンスに悪影響を及ぼす可能性があります。 配信と支出の優先順位がパフォーマンスの最適化よりも高い場合にのみ使用してください。

## [!UICONTROL Flighting]

（パッケージレベルのペーシングを含むパッケージ） パッケージのフライト期間（パッケージ全体の[!UICONTROL Flight Dates]内のカスタム飛行期間を含む）。 カスタムフライトを設定できるのは、[!UICONTROL Activate Custom Flighting] セクションで[!UICONTROL Goals & Budget] オプションが有効になっている場合のみです。

**[!UICONTROL Automatically rollover remaining flight budget to next flight]:** （[!UICONTROL Activate Custom Flighting] オプションが有効になっている場合にのみ使用可能）は、前のフライトの残りの予算を、次のフライトの既存の予算に自動的に追加します。

[!UICONTROL Packages] ビューと[!DNL Package Name] > [!UICONTROL Flights] ビューでは、現在のフライト目標を示す[!UICONTROL Interval Goal] フィールドに、ロールオーバーの予算が含まれています。

**[!DNL Flight N]:** （[!UICONTROL Activate Custom Flighting] オプションが有効になっている場合にのみ使用可能）各フライトについて、開始日、終了日、および目標支出目標を指定します。 別のフライトを追加するには、**[!UICONTROL Add Flight]**&#x200B;をクリックします。

「[!UICONTROL Automatically rollover remaining flight budget to next flight]」オプションが有効になっていない既存のパッケージの場合、オプションで設定を再度開いて、任意のフライトの&#x200B;**[!UICONTROL Rollover]**&#x200B;列に値を入力し、潜在的な未使用の予算を次のフライトに追加できます。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのパッケージ管理について](package-about.md)
>* [&#x200B; パッケージを作成](package-create.md)
>* [&#x200B; パッケージの編集](package-edit.md)
>* [&#x200B; プレースメントをパッケージに添付](package-attach-placement.md)
>* [&#x200B; パッケージの変更ログを表示](package-change-log.md)
>* キャンペーン管理に関する[FAQ](/help/dsp/campaign-management/faq-campaign-management.md)
