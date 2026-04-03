---
title: Advertising DSPでのプレースメント管理について
description: プレースメント管理の詳細。
feature: DSP Placements
exl-id: 903ba200-6bb3-4c31-b7a9-03ada3de5451
TQID: https://experienceleague.adobe.com/2NzvUNMqkGVsPaEDM3ifXGNOAIuR1qifdC1-pacbK7U
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 387
ht-degree: 0%

---

# Advertising DSPでのプレースメント管理について

プレースメントには、同じ広告タイプの1つ以上の広告のターゲティングパラメーターが含まれます。 単一のキャンペーンまたはパッケージのプレースメントを作成し、それに広告を割り当てることができます。 各キャンペーンまたはプレースメントには、指定された広告ローテーションを含む複数のプレースメントを含めることができます。 デフォルトでは、広告は均等に回転します。 様々なプレースメントターゲットタイプに対して入札乗数を個別に設定できます。

アクティブなプレースメントをアクティブなパッケージまたはキャンペーンに割り当てると、プレースメント内のすべてのアクティブで承認済みの広告は、プレースメントのターゲティングパラメーターに基づいて実行する資格があります。

プレースメントは、手動で作成することも、既存のプレースメントを複製することもできます。 また、手動または既存のプレースメントから再利用するプレースメントテンプレートを作成することもできます。 任意のプレースメントに追加の広告を添付できます。 また、個々のプレースメントを編集、一時停止、アーカイブしたり、一括編集ツールを使用して変更を加えたりすることもできます。

## 使用可能な配置タイプ

* プレロール
* モバイル
* 表示
* ネイティブ
* オーディオ
* コネクテッド TV
* ユニバーサルビデオ

## [!UICONTROL Placements] ダッシュボード

[!UICONTROL Placements] ダッシュボードは、すべてのプレースメントのパフォーマンスと経済レポートを一元化し、指定した日付範囲内でのプレースメントのパフォーマンスを素早く把握します。

![配置ダッシュボード &#x200B;](/help/dsp/assets/placement-dashboard.png)

ダッシュボードには、3つの指標を含む、カスタマイズ可能で大まかなトレンドチャートが用意されています。

ダッシュボードには、デフォルトでペーシングと配信の指標も配置ごとに表示されます。 オプションで、プレースメントのパフォーマンス指標を表示したり、カスタム列セットを作成したりできます。 XLSM （マクロ対応Excel スプレッドシート）形式のレポートとして、データテーブル全体をブラウザーのデフォルトのダウンロードフォルダーにダウンロードできます。

プレースメントごとに、パフォーマンス指標、ペーシングと配信指標、サイト、広告、インベントリ別のカスタム列セット、頻度の指標を含む詳細ビュー（[the [!UICONTROL Inspector]](/help/dsp/campaign-management/reports/campaign-reports-about.md)）を開くことができます。 サイトの除外、広告の一時停止、取引の編集など、含まれているサイト、広告、インベントリに対して素早くアクションを実行することもできます。 インスペクターを開くには、配置行の上にカーソルを置いて&#x200B;**[!UICONTROL More]**&#x200B;をクリックし、**[!UICONTROL Sites]**、**[!UICONTROL Ads]**、**[!UICONTROL Frequency]**&#x200B;または&#x200B;**[!UICONTROL Inventory]**&#x200B;をクリックします。 [!UICONTROL Sites]、[!UICONTROL Ads]、[!UICONTROL Frequency]または[!UICONTROL Inventory] タブのデータを、XLSM形式のレポートとしてブラウザーのデフォルトのダウンロードフォルダーに書き出すことができます。

>[!NOTE]
>
>[&#x200B; カスタムレポート &#x200B;](/help/dsp/reports/report-about.md)を使用して、プレースメントレポートのコンテンツと配信をさらにカスタマイズできます。

>[!MORELIKETHIS]
>
>* [&#x200B; プレースメントの作成](placement-create.md)
>* [&#x200B; プレースメントの入札乗数を管理](placement-manage-bid-multipliers.md)
>* [&#x200B; プレースメントの変更ログを表示](placement-change-log.md)
>* [配置の設定](placement-settings.md)
>* [&#x200B; パフォーマンスのトラブルシューティング &#x200B;](/help/dsp/optimization/troubleshooting-performance.md)
