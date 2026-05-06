---
title: （新しいUI）目的について
description: ビジネス目標を達成する方法を解説します。
feature: Search Objectives, Search Optimization
hide: true
exl-id: 4e417307-1403-4420-85f9-2fa04c253b58
TQID: https://experienceleague.adobe.com/fcdOJhTTB-IML-aownM6-vyYM4NJspKpCraypmuLooE
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
autotag-review: '2026-04-14T00:06:19.870Z'
source-git-commit: 604fb0c3541ba9c3b1fdb1c3cae5464bfcf67d4d
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# （新しいUI）目的について

<!-- no subfeature tag for objectives -->

*Beta機能*

目標とは、利益を最大化したり、特定の販売目標を達成したりするなど、広告主がビジネス目標を達成するために設定する目標です。 Advertising Search, Social, &amp; CommerceおよびAdvertising DSPの使用目的：

* Search, Social, &amp; Commerceの各ポートフォリオには、最適化機能がポートフォリオのクリックと収益モデルを作成できるように、目的が必要です。

* DSPでは、目標は、Search、Social、およびCommerce アカウントにリンクされているDSP アカウントのカスタム目標として表示されます。 最適化目標「広告費用対効果（ROAS）の最大化」または「顧客獲得単価（CPA）」を使用する各パッケージには、全体的な最適化目標の達成に役立つカスタム目標が含まれている必要があります。

目的は、追跡および最適化されるコンバージョン指標と、これらの指標の相対的な重みによって構成されます。 例えば、2つのオンライン購読レベルと1つの印刷物の購読レベルを持つオンライン雑誌で、目的の「利益を最大化」が3つの指標を持つとします。20米ドルの「基本的なオンライン購読」、40米ドルの「プレミアムオンライン購読」、30米ドルの「印刷物の購読」です。 雑誌が購読の1回限りの金銭的価値に応じて重みを与えたい場合、指標の相対的な重みはそれぞれ1、2、および1.5になります。

目的の各指標について、次のことができます。

* モバイルデバイスからのコンバージョン用に個別の重みを設定します。

* 指標を[!UICONTROL Goal]指標または[!UICONTROL Assist]指標としてラベル付けします。

* 指標に重み付けの推奨事項を適用します。

>[!NOTE]
>* （検索、ソーシャル、およびCommerce）ポートフォリオを[作成](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md)するか、後で[&#x200B; ポートフォリオ設定を変更](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md)することで、目標をポートフォリオに関連付けることができます。
>* （Search、Social、およびCommerce アカウントにリンクされたDSP アカウントを持つ広告主） Advertising DSPでは、目的をパッケージレベルのペーシングを持つパッケージの[&#x200B; カスタム最適化目標](/help/dsp/campaign-management/packages/package-settings.md)として選択できます。
>* 複数のSearch、Social、およびCommerce ポートフォリオや複数のDSP パッケージに同じ目的を使用できます。
>* [!UICONTROL Objectives] ビューの各目的の指標には、DSPのデータは含まれていません。

## 利用可能な指標

目標には、次のいずれかを含めることができます。

* [Adobe Advertising コンバージョントラッキングピクセル &#x200B;](/help/search-social-commerce/tracking/conversion-tracking-advertising.md)を使用してAdobe Advertisingが追跡する指標。

* [&#x200B; コンバージョンフィード ファイルから広告主が追跡した指標](/help/search-social-commerce/tracking/conversion-tracking-about.md).<!-- Search only, or might DSP-only clients also have these? -->

* （広告主と[!DNL Adobe Analytics for Advertising]） [&#x200B; コンバージョンとサイトエンゲージメントの指標がAdobe Analytics](/help/integrations/analytics/overview.md)から同期されました。

  Search, Social, &amp; Commerceでは、次の[&#x200B; サイトエンゲージメント指標](/help/integrations/analytics/analytics-data-in-advertising.md)がポートフォリオ入札アルゴリズムに自動的に組み込まれます：`timespent_secs_1stvisit`、`timespent_secs_total`、`pageviews_1stvisit`、`pageviews_total`、および`bounces`。

* [!DNL Google]指標：<!-- Search only, or might DSP-only clients also have these? -->

   * 同期した[!DNL Google Ads] アカウントから[[!DNL Google Ads]件のトラッキングされたコンバージョン &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)。

   * （統合[[!DNL Google Analytics] の広告主](/help/search-social-commerce/admin/data-sources/data-source-about.md)） ページビュー、セッション、直帰率（バウンス/セッションとして計算）、セッション時間。

     Search, Social, &amp; Commerceでは、これらの指標は自動的にポートフォリオ入札アルゴリズムに組み込まれます。

## 広告ネットワークに目的をアップロードするオプション

オプションで[&#x200B; アカウントのポートフォリオの目標を [!DNL Google Ads] および/または [!DNL Microsoft Advertising]  コンバージョン &#x200B;](/help/search-social-commerce/tools/objective-upload-to-networks.md)として アップロードして、キャンペーンレベルまたは広告グループレベルの最適化に使用できます。 このオプションを有効にすると、Search, Social, &amp; Commerceは、EF ID （クリック ID）レベルの重み付けされた収益データを毎日アドネットワークに渡します。 ネットワークで追跡される広告の指標が省略されます。

>[!MORELIKETHIS]
>
>* [目標を作成](objective-create.md)
>* [目標を編集](objective-edit.md)
>* [目標を削除](objective-delete.md)
>* [目標に重み付けの推奨事項を適用](objective-apply-weight-recommendations.md)
>* [目標の設定](objective-settings.md)
>* [目的のパフォーマンスデータをダウンロード &#x200B;](objective-download-performance-data.md)
