---
title: （新しいUI）広告ネットワークアカウントについて
description: 新しい検索、ソーシャル、およびCommerce UIの広告ネットワークアカウントについて説明します。
feature: Search Campaign Management
exl-id: 62c69582-6b95-4ae3-b027-d1efc3deb39e
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 0%

---

# （新しいUI）広告ネットワークアカウントについて

Search, Social, &amp; Commerceは、サポートされている広告ネットワーク上で広告主のアカウントをトラッキングできます。 アカウントのトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。 Search, Social, &amp; Commerceと同期するか、広告で入札や予算を最適化するかにかかわらず、あらゆるタイプのアカウントの詳細を設定する必要があります。

## API経由でアカウントを同期

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称[!DNL Bing Ads]）、[!DNL LY Ads] （旧称[!DNL Yahoo! Japan Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yandex]および既存の[!DNL Baidu] アカウント*

Search, Social, &amp; Commerceは、（*syncs*）をサポートされている広告ネットワークアカウントと同期させ、広告のパフォーマンスを追跡、レポート、視覚化できるようにします。 [!DNL Yahoo! Display Network]を除くすべてのアドネットワークでは、Search, Social, &amp; Commerceでアカウントのキャンペーンをオプションで管理できます。[!DNL Yahoo! Display Network]、キャンペーンは読み取り専用です。 すべての広告ネットワークに対して、ポートフォリオにキャンペーンを追加することで、最適化機能で管理対象アカウントのキャンペーンの入札額、キャンペーン予算、キャンペーン入札戦略ターゲットを最適化できます。

アカウントの同期を有効にするには、アカウントレコードにアカウントアクセス資格情報が含まれており、有効（アクティブ）である必要があります。

Search, Social, &amp; Commerceは、同期中に、広告主のキャンペーン構造と、Search, Social, &amp; Commerceで管理または報告されているほとんどの属性を含む、サポートされているキャンペーンエンティティを取得します。 クリックデータは含まれず、Search, Social, &amp; Commerceの外部に入力された入札額や入札修飾子も含まれません。 Search, Social, &amp; Commerceは、1日に1回、広告ネットワークのアカウントと自動的に同期します。また、広告ネットワークの1つで新しいキャンペーンが検出されるたびに同期します。 さらに、検索、ソーシャル、Commerce内から作成されたキャンペーンデータへのあらゆる変更が、広告ネットワークにすぐに送信されます。 必要に応じて、オプションで手動同期をリクエストできます。

同期済みキャンペーンの作成と編集について詳しくは、「キャンペーン管理」の章を参照してください。

## 手作業でデータをアップロードするアカウント

Search, Social, &amp; CommerceがAPI サポートを提供しないオンライン広告ネットワークの場合、レポートとパフォーマンスシミュレーション用アカウントのキャンペーンコンテンツとオフラインのコスト、クリック、コンバージョンのデータをアップロードできます。 Search, Social, &amp; Commerceは、データを広告ネットワークと同期させたり、自動入札を提供したり、あらゆる種類の最適化を提供したりすることはできませんが、クロスチャネルのインサイトを合理化し、手作業による最適化の機会を特定することを可能にします。

## テンプレートベースのトラッキング専用アカウント

*既存の[!DNL Naver] アカウントでのみ利用可能*

トラッキング施策を利用すると、広告ネットワークから直接購入した広告のパフォーマンスを追跡、報告、可視化できます。 Search, Social, &amp; Commerceでは、データと広告ネットワークの同期が取れず、自動入札も提供されず、あらゆる種類の最適化やシミュレーションも提供されません。

Search, Social, &amp; Commerceでコンバージョンをクリックに関連付けられるようにするには、アカウントレコードにトラッキングオプションを設定し、アカウントレコードを有効にします。 次に、バルクシートを使用して広告とキーワードのトラッキング URLを生成し、[!DNL Naver]広告マネージャー内にトラッキング URLを手動で追加できます。

Search, Social, &amp; Commerceで新しい[!DNL Naver] アカウントを設定することはできません。 [!DNL Naver]件のトラッキング専用キャンペーンについて詳しくは、「[実装 [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [API接続による広告ネットワークアカウントの管理](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
>* [&#x200B; データのアップロード用の広告ネットワークアカウントの管理](/help/search-social-commerce/new-ui/set-up/accounts/data-upload-accounts/data-upload-account-manage.md)
>* [&#x200B; トラッキング専用の [!DNL Naver]  アカウントの管理](/help/search-social-commerce/new-ui/set-up/accounts/template-account-manage.md)
>* [&#x200B; トラッキング専用アカウントを実装 [!DNL Naver] します](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [&#x200B; マーチャント センターのアカウントの管理](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)
