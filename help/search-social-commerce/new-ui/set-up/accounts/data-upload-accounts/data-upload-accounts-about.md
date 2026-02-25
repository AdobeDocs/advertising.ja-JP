---
title: null
description: null
source-git-commit: f2b29c2f3a38cadc31a9b3110aa82feadd62e5cc
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 0%

---

# レポートおよびシミュレーション用のアカウントデータのアップロードについて

<!-- Move all related files into one page? -->

検索、ソーシャル、Commerceでは API のサポートを提供していないオンライン広告ネットワークを使用している場合は、キャンペーンコンテンツやオフラインコスト、クリック、コンバージョンデータをアップロードし、レポートやパフォーマンスのシミュレーションに使用するアカウントを作成できます。 [[!DNL Adobe Analytics for Advertising]  統合 ](/help/integrations/analytics/overview.md) を持つ広告主は、Adobe Analytics内で自分のアカウントのデータを表示することもできます。

この機能は、標準の 3 層キャンペーン構造（キャンペーン、広告グループまたは広告セット、入札単位（広告またはキーワード））に従う広告ネットワークで使用できます。 Adobe DSPの場合、この機能は、パッケージに割り当てられたパッケージとプレースメントに対して使用できますが、プレースメントレベルのペーシングを使用したキャンペーンやプレースメントに対しては使用できません。

標準のサポートは、次のネットワークで利用できます。<!-- But what if you want to use something else? Is that possible currently? -->

<!-- * Adobe Demand Side Platform (Advertising DSP) [Is any data upload required, or just an initial setup of an S3 bucket and/or something else, and then DSP sends the data automatically? If so, then I may need to reframe this whole chapter accordingly.] -->
<!-- * [!DNL Reddit Ads] -->

* [!DNL Apple Search Ads]
* [!DNL LinkedIn Ads]
* [!DNL TikTok Ads]

検索、ソーシャル、CommerceのクリックのトラッキングとAdobe Advertisingのコンバージョントラッキングは、この機能ではサポートされません。

## 検索、ソーシャル、Commerce内で使用できる機能

* トラッキングとレポート：

   * キャンペーン管理ビュー内で入札単位レベルまで読み取り専用のキャンペーンコンポーネント。

   * キャンペーン管理ビューおよびカスタムレポート内の広告グループレベルま <!-- verify the entity level --> のパフォーマンスデータ。 [!DNL Adobe Analytics for Advertising]）を使用している広告主は、さらに、広告主に対して指定されたAdobe Analytics レポートスイート内の広告グループレベル <!-- verify the entity level --> まで、パフォーマンスデータを取得します。&lt;!— データタイプが制限されているかどうかを確認します（コスト、クリック、インプレッション、売上高など）。—>

* キャンペーンをポートフォリオに追加する際のパフォーマンスシミュレーション。<!-- How does this even work? Do they need to be in standard or hybrid portfolios, with active or optimized status, and can you mix these campaigns with API-synced campaigns? If so, do we just ignore these campaigns and optimize the others? -->

  検索、ソーシャル、Commerceでは、ポートフォリオ内のこれらのタイプのキャンペーンに対して、何も最適化されず、入札もされません。

## オフラインアカウントを設定するためのワークフロー

<!-- subtitle wording? -->

1. [ ダミーのアカウントレコードを設定 ](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md) します。

1. 単一のアカウントのデータファイルを作成します。これには <!--  in what file format? --> キャンペーン、広告グループ、広告の日レベルでのステータスが含まれます。

データは広告ネットワークのデータ要件に従う必要があるので、各エンティティのデータフィールドは広告ネットワークによって異なる場合があります。

1. <!-- For all ad networks (excluding DSP), -->次のいずれかの方法で、単一のアカウントの初期データをアップロードします。

* デバイスまたはネットワークから手動でファイルをアップロードします。

* [!DNL Amazon Web Services] （AWS） [!DNL Simple Storage Service] （[!DNL S3]）バケットの検索、ソーシャル、Commerceに割り当てられたフォルダーにデータをアップロードします。

  >[!PREREQUISITES]
  >
  >* 検索、ソーシャル、Commerce広告主アカウントのアカウントデータのアップロードを有効にする場合は、Adobe アカウントチームにお問い合わせください。 チームは、[!DNL S3] バケット内で組織固有のフォルダーを容易に作成でき、完了するとお知らせします。<!-- Add more context about the bucket we'll use here or in the intro. Do we have one bucket (potentially with multiple folders) per client, or do we share them (if so, do we need to state how in docs? -->
  >* アカウントの [!DNL S3] クラウドストレージパス、アクセスキー ID および秘密アクセスキーを取得します。 同じアクセスキー ID と秘密アクセスキーが、組織のすべてのデータアップロード <!-- naming convention?--> アカウントに使用されます。

1. 新しいデータファイルのアップロードを毎日続けます。

1. 30 日間データをアップロードしたら、オプションでキャンペーンをに追加し、ポートフォリオを作成して <!--what type? how should we refer to them? --> シミュレーションを生成できます。

[ 各データアップロードのログを表示 ](upload-log.md) して、そのステータスを確認できます。 また、アップロードを開始しても、アップロードが完全に成功しない場合は、通知設定に基づいて、[ 通知センター ](/help/search-social-commerce/notifications/notification-about.md) を介してエラー通知が届きます。

<!-- Data validation, and any troubleshooting? -->

>[!MORELIKETHIS]
>
>* [ レポートおよびシミュレーション用のアカウントデータのアップロードについて ](data-upload-accounts-about.md)
>* [ アカウントデータの  [!DNL Amazon] [!DNL S3] バケットへのアップロード ](upload-data-from-s3-bucket.md)
>* [ アカウントデータを手動でアップロード ](upload-data-manually.md)
>* [ アップロードされたアカウントデータファイルのログを表示 ](upload-log.md)
>* [ データのアップロード用の広告ネットワークアカウントの管理 ](/help/search-social-commerce/campaign-management/accounts/data-upload-account-manage.md)
