---
title: ' [!DNL Naver]  トラッキング専用アカウントを実装'
description: 広告ネットワークから直接購入した広告のパフォーマンスを追跡、報告、視覚化できるように、 [!DNL Naver]  アカウントのトラッキングキャンペーンを設定する方法について説明します。
exl-id: acbaf4f0-eb55-4788-bc84-c3181d635f1d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/ny0Bdmm-faAvcnnS77oGVJGwGr3tAHOtFpQ-EGhcBVs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: baec698f16aafc163adf2c4cfa76c92af7e1ad61
workflow-type: tm+mt
source-wordcount: 687
ht-degree: 0%

---

# [!DNL Naver]個のトラッキング専用アカウントを実装

*[!DNL Naver]アカウントのみ*

[!DNL Naver] アカウントに対してトラッキングキャンペーンを作成して、広告ネットワークから直接購入した広告のパフォーマンスを追跡、報告、可視化できます。 Search, Social, &amp; Commerceでは、データが広告ネットワークと同期されず、トラッキングが自動的にアップロードされず、アカウントの入札も行われません。

トラッキング施策では、既存の施策、広告グループ、キーワードをレプリケートします。 Search, Social, &amp; Commerceでアカウント構造を作成し、広告ネットワーク内の元のキャンペーンにトラッキングを追加したら、キーワードまたは広告の毎日のネットワークトラフィック指標をアップロードできます。 Search, Social, &amp; Commerceは、コンバージョンが広告やキーワードに起因するものであると考えます。

あらゆるキャンペーンをまたいで、個々のキャンペーン、広告グループ、キーワード/広告のパフォーマンス指標を追跡できます。 また、最も基本的なレポート、高度なレポート、アシストレポートに、他の広告ネットワークのデータなどの情報を含めることもできます。 Adobe Analyticsへの指標の書き出しのサポートは利用できませんが、Search, Social, &amp; Commerceでは、 [!DNL Analytics][&#128279;](/help/integrations/analytics/analytics-data-in-advertising.md)でトラッキングしている指標をSearch, Social, &amp; Commerceに同期できます。

>[!NOTE]
>
>最適化のためにトラッキングキャンペーンをポートフォリオに追加することはできません。

1. Search, Social, &amp; Commerceでトラッキング施策を作成する：

   1. [&#x200B; ダミーネットワークアカウントの詳細](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)を作成します。 1つの広告ネットワーク内に複数のアカウントがある場合は、[!UICONTROL Accounts] ビューで1つのアカウントに統合します。

      [!DNL Naver]は、トラッキングパラメーターを広告ネットワークにアップロードするためのAPI サポートを提供していません。 ただし、バルクシートを使用してトラッキングパラメーターを生成し、広告ネットワーク内で手動で追加できます（手順2に従います）。 トラッキングパラメーターを生成するには、「[!UICONTROL EF Redirect]」トラッキングメソッドを使用する必要があります。 必要に応じて、任意の追加パラメーターを追加できます。

      Search, Social, &amp; Commerceでは、アカウントのバルクシート内で生成されるトラッキング URLにパラメーター`ev_cl={ef_uniqueid}`が自動的に含まれます。 この一意のIDは、キャンペーンデータと任意のコストを照合し、アップロードしたデータをクリックするために使用されます。

   1. 追跡するキャンペーンを設定：

      1. 広告ネットワーク内で、アカウントの検索、ソーシャル、およびCommerceをトラッキングするためにすべてのエンティティと必要な親エンティティを含むバルクシートファイルを作成します。

         親キャンペーンや広告グループを含む、キーワードに関するデータを含めることができます。

      1. 必要に応じて、Bulksheet ファイルを編集し、 [!DNL Naver] accounts[&#128279;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)に必要なSearch, Social, &amp; Commerce Bulksheet フォーマットに従います。

      1. Search, Social, &amp; Commerceで、[&#x200B; バルクシート ファイルをアップロード &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md)。

         >[!NOTE]
         >
         >注意：Search, Social, &amp; Commerceでは、アドネットワークアカウントにデータを投稿しません。

1. キャンペーンのトラッキングを設定します。

   1. Search, Social, &amp; Commerceで、「[!UICONTROL Generate Tracking URLs]」オプションを使用して[新しいバルクシート ファイル &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)をダウンロードします。

   「[!UICONTROL Generate Tracking URLs]」オプションを使用すると、キーワードごとに[!UICONTROL Destination URL] フィールドに[!UICONTROL Base URL]値の前に検索、ソーシャル、およびCommerce トラッキングコードが入力されます。

   トラッキングを使用した宛先URLの例を次に示します。

   `http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com`

   1. ダウンロードしたバルクシート ファイルの[!UICONTROL Destination URL]値を、ネットワーク上の関連するキーワード設定にコピーします。

      ファイルを広告ネットワークのエディター内のネットワークにアップロードすることで、関連するエンティティにURLを追加できます。 その場合、ネットワークのデータ要件に従って、一部の列を削除する必要がある場合があります。 それ以外の場合は、ネットワーク上でURLを手動で入力する必要があります。

1. 追跡中のキーワードまたは広告グループレベルのブランド広告について、広告ネットワークから毎日集計されたクリックとコストのデータを定期的にダウンロードし、[&#x200B; クリックとコストのデータを](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)検索、ソーシャル、Commerceに[必要なフォーマット &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)でアップロードします。

   完全なアカウント階層と、含める指標を含めます。 Search, Social, &amp; Commerceは、アップロードしたデータを、既存の施策のデータと照合して管理します。

1. （オプション） web ページでAdobe Advertisingのコンバージョントラッキングサービスタグを使用して、広告ネットワークでトラッキングされていないコンバージョンをトラッキングする場合は、毎日の集約コンバージョンデータを含むフィードファイルを送信して、トラッキングキャンペーンに追加します。

   詳しくは、Adobe アカウントチームにお問い合わせください。

アップロードされたすべてのトラッキングデータは、[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns]から、[!UICONTROL Accounts]、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、および[!UICONTROL Keywords]のビューで利用できます。 [!UICONTROL Insights & Reports] ビューのレポートでも使用できます。

>[!MORELIKETHIS]
>
>* [付録 –  [!DNL Naver]  アカウント &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)に必要なバルクシート データ
>* [&#x200B; トラッキング専用アカウント  [!DNL Naver] のトラフィックとコンバージョン指標をアップロード &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>*  [!DNL Naver]  トラッキング専用アカウント [&#128279;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)の指標データ要件
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)の クリックトラッキング形式
