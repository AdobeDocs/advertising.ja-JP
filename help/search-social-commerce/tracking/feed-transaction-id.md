---
title: トランザクション ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータにトランザクション ID フィードを使用する方法を説明します。
exl-id: 3341ac20-d435-4387-99da-7b874e53c2e7
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# トランザクション ID フィードを使用したコンバージョントラッキング

広告主がオンライン取引とオフライン取引の両方を保有している場合、Adobe AdvertisingはAdobe Advertisingコンバージョントラッキングピクセルを介してオンライン取引をトラッキングでき、広告主は取引 ID を使用してオフライン取引をトラッキングし、フィードを介して配信できます。

* オンライン取引の場合、Adobe Advertisingは広告のクリック数と、結果として生じる web サイト上の取引を追跡します。

* 広告主は、オフラインコンバージョンを追跡し、トランザクションレベルのフィードファイルをAdobe Advertisingに送信する必要があります。

## 実装の概要

*エージェンシーアカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. アカウントまたはキャンペーンのトラッキングオプション「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」を使用して、アカウントまたはキャンペーンの各キーワード（キーワードレベルのトラッキングの場合）または広告（広告レベルのトラッキングの場合）の宛先 URL または最終 URL を自動的に生成します。

1. オンラインコンバージョン用にAdobe Advertisingコンバージョントラッキングを設定します。 このプロセスは、Adobe Advertisingのピクセルベースのコンバージョントラッキングを使用する広告主の場合と同じです。 一意のトランザクション ID （`ev_transid=<transid>`）のパラメーターを含むコンバージョンタグを生成することが重要です。

1. 各トランザクションのオフライン部分に対して、広告主は、トランザクションのオンライン部分で使用されたのと同じトランザクション ID を生成し、フィードファイルに含めます。

1. 広告主は、指定されたサーバーの場所に [&#x200B; 必要な変換データ &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) を含むファイルをアップロードします。

1. テクニカルサポートは、アップロードされたファイルのコンバージョンデータを解析して、Adobe Advertisingにアップロードします。 次に、Adobe Advertisingは、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、[&#x200B; 孤立トランザクション &#x200B;](/help/search-social-commerce/glossary.md#o-p) の有無を確認します。

>[!MORELIKETHIS]
>
>* [&#x200B; 変換フィードファイルのファイル要件 &#x200B;](feed-file-requirements.md)
>* [&#x200B; トランザクション ID を使用したデータフィードに関するデータ要件 &#x200B;](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)
