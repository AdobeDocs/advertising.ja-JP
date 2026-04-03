---
title: プログラム的に取引を保証する
description: パブリッシャーと交渉したプログラマティック保証（PG）取引を設定する方法について説明します。
feature: DSP Private Inventory, DSP Deal IDs, DSP Programmatic Guaranteed Deals
exl-id: d962942f-c248-4b48-97bd-baa2df3a519e
TQID: https://experienceleague.adobe.com/z7kz7dnCjgCGmlgDlFvbZXTn8d9-OMEunv-Sm-k6TzY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 452
ht-degree: 0%

---

# プログラム的に取引を保証する

*[サポートされているサプライサイドプラットフォームのみ](programmatic-guaranteed-about.md)*

サポートされている発行者とのプログラマティック保証（PG）契約を交渉した後は、[!DNL Deal ID Inbox]を使用するか、契約の詳細を手動で入力することで、DSP内で契約を設定できます。

>[!NOTE]
>
> PG取引の場合、発行者はすべての予算ペーシング、予算上限設定、およびターゲティングを処理します。 PGからDSPを使用できるすべてのSSPは、発行者が予算上限を設定できることを確認します。
>
> [!DNL FreeWheel]でパブリッシャーとのプログラム的な保証取引を設定するには、追加の権限と手順が必要です。 詳しくは、「[でのプログラマティック保証取引の設定の概要」を参照してください。 [!DNL FreeWheel]](freewheel-overview.md)

## [!DNL Deal ID Inbox]を使用してプログラムによる保証契約を設定します {#pg-setup-deal-id-inbox}

次の方法は、[!DNL FreeWheel]、[!DNL Google Authorized Buyers]、[!DNL Magnite DV+]の場合に推奨される手順です。

1. [取引を承諾](deal-id-inbox-accept.md)。

1. 取引を保存したら、取引に使用する広告（またはパブリッシャーが管理する広告の1x1 トラッキングピクセル）を選択し、プロンプトに従ってプログラマティック保証（PG）のデフォルトのプレースメントを作成します。

   取引のデフォルトのPG プレースメントを作成することは、購入の100%を配信するために必須です。 この種類のプレースメントにはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

   * 1件の契約を受け入れると、PGのデフォルトのプレースメント作成ワークフローに自動的にリダイレクトされます。

     すべての[!DNL FreeWheel]件の契約は、1件の契約として提案されます。

   * 複数のPG取引IDを持つ提案を受け入れる場合は、作成する必要がある各PGのデフォルトプレースメントを特定します。 必要なプレースメントをすべて作成すると、「続行」ボタンが有効になります。

1. （オプション） ![ オプションメニュー](/help/dsp/assets/options-menu.png)**>[!UICONTROL Attach new placement]**&#x200B;をクリックして、追加のPGまたは非PG配置でPG取引をターゲットにします。

   取引では、あらゆるメディアタイプ（コネクテッド TV、デスクトップ PC、オーディオなど）の組み合わせをサポートする複数の配置をターゲットにすることができます。

## 手作業でプログラム的に保証する契約を設定する

他のすべてのSSPに対してこの方法を使用します。

1. [取引IDの詳細を手動で設定します](deal-id-create.md)。

1. 契約を保存したら、契約に使用する広告（またはパブリッシャーが管理する広告の1x1 トラッキングピクセル）を選択し、プロンプトに従ってPGのデフォルトのプレースメントを作成します。

   取引のPG デフォルトプレースメントを作成することは、購入の100%を提供するために必須です。 この種類のプレースメントにはターゲティングがないので、DSPはパブリッシャーからのすべての入札リクエストに入札を返すことができます。

1. （オプション） ![ オプションメニュー](/help/dsp/assets/options-menu.png)**>[!UICONTROL Attach new placement]**&#x200B;をクリックして、追加のPGまたは非PG配置でPG取引をターゲットにします。

   取引では、あらゆるメディアタイプ（コネクテッド TV、デスクトップ PC、オーディオなど）の組み合わせをサポートする複数の配置をターゲットにすることができます。

>[!MORELIKETHIS]
>
>* [ プログラマティック保証取引について](programmatic-guaranteed-about.md)
>* [ プログラマティック保証取引の交渉に関するヒント ](/help/dsp/inventory/programmatic-guaranteed-tips.md)
>* [様とのプログラムで保証された契約の広告を送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [取引IDの詳細を手動で作成する](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [Advertising DSPの在庫機能の概要](inventory-overview.md)
