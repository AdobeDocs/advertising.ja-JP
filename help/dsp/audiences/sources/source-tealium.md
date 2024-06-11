---
title: からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL Tealium] ファーストパーティセグメント。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: 096ca9b5fce101995ca620b78f2ad8abf40355cd
workflow-type: tm+mt
source-wordcount: '1104'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL Tealium] ユニバーサル ID に

*ベータ版機能*

とのDSP統合の使用 [!DNL Tealium] 顧客データプラットフォーム：組織のファーストパーティのハッシュ化されたメールアドレスをターゲット広告のためにユニバーサル ID に変換します。 プロセスでは、 [!DNL Amazon Web Services] （AWS） firehose コネクタ。 Tealium からDSPにデータを共有するには、次の手順に従います。

1. （メールアドレスを変換： [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->、を使用する広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [有効化するトラッキングの設定 [!DNL Analytics] 測定](#analytics-tracking).

1. [DSPでのオーディエンスソースの作成](#source-create).

1. [セグメントマッピングデータの準備と共有](#map-data).

1. [でのコネクタの作成 [!DNL Tealium] セグメントデータを共有するには](#tealium-connector).

1. [内の既存のコネクタを複製 [!DNL Tealium] セグメントの共有を続行するには](#duplicate-connector).

1. [ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較](#compare-id-count).

セグメントは、24 時間以内にDSPで使用可能になり、24 時間ごとに更新されます。

## 手順 1：のトラッキングの設定 [!DNL Analytics] 測定 {#analytics-tracking}

*を使用した広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスをに変換するには [!DNL RampIDs] または [!DNL ID5] ID に関しては、次の手順を実行する必要があります。

1. （まだ完了していない場合）すべて完了 [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) また、次のことを確認します [AMO ID と EF ID](/help/integrations/analytics/ids.md) はトラッキング URL に入力されています。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **の場合 [!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへの変換に一致するように（モバイルアプリではなく）、web ページに追加の JavaScript タグをデプロイする必要があります。 Adobeアカウントチームにお問い合わせください。チームからは、に登録するための手順が示されます [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] 認証トラフィックソリューション。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [オーディエンスソースの作成](source-manage.md) オーディエンスをDSP アカウントまたは広告主アカウントに読み込みます。 ユーザー識別子を任意のに変換することもできます [使用可能なユニバーサル ID 形式](source-about.md).

   ソース設定には、自動生成されたソースキーが含まれ、セグメントマッピングデータの準備に使用されます。

1. オーディエンスソースを作成したら、ソースコードキーをと共有します。 [!DNL Tealium] ユーザー。

## 手順 3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. 広告主は、内でデータを準備する必要があります [!DNL Tealium]:

   1. SHA-256 アルゴリズムを使用して、広告主のオーディエンスのメール ID をハッシュ化します。

   1. ハッシュ化されたメール ID を含む列を、訪問者 ID タイプの属性にマッピングします。

   1. を使用したオーディエンスの作成 `Tealium_visitor_id` 属性。 適切なエンリッチメントを適用して、オーディエンスをトリガーに設定します。 を参照してください。 [[!DNL Tealium] 訪問者 ID 属性に関するドキュメント](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

1. DSPでセグメントを作成するには、広告主がセグメントマッピングデータをAdobeアカウントチームに提供する必要があります。 コンマ区切り値ファイルで、次の列名と値を使用します。

   * **外部セグメントキー：** 外部セグメントキー（後で、のコネクタのアクション設定で指定します） [!DNL Tealium]. 推奨される命名規則は「」です`<DSP source key>_<Tealium segment name>`例えば、「57bf424dc10_coffee-drinkers」などです。 DSP ソースキーには、を使用します [!UICONTROL Source Key] DSP オーディエンスソースの設定から。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的、ルール、またはその両方。

   * **親 ID :** 空白のままにする

   * **ビデオ CPM:** 0

   * **CPM を表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順 4：でのコネクタの作成 [!DNL Tealium] セグメントデータを共有するには {#tealium-connector}

共有するセグメントごとに、データの変化をトリガーするアクションごとに個別のコネクタを作成します。 例えば、それぞれが 2 つのトリガーを持つ 2 つのセグメントを共有するには、4 つのコネクタを作成します。

1. Adobeアカウントチームは、広告主にAWS firehose コネクタ資格情報を提供します。

1. 対象： [!DNL Tealium], [コネクタを追加](https://docs.tealium.com/server-side/connectors/add/)。使用するオプションは次のとおりです。

   1. 「」を選択します [!DNL AWS Firehose] コネクタ。

   1. ソース設定で、次の操作を行います。

      1. 共有するオーディエンスセグメントを選択します。

      1. トリガーを設定します。

         * セグメントの最初のコネクタには、トリガーを選択します `Joined Audience`. これにより、ユーザーがセグメントに参加するたびに、データがDSPと共有されます。

         * セグメントの 2 番目のコネクタには、トリガーを選択します `Left Audience`. このコネクタは、すべてのオプトアウトと、DSPでセグメントを離れるユーザーを処理するために使用されます。

   1. 設定で、AWS firehose コネクタを指定します。 DSP用の Firehose コネクタをまだ追加していない場合は、次の情報を使用して Firehose コネクタを追加します。

      * **名前：** コネクタの名前。

      * **アクセスキー：** Adobeアカウントチームから提供されたアクセスキー。

      * **秘密鍵：** Adobeアカウントチームから提供された秘密鍵。

      * **地域：** 米国東部バージニア州（米国東部–1）

   1. アクション設定で、次の操作を行います。

      1. 次の情報を使用して、「顧客データを配信ストリームに送信（詳細）」アクションを作成し、セグメントにデータを追加します。

         * **アクション名：** アクションの名前。

         * **アクションタイプ：** 顧客データを配信ストリームに送信（詳細）

         * **配信ストリーム :** Tealium_CDP_Connector

         * **メッセージデータ :**  次の手順を実行します。

            1. セグメントの属性を 1 つ選択します。

               * Hashed_Email 属性に、カスタムメッセージという名前を付けます `hashed_email`.

               * 「Cookies」属性に、カスタムメッセージという名前を付けます `cookies`.

            1. カスタムフィールドを作成するオプションの [!DNL Source Key] フィールドに、 [!UICONTROL External Segment Key] それはに含まれていた [セグメントマッピングデータ](#map-data) 前の手順で、

               DSPはこのキーを使用してセグメントにデータを入力します。

            1. （推奨）更新アクションを作成して、セグメントを最新の状態に保ちます。

## 手順 5：での既存のコネクタの複製 [!DNL Tealium] セグメントの共有を続行するには {#duplicate-connector}

セグメントごとに 1 つのコネクタと、コネクタごとに 1 つのセグメントのみを使用できます。

1. 対象： [!DNL Tealium]を選択し、別のセグメントを作成するセグメントを複製して、新しいセグメントの名前を変更します。

1. 対象： [!DNL Tealium]、複製 [作成したコネクタ](#tealium-connector) 前の手順で、新しいコネクタの名前を「」から変更します。`<original name>-copy`」を選択します。

## 手順 6：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

すべての手順を完了したら、オーディエンスライブラリ（からオーディエンスを作成または編集する際に使用可能）で検証します。 [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択した場合、24 時間以内にセグメントが入力されます。 ユニバーサル ID の数と、元のハッシュ化されたメールアドレスの数を比較します。

ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。 例えば、顧客データプラットフォームからハッシュ化されたメールアドレスを 100 個送信する場合は、90 個を超えるユニバーサル ID に翻訳する必要があります。 90% 以下の翻訳率が課題です。 セグメント数の変化について詳しくは、「」を参照してください[メール ID とユニバーサル ID のデータの相違の原因](#universal-ids-data-variances).」と入力します。

セグメントは 24 時間ごとに更新されます。 ただし、セグメントへの追加は、プライバシーコンプライアンスを確保するために 30 日後に有効期限が切れるので、オーディエンスを次から再度プッシュして更新します。 [!DNL Tealium] 30 日以内に 1 回。

トラブルシューティングのサポートについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
