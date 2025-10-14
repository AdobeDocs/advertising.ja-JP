---
title: チャネルデータがAdobe Advertisingによって異なる可能性がある理由  [!DNL Marketing Channels]
description: AMO ID でトラッキングされるチャネルデータが、 [!DNL Analytics Marketing Channels] でトラッキングされるチャネルデータと異なる可能性がある理由を説明します。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# チャネルデータがAdobe Advertisingと [!DNL Marketing Channels] 間で異なる可能性がある理由

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

Adobe Advertisingと [!DNL Marketing Channels] データセットの統合について知っているユーザーからのよくある質問は、「AMO ID と [!DNL Marketing Channels] の間のデータの相違の原因は何か」です。 また、場合によっては、「なぜデータが壊れているのですか？ レポート全体ですべての指標を一致させる必要があります。」 幸いにも、不一致はデータが「壊れている」ことを示すものではなく、不一致が予想され、望ましいことさえあります。 統合がこのように設計された理由を見てみましょう。

2 つのデータセットの主なユースケースは異なります。

* [!DNL Marketing Channels]:[!DNL Marketing Channels] の主なユースケースは、共通のアトリビューションモデルを使用して複数のチャネルのデータを比較することです。 アナリストは、[!UICONTROL Marketing Channel] ディメンションを使用して、チャネルの相互関係に関するインサイトを深めることができます。 このインサイトは、各チャネルへの投資方法に関するマクロレベルの決定に役立ち、各チャネルの訪問者が web サイトとどのようにやり取りするかについてのインサイトを導くことができます。

  そのため、[!DNL Analytics] [!UICONTROL Marketing Channel] ディメンションは、すべてのチャネルをキャプチャおよびトラックするように設定されています。 [!DNL Marketing Channels] た、Advertising DSPのビュースルーおよびクリックスルーを取り込むように設定でき、他のマーケティングチャネルとの関連で取り込むことができます。

* Adobe Advertising AMO ID:Adobe Advertising AMO ID データの主なユースケースは、[!DNL Adobe Sensei] を利用した高度な入札アルゴリズムを提供することです。 このアルゴリズムは、広告費用を最大化し、[!DNL DSP] キャンペーンまたは [!DNL Search, Social, & Commerce] ポートフォリオの目標を達成するために、毎日何千ものマイクロレベルの入札決定を自動的に行います。 アルゴリズムがキャンペーンに接続できるコンバージョンデータが多いほど、アルゴリズムはこれらの入札決定をしやすくなります。

  このデータを収集するために、[!DNL Analytics for Advertising] インテグレーションにより、Adobe Analyticsの AMO ID ディメンションにクリックスルーおよびビュースルーのトラッキングコードとして変換できる未加工の AMO ID が渡されます。このディメンションは、カスタム変数（eVar）または予約変数（rVar）として保存されます。 他のチャネルのクリックスルーは AMO ID ディメンションで設定されないので、AMO ID ディメンションはこれらの他のチャネルからのエントリを追跡できません。 その結果、AMO ID はエントリポイントを通じて持続 [!DNL Marketing Channels] ます。

Adobe Advertisingの追跡データと [!DNL Analytics] の追跡データの間で発生する可能性のあるデータの相違について詳しくは、「[&#x200B; とAdobe Advertisingの間で予期されるデータの相違  [!DNL Analytics]  を参照してください &#x200B;](../data-variances.md)。

>[!MORELIKETHIS]
>
>* [&#x200B; とAdobe Advertisingの間で予期されるデータ  [!DNL Analytics]  相違 &#x200B;](/help/integrations/analytics/data-variances.md)
>* [&#x200B; の基本  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertising ID を使用した処理ルール  [!DNL Marketing Channels]  作成 &#x200B;](mc-ids.md)
>* [Adobe Advertisingデ  [!DNL Analytics Marketing Channels]  タの使用 &#x200B;](mc-ac-data.md)
>* [&#x200B; ビデオ：Adobe Advertisingレポート  [!DNL Marketing Channels]  使用 &#x200B;](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=ja)
