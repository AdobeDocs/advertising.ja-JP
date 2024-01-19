---
title: とのDSP統合を使用する際のワークフロー [!DNL Tealium]
description: DSPが [!DNL Tealium] ファーストパーティセグメント。
feature: DSP Audiences
exl-id: 100abbe7-e228-4eb6-a5b9-bf74e83b3aa2
source-git-commit: b94541bf8675d535b2f19b26c05235eb56bc6c0b
workflow-type: tm+mt
source-wordcount: '678'
ht-degree: 0%

---

# とのDSP統合を使用する際のワークフロー [!DNL Tealium]

組織のファーストパーティデータを [!DNL Tealium] 顧客データプラットフォーム [!DNL Amazon Web Services] (AWS) 消防コネクタ Tealium のデータをDSPと共有するには、次の 4 つの手順があります。

1. [DSPでのオーディエンスソースの作成](#source-create).

1. [セグメントマッピングデータの準備と共有](#map-data).

1. [でのコネクタの作成 [!DNL Tealium] セグメントデータを共有するには](#tealium-connector).

1. [で既存のコネクタを複製します。 [!DNL Tealium] セグメントを共有し続けるには](#duplicate-connector).

## 手順 1:DSPでのオーディエンスソースの作成 {#source-create}

* [オーディエンスソースの作成](source-create.md) オーディエンスをDSPアカウントまたは広告主アカウントにインポートし、ソースコードキーを [!DNL Tealium] ユーザー。

## 手順 2：セグメントマッピングデータの準備と共有 {#map-data}

1. 広告主は、セグメントマッピングデータを準備して共有する必要があります。

   1. 広告主は、内でデータを準備する必要があります [!DNL Tealium]:

      1. 広告主のオーディエンスの電子メール ID は、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。

      1. ハッシュ化された電子メール ID を含む列は、訪問者 ID のタイプの属性にマッピングする必要があります。

      1. オーディエンスは、 `Tealium_visitor_id` 属性。 オーディエンスのトリガーに適切なエンリッチメントを適用する必要があります。 詳しくは、 [[!DNL Tealium] 訪問者 ID 属性に関するドキュメント](https://docs.tealium.com/server-side/visitor-stitching/visitor-id-attribute/).

   1. DSPでセグメントを作成するには、広告主がセグメントマッピングデータをAdobeアカウントチームに提供する必要があります。 次の列名と値をコンマ区切り値ファイルで使用します。

      * **外部セグメントキー：** 外部セグメントキー。後で、 [!DNL Tealium]. 推奨される命名規則は、「`<DSP source key>_<Tealium segment name>`、「57bf424dc10_coffee-drinkers」など。

      * **セグメント名：** セグメント名。

      * **セグメントの説明：** セグメントの目的、ルール、またはその両方。

      * **親 ID :** 空白のままにする

      * **ビデオ CPM:** 0

      * **CPM を表示：** 0

      * **セグメントウィンドウ：** セグメントの有効期間。

## 手順 3：でコネクタを作成する [!DNL Tealium] セグメントデータを共有するには {#tealium-connector}

共有するセグメントごとに、データの変更をトリガーするアクションごとに別々のコネクタを作成します。 例えば、2 つのトリガーを持つ 2 つのセグメントを共有するには、4 つのコネクタを作成します。

1. Adobeアカウントチームは、広告主にAWS Firehose コネクタの資格情報を提供します。

1. In [!DNL Tealium], [コネクタの追加](https://docs.tealium.com/server-side/connectors/add/)（次のオプションを使用）

   1. を選択します。 [!DNL AWS Firehose] コネクタ。

   1. ソース設定で、以下の手順を実行します。

      1. 共有するオーディエンスセグメントを選択します。

      1. トリガー:

         * セグメントの最初のコネクタに対して、「 」トリガーを選択します。 `Joined Audience`. これにより、ユーザーがセグメントに結合するたびに、DSPとデータが共有されます。

         * セグメントの 2 番目のコネクタに対して、トリガー `Left Audience`. このコネクタは、DSPでセグメントを離脱するすべてのオプトアウトおよびユーザーを処理するために使用されます。

   1. 設定で、AWS Firehose コネクタを指定します。 DSP用の消防コネクタをまだ追加していない場合は、次の情報を使用して消防コネクタを追加します。

      * **名前：** コネクタの名前。

      * **アクセスキー：** Adobeアカウントチームが提供するアクセスキー。

      * **秘密鍵：** アカウントチームから提供されたAdobeキー。

      * **地域：** 米国東北バージニア州（米国東部 —1）

   1. アクション設定で、次の操作を行います。

      1. 次の情報を使用して、「顧客データを配信ストリームに送信（詳細）」アクションを作成し、セグメントにデータを追加します。

         * **アクション名：** アクションの名前。

         * **アクションタイプ：** 顧客データを配信ストリームに送信（詳細）

         * **配信ストリーム：** Tealium_CDP_Connector

         * **メッセージデータ：**  次の操作を実行します。

            1. セグメントの属性を 1 つ選択します。

               * Hashed_Email 属性に、カスタムメッセージに名前を付けます。 `hashed_email`.

               * Cookies 属性に、カスタムメッセージに名前を付けます。 `cookies`.

            1. カスタムフィールドを作成するオプション ( [!DNL Source Key] フィールドに、 [!UICONTROL External Segment Key] のセグメントマッピングデータに含まれていた [手順 2](#map-data).

               DSPは、このキーを使用してセグメントを設定します。

            1. （推奨）セグメントを新しく保つ更新アクションを作成します。

## 手順 4：で既存のコネクタを複製する [!DNL Tealium] セグメントを共有し続けるには {#duplicate-connector}

1 つのセグメントにつき 1 つのコネクタ、1 つのコネクタにつき 1 つのセグメントのみを指定できます。

1. In [!DNL Tealium]をクリックし、別のセグメントを作成するセグメントを複製して、新しいセグメントの名前を変更します。

1. In [!DNL Tealium]に設定する場合は、で作成したコネクタを複製します。 [手順 3](#tealium-connector)をクリックし、新しいコネクタ名を「`<original name>-copy`」が新しいセグメント名に追加されました。

>[!MORELIKETHIS]
>
>* [オーディエンスソースからの認証済みセグメントのアクティブ化について](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを作成してファーストパーティオーディエンスをアクティブ化する](source-create.md)
>* [Audience Source 設定](source-settings.md)
>* [とのDSP統合を使用する際のワークフロー [!DNL Adobe Real-Time CDP]](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
