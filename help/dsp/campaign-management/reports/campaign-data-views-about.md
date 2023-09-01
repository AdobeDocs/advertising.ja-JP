---
title: Campaign のデータビューについて
description: キャンペーン、パッケージ、プレースメントおよび広告のデータビューをカスタマイズする方法について説明します。
feature: DSP Campaign Data Views
exl-id: 125f8f49-2fa3-4838-82dc-4760d2ea9c7e
source-git-commit: 16081f3ec55eb6d2d42927e440fba17cd0f4265c
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 0%

---

# Campaign のデータビューについて

すべてのキャンペーン管理ビュー ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]を参照 )、データテーブル内に表示されるデータをカスタマイズできます。 データは、次の方法でカスタマイズできます。

* 表示セレクターからビューを選択するか、既存のビューの列を編集して変更を一時的に適用するか、カスタムの列ビューを作成して、データ列とその順序を指定します。

  各キャンペーン管理レベル ([!UICONTROL Campaigns], [!UICONTROL Packages], [!UICONTROL Placements]、および [!UICONTROL Ads]) には、組み込み [!UICONTROL Pacing] および [!UICONTROL Performance] ビューに含まれているエンティティの関連指標が表示されます。 デフォルトでは、 [!UICONTROL Pacing] ビューが表示され、パフォーマンスの低いキャンペーンとキャンペーンのコンポーネントを一目で特定できます。 オプションで、 [列表示を変更する](column-view-change.md) パフォーマンスデータを表示するには ( [!UICONTROL Performance] 表示 ) または保存されている列セット。 オプションで、 [列を編集](column-view-edit.md) （内） [!UICONTROL Pacing] または [!UICONTROL Performance] 変更を一時的に適用する場合に表示します。

  また、 [カスタム列セット](column-view-create.md) 任意の順序で、必要な列を含む

  ![列表示セレクター](/help/dsp/assets/column-view-selector.png)

  列表示エディターでは、すべての指標がカテゴリ別にアルファベット順に表示されます。 [!UICONTROL Settings], [!UICONTROL Spend], [!UICONTROL Pacing], [!UICONTROL Reporting] (DSPが追跡する標準指標 ) [!UICONTROL Viewability]、および [!UICONTROL Conversions]. 指標に「([!UICONTROL Lifetime])」の戻り値を検索すると、ページで選択した日付範囲に関係なく、キャンペーンの開始時点からの戻り値が返されます。

  ![列表示エディター](/help/dsp/assets/column-view-editor.png)

  DSPでは、最新のビューがデフォルトのビューとして保存されるので、ページに戻るたびに、関連のある指標が常に表示されます。

* 適用 [フィルター](campaign-data-filter.md) をクリックして、現在のタブに表示されるデータを変更します。 使用可能なフィルターは、エンティティのタイプによって異なりますが、エンティティ名、ステータス、追加のプロパティ列などが含まれる場合があります。

* すべての標準ビューとカスタムビューで使用される日付範囲を変更します。

* [任意の列の値でデータを並べ替え](campaign-data-sort.md).

* ページの右下に 25 行、50 行、100 行を表示するかどうかを制御します。

>[!MORELIKETHIS]
>
>* [プラットフォーム内レポートについて](campaign-reports-about.md)
>* [列表示の変更](column-view-change.md)
>* [カスタム列表示の作成](column-view-create.md)
>* [カスタム列表示の編集](column-view-edit.md)
>* [データビジュアライゼーションの管理](campaign-data-visualization-manage.md)
>* [プレースメントのサイト、広告、頻度の詳細を表示](placement-details-view.md)
>* [配置予測レポートの表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [配置診断レポートの表示](placement-diagnostics.md)
>* [Campaign Managementビューからのデータの書き出し](campaign-export-data.md)
>* [ビデオ：DSPアカウントの構造とユーザーインターフェイス](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/ui.html)
