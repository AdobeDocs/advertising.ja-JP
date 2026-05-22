---
title: ユーザーIDを [!DNL ActionIQ] からユニバーサル IDに変換
description: DSPで [!DNL ActionIQ]  ファーストパーティセグメントの取り込みを有効にする方法について説明します。
feature: DSP Audiences
source-git-commit: 14a4d5b0bbe27697668b4a1a8eb3a7f74a18cc04
workflow-type: tm+mt
source-wordcount: '265'
ht-degree: 0%

---

# ユーザーIDを[!DNL ActionIQ]からユニバーサル IDに変換

[!DNL ActionIQ] Customer Data PlatformとのDSP統合を使用して、ターゲット広告のためにハッシュ化された電子メールアドレスをユニバーサル IDに変換します。

[!DNL ActionIQ]のデータをDSPと共有するには、<!-- NN -->の手順があります。

1. [DSPでオーディエンスソースを作成](#source-create)。

1. ?

## 手順1:DSPでオーディエンスソースを作成する {#source-create}

1. [ オーディエンスソース ](source-manage.md)を作成して、ユーザーIDを変換する[ ユニバーサル ID形式](source-about.md)を指定して、DSP アカウントまたは広告主アカウントにオーディエンスを読み込みます。

1. オーディエンスソースを作成したら、ソースコードのキーを[!DNL ActionIQ] ユーザーと共有します。

## ステップ 2:

## ステップ 3:

1. オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用可能）で、セグメントが入力されていることを確認し、ユニバーサル IDの数と元のハッシュ化されたメールアドレスの数を比較します。

   これらのセグメントは、24時間以内にDSPで利用できるようになります。 DSPがセグメントデータを受け取った後、オーディエンスサイズは9時間以内に表示されます。 使用可能なIDの翻訳率と、セグメント数が異なる理由については、「[ メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

セグメントは24時間ごとに更新されます。

## トラブルシューティング

翻訳率とユーザー数の問題をトラブルシューティングするには、「[ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

変換手順に関する問題をトラブルシューティングするには、Adobe アカウントチームまたは`adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [ オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [ ユーザーIDを [!DNL Adobe Real-Time CDP] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [ ユーザーIDを [!DNL Tealium] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-tealium.md)
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
