---
title: DSP Media のAdobe Audience Managerへの公開データ送信の概要
description: Audience Managerイベントピクセルを使用して、Advertising DSP キャンペーンからインプレッションレベルおよびクリックレベルのデータを取り込む方法を説明します
feature: Integration with Adobe Audience Manager
exl-id: c299cdf0-a83e-4026-8b8b-22ce08af0cc4
source-git-commit: c204955ec48826d00a5f78e5be4849f53d09e224
workflow-type: tm+mt
source-wordcount: '529'
ht-degree: 0%

---

# DSP Media のAdobe Audience Managerへの公開データ送信の概要

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを行う広告主*

Adobe Audience Managerを使用するAdvertising DSPのお客様は、Audience Managerイベントピクセルを使用して、DSP キャンペーンからインプレッションレベルのデータとクリックレベルのデータを取り込むことができます。 イベントピクセルは、アクションにつながるシグナルとしてデータをAudience Managerに送ります。 これらのシグナルにより、より高度なセグメント化、頻度管理、マーケティング分析、レポートインサイトなど、様々なDSP ユースケースが可能になります。

DSPは、これらのシグナルをAudience Managerに送信するのに課金しません。 ただし、標準のAudience Manager取得コストは、Audience Managerの契約に従ってサーバーの呼び出しに基づいて支払います。 Audience Managerは、2 つの異なる方法でトラッキングされる重複イベントを削除して、各イベントが 1 回だけ請求されるようにします。

>[!NOTE]
>
> また、Audience Managerは ad server ログファイルからのデータのキャプチャもサポートしているので、柔軟性が低くなります。 このプロセスについては、このドキュメントでは説明しません。

## プライマリの利点

* DSP campaign のデータはリアルタイムでAudience Managerに送られ、セグメントの定義に使用するルールベースの特性を作成するために使用できます。

* セグメントは、ユーザー特性とセグメントの選定の直後にターゲティングに使用できるので、リアルタイムターゲティングの取り組みを強化します。

* クリエイティブのフリークエンシーキャップ、以前のキャンペーンで使用したユーザーのリターゲティング、ダウンストリームサイトの行動とエントリポイントの分析などのユースケースでキャンペーンデータを活用できます。

* 集計データを使用すると、キャンペーンパフォーマンスの統一されたビューを提供し、カスタムコンバージョンパスの特定に役立ちます。また、Audience Manager[!DNL Audience Optimization Reports] ールまたは [[!DNL Audience Analytics] Adobe Analyticsとの統合 ](/help/integrations/audience-manager/audience-analytics.md) を通じてコンバージョンにつながるイベントのシーケンスを改善するために使用できます。

## データの追跡方法

Audience Managerインプレッションとクリックイベントのピクセルは cookie ベースです。 ピクセルでは、モバイルアプリや接続されたテレビ（CTV）など、Cookie のない環境で発生するイベントはキャプチャされません。<!-- 6/24: CTV inventory isn't clickable, and impression tracking would be lost when we convert users from IP to cookies. -->

### インプレッショントラッキングのピクセル

Audience Managerは、広告に 1 xl ピクセルの透明なイベントトラッキングピクセルを付加すると、広告のインプレッションデータをトラッキングします。 イベントピクセルは、広告がユーザーに提供され、web ブラウザーによって読み込まれるたびに読み込まれます。 ピクセルは、Audience Managerのレガシードメインである [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) のクライアント固有のサブドメインから読み込まれ、キーと値のペアとしてパラメーターを含みます。 イベント呼び出しは、インプレッションおよびコンバージョンデータを収集し、Audience Managerデータ収集サーバーに送信します。

### クリック追跡ピクセル

Audience Managerは、インプレッションと同様にクリック数を追跡しますが、広告が配信されるたびに透明なイベントピクセルを読み込まない点が異なります。 代わりに、クリックデータが広告のクリックスルー URL でトラッキングされます。 この AD は、クライアント固有の [`demdex.net`](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reference/demdex-calls.html) のサブドメインを指します。これは、Audience Managerデータ収集サーバによって処理されるAudience Manager用の従来のドメインです。 次に、サーバーは目的のランディングページにユーザーをリダイレクトします。 URL には、パラメーターがキーと値のペアとして含まれています。

>[!NOTE]
>
>組織で [!DNL Analytics] トラッキングを使用している場合は、Audience Managerのクリックのトラッキングは不要な場合があります。 Adobe Analyticsは、クリック信号をキャプチャし、[ サーバーサイド転送 ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/server-side-forwarding/ssf.html) を介してAudience Managerに送信できます。

>[!MORELIKETHIS]
>
>* [Advertising DSP キャンペーンからクリックとインプレッションのデータを収集 ](collect.md)
>* [ ユースケース ](use-cases.md)
