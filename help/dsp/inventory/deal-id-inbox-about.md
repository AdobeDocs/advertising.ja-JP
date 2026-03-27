---
title: '[!UICONTROL Deal ID Inbox]について'
description: '[!UICONTROL Deal ID Inbox]機能について説明します。この機能を使用すると、既に [!DNL FreeWheel], [!DNL Google Authorized Buyers]  （旧称 [!DNL AdX]), and [!DNL Magnite DV+] ）でパブリッシャーと交渉したプライベート取引を受け入れることができます。 [!DNL Rubicon]'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox]について

Advertising DSP [!UICONTROL Deal ID Inbox]を使用すると、DSPがパブリッシャーからサプライサイドプラットフォーム（SSP）を通じて読み込んだ契約をすばやく設定できるので、各契約を手動で設定する必要はありません。 [!DNL FreeWheel]、[!DNL Google Authorized Buyers] （旧称[!DNL AdX]）、[!DNL Magnite DV+] （旧称[!DNL Rubicon]）でパブリッシャーと既に交渉した保証および保証されていないプライベート在庫取引を、[!UICONTROL Deal ID Inbox]から受け入れることができます。

>[!NOTE]
>
>Advertising DSPは、[!DNL FreeWheel] APIと統合する最初のDSPです。

[!UICONTROL Deal ID Inbox]では、発行者が見た契約の詳細を確認し、契約の設定を迅速化し、手作業による入力エラーを回避できます。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSPでは、東部標準時の午前4:30時に、すべての取引詳細が毎日自動的に更新されます。 また、すべての[!DNL FreeWheel]件の取引が更新され、1時間ごとに[!DNL Google]と[!DNL Magnite DV+]から既存の取引が更新されます。 また、取引の詳細を手動で更新して、いつでも新しい取引を入力することもできます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>[!DNL Google Authorized Buyers]を通じてプログラムで保証された契約の場合、予算の90%以上を提供する必要があります。そうしないと、[!DNL Google]で[!UICONTROL Deal ID Inbox]件の契約へのアクセス権をアカウントが失います。

## [!UICONTROL Deal ID Inbox]を実装しています

[!UICONTROL Deal ID Inbox]で契約を受け取るには、組織のDSP アカウントをSSP アカウントにマッピングする必要があります。 DSPでは、組織のアカウント名を関連するSSPと共有できます。 手順については、Adobe アカウントチームにお問い合わせください。

取引交渉中に、親のDSP アカウントではなく、購入者に取引を送信するようにパブリッシャーに伝えます。 契約IDは、SSPに応じて名前またはIDにすることができます。

## 取引に対して実行できるアクション

* **契約を確認**&#x200B;して、SSPが正しい発行者、フライト日、CPM、およびその他の契約の詳細を送信したことを確認します。 ミスがあった場合は、DSP以外のサイトで連絡を取り、問題を修正して再送信できるようにします。

* **お得な情報を確認した後**&#x200B;に同意すると、[!UICONTROL Deal ID Inbox]には表示されなくなります。 承認されたお得な情報は[!UICONTROL Inventory] > [!UICONTROL Deals]に一覧表示され、広告主のプレースメント内でターゲットする準備ができています。

* **不要な取引**&#x200B;または未承諾の取引を無視します。 無視された取引は、[!UICONTROL Ignored Deals]内の[!UICONTROL Deal ID Inbox] タブに移動され、アーカイブとして機能します。 DSPでは、取引を無視しても、SSPやパブリッシャーにアラートは通知されません。

* **既に受け入れられている取引**&#x200B;の詳細を[!UICONTROL Inventory] > [!UICONTROL Deals]から変更します（[!UICONTROL Deal ID Inbox]には含まれません）。 同様に、広告主が契約に変更を送信する場合、契約の設定後に[!UICONTROL Inventory]がSSPからの変更を同期しないため、広告主は[!UICONTROL Deals] > [!UICONTROL Deal ID Inbox]でそれらの変更を実装する責任があります。

## どのような取引が認められないのか。

取引リストに![同意](/help/dsp/assets/accept.png) アイコンまたは[!UICONTROL Accept] ボタンが含まれていない場合、[!UICONTROL Deal ID Inbox]から同意することはできません。 代わりに、[取引IDの詳細を手動で作成できます](/help/dsp/inventory/deal-id-create.md)。

次の種類のお得な情報は受け取ることができません。

* 米ドル以外の[!DNL Google]件の取引。

* USD以外の[!DNL Magnite DV+]件の案件

* アカウント通貨に含まれていない[!DNL FreeWheel]件の取引。

* 今日より前に終了日が設定されている契約。

* 「複数のメディアタイプ」としてラベル付けされた古い[!DNL Magnite DV+]件の取引。

取引の詳細には、取引が受け入れられない理由が含まれます。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [在庫機能の概要](inventory-overview.md)
