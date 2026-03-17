---
title: Adobe Experience Cloudのソリューションおよびサービスとの統合
description: Adobe Experience Cloud ソリューションおよびサービスと検索、ソーシャル、Commerceの統合について説明します。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: 3f91cd92a364a8e9dd569bd590c59740ea1493d7
workflow-type: tm+mt
source-wordcount: '573'
ht-degree: 0%

---

# Adobe Experience Cloudのソリューションおよびサービスとの統合

Advertisingの検索、ソーシャル、Commerceは、次の [!DNL Adobe] 製品と統合されています。

* [Adobe Experience Platformのタグ ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) - Adobe Experience Platform用 [Adobe Advertising Cloud 拡張機能 ](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud) を使用して、広告ランディングページ用に [Adobe Advertising コンバージョントラッキングタグの作成 ](/help/search-social-commerce/tools/conversion-tag-generate.md) およびサードパーティのトラッキングタグを作成）できます。 組織がExperience Platform アカウントを持っていない場合でも、Adobe Experience Cloudのお客様が無償で利用できる [Adobe Experience Platform Data Collection のユーザーインターフェイス ](https://experience.adobe.com/#/data-collection/) で直接拡張機能をインストールできます。

  必要な拡張機能をインストールするには、組織の管理者に連絡して UI のデータ収集機能へのアクセス権を取得し、`manage_properties` の権限の付与を依頼します。

  **メモ：** 検索、ソーシャル、Commerce内に [ コンバージョントラッキングタグを直接作成 ](/help/search-social-commerce/tools/conversion-tag-generate.md) することもできます。

<!-- another link re tags, which is more direct within the tags docs but not very useful:  https://exchange.adobe.com/apps/ec/100155 -->

* Adobe Analytics - （オプトイン機能）Adobe Advertisingと [!DNL Analytics] は、次のように統合されます。

   * Adobe Advertisingと [!DNL Analytics] はシームレスにデータを共有します。 [!DNL Analytics] は、サイトエンゲージメントおよびコンバージョンデータを毎日、検索、ソーシャル、Commerceに送信でき、そこで広告の最適化やレポート作成にデータを利用できます。 また、Adobe Advertisingは、インプレッション数、クリック数、コストを含む広告トラフィックデータを、毎日広告ネットワークから [!DNL Analytics] に送信できます。ここで、データはすべてのレポートツールで利用できます。

     各広告ネットワークと広告タイプのサポートについて詳しくは [](/help/search-social-commerce/introduction/supported-inventory.md) サポートされてい [!DNL Analytics] 在庫」を参照してください。 データ交換の詳細については、「[ の概要  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}」も参照してください。

     データを交換するには、最初にAdobe Advertisingと [!DNL Analytics] の両方を設定する必要があります。 初期設定について詳しくは、Adobe アカウントチームにお問い合わせください。

     >[!NOTE]
     >
     >デフォルトでは、[!DNL Analytics] の指標は、検索画面、ソーシャル画面およびCommerce画面には表示されません。 [ 実装チームが選択した標準イベントまたはカスタムイベントをAdobe Advertisingに渡すように設定したら ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) 指標を明示的に [!DNL Adobe] キャンペーン管理ビュー、ポートフォリオ、レポートで使用できるようにする）必要があります。 オプションで、表示される指標名を（[!DNL Analytics] で変更せずに）変更できます。 UI で指標を表示可能にし、[!UICONTROL Admin] / [!UICONTROL Conversions] から指標の名前を変更できます。

   * [!DNL Analytics] を持つがAudience Managerを持たない広告主は、Adobe Experience Cloudと共有される [ セグメントから  [!DNL Google Ads]  作成 ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) カスタマーマッチオーディエンス [!DNL Analytics] を行うことができます。 広告主が資格を得るには、[Adobe Experience Platform ID サービスを実装し ](https://experienceleague.adobe.com/docs/id-service/using/home.html)Web サイトにタグをデプロイする必要があります。 その後、[!DNL Google Ads] キャンペーンのオーディエンスをキャンペーンレベルまたは広告グループレベルの [ ターゲット ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [ 除外 ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) として使用できます。

* Adobe Audience Manager セグメント – （オプトイン機能）検索、ソーシャル、Commerceを宛先として持つAudience Manager セグメントから [ 作成  [!DNL Google Ads]  カスタマーマッチオーディエンス ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) を使用）できます。 これには、Adobe Experience Cloudに公開される [!DNL Analytics] セグメントと、Adobe Experience Cloud オーディエンスライブラリを使用して作成されるセグメントが含まれる場合があります。 その後、[!DNL Google Ads] キャンペーンのオーディエンスをキャンペーンレベルまたは広告グループレベルの [ ターゲット ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [ 除外 ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) として使用できます。

  詳しくは、「[Adobe Audience ManagerとのAdobe Advertising統合 ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)」を参照してください。

* Adobe Target - Search、Social、およびCommerceと [!DNL Target] の間にクリックスルーのシグナル共有を実装し、広告に [!DNL Target] する A/B テストアクティビティを設定してから、Analysis Workspaceを使用してテストデータ [!DNL Analytics] 表示できます。

* Adobe Campaign[ 内のメールリストを使用して、カスタマーマッチオーディエ  [!DNL Google Ads]  スを作成および更新  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md) できます。

* Adobe Experience Cloud通知 – （Adobe Experience Cloudでログインしている場合）各ページの上部にある通知リンク（[ アラート通知 ](/help/search-social-commerce/assets/notifications-panel.png "アラート通知")）から、Adobe Experience Cloud システムのアップデート、投稿、メンションおよび共有されているアセットをすべて表示できます。 Adobe Experience Cloudへのアクセスについて詳しくは、Adobe アカウントチームにお問い合わせください。
