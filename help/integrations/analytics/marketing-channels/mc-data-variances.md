---
title: Adobe Advertisingと  [!DNL Marketing Channels] の間でチャネルデータが変化する理由
description: AMO ID でトラッキングされるチャネルデータが、 [!DNL Analytics Marketing Channels] でトラッキングされるチャネルデータと異なる可能性がある理由を説明します。
feature: Integration with Adobe Analytics
exl-id: 72e3aa1e-85ed-485a-b93f-5e67dd0140ce
source-git-commit: de2a2a097802cc4a7b5ac63bee2eb326895e70f1
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# チャネルデータがAdobe Advertisingと [!DNL Marketing Channels] で異なる可能性がある理由

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

Adobe Advertisingと [!DNL Marketing Channels] データセットの統合について知っているユーザーからのよくある質問は、「AMO ID と [!DNL Marketing Channels] の間のデータの相違の原因は何か」です。 また、場合によっては、「なぜデータが壊れているのですか？ レポート全体ですべての指標を一致させる必要があります。」 幸いにも、不一致はデータが「壊れている」ことを示すものではなく、不一致が予想され、望ましいことさえあります。 統合がこのように設計された理由を見てみましょう。

2 つのデータセットの主なユースケースは異なります。

* [!DNL Marketing Channels]:[!DNL Marketing Channels] の主なユースケースは、共通のアトリビューションモデルを使用して複数のチャネルのデータを比較することです。 アナリストは、[!UICONTROL Marketing Channel] ディメンションを使用して、チャネルの相互関係に関するインサイトを深めることができます。 このinsightは、各チャネルへの投資方法に関するマクロレベルの決定に役立ち、各チャネルの訪問者が web サイトとどのようにやり取りするかについてのインサイトを導くことができます。

  そのため、[!DNL Analytics] [!UICONTROL Marketing Channel] ディメンションは、すべてのチャネルをキャプチャおよびトラックするように設定されています。 [!DNL Marketing Channels] た、Advertising DSPのビュースルーおよびクリックスルーを取り込むように設定でき、他のマーケティングチャネルとの関連で取り込むことができます。

* Adobe Advertising AMO ID: Adobe Advertising AMO ID データの主なユースケースは、[!DNL Adobe AI] を利用した高度な入札アルゴリズムを提供することです。 このアルゴリズムは、広告費用を最大化し、[!DNL DSP] キャンペーンまたは [!DNL Search, Social, & Commerce] ポートフォリオの目標を達成するために、毎日何千ものマイクロレベルの入札決定を自動的に行います。 アルゴリズムがキャンペーンに接続できるコンバージョンデータが多いほど、アルゴリズムはこれらの入札決定をしやすくなります。

  このデータを収集するために、[!DNL Analytics for Advertising] インテグレーションにより、Adobe Analyticsの AMO ID ディメンションにクリックスルーおよびビュースルートラッキングコードとして変換できる未加工の AMO ID が渡されます。このディメンションは、カスタム変数（eVar）または予約変数（rVar）として保存されます。 他のチャネルのクリックスルーは AMO ID ディメンションで設定されないので、AMO ID ディメンションはこれらの他のチャネルからのエントリを追跡できません。 その結果、AMO ID はエントリポイントを通じて持続 [!DNL Marketing Channels] ます。

Adobe Advertisingで追跡されたデータと [!DNL Analytics] で追跡されたデータの間で発生する可能性のあるデータの相違について詳しくは、「[ とAdobe Advertisingの間で予期されるデータの相違  [!DNL Analytics]  を参照してください ](../data-variances.md)。

>[!MORELIKETHIS]
>
>* [ とAdobe Advertisingの間で予想されるデ  [!DNL Analytics]  タの相違 ](/help/integrations/analytics/data-variances.md)
>* [ の基本  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertising ID を使用した処理ルール  [!DNL Marketing Channels]  作成 ](mc-ids.md)
>* [Adobe Advertising Data [!DNL Analytics Marketing Channels]  使用 ](mc-ac-data.md)
>* [ ビデオ：Adobe Advertising レポート  [!DNL Marketing Channels]  使用 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
