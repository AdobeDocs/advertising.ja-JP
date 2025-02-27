---
title: 用語集
description: 主要用語の定義を参照してください。
feature: Creative Introduction
source-git-commit: 4e61ce32862411a7a83c66773e41d032770ad861
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 0%

---

# 用語集 {#glossary}

*クローズドベータ版*

<!-- more feature metadata?? -->

<!-- ## A-B {#a-b} -->

<!-- not sure I need these "x-through" terms since that we're not creating conversion pixels in this UI, but see if they come up in other text -->

**クリックスルー：** コンバージョンにつながる広告クリック。

**data pass target:** データパスターゲットを使用すると、DSP、パブリッシャー、パートナーからリアルタイムに提供されたデータに基づいて、広告要素を選択できます。 これには、サードパーティのデータが含まれる場合があります。

<!-- verify this -->広告エクスペリエンスでは、各データパスターゲットには最大 5 つのキーと値のペアを含めることができます。そのレベルの最初のターゲットノードで、キーと少なくとも 1 つの値を指定します。同じキーを兄弟ターゲットノードでも使用できます。 各キーと値のペアは、このエクスペリエンスの広告タグにマクロとして追加されます。 広告インプレッションの時点で、値をそのインプレッションに固有のデータに置き換える責任は、DSP、パブリッシャーまたはパートナーにあります。 情報は [!DNL Creative] に返されるので、エクスペリエンスで定義されたルールに基づいて適切な広告エクスペリエンスを表示できます。

例えば、女性でセグメント 1234 を閲覧者とする 1 人以上の可能性のあるクリエイティブをターゲットにするには、ターゲットノードのデータパスターゲット `gender=female` と `segment=1234` を設定します。 インプレッションを提供するDSPがタグに性別とセグメント情報を入力し、指定された要件を満たす訪問者は、関連するクリエイティブの 1 つに表示されます。

**エンゲージメントスルー：** コンバージョンにつながる広告エンゲージメント（カルーセル広告のスクロールや広告の展開など）。 このタイプのイベントは、ランディングページやランディングページ上のイベントに到達するための広告のクリックとは別のものです。

<!-- or flexible html5 creative variation? Not sure we need to mention this since there's no place to view the different variations per se:

**variation of a flexible HTML5 creative:** A derivation of a flexible HTML5 creative asset in your [!UICONTROL Creative Libraries], which is generated when you assign the creative to an experience and change any of the default attributes within the experience.
-->

**ビュースルー：** 広告インプレッション、またはインプレッションの文字列。ユーザーが広告をクリックしなくてもコンバージョンが発生します。
