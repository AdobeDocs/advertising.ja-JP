---
title: 最新情報
description: Adobe AdvertisingとAdobe Experience Cloudのその他の製品およびサービスとの統合のアップデートについて説明します。
cloud: Experience Cloud
product: advertising cloud
index: true
exl-id: e5874077-d2a8-43bb-ad4e-55547442c8a4
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '831'
ht-degree: 0%

---

# 最新情報

以下の機能は新規または最近変更されました。

| 日付 | 機能 | 説明 | 詳細 |
| ---- | ------- | ----------- | -------------------- |
| 2025年9月8日（PT） | Customer Journey Analyticsとの連携 | （Beta機能）Customer Journey Analyticsを使用しているが[!DNL Analytics for Advertising]ではない広告主は、[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja)を使用して、Adobe AdvertisingとCustomer Journey Analytics間でデータをネイティブに交換できるようになりました。 | 「[Adobe AdvertisingとCustomer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md)の連携の概要」を参照してください。 |
| 2025年3月26日（PT） | [!DNL Adobe Analytics for Advertising] | （検索、ソーシャル、およびCommerceを使用する広告主、[!DNL Microsoft Advertising] アカウント、および[!DNL Adobe Analytics for Advertising]） [!UICONTROL Auto Upload] トラッキングオプションを使用するアカウントの場合、すべてのキャンペーンタイプのランディングページサフィックスのAMO ID パラメーターのフォーマットが、最新のフォーマットに更新されました。 以前は、ほとんどのアカウントのパフォーマンスの最大キャンペーンは新しい形式に移行されていました。<br><br>新しい形式に移行されていない[!UICONTROL Auto Upload]追跡オプションを持たないアカウントの場合、新しいAMO ID形式を含めるには、各ランディングページのサフィックスを手動で更新する必要があります。<br><br>現在の形式：`s_kwcid=AL!{userid}!10!{AdId}!!!!{OrderItemId}!!{CampaignId}!{AdGroupId}` | 「[概要 [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)」および[AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)を参照してください。」 |
| 2024年11月13日（PT） | [!DNL Analytics for Advertising] | （広告主が[!DNL Analytics for Advertising]とAdobe Customer Journey Analyticsを使用している場合）予約済み変数を使用してAMO IDとEF IDを取得する場合は、AMO IDとEF IDの予約済み変数をできるだけ早く標準[!DNL eVars]にコピーすることで、Adobe AdvertisingとAdobe Customer Journey Analyticsの間の今後の統合に備えることができます。 これにより、タスクを完了するとすぐにAMO IDとEF IDの履歴データの収集が可能になり、履歴データは今後の使用に利用できるようになります。 予約済み変数を使用しており、このタスクを完了する必要がある場合は、Adobe アカウントチームから通知されます。 | 「[Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集する](/help/integrations/analytics/rvars-to-evars.md)」を参照してください。 |
| 2024年10月29日（PT）リリース | [!DNL Adobe Analytics for Advertising] | （パフォーマンスの最大キャンペーンが[!DNL Adobe Analytics for Advertising]と[!DNL Microsoft Advertising]件の広告主）パフォーマンスの最大キャンペーンの新しいAMO ID （[!DNL s_kwcid]）パラメーターをパフォーマンスの最大キャンペーンのトラッキング URLに実装すると、Adobe Analyticsでパフォーマンスの最大キャンペーンのアセットグループレベルのデータが利用できるようになりました。このパラメーターには広告とキーワードは含まれていません。 パフォーマンス最大数キャンペーンを含むほとんどのアカウントのトラッキングは、既に新しい形式に移行されていました。 ただし、新しい形式に移行されていない[!UICONTROL Auto Upload] トラッキングオプションを持たないパフォーマンス最大キャンペーンを持つアカウントの場合は、新しいAMO ID形式を含めるように、各ランディングページサフィックスを手動で更新する必要があります。パフォーマンスの最大化キャンペーンの<br><br>Adobe Analytics データは、Search、Social、およびCommerceでも利用できます。 | 新しい[AMO ID形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)と[いつ、どのようにトラッキング URLにパラメーターを追加するかを参照してください](/help/integrations/analytics/ids.md)。 |
| 2023年12月16日（PT） | ヘルプ | 新しいドキュメントでは、Search, Social, &amp; Commerceの広告からのクリックスルーのトラフィックに対して[!DNL Target]でA/B テストを設定する方法と、[!DNL Analytics]でテストを測定して視覚化する方法に関するヒントについて説明します。 | 「[Search, Social, &amp; Commerce ads](/help/integrations/target/ab-tests-search.md)のAdobe TargetでのA/B テストの設定」を参照してください。 |
| 2023年8月8日（PT） | [!DNL Analytics for Advertising] | 標準、カスタム、予約済みのコンバージョン指標およびトラフィック指標を含む一部の[!DNL Analytics]成功イベント指標は、DSPおよびSearch、Social、およびCommerceで自動的に使用できます。 これで、既存の[!DNL Analytics] [!DNL eVars]および[!DNL props]に基づいて、独自の成功指標を設定できるようになりました。[!DNL eVar] レベルおよび[!DNL prop] レベルのデータをカスタム成功イベントにファネリングします。 | 「[Adobe Analytics [!DNL eVars] および [!DNL Props]](/help/integrations/analytics/conversion-metrics-from-evars.md)からコンバージョン指標を作成する」を参照してください。 |
| 2023年7月13日（PT） | レポート | （DSP ユーザーが[!DNL Analytics for Advertising]）コネクテッド TV （CTV）のプレースメントのビュースルーコンバージョンが、Adobe Analytics内で利用可能なコンバージョンデータに含まれるようになりました。 | 「[&#x200B; [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md#integration-examples)の概要」の「統合の使用例」の節を参照してください。 |
| 2022年11月1日（PT） | ヘルプ | 新しいドキュメントでは、Advertising DSPとAdobe Target間のクリックスルーおよびビュースルーシグナルの共有を実装する方法、DSP広告用に[!DNL Target]でA/B テストアクティビティを設定する方法、およびテストデータを表示するようにAdobe Analytics Analysis Workspaceを設定する方法について説明します。 | 「[Advertising DSP ads](/help/integrations/target/ab-tests-dsp.md)のAdobe TargetでのA/B テストの設定」を参照してください。 |
| 2022年8月17日（PT） | ヘルプ | 新しい章では、Adobe AdvertisingとAdobe Audience Managerの統合に関するあらゆる方法について説明します。 | 「[Adobe Audience ManagerとAdobe Audience Manager](/help/integrations/audience-manager/overview.md)」の概要を含む、「Adobe Advertisingとの統合」の章を参照してください。 |
| 2021年4月27日（PT） | [!DNL Analytics for Advertising] | [!DNL Analytics for Advertising]広告タグに[!DNL Google Campaign Manager 360] マクロを追加してクリックデータをAdobe Analyticsに送信する理由と方法について説明します。 | 「[追加 [!DNL Analytics for Advertising]  マクロを [!DNL Google Campaign Manager 360] 広告タグ &#x200B;](/help/integrations/analytics/macros-google-campaign-manager.md)に追加」を参照してください。 |
| 2021年4月19日（PT） | [!DNL Analytics for Advertising] | クリックデータをAdobe Analyticsに送信するために[!DNL Flashtalking]広告タグにマクロを追加する理由と方法について説明します。 | 「[追加 [!DNL Analytics for Advertising]  マクロを [!DNL Flashtalking] 広告タグ &#x200B;](/help/integrations/analytics/macros-flashtalking.md)に追加」を参照してください。 |
| 2021年10月27日（PT） | [!DNL Analytics for Advertising] | 組織が従来のAdobe Analytics `visitorAPI.js` ライブラリを使用してから、データ収集のために[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=ja) ライブラリ （`alloy.js`）に切り替える場合は、ID ステッチを有効にするために、いくつかの変更を行う必要があります。 | 「[Adobe Experience Platformでの [!DNL Last Event Service] JavaScript ライブラリの使用 [!DNL Web SDK]](/help/integrations/analytics/web-sdk.md)」を参照してください。 |
| 2021年5月26日（PT） | ヘルプ | 章「[!DNL Analytics for Advertising]」には、「Working in [!DNL Analytics Marketing Channels]」のサブチャプターが含まれるようになりました。 | 「[処理ルール  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-overview.md)," "[Using Adobe Advertising IDs to create [!DNL Marketing Channels] の基本](/help/integrations/analytics/marketing-channels/mc-ids.md)」、「[Adobe Advertising data [!DNL Analytics Marketing Channels] を使用する」および「](/help/integrations/analytics/marketing-channels/mc-ac-data.md)Adobe Advertisingと[の間でチャネルデータが異なる理由」を参照してください。 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md) |
| 2021年5月26日（PT） | ヘルプ | [!DNL Analytics for Advertising]に関するすべてのビデオチュートリアルへのリンクが追加されました。 | 「[Adobe Advertising統合に関するビデオチュートリアル &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/overview.html?lang=ja)」を参照してください。 |

{style="table-layout:auto"}

<!--
 At some point, just make this an overview page instead?

Adobe Advertising is integrated with the following Adobe Experience Cloud products:

* [Adobe Analytics](/help/integrations/analytics/overview.md)

* Adobe Audience Manager

* Adobe Campaign (Adobe Advertising Search only)

 -->
