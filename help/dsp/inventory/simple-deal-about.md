---
title: '[!UICONTROL Simple Ad Serving]について'
description: イベントトラッキングピクセルを使用した[!UICONTROL Simple Ad Serving]件の取引について説明します。
feature: DSP Simple Ad Serving
exl-id: 327a2c93-d729-42e1-856f-f0e05efab7ca
TQID: https://experienceleague.adobe.com/w4KFePatd7CZ1xC8dd1CItl88-6myAZw8TuatHzHnRI
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 227
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving]について

[!UICONTROL Simple Ad Serving]は、指定されたパブリッシャーと単一の広告タイプに対して、単一の専用プレースメントを使用する、決定されていない保証付き広告の配信とレポートを提供します。 発行者が案件IDで案件を実行できない場合は、[!DNL Simple Ad Serving]を使用します。 ターゲティング、予算のペーシングとキャッピング、頻度のキャッピングはすべてメディア企業が処理します。 イベントトラッキングピクセルを通じて契約を実行します。

[!UICONTROL Simple Ad Serving]では、各広告はパブリッシャー（サイトサービス）によって直接配信され、DSPはパブリッシャーに送信するイベントトラッキングピクセルを提供します。パブリッシャーは、DSP広告を実装してトラフィックを送信する必要があります。 在庫の種類に応じて、イベントピクセルはインプレッション、クリックスルー、動画再生イベントを測定します。

次の広告タイプを使用できます。

* デスクトップ標準プレロール
* タブレットおよびモバイル標準のプレロール
* コネクテッド TV標準プレロール
* 表示
* オーディオ

[!UICONTROL Simple Ad Serving] > [!UICONTROL Inventory] ビューで[!UICONTROL Deals]件の取引を作成できます。 DSPは、広告のサブタイプ「[!DNL Simple ad serving]」を含むプレースメントを自動的に生成します。 プレースメントは取引をターゲットにしていますが、追加のターゲティング、予算、頻度の上限は許可されていません。 取引名、CPM、インプレッション、フライト日など、一部の取引設定のみを編集できます。<!-- If you need multiple tracking tags for a [!UICONTROL Simple Ad Serving] deal, create a duplicate deal. -->

[!UICONTROL Simple Ad Serving]件のプレースメントは、アカウントの使用可能な資金またはキャンペーンとパッケージの予算に準拠していません。 しかし、それらの予算に対して支出を追跡し、カウントします。 CPMが0 ドルの場合でも、イベントデータは常に追跡されます。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Simple Ad Serving]件の取引を作成](simple-deal-create.md)
>* [取引設定[!UICONTROL Simple Ad Serving]を編集](simple-deal-edit.md)
>* [[!UICONTROL Simple Ad Serving]設定](simple-deal-settings.md)
>* [取引に関する詳細なレポートを表示](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
