---
title: Adobe Experience Cloudのソリューションおよびサービスとの統合
description: Adobe Experience Cloud ソリューションおよびサービスと検索、ソーシャル、Commerceの統合について説明します。
exl-id: 26456f60-937a-4f39-b5cf-a71c1c1b4833
feature: Search Introduction
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# Adobe Experience Cloudのソリューションおよびサービスとの統合

Advertisingの検索、ソーシャル、Commerceは、次の [!DNL Adobe] 製品と統合されています。

* [Adobe Experience Platformのタグ ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html?lang=ja) - Adobe Experience Platformの [Adobe Advertising Cloud拡張機能 ](https://exchange.adobe.com/apps/ec/100155) を使用して、広告ランディングページ用に、サードパーティのトラッキングタグに加えて、Adobe Advertisingコンバージョントラッキングタグを作成できます。 （[ 検索、ソーシャル、Commerce内に直接、コンバージョントラッキングタグを作成する ](/help/search-social-commerce/tools/conversion-tag-generate.md) こともできます。） タグに含める情報については、Adobeアカウントチームまたは実装チームにお問い合わせください。

* Adobe Analytics - （オプトイン機能）Adobe Advertisingと [!DNL Analytics] は、次のように統合されています。

   * Adobe Advertisingと [!DNL Analytics] はシームレスにデータを共有します。 [!DNL Analytics] は、サイトエンゲージメントおよびコンバージョンデータを毎日、検索、ソーシャル、Commerceに送信でき、そこで広告の最適化やレポート作成にデータを利用できます。 また、Adobe Advertisingは、インプレッション数、クリック数、コストなどの広告トラフィックデータを、毎日広告ネットワークから [!DNL Analytics] に送信できます。

     各広告ネットワークと広告タイプのサポートについて詳しくは [&#128279;](/help/search-social-commerce/introduction/supported-inventory.md) サポートされてい [!DNL Analytics] 在庫」を参照してください。 データ交換の詳細については、「[ の概要  [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html?lang=ja){target="_blank"}」も参照してください。

     データを交換するには、最初にAdobe Advertisingと [!DNL Analytics] の両方を設定する必要があります。 初期設定について詳しくは、Adobeアカウントチームにお問い合わせください。

     >[!NOTE]
     >
     >デフォルトでは、[!DNL Analytics] の指標は、検索画面、ソーシャル画面およびCommerce画面には表示されません。 [!DNL Adobe] 実装チームが選択した標準イベントまたはカスタムイベントをAdobe Advertisingに渡すように設定したら [&#128279;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) 指標を明示的に  キャンペーン管理ビュー、ポートフォリオ、レポートで使用できるようにする）必要があります。 オプションで、表示される指標名を（[!DNL Analytics] で変更せずに）変更できます。 UI で指標を表示可能にし、[!UICONTROL Admin] / [!UICONTROL Conversions] から指標の名前を変更できます。

   * [!DNL Analytics] を持つがAudience Managerを持たない広告主は、Adobe Experience Cloudと共有される [!DNL Analytics] セグメントから [ カスタマーマッチオーディエンスを作成  [!DNL Google Ads]  作成 ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) できます。 広告主が資格を得るには、[Adobe Experience Platform ID サービスを実装し ](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja)Web サイトにタグをデプロイする必要があります。 その後、[!DNL Google Ads] キャンペーンのオーディエンスをキャンペーンレベルまたは広告グループレベルの [ ターゲット ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [ 除外 ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) として使用できます。

* Adobe Audience Manager セグメント – （オプトイン機能）検索、ソーシャル、Commerceを宛先として持つAudience Managerセグメントから [ 作成  [!DNL Google Ads]  カスタマーマッチオーディエンス ](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) を使用）できます。 これには、Adobe Experience Cloudに公開される [!DNL Analytics] セグメントと、Adobe Experience Cloud オーディエンスライブラリを使用して作成されるセグメントが含まれる場合があります。 その後、[!DNL Google Ads] キャンペーンのオーディエンスをキャンペーンレベルまたは広告グループレベルの [ ターゲット ](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [ 除外 ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md) として使用できます。

  詳しくは、「[Adobe Audience ManagerとのAdobe Advertising統合 ](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html?lang=ja)」を参照してください。

* Adobe Target - Search、Social、およびCommerceと [!DNL Target] の間にクリックスルーのシグナル共有を実装し、広告に [!DNL Target] する A/B テストアクティビティを設定してから、Analysis Workspaceを使用してテストデータ [!DNL Analytics] 表示できます。

* Adobe Campaign[ 内のメールリストを使用して、カスタマーマッチオーディエ  [!DNL Google Ads]  スを作成および更新  [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md) できます。

* Adobe Experience Cloud通知 – （Adobe Experience Cloudでログインしている場合）各ページの上部にある通知リンク（[ アラート通知 ](/help/search-social-commerce/assets/notifications-panel.png "アラート通知")）から、Adobe Experience Cloud システムのアップデート、投稿、メンションおよび共有されているアセットをすべて表示できます。 Adobe Experience Cloudへのアクセスについて詳しくは、Adobeアカウントチームにお問い合わせください。
