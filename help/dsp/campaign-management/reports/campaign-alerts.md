---
title: アラートの表示
description: キャンペーンおよびキャンペーンコンポーネントのアラートと推奨解決方法を表示する方法を説明します。
feature: DSP Campaigns, DSP Packages, DSP Placements, DSP Ads, DSP Campaign Data Views
source-git-commit: 70592355207ba43341eb208750dcd3fc00db51c1
workflow-type: tm+mt
source-wordcount: '631'
ht-degree: 0%

---

# アラートの表示

*ベータ版機能*

DSPを使用すると、キャンペーンまたはキャンペーンコンポーネントのいつ問題が発生しているかを特定できます。 各問題に対して、DSPはタイムスタンプと、問題を解決するために推奨されるアクションを持つアラートを作成します。 アラートの理由には、設定の問題（広告がプレースメントに添付されていない場合や、契約が正しく設定されていない場合など）、広告拒否、キャンペーンの正常性の問題（広告配信やパフォーマンスの低下など）があります。 アラートは、キャンペーン、パッケージ、プレースメント、広告、および契約レベルで使用できます。

アラートは、次の場所で使用できます。

* A [!UICONTROL Pulse Panel] アイコン [!UICONTROL Campaigns], [!UICONTROL Packages] およびパッケージの詳細 [!UICONTROL Placements]、および [!UICONTROL Ads] ビューは、そのビュー内のアイテムに対してアラートが使用可能かどうかを示します。 アイコンに青い点 (![アラートが使用可能な場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel.png "アラートが使用可能な場合のパルスパネルアイコン"))、アラートを使用できます。 ドットが表示されない場合 (![アラートがない場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel-empty.png "アラートがない場合のパルスパネルアイコン")) の場合、使用できるアラートはありません。

* 同じビューのデータテーブルには、「[!UICONTROL Alerts]」列は、項目（またはそのコンポーネント）がいつ問題を持つかを示します。 アラート指標には、「重大」(![重大](/help/dsp/assets/indicator-critical.png "重大")), &quot;Warning&quot; (![警告](/help/dsp/assets/indicator-warning.png "警告"))、および&quot;情報&quot; (![情報](/help/dsp/assets/indicator-information.png "情報")) をクリックします。

任意のアラートに対してキャンペーンの管理ビューを開き、必要に応じて設定を編集して問題を解決できます。

個々のアラートを無視して、個々のアラートを [!UICONTROL Pulse] パネル。

アラートとアラート指標は、基になる問題が解決されると自動的に非表示になります。

## でアラートを表示する [!UICONTROL Pulse Panel]

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. 次のいずれかの操作を行います。

   * （該当するすべてのアラートの場合）任意のキャンペーン管理ビューのツールバーの右側にある、 ![アラートが使用可能な場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel.png "アラートが使用可能な場合のパルスパネルアイコン").

   * （特定のキャンペーンのすべてのアラートについて）キャンペーン行のアラートインジケーターをクリックし、 **[!UICONTROL View in Pulse panel]**.

   * （特定のパッケージ、配置または広告に関するすべてのアラートに対して）次の操作を実行します。

      1. キャンペーン名をクリックします。

      1. サブメニューで、 **[!UICONTROL Packages]**, **[!UICONTROL Placements]**&#x200B;または **[!UICONTROL Ads]** をクリックして、関連するキャンペーンコンポーネントビューを開きます。

      1. パッケージ、プレースメント、または広告行のアラートインジケーターをクリックし、 **[!UICONTROL View in Pulse Panel]**.

   ターゲットを絞った契約を含む、キャンペーンとそのコンポーネントに関連するすべてのアラートが表示されます。 デフォルトでは、重要なアラートが最初に表示されます。

1. （オプション）最初の検出日に従ってアラートをグループ化したり、アラートステータス、コンポーネントステータス、コンポーネントタイプ別、または特定のキャンペーン名でアラートをフィルタリングするには、 ![フィルターボタン](/help/dsp/assets/filter.png) パネルの右上で、フィルターオプションを選択し、 **[!UICONTROL Apply]**.

1. 特定のアラートタイプの影響を受けるすべてのキャンペーンコンポーネントのリストを表示するには、アラート名 ( 例：[!UICONTROL Package: No Active Placement (*N*)]&quot;. 推奨されるアクションを含め、影響を受ける各コンポーネントの詳細を表示するには、 [!UICONTROL EXPAND ALL] またはコンポーネント名をクリックします。 影響を受けるコンポーネントの関連するキャンペーン管理ビューを開き、推奨される変更を行うには、コンポーネント名の上にカーソルを置いたまま、 ![表示に移動](/help/dsp/assets/go-to-view.png "表示に移動").

1. （オプション）アラートを無視（非表示）するには、コンポーネント名の上にカーソルを置いたまま、 ![無視](/help/dsp/assets/alert-ignore.png "無視")をクリックし、 **[!UICONTROL Ignore indefinitely]**.  <!-- **[!UICONTROL Ignore alert for three days]**, **[!UICONTROL Ignore alert until next check]**, or **[!UICONTROL Ignore indefinitely] -->

アラートを無視して操作を元に戻すには、数秒後に実行します。 オプションメッセージが閉じた後は、アクションをキャンセルできません。

1. （オプション）無視されたアラートを取得するには、アラートをフィルターして、 [!UICONTROL Alert Status] 」[!UICONTROL All]&quot;または&quot;[!UICONTROL Ignored].&quot; アラートの無視を解除するには、コンポーネント名の上にカーソルを置いたまま、 ![無視しない](/help/dsp/assets/alert-un-ignore.png "無視しない").

## を閉じる [!UICONTROL Pulse Panel]

* ツールバーの右側で、 ![アラートが使用可能な場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel.png "アラートが使用可能な場合のパルスパネルアイコン") または ![アラートがない場合のパルスパネルアイコン](/help/dsp/assets/alerts-panel-empty.png "アラートがない場合のパルスパネルアイコン").

>[!MORELIKETHIS]
>
>* [Campaign Managementビューでのパフォーマンスレポートのタイプ](campaign-reports-about.md)
