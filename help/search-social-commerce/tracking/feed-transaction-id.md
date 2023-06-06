---
title: トランザクション ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータでのトランザクション ID フィードの使用について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 0%

---

# トランザクション ID フィードを使用したコンバージョントラッキング

Adobe広告主がオンラインとオフラインの両方のトランザクションを持つ場合、広告主はAdobeAdvertising conversion-tracking ピクセルを介してオンライントランザクションを追跡し、広告主はトランザクション ID を使用してオフライントランザクションを追跡してフィードを介して配信できます。

* オンライントランザクションの場合、Adobe広告は、広告のクリック数および Web サイトでの結果のトランザクション数を追跡します。

* 広告主は、オフラインのコンバージョンを追跡し、トランザクションレベルのフィードファイルをAdobe広告に送信する必要があります。

## 実装の概要

*代理店のアカウントマネージャー [!DNL Adobe] アカウントマネージャー、管理者ユーザーロールのみ*

1. アカウントまたはキャンペーントラッキングオプションを使用する」[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]」をクリックします。

1. オンラインコンバージョン用にAdobe広告コンバージョントラッキングを設定します。 このプロセスは、Adobe広告のピクセルベースのコンバージョントラッキングを使用する広告主の場合と同じです。 一意のトランザクション ID(`ev_transid=<transid>`) をクリックします。

1. 広告主は、各トランザクションのオフライン部分に対して、フィードファイルに含めるトランザクションのオンライン部分で使用されたのと同じトランザクション ID を生成します。

1. 広告主が、 [必要なコンバージョンデータ](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md) を指定したサーバーの場所に追加します。

1. テクニカルサービスは、アップロードされたファイルのコンバージョンデータを解析し、そのデータをAdobe広告にアップロードします。 Adobe広告は、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [コンバージョンフィードファイルのファイル要件](feed-file-requirements.md)
>* [トランザクション ID を使用するデータフィードのデータ要件](/help/search-social-commerce/tracking/feed-transaction-id-data-requirements.md)

