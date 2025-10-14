---
title: （新しい UI）目標について
description: ビジネス目標を達成するための目標について説明します。
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
source-git-commit: df5d34c7d86174107278e0cd4f5a99329a21ca61
workflow-type: tm+mt
source-wordcount: '511'
ht-degree: 0%

---

# （新しい UI）目標について

*Beta機能*

目標は、利益の最大化や特定の販売目標の達成など、広告主がビジネス目標を達成するために設定する目標です。 Advertising Search、Social、Commerce、Advertising DSPの両方が目標を使用します。

* 最適化機能でポートフォリオのクリック数および売上高モデルを作成できるように、検索、ソーシャル、Commerceの各ポートフォリオに目標を設定する必要があります。

* DSPでは、検索、ソーシャル、Commerceの各アカウントにリンクされたDSP アカウントのカスタム目標として目標が表示されます。 「広告費用対効果（ROAS）の最大化」または「獲得あたりのコストの最小化（CPA）」の最適化目標を使用する各パッケージには、全体の最適化目標を達成するのに役立つカスタム目標を含める必要があります。

目的は、追跡および最適化するコンバージョン指標と、それらの指標の相対的な重み付けで構成されます。 例えば、2 つのオンライン購読レベルと 1 つの印刷購読レベルを持ち、「利益を最大化」という目的を持つオンライン雑誌が、20 USD と評価される「基本オンライン購読」、40 USD と評価される「プレミアムオンライン購読」、30 USD と評価される「印刷購読」の 3 つの指標を持つとします。 サブスクリプションの 1 回限りの金額に応じて重みを付ける場合、指標の相対的な重みはそれぞれ 1、2、1.5 になります。

目標の各指標に対して、次の操作を実行できます。

* モバイルデバイスからのコンバージョンに対して別々の重み付けを設定します。

* 指標を [!UICONTROL Goal] の指標または [!UICONTROL Assist] の指標としてラベル付けします。

* 指標に重み付けレコメンデーションを適用します。

>[!NOTE]
>* （検索、ソーシャル、Commerce）目標をポートフォリオに関連付けるには、[&#x200B; ポートフォリオを作成 &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md)、後で [&#x200B; ポートフォリオ設定を変更 &#x200B;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md) します。
>* （検索、ソーシャル、CommerceアカウントにリンクしたDSP アカウントを持つ広告主） Advertising DSPでは、パッケージレベルのペーシングを使用するパッケージの [&#x200B; カスタム最適化目標 &#x200B;](/help/dsp/campaign-management/packages/package-settings.md) として目的を選択できます。
>* 複数の検索、ソーシャル、Commerceのポートフォリオや複数のDSP パッケージに対して、同じ目的を使用できます。
>* [!UICONTROL Objectives] ビュー内の各目的の指標には、DSPのデータは含まれません。

## 使用可能な指標

目標には、次のいずれかを含めることができます。

* Adobe Advertisingが [Adobe Advertising コンバージョントラッキングピクセル &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md) を使用して追跡する指標。

* [&#x200B; コンバージョンフィードファイルから広告主が追跡した指標 &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* （[!DNL Adobe Analytics for Advertising] を使用する広告主） [Adobe Analyticsから同期されたコンバージョンおよびサイトエンゲージメント指標 &#x200B;](/help/integrations/analytics/overview.md)。

  検索、ソーシャル、Commerceでは、[、](/help/integrations/analytics/analytics-data-in-advertising.md)、`timespent_secs_1stvisit`、`timespent_secs_total`、`pageviews_1stvisit` の `pageviews_total` サイトエンゲージメント指標 `bounces` が、ポートフォリオ入札アルゴリズムに自動的に組み込まれます。

* [!DNL Google] 指標：<!-- Search only, or might DSP-only clients also have these? -->

   * 同期された [[!DNL Google Ads] アカウントからの &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) [!DNL Google Ads] で追跡されたコンバージョン。

   * （[[!DNL Google Analytics]  統合 &#x200B;](/help/search-social-commerce/admin/data-sources/data-source-about.md)）ページビュー、セッション、バウンス率（バウンス/セッションとして計算）、セッション時間を使用する広告主。

     検索、ソーシャル、Commerceでは、これらの指標は、ポートフォリオ入札アルゴリズムに自動的に組み込まれます。

## 広告ネットワークに目標をアップロードするオプション

オプションで [&#x200B; アカウントのポートフォリオの目標をコンバージョンとして  [!DNL Google Ads]  アップロード  [!DNL Microsoft Advertising]  でき、キャンペーンレベルまたは広告グループレベルの最適化に使用できる &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md) うになります。 このオプションを有効にすると、検索、ソーシャル、Commerceでは、毎日、EF ID （クリック ID）レベルで重み付けされた売上高データが広告ネットワークに渡されます。 ネットワークで追跡される広告の指標は省略されます。

>[!MORELIKETHIS]
>
>* [&#x200B; 目標の作成 &#x200B;](objective-create.md)
>* [&#x200B; 目標の編集 &#x200B;](objective-edit.md)
>* [&#x200B; 目標の削除 &#x200B;](objective-delete.md)
>* [&#x200B; 目標への重み付けレコメンデーションの適用 &#x200B;](objective-apply-weight-recommendations.md)
>* [&#x200B; 目標の設定 &#x200B;](objective-settings.md)
