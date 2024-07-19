---
title: Adobe Advertisingデ  [!DNL Marketing Channels]  タの使用
description: ' [!DNL Analytics Marketing Channels] でAdobe Advertisingデータを使用する方法を説明します。'
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
source-git-commit: 7e614ecb517515217d812926f61ca10437820efd
workflow-type: tm+mt
source-wordcount: '713'
ht-degree: 0%

---

# Adobe Advertisingデータでの [!DNL Analytics Marketing Channels] の使用

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

Adobe Advertisingレポートと [!DNL Analytics Marketing Channels] レポートの両方を使用すると、デジタルメディアがサイトアクティビティに与える影響に関する貴重なインサイトを得ることができます。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

次の図は、1 人の訪問者のジャーニーを構成する個々の訪問を、Adobe Advertisingと [!DNL Marketing Channels] でトラッキングする方法を示しています。 [!DNL Analytics] のAdobe Advertisingレポートは、AMO ID を使用して、Adobe Advertisingを通じてトラフィックに送信される、有料ディスプレイ、検索、ソーシャルおよびコマースチャネル広告のみに制限されます。 ただし、[!DNL Marketing Channels] では、[!DNL Marketing Channels] 処理ルールで設定されたすべてのチャネルが追跡されます。

![ 訪問者のジャーニーにおける個々の訪問のAdobe Advertisingとトラッ [!DNL Marketing Channels] ング方法 ](/help/integrations/assets/a4adc-mc-sample-journey2.png)

1 回目の訪問で、ユーザーはメールキャンペーンを通じて web サイトに入り、10 回のページビューを実行した後、左に移動しました。 2 回目の訪問では、ユーザーはディスプレイ広告を使用してサイトに入り、10 回のページビューを実行してから離れました。 3 回目の訪問では、ユーザーは自然検索でサイトに入り、5 つのページビューを実行、250 ドルのコンバージョンを実行、左側を実行しました。 [!DNL Marketing Channels] とAdobe Advertisingのトラッキングの違いに注意してください。 このジャーニーでAdobe Advertisingが追跡するチャネルは [!UICONTROL Display] のみです。 Adobe Advertisingは、[!UICONTROL Display] チャネルの訪問をトラッキングし、後続のエンゲージメントデータ（ページビューなど）とコンバージョンをその広告の影響に戻す属性にします。 [!DNL Marketing Channels] の一方で、は、すべてのチャネルの完全なビューを提供します。

AMO ID は訪問者のジャーニーを通じて永続的なので、AMO ID データを使用して、Adobe Advertisingが他のマーケティングチャネルに与える影響を確認できます。 AMO ID[ デフォルトでは 60 日間保持 ](/help/integrations/analytics/overview.md) ですが、必要に応じて永続性を設定できます。

## Adobe Advertisingとマーケティングチャネルデータを組み合わせてメディアのパフォーマンスを分析する方法

[!DNL Analytics] 内では、有料広告データを保持するAdobe Advertisingと [!DNL Marketing Channels] の包括的な訪問データを組み合わせて、メディアのパフォーマンスをより詳細に分析し、カスタマージャーニーにより良い影響を与えることができます。

次の分析では、Adobe Advertisingデータを使用して、ディスプレイ広告がサイトコンバージョンに与える影響のバージョンを示します。 3 つの列はすべて同じコンバージョン指標を使用しますが、各列は異なるストーリーを示します。

* 列 1 は、訪問者のジャーニー全体を通して持続する AMO ID データを調べます。 列 1 は、ある時点で 641 件の Applications Starts が、ビュースルーまたはクリックスルーのいずれかを介してAdobe Advertising広告とリンクされたことを示しています。 このビューでは、他の [!DNL Marketing Channels] アトリビューションを考慮しません。

* ただし、[!DNL Marketing Channels] データセットでは、641 件のアプリケーション開始は、他のマーケティングチャネルに関連付けられます。 最後の 2 つの列は、641 のアプリケーション開始を取り、データを [!UICONTROL Display Click-Through] チャネルと [!UICONTROL Display View-Through] チャネルに制限し、ラストタッチアトリビューションモデルで発生するコンバージョンを示しています。

![ 表示広告がサイトコンバージョンに与える影響の例 ](/help/integrations/assets/a4adc-mc-display-impact.png)

この分析をさらに 1 段階進めることができます。 マーケティングチャネルでAdobe Advertising行をさらに分類して、Adobe Advertisingコンバージョンが 641 件のアプリケーション開始に関連付けられている場所を確認できます。 これらのコンバージョンのうち 5 つはラストタッチディスプレイのクリックスルーに関連付けられ、19 はラストタッチディスプレイのビュースルーに関連付けられていることはすでに知っています。 この場合でも、他のマーケティングチャネルに関連付けられた 617 アプリケーション開始が残ります。 ラストタッチチャネル ディメンションをAdvertising DSP行項目の上にドラッグ&amp;ドロップすると、残りのアプリケーションスタートのチャネル属性が表示され、ディスプレイチャネルのクロスチャネル影響を確認できます。

![ ラストタッチチャネル ディメンションの追加方法 ](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

これで、残りのアプリケーション開始の属性がどのように設定されているかを確認できます。 メールには、AMO ID が保持される 357 のラストタッチアプリケーション開始のクレジットが付与されます。 このタイプの分析を使用すると、Adobe Advertisingのディスプレイ広告がすべてのチャネルに与えた影響を確認できます。 データセットとアトリビューションモデルが 1 つしかない場合、このタイプのインサイトは使用できません。

![ ディスプレイチャネルのクロスチャネル影響の例 ](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

スタックグラフを「100% 積み重ね」に設定して、経時的なトレンドデータを表示することで、分析をさらに改善できます。 このビジュアライゼーションにより、ディスプレイマーケティングキャンペーンの影響を大きく受けるラストタッチマーケティングチャネルを監視しやすくなります。

![ ディスプレイチャネルのクロスチャネル影響のトレンドの例 ](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [ の基本  [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertising ID を使用した処理ルール  [!DNL Marketing Channels]  作成 ](mc-ids.md)
>* [ チャネルデータがAdobe Advertisingによって異なる理由  [!DNL Marketing Channels]](mc-data-variances.md)
>* [ ビデオ：Adobe Advertisingレポート  [!DNL Marketing Channels]  使用 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ 概要  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
