---
title: Web ページのコンバージョントラッキングの設定
description: 広告インプレッションおよびAdobeクリックによるコンバージョンを追跡するために、広告広告を有効にする方法を説明します。
source-git-commit: cd8367fbae2234cfdb937c5da8f21f94a615e92a
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# Web ページのコンバージョントラッキングの設定

<!-- I don't think this is necessary here -- we already have a bullet point in the implementation overview -- so removing from TOC. -->

コンバージョンデータに関するレポートを生成する前に、Adobe広告には、キーワードと広告ごとに、インプレッション、クリック、コスト、コンバージョン（トランザクション）の各データが必要です。 Adobe広告はまた、このデータを使用して、キャンペーンの予算やキーワードおよび広告の入札を最適化するために必要なデータ予測モデルを構築します。

Adobe広告で広告インプレッション数およびクリック数によるコンバージョンを追跡できるようにするには、次の手順を実行する必要があります。

* Search、Social、&amp;Commerce が管理する各広告キャンペーンのキーワード、広告、配置、サイトリンク、製品グループのトラッキングテンプレートまたはリンク先 URL に、一意のクリックトラッキングコード（およびエンドユーザーをトラッキングサーバーにリダイレクトする追加コード）を含めます。 これにより、Adobe広告は、各広告インプレッション（ディスプレイ広告およびソーシャル広告のみ）と、広告の各クリックを追跡できます。

* コンバージョンデータを追跡するには、次のいずれかの方法を使用します。

   * **Adobe広告で追跡されたコンバージョン：** 広告主は、各コンバージョンページにAdobe広告のコンバージョントラッキングタグを挿入します。

   * **Adobe Analyticsコンバージョン：** 広告主は、すべてのコンバージョンにAdobe Analyticsトラッキングを使用します。

   * **[!DNL Google Analytics]コンバージョン：** 広告主が [!DNL Google Analytics] タグで、すべてのコンバージョンを追跡できます。

   * **広告主がトラッキングしたコンバージョン：** 広告主は、オンラインとオフラインのコンバージョンデータを任意に組み合わせて、日別フィードファイルを提供します。

トラッキングの実装について詳しくは、「トラッキング」に関するヘルプの章を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe広告コンバージョンタグの生成](/help/search-social-commerce/tools/conversion-tag-generate.md)
>* [トラッキング URL ツールを使用して、検索、ソーシャル、およびコマースのクリックトラッキング URL を生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [検索、ソーシャル、コマースのクリック追跡 URL のデコード](/help/search-social-commerce/tools/click-tracking-url-decode.md)

