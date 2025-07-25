---
title: 新機能
description: Adobe Experience CloudのAdobe Advertisingと他の製品およびサービスとの統合のアップデートについて説明します。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: ae93aff0056e58fd4427620d2eab76330a73039c
workflow-type: tm+mt
source-wordcount: '790'
ht-degree: 0%

---

# 新機能

次の機能は、新規または最近変更された機能です。

| 日付 | 機能 | 説明 | 詳細情報 |
| ---- | ------- | ----------- | -------------------- |
| 2025 年 3 月 26 日（Pt） | [!DNL Adobe Analytics for Advertising] | （検索、ソーシャル、Commerce、[!DNL Microsoft Advertising] アカウント、[!DNL Adobe Analytics for Advertising] を使用する広告主） [!UICONTROL Auto Upload] トラッキングオプションを使用するアカウントの場合、すべてのキャンペーンタイプのランディングページサフィックスの AMO ID パラメーターの形式が最新の形式に更新されました。 以前は、ほとんどのアカウントのパフォーマンス最大化キャンペーンは、新しいフォーマットに移行されていました。<br><br> ただし、[!UICONTROL Auto Upload] トラッキングオプションを持たないアカウントで、新しい形式にまだ移行されていない場合、新しい AMO ID 形式を含めるには、各ランディングページのサフィックスを手動で更新する必要があります。<br><br> 現在の形式：`s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | [ 概要  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)」および [AMO ID 形式 ](/help/integrations/analytics/ids.md#amo-id-formats)」を参照してください。 |
| 2024 年 11 月 13 日（Pt） | [!DNL Analytics for Advertising] | （[!DNL Analytics for Advertising] およびAdobe Customer Journey Analyticsを使用する広告主）予約変数を使用して AMO ID および EF ID を取得する場合は、AMO ID および EF ID の予約変数を可能な限り早く標準 [!DNL eVars] にコピーすることで、Adobe AdvertisingとAdobe Customer Journey Analyticsの間で今後の統合に備えることができます。 これにより、タスクが完了するとすぐに AMO ID と EF ID の履歴データを収集でき、履歴データは今後の使用のために利用できるようになります。 予約変数を使用していて、このタスクを実行する必要がある場合は、Adobe アカウントチームからお知らせします。 | [Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データの収集 ](/help/integrations/analytics/rvars-to-evars.md) を参照してください。 |
| リリース日：2024 年 10 月 29 日（Pt） | [!DNL Adobe Analytics for Advertising] | （[!DNL Adobe Analytics for Advertising] および [!DNL Microsoft Advertising] の Performance MAX キャンペーンを使用する広告主）広告およびキーワードを含まない Performance MAX キャンペーンのトラッキング URL に新しい AMO ID （[!DNL s_kwcid]）パラメーターを実装した際に、Performance MAX キャンペーンのアセットグループレベルのデータがAdobe Analyticsで使用できるようになりました。 Performance MAX キャンペーンを使用するほとんどのアカウントのトラッキングは、既に新しいフォーマットに移行されています。 ただし、[!UICONTROL Auto Upload] トラッキングオプションを持たず、新しい形式に移行されていない performance max キャンペーンのアカウントの場合、新しい AMO ID 形式を含めるには、各ランディングページのサフィックスを手動で更新する必要があります。<br><br>Performance MAX キャンペーンのAdobe Analytics データは、検索、ソーシャル、Commerceでも利用できます。 | 新しい [AMO ID 形式 ](/help/integrations/analytics/ids.md#amo-id-formats) および [ トラッキング URL にパラメーターを追加するタイミングと方法 ](/help/integrations/analytics/ids.md#amo-id-implement) を参照してください。 |
| 2023 年 12 月 16 日（Pt） | ヘルプ | 新しいドキュメントでは、検索、ソーシャル、Commerceの広告からのクリックスルートラフィックに対して [!DNL Target] で A/B テストを設定する方法と、[!DNL Analytics] でテストを測定および視覚化する方法に関するヒントを説明します。 | 詳しくは、「[ 検索、ソーシャル、Commerce広告用のAdobe Targetでの A/B テストの設定 ](/help/integrations/target/ab-tests-search.md) を参照してください。 |
| 2023 年 8 月 8 日（Pt） | [!DNL Analytics for Advertising] | 標準、カスタムおよび予約済みのコンバージョン指標やトラフィック指標など、一部の [!DNL Analytics] スタムサクセスイベント指標は、DSPや、検索、ソーシャル、Commerceで自動的に使用できます。 現在は、[!DNL Analytics] レベルおよび [!DNL eVars] レベルのデータをカスタムの成功イベントに送ることで、既存の [!DNL props] [!DNL eVar] と [!DNL prop] に基づいて独自の成功指標を設定することもできます。 | [Adobe Analyticsからのコンバージョン指標の作成  [!DNL eVars]  および  [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)」を参照してください。 |
| 2023 年 7 月 13 日（Pt） | 報告書 | （[!DNL Analytics for Advertising] を使用するDSP ユーザー）接続された TV （CTV）プレースメントのビュースルーコンバージョンが、Adobe Analyticsで利用可能なコンバージョンデータに含まれるようになりました。 | 「の概要 [ の「統合の使用例」の節を参照してくだ  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples) い。 |
| 2022 年 11 月 1 日（Pt） | ヘルプ | Advertising DSPとAdobe Analyticsの間でクリックスルーおよびビュースルーシグナルの共有を実装する方法、Adobe Target広告に [!DNL Target] して A/B テストアクティビティを設定する方法、およびDSP Analysis Workspaceを設定してテストデータを表示する方法に関する新しいドキュメントが用意されました。 | [Adobe TargetでのAdvertising DSP広告用 A/B テストの設定 ](/help/integrations/target/ab-tests-dsp.md) を参照してください。 |
| 2022 年 8 月 17 日（Pt） | ヘルプ | 新しい章では、Adobe AdvertisingとAdobe Audience Managerを統合するあらゆる方法について説明します。 | 「[Adobe Audience ManagerとAdobe Audience Managerの統合 ](/help/integrations/audience-manager/overview.md)」の概要を含め、「Adobe Advertisingとの統合」の章を参照してください。 |
| 2021 年 4 月 27 日（Pt） | [!DNL Analytics for Advertising] | [!DNL Analytics for Advertising] 広告タグに [!DNL Google Campaign Manager 360] マクロを追加して、クリックデータをAdobe Analyticsに送信する理由と方法を説明します。 | 「[ タグに追加  [!DNL Analytics for Advertising]  マクロ  [!DNL Google Campaign Manager 360]  を参照 ](/help/integrations/analytics/macros-google-campaign-manager.md)。 |
| 2021 年 4 月 19 日（Pt） | [!DNL Analytics for Advertising] | [!DNL Flashtalking] ad タグにマクロを追加してクリックデータをAdobe Analyticsに送信する理由と方法を説明します。 | 「[ タグに追加  [!DNL Analytics for Advertising]  マクロ  [!DNL Flashtalking]  を参照 ](/help/integrations/analytics/macros-flashtalking.md)。 |
| 2021 年 10 月 27 日（Pt） | [!DNL Analytics for Advertising] | 組織がデータ収集用に使用していた従来のAdobe Analytics `visitorAPI.js` ライブラリを [Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja) ライブラリ（`alloy.js`）に切り替える場合は、ID のステッチを有効にするためにいくつかの変更を加える必要があります。 | [Adobe Experience Platformでの  [!DNL Last Event Service] JavaScript Library の使用  [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md) を参照してください。 |
| 2021 年 5 月 26 日（Pt） | ヘルプ | 「[!DNL Analytics for Advertising]」の章に、「[!DNL Analytics Marketing Channels] での作業」に関するサブチャプターが含まれるようになりました。 | 参照：「[ マーケティングチャネルの基本 ](/help/integrations/analytics/marketing-channels/mc-overview.md)」、「[Adobe Advertising ID を使用した  [!DNL Analytics Marketing Channels]  処理ルールの作成 ](/help/integrations/analytics/marketing-channels/mc-ids.md)」、「[Adobe Advertising データの使用  [!DNL Analytics Marketing Channels]  使用 ](/help/integrations/analytics/marketing-channels/mc-ac-data.md)」および「[Adobe Advertisingと  [!DNL Analytics Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) の間でチャネルデータが変化する理由」 |
| 2021 年 5 月 26 日（Pt） | ヘルプ | [!DNL Analytics for Advertising] に関するすべてのビデオチュートリアルへのリンクを追加しました。 | 詳しくは、「[Adobe Advertising統合のビデオチュートリアル ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=ja)」を参照してください。 |

{style="table-layout:auto"}

<!-- At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
