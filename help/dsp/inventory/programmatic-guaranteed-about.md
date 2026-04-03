---
title: プログラマティック保証取引について
description: プログラマティック保証型（PG）取引と、その提供が認定されているSSPについて説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 47c89d8a-f45f-4fcb-84a6-031f7d7f580f
TQID: https://experienceleague.adobe.com/LJPeIv8z6DiQS-eCe8obWgKkWi5onwpBadIgElLzkXw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 240
ht-degree: 0%

---

# プログラマティック保証取引について

プログラマティック保証型（PG）取引とは、広告サーバータグではなく、取引IDを介してメディア企業と直接やり取りして購入する保証型の取引です。 PGは、ユーザーとパブリッシャーが管理する柔軟性が高く、通常のタグ購入よりも高い透明性を提供します。 請求とレポートはDSPを通じて統合されるため、時間を節約できます。

## PG契約の特徴

* 契約は常にDSPを通じて請求されます。
* その取り引きには一定の価格と数量があります。
* メディア企業やサプライサイドプラットフォーム（SSP）は、予算のペーシング、予算上限、ターゲティングなどを担当します。
* 通常、パブリッシャーの広告サーバーでは、契約の優先順位が高くなります。
* 入札リクエストは、単一の取引や購入者に限定されません。
* 単一の案件IDでは、複数のタイプの動画がサポートされています。
* 発行者が管理する広告は、[!DNL Google Authorized Buyers] SSP経由で受け入れられます。
* SSPとパブリッシャーには配信SLAがあります。

PG取引には、PGのデフォルトのプレースメントと広告（またはパブリッシャーが管理する広告の場合は1x1 ピクセル）が必要なので、DSPは入札リクエストごとにリクエストを返し、SSPで配信SLAを満たすことができます。 必須のPG デフォルトプレースメントを設定したら、PG ディールを他のプレースメントでターゲットにすることもできます。

## DSPのPG契約で認定されたSSP

* [!DNL Ambient Digital]
* [!DNL FreeWheel]
* [!DNL Google Authorized Buyers]
* [!DNL Magnite CTV] （以前の[!DNL Telaria]）
* [!DNL Magnite DV+] （以前の[!DNL Rubicon]）
* [!DNL OpenX]
* [!DNL SpotX]

>[!MORELIKETHIS]
>
>* [ プログラマティック保証取引の交渉に関するヒント ](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [ プログラム的な保証契約の設定](programmatic-guaranteed-set-up.md)
>* [SSP パートナー](ssp-partners.md)
>* [Advertising DSPの在庫機能の概要](inventory-overview.md)
