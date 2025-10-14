---
title: 手動の取引 ID 設定
description: 手動で入力した取引 ID の設定の説明を参照してください。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
source-git-commit: badf6a1d7059b9e7e261165b19e00f09573b9e53
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# 手動の取引 ID 設定

| セクション | パラメーター | 説明 | 必須 | 編集可能 |
|---------|-----------|-------------|----------|----------|
| [ 契約詳細 ] | [!UICONTROL Deal name] | Advertising DSPで [!UICONTROL Deal ID] を識別するための名前。 名前を入力するか、「**[!UICONTROL Auto-name]**」を選択すると、DSPは取引の詳細に基づいて名前を生成します。<br><br> 自動生成される名前の例：`[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | はい | はい |
| | [!UICONTROL External deal ID] | パブリッシャーおよび SSP がこの取引を識別するために使用する ID。 | はい | 不可 |
| | [!UICONTROL Publisher] | この在庫を販売しているパブリッシャーの名前。 | はい | 不可 |
| | [!UICONTROL SSP] | この取引が実行される供給側プラットフォーム（SSP）。 | はい | 不可 |
| | [!UICONTROL Media type] | この契約を通じて購入されたメディアのタイプ：*[!UICONTROL Desktop video]*、*[!UICONTROL Mobile video]*、*[!UICONTROL Connected TV]*、*[!UICONTROL Display]*、*[!UICONTROL Audio]* または *[!UICONTROL Publisher Managed]*。 オプションは SSP によって異なります。<br><br> 取引で複数のメディアタイプが許可されている場合は、取引を作成する際に、デフォルトのプレースメントのメディアタイプを選択します。 後で、値を変更することも、単に [&#x200B; 追加のメディアタイプで新しいプレースメントを添付する &#x200B;](deal-id-attach-placements.md) こともできます <!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. -->。 | はい | 不可 |
| | [!UICONTROL Deal type] | 契約のコミットメントと価格設定の構造：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*：あなたとパブリッシャーは、インプレッション配信の固定数をコミットしていません。 この取引は在庫の最低価格を指定しますが、CPM は市場の状況に応じて変動し、増加する可能性があります。</li><li>*[!UICONTROL Non guaranteed (fixed)]*：あなたとパブリッシャーは、インプレッション配信の固定数をコミットしていません。 価格は交渉済みの固定レートで設定されます。</li><li>*[!UICONTROL Guaranteed (fixed)]*：お客様とパブリッシャーは、インプレッション数、ターゲティング、フライト日、固定価格について事前に定義された数値に同意しました。<br><br><b> 注：</b> 保証契約には、[!UICONTROL Tracking] のセクションにフライト日と指定されたインプレッション数が必要です。 また、取引にデフォルトのプログラム保証（PG）プレースメントを作成する必要があり、オプションで、代わりに他のプレースメントに取引を使用することもできます。</li></ul> | はい | 不可 |
| | [!UICONTROL CPM] | 1000 インプレッション数（CPM）あたりのネゴシエートされたコスト。 | はい | はい |
| | [ 通貨 ] | 取引の通貨。<br><br> すべての SSP は米ドルで取引を受け付けます。 SSP がDSP アカウントの通貨を受け入れると、その通貨も使用できます。 | はい | 不可 |
| | [!UICONTROL Billing method] | すべての取引 ID は [!DNL Adobe] で調達され、請求されます。 DSPでは、利用可能なすべてのメディアのベンダーを使用状況に基づいて支払い、ベンダーとの不一致を管理し、1 つの請求書をアカウントに送信します。 このオプションには、アカウントのレートカードに記載されている追加料金が発生します。 | はい | 不可 |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 取引にアクセスできるユーザーアカウントの電子メールアドレス。 | 不可 | はい |
| | [!UICONTROL Advertisers that can access this deal] | この取引にアクセスできるアカウント内の特定の広告主。<br><br><b> メモ：</b> 広告ビューから、追加のアカウントで広告 [!UICONTROL Deals] と契約を共有できます。 [ 取引 ] 行で、[**[!UICONTROL #]**]、[**[!UICONTROL share]**] の順にクリックし、電子メール アドレスと取引を共有します。 | はい | はい |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | この取引を使用するトラフィックの開始日と終了日。 これらの日付はトラッキング目的のみで、広告の配信には影響しません。<br><br><b> ヒント：</b>[!UICONTROL Inventory]/[!UICONTROL Deals] ビューの「[!UICONTROL Pacing & Budget]」列には、指定したフライト日とインプレッション目標に対する契約のペースが表示されます。 配信のペースがアンダーペーシングまたはオーバーペーシングの場合は、パブリッシャーに連絡して、契約を通じて送信される量を調整してください。 | 保証された取引：はい <br> 保証されていない取引：いいえ | はい |
| | [!UICONTROL Impressions] | （保証されていない取引の場合はオプション）この取引を使用して実行する予定の推定インプレッション数。 この値はトラッキング目的でのみ使用します。パブリッシャーは広告の配信を制御します。 | 保証された取引：はい <br> 保証されていない取引：いいえ | はい |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [&#x200B; 取引 ID の詳細の手動作成 &#x200B;](deal-id-create.md)
>* [SSP パートナー &#x200B;](ssp-partners.md)
>* [&#x200B; プライベートインベントリについて &#x200B;](private-inventory-about.md)
