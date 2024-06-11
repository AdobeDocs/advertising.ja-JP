---
title: からのユーザー ID の変換 [!DNL Optimizely] ユニバーサル ID に
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL Optimizely] ファーストパーティセグメント。
feature: DSP Audiences
source-git-commit: 23d4dc50d1c6bf966148dab772e0e770087ac869
workflow-type: tm+mt
source-wordcount: '616'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL Optimizely] ユニバーサル ID に

*ベータ版機能*

とのDSP統合の使用 [!DNL Optimizely] 顧客データプラットフォーム：組織のファーストパーティのハッシュ化されたメールアドレスをターゲット広告のためにユニバーサル ID に変換します。

1. （メールアドレスを変換： [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->、を使用する広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [有効化するトラッキングの設定 [!DNL Analytics] 測定](#analytics-tracking).

1. [DSPでのオーディエンスソースの作成](#source-create).

1. [セグメントデータの準備とプッシュ](#push-data).

1. [ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較](#compare-id-count).

## 手順 1：のトラッキングの設定 [!DNL Analytics] 測定 {#analytics-tracking}

*を使用した広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスをに変換するには [!DNL RampIDs] または [!DNL ID5] ID に関しては、次の手順を実行する必要があります。

1. （まだ完了していない場合）すべて完了 [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) また、次のことを確認します [AMO ID と EF ID](/help/integrations/analytics/ids.md) はトラッキング URL に入力されています。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **の場合 [!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへの変換に一致するように（モバイルアプリではなく）、web ページに追加の JavaScript タグをデプロイする必要があります。 Adobeアカウントチームにお問い合わせください。チームからは、に登録するための手順が示されます [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] 認証トラフィックソリューション。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [オーディエンスソースの作成](source-manage.md) オーディエンスをDSP アカウントまたは広告主アカウントに読み込みます。 ユーザー識別子を任意のに変換することもできます [使用可能なユニバーサル ID 形式](source-about.md).

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用されます。

1. オーディエンスソースを作成したら、ソースコードキーをと共有します。 [!DNL Optimizely] ユーザー。

## 手順 3：セグメントデータの準備とプッシュ {#push-data}

広告主は、次の方法でデータを準備し、プッシュする必要があります [!DNL Optimizely] 代表者。

1. 内 [!DNL Optimizely Data Platform]は、SHA-256 アルゴリズムを使用して、広告主のオーディエンスのメール ID をハッシュ化します。

1. 広告主に連絡 [!DNL Optimizely] セグメントをDSPにプッシュする手順の担当者。 セグメントをプッシュする際には、次の情報を含めます。

   * **ソースキー：** これは、で作成されたソースキーです。 [手順 2](#source-create).

   * **アカウント コード：** これは、DSP内の次の場所にある、英数字のDSP アカウントコードです。 [!UICONTROL Settings] > [!UICONTROL Account].

セグメントは、24 時間以内にDSPで使用可能になり、広告主に設定されたとおりに更新されます。 セグメントの更新頻度に関係なく、プライバシーコンプライアンスを確保するためにセグメントへの追加の有効期限が 30 日後に切れるので、オーディエンスをから再プッシュしてオーディエンスを更新します。 [!DNL Optimizely] 30 日以内に 1 回。

<!--
Are they using the Data Platform web services, another type of API, or a UI? Add a link to instructions, including how to designate DSP as the destination. And where will they input the DSP-specific fields?]
-->

## 手順 4：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

すべての手順を完了したら、オーディエンスライブラリ（からオーディエンスを作成または編集する際に使用可能）で検証します。 [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択した場合、セグメントが使用可能になり、24 時間以内に入力されます。 ユニバーサル ID の数と、元のハッシュ化されたメールアドレスの数を比較します。

ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。 例えば、顧客データプラットフォームからハッシュ化されたメールアドレスを 100 個送信する場合は、90 個を超えるユニバーサル ID に翻訳する必要があります。 90% 以下の翻訳率が課題です。 セグメント数の変化について詳しくは、「」を参照してください[メール ID とユニバーサル ID のデータの相違の原因](#universal-ids-data-variances).」と入力します。

トラブルシューティングのサポートについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
