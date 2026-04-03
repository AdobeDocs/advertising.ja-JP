---
title: EF ID フィードを使用したコンバージョンの追跡
description: コンバージョン トラッキング データにEF ID フィードを使用する方法について説明します。
exl-id: fd065313-3d27-4bb9-a934-e815e02cf405
feature: Search Tracking
TQID: https://experienceleague.adobe.com/D4OpKvTL-jjIOgMaakH78aYA7q9p2BXcc2P-RI8blfY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 349
ht-degree: 0%

---

# EF ID フィードを使用したコンバージョンの追跡

この方法では、ユーザーがクリックして広告をクリックし、ランディングページに到着するたびに`ef_id`値がAdvertising Cloudによって収集され、広告主は`ef_id`値をコンバージョンデータと共に保存し、データフィードに送信します。

## 導入の概要

*代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. アカウントまたはキャンペーンのトラッキングオプション「[!UICONTROL EF Redirect]」、「[!UICONTROL Token]」、「[!UICONTROL Auto Upload]」のリダイレクトタイプを使用すると、アカウントまたはキャンペーンのキーワード（キーワードレベルのトラッキング用）または広告（広告レベルのトラッキング用）ごとに、Adobe Advertising トークン（ef_id）を含む宛先URLまたは最終URLを自動的に生成できます。

   >[!NOTE]
   >* この方法では、広告主がAdobe Advertisingのコンバージョントラッキングタグを使用する必要はありません。
   >* 既存のアカウントまたはキャンペーンのリダイレクトタイプを[!UICONTROL Standard]から[!UICONTROL Token]に切り替える場合、またはその逆に切り替える場合は、該当するすべてのトラッキング URLを再生成する必要があります。

   ef_idは、エンドユーザーが広告をクリックし、Adobe Advertising サーバーにリダイレクトされると、ランディングページ URLに入力され、追加されます。 その後、ef_idは、広告またはキーワードの宛先URLまたは最終的なURLで広告主に渡されます。 次に、リダイレクト中に広告主に渡される宛先URLの例を示します。

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 広告主は、リダイレクトからef_idを抽出し、関連する変換データと共にフィードファイルに含めるように格納します。 ef_idを変更したり、大文字と小文字を変更しないでください。

1. （オプションですが推奨）広告主は、フィードファイルに含めるトランザクションごとに一意のトランザクション IDを作成できます。

1. 広告主は、[必要な変換データ ](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)を含むファイルを、指定されたサーバーの場所にアップロードします。

1. テクニカルサービスは、アップロードされたファイル内のコンバージョンデータを解析し、そのデータをAdobe Advertisingにアップロードします。 続いて、Adobe Advertisingを利用して、個々のキーワード、広告、プレースメントに関するデータを追跡し、それぞれに対する売上予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータに対して検証し、[孤立トランザクション ](/help/search-social-commerce/glossary.md#o-p)をチェックします。

>[!MORELIKETHIS]
>
>* [変換フィード ファイルの必要ファイル数](feed-file-requirements.md)
>* [EF IDを使用したデータフィードのデータ要件](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)
