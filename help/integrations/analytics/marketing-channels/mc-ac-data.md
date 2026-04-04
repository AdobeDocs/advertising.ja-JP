---
title: Adobe Advertising データで [!DNL Marketing Channels] を使用する
description: ' [!DNL Analytics Marketing Channels]でのAdobe Advertising データの使用方法について説明します。'
feature: Integration with Adobe Analytics
exl-id: 522c7f01-1138-477d-8018-36030caab55e
TQID: https://experienceleague.adobe.com/VQMlRz2xtbbr6Nns5EZOh9zUUKIifKy-DGN-9JateJs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 713
ht-degree: 0%

---

# Adobe Advertising データで[!DNL Analytics Marketing Channels]を使用する

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

Adobe Advertisingと[!DNL Analytics Marketing Channels]の両方のレポートを使用すると、デジタルメディアがサイトのアクティビティに与える影響に関する貴重なinsightを得ることができます。

<!-- from video: By using Marketing Channels with your Adobe Advertising data, you can get a more holistic view of how your advertising efforts are affecting site behavior. In particular, you can see the value of your view-through and click-through data, and how your advertising assists or is assisted by other channels. -->

次の図は、Adobe Advertisingと[!DNL Marketing Channels]が1人の訪問者のジャーニーを構成する個々の訪問をどのように追跡しているかを示しています。 [!DNL Analytics]のAdobe Advertising レポートは、AMO IDを使用してAdobe Advertisingを通じてトラフィックされた有料ディスプレイ広告、検索広告、ソーシャル広告、コマースチャネル広告に限定されます。 ただし、[!DNL Marketing Channels]は、[!DNL Marketing Channels]処理ルールで設定されたすべてのチャネルを追跡します。

![Adobe Advertisingと[!DNL Marketing Channels]が訪問者のジャーニーの個々の訪問を追跡する方法](/help/integrations/assets/a4adc-mc-sample-journey2.png)

初回訪問では、利用者はメールキャンペーンを通じてweb サイトにアクセスし、10回のページビューを実行したあと、サイトを離れました。 2回目の訪問では、ユーザーはディスプレイ広告を介してサイトに入り、10回のページビューを実行してから離れました。 3回目の訪問では、利用者は自然検索でサイトにアクセスし、5つのページビューを実行し、250 ドルのコンバージョンを実行しました。そして、左側には、 [!DNL Marketing Channels]とAdobe Advertisingのトラッキングの違いに注目してください。 このジャーニーでAdobe Advertisingが追跡するチャネルは[!UICONTROL Display]のみです。 Adobe Advertisingは、[!UICONTROL Display] チャネルの訪問を追跡し、その後のエンゲージメントデータ（ページビューなど）とコンバージョンをその広告の影響に関連付けます。 一方、[!DNL Marketing Channels]では、すべてのチャネルの全体像が表示されます。

AMO IDは訪問者のジャーニーを通じて保持されるので、AMO ID データを使用して、Adobe Advertisingが他のマーケティングチャネルにどのように影響するかを確認できます。 AMO ID [は、デフォルトで60日間保持されますが](/help/integrations/analytics/overview.md)、必要に応じて永続性を設定できます。

## Adobe Advertisingとマーケティングチャネルのデータを組み合わせてメディアパフォーマンスを分析する方法

[!DNL Analytics]内では、Adobe Advertisingに保持されている有料広告データと[!DNL Marketing Channels]の包括的な訪問データを組み合わせて、メディアのパフォーマンスをより詳細に分析することで、カスタマージャーニーをより効果的に影響させることができます。

次の分析では、Adobe Advertisingのデータを使用して、ディスプレイ広告がサイトコンバージョンに与える影響を示しています。 3つの列はすべて同じコンバージョン指標を使用していますが、各列で伝えられるストーリーは異なります。

* 列1は、訪問者のジャーニー全体で永続的なAMO ID データを示しています。 列1は、641件の「申し込み処理の開始」が、ビュースルーまたはクリックスルーイベントを通じて、Adobe Advertising広告にリンクされていることを示しています。 このビューでは、他の[!DNL Marketing Channels] アトリビューションは考慮されていません。

* ただし、[!DNL Marketing Channels] データセットでは、641 アプリケーションの開始は他のマーケティングチャネルに起因しています。 最後の2つの列は641 Applications Startsを取り、データを[!UICONTROL Display Click-Through]および[!UICONTROL Display View-Through] チャネルに制限し、ラストタッチアトリビューションモデルで発生するコンバージョンを示します。

![&#x200B; ディスプレイ広告がサイトコンバージョンに与える影響の例](/help/integrations/assets/a4adc-mc-display-impact.png)

この分析をさらに一歩進めることができます。 マーケティングチャネル別にAdobe Advertisingの行をさらに分割して、Adobe Advertising コンバージョンが641 Applications Startsに起因する場所を確認できます。 これらのコンバージョンのうち5つはラストタッチディスプレイのクリックスルーに起因するもので、19はラストタッチディスプレイのビュースルーに起因するものであることはすでにわかっています。 それでも617件の申し込みが他のマーケティングチャネルから始まっている。 最後のタッチチャネルのディメンションをAdvertising DSPの行の上にドラッグ&amp;ドロップすると、アプリケーションの開始の残りの部分のチャネルアトリビューションが表示され、表示チャネルのクロスチャネルの影響が表示されます。

![最後のタッチチャネルディメンションを追加する方法](/help/integrations/assets/a4adc-mc-display-impact-ltc.png)

これで、残りのアプリケーションの開始がどのように関連付けられているかを確認できます。 電子メールには、AMO IDが保持される357 ラストタッチアプリケーション開始のクレジットが割り当てられます。 Adobe Advertisingのディスプレイ広告が、あらゆるチャネルに与えた影響を明らかにすることができます。 データセットとアトリビューションモデルがひとつしかないため、この種類のinsightは利用できません。

![表示チャネルのクロスチャネルへの影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel.png)

「100%積み重ね」に設定したスタックグラフを使用して、トレンドデータを経時的に表示することで、分析をさらに向上させることができます。 このビジュアライゼーションにより、ディスプレイマーケティング施策の影響が最も大きいラストタッチマーケティングチャネルを容易に追跡できます。

![表示チャネルのクロスチャネルのトレンドの影響の例](/help/integrations/assets/a4adc-mc-display-impact-x-channel-trend.png)

>[!MORELIKETHIS]
>
>* [の基本 [!DNL Analytics Marketing Channels]](mc-overview.md)
>* [Adobe Advertising IDを使用して [!DNL Marketing Channels] 処理ルールを作成](mc-ids.md)
>* [Adobe Advertisingと [!DNL Marketing Channels]](mc-data-variances.md)でチャネルデータが異なる理由
>* [&#x200B; ビデオ： [!DNL Marketing Channels] をAdobe Advertising レポートに使用](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html?lang=ja)
>* [概要： [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
