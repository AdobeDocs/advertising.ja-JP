---
title: レポートおよびシミュレーション用のオフラインアカウントデータのアップロード
description: オフラインアカウントデータを手動で、または  [!DNL Amazon] [!DNL S3] バケットにアップロードして、レポートやシミュレーションをサポートする方法を説明します。 ログファイルは、アップロードジョブの進行状況を追跡します。
source-git-commit: 8ba0f8fa6050a3e6ec93bcf08df2c0204191fc02
workflow-type: tm+mt
source-wordcount: '683'
ht-degree: 0%

---

# レポートおよびシミュレーション用のオフラインアカウントデータのアップロード

*アカウントのデータのアップロードを有効にした広告主*

レポートやパフォーマンスのシミュレーションに対する API のサポートなしで、キャンペーンコンテンツとオフラインコスト、クリック、コンバージョンデータをアカウントにアップロードします。

[!UICONTROL Upload Logs] の機能を使用して、アップロードジョブの進行状況を追跡できます。

* アカウントにアップロードされた各ファイルのリストを表示します。 各ファイルアップロードジョブに関する情報には、ファイル名、アップロードチャネル（*[!UICONTROL Cloud Storage]* または *[!UICONTROL Drag & Drop]*）、同期日とステータス、不完全なアップロードの理由が含まれます。

* 任意のジョブに対してアップロードされたアカウントエンティティと関連指標を含むファイルをダウンロードします。 ファイルはコンマ区切り値（CSV）形式です。

## アカウントデータを手動でアップロード

ファイルにデータを手動でアップロードすることで、アカウントにキャンペーンコンテンツとコスト、クリックおよびコンバージョンデータを入力できます。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの操作をおこないます。

   * （[!UICONTROL Accounts] ビューから）:

      1. アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Upload]**」をクリックします。

      1. ファイルをボックスにドラッグするか、**[!UICONTROL Browse Files]** をクリックして、デバイスまたはネットワークからファイルを選択します。

      1. 「**[!UICONTROL Upload Files]**」をクリックします。

   * （アカウント設定から）

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

         * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. 「**[!UICONTROL Upload File]**」タブをクリックします。

      1. ファイルをボックスにドラッグするか、**[!UICONTROL Browse Files]** をクリックして、デバイスまたはネットワークからファイルを選択します。

      1. 「**[!UICONTROL Save]**」をクリックします。

## [!DNL Amazon] [!DNL S3] バケットへのアカウントデータのアップロード {#data-upload-s3}

アカウントにキャンペーンコンテンツとコスト、クリック数およびコンバージョンデータを入力するには、データを、[!DNL Amazon Web Services] （AWS） [!DNL Simple Storage Service] （[!DNL S3]）バケットの検索、ソーシャルおよびCommerceに割り当てられたフォルダーにアップロードします。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* 検索、ソーシャル、Commerce広告主アカウントのアカウントデータのアップロードを有効にする場合は、Adobe アカウントチームにお問い合わせください。 チームは、[!DNL S3] バケット内で組織固有のフォルダーを容易に作成でき、完了するとお知らせします。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* アカウントの [!DNL S3] クラウドストレージパス、アクセスキー ID および秘密アクセスキーを取得します。 同じアクセスキー ID と秘密アクセスキーが、組織のすべてのデータアップロード <!-- naming convention?--> アカウントに使用されます。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの操作をおこないます。

   * （[!UICONTROL Accounts] ビューから）:

      1. アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Upload]**」をクリックします。

      1. [[!UICONTROL Cloud Storage Link]] ボックスの [**[!UICONTROL Go to the Link]**] をクリックします。

      1. 「**[!UICONTROL Show Access Key and Secret]**」をクリックします。

      1. 「[!UICONTROL Storage Link]」フィールドの横にある「**[!UICONTROL Copy]**」をクリックしてリンクをクリップボードにコピーし、安全な場所にリンクを保存します。

      1. 同様に、[!UICONTROL Access Key] と [!UICONTROL Secret Key] の値をコピーして安全に保存します。

      1. 「**[!UICONTROL Done]**」をクリックします。

   * （アカウント設定から）

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

         * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. 「**[!UICONTROL Upload File]**」タブをクリックします。

      1. [[!UICONTROL Cloud Storage Link]] ボックスの [**[!UICONTROL Go to the Link]**] をクリックします。

      1. 「**[!UICONTROL Show Access Key and Secret]**」をクリックします。

      1. 「[!UICONTROL Storage Link]」フィールドの横にある「**[!UICONTROL Copy]**」をクリックしてリンクをクリップボードにコピーし、安全な場所にリンクを保存します。

      1. 同様に、[!UICONTROL Access Key] と [!UICONTROL Secret Key] の値をコピーして安全に保存します。

      1. 「**[!UICONTROL Done]**」をクリックします。

      1. 「**[!UICONTROL Save]**」をクリックします。

1. （組織ごとに 1 回） ローカルのAWS環境を設定します。

   1. [!DNL AWS Command Line Interface] （AWS CLI）を次の場所からダウンロードしてインストールします：[https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)。

   1. AWSの認証情報を設定します。

      1. プレーンテキストファイルを作成し、`~/.aws/credentials` という名前（ファイル拡張子なし）を付けます。

      1. ファイルを任意のテキストエディターで開き、組織のアクセスキー ID と秘密アクセスキーを次のように入力します。

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. 広告ネットワークからアカウントデータレポートをダウンロードして保存します。

1. AWS CLI で、次のコマンドを実行して、アカウントデータを [!DNL S3] Cloud の場所にアップロードします。

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   例：`aws s3 cp filename.txt s3://cloud-location/`

## アップロードされたアカウントデータファイルのログの表示

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Upload Logs]**] をクリックします。

1. （任意）アップロードしたファイルのデータをダウンロードするには、![&#x200B; 列の &#x200B;](/help/search-social-commerce/assets/download.png " ダウンロード ") ダウンロード [!UICONTROL Download] をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

## 必要なデータ

データは、広告ネットワークのデータ要件に従う必要があります。 各エンティティのデータフィールドは、広告ネットワークによって異なる場合があります。
