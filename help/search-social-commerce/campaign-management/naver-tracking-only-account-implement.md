---
title: 実装  [!DNL Naver]  トラッキング専用アカウント
description: ' [!DNL Naver]  アカウントのトラッキングキャンペーンを設定し、広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、視覚化する方法を説明します。'
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '687'
ht-degree: 0%

---

# [!DNL Naver] トラッキング専用アカウントの実装

*[!DNL Naver]アカウントのみ*

[!DNL Naver] アカウントのトラッキングキャンペーンを作成すると、広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、視覚化できます。 検索、ソーシャル、Commerceでは、データが広告ネットワークと同期されたり、トラッキングが自動的にアップロードされたり、アカウントに入札が行われたりすることはありません。

トラッキングキャンペーンは、既存のキャンペーン、広告グループおよびキーワードをレプリケートします。 検索、ソーシャル、Commerceでアカウント構造を作成し、広告ネットワーク内の元のキャンペーンにトラッキングを追加したら、キーワードまたは広告の毎日のネットワークトラフィック指標をアップロードできます。 検索、ソーシャル、Commerceを実行すると、コンバージョンが広告とキーワードに関連付けられます。

すべてのキャンペーンにわたって、また個々のキャンペーン、広告グループ、キーワード/広告についてパフォーマンス指標を追跡できます。 また、これらの情報を、他の広告ネットワークのデータと共に、最も基本的なレポート、高度なレポート、アシストレポートに含めることもできます。 指標のAdobe Analyticsへの書き出しはサポートされていませんが、検索、ソーシャル、Commerceでは、[ 追跡している指標  [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) を検索、ソーシャル、Commerceに同期できます。

>[!NOTE]
>
>最適化のためにトラッキングキャンペーンをポートフォリオに追加することはできません。

1. 検索、ソーシャル、Commerceでトラッキングキャンペーンを作成します。

   1. [ ダミーネットワークアカウントの詳細 ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md) を作成します。 1 つの広告ネットワーク内に複数のアカウントがある場合は、[!UICONTROL Accounts] ビューでそれらを 1 つのアカウントに統合します。

      [!DNL Naver] は、トラッキングパラメーターを広告ネットワークにアップロードするための API サポートを提供していません。 ただし、バルクシートを使用してトラッキングパラメーターを生成し、手動で広告ネットワーク内に追加することができます（手順 2 あたり）。 トラッキングパラメーターを生成するには、「[!UICONTROL EF Redirect]」トラッキングメソッドを使用する必要があります。 必要に応じて、追加パラメーターを追加できます。

      検索、ソーシャル、Commerceでは、生成する任意のトラッキング URL 内のパラメーター `ev_cl={ef_uniqueid}` が、アカウントのバルクシートに自動的に含まれます。 この一意の ID は、キャンペーンデータと、アップロードした任意のコストおよびクリックデータを照合するために使用されます。

   1. 追跡するキャンペーンの設定：

      1. 広告ネットワーク内に、アカウントの検索、ソーシャル、Commerceでトラッキングする必要があるすべてのエンティティと、それらのエンティティに必要な親エンティティを含むバルクシートファイルを作成します。

         親キャンペーンや広告グループなど、キーワードに関するデータを含めることができます。

      1. 必要に応じて、バルクシートファイルを編集して、検索、ソーシャル、Commerce[ アカウントに必要なバルクシート形式 ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md) に従う  [!DNL Naver]  うにします。

      1. 検索、ソーシャル、Commerceで [ バルクシートファイルをアップロード ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md) します。

         >[!NOTE]
         >
         >メモ：検索、ソーシャル、Commerceでは、データが広告ネットワークアカウントに投稿されません。

1. キャンペーンのトラッキングの設定：

   1. 検索、ソーシャル、Commerceで [ 新しいバルクシートファイルをダウンロード ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)」オプションを使用して「[!UICONTROL Generate Tracking URLs]」を選択します。

   「[!UICONTROL Generate Tracking URLs]」オプションを使用すると、各キーワードの [!UICONTROL Destination URL] フィールドに、[!UICONTROL Base URL] 値の先頭にプレフィックスが付いた検索、ソーシャル、Commerceのトラッキングコードが入力されます。

   以下はトラッキングを含む宛先 URL の例です。

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. ダウンロードしたバルクシートファイルの [!UICONTROL Destination URL] の値を、ネットワーク上の関連キーワード設定にコピーします。

      広告ネットワークのエディター内でファイルをネットワークにアップロードすることで、関連するエンティティに URL を追加できる場合があります。 その場合、ネットワークのデータ要件に応じて、一部の列を削除する必要が生じる場合があります。 そうでない場合は、ネットワーク上で URL を手動で入力する必要があります。

1. トラッキングしているキーワードまたは広告グループレベルのブランド広告について、広告ネットワークから毎日集計されたクリック数とコスト数のデータを定期的にダウンロードし [ クリック数とコスト数のデータをアップロード ](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)、検索、ソーシャル、Commerceを [ 必須形式 ](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md) で開きます。

   完全なアカウント階層と、組み込む指標を含めます。 検索、ソーシャル、Commerceを実行すると、アップロードされたデータが既存のキャンペーンのデータと照合されます。

1. （オプション） Web ページでAdobe Advertising コンバージョントラッキングサービスタグを使用して広告ネットワークで追跡されないコンバージョンを追跡する場合は、毎日の集計コンバージョンデータを含むフィードファイルを送信してトラッキングキャンペーンに追加します。

   詳しくは、Adobe アカウントチームにお問い合わせください。

アップロードされたすべてのトラッキングデータは、[!UICONTROL Accounts]、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups] および [!UICONTROL Keywords] ビュー内の [!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] から使用できます。 また、[!UICONTROL Insights & Reports] ビューのレポートでも使用できます。

>[!MORELIKETHIS]
>
>* [ 付録 – アカウントに必須のバルクシ  [!DNL Naver]  トデータ ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [ トラッキング専用アカウントのトラフィックおよびコ  [!DNL Naver]  バージョン指標のアップロード ](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [ トラッキング専用アカウント  [!DNL Naver]  指標データ要件 ](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [ のクリック追跡形式  [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
