---
title: 手動取引ID設定
description: 手動で入力された案件IDの設定の説明を参照してください。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 9d3417cb-8b44-4f1c-afc4-eea6a2e5b9d7
TQID: https://experienceleague.adobe.com/1jcBNsmB8-5zM6udv9o3mILo70vOGrzZxEwPM62LPs0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 518
ht-degree: 0%

---

# 手動取引ID設定

| セクション | パラメーター | 説明 | 必須 | 編集可能 |
|---------|-----------|-------------|----------|----------|
| [取引の詳細] | [!UICONTROL Deal name] | Advertising DSPで[!UICONTROL Deal ID]を識別する名前。 名前を入力するか、**[!UICONTROL Auto-name]**&#x200B;を選択して、DSPが契約の詳細に基づいて名前を生成できるようにします。<br><br>自動生成された名前の例：`[!DNL 24159708 - Deal ID - Guaranteed Fixed - USD - 5 - 24Kitchen - Private]` | はい | はい |
| | [!UICONTROL External deal ID] | この取引を識別するためにパブリッシャーとSSPが使用するID。 | はい | いいえ |
| | [!UICONTROL Publisher] | この在庫を販売している発行者の名前。 | はい | いいえ |
| | [!UICONTROL SSP] | この取引を実行するサプライサイドプラットフォーム（SSP）。 | はい | いいえ |
| | [!UICONTROL Media type] | この契約で購入したメディアの種類：*[!UICONTROL Desktop video]*、*[!UICONTROL Mobile video]*、*[!UICONTROL Connected TV]*、*[!UICONTROL Display]*、*[!UICONTROL Audio]*、または&#x200B;*[!UICONTROL Publisher Managed]*。 オプションはSSPによって異なります。<br><br>取引で複数のメディアタイプが許可されている場合は、取引の作成時にデフォルトのプレースメントのメディアタイプを選択します。 後で、値を変更するか、追加のメディアタイプ [で新しいプレースメントを](deal-id-attach-placements.md) アタッチするだけです。<!-- It would be ideal if this field was multi-select rather than a radio button, so you don't have to "change" the value later. --> | はい | いいえ |
| | [!UICONTROL Deal type] | 契約のコミットメントと価格構造：<br><ul><li>*[!UICONTROL Non guaranteed (floor)]*：あなたとパブリッシャーは、インプレッション配信の数が固定されていません。 この取引は、在庫の最低価格を規定していますが、CPMは市場の状況によって変動し、増加する可能性があります。</li><li>*[!UICONTROL Non guaranteed (fixed)]*：あなたとパブリッシャーは、インプレッション配信の数が固定されていません。 価格は交渉済みの固定レートで設定されています。</li><li>*[!UICONTROL Guaranteed (fixed)]*：お客様とパブリッシャーは、事前に定義されたインプレッション数、ターゲティング、フライト日、および固定価格について合意しました。<br><br><b>注意：</b>保証された契約には、フライト日と[!UICONTROL Tracking] セクションで指定された数のインプレッションが必要です。 また、取引のデフォルトのプログラマティック保証（PG）プレースメントを作成する必要があり、オプションで他のプレースメントに取引を使用することもできます。</li></ul> | はい | いいえ |
| | [!UICONTROL CPM] | 1000 インプレッションあたりの交渉済みコスト（CPM）。 | はい | はい |
| | [通貨] | 取引の通貨。<br><br>すべてのSSPがUSDでの取引を受け付けています。 SSPがDSP アカウントの通貨を受け入れると、その通貨も使用可能になります。 | はい | いいえ |
| | [!UICONTROL Billing method] | すべての案件IDは[!DNL Adobe]件の資金調達および請求済みです。 DSPは、利用可能なあらゆるメディアベンダーに利用状況に基づいて支払いを行い、ベンダーとの不一致を管理し、一括請求書をアカウントに送信します。 このオプションには、アカウントのレートカードに記載されている追加料金が発生します。 | はい | いいえ |
| [!UICONTROL Advertisers] | [!UICONTROL Account email] | 取引にアクセスできるユーザーアカウントの電子メールアドレス。 | いいえ | はい |
| | [!UICONTROL Advertisers that can access this deal] | この契約にアクセスできるアカウント内の特定の広告主。<br><br><b>注：</b> [!UICONTROL Deals] ビューから、追加アカウントの広告主と契約を共有できます。 取引行で「**[!UICONTROL #]**」をクリックし、「**[!UICONTROL share]**」をクリックしてから、電子メールアドレスと取引を共有します。 | はい | はい |
| [!UICONTROL Tracking] | [!UICONTROL Flight Dates] | この取引を使用したトラフィックの開始日と終了日。 これらの日付は追跡目的でのみ使用され、広告配信には影響しません。<br><br><b> ヒント：</b> [!UICONTROL Inventory] > [!UICONTROL Deals] ビューでは、[!UICONTROL Pacing & Budget]列に、指定されたフライト日とインプレッション目標に対する契約のペースが表示されます。 配信の量が不足している場合や、ペースが過剰な場合は、メディア企業に連絡して、成約を通じて送信する配信数を調整してください。 | 保証されたお得な情報：はい<br>保証されていない情報：いいえ | はい |
| | [!UICONTROL Impressions] | （保証されていない契約の場合はオプション）この契約を使用して実行するインプレッションの推定数。 この値は追跡目的でのみ使用されます。パブリッシャーは広告の配信を制御します。 | 保証されたお得な情報：はい<br>保証されていない情報：いいえ | はい |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [取引IDの詳細を手動で作成する](deal-id-create.md)
>* [SSP パートナー](ssp-partners.md)
>* [&#x200B; プライベートインベントリについて](private-inventory-about.md)
