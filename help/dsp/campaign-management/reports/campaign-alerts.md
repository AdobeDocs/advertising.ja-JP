---
title: アラートの表示
description: キャンペーンおよびキャンペーンコンポーネントのアラートと推奨される解決策を表示する方法について説明します。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 39f77087769eda3cc200447aeb0a6d1648e23b42
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%

---

# アラートの表示

DSPは、キャンペーンやキャンペーンコンポーネントに問題が発生したタイミングを特定するのに役立ちます。 DSPでは、問題ごとに、タイムスタンプと問題解決のために推奨されるアクションを含むアラートが作成されます。 アラートの理由には、設定の問題（広告がプレースメントに添付されていない場合や契約の設定が正しくない場合など）、広告の拒否、キャンペーンの正常性の問題（広告の配信やパフォーマンスの低下など）が含まれます。 アラートは、キャンペーンレベル、パッケージレベル、プレースメント レベル、広告レベルおよび取引レベルで使用できます。

アラートは次の場所で利用できます。

* [!UICONTROL Pulse Panel]、[!UICONTROL Campaigns]、パッケージの詳細、[!UICONTROL Packages]、[!UICONTROL Placements] の各ビューの [!UICONTROL Ads] のアイコンは、そのビューの項目でアラートが使用できるかどうかを示します。 アイコンに青いドットが付いている場合（![ アラートが使用可能な場合は Pulse Panel アイコン ](/help/dsp/assets/alerts-panel.png " アラートが使用可能な場合は Pulse Panel アイコン ")）、アラートを使用できます。 ドットが表示されない場合（![アラートが利用できない場合の Pulse Panel アイコン](/help/dsp/assets/alerts-panel-empty.png "アラートが利用できない場合の Pulse Panel アイコン")）、アラートは使用できません。

* 同じビューのデータテーブルには、アイテム（またはそのコンポーネント）に問題があることを示す「[!UICONTROL Alerts]」列が含まれています。 アラート・インジケータには、「Critical」（![Critical](/help/dsp/assets/indicator-critical.png "Critical")）、「Warning」（![警告](/help/dsp/assets/indicator-warning.png "警告")）、「Information」（![Information](/help/dsp/assets/indicator-information.png "Information")）が含まれます。

任意のアラートに関連するキャンペーン管理ビューを開くことができるので、必要に応じて問題を解決するための設定を編集できます。

また、個々のアラートを無視するように選択して、アラートを [!UICONTROL Pulse] ントロールパネルから削除することもできます。

基になる問題が解決されると、アラートおよびアラート指標は自動的に消えます。

## [!UICONTROL Pulse Panel] でアラートを表示

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 次のいずれかの操作をおこないます。

   * （ビューに適用可能なすべてのアラートの場合）任意のキャンペーン管理ビューのツールバーの右側にある ![ アラートが使用可能な場合はパルスパネルアイコン ](/help/dsp/assets/alerts-panel.png " アラートが使用可能な場合はパルスパネルアイコン ") をクリックします。

   * （特定のキャンペーンのすべてのアラートの場合）キャンペーン行のアラートインジケーターをクリックして、「**[!UICONTROL View in Pulse panel]**」をクリックします。

   * （特定のパッケージ、プレースメントまたは広告に関するすべてのアラートの場合）次の操作を行います。

      1. キャンペーン名をクリックします。

      1. サブメニューで、**[!UICONTROL Packages]**、**[!UICONTROL Placements]** または **[!UICONTROL Ads]** をクリックして、関連するキャンペーンコンポーネントビューを開きます。

      1. パッケージ、プレースメント、または広告行のアラートインジケーターをクリックし、「**[!UICONTROL View in Pulse Panel]**」をクリックします。

   ターゲットの取引を含め、キャンペーンとそのコンポーネントに関連付けられているすべてのアラートが一覧表示されます。 デフォルトでは、重要なアラートが最初に表示されます。

1. （オプション）最初の検出日に従ってアラートをグループ化する場合、またはアラートのステータス、コンポーネントのステータス、コンポーネントのタイプ、特定のキャンペーン名を使用してアラートをフィルタ処理する場合は、パネルの右上にある「![ フィルタ」ボタン ](/help/dsp/assets/filter.png) をクリックし、フィルタ・オプションを選択して「**[!UICONTROL Apply]**」をクリックします。

1. 特定のアラートタイプに影響を受けるすべてのキャンペーンコンポーネントのリストを表示するには、「[!UICONTROL Package: No Active Placement (*N*） ]」などのアラート名をクリックします。 影響を受ける各コンポーネントの詳細（推奨されるアクションを含む）を表示するには、「[!UICONTROL EXPAND ALL]」をクリックするか、コンポーネント名をクリックします。 影響を受けるコンポーネントに関連するキャンペーン管理ビューを開き、推奨される変更を行うには、コンポーネント名にカーソルを置いて、「![ ビューに移動 ](/help/dsp/assets/go-to-view.png " ビューに移動 ")」をクリックします。

1. （オプション）アラートを無視（非表示）するには、コンポーネント名の上にカーソルを置いて ![ 無視 ](/help/dsp/assets/alert-ignore.png " 無視 ") をクリックし、「**[!UICONTROL Ignore alert till next check]**」、「**[!UICONTROL Ignore alert for 3 days]**」、または「**[!UICONTROL Ignore indefinitely]**」をクリックします。

アラートを無視してから数秒後に、アクションを取り消すことができます。 オプションメッセージが閉じると、アクションをキャンセルできなくなります。

1. （任意）無視されたアラートを取得するには、アラートをフィルタリングして「[!UICONTROL Alert Status]」または「[!UICONTROL All]」の [!UICONTROL Ignored] を表示します。 アラートの無視を解除するには、コンポーネント名の上にカーソルを置き、![Un-ignore](/help/dsp/assets/alert-un-ignore.png "Un-ignore") をクリックします。

## [!UICONTROL Pulse Panel] を閉じる

* ツールバーの右側にある「![Pulse Panel icon when alerts available](/help/dsp/assets/alerts-panel.png "Pulse Panel icon when alerts available") or ![アラートが利用できない場合の Pulse Panel アイコン](/help/dsp/assets/alerts-panel-empty.png "アラートが利用できない場合の Pulse Panel アイコン")」をクリックします。

>[!MORELIKETHIS]
>
>* [ キャンペーン管理ビューでのパフォーマンスレポートのタイプ ](campaign-reports-about.md)
