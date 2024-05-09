---
title: プログラムで保証された取引の設定
description: パブリッシャーと交渉したプログラム保証（PG）取引を設定する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# プログラムで保証された取引の設定

*[サプライサイドプラットフォームのみサポート](programmatic-guaranteed-about.md)*

サポートされているパブリッシャーとプログラム保証（PG）契約をネゴシエートした後は、次のいずれかを使用して、DSP内で契約を設定できます [!DNL Deal ID inbox] または、契約の詳細を手動で入力します。

>[!NOTE]
>
> PG 取引の場合、パブリッシャーは、すべての予算ペーシング、予算キャッピングおよびターゲティングを処理します。 DSP経由で PG を許可するすべての SSP は、パブリッシャーがバジェットキャッピングを設定できることを確認します。
>
> プログラムで保証された取引の設定をパブリッシャーとオンにする [!DNL FreeWheel] 追加の権限と手順が必要です。 参照先」[でのプログラムで保証された取引の設定の概要 [!DNL FreeWheel]](freewheel-overview.md)」を参照してください。

## を使用した、プログラムで保証された取引の設定 [!DNL Deal ID Inbox] {#pg-setup-deal-id-inbox}

以下の方法は、推奨される手順です [!DNL FreeWheel], [!DNL Google Authorized Buyers]、および [!DNL Magnite DV+].

1. [取引を受け入れる](deal-id-inbox-accept.md).

1. 取引を保存したら、プロンプトが表示されたら、取引に使用する広告（または公開者管理広告の 1x1 トラッキングピクセル）を選択し、プログラム保証（PG）のデフォルト配置を作成します。

   購入の 100% を提供するには、契約のデフォルト PG 配置の作成が必須です。 このタイプのプレースメントにはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

   * 1 つの取引を受け入れる場合は、PG のデフォルトのプレースメント作成ワークフローに自動的にリダイレクトされます。

     すべて [!DNL FreeWheel] 契約は 1 つの契約として提案されます。

   * 複数の PG 取引 ID を持つ提案を受け入れる場合は、作成する必要がある各 PG デフォルト配置を特定します。 必要なプレースメントをすべて作成すると、「続行」ボタンが有効になります。

1. （オプション）をクリックして、追加の PG または PG 以外の配置で PG 取引をターゲットに設定します ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   契約のターゲットは、あらゆるメディアタイプ（コネクテッド TV、デスクトップ、オーディオなど）の任意の組み合わせをサポートする複数のプレースメントにすることができます。

## プログラムで保証された取引の手動設定

他のすべての SSP に対してこの方法を使用します。

1. [取引 ID の詳細の手動設定](deal-id-create.md).

1. 契約を保存したら、契約に使用する広告（または公開者管理広告の 1x1 トラッキングピクセル）を選択し、プロンプトに従って PG デフォルトのプレースメントを作成します。

   購入の 100% を配信するには、契約の PG デフォルト配置の作成が必須です。 このタイプのプレースメントにはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

1. （オプション）をクリックして、追加の PG または PG 以外の配置で PG 取引をターゲットに設定します ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL Attach new placement]**.

   契約のターゲットは、あらゆるメディアタイプ（コネクテッド TV、デスクトップ、オーディオなど）の任意の組み合わせをサポートする複数のプレースメントにすることができます。

>[!MORELIKETHIS]
>
>* [プログラムで保証された取引について](programmatic-guaranteed-about.md)
>* [プログラムで保証された取引を交渉するためのヒント](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [プログラムで保証された取引の広告を送信する [!DNL FreeWheel]](freewheel-submit.md)
>* [取引 ID インボックスでの取引の承認](deal-id-inbox-accept.md)
>* [取引 ID の詳細の手動作成](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [インベントリ機能の概要](inventory-overview.md)
