---
title: からのユーザー ID の変換 [!DNL Amperity] ユニバーサル ID に
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL Amperity] ファーストパーティセグメント。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: ed74f3fa3d0036e0dc8a529b05452567527f68a1
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL Amperity] ユニバーサル ID に

*Beta機能*

とのDSP統合の使用 [!DNL Amperity] 顧客データプラットフォーム：組織のファーストパーティのハッシュ化されたメールアドレスをターゲット広告のためにユニバーサル ID に変換します。

1. （メールアドレスを変換： [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->、を使用する広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [有効化するトラッキングの設定 [!DNL Analytics] 測定](#analytics-tracking).

1. [DSPでのオーディエンスソースの作成](#source-create).

1. [セグメントマッピングデータの準備と共有](#map-data).

1. [からのデータプッシュをリクエスト [!DNL Amperity] DSPへ](#push-data).

1. [ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較](#compare-id-count).

## 手順 1：のトラッキングの設定 [!DNL Analytics] 測定 {#analytics-tracking}

*を使用した広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスをに変換するには [!DNL RampIDs] または [!DNL ID5] ID に関しては、次の手順を実行する必要があります。

1. （まだ完了していない場合）すべて完了 [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) また、次のことを確認します [AMO ID と EF ID](/help/integrations/analytics/ids.md) はトラッキング URL に入力されています。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **の場合 [!DNL RampIDs]:** デスクトップブラウザーとモバイル web ブラウザー（モバイルアプリではない）の ID からビュースルーへのコンバージョンに一致させるために、web ページに追加のJavaScript タグをデプロイする必要があります。 Adobeアカウントチームにお問い合わせください。チームからは、に登録するための手順が示されます [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] 認証トラフィックソリューション。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [オーディエンスソースの作成](source-manage.md) オーディエンスをDSP アカウントまたは広告主アカウントに読み込みます。 ユーザー識別子を任意のに変換することもできます [使用可能なユニバーサル ID 形式](source-about.md).

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用されます。

1. オーディエンスソースを作成したら、ソースコードキーをと共有します。 [!DNL Amperity] ユーザー。

## 手順 3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. 内 [!DNL Amperity]は、SHA-256 アルゴリズムを使用してオーディエンスのメール ID をハッシュ化します。

1. DSPでセグメントを作成するには、広告主がセグメントマッピングデータをAdobeアカウントチームに提供する必要があります。 コンマ区切り値ファイルで、次の列名と値を使用します。

   * **外部セグメントキー：** この [!DNL Amperity] セグメントに関連付けられたセグメントキー。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的、ルール、またはその両方。

   * **親 ID :** 空白のままにする

   * **ビデオ CPM:** 0

   * **CPM を表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順 4：からのデータプッシュをリクエストする [!DNL Amperity] DSPへ {#push-data}

1. DSP内でセグメントがマッピングされたら、広告主は自分で作業する必要があります [!DNL Amperity] セグメントデータをDSPに配信する担当者。

1. 次に、広告主は、セグメントデータが受信されたことをAdobeアカウントチームに確認する必要があります。

セグメントは、24 時間以内にDSPで使用可能になります。 オーディエンスライブラリでの検証（オーディエンスの作成または編集時に使用できます） [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択した場合、セグメントが使用可能になり、データが入力されます。

内の広告主向けに設定されたとおりにセグメントが更新されます [!DNL Amperity]. セグメントの更新頻度に関係なく、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に期限切れになります。 から再プッシュしてセグメントを更新 [!DNL Amperity] 有効期限の前。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

## 手順 5：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。 オーディエンスライブラリで（オーディエンスを作成または編集する際に使用できます） [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）で、ユニバーサル ID の数と元のハッシュ化されたメールアドレスの数を比較します。

ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。この翻訳率は [!DNL RampIDs] ハッシュ化されたメールアドレスがすべて一意の場合、特に 95% である必要があります。 例えば、ハッシュ化されたメールアドレスが 100 個ある場合は、少なくとも 95 個に翻訳する必要があります [!DNL RampIDs] または、90 を超えるその他のタイプのユニバーサル ID。 翻訳率の低下が問題です。 セグメント数の変化について詳しくは、「」を参照してください[メール ID とユニバーサル ID のデータの相違の原因](#universal-ids-data-variances).」と入力します。

トラブルシューティングのサポートについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
