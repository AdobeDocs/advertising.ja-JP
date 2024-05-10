---
title: について [!UICONTROL Deal ID Inbox]
description: について説明します [!UICONTROL Deal ID inbox] この機能により、既にパブリッシャーとネゴシエートしたプライベートな取引を受け入れることができます [!DNL FreeWheel], [!DNL Google Authorized Buyers] （旧称： [!DNL AdX]), and [!DNL Magnite DV+] （formerly [!DNL Rubicon]）に設定します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: a1ba7de0-d6b4-4e22-8615-3e62d2ffdf5c
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# について [!UICONTROL Deal ID Inbox]

広告DSP [!UICONTROL Deal ID inbox] では、DSPが SSP （Supply Side Platform）を通じてパブリッシャーからインポートした取引をすばやく設定できるので、各取引を手動で設定する必要はありません。 既にパブリッシャーと交渉した、保証されている/保証されていないプライベート在庫取引を受け入れることができます [!DNL FreeWheel], [!DNL Google Authorized Buyers] （旧称： [!DNL AdX]）、および [!DNL Magnite DV+] （formerly [!DNL Rubicon]）から [!UICONTROL Deal ID inbox].

>[!NOTE]
>
>Advertising DSPは、と統合された最初のDSPです [!DNL FreeWheel] API です。

が含まれる [!UICONTROL Deal ID inbox]を使用すると、パブリッシャーが表示する取引の詳細を確認し、取引の設定を迅速化し、手動入力エラーを回避できます。

<!-- 
Accepting a deal automatically pre-populates a new Deal ID record with details from the publisher, and you need to enter only the publisher [always? or just in some cases?], the media type, who can access the deal, and any attribute labels to apply to the deal so it's easy to find. [Are labels a dimension you can report on?]

For each available deal, you can review the deal details sent directly from the publisher. Some deals are grouped as proposals (packages), and you can see the individual deal details by reviewing the deal.

You can accept any available deal or move an incorrect deal to the Ignored Deals tab. You can also un-ignore deals, which moves them back to the New Deals tab so you can potentially accept them.

For each deal, you can select one publisher and one media type (Desktop Video, Mobile Video, Connected TV, Display, or Audio), and you can share the deal with specific advertisers and with all advertisers for a specific account.
 -->

DSPは、毎日午前 4 時 30 分（EST）にすべての取引詳細を自動更新します。 また、すべての [!DNL FreeWheel] の取引と既存の取引の更新 [!DNL Google] および [!DNL Magnite DV+] 毎時。 また、取引詳細を手動で更新して、いつでも新しい取引を入力することもできます。

<!-- MC: I'm not sure where I got the following. Is this currently true? -->
>[!NOTE]
>
>を介したプログラムで保証された取引の場合 [!DNL Google Authorized Buyers]、予算の 90% 以上でを配信する必要があります。そうでない場合、アカウントがへのアクセスを失います [!DNL Google] 次の項目を取引 [!UICONTROL Deal ID inbox].

## の実装 [!UICONTROL Deal ID Inbox]

お得な情報を [!UICONTROL Deal ID inbox]を入力します。SSP アカウントは、組織のDSP アカウントを SSP アカウントにマッピングする必要があります。 DSPは、組織のアカウント名を関連する SSP と共有できます。 手順については、Adobeアカウントチームにお問い合わせください。

取引ネゴシエーション中に、親DSPアカウントではなくバイヤーに取引を送付するようにパブリッシャに伝えます。 取引識別子は、SSP に応じて名前または ID にすることができます。

## 取引に対して実行できるアクション

* **契約のレビュー** ssp が正しいパブリッシャー、フライト日、CPM、その他の契約の詳細を送信したことを確認します。 パブリッシャーが誤った場合は、DSP外のユーザーに連絡して、取引を修正し再送信してもらいます。

* **取引の承認** 確認すると、に表示されなくなります [!UICONTROL Deal ID inbox]. 受け入れられた取引のリストは、次のとおりです。 [!UICONTROL Inventory] > [!UICONTROL Deals] 広告主のプレースメント内をターゲットにする準備ができています。

* **契約を無視** 不要または一方的です。 無視された取引はに移動されます [!UICONTROL Ignored Deals] 内のタブ [!UICONTROL Deal ID inbox]アーカイブとして機能します。 契約を無視しても、DSPは SSP やパブリッシャーに警告しません。

* **既に承認済みの取引の詳細を変更** から [!UICONTROL Inventory] > [!UICONTROL Deals] （次に含まれない [!UICONTROL Deal ID inbox]）に設定します。 同様に、パブリッシャーが契約に変更を送信する場合、広告主は [!UICONTROL Inventory] > [!UICONTROL Deals] なぜなら [!UICONTROL Deal ID inbox] は、取引が設定された後に SSP からの変更を同期しません。

## どのような種類の取引を受け入れることができますか？

取引リストに ![承諾](/help/dsp/assets/accept.png) アイコンまたは [!UICONTROL Accept] ボタンを使用します。このボタンは、 [!UICONTROL Deal ID inbox]. 代わりに、次のことができます [取引 ID の詳細の手動作成](/help/dsp/inventory/deal-id-create.md).

以下のタイプの取引は受け付けられません。

* [!DNL Google] 米ドル以外の契約。

* [!DNL Magnite DV+] 米ドル以外の契約

* [!DNL FreeWheel] お使いのアカウントの通貨に含まれていない取引。

* 今日より前に終了日がある取引。

* 旧 [!DNL Magnite DV+] 「複数のメディアタイプ」というラベルが付けられた取引。

契約の詳細には、契約が受け入れられないという理由が含まれています。

>[!MORELIKETHIS]
>
>* [取引 ID インボックスでの取引の承認](deal-id-inbox-accept.md)
>* [インベントリ機能の概要](inventory-overview.md)
