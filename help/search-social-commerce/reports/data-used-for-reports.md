---
title: レポートに使用するデータ
description: データビューとカスタムレポートで使用できる様々なタイプのデータについて説明します。
exl-id: 3e1f2967-5034-46bc-8473-63cffeeeecba
feature: Search Reports
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# レポートに使用するデータ

検索、ソーシャル、コマースには、クリックデータとコンバージョンデータに基づく、包括的なパフォーマンスレポートのセットが含まれます。 ポートフォリオまたは広告アカウントの様々なコンポーネントの基本的なパフォーマンスデータは、 [!UICONTROL Portfolios] および [!UICONTROL Campaigns] 表示を使用して、様々な基本レポートと詳細レポートを生成する方法も説明します。

また、Adobe Advertisingコンバージョントラッキングサービスを使用する広告主は、参照元 Web サイトの地理的な場所またはドメイン名のクリック数、各チャネルの広告とコンバージョンにつながる様々なイベントが全体のコンバージョン率にどのように貢献し、コンバージョンを 1 つに分布します [コンバージョン指標](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) マーケティングチャネル別。 使用できるレポートは、ユーザーのアカウントタイプによって異なります。 Adobeアカウントチームは、すべてのレポートにアクセスできます。

ほとんどのレポートは、表示する情報のみを表示するようにカスタマイズできます。 次の標準指標は、ほとんどのレポートで使用でき、広告レベルで計算されます。

* **標準的なパフォーマンス指標：**

   * **[!UICONTROL Impressions]:** 広告が配置された合計回数。

   * **[!UICONTROL Clicks]:** 広告内のリンクがクリックされた回数の合計。

   * **[!UICONTROL Cost]:** 広告の合計コスト。 クリック課金 (PPC) 広告のコストは、常にクリック数にクリックあたりのコストを掛けた値です。

   * **[!UICONTROL Cost per Click]:** 広告に対する 1 回のクリックに対する平均コストです。これは、広告のコストを広告のクリック総数で割った値です。 例えば、広告インプレッションに 100 USD を費やし、広告が 10 回のクリックを生成した場合、クリックあたりのコストは 100 USD/10=10 USD になります。

   * **[!UICONTROL Average Position]:** （該当する場合）配置された広告の平均順位。インプレッション数で重み付けされます。

   * **[!UICONTROL Estimated Clicks]:** (Adobe Advertisingコンバージョントラッキングサービスを使用する広告主向けの高度なレポートのみに含まれる ) 参照元 Web サイトの市区町村またはドメイン名に対する推定クリック数の合計です。 これには、広告主が広告アカウントを持たない広告ネットワークのデータが含まれる場合があります。

* **コンバージョン指標：** 各広告主のコンバージョン指標、またはコンバージョン指標に向けて追跡されたトランザクションデータのコンバージョンの合計数。 これには、Adobe Analyticsから同期される計算指標や高度な計算指標ではなく、コンバージョン指標やサイトエンゲージメント指標を含めることができます。

  これには次も含まれます。 [[!DNL Google Ads]追跡されたコンバージョン](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) および [[!DNL Google Analytics]追跡されたコンバージョン](/help/search-social-commerce/admin/data-sources/data-source-about.md) 広告主アカウントに同期される

* **カスタム指標：** 独自の指標。既存の指標（注文あたりのコストなど）に基づいて数式を作成することで導き出します。

## データの可用性

レポートを生成する際に、コンバージョンにつながる一連のイベントのコンバージョンデータの属性を設定する方法を選択できます。 例えば、コンバージョン全体を最後のイベントに関連付けたり、最後のイベントに他よりも多くの重みを付けたりできます。 デフォルトでは、コンバージョンは最後のイベントに関連付けられます。

レポートに指定するアトリビューションルールに応じて、各レポートタイプのデータは次の日付で利用できます。

| レポートグループ | レポート | データを利用できる日付 |
|---|---|---|
| [!UICONTROL Basic Reports] | [!UICONTROL Campaign Hourly Report] | 2021 年 5 月 15 日より。<br><br><b>例外：</b> 目立ち度の指標のデータは、2022 年 9 月 8 日より利用可能になります。 |
| | その他すべて [!UICONTROL Basic Reports] | 過去 36 ヶ月。<br><br><b>例外：</b> 目立ち度の指標のデータは、2022 年 9 月 8 日より利用可能になります。 |
| [!UICONTROL Advanced Reports] | [!UICONTROL Transaction Report] | 過去 45 日間。 |
| | [!UICONTROL Domain Referral Report], [!UICONTROL Geo Distribution Report] | 過去 2 か月と現在の月を足した値。 |
| [!UICONTROL Assist Reports] | すべて | 過去 18 ヶ月間。 |
| [!UICONTROL Specialty Reports] | [!UICONTROL AdWords Audience Target Report] | 前年。 |
| | [!UICONTROL RSA Assets Report] | 2022 年 8 月 10 日より。 |
| | [!UICONTROL MSA Ad Extension by Ad Report], [!UICONTROL MSA Ad Extension by Keyword Report], [!UICONTROL MSA Ad Extension Detail Report] | 過去 180 日間。 |
| | その他すべて [!UICONTROL Specialty Reports] | 過去 2 か月。 |
| [!UICONTROL Model Accuracy Reports] | [!UICONTROL Forecast Accuracy Report] | 過去 18 ヶ月間。 |
| [!UICONTROL Change History Report] | — | 過去 31 日間。 |

>[!MORELIKETHIS]
>
>* [レポートについて](report-about.md)
>* [レポートの初期設定タスク](initial-setup.md)
