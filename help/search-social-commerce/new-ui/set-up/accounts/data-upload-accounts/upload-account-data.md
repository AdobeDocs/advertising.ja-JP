---
title: レポートとシミュレーション用のオフラインアカウントデータのアップロード
description: レポートとシミュレーションのサポートのために、オフラインのアカウントデータを手動または [!DNL Amazon] [!DNL S3] バケットにアップロードする方法について説明します。 ログファイルは、アップロードジョブの進行状況を追跡します。
source-git-commit: c2fde4837c4300f4e55b3591992af64630d58ba6
workflow-type: tm+mt
source-wordcount: '700'
ht-degree: 0%

---

# レポートとシミュレーション用のオフラインアカウントデータのアップロード

*アカウントデータのアップロードが有効になっている広告主*

レポートとパフォーマンスのシミュレーションにAPIをサポートすることなく、キャンペーンのコンテンツやオフラインコスト、クリック、アカウントのコンバージョンデータをアップロードできます。

[!UICONTROL Upload Logs]機能を使用して、アップロードジョブの進行状況を追跡できます。

* アカウントにアップロードされた各ファイルのリストを表示します。 各ファイルのアップロードジョブに関する情報には、ファイル名、アップロードチャネル （*[!UICONTROL Cloud Storage]*&#x200B;または&#x200B;*[!UICONTROL Drag & Drop]*）、同期日とステータス、不完全なアップロードの理由が含まれます。

* 任意のジョブにアップロードされたアカウントエンティティと関連する指標を含むファイルをダウンロードします。 ファイルはコンマ区切り値（CSV）形式です。

## アカウントデータを手動でアップロード

データをファイルに手動でアップロードすることで、キャンペーンのコンテンツやコスト、クリック、コンバージョンデータをアカウントに入力することができます。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （[!UICONTROL Accounts] ビューから）:

      1. アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Upload]**」をクリックします。

      1. ファイルをボックスにドラッグするか、**[!UICONTROL Browse Files]**&#x200B;をクリックして、デバイスまたはネットワークからファイルを選択します。

      1. **[!UICONTROL Upload Files]**&#x200B;をクリックします。

   * （アカウント設定から）:

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

         * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. 「**[!UICONTROL Upload File]**」タブをクリックします。

      1. ファイルをボックスにドラッグするか、**[!UICONTROL Browse Files]**&#x200B;をクリックして、デバイスまたはネットワークからファイルを選択します。

      1. **[!UICONTROL Save]**&#x200B;をクリックします。

## アカウントデータを[!DNL Amazon] [!DNL S3] バケットにアップロード {#data-upload-s3}

[!DNL Amazon Web Services] （AWS） [!DNL Simple Storage Service] （[!DNL S3]）バケットのSearch, Social, &amp; Commerceで割り当てられたフォルダーにデータをアップロードすることで、キャンペーンの内容とコスト、クリック、コンバージョンデータをアカウントに入力できます。

<!--
See "XXX" for information about supported ad networks and account structures.

[supported ad networks and campaign types](/help/search-social-commerce/introduction/supported-inventory.md)
-->

>[!PREREQUISITES]
>
>* Search, Social, &amp; Commerce広告主アカウントのアカウントデータのアップロードを有効にするには、Adobe アカウントチームにお問い合わせください。 チームは、[!DNL S3] バケット内の組織固有のフォルダーの作成を促進し、完了したら通知を受け取ります。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
>* アカウントの[!DNL S3] クラウド ストレージ パス、アクセス キーID、および秘密アクセス キーを取得します。 同じアクセス キーIDと秘密アクセス キーが、組織のすべてのデータ アップロード <!-- naming convention?--> アカウントに使用されます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （[!UICONTROL Accounts] ビューから）:

      1. アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Upload]**」をクリックします。

      1. [!UICONTROL Cloud Storage Link] ボックスで、**[!UICONTROL Go to the Link]**&#x200B;をクリックします。

      1. **[!UICONTROL Show Access Key and Secret]**&#x200B;をクリックします。

      1. 「[!UICONTROL Storage Link]」フィールドの横にある「**[!UICONTROL Copy]**」をクリックしてリンクをクリップボードにコピーし、リンクを安全な場所に保存します。

      1. 同様に、[!UICONTROL Access Key]と[!UICONTROL Secret Key]の値をコピーして安全に保存します。

      1. **[!UICONTROL Done]**&#x200B;をクリックします。

   * （アカウント設定から）:

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

         * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. 「**[!UICONTROL Upload File]**」タブをクリックします。

      1. [!UICONTROL Cloud Storage Link] ボックスで、**[!UICONTROL Go to the Link]**&#x200B;をクリックします。

      1. **[!UICONTROL Show Access Key and Secret]**&#x200B;をクリックします。

      1. 「[!UICONTROL Storage Link]」フィールドの横にある「**[!UICONTROL Copy]**」をクリックしてリンクをクリップボードにコピーし、リンクを安全な場所に保存します。

      1. 同様に、[!UICONTROL Access Key]と[!UICONTROL Secret Key]の値をコピーして安全に保存します。

      1. **[!UICONTROL Done]**&#x200B;をクリックします。

      1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （組織ごとに1回）ローカル AWS環境を設定します。

   1. 次の場所から[!DNL AWS Command Line Interface] （AWS CLI）をダウンロードしてインストールします：[https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html](https://docs.aws.amazon.com/cli/latest/userguide/getting-started-install.html)。

   1. AWSの資格情報を設定します。

      1. プレーンテキストファイルを作成し、`~/.aws/credentials`という名前を付けます（ファイル拡張子は使用しません）。

      1. 任意のテキストエディターでファイルを開き、組織のアクセスキーIDとシークレットアクセスキーを次のように入力します。

         ```
         [default]
         aws_access_key_id = <Access key copied in Step 2>
         aws_secret_access_key = <Secret key copied in Step 2>
         ```

1. 広告ネットワークからアカウントデータレポートをダウンロードして保存します。

1. AWS CLIで次のコマンドを実行して、アカウントデータを[!DNL S3] クラウドの場所にアップロードします。

   ```
   aws s3 cp <local-report-file-location <S3-cloud-location-associated-with-your-account>
   ```

   例：`aws s3 cp filename.txt s3://cloud-location/`

## アップロードされたアカウントデータファイルのログを表示する

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Upload Logs]**&#x200B;をクリックします。

1. （オプション）アップロードしたファイルのデータをダウンロードするには、[!UICONTROL Download]列の![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

## 必要なデータ

データは、広告ネットワークのデータ要件に従う必要があります。 各エンティティのデータフィールドは、広告ネットワークによって異なる場合があります。
