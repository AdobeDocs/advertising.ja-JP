---
title: 実装方法 [!DNL Naver] トラッキング専用アカウント
description: 次の目的でトラッキングキャンペーンを設定する方法を説明します。 [!DNL Naver] 広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、および視覚化できるアカウント。
exl-id: 8013d4e8-0b4f-41a7-9c1b-10c55349930f
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '686'
ht-degree: 0%

---

# 実装方法 [!DNL Naver] トラッキング専用アカウント

*[!DNL Naver]アカウントのみ*

次の目的でトラッキングキャンペーンを作成できます： [!DNL Naver] 広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、および視覚化できるアカウント。 検索、ソーシャル、コマースでは、広告ネットワークとデータを同期したり、追跡を自動的にアップロードしたり、アカウントの入札を配置したりすることはできません。

トラッキングキャンペーンは、既存のキャンペーン、広告グループ、キーワードを複製します。 検索、ソーシャル、コマースのアカウント構造を作成し、広告ネットワーク内の元のキャンペーンにトラッキングを追加したら、キーワードまたは広告に関する毎日のネットワークトラフィック指標をアップロードできます。 その後、検索、ソーシャル、コマースは、コンバージョンを、広告とキーワードに関連付けることができます。

すべてのキャンペーン、および個々のキャンペーン、広告グループ、キーワード/広告に関するパフォーマンス指標を追跡できます。 また、他の広告ネットワークのデータに加えて、最も基本的なレポート、高度なレポート、アシストレポートに関する情報を含めることもできます。 Adobe Analyticsへの指標の書き出しはサポートされていませんが、検索、ソーシャル、コマースは同期できます [追跡している指標 [!DNL Analytics]](/help/integrations/analytics/analytics-data-in-advertising.md) を Search、Social、および Commerce に追加します。

>[!NOTE]
>
>最適化のためにトラッキングキャンペーンをポートフォリオに追加することはできません。

1. 検索、ソーシャル、コマースでトラッキングキャンペーンを作成します。

   1. 作成 [ダミーネットワークアカウントの詳細](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md). 1 つの広告ネットワーク内に複数のアカウントがある場合は、それらを [!UICONTROL Accounts] 表示。

      [!DNL Naver] では、広告ネットワークにトラッキングパラメーターをアップロードする API サポートを提供していません。 ただし、一括送信シートを使用してトラッキングパラメーターを生成し、（手順 2 に従って）広告ネットワーク内に手動で追加することができます。 トラッキングパラメーターを生成するには、[!UICONTROL EF Redirect]」トラッキングメソッド。 必要に応じて、任意の追加パラメータを追加できます。

      検索、ソーシャル、コマースでは、パラメーターが自動的に含まれます `ev_cl={ef_uniqueid}` アカウントの一括送信シート内で生成される追跡 URL 内。 この一意の ID は、任意のコストでキャンペーンデータとの照合に使用され、アップロードしたクリックデータを表示します。

   1. 追跡するキャンペーンの設定：

      1. 広告ネットワーク内で、検索、ソーシャル、コマースでアカウントを追跡するために必要なすべてのエンティティとその親エンティティを含むバルクシートファイルを作成します。

         親キャンペーンや広告グループなど、キーワードに関するデータを含めることができます。

      1. 必要に応じて、Search、Social、&amp;Commerce に従うようにバルクシートファイルを編集します。 [次に必要なバルクシートフォーマット： [!DNL Naver] アカウント](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md).

      1. 検索、ソーシャル、コマースで、 [bulksheet ファイルのアップロード](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-upload.md).

         >[!NOTE]
         >
         >注意：検索、ソーシャル、コマースでは、広告ネットワークアカウントにデータが投稿されません。

1. キャンペーンのトラッキングを設定します。

   1. 検索、ソーシャル、コマースで、 [新しい bulksheet ファイルをダウンロードする](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) オプションを「[!UICONTROL Generate Tracking URLs].&quot;

   「[!UICONTROL Generate Tracking URLs]「 」オプションを選択すると、 [!UICONTROL Destination URL] フィールドに追加します。 [!UICONTROL Base URL] の値です。

   トラッキングを使用したリンク先 URL の例を次に示します。

   ```http://pixel.everesttech.net/1234/cq?ev_sid=87&ev_cl=258e27dcec70156a667f2229020e488&url=http%3A//www.example.com```

   1. をコピーします。 [!UICONTROL Destination URL] の値を指定します。

      広告ネットワークのエディター内でネットワークにファイルをアップロードすることで、URL を関連エンティティに追加できます。 その場合は、ネットワークのデータ要件に応じて、一部の列を削除する必要が生じる場合があります。 それ以外の場合は、URL を手動でネットワークに入力する必要があります。

1. 追跡するキーワードまたは広告グループレベルのブランド広告に関して、広告ネットワークから毎日集計されたクリックとコストのデータを定期的にダウンロードし、次にコストをかけます。 [クリック数とコストのデータをアップロード](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md) 検索、ソーシャル、コマースを [必須形式](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md).

   完全なアカウント階層と、含める指標を含めます。 検索、ソーシャル、コマースは、アップロードされたデータを既存のキャンペーンのデータと照合します。

1. （オプション）Web ページでAdobe Advertisingコンバージョントラッキングサービスタグを使用して、広告ネットワーク上で追跡されていないコンバージョンを追跡する場合は、日別に集計したコンバージョンデータを含むフィードファイルを送信して、トラッキングキャンペーンに追加します。

   詳しくは、担当のAdobeアカウントチームにお問い合わせください。

アップロードされたすべてのトラッキングデータは、 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 内 [!UICONTROL Accounts], [!UICONTROL Campaigns], [!UICONTROL Ad Groups]、および [!UICONTROL Keywords] ビュー。 また、 [!UICONTROL Insights & Reports] 表示。

>[!MORELIKETHIS]
>
>* [付録 — の必須バルクシートデータ [!DNL Naver] アカウント](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)
>* [次のトラフィック指標とコンバージョン指標をアップロード： [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
>* [次の指標データ要件： [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-data-requirements.md)
>* [のクリック追跡形式 [!DNL Naver]](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)
