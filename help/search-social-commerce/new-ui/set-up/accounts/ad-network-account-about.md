---
title: （新しい UI）広告ネットワークアカウントについて
description: 新しい検索、ソーシャル、Commerce UI での広告ネットワークアカウントについて説明します。
feature: Search Campaign Management
source-git-commit: e62eb730ec88a37cbe34e35d7b9bf99e0d4fd41d
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 0%

---

# （新しい UI）広告ネットワークアカウントについて

検索、ソーシャル、Commerceでは、サポートされている広告ネットワーク上の広告主のアカウントをトラッキングできます。 アカウントのトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。 検索、ソーシャル、Commerceで同期するか、広告の入札や予算を最適化するかにかかわらず、あらゆるタイプのアカウントにアカウントの詳細を設定する必要があります。

## API を使用して同期されたアカウント

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称 [!DNL Bing Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウント*

検索、ソーシャル、Commerceは、サポートされている広告ネットワークアカウントと（*syncs*）同期するので、広告のパフォーマンスを追跡、レポート、視覚化できます。 [!DNL Yahoo! Display Network] を除くすべての広告ネットワークで、オプションで検索、ソーシャル、Commerceのアカウントのキャンペーンを管理できます。[!DNL Yahoo! Display Network] の場合、キャンペーンは読み取り専用です。 すべての広告ネットワークで、最適化機能を使用して、キャンペーンをポートフォリオに追加することで、管理アカウントのキャンペーンの入札、キャンペーン予算およびキャンペーン入札戦略ターゲットを最適化できます。

アカウントの同期を有効にするには、アカウントレコードにアカウントアクセス資格情報が含まれ、有効（アクティブ）になっている必要があります。

同期中、検索、ソーシャル、Commerceは、検索、ソーシャル、Commerceで管理またはレポートされる属性のほとんどを含め、広告主のキャンペーン構造とサポートされるキャンペーンエンティティを取り込みます。 クリックデータや、検索、ソーシャル、Commerceの外部で入力された入札および入札修飾子は含まれません。これらは個別に収集されます。 検索、ソーシャル、Commerceは、1 日に 1 回、および広告ネットワークの 1 つに新しいキャンペーンが検出されるたびに、広告ネットワークアカウントと自動的に同期されます。 さらに、検索、ソーシャル、Commerce内で作成されたキャンペーンデータに対するすべての変更を、即座に広告ネットワークに送信します。 必要に応じて、手動での同期をリクエストすることもできます。

同期されたキャンペーンの作成および編集について詳しくは、「キャンペーン管理」の章を参照してください。

## 手動でデータをアップロードしたアカウント

検索、ソーシャル、Commerceでは API のサポートを提供していないオンライン広告ネットワークの場合は、キャンペーンコンテンツやオフラインのコスト、クリック、コンバージョンデータをアップロードし、アカウントにアクセスしてレポートやパフォーマンスのシミュレーションを行うことができます。 検索、ソーシャル、Commerceでは、データを広告ネットワークと同期したり、自動入札を行ったり、あらゆる種類の最適化を行ったりしませんが、クロスチャネルインサイトを効率化したり、手動で最適化する機会を特定したりすることはできます。

## テンプレートベースのトラッキング専用アカウント

*既存の [!DNL Naver] アカウントでのみ使用可能*

トラッキングキャンペーンを使用すると、広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、視覚化できます。 検索、ソーシャル、Commerceでは、データを広告ネットワークと同期したり、自動入札を行ったり、あらゆる種類の最適化やシミュレーションを行ったりしません。

検索、ソーシャル、Commerceでコンバージョンをクリック数に関連付けるには、アカウントレコードにトラッキングオプションを設定し、アカウントレコードを有効にします。 その後、バルクシートを使用して広告とキーワードのトラッキング URL を生成し、[!DNL Naver] の広告マネージャー内にトラッキング URL を手動で追加できます。

検索、ソーシャル、Commerceで新しい [!DNL Naver] アカウントを設定することはできません。 [!DNL Naver] のトラッキング専用キャンペーンの詳細については、「[&#x200B; トラッキング専用アカウントの実装  [!DNL Naver]  を参照 &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) てください。

>[!MORELIKETHIS]
>
>* [API 接続を使用した広告ネットワークアカウントの管理 &#x200B;](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [&#x200B; データのアップロード用の広告ネットワークアカウントの管理 &#x200B;](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [&#x200B; トラッキング専用の管理  [!DNL Naver]  アカウント &#x200B;](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [&#x200B; 実装  [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [&#x200B; マーチャントセンターアカウントの管理 &#x200B;](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
