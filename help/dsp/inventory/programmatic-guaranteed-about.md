---
title: プログラムで保証された取引について
description: プログラム保証（PG）取引と、それらを提供することが認定されている SSP について説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: 47c89d8a-f45f-4fcb-84a6-031f7d7f580f
source-git-commit: d5a291c8d1f464e1c22777512d29f4e041bb7988
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# プログラムで保証された取引について

プログラム保証（PG）取引は、（広告サーバタグではなく）取引 ID を使用して、パブリッシャーと直接行う保証された購入です。 PG は、ユーザーとパブリッシャーにとって管理する柔軟性が高く、通常のタグ購入よりも透明性が高くなります。 請求とレポートはDSPによって統合されるので、時間を節約できます。

## PG 取引の機能

* 契約は常にDSPを通じて請求されます。
* 契約には固定価格と数量があります。
* パブリッシャーまたは供給側プラットフォーム（SSP）は、すべての予算ペーシング、予算キャッピング、あらゆるターゲティングを処理します。
* 通常、パブリッシャーの広告サーバーでは、契約の優先度が高くなります。
* 入札リクエストは、1 つの取引や購入者に限定されません。
* 1 つの取引 ID で複数のタイプのビデオがサポートされます。
* パブリッシャーが管理する広告は、[!DNL Google Authorized Buyers] SSP を介して受け付けます。
* SSP とパブリッシャーには配信 SLA があります。

DSPが各入札要求にリクエストを返し、SSP の配信 SLA を満たすことができるように、PG の取引には PG のデフォルトの配置と広告（公開者管理広告の場合は 1 x 1 ピクセル）が必要です。 必須の PG デフォルト配置を設定したら、他の配置で PG 取引をターゲットに設定することもできます。

## DSPでの PG 取引に関して認定された SSP

* [!DNL Ambient Digital]
* [!DNL FreeWheel]
* [!DNL Google Authorized Buyers]
* [!DNL Magnite CTV] （formerly [!DNL Telaria]）
* [!DNL Magnite DV+] （formerly [!DNL Rubicon]）
* [!DNL OpenX]
* [!DNL SpotX]

>[!MORELIKETHIS]
>
>* [ プログラムで保証された取引の交渉に関するヒント ](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [ プログラムで保証された取引の設定 ](programmatic-guaranteed-set-up.md)
>* [SSP パートナー ](ssp-partners.md)
>* [ インベントリ機能の概要 ](inventory-overview.md)
