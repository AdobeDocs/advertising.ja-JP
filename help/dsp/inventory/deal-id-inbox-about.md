---
title: '[!UICONTROL Deal ID Inbox] について'
description: 公開者と既に交渉したプライベートな取引を  [!DNL FreeWheel], [!DNL Google Authorized Buyers]  （旧称  [!DNL AdX]), and [!DNL Magnite DV+]  （旧称  [!DNL Rubicon]）で受け入れることができる [!UICONTROL Deal ID inbox] 機能について説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: 394a281c9b9d7eeab939f4c58508ec1f34eba67c
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox] について

Advertising DSP [!UICONTROL Deal ID inbox] を使用すると、DSPがサプライサイドプラットフォーム（SSP）を通じてパブリッシャーから読み込んだ取引をすばやく設定できるので、各取引を手動で設定する必要はありません。 [!DNL FreeWheel]、[!DNL Google Authorized Buyers] （旧称 [!DNL AdX]）、[!DNL Magnite DV+] （旧称 [!DNL Rubicon]）のパブリッシャーと既に交渉した、保証されている場合と保証されていない場合のプライベートインベントリの取引は、[!UICONTROL Deal ID inbox] から受け入れることができます。

>[!NOTE]
>
>Advertising DSPは、[!DNL FreeWheel] API と統合された最初のDSPです。

[!UICONTROL Deal ID inbox] では、パブリッシャーが表示する取引の詳細を確認し、取引の設定をスピードアップし、手動入力エラーを回避できます。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSPは、毎日午前 4 時 30 分（EST）にすべての取引詳細を自動更新します。 また、すべての [!DNL FreeWheel] の取引を更新し、[!DNL Google] 時および [!DNL Magnite DV+] 時から既存の取引を更新します。 また、取引詳細を手動で更新して、いつでも新しい取引を入力することもできます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->

>[!NOTE]
>
>[!DNL Google Authorized Buyers] を通じてプログラムで保証された取引の場合、予算の 90% 以上を引き渡す必要があります。そうでない場合、アカウントが [!UICONTROL Deal ID inbox] の [!DNL Google] の取引へのアクセス権を失います。

## [!UICONTROL Deal ID Inbox] の実装

[!UICONTROL Deal ID inbox] で取引を受け取るには、SSP アカウントで組織のDSP アカウントを SSP アカウントにマッピングする必要があります。 DSPは、組織のアカウント名を関連する SSP と共有できます。 手順については、Adobe アカウントチームにお問い合わせください。

取引ネゴシエーション中に、親のDSPアカウントではなく、バイヤーに取引を送付するようにパブリッシャに伝えます。 取引識別子は、SSP に応じて名前または ID にすることができます。

## 取引に対して実行できるアクション

* **契約を確認** して、SSP が正しいパブリッシャー、フライト日、CPM、その他の契約の詳細を送信したことを確認します。 パブリッシャーが誤った場合は、DSP外のユーザーに連絡して、取引を修正し再送信してもらいます。

* **契約を承認** 確認すると、[!UICONTROL Deal ID inbox] ージに表示されなくなります。 受け入れられた取引は [!UICONTROL Inventory]/[!UICONTROL Deals] にリストされ、広告主のプレースメント内でターゲットにする準備が整います。

* 不要または未承諾の **取引を無視** します。 無視された取引は、[!UICONTROL Deal ID inbox] 内の「[!UICONTROL Ignored Deals]」タブに移動され、アーカイブとして機能します。 契約を無視しても、DSPは SSP やパブリッシャーに警告しません。

* **既に受け入れられた取引の詳細を変更**、[!UICONTROL Inventory]/[!UICONTROL Deals] （[!UICONTROL Deal ID inbox] にはない）から行います。 同様に、パブリッシャーが契約に変更を送信する場合、契約が設定されると、[!UICONTROL Deal ID inbox] が SSP からの変更を同期しないため、広告主は [!UICONTROL Inventory] > [!UICONTROL Deals] でこれらの変更を実装する責任があります。

## どのような種類の取引を受け入れることができますか？

取引リストに ![&#x200B; 同意する &#x200B;](/help/dsp/assets/accept.png) アイコンや [!UICONTROL Accept] ボタンが含まれていない場合、[!UICONTROL Deal ID inbox] ージから受け入れることはできません。 代わりに、[&#x200B; 取引 ID の詳細を手動で作成 &#x200B;](/help/dsp/inventory/deal-id-create.md) できます。

以下のタイプの取引は受け付けられません。

* 米ドル以外の [!DNL Google] のお得な情報。

* 米ドル以外の [!DNL Magnite DV+] の取引

* お使いのアカウントの通貨に含まれない取引を [!DNL FreeWheel] します。

* 今日より前に終了日がある取引。

* 「複数のメディアタイプ」というラベルが付けられた古い [!DNL Magnite DV+] の取引。

契約の詳細には、契約が受け入れられないという理由が含まれています。

>[!MORELIKETHIS]
>
>* [&#x200B; 取引 ID インボックスでの取引の承認 &#x200B;](deal-id-inbox-accept.md)
>* [&#x200B; インベントリ機能の概要 &#x200B;](inventory-overview.md)
