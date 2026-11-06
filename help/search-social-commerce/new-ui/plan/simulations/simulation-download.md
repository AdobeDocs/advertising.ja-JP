---
title: シミュレーションのダウンロード
description: シミュレーションを個別または結合されたスプレッドシート ファイルとしてダウンロードする方法について説明します。
feature: Search Optimization, Search Portfolios, Search Simulations
hide: true
exl-id: 46c8c9de-b558-486e-9453-feb5d359aaec
autotag-review: '2026-04-14T00:04:41.270Z'
TQID: 'https://experienceleague.adobe.com/5FVQv17adrIz6OJU1K3ftG8NRO-0evlIzc1tGIFoHfY'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: 893a7eac-45bd-56c2-a120-18db6d297dcc
    internal-label: Search Portfolios
  - id: 1d0fea65-a874-543d-94c9-b4dbf9e0360a
    internal-label: Search Simulations
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Admin
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: cb2d71e240af5ea1278cb2c00046d80040c914ce
workflow-type: tm+mt
source-wordcount: '242'
ht-degree: 0%
---
# シミュレーションのダウンロード

<!-- No subfeature tag for simulations or portfolios -->

*Beta機能*

[!UICONTROL Simulations] ビューから、1回に最大10個の週単位またはカスタム シミュレーションをダウンロードできます。 1つのシミュレーションが[!DNL Microsoft Excel] ワークブック （XLSX ファイル）としてダウンロードされます。 複数のシミュレーションの場合は、1つの結合ワークブックまたは各シミュレーションごとに個別のワークブックを含むZIP ファイルをダウンロードできます。

シミュレーションをダウンロードするには、[!UICONTROL View Simulation]権限を持つ[!UICONTROL Simulations] ビューにアクセスする必要があります。

>[!NOTE]
>
>* [ シミュレーション結果を画面で表示することもできます](simulation-view.md)。
>* [追加の多くの指標とほとんどのシミュレーション設定の列を含めるように[!UICONTROL Simulations] ビュー](/help/search-social-commerce/common-tasks/data-views/custom-default-views-manage.md)をカスタマイズできます。 含めることができる列について詳しくは、「[ シミュレーションについて](simulation-about.md#simulations-actions)」の「使用可能なアクション」の節を参照してください。
>* [!UICONTROL Portfolios] ビュー](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create-simulation.md#download-simulations)から、最大100 ポートフォリオの週次シミュレーションを[ ダウンロードすることもできます。

1. メインメニューで、**[!UICONTROL Plan]>[!UICONTROL Simulations]**&#x200B;をクリックします。

1. ダウンロードする最大10個のシミュレーションの横にあるチェックボックスをオンにします。

   ステータスが[!UICONTROL Successful]のシミュレーションのみを選択します。 選択したシミュレーションのステータスが[!UICONTROL Failed]、[!UICONTROL Queued]または[!UICONTROL In Progress]の場合、ダウンロードは開始されません。 ダウンロードする前に、これらの選択を消去します。

1. データテーブルの上のツールバーで、**[!UICONTROL Download Simulation]**&#x200B;をクリックします。

1. （複数のシミュレーションを選択した場合） ダウンロードオプションを選択します。

   * **[!UICONTROL Download as Single File]**：選択したすべてのシミュレーションを含む1つのワークブックをダウンロードします。

   * **[!UICONTROL Download as Multiple Files]**：選択したシミュレーションごとに個別のワークブックを含むZIP ファイルをダウンロードします。

ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。 ZIP ファイルをダウンロードする場合は、ファイルを解凍してワークブックを表示します。

>[!MORELIKETHIS]
>
>* [ シミュレーションについて](simulation-about.md)
>* [ シミュレーションの実行または再実行](simulation-create.md)
>* [ シミュレーションの詳細を表示](simulation-view.md)
