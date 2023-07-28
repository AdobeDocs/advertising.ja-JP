---
title: トランザクション ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータでのトランザクション ID フィードの使用について説明します。
exl-id: 58f231a6-970b-46b4-824b-67b3d3f83051
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# トランザクション ID フィードを使用したコンバージョントラッキング

Adobe Advertising主がオンラインとオフラインの両方のトランザクションを持っている場合、広告主はAdobe Advertisingのコンバージョントラッキングピクセルを使用してオンライントランザクションを追跡し、広告主はトランザクション ID を使用してオフライントランザクションを追跡してフィードを介して配信できます。

* オンライントランザクションの場合、Adobe Advertisingは広告のクリック数と Web サイトでの結果のトランザクション数を追跡します。

* 広告主は、オフラインのコンバージョンを追跡し、トランザクションレベルのフィードファイルをAdobe Advertisingに送信する必要があります。

## 実装の概要

*代理店のアカウントマネージャー [!DNL Adobe] アカウントマネージャー、管理者ユーザーロールのみ*

1. アカウントまたはキャンペーントラッキングオプションを使用する」[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]」をクリックします。

1. オンラインコンバージョンのAdobe Advertisingコンバージョントラッキングを設定します。 このプロセスは、ピクセルベースのコンバージョントラッキングをAdobe Advertisingする広告主の場合と同じです。 一意のトランザクション ID(`ev_transid=<transid>`) をクリックします。

1. 広告主は、各トランザクションのオフライン部分に対して、フィードファイルに含めるトランザクションのオンライン部分で使用されたのと同じトランザクション ID を生成します。

1. 広告主が、 [必要なコンバージョンデータ](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) を指定したサーバーの場所に追加します。

1. テクニカルサービスは、アップロードされたファイルの変換データを解析し、そのデータをAdobe Advertisingにアップロードします。 Adobe Advertisingは、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [コンバージョンフィードファイルのファイル要件](feed-file-requirements.md)
>* [トランザクション ID を使用するデータフィードのデータ要件](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
