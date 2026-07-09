---
title: ユーザーIDを [!DNL Tealium] からユニバーサル IDに変換
description: DSPで [!DNL Tealium]  ファーストパーティセグメントの取り込みを有効にする方法について説明します。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
TQID: https://experienceleague.adobe.com/X8mcqFiON6JMoB5KdS5Z0GVLYp-htw2ddCtmuZFflqo
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 50af5a8fc6e5e82268489259073e27911ca5a45c
workflow-type: tm+mt
source-wordcount: 1120
ht-degree: 0%

---

# ユーザーIDを[!DNL Tealium]からユニバーサル IDに変換

[!DNL Tealium] Customer Data PlatformとのDSP統合を使用して、組織の1st パーティハッシュ化されたメールアドレスを、ターゲット広告のユニバーサル IDに変換します。 このプロセスでは、[!DNL Amazon Web Services] （AWS） ファイアホースコネクタを使用します。 TealiumからDSPにデータを共有するには、次の手順に従います。

1. （電子メールアドレスを[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->に変換するには、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を持つ広告主） [ トラッキングを設定して [!DNL Analytics] 測定](#analytics-tracking)を有効にします。

1. [DSPでオーディエンスソースを作成](#source-create)。

1. [ セグメントマッピングデータの準備と共有](#map-data)。

1. [でコネクタを作成して [!DNL Tealium]  セグメントデータを共有](#tealium-connector)します。

1. [で既存のコネクタを複製して [!DNL Tealium]  セグメントを引き続き共有します](#duplicate-connector)。

1. [ ユニバーサル IDの数とハッシュ化された電子メールアドレスの数を比較](#compare-id-count)。

## 手順1: [!DNL Analytics]測定用トラッキングの設定 {#analytics-tracking}

*広告主と[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスを[!DNL RampIDs]または[!DNL ID5]のIDに変換するには、次の操作を行う必要があります。

1. （まだ実行していない場合）実装の[前提条件をすべて完了し、[AMO IDとEF ID](/help/integrations/analytics/ids.md)がトラッキング URLに入力されていることを確認します。 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)

1. ユニバーサル ID パートナーに登録し、web ページにユニバーサル ID固有のコードをデプロイして、デスクトップおよびモバイルのweb ブラウザー（モバイルアプリは除く）のIDからビュースルーのコンバージョンを一致させます。

   * **[!DNL RampIDs]の場合：** デスクトップおよびモバイル web ブラウザー（モバイルアプリではない）のIDからビュースルーに一致させるには、web ページにJavaScript タグを追加してデプロイする必要があります。 [!DNL LiveRamp]認証トラフィックソリューション（ats.js）から[!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順については、Adobe アカウントチームにお問い合わせください。 登録は無料ですが、契約書に署名する必要があります。 登録が完了すると、Adobeアカウントチームが独自のタグを生成し、web ページへの導入に使用します。

## 手順2:DSPでオーディエンスソースを作成する {#source-create}

1. [ オーディエンスソースを作成](source-manage.md)して、DSP アカウントまたは広告主アカウントにオーディエンスを読み込みます。 ユーザーIDを[使用可能なユニバーサル ID形式](source-about.md)のいずれかに変換することを選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントマッピングデータの準備に使用します。

1. オーディエンスソースを作成したら、ソースコードのキーを[!DNL Tealium] ユーザーと共有します。

## 手順3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. 広告主は、[!DNL Tealium]内のデータを準備する必要があります。

   1. SHA-256 アルゴリズムを使用して、広告主のオーディエンスのメール IDをハッシュ化します。

   1. ハッシュ化されたメール IDを含む列を、訪問者IDのタイプの属性にマッピングします。

   1. `Tealium_visitor_id`属性を使用してオーディエンスを作成します。 適切なエンリッチメントを適用してオーディエンスをトリガーにする： 訪問者ID属性](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/)に関する[[!DNL Tealium]  ドキュメントを参照してください。

1. 広告主は、DSPでセグメントを作成するために、Adobe アカウントチームにセグメントマッピングデータを提供する必要があります。 コンマ区切りの値ファイルでは、次の列名と値を使用します。

   * **外部セグメントキー：**&#x200B;外部セグメントキー。後で[!DNL Tealium]のコネクタのアクション設定で指定します。 推奨される命名規則は、「57bf424dc10_coffee-drinkers」のように「`<DSP source key>_<Tealium segment name>`」です。 DSP ソースキーの場合は、DSP オーディエンスソース設定の[!UICONTROL Source Key]を使用します。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的またはルール、またはその両方。

   * **親ID:**&#x200B;空白のままにする

   * **ビデオ CPM:** 0

   * **CPMの表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順4: [!DNL Tealium]でコネクタを作成してセグメントデータを共有する {#tealium-connector}

共有するセグメントごとに、データの変更をトリガーするアクションごとに個別のコネクタを作成します。 例えば、2つのセグメントをそれぞれ2つのトリガーで構成する場合は、4つのコネクタを作成します。

1. Adobe アカウントチームは、広告主にAWS ファイアホースコネクタの資格情報を提供します。

1. [!DNL Tealium]で、[次のオプションを使用してコネクタ ](https://docs.tealium.com/server-side/connectors/add/)を追加します。

   1. [!DNL AWS Firehose] コネクタを選択します。

   1. ソース設定で、次の操作を行います。

      1. 共有するオーディエンスセグメントを選択します。

      1. トリガーの設定：

         * セグメントの最初のコネクタで、トリガー `Joined Audience`を選択します。 これにより、ユーザーがセグメントに参加するたびに、データがDSPと共有されます。

         * セグメントの2番目のコネクタで、トリガー `Left Audience`を選択します。 このコネクタは、DSPでセグメントを離れるすべてのオプトアウトとユーザーを処理するために使用されます。

   1. 設定で、AWS ファイアホースコネクタを指定します。 DSP用のfirehose コネクタをまだ追加していない場合は、次の情報を使用してfirehose コネクタを追加します。

      * **名前：** コネクタの名前。

      * **アクセスキー：** Adobe アカウントチームが提供するアクセスキー。

      * **秘密鍵：** Adobe アカウントチームが提供する秘密鍵。

      * **地域：**&#x200B;米国東北バージニア州（us-east-1）

   1. アクション設定で、次の操作を行います。

      1. 「顧客データを配信ストリームに送信（詳細）」アクションを作成して、次の情報を使用してセグメントにデータを追加します。

         * **アクション名：** アクションの名前。

         * **アクションの種類：**&#x200B;顧客データを配信ストリームに送信（詳細）

         * **配信ストリーム：** Tealium_CDP_Connector

         * **メッセージデータ：**&#x200B;次の操作を行います。

            1. セグメントの属性を1つ選択します。

               * Hashed_Email属性に、カスタムメッセージに`hashed_email`という名前を付けます。

               * Cookie属性に、カスタムメッセージ `cookies`という名前を付けます。

            1. カスタムフィールドを作成するオプションで、[!DNL Source Key] フィールドに、前の手順で[ セグメントマッピングデータ ](#map-data)に含まれていた[!UICONTROL External Segment Key]を入力します。

               DSPはこのキーを使用してセグメントに情報を入力します。

            1. （推奨）更新アクションを作成して、セグメントを新鮮な状態に保ちます。

## 手順5: セグメントの共有を続行するには、[!DNL Tealium]の既存のコネクタを複製します {#duplicate-connector}

1つのセグメントにつき1つのコネクタのみを使用し、1つのコネクタにつき1つのセグメントのみを使用できます。

1. [!DNL Tealium]で、別のセグメントを作成するセグメントを複製し、新しいセグメントの名前を変更します。

1. [!DNL Tealium]で、前の手順で作成したコネクタ [を複製し、新しいコネクタの名前を「`<original name>-copy`」から新しいセグメント名に変更します。](#tealium-connector)

## 手順6：ユニバーサル IDの数とハッシュ化されたメールアドレスの数を比較する {#compare-id-count}

これらのセグメントは、24時間以内にDSPで利用できるようになります。 DSPがセグメントデータを受け取った後、オーディエンスサイズは9時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用可能）で、セグメントが入力されていることを確認し、ユニバーサル IDの数と元のハッシュ化されたメールアドレスの数を比較します。 使用可能なIDの翻訳率と、セグメント数が異なる理由については、「[ メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

セグメントは24時間ごとに更新されます。 ただし、セグメントに含めるには、デフォルトで30日が経過するか、顧客が指定した有効期限が経過した後に有効期限が切れます。 有効期限が切れる前に[!DNL Tealium]からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobe アカウントチームにお問い合わせください。

## トラブルシューティング

翻訳率とユーザー数の問題をトラブルシューティングするには、「[ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

変換手順に関する問題をトラブルシューティングするには、Adobe アカウントチームまたは`adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [ オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
