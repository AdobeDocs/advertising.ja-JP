---
title: アラートを表示
description: キャンペーンとキャンペーンコンポーネントに関するアラートと推奨される解決策を表示する方法について説明します。 アラートを使用して、キャンペーンの問題をトラブルシューティングします。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
exl-id: 667bf1c3-3bad-4a1a-b907-0c9bfe5362a9
source-git-commit: 747606b120cdd36eb025b320f89abb5cc7704bf0
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 0%

---

# アラートを表示

DSPは、どのキャンペーンやキャンペーンコンポーネントにも問題があるかどうかを特定するのに役立ちます。 各問題について、DSPはタイムスタンプと、問題を解決するための推奨アクションを含むアラートを作成します。 アラートの理由には、設定の問題（広告がプレースメントにアタッチされていない場合や、取引が誤って設定されている場合など）、広告の拒否、キャンペーンの正常性の問題（広告配信の低下やパフォーマンスの低下など）が含まれます。 アラートは、キャンペーン、パッケージ、プレースメント、広告、取引の各レベルで利用できます。

アラートは、次の場所で使用できます。

* [!UICONTROL Pulse Panel]、[!UICONTROL Campaigns]、パッケージの詳細、[!UICONTROL Packages]、[!UICONTROL Placements]の各ビューの[!UICONTROL Ads] アイコンは、そのビューの項目にアラートが使用可能かどうかを示します。 アイコンに青い点（![&#x200B; アラートが使用可能な場合はPulse Panel アイコン &#x200B;](/help/dsp/assets/alerts-panel.png " アラートが使用可能な場合はPulse Panel アイコン ")）がある場合、アラートが使用可能になります。 ドットが表示されない場合（![アラートがない場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel-empty.png "アラートがない場合のパルスパネルアイコン")）、アラートは使用できません。

* 同じビュー内のデータテーブルには、アイテム（またはそのコンポーネント）に問題があるタイミングを示す「[!UICONTROL Alerts]」列が含まれています。 アラート指標には、「重要」（![重要](/help/dsp/assets/indicator-critical.png "重要")）、「警告」（![警告](/help/dsp/assets/indicator-warning.png "警告")）および「情報」（![情報](/help/dsp/assets/indicator-information.png "情報")）が含まれます。

任意のアラートに対して関連するキャンペーン管理ビューを開くことで、必要に応じて設定を編集して問題を解決できます。

また、個別のアラートを無視して、[!UICONTROL Pulse] パネルから削除することもできます。

アラートとアラートインジケーターは、根本的な問題が解決されると自動的に消えます。

## [!UICONTROL Pulse Panel]でアラートを表示

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （ビューに適用されるすべてのアラートについて）任意のキャンペーン管理ビューのツールバーの右側で、![&#x200B; アラートが使用可能な場合はPulse Panel アイコンをクリックします](/help/dsp/assets/alerts-panel.png " アラートが使用可能な場合はPulse Panel アイコン ")。

   * （特定のキャンペーンのすべてのアラートについて） キャンペーン行のアラートインジケーターをクリックし、**[!UICONTROL View in Pulse panel]**&#x200B;をクリックします。

   * （特定のパッケージ、プレースメント、または広告に関するすべてのアラートについて）次の操作を行います。

      1. キャンペーン名をクリックします。

      1. サブメニューで「**[!UICONTROL Packages]**」、「**[!UICONTROL Placements]**」または「**[!UICONTROL Ads]**」をクリックして、関連するキャンペーンコンポーネントビューを開きます。

      1. パッケージ、プレースメントまたは広告行のアラートインジケーターをクリックし、**[!UICONTROL View in Pulse Panel]**&#x200B;をクリックします。

   キャンペーンとそのコンポーネントに関連するすべてのアラート（ターゲットを絞った取引を含む）がリストされます。 デフォルトでは、クリティカルアラートが最初にリストされます。

1. （Advertising Creativeを使用する広告主。オプション）「**[!UICONTROL Creative]**」タブをクリックして、Advertising Creative エクスペリエンスを含むプレースメントのアラートを表示します。

1. （オプション）最初の検出日に従ってアラートをグループ化するか、アラートのステータス、コンポーネントのステータス、コンポーネントタイプ、または特定のキャンペーン名でアラートをフィルタリングするには、パネルの右上にある「![&#x200B; フィルターボタン &#x200B;](/help/dsp/assets/filter.png)」をクリックし、フィルターオプションを選択して、**[!UICONTROL Apply]**。

1. 特定のアラートタイプの影響を受けるすべてのキャンペーンコンポーネントのリストを表示するには、「[!UICONTROL Package: No Active Placement (*N*） &#x200B;]」などのアラート名をクリックします。 推奨アクションを含め、影響を受ける各コンポーネントの詳細を表示するには、[!UICONTROL EXPAND ALL]をクリックするか、コンポーネント名をクリックします。 影響を受けるコンポーネントの関連するキャンペーン管理ビューを開いて、推奨される変更を行えるようにするには、コンポーネント名にカーソルを置き、![&#x200B; ビューに移動](/help/dsp/assets/go-to-view.png " ビューに移動")をクリックします。

1. （オプション）アラートを無視（非表示）するには、コンポーネント名の上にカーソルを置いて![無視](/help/dsp/assets/alert-ignore.png "無視")をクリックし、**[!UICONTROL Ignore alert till next check]**、**[!UICONTROL Ignore alert for 3 days]**&#x200B;または&#x200B;**[!UICONTROL Ignore indefinitely]**&#x200B;をクリックします。

アクションを元に戻すアラートを無視してから数秒経過します。 オプションメッセージが閉じると、アクションをキャンセルすることはできません。

1. （オプション）無視されたアラートを取得するには、アラートをフィルタリングして、「[!UICONTROL Alert Status]」または「[!UICONTROL All]」の[!UICONTROL Ignored]を表示します。 アラートを無視するには、コンポーネント名の上にカーソルを置き、![無視しない](/help/dsp/assets/alert-un-ignore.png "無視しない")をクリックします。

## [!UICONTROL Pulse Panel]を閉じる

* ツールバーの右側で、![&#x200B; アラートが使用可能な場合はPulse Panel アイコン &#x200B;](/help/dsp/assets/alerts-panel.png " アラートが使用可能な場合はPulse Panel アイコン ")または![アラートがない場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel-empty.png "アラートがない場合のパルスパネルアイコン")をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーン管理ビューのパフォーマンスレポートの種類](campaign-reports-about.md)
