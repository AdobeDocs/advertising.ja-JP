---
title: レポートに使用するデータ
description: データビューとカスタムレポートで使用できる様々なタイプのデータについて説明します。
exl-id: ba808b21-4421-4de5-9293-a20ec67cc81c
feature: Search Reports
source-git-commit: f357d9a9ec0f8b38fbc43726265521e6fd77c7d0
workflow-type: tm+mt
source-wordcount: '599'
ht-degree: 0%

---

# レポートに使用するデータ

検索、ソーシャル、Commerceには、クリックおよびコンバージョンデータに基づく包括的なパフォーマンスレポートのセットが含まれています。 ポートフォリオまたは広告アカウントの様々なコンポーネントに関する基本的なパフォーマンスデータは、[!UICONTROL Portfolios] ビューと [!UICONTROL Campaigns] ビューから表示できるほか、様々な基本レポートと詳細レポートを生成して表示できます。

また、Adobe Advertisingコンバージョントラッキングサービスを使用する広告主は、参照する Web サイトの地理的な場所やドメイン名のクリック数、各チャネルの広告およびコンバージョンにつながる様々なイベントが全体的なコンバージョン率にどのように貢献しているか、マーケティングチャネル別に 1 つの [&#x200B; コンバージョン指標 &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) のコンバージョンの分布を特定することもできます。 使用可能なレポートは、ユーザーアカウントのタイプによって異なります。 Adobeアカウントチームは、すべてのレポートにアクセスできます。

ほとんどのレポートは、必要な情報のみを表示するようにカスタマイズできます。 ほとんどのレポートで使用でき、広告レベルで計算される標準指標は次のとおりです。

* **標準パフォーマンス指標：**

   * **[!UICONTROL Impressions]:** 広告が配置された合計回数。

   * **[!UICONTROL Clicks]:** 広告内のリンクがクリックされた合計回数。

   * **[!UICONTROL Cost]:** 広告の合計コスト。 クリック課金（PPC）広告のコストは、常にクリック数にクリック単価を掛けた値です。

   * **[!UICONTROL Cost per Click]:** 広告の 1 回のクリックの平均コスト。これは、広告のコストを広告のクリック総数で割った値です。 例えば、広告インプレッションに 100 USD を費やし、広告が 10 クリックを生成した場合、クリックあたりのコストは 100 USD/10=10 クリックあたり 10 USD になります。

   * **[!UICONTROL Average Position]:** （該当する場合）配置された広告の平均位置。インプレッション数で重み付けされます。

   * **[!UICONTROL Estimated Clicks]:** （Adobe Advertisingコンバージョントラッキングサービスを使用する広告主の詳細レポートにのみ含まれる）参照元の web サイトの市区町村またはドメイン名の推定クリック総数。 これには、広告主が広告アカウントを持たない広告ネットワークのデータが含まれる場合があります。

* **コンバージョン指標：** 広告主のコンバージョン指標またはコンバージョン指標に対して追跡されたトランザクションデータごとのコンバージョンの合計数。 これには、Adobe Analyticsから同期されたコンバージョン指標とサイトエンゲージメント指標が含まれますが、計算指標や高度な計算指標は含まれません。

  これには、広告主アカウントに対して同期される [[!DNL Google Ads] 追跡コンバージョン &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) および [[!DNL Google Analytics] 追跡コ &#x200B;](/help/search-social-commerce/admin/data-sources/data-source-about.md) ンバージョンも含まれる場合があります。

* **カスタム指標：** 既存の指標（注文あたりのコストなど）に基づいて数式を作成することによって導き出される独自の指標。

## データの可用性

レポートを生成する際に、コンバージョンにつながる一連のイベントにおけるコンバージョンデータの属性方法を選択できます。 例えば、コンバージョン全体を最後のイベントに関連付けたり、最後のイベントに他のイベントよりも重みを付けたりできます。 デフォルトでは、コンバージョンは最後のイベントに関連付けられます。

レポートに指定したアトリビューションルールに応じて、次の日付の各レポートタイプのデータを使用できます。

| 報告書グループ | 報告書 | データを利用できる日付 |
| --- | --- | --- |
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | 2021 年 5 月 15 日より。<br><br><b> 例外：</b> 知名度の指標データは、2022 年 9 月 8 日（PT）から利用できるようになります。 |
| | その他すべての [!UICONTROL Basic Reports] | 過去 36 か月。<br><br><b> 例外：</b> 知名度の指標データは、2022 年 9 月 8 日（PT）から利用できるようになります。 |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | 過去 45 日間。 |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | 過去 2 か月と現在の月の合計。 |
| [!UICONTROL Assist Reports] | すべて | 過去 18 か月。 |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | 前年。 |
| | [!UICONTROL Google Asset Group Performance Report] | 制限なし |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report], [!UICONTROL MSA Network Impression Share Report], [!UICONTROL MSA Network Performance Report] | 過去 180 日間。 |
| | [!UICONTROL RSA Assets Report] | 2022 年 8 月 10 日より。 |
| | その他すべての [!UICONTROL Specialty Reports] | 過去 2 か月。 |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | 過去 18 か月。 |
| [!UICONTROL Change History Report] | — | 過去 31 日間。 |

>[!MORELIKETHIS]
>
>* [&#x200B; レポートについて &#x200B;](report-about.md)
>* [&#x200B; レポートの初期設定タスク &#x200B;](initial-setup.md)
