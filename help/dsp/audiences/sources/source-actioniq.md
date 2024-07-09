---
title: '"ユーザー ID を次から変換 [!DNL ActionIQ] ユニバーサル ID へ」'
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL ActionIQ] ファーストパーティセグメント」を参照してください。
feature: DSP Audiences
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '269'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL ActionIQ] ユニバーサル ID に

*Beta機能*

とのDSP統合の使用 [!DNL ActionIQ] 顧客データプラットフォーム：ターゲット広告のために、ハッシュ化されたメールアドレスをユニバーサル ID に変換します。

次のものがあります <!-- NN --> からのデータ共有手順 [!DNL ActionIQ] DSPを使用する場合：

1. [DSPでのオーディエンスソースの作成](#source-create).

1. ?

## 手順 1:DSPでのオーディエンスソースの作成 {#source-create}

1. [オーディエンスソースの作成](source-manage.md) を指定して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 [ユニバーサル ID 形式](source-about.md) にユーザー識別情報を変換します。

1. オーディエンスソースを作成したら、ソースコードキーをと共有します。 [!DNL ActionIQ] ユーザー。

## 手順 2:

## 手順 3:

1. オーディエンスライブラリでの検証（オーディエンスの作成または編集時に使用できます） [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択し、ユニバーサル ID の数と元のハッシュ化されたメールアドレスの数を比較します。

   セグメントは、24 時間以内にDSPで使用可能になります。 DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「」を参照してください。[メール ID とユニバーサル ID のデータの相違](#universal-ids-data-variances).」と入力します。

セグメントは 24 時間ごとに更新されます。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「」を参照してください。[ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md).」と入力します。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [からのユーザー ID の変換 [!DNL Adobe Real-Time CDP] ユニバーサル ID に](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
