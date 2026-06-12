---
title: Adobe CX Enterpriseのソリューションおよびサービスとの統合
description: Search, Social, & CommerceとAdobe CX Enterpriseのソリューションやサービスの連携について説明します。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
TQID: https://experienceleague.adobe.com/vIjCxWutfGn8H9-TqxLvztNazb9RWq7ECeoOQXLfyEw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: f2860a4b-f905-4545-bead-1bbc92564592
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 619
ht-degree: 0%

---

# Adobe CX Enterpriseのソリューションおよびサービスとの統合

Advertising Search, Social, &amp; Commerceは、次の[!DNL Adobe]製品と統合されています。

* [Adobe Experience Platformのタグ &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — Adobe Experience Platform用の[Adobe Advertising Cloud拡張機能](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud)を使用して、広告ランディングページ用のAdobe Advertising コンバージョン トラッキングタグ [&#128279;](/help/search-social-commerce/tools/conversion-tag-generate.md)およびサードパーティのトラッキングタグを[作成できます。 組織にExperience Platform アカウントがない場合でも、Adobe CX Enterpriseのお客様が無料で利用できるAdobe Experience Platform Data Collection](https://experience.adobe.com/#/data-collection/)の ユーザーインターフェイスに直接拡張機能をインストールできます。

  必要な拡張機能をインストールするには、組織管理者に連絡して、UIのデータ収集機能へのアクセス権を取得し、`manage_properties`権限の付与を依頼してください。

  **注：** Search, Social, &amp; Commerce[&#128279;](/help/search-social-commerce/tools/conversion-tag-generate.md)内で直接 コンバージョン トラッキング タグを作成することもできます。

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics — （オプトイン機能） Adobe Advertisingと[!DNL Analytics]は、次の方法で統合されます。

   * Adobe Advertisingと[!DNL Analytics]はシームレスにデータを共有します。 [!DNL Analytics]は、サイトのエンゲージメントとコンバージョンデータをSearch, Social, &amp; Commerceに毎日送信できます。このデータは、広告の最適化とレポートに利用できます。 また、Adobe Advertisingでは、広告ネットワークから毎日[!DNL Analytics]に広告トラフィックデータ（インプレッション数、クリック数、コストを含む）を送信できます。このデータは、すべてのレポートツールで利用できます。

     各広告ネットワークと広告タイプの[!DNL Analytics]のサポートについて詳しくは、「[&#x200B; サポートされているインベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。 データ交換について詳しくは、「[概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}」も参照してください。

     データを交換するには、最初にAdobe Advertisingと[!DNL Analytics]の両方を設定する必要があります。 初期設定について詳しくは、Adobe アカウントチームにお問い合わせください。

     >[!NOTE]
     >
     >デフォルトでは、[!DNL Analytics]指標はSearch、Social、Commerceの画面には表示されません。 [!DNL Adobe]実装チームが選択した標準イベントまたはカスタムイベントをAdobe Advertisingに渡すように設定した後、[指標をキャンペーン管理ビュー、ポートフォリオ、レポート &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)で明示的に使用できるようにする必要があります。 オプションで、表示される指標名を変更できます（[!DNL Analytics]では変更されません）。 UIで指標を表示できるようにし、指標の名前を[!UICONTROL Admin] > [!UICONTROL Conversions]から変更できます。

   * [!DNL Analytics]を持つがAudience Managerを持たない広告主は、Adobe CX Enterpriseと共有されている[!DNL Analytics] セグメントから[customer match audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)を作成できます。  [!DNL Google Ads] 広告主が資格を得るには、[Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html)を実装し、そのweb サイトにタグをデプロイする必要があります。 次に、[!DNL Google Ads]件のキャンペーンのオーディエンスを、キャンペーンレベルまたは広告グループレベルの[&#x200B; ターゲット &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)または[除外](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)として使用できます。

* Adobe Audience Manager セグメント – （オプトイン機能）検索、ソーシャル、およびCommerceを宛先として持つAudience Manager セグメントから[customer match audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md)を作成できます。  [!DNL Google Ads] これには、Adobe CX Enterpriseに公開される[!DNL Analytics]個のセグメントと、Adobe CX Enterprise Audience Libraryを使用して作成されるセグメントが含まれます。 次に、[!DNL Google Ads]件のキャンペーンのオーディエンスを、キャンペーンレベルまたは広告グループレベルの[&#x200B; ターゲット &#x200B;](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md)または[除外](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)として使用できます。

  詳しくは、「[Adobe AdvertisingとAdobe Audience Manager](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)」を参照してください。

* Adobe Target — Search、Social、およびCommerceと[!DNL Target]の間でクリックスルー信号の共有を実装し、広告用に[!DNL Target]でA/B テストアクティビティを設定し、[!DNL Analytics] Analysis Workspaceを使用してテストデータを表示できます。

* Adobe Campaign — [!DNL Campaign][&#128279;](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)内のメールリストを使用して、顧客マッチオーディエンスを作成および更新できます。 [!DNL Google Ads] 

* Adobe CX Enterprise Notifications — （Adobe CX Enterpriseを介してログインしている場合）各ページの上部にある通知リンク（[&#x200B; アラート通知](/help/search-social-commerce/assets/notifications-panel.png "アラート通知")）から、すべてのAdobe CX Enterprise システムの更新、投稿、メンション、および共有アセットを表示できます。 Adobe CX Enterpriseへのアクセスについて詳しくは、Adobe アカウントチームにお問い合わせください。
