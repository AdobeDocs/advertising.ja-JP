---
title: 約[!UICONTROL CCPA Opt-out-of-Sale]個のセグメントとレポート
description: CCPA オプトアウトのリクエストからIDを追跡するためのセグメントの作成と、IDのレポートを取得する方法について説明します。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
TQID: 'https://experienceleague.adobe.com/Bp8Fj0z7lqSXmHd-aJQa6ocQyj6FVQuydArNBucpJp4'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 2b670c6e-542a-5afe-b96b-d9ce7818cd55
    internal-label: DSP Segments
  - id: b2025470-04ef-4dd9-bdd4-44407644aeb6
    internal-label: Compliance
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
    internal-label: Segments
  - id: c867fa1b-f589-43fa-b071-3c62f0038f23
    internal-label: CCPA
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '274'
ht-degree: 0%
---
# 約[!UICONTROL CCPA Opt-out-of-Sale]個のセグメントとレポート

ユーザーIDは、カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイト上の消費者オプトアウトの要求から、[CCPA オプトアウトの販売セグメントを作成して実装することで](ccpa-opt-out-segment-create.md)追跡できます。 ユーザーはCCPAの販売不可セグメントに無期限で残ります。

セグメントピクセルタグが実装されると、Adobe Advertisingは広告主の代わりにID プールの収集を開始します。

## 消費者の販売拒否レポート

Adobe Advertisingは、お客様がアカウントのオプトアウト要求を送信したIDの月次レポートを生成します。 このデータは、DSPで作成されたCCPAのオプトアウトオブセールセグメントと、Privacy Service APIを介して送信された送信を使用してキャプチャされたリクエストを統合します。  レポートは、前月の各月の最初に生成されます。 例えば、6月の月間ユーザーリストは7月1日に利用できます。

各レポートは、GZIP形式に圧縮されたタブ区切りのテキストファイルとして使用できます。 CCPAのオプトアウトオブセールスセグメントで取得されたユーザーIDは、セグメントおよび広告主によって識別されます。

DSP内またはDSP [!DNL Trafficking API]を使用して、過去3か月間に作成された月次レポート [&#128279;](ccpa-opt-out-segment-report-retrieve.md)へのリンクを取得できます。 各リンクは7日間有効ですが、顧客が取得するたびに更新されます。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのカリフォルニア州消費者プライバシー法に対するサポート：消費者の販売拒否サポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [消費者のオプトアウトに関するレポートを取得](ccpa-opt-out-segment-report-retrieve.md)
>* [&#x200B; オーディエンス管理について](audience-about.md)
