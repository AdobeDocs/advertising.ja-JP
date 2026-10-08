---
title: Adobe Advertisingと[!DNL Marketing Channels]でチャネルデータが異なる理由
description: AMO IDによって追跡されるチャネルデータが、[!DNL Analytics Marketing Channels]によって追跡されるチャネルデータと異なる理由を説明します。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
TQID: 'https://experienceleague.adobe.com/zzYKrbiwvW9Ysf7baDfKGsETmSvYbXDY7-lIygorXH8'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: f2860a4b-f905-4545-bead-1bbc92564592
    internal-label: Advertising integrations
subfeature_v2:
  - id: cfd751d4-ee56-4323-8fd1-dc174b031709
    internal-label: Analytics integration
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: dba482e5-29a8-4127-afa2-c4b913512ef8
    internal-label: Data and analytics
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%
---
# Adobe Advertisingと[!DNL Marketing Channels]でチャネルデータが異なる理由

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

Adobe Advertisingと[!DNL Marketing Channels] データセットの統合について学ぶユーザーからの一般的な質問は、「AMO IDと[!DNL Marketing Channels]の間のデータの相違の原因は何ですか？」です。 または、時々、「なぜデータが壊れているのですか？ レポート間で一致させるすべての指標が必要です。」 幸いなことに、不一致はデータが「壊れている」ことを示すものではなく、不一致は期待されており、望まれていることもあります。 統合がこのように設計された理由を見てみましょう。

2つのデータセットには、主に異なるユースケースがあります。

* [!DNL Marketing Channels]: [!DNL Marketing Channels]の主な使用例は、共通のアトリビューションモデルを使用して複数のチャネルのデータを比較することです。 アナリストは、[!UICONTROL Marketing Channel] ディメンションを使用して、チャネル同士がどのように相互作用しているかについてのインサイトを増やすことができます。 このinsightは、各チャネルへの投資方法に関するマクロレベルの意思決定を促進し、各チャネルの訪問者がweb サイトとどのようにやり取りしているのかを把握するのに役立ちます。

  したがって、[!DNL Analytics] [!UICONTROL Marketing Channel] ディメンションは、すべてのチャネルをキャプチャして追跡するように設定されています。 [!DNL Marketing Channels]は、Advertising DSPのビュースルーとクリックスルーをキャプチャするように設定することもでき、他のマーケティングチャネルに対しても設定できます。

* Adobe Advertising AMO ID: Adobe Advertising AMO ID データの主な使用例は、高度な[!DNL Adobe AI]を活用した入札アルゴリズムをフィードすることです。 アルゴリズムは、広告費を最大化し、[!DNL DSP] キャンペーンまたは[!DNL Search, Social, & Commerce] ポートフォリオの目標を達成するために、毎日数千のマイクロレベル入札決定を自動的に行います。 アルゴリズムがキャンペーンを接続できるコンバージョンデータが多ければ多いほど、アルゴリズムはこれらの入札に関する意思決定をより的確におこなうことができます。

  このデータを収集するために、[!DNL Analytics for Advertising]統合は、Adobe AnalyticsのAMO ID ディメンションでクリックスルートラッキングコードおよびビュースルートラッキングコードとして変換できる生のAMO IDを渡します。このコードは、カスタム変数（eVar）または予約変数（rVar）として保存されます。 他のチャネルのクリックスルーはAMO ID ディメンションで設定されないため、AMO ID ディメンションでは、これらの他のチャネルからのエントリを追跡できません。 その結果、AMO IDは[!DNL Marketing Channels]個のエントリポイントを通じて保持されます。

Adobe Advertisingで追跡されたデータと[!DNL Analytics]で追跡されたデータとの間で考えられるデータの相違について詳しくは、「[Adobe Advertisingと [!DNL Analytics] の間の予想されるデータの相違」を参照してください。](../data-variances.md)

>[!MORELIKETHIS]
>
>* [&#x200B; [!DNL Analytics] とAdobe Advertising](/help/integrations/analytics/data-variances.md)の間の予期されるデータの差異
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertising IDを使用して [!DNL Marketing Channels] 処理ルールを作成](mc-ids.md)
>* [Adobe Advertising data](mc-ac-data.md)での [!DNL Analytics Marketing Channels] の使用
>* [&#x200B; ビデオ： [!DNL Marketing Channels] をAdobe Advertising レポートに使用](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
