---
title: EF ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータに EF ID フィードを使用する方法を説明します。
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '349'
ht-degree: 0%

---

# EF ID フィードを使用したコンバージョントラッキング

この手法では、Advertising Cloudは、ユーザーがクリックして広告を出し、ランディングページに到達するたびに `ef_id` 値を収集し、広告主はその `ef_id` 値をコンバージョンデータと共に蓄積し、データフィードに送る。

## 実装の概要

*エージェンシーアカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. アカウントまたはキャンペーンのトラッキングオプション「[!UICONTROL EF Redirect]」、リダイレクトタイプ「[!UICONTROL Token]」、「[!UICONTROL Auto Upload]」を使用して、アカウントまたはキャンペーンの各キーワード （キーワードレベルのトラッキングの場合）または広告（Adobe Advertisingレベルのトラッキングの場合）の広告トークン （ef_id）を含む宛先 URL または最終 URL を自動生成します。

   >[!NOTE]
   >* この手法では、広告主がAdobe Advertisingのコンバージョントラッキングタグを使用する必要はありません。
   >* 既存のアカウントまたはキャンペーンのリダイレクトタイプを [!UICONTROL Standard] から [!UICONTROL Token] に、またはその逆に切り替える場合は、適用可能なすべてのトラッキング URL を再生成する必要があります。

   ef_id は、エンドユーザーが広告をクリックしてAdobe Advertisingサーバーにリダイレクトされたときに、入力され、ランディングページの URL に追加されます。 その後、ef_id が宛先 URL の広告主に渡されるか、広告またはキーワードの最終的な URL に渡されます。 次に、リダイレクト中に広告主に渡される宛先 URL の例を示します。

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 広告主は、リダイレクトから ef_id を抽出し、それを関連する変換データと共にフィードファイルに格納する。 ef_id を変更したり、大文字と小文字を変更したりしないでください。

1. （オプションですが推奨）広告主は、フィードファイルに含めるトランザクションごとに一意のトランザクション ID を作成できます。

1. 広告主は、指定されたサーバーの場所に [&#x200B; 必要な変換データ &#x200B;](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) を含むファイルをアップロードします。

1. テクニカルサポートは、アップロードされたファイルのコンバージョンデータを解析して、Adobe Advertisingにアップロードします。 次に、Adobe Advertisingは、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、[&#x200B; 孤立トランザクション &#x200B;](/help/search-social-commerce/glossary.md#o-p) の有無を確認します。

>[!MORELIKETHIS]
>
>* [&#x200B; 変換フィードファイルのファイル要件 &#x200B;](feed-file-requirements.md)
>* [EF ID を使用したデータフィードのデータ要件 &#x200B;](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
