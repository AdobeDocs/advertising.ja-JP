---
title: 広告ネットワークアカウントについて
description: Search, Social, & Commerceの広告ネットワークアカウントについて説明します。
exl-id: cb3e650d-721f-48ec-ada3-50bdd7c0375b
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/90Dq2tehH-k2aY3Ij30aHF-XQGdvlPY346moWkg3xmk
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 426
ht-degree: 0%

---

# 広告ネットワークアカウントについて

*代理店アカウントマネージャー、Adobe アカウントマネージャー、管理者ユーザーの役割のみ*

Search, Social, &amp; Commerceは、サポートされている広告ネットワーク上で広告主のアカウントをトラッキングできます。 アカウントのトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。 Search, Social, &amp; Commerceと同期するか、広告で入札や予算を最適化するかにかかわらず、あらゆるタイプのアカウントの詳細を設定する必要があります。

## API経由でアカウントを同期

*[!DNL Google Ads]、[!DNL Microsoft Advertising] （旧称[!DNL Bing Ads]）、[!DNL Yahoo! Display Network]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex]、および既存の[!DNL Baidu] アカウント*

Search, Social, &amp; Commerceは、（*syncs*）をサポートされている広告ネットワークアカウントと同期させ、広告のパフォーマンスを追跡、レポート、視覚化できるようにします。 [!DNL Yahoo! Display Network]を除くすべてのアドネットワークでは、Search, Social, &amp; Commerceでアカウントのキャンペーンをオプションで管理できます。[!DNL Yahoo! Display Network]、キャンペーンは読み取り専用です。 すべての広告ネットワークに対して、ポートフォリオにキャンペーンを追加することで、最適化機能で管理対象アカウントのキャンペーンの入札額、キャンペーン予算、キャンペーン入札戦略ターゲットを最適化できます。

アカウントの同期を有効にするには、アカウントレコードにアカウントアクセス資格情報が含まれており、有効（アクティブ）である必要があります。

Search, Social, &amp; Commerceは、同期中に、広告主のキャンペーン構造と、Search, Social, &amp; Commerceで管理または報告されているほとんどの属性を含む、サポートされているキャンペーンエンティティを取得します。 クリックデータは含まれず、Search, Social, &amp; Commerceの外部に入力された入札額や入札修飾子も含まれません。 Search, Social, &amp; Commerceは、1日に1回、広告ネットワークのアカウントと自動的に同期します。また、広告ネットワークの1つで新しいキャンペーンが検出されるたびに同期します。 さらに、検索、ソーシャル、Commerce内から作成されたキャンペーンデータへのあらゆる変更が、広告ネットワークにすぐに送信されます。 必要に応じて、オプションで手動同期をリクエストできます。

同期済みキャンペーンの作成と編集について詳しくは、「キャンペーン管理」の章を参照してください。

## トラッキング専用アカウント

*[!DNL Naver]アカウント*

トラッキング施策を利用すると、広告ネットワークから直接購入した広告のパフォーマンスを追跡、報告、可視化できます。 Search, Social, &amp; Commerceでは、データが広告ネットワークと同期せず、アカウントの入札も行われず、どのような種類の最適化やシミュレーションも提供されません。

Search, Social, &amp; Commerceでコンバージョンをクリックに関連付けられるようにするには、アカウントレコードにトラッキングオプションを設定し、アカウントレコードを有効にします。 次に、バルクシートを使用して広告とキーワードのトラッキング URLを生成し、[!DNL Naver]広告マネージャー内にトラッキング URLを手動で追加できます。

[!DNL Naver]件のトラッキング専用キャンペーンについて詳しくは、「[実装 [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
>* [&#x200B; マーチャント センターのアカウントの管理](merchant-account-manage.md)
>* [&#x200B; アカウント  [!DNL Google Ads] のAMO ID トラッキングコードを更新します](update-amo-id-google.md)
