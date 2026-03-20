---
title: '[!UICONTROL Simple Ad Serving] について'
description: イベント追跡ピクセルを使用した [!UICONTROL Simple Ad Serving] 取引について説明します。
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
source-git-commit: d6416dae58543e1287b7af7df44eada4be023731
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] について

[!UICONTROL Simple Ad Serving] は、1 つの専用プレースメントを使用して、指定されたパブリッシャーおよび 1 つの広告タイプに対して、保証された、決定されていない広告の配信およびレポートを提供します。 パブリッシャーが取引 ID を使用して取引を実行できない場合は、[!DNL Simple Ad Serving] を使用します。 すべてのターゲティング、予算ペーシングとキャッピング、フリークエンシーキャップは、パブリッシャーが処理します。 これらの取引をイベントトラッキングピクセルで実行します。

[!UICONTROL Simple Ad Serving] では、各広告はパブリッシャー（サイトサーバー）から直接提供され、DSPはイベントトラッキングピクセルを提供してパブリッシャーに送信します。パブリッシャーはピクセルを実装し、DSP広告をトラフィック処理する必要があります。 在庫タイプに応じて、イベントピクセルは、インプレッション、クリックスルーおよびビデオ再生イベントを測定します。

次の広告タイプを使用できます。

* デスクトップ標準プリロール
* タブレットおよびモバイルの標準プリロール
* 接続された TV 標準プリロール
* 表示
* 音声

[!UICONTROL Simple Ad Serving]/[!UICONTROL Inventory] ビューで [!UICONTROL Deals] しい取引を作成できます。 DSPは、サブタイプ「[!DNL Simple ad serving]」の広告のプレースメントを自動的に生成します。 プレースメントは契約をターゲットにしますが、追加のターゲティング、予算、フリークエンシーキャップは許可しません。 取引名、CPM、インプレッション数、取引日など、一部の取引設定のみを編集できます。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving] のプレースメントは、アカウントの使用可能な資金や、キャンペーンおよびパッケージの予算に準拠していません。 ただし、費用は追跡され、これらの予算にカウントされます。 CPMが$0 の場合でも、イベントデータは常にトラッキングされます。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Simple Ad Serving] しい取引の作成 &#x200B;](simple-deal-create.md)
>* [[!UICONTROL Simple Ad Serving] 取引設定の編集 &#x200B;](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving] 設定 &#x200B;](simple-deal-settings.md)
>* [&#x200B; 取引の詳細レポートの表示 &#x200B;](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
