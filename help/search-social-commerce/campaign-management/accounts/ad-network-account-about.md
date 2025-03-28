---
title: 広告ネットワークアカウントについて
description: 広告ネットワークアカウントについては、検索、ソーシャル、Commerceを参照してください。
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
source-git-commit: 0af1c5591a59b9e1813209fea3ac6aaecc0e649b
workflow-type: tm+mt
source-wordcount: '426'
ht-degree: 0%

---

# 広告ネットワークアカウントについて

*エージェンシーアカウント管理者、Adobeアカウント管理者、管理者ユーザーの役割のみ*

検索、ソーシャル、Commerceでは、サポートされている広告ネットワーク上の広告主のアカウントをトラッキングできます。 アカウントのトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。 検索、ソーシャル、Commerceで同期するか、広告の入札や予算を最適化するかにかかわらず、あらゆるタイプのアカウントにアカウントの詳細を設定する必要があります。

## API を使用して同期されたアカウント

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称 [!DNL Bing Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウント*

検索、ソーシャル、Commerceは、サポートされている広告ネットワークアカウントと（*syncs*）同期するので、広告のパフォーマンスを追跡、レポート、視覚化できます。 [!DNL Yahoo! Display Network] を除くすべての広告ネットワークで、オプションで検索、ソーシャル、Commerceのアカウントのキャンペーンを管理できます。[!DNL Yahoo! Display Network] の場合、キャンペーンは読み取り専用です。 すべての広告ネットワークで、最適化機能を使用して、キャンペーンをポートフォリオに追加することで、管理アカウントのキャンペーンの入札、キャンペーン予算およびキャンペーン入札戦略ターゲットを最適化できます。

アカウントの同期を有効にするには、アカウントレコードにアカウントアクセス資格情報が含まれ、有効（アクティブ）になっている必要があります。

同期中、検索、ソーシャル、Commerceは、検索、ソーシャル、Commerceで管理またはレポートされる属性のほとんどを含め、広告主のキャンペーン構造とサポートされるキャンペーンエンティティを取り込みます。 クリックデータや、検索、ソーシャル、Commerceの外部で入力された入札および入札修飾子は含まれません。これらは個別に収集されます。 検索、ソーシャル、Commerceは、1 日に 1 回、および広告ネットワークの 1 つに新しいキャンペーンが検出されるたびに、広告ネットワークアカウントと自動的に同期されます。 さらに、検索、ソーシャル、Commerce内で作成されたキャンペーンデータに対するすべての変更を、即座に広告ネットワークに送信します。 必要に応じて、手動での同期をリクエストすることもできます。

同期されたキャンペーンの作成と編集について詳しくは、「Campaign Management」の章を参照してください。

## トラッキング専用アカウント

*[!DNL Naver]アカウント*

トラッキングキャンペーンを使用すると、広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、視覚化できます。 検索、ソーシャル、Commerceでは、データが広告ネットワークと同期されず、アカウントの入札も行われず、最適化やシミュレーションも行われません。

検索、ソーシャル、Commerceでコンバージョンをクリック数に関連付けるには、アカウントレコードにトラッキングオプションを設定し、アカウントレコードを有効にします。 その後、バルクシートを使用して広告とキーワードのトラッキング URL を生成し、[!DNL Naver] の広告マネージャー内にトラッキング URL を手動で追加できます。

[!DNL Naver] のトラッキング専用キャンペーンの詳細については、「[ トラッキング専用アカウントの実装  [!DNL Naver]  を参照 ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) てください。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークアカウントの管理 ](ad-network-account-manage.md)
>* [ マーチャントセンターアカウントの管理 ](merchant-account-manage.md)
>* [ アカウントの AMO ID トラッキングコード  [!DNL Google Ads]  更新 ](update-amo-id-google.md)
