---
title: トランザクション ID フィードを使用したコンバージョン追跡
description: コンバージョン追跡データにトランザクション ID フィードを使用する方法について説明します。
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
TQID: https://experienceleague.adobe.com/wGlR5tUF7ajbnQLUnW0c-U84BskLzr63Wet-e-x823M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 293
ht-degree: 0%

---

# トランザクション ID フィードを使用したコンバージョン追跡

広告主がオンラインとオフラインの両方のトランザクションを持っている場合、Adobe AdvertisingはAdobe Advertising コンバージョントラッキングピクセルを介してオンライントランザクションをトラッキングでき、広告主はトランザクション IDを使用してオフライントランザクションをトラッキングし、フィードを介して配信できます。

* オンライントランザクションの場合、Adobe Advertisingは、広告のクリック数とweb サイトでのトランザクション数を追跡します。

* 広告主は、オフラインコンバージョンを追跡し、トランザクションレベルのフィードファイルをAdobe Advertisingに送信する必要があります。

## 導入の概要

*代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. アカウントまたはキャンペーンのトラッキングオプション「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」を使用すると、アカウントまたはキャンペーンのキーワード（キーワードレベルのトラッキング用）または広告（広告レベルのトラッキング用）ごとに、宛先URLまたは最終的なURLを自動的に生成できます。

1. オンラインコンバージョンのAdobe Advertising コンバージョントラッキングを設定します。 このプロセスは、Adobe Advertising ピクセルベースのコンバージョントラッキングを使用する広告主の場合と同じです。 一意のトランザクション ID （`ev_transid=<transid>`）のパラメーターを含むコンバージョンタグを生成することが重要です。

1. 広告主は、各トランザクションのオフライン部分について、フィードファイルに含めるためにトランザクションのオンライン部分で使用したのと同じトランザクション IDを生成します。

1. 広告主は、[必要な変換データ &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)を含むファイルを、指定されたサーバーの場所にアップロードします。

1. テクニカルサービスは、アップロードされたファイル内のコンバージョンデータを解析し、そのデータをAdobe Advertisingにアップロードします。 続いて、Adobe Advertisingを利用して、個々のキーワード、広告、プレースメントに関するデータを追跡し、それぞれに対する売上予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータに対して検証し、[孤立トランザクション &#x200B;](/help/search-social-commerce/glossary.md#o-p)をチェックします。

>[!MORELIKETHIS]
>
>* [変換フィード ファイルの必要ファイル数](feed-file-requirements.md)
>* [&#x200B; トランザクション ID](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)を使用したデータフィードのデータ要件
