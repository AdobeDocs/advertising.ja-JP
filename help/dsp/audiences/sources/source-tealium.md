---
title: ユーザー ID をユニバーサル ID [!DNL Tealium]  からユニバーサル ID に変換
description: DSPでファーストパーティセグメントを取り込む方法  [!DNL Tealium]  説明します。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '1092'
ht-degree: 0%

---

# ユーザー ID を [!DNL Tealium] からユニバーサル ID に変換

*Beta機能*

DSPと [!DNL Tealium] customer data platform の統合を使用すると、組織のファーストパーティのハッシュ化されたメールアドレスを、ターゲット広告のためのユニバーサル ID に変換できます。 このプロセスでは、[!DNL Amazon Web Services] （AWS） firehose コネクタを使用します。 Tealium からDSPにデータを共有するには、次の手順に従います。

1. （メールアドレスを [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> に変換するには：[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主） [ トラッキングを設定して有効  [!DNL Analytics]  測定 ](#analytics-tracking) します。

1. [DSPでオーディエンスソースを作成 ](#source-create) します。

1. [ セグメントマッピングデータの準備と共有 ](#map-data)。

1. [ セグメントデータを共有するため  [!DNL Tealium]  にコネクタを作成します ](#tealium-connector)。

1. [ セグメントの共有を続行するには  [!DNL Tealium]  既存のコネクタを内で複製します ](#duplicate-connector)。

1. [ ユニバーサル ID の数とハッシュ化されたメールアドレスの数を比較 ](#compare-id-count)。

## 手順 1:[!DNL Analytics] 測定のトラッキングの設定 {#analytics-tracking}

*[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主）*

メールアドレスを [!DNL RampIDs] ID または [!DNL ID5] ID に変換するには、次の手順を実行する必要があります。

1. （まだ行っていない場合）すべての [ 実装の前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) を完了し、[AMO ID と EF ID](/help/integrations/analytics/ids.md) がトラッキング URL に入力されていることを確認します。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **[!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへのコンバージョンに一致するように、web ページに追加のJavaScript タグをデプロイする必要があります（モバイルアプリは除く）。 Adobeアカウントチームに問い合わせてください。このチームには、[!DNL LiveRamp] Authentication Traffic Solutions の [!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順が記載されています。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [ オーディエンスソースを作成 ](source-manage.md) して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 ユーザー識別子を任意の [ 使用可能なユニバーサル ID 形式 ](source-about.md) に変換するよう選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントマッピングデータの準備に使用されます。

1. オーディエンスソースを作成したら、[!DNL Tealium] ユーザーとソースコードキーを共有します。

## 手順 3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. 広告主は、[!DNL Tealium] 内でデータを準備する必要があります。

   1. SHA-256 アルゴリズムを使用して、広告主のオーディエンスのメール ID をハッシュ化します。

   1. ハッシュ化されたメール ID を含む列を、訪問者 ID タイプの属性にマッピングします。

   1. `Tealium_visitor_id` 属性を持つオーディエンスを作成します。 適切なエンリッチメントを適用して、オーディエンスをトリガーに設定します。 詳しくは、[[!DNL Tealium]  訪問者 ID 属性に関するドキュメント ](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/) を参照してください。

1. DSPでセグメントを作成するには、広告主がセグメントマッピングデータをAdobeアカウントチームに提供する必要があります。 コンマ区切り値ファイルで、次の列名と値を使用します。

   * **外部セグメントキー：** 外部セグメントキー。後で [!DNL Tealium] のコネクタのアクション設定で指定します。 推奨される命名規則は「`<DSP source key>_<Tealium segment name>`」（「57bf424dc10_coffee-drinkers」など）です。 DSP ソースキーには、DSP オーディエンスソース設定の [!UICONTROL Source Key] を使用します。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的、ルールまたはその両方。

   * **親 ID:** 空白のままにします

   * **ビデオ CPM:** 0

   * **CPM を表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順 4:[!DNL Tealium] でコネクタを作成して、セグメントデータを共有する {#tealium-connector}

共有するセグメントごとに、データの変化をトリガーするアクションごとに個別のコネクタを作成します。 例えば、それぞれが 2 つのトリガーを持つ 2 つのセグメントを共有するには、4 つのコネクタを作成します。

1. Adobeアカウントチームは、広告主にAWS firehose コネクタ資格情報を提供します。

1. ま [!DNL Tealium]、次のオプションを使用して [ コネクタを追加 ](https://docs.tealium.com/server-side/connectors/add/) します。

   1. [!DNL AWS Firehose] コネクタを選択します。

   1. ソース設定で、次の操作を行います。

      1. 共有するオーディエンスセグメントを選択します。

      1. トリガーを設定します。

         * セグメントの最初のコネクタに対して、トリガー`Joined Audience` を選択します。 これにより、ユーザーがセグメントに参加するたびに、データがDSPと共有されます。

         * セグメントの 2 番目のコネクタには、トリガー`Left Audience` を選択します。 このコネクタは、すべてのオプトアウトと、DSPでセグメントを離れるユーザーを処理するために使用されます。

   1. 設定で、AWS firehose コネクタを指定します。 DSP用の Firehose コネクタをまだ追加していない場合は、次の情報を使用して Firehose コネクタを追加します。

      * **Name:** コネクタの名前。

      * **アクセスキー：** Adobeアカウントチームから提供されたアクセスキー。

      * **秘密鍵：** Adobeアカウントチームから提供された秘密鍵。

      * **地域：** 米国東部バージニア州（us-east-1）

   1. アクション設定で、次の操作を行います。

      1. 次の情報を使用して、「顧客データを配信ストリームに送信（詳細）」アクションを作成し、セグメントにデータを追加します。

         * **アクション名：** アクションの名前。

         * **アクションタイプ：** 顧客データを配信ストリームに送信（詳細）

         * **配信ストリーム：** Tealium_CDP_Connector

         * **メッセージデータ：** 次の手順を実行します。

            1. セグメントの属性を 1 つ選択します。

               * Hashed_Email 属性には、カスタムメッセージに `hashed_email` という名前を付けます。

               * 「Cookies」属性に、カスタムメッセージに `cookies` という名前を付けます。

            1. カスタムフィールドを作成するオプションの「[!DNL Source Key]」フィールドに、前の手順で [ セグメントマッピングデータ ](#map-data) に含めた [!UICONTROL External Segment Key] を入力します。

               DSPはこのキーを使用してセグメントにデータを入力します。

            1. （推奨）更新アクションを作成して、セグメントを最新の状態に保ちます。

## 手順 5：既存のコネクタを複製して [!DNL Tealium] セグメントの共有を続行 {#duplicate-connector}

セグメントごとに 1 つのコネクタと、コネクタごとに 1 つのセグメントのみを使用できます。

1. [!DNL Tealium] で、別のセグメントを作成するセグメントを複製し、新しいセグメントの名前を変更します。

1. [!DNL Tealium] では、前の手順で [ 作成したコネクタ ](#tealium-connector) を複製し、新しいコネクタの名前を「`<original name>-copy`」から新しいセグメント名に変更します。

## 手順 6：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

セグメントは、24 時間以内にDSPで使用可能になります。 DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）でセグメントが入力されていることを確認し、ユニバーサル ID の数を元のハッシュ化されたメールアドレスの数と比較します。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「[ メール ID とユニバーサル ID の間のデータの相違 ](#universal-ids-data-variances) を参照してください。

セグメントは 24 時間ごとに更新されます。 ただし、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に有効期限が切れます。 有効期限が切れる前に [!DNL Tealium] からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「[ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com` に問い合わせてください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](source-manage.md)
>* [ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
