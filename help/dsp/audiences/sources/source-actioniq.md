---
title: 「ユーザー ID をユニバーサル ID からユ  [!DNL ActionIQ]  ザ ID に変換」
description: DSPでファーストパーティセグメントを取り込む方法  [!DNL ActionIQ]  説明します。
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# ユーザー ID を [!DNL ActionIQ] からユニバーサル ID に変換

*Beta機能*

DSPと [!DNL ActionIQ] customer data platform の統合を使用すると、ターゲット広告のために、ハッシュ化されたメールアドレスをユニバーサル ID に変換できます。

[!DNL ActionIQ] からDSP<!-- NN --> データを共有するには、次の手順を実行します。

1. [DSPでオーディエンスソースを作成 ](#source-create) します。

1. ?

## 手順 1:DSPでのオーディエンスソースの作成 {#source-create}

1. [ オーディエンスソースを作成 ](source-manage.md) して、ユーザー識別子の変換先となる [ ユニバーサル ID 形式 ](source-about.md) を指定して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。

1. オーディエンスソースを作成したら、[!DNL ActionIQ] ユーザーとソースコードキーを共有します。

## 手順 2:

## 手順 3:

1. オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）でセグメントが入力されていることを確認し、ユニバーサル ID の数を元のハッシュ化されたメールアドレスの数と比較します。

   セグメントは、24 時間以内にDSPで使用可能になります。 DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「[ メール ID とユニバーサル ID の間のデータの相違 ](#universal-ids-data-variances) を参照してください。

セグメントは 24 時間ごとに更新されます。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「[ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com` に問い合わせてください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](source-manage.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Adobe Real-Time CDP]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Tealium]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
