---
title: '"ユーザー ID を次から変換 [!DNL ActionIQ] ユニバーサル ID へ」'
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL ActionIQ] ファーストパーティセグメント」を参照してください。
feature: DSP Audiences
source-git-commit: bd0586516c2457e4dfcd1a23046707e8bf652e3b
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL ActionIQ] ユニバーサル ID に

*ベータ版機能*

とのDSP統合の使用 [!DNL ActionIQ] 顧客データプラットフォーム：ターゲット広告のために、ハッシュ化されたメールアドレスをユニバーサル ID に変換します。

次のものがあります <!-- NN --> からのデータ共有手順 [!DNL ActionIQ] DSPを使用する場合：

1. [DSPでのオーディエンスソースの作成](#source-create).

1. ?

## 手順 1:DSPでのオーディエンスソースの作成 {#source-create}

1. [オーディエンスソースの作成](source-create.md) を指定して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 [ユニバーサル ID 形式](source-about.md) にユーザー識別情報を変換します。

1. オーディエンスソースを作成したら、ソースコードキーをと共有します。 [!DNL ActionIQ] ユーザー。

1. すべての手順を完了したら、オーディエンスライブラリ（からオーディエンスを作成または編集する際に使用可能）で検証します。 [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択した場合、24 時間以内にセグメントが入力されます。 ユニバーサル ID の数と、元のハッシュ化されたメールアドレスの数を比較します。

   ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。 例えば、顧客データプラットフォームからハッシュ化されたメールアドレスを 100 個送信する場合は、90 個を超えるユニバーサル ID に翻訳する必要があります。 90% 以下の翻訳率が課題です。 セグメント数の変化について詳しくは、「」を参照してください[メール ID とユニバーサル ID のデータの相違の原因](#universal-ids-data-variances).」と入力します。

   トラブルシューティングのサポートについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

セグメントは 24 時間ごとに更新されます。

## 手順 2:

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを作成してユニバーサル ID オーディエンスを有効化](source-create.md)
>* [オーディエンスソース設定](source-settings.md)
>* [からのユーザー ID の変換 [!DNL Adobe Real-Time CDP] ユニバーサル ID に](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)

<!--
>* [Convert User IDs from [!DNL Optimizely] to Universal IDs](/help/dsp/audiences/sources/source-optimizely.md)
-->
