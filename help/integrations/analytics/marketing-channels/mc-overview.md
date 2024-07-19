---
title: の基本  [!DNL Marketing Channels]
description: ユーザーが理解する必要  [!DNL Analytics Marketing Channels]  ある主  [!DNL Analytics for Advertising]  情報を説明します。
feature: Integration with Adobe Analytics
exl-id: de02dff5-86ce-41e8-89c6-3c11f6375b77
source-git-commit: 29b49e8fa54580d7cdd62f9a10fd2616def4694b
workflow-type: tm+mt
source-wordcount: '548'
ht-degree: 0%

---

# [!DNL Analytics Marketing Channels] の基本

このページでは、ユーザーが理解する必要のある [!DNL Analytics Marketing Channels] に関 [!DNL Analytics for Advertising] る主な情報を説明します。

[!DNL Marketing Channels] の完全なドキュメントについては、「[ 基本を学ぶ  [!DNL Marketing Channels]](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/c-getting-started-mchannel.html) を参照してください。

## [!DNL Marketing Channels] の概要

[!DNL Marketing Channels] は、Adobe Analyticsの主な機能です。 レポート [!DNL Marketing Channels]、レポートウィンドウを通じて顧客が web サイトに到達する方法と、各チャネルが売上高やオンサイト行動にどのように影響するかを示します。

次のクロス訪問ジャーニーの例について考えてみます。 Web サイトへの各訪問は、訪問者がエントリしたマーケティングチャネルで示されます。 最初の訪問はメールで、ファーストタッチチャネルとも呼ばれます。 訪問 2 の表示は参加チャネルであり、自然検索はラストタッチチャネルと見なされます。 [!UICONTROL Attribution IQ] 内で [!UICONTROL Last Touch Attribution] を使用すると、Natural Search は$250 のコンバージョンイベントに対してフルクレジットを受け取ります。 Experience CloudID サービスを使用すると、これらの個々の訪問を結び付けて、1 人の訪問者による 1 つのジャーニーを表示できます。

![ マーケティングチャネルでのクロス訪問コンバージョンジャーニーの例 ](/help/integrations/assets/a4adc-mc-sample-journey.png)

処理ルール [!UICONTROL Marketing Channels] 使用すると、一連のロジックを作成して、トラフィックを推進するチャネルを決定し、ユーザーがサイトにアクセスするたびに各チャネルを追跡できます。 例えば、[!UICONTROL Email] チャネルは、クリック時に生成される一意のトラッキングコードで示され、Adobe Analyticsがログに記録される際に、訪問がメールマーケティングキャンペーンからの訪問として分類されます。

## 処理ルールとマーケティングチャネルの設定方法

ユーザーは、web サイトにアクセスするたびに、URL をクリックするか、アドレスバーに直接入力します。 ユーザーが web サイトに入ると、[!DNL Analytics] は、訪問の原因となったチャネルを特定するために使用できる情報を追跡します。

多くの場合、マーケターは、チャネルの URL にクエリ文字列パラメーターのトラッキングコードを付加して、サイトに対するチャネルの影響を追跡します。 特定 [!DNL Marketing Channels] トラッキングパラメーターおよび値をリッスンするように処理ルールを設定することにより、追加のトラッキングを行わずにチャネルを決定することができます。 例えば、すべてのメールキャンペーン URL が `www.adobe.com?cid=email…` 形式（URL にはクエリ文字列パラメーターと値 `cid=email` が含まれる）に従う場合、このトラッキングコードをリッスンし、[!UICONTROL Email] チャネルに訪問をバケット化するルールを作成できます。

その他のチャネルには追跡可能な URL パスがなく、識別のためにさらにロジックが必要な場合。 例えば、ユーザーがソーシャルネットワーク上で有機的に共有されているリンクをクリックした [!UICONTROL Earned Social] は、追跡する重要なチャネルです。 ただし、マーケターが、共有される URL にクエリ文字列パラメーターのトラッキングコードを追加する方法はありません。 この場合、対象となるソーシャルネットワークの参照ドメインと、チャネルを決定する有料のトラッキングコードがないかどうかをリッスンする処理ルールを作成できます。 これらの要件を満たす訪問は、マーケティングチャネルレポート内で獲得したソーシャルとして追跡されます。

Adobeでは、分析チームと協力して、ビジネスに関連するすべてのチャネルをトラッキングするための包括的な [!DNL Marketing Channels] 処理ルールのセットを作成することをお勧めします。 これにより、強力なアトリビューションレポートを作成できます。

カスタムマーケティングチャネルの作成に必要なシグナルにAdobe Advertisingがどのように関与するかを理解するには、「[Advertising ID を使用した  [!DNL Marketing Channels]  ルールの作成 ](mc-ids.md) を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe Advertising ID を使用した処理ルール  [!DNL Marketing Channels]  作成 ](mc-ids.md)
>* [ チャネルデータがAdobe Advertisingによって異なる理由  [!DNL Marketing Channels]](mc-data-variances.md)
>* [Adobe Advertisingデ  [!DNL Analytics Marketing Channels]  タの使用 ](mc-ac-data.md)
>* [ ビデオ：Adobe Advertisingレポート  [!DNL Marketing Channels]  使用 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/analytics/analytics-reporting-a4adc.html)
>* [ 概要  [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)
