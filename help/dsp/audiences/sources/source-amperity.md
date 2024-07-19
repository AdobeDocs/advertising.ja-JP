---
title: ユーザー ID をユニバーサル ID [!DNL Amperity]  からユニバーサル ID に変換
description: DSPでファーストパーティセグメントを取り込む方法  [!DNL Amperity]  説明します。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '697'
ht-degree: 0%

---

# ユーザー ID を [!DNL Amperity] からユニバーサル ID に変換

*Beta機能*

DSPと [!DNL Amperity] customer data platform の統合を使用すると、組織のファーストパーティのハッシュ化されたメールアドレスを、ターゲット広告のためのユニバーサル ID に変換できます。

1. （メールアドレスを [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> に変換するには：[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主） [ トラッキングを設定して有効  [!DNL Analytics]  測定 ](#analytics-tracking) します。

1. [DSPでオーディエンスソースを作成 ](#source-create) します。

1. [ セグメントマッピングデータの準備と共有 ](#map-data)。

1. [DSPからのデータのプッシュ  [!DNL Amperity]  リクエスト ](#push-data)。

1. [ ユニバーサル ID の数とハッシュ化されたメールアドレスの数を比較 ](#compare-id-count)。

## 手順 1:[!DNL Analytics] 測定のトラッキングの設定 {#analytics-tracking}

*[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主）*

メールアドレスを [!DNL RampIDs] ID または [!DNL ID5] ID に変換するには、次の手順を実行する必要があります。

1. （まだ行っていない場合）すべての [ 実装の前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) を完了し、[AMO ID と EF ID](/help/integrations/analytics/ids.md) がトラッキング URL に入力されていることを確認します。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **[!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへのコンバージョンに一致するように、web ページに追加のJavaScript タグをデプロイする必要があります（モバイルアプリは除く）。 Adobeアカウントチームに問い合わせてください。このチームには、[!DNL LiveRamp] Authentication Traffic Solutions の [!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順が記載されています。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [ オーディエンスソースを作成 ](source-manage.md) して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 ユーザー識別子を任意の [ 使用可能なユニバーサル ID 形式 ](source-about.md) に変換するよう選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用されます。

1. オーディエンスソースを作成したら、[!DNL Amperity] ユーザーとソースコードキーを共有します。

## 手順 3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. [!DNL Amperity] 内で、SHA-256 アルゴリズムを使用して、オーディエンスのメール ID をハッシュ化します。

1. DSPでセグメントを作成するには、広告主がセグメントマッピングデータをAdobeアカウントチームに提供する必要があります。 コンマ区切り値ファイルで、次の列名と値を使用します。

   * **外部セグメントキー：** セグメントに関連付けられた [!DNL Amperity] 部セグメントキー。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的、ルールまたはその両方。

   * **親 ID:** 空白のままにします

   * **ビデオ CPM:** 0

   * **CPM を表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順 4:[!DNL Amperity] からDSPへのデータプッシュをリクエストする {#push-data}

1. DSP内でセグメントがマッピングされたら、広告主は [!DNL Amperity] の担当者と協力してセグメントデータをDSPに配信する必要があります。

1. 次に、広告主は、セグメントデータが受信されたことをAdobeアカウントチームに確認する必要があります。

セグメントは、24 時間以内にDSPで使用可能になります。 オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）で、セグメントが使用可能であり、データが入力されていることを確認します。

セグメントは、[!DNL Amperity] 内で広告主に対して設定されたとおりに更新されます。 セグメントの更新頻度に関係なく、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に期限切れになります。 有効期限が切れる前に [!DNL Amperity] からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

## 手順 5：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する際に使用できる）で、ユニバーサル ID の数を元のハッシュ化されたメールアドレスの数と比較します。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「[ メール ID とユニバーサル ID の間のデータの相違 ](#universal-ids-data-variances) を参照してください。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「[ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com` に問い合わせてください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](source-manage.md)
>* [ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
