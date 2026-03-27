---
title: ' [!DNL Marketing Channels]の基本'
description: ' [!DNL Analytics Marketing Channels]  ユーザーが理解する必要がある [!DNL Analytics for Advertising] に関する重要な情報を学習します。'
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 81943936f828fa9472cff1b5b1c09e473396b818
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels]の基本

このページでは、[!DNL Analytics Marketing Channels] ユーザーが理解する必要がある[!DNL Analytics for Advertising]に関する重要な情報について説明します。

[!DNL Marketing Channels]に関する完全なドキュメントについては、「[&#x200B; [!DNL Marketing Channels]](https://experienceleague.adobe.com/ja/docs/analytics/components/marketing-channels/c-getting-started-mchannel)の基本を学ぶ」を参照してください。

## [!DNL Marketing Channels]の概要

[!DNL Marketing Channels]はAdobe Analyticsの主な機能です。 [!DNL Marketing Channels]件のレポートでは、レポート期間に顧客がweb サイトに到達した方法と、各チャネルが収益またはサイト上の行動にどのような影響を与えたかを示します。

相互訪問ジャーニーの例を考えてみましょう。 web サイトへの各訪問は、訪問者が入力したマーケティングチャネルで示されます。 初回訪問は、ファーストタッチチャネルとも呼ばれ、メールです。 訪問2のディスプレイは参加チャネルであり、自然検索はラストタッチチャネルと見なされます。 [!UICONTROL Last Touch Attribution]内で[!UICONTROL Attribution IQ]を使用する場合、自然検索は$250 コンバージョンイベントに対する完全なクレジットを受け取ります。 Experience Cloud ID サービスを使用すると、これらの個々の訪問を結び付けて、1人の訪問者が1つのジャーニーを表示できます。

![&#x200B; マーケティングチャネルでのクロスビジットのコンバージョンジャーニーの例](/help/integrations/assets/a4adc-mc-sample-journey.png)

[!UICONTROL Marketing Channels]処理ルールを使用して、トラフィックを促進するチャネルを決定する一連のロジックを作成し、ユーザーがサイトにアクセスする際に各チャネルを追跡できます。 例えば、[!UICONTROL Email] チャネルは、クリック時に生成された一意のトラッキングコードで示されます。このトラッキングコードは、Adobe Analyticsによって記録された場合、訪問をメールマーケティングキャンペーンから発生したものとして分類します。

## 処理ルールとマーケティングチャネルの設定方法

オーディエンスがweb サイトにアクセスするたびに、クリックするか、アドレスバーに直接入力したURLを通じてアクセスします。 ユーザーがweb サイトにアクセスすると、[!DNL Analytics]は、訪問を促したチャネルの決定に使用できる情報を追跡します。

多くのマーケターは、チャネル URLにクエリ文字列パラメーターのトラッキングコードを追加して、サイトへのチャネルの影響を追跡できます。 特定のトラッキングパラメーターと値をリッスンするように[!DNL Marketing Channels]処理ルールを設定して、追加のトラッキングなしでチャネルを決定できます。 例えば、すべてのメールキャンペーン URLが形式`www.adobe.com?cid=email…` （URLにクエリ文字列パラメーターと値`cid=email`が含まれる）に従っている場合、このトラッキングコードをリッスンし、[!UICONTROL Email] チャネルで訪問をバケット化するルールを作成できます。

他のチャネルでは追跡可能なURL パスがなく、識別のためにさらなるロジックが必要です。 例えば、ユーザーがソーシャルネットワーク上で別のユーザーが有機的に共有したリンクをクリックする[!UICONTROL Earned Social]は、追跡すべき重要なチャネルです。 ただし、マーケターは、共有されたURLにクエリ文字列パラメーター追跡コードを追加する方法はありません。 この場合、興味のあるソーシャルネットワークの参照ドメインと、有料トラッキングコードがないことをリッスンしてチャネルを決定するための処理ルールを作成できます。 これらの要件を満たした訪問は、マーケティングチャネルレポート内でアーンドソーシャルとして追跡されます。

Adobeでは、[!DNL Analytics] チームと協力して、関連するすべてのチャネルを追跡する包括的な[!DNL Marketing Channels]処理ルールのセットを構築することをお勧めします。 これにより、強力なアトリビューションレポートを作成できます。

Adobe Advertisingがカスタムマーケティングチャネルの作成に必要なシグナルにどのように役立つのか、「[Adobe Advertising IDを使用した処理ルール  [!DNL Marketing Channels] の作成](mc-ids.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe Advertising IDを使用して [!DNL Marketing Channels] 処理ルールを作成](mc-ids.md)
>* [Adobe Advertisingと [!DNL Marketing Channels]](mc-data-variances.md)でチャネルデータが異なる理由
>* [Adobe Advertising data [!DNL Analytics Marketing Channels] での](mc-ac-data.md)の使用
>* [&#x200B; ビデオ： [!DNL Marketing Channels] をAdobe Advertising レポートに使用](https://experienceleague.adobe.com/ja/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc)
>* [概要： [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
