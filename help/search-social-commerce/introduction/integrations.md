---
title: Adobe Experience Cloudソリューションおよびサービスとの統合
description: Adobe Experience Cloudのソリューションおよびサービスとの Search、Social、および Commerce の統合について説明します。
exl-id: e8b521f5-f426-4c50-9df4-361a047c9ff0
feature: Search Introduction
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '550'
ht-degree: 0%

---

# Adobe Experience Cloudソリューションおよびサービスとの統合

広告検索、ソーシャル、コマースは、次の [!DNL Adobe] 製品。

* [Adobe Experience Platformのタグ](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/overview.html) — [Adobe Advertising Cloud Extension](https://exchange.adobe.com/apps/ec/100155) Adobe Experience Platformで、広告ランディングページのAdobe Advertisingコンバージョントラッキングタグとサードパーティトラッキングタグを作成する場合。 ( また、 [検索、ソーシャル、コマース内で直接コンバージョントラッキングタグを作成します。](/help/search-social-commerce/tools/conversion-tag-generate.md).) タグに含める情報については、Adobeのアカウントチームまたは実装チームにお問い合わせください。

* Adobe Analytics — （オプトイン機能）Adobe Advertisingおよび [!DNL Analytics] は、次の方法で統合されます。

   * Adobe Advertisingと [!DNL Analytics] データをシームレスに共有します。 [!DNL Analytics] は、サイトエンゲージメントおよびコンバージョンデータを毎日検索、ソーシャル、コマースに送信できます。検索では、データを広告の最適化やレポート作成に使用できます。 また、Adobe Advertisingは、インプレッション数、クリック数、コストなどの広告トラフィックデータを広告ネットワークから毎日に送信できます。 [!DNL Analytics]（すべてのレポートツールでデータを使用できます）。

     参照：[サポートされている在庫](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。 [!DNL Analytics] 各広告ネットワークおよび広告タイプのサポート。 関連項目：[の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html){target="_blank"}」を参照してください。

     データを交換するには、Adobe Advertisingと [!DNL Analytics] は、最初に設定する必要があります。 初期設定の詳細については、担当のAdobeアカウントチームにお問い合わせください。

     >[!NOTE]
     >
     >デフォルトでは、 [!DNL Analytics] 指標は、検索、ソーシャル、コマースの各画面に表示されません。 明示的に [キャンペーン管理ビュー、ポートフォリオおよびレポートで指標を使用できるようにする](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md) の後 [!DNL Adobe] 実装チームが、選択した標準イベントまたはカスタムイベントをAdobe Advertisingに渡すように設定しました。 オプションで、表示される指標の名前を変更できます ( [!DNL Analytics]) をクリックします。 UI で指標を表示可能にし、指標の名前を [!UICONTROL Admin] > [!UICONTROL Transaction Properties].

   * 次を持つ広告主 [!DNL Analytics] しかし、Audience Managerはできない [作成 [!DNL Google Ads] 顧客一致オーディエンス](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) から [!DNL Analytics] Adobe Experience Cloudと共有されるセグメント。 実施要件を満たすには、広告主が [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) をクリックし、Web サイトにタグをデプロイします。 その後、 [!DNL Google Ads] キャンペーンレベルまたは広告グループレベルとしてのキャンペーン [ターゲット](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [除外](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

* Adobe Audience Managerセグメント — （オプトイン機能）次のことができます。 [作成 [!DNL Google Ads] 顧客一致オーディエンス](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md) を、Search、Social、および Commerce を宛先とするAudience Managerセグメントから削除します。 これには次が含まれます。 [!DNL Analytics] Adobe Experience Cloudに公開されたセグメントと、Adobe Experience Cloud Audience Library を使用して作成されたセグメント。 その後、 [!DNL Google Ads] キャンペーンレベルまたは広告グループレベルとしてのキャンペーン [ターゲット](/help/search-social-commerce/campaign-management/campaigns/audience-targets-manage.md) または [除外](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md).

  参照：[Adobe Audience ManagerとのAdobe Advertising統合](https://experienceleague.adobe.com/docs/advertising/integrations/audience-manager/overview.html)」を参照してください。

* Adobe Target — 検索、ソーシャル、コマース、およびコマース間でのクリックスルーシグナル共有を実装できます。 [!DNL Target]、A/B テストアクティビティを [!DNL Target] 広告の場合は、 [!DNL Analytics] Analysis Workspaceをクリックして、テストデータを表示します。

* Adobe Campaign — 以下を実行できます。 [作成と更新 [!DNL Google Ads] 内の電子メールリストを使用した顧客一致オーディエンス [!DNL Campaign]](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md).

* Adobe Experience Cloud通知 — (Adobe Experience Cloudを通じてログインしている場合 ) 通知リンク ([アラート通知](/help/search-social-commerce/assets/notifications-panel.png "アラート通知")) を各ページの上部に表示すると、Adobe Experience Cloudのすべてのシステム更新、投稿、メンションおよび共有されたアセットを表示できます。 Adobe Experience Cloudへのアクセスについて詳しくは、Adobeのアカウントチームにお問い合わせください。
