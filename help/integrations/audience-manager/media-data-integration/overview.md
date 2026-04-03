---
title: Adobe Audience ManagerへのDSP メディア露出データの送信の概要
description: Audience Manager イベントピクセルを使用して、Advertising DSP キャンペーンからインプレッションレベルおよびクリックレベルのデータを取得する方法について説明します
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
TQID: https://experienceleague.adobe.com/MqAVZH8WKVulxVDOD3SDbROYnkRG0tlm028WGBL9wOM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 529
ht-degree: 0%

---

# Adobe Audience ManagerへのDSP メディア露出データの送信の概要

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを使用する広告主*

Adobe Audience Managerを使用しているAdvertising DSPのお客様は、Audience Manager イベントピクセルを使用して、DSP キャンペーンからインプレッションレベルのデータとクリックレベルのデータを取得できます。 イベントピクセルは、データを実用的なシグナルとしてAudience Managerに送信します。 これらのシグナルにより、より高度なセグメンテーション、頻度の管理、マーケティング分析、レポートインサイトなど、DSPの様々なユースケースが可能になります。

DSPでは、Audience Managerにこれらのシグナルを送信する料金は請求されません。 ただし、標準的なAudience Manager取り込みコストは、Audience Manager契約に従ってサーバーコールに基づいて支払います。 Audience Managerでは、2つの異なる方法で追跡される重複したイベントが削除されるため、各イベントは1回だけ課金されます。

>[!NOTE]
>
> Audience Managerでは、広告サーバーのログファイルからのデータのキャプチャもサポートしているため、柔軟性が低くなります。 このドキュメントでは、そのプロセスについては説明しません。

## プライマリの利点

* DSPのキャンペーンデータは、Audience Managerにリアルタイムで取り込まれます。これにより、ルールベースの特性を構築し、セグメントの定義に使用できます。

* セグメントは、ユーザーの特性とセグメント評価の直後にターゲティングで利用でき、リアルタイムのターゲティング活動を強化します。

* クリエイターをまたいだ配信頻度の上限、過去のキャンペーンに触れた利用者のリターゲティング、下流サイトの行動やエントリポイントの分析など、ユースケースごとにキャンペーンデータを活用できます。

* 集約されたデータは、キャンペーンのパフォーマンスの統合ビューを提供し、カスタムコンバージョンパスの特定に役立ちます。Audience Manager [!DNL Audience Optimization Reports]またはAdobe Analytics [[!DNL Audience Analytics] との](/help/integrations/audience-manager/audience-analytics.md)統合を通じて、コンバージョンにつながるイベントのシーケンスを改善するために使用できます。

## データの追跡方法

Audience Managerのインプレッションとクリックのイベントピクセルは、cookie ベースです。 ピクセルは、モバイルアプリやコネクテッド TV （CTV）など、Cookieのない環境で発生するイベントをキャプチャしません。<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### インプレッション追跡ピクセル

Audience Managerは、1xl ピクセルの透明なイベントトラッキングピクセルを広告にアタッチすると、広告のインプレッションデータをトラッキングします。 イベントピクセルは、広告がユーザーに配信され、web ブラウザーによって読み込まれるたびに読み込まれます。 ピクセルは、Audience Managerのレガシードメインである[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)のクライアント固有のサブドメインから読み込まれ、キーと値のペアとしてパラメーターを含みます。 イベント呼び出しは、インプレッションとコンバージョンデータを収集し、それをAudience Manager データ収集サーバーに送信します。

### クリックトラッキングピクセル

Audience Managerでは、広告が配信されるたびに透明なイベントピクセルが読み込まれない点を除いて、クリック数はインプレッション数と同様に追跡されます。 代わりに、クリックデータは広告のクリックスルーURLで追跡されます。 この広告は、Audience Manager データ コレクション サーバーによる処理のために、Audience Managerのレガシードメインである[`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html)のクライアント固有のサブドメインを指しています。 その後、サーバーはユーザーを意図したランディングページにリダイレクトします。 URLには、キーと値のペアとしてパラメーターが含まれています。

>[!NOTE]
>
>お客様の組織で[!DNL Analytics] トラッキングを使用している場合は、Audience Manager クリック トラッキングが不要になる可能性があります。 Adobe Analyticsはクリックのシグナルをキャプチャし、[&#x200B; サーバーサイド転送](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html)を通じてAudience Managerに送信できます。

>[!MORELIKETHIS]
>
>* [Advertising DSP キャンペーンからクリックとインプレッションのデータを収集](collect.md)
>* [&#x200B; ユースケース &#x200B;](use-cases.md)
