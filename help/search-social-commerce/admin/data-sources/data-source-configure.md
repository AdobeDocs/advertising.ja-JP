---
title: ' [!DNL Google Analytics]  ビューをデータソースとして設定'
description: ' [!DNL Google Analytics]  ビューからデータソースを設定する方法について説明します。'
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/Tvl3PF1mPSWuoWdVVreAoo6aXe3Kg9-9DXsOz3porOI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 568
ht-degree: 0%

---

# [!DNL Google Analytics] ビューをデータソースとして設定

*代理店の管理者、代理店のアカウントマネージャー、Adobeのアカウントマネージャー、および管理者のみ*

[!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせごとに1つのデータソースを作成できます。

複数のプロパティまたは1つのプロパティの複数のビューの指標を統合するには、それぞれに個別のデータソースを設定します。

1. [&#x200B; アカウント  [!DNL Google Analytics] を統合するためのすべての前提条件を実行します](data-source-prerequisites.md)。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. [!UICONTROL Deployment Prerequisites] ダイアログで、チェックボックスを選択して、必要なカスタムディメンション「ef_id」が[!DNL Google Analytics] アカウントに実装されていることを確認し、**[!UICONTROL Continue]**&#x200B;をクリックします。

   一部の前提条件は、組織内の他の役割によって実行された可能性があります。 前提条件についてご不明な点がある場合は、Adobeアカウントチームにお問い合わせください。

1. [&#x200B; データソース設定](data-source-settings.md)を入力します。

   1. 「**[!UICONTROL Connect to [!DNL Google Analytics]]**」セクションで、次の操作を行います。

      1. [!DNL Google Analytics] アカウントの数値IDを入力してください。

      1. このデータソースのデータへのアクセスに使用する電子メールアドレスを入力してください。 メールアドレスは[!DNL Google] アカウントに登録し、[!DNL Google Analytics] アカウントに「読み取りと分析」権限を持っている必要があります。 [&#x200B; [!DNL Google Analytics]でユーザー権限を割り当てる方法については、](https://support.google.com/analytics/answer/9305587)の手順を参照してください。

         >[!TIP]
         >
         >Adobe Advertising内で特定の[!DNL Google Analytics]個のプロパティとビューのみを使用できるようにするには、それらのプロパティとビューのみにアクセスできるメールアドレスを使用してログインします。

         >[!NOTE]
         >
         >後でこの電子メールアカウントのパスワードを変更すると、電子メールアカウントに対して開いているすべての接続が閉じられます。 データの同期を再開するには、このページに戻り、[再認証](data-source-reauthenticate.md)してください。

      1. このチェックボックスをオンにすると、Adobe Advertisingによるアカウントの指標へのアクセスが許可されます。

      1. **[!UICONTROL Authenticate]**&#x200B;をクリックします。

   1. [!UICONTROL Account Details] セクションで、読み込む指標のプロパティとビューを指定します。 さらに、「ef_id」クエリ文字列パラメーターの値が入力されたカスタムディメンションを指定します。

   1. [!UICONTROL Import Metrics] セクションで、フィードに含める指標を指定します。

      自動的に含まれている[!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]または[!UICONTROL Session Duration]は削除できません。 データを含めずに、最大16個の有効な指標または指標を追加できます。

      >[!WARNING]
      >
      >[!DNL Google Analytics]は、1つのデータフィードで最大10個の指標を許可します。 Search, Social, &amp; Commerceは、合計20個の指標で最大2つのフィードをサポートできますが、2番目のフィードを使用すると、API呼び出しが[!DNL Google Analytics]に倍増します。 多数の指標がある場合は、目的で最適化に使用する指標のみを選択します。 [&#x200B; [!DNL Google Analytics]へのAPI リクエストの](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas)割り当てと呼び出し制限について詳しく説明します。

   1. 「[!UICONTROL Metric Tag]」セクションで、データソースの各指標に追加するタグの名前を入力します。

1. 右上の「**[!UICONTROL Post]**」をクリックします。

   データソースの名前は「AccountName > PropertyName > ViewName」で、自動的にアクティブ化されます。 データソースを一時停止するには、「[Data Sourceからのフィードの一時停止](data-source-pause.md)」を参照してください。

   指標は、広告主のタイムゾーンの05:00から始まる毎日のデータ同期が完了した翌日に使用できます。 指標が使用可能になると、[[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)に表示されます。 新しいコンバージョン指標は&quot;`ga:backEndMetricName_propertyID_viewID`&quot;という名前で、&quot;backEndMetricName&quot;はAPIで使用される指標の名前です。 新しいコンバージョン指標の表示名は「`friendlyMetricName_ga:MetricTag`」です。「friendlyMetricName」は[!DNL Google Analytics]に表示される指標の名前、「MetricTag」はデータソース設定で定義されている[!UICONTROL Metric Tag]です。

   キャンペーン管理、ポートフォリオ管理のビュー、レポート、最適化目標に指標を直接追加できます。

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics]  コンバージョン指標](data-source-about.md)
>* [&#x200B; データソースを設定するための前提条件 [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースの編集 [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期を一時停止](data-source-pause.md)
>* [&#x200B; データソースを再認証 [!DNL Google Analytics] します](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定](data-source-settings.md)
>* [付録 – 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
