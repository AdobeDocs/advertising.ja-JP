---
title: 用語集
description: 主要用語の定義を参照してください。
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '286'
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

**エンゲージメントスルー：** コンバージョンにつながる広告エンゲージメント（ビデオの視聴や広告の展開など）。

<!-- or flexible html5 creative variation? -->
**フレキシブルHTML5 クリエイティブのバリエーション：** コンテン [!UICONTROL Creative Libraries] 内のフレキシブルHTML5 クリエイティブアセットの派生。クリエイティブをエクスペリエンスに割り当て、エクスペリエンス内のデフォルト属性を変更した場合に生成されます。

<!-- Not sure if this will be implemented, and how:
You can view all derived creatives, including not only the base creatives you've added but also each child creative derivation, in the card view in [!UICONTROL Creative] > [!UICONTROL Libraries]. In the toolbar, click __?__ , and then select Derived Creatives. [Clarify how to tell which have variations. I can't find any now.]
-->

**ビュースルー：** 広告インプレッション、またはインプレッションの文字列。ユーザーが広告をクリックしなくてもコンバージョンが発生します。
