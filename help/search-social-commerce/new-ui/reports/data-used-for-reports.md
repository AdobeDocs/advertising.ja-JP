---
title: （新しいUI）レポートに使用するデータ
description: データビューとカスタムレポートで利用できるさまざまな種類のデータについて説明します。
feature: Search Reports
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: ff99aaef-142d-4c93-a88c-011e979e3843id: c916feea-e212-4773-b673-4daed287b8a3id: adcb1be7-7ed0-464d-a8d4-c905c9d47742id: fa0141e5-dc99-4fbd-9c0e-40aff66de606id: b36a77b1-3c8f-4e1c-8b0b-6e0ba3fb2664id: e246c273-d720-4ece-b29b-7aaba7d50169
source-git-commit: 18f4c5afafd63a6ae9421bf80b4e5b5fd424ed86
workflow-type: tm+mt
source-wordcount: 604
ht-degree: 0%

---

# （新しいUI）レポートに使用するデータ

Search, Social, &amp; Commerceには、クリックとコンバージョンのデータにもとづく包括的なパフォーマンスレポートが用意されています。 ポートフォリオまたは広告アカウントの様々なコンポーネントの基本的なパフォーマンスデータを、[!UICONTROL Portfolios]および[!UICONTROL Campaigns] ビューから表示できます。また、様々な基本および高度なレポートを生成することもできます。

Adobe Advertising コンバージョン追跡サービスを使用する広告主は、参照web サイトの地理的な場所またはドメイン名のクリック数、各チャネルの広告とコンバージョンにつながる様々なイベントが全体的なコンバージョン率にどのように貢献しているか、マーケティングチャネル別の単一の[ コンバージョン指標](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)のコンバージョンの分布も特定できます。 利用できるレポートは、ユーザーアカウントの種類によって異なります。 Adobeアカウントチームは、すべてのレポートにアクセスできます。

ほとんどのレポートは、表示する情報のみを表示するようにカスタマイズできます。 ほとんどのレポートでは、次の標準指標を使用でき、広告レベルで計算されます。

* **標準パフォーマンス指標：**

   * **[!UICONTROL Impressions]:**&#x200B;広告が配置された合計回数。

   * **[!UICONTROL Clicks]:**&#x200B;広告内のリンクがクリックされた合計回数。

   * **[!UICONTROL Cost]:**&#x200B;広告の総費用。 PPC （クリック報酬型）広告のコストは、常に、クリック数にクリック単価を掛けたものです。

   * **[!UICONTROL Cost per Click]:**&#x200B;広告の1 クリックの平均コスト。広告のコストを、広告の総クリック数で割ったものです。 例えば、広告インプレッションに100米ドルを費やし、広告が10 クリックを生成した場合、クリックあたりのコストは100米ドル/10=10米ドルです。

   * **[!UICONTROL Average Position]:** （該当する場合）配置された広告の平均位置を、インプレッション数で重み付けします。

   * **[!UICONTROL Estimated Clicks]:** （Adobe Advertising コンバージョントラッキングサービスを使用する広告主向けの高度なレポートに含まれる）参照元web サイトの市区町村またはドメイン名の推定クリック数。 これには、広告主が広告アカウントを持っていない広告ネットワークのデータが含まれます。

* **コンバージョン指標：**&#x200B;広告主のコンバージョン指標、またはコンバージョン指標に向けて追跡されたトランザクションデータのそれぞれのコンバージョンの合計数。 これには、コンバージョンやサイトエンゲージメントの指標は含まれますが、Adobe Analyticsから同期される計算指標や高度な計算指標は含まれません。

  これには、広告主アカウント用に同期されている[[!DNL Google Ads]件のトラッキング済みコンバージョン ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)と[[!DNL Google Analytics]件のトラッキング済みコンバージョン ](/help/search-social-commerce/admin/data-sources/data-source-about.md)が含まれる場合もあります。

* **カスタム指標：**&#x200B;既存の指標（注文単価など）に基づいて数式を作成して導き出す独自の指標。

## データの可用性

レポートを生成する際に、コンバージョンにつながる一連のイベントでコンバージョンデータをアトリビューションする方法を選択できます。 例えば、コンバージョン全体を最後のイベントに関連付けるか、最後のイベントに他のイベントよりも重みを付けるかを選択できます。 デフォルトでは、コンバージョンは最後のイベントに関連付けられます。

レポートに指定するアトリビューションルールに応じて、各レポートタイプのデータは次の日付で使用できます。

| レポートグループ | レポート | データが使用可能な日付 |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | 2021年5月15日以降。<br><br><b>例外：</b> プロミネンス指標データは、2022年9月8日から利用できます。 |
| | その他すべての[!UICONTROL Basic Reports] | 過去36か月間の例外：<br><br><b>例外：</b> プロミネンス指標データは、2022年9月8日から利用できます。 |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | 過去45日間。 |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | 前の2か月（2）と現在の月。 |
| [!UICONTROL Assist Reports] | すべて | 過去18か月。 |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | 前年です。 |
| | [!UICONTROL Google Asset Group Performance Report] | 制限なし |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | 過去180日間。 |
| | [!UICONTROL RSA Assets Report] | 2022年8月10日より。 |
| | その他すべての[!UICONTROL Specialty Reports] | 過去2か月（2）。 |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | 過去18か月。 |
| [!UICONTROL Change History Report] | — | 過去31日間。 |

>[!MORELIKETHIS]
>
>* [ レポートについて](report-about.md)
>* [ レポートの初期設定タスク ](initial-setup.md)
