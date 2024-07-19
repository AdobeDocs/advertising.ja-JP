---
title: データソ  [!DNL Google Analytics]  スとしてのビューの設定
description: ' [!DNL Google Analytics]  ビューからデータソースを設定する方法を説明します。'
role: User, Admin
exl-id: 9e299e42-4971-49ea-a515-54a97eb13e0d
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '568'
ht-degree: 0%

---

# [!DNL Google Analytics] ビューをデータソースとして設定する

*代理店管理者、代理店口座管理者、Adobe口座管理者、管理者専用*

アカウント、プロパティ、ビューの組み合わせ [!DNL Google Analytics] とに 1 つのデータソースを作成できます。

複数のプロパティまたは単一のプロパティの複数のビューの指標を統合するには、それぞれに個別のデータソースを設定します。

1. [ アカウントの統合に必要なすべての前提条件  [!DNL Google Analytics]  実行します ](data-source-prerequisites.md)。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Data Source Setup]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. [!UICONTROL Deployment Prerequisites] ダイアログで、必要なカスタムディメンション「ef_id」が [!DNL Google Analytics] アカウントに実装されていることを確認するチェックボックスを選択し、「**[!UICONTROL Continue]**」をクリックします。

   組織の他の役割によって、いくつかの前提条件が実行されている可能性があります。 前提条件について質問がある場合は、Adobeアカウントチームにお問い合わせください。

1. [ データソース設定 ](data-source-settings.md) を入力します。

   1. **[!UICONTROL Connect to [!DNL Google Analytics]]** セクションで、次の操作を行います。

      1. [!DNL Google Analytics] アカウントの数値 ID を入力します。

      1. このデータ ソースのデータへのアクセスに使用する電子メール アドレスを入力します。 メールアドレスは、[!DNL Google] アカウントに登録され、[!DNL Google Analytics] アカウントの「読み取りと分析」権限を持っている必要があります。 [ のユーザー権限の割り当て手順  [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587) を参照してください。

         >[!TIP]
         >
         >Adobe Advertising内で特定の [!DNL Google Analytics] プロパティおよびビューのみを使用できるようにするには、これらのプロパティおよびビューにのみアクセスできるメールアドレスを使用してログインします。

         >[!NOTE]
         >
         >このメールアカウントのパスワードを後で変更した場合、そのメールアカウントへの開いているすべての接続は閉じられます。 データの同期を再開するには、このページに戻って [ 再認証 ](data-source-reauthenticate.md) してください。

      1. チェックボックスをオンにして、Adobe Advertisingがアカウントの指標にアクセスすることを許可します。

      1. 「**[!UICONTROL Authenticate]**」をクリックします。

   1. 「[!UICONTROL Account Details]」セクションで、インポートする指標のプロパティとビューを指定します。 さらに、「ef_id」クエリ文字列パラメーターの値が入力されたカスタムディメンションを指定します。

   1. 「[!UICONTROL Import Metrics]」セクションで、フィードに含める指標を指定します。

      自動的に含まれる [!UICONTROL Pageviews]、[!UICONTROL Sessions]、[!UICONTROL Bounces]、[!UICONTROL Session Duration] は削除できません。 データを使用せずに、最大 16 個の有効な指標または指標を追加できます。

      >[!WARNING]
      >
      >[!DNL Google Analytics] では、1 つのデータフィードに最大 10 個の指標を使用できます。 検索、ソーシャル、Commerceでは、合計 20 個の指標を持つ最大 2 つのフィードをサポートできますが、2 番目のフィードを使用すると、[!DNL Google Analytics] への API 呼び出しが 2 倍になります。 指標が多数ある場合は、最適化の目標で使用する指標のみを選択します。 [ への API リクエストの割り当て量と呼び出し制限  [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas) の詳細を参照してください。

   1. 「[!UICONTROL Metric Tag]」セクションで、データソースの各指標に追加するタグの名前を入力します。

1. 右上で、「**[!UICONTROL Post]**」をクリックします。

   データソースの名前は「AccountName/PropertyName/ViewName」で、自動的にアクティベートされます。 データソースを一時停止するには、「[Data Sourceからのフィードの一時停止 ](data-source-pause.md) を参照してください。

   指標は、毎日のデータ同期が完了した翌日（広告主のタイムゾーンの 05:00 から開始）に利用できます。 指標が使用可能になると、[[!UICONTROL Admin] > [!UICONTROL Conversions]](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md) に表示されます。 新しいコンバージョン指標の名前はそれぞれ「`ga:backEndMetricName_propertyID_viewID`」です。ここで、「backEndMetricName」は API で使用される指標名です。 新しい各コンバージョン指標の表示名は「`friendlyMetricName_ga:MetricTag`」です。「friendlyMetricName」は [!DNL Google Analytics] に表示される指標名で、「MetricTag」はデータソース設定で定義された [!UICONTROL Metric Tag] です。

   指標を、キャンペーン管理およびポートフォリオ管理のビュー、レポート、最適化の目標に直接追加できます。

>[!MORELIKETHIS]
>
>* [ 同期  [!DNL Google Analytics]  コンバージョン指標について ](data-source-about.md)
>* [ データソースを設定するため  [!DNL Google Analytics]  前提条件 ](data-source-prerequisites.md)
>* [ データソース  [!DNL Google Analytics]  編集 ](data-source-edit.md)
>* [ データソースの同期の一時停止 ](data-source-pause.md)
>* [ データソース  [!DNL Google Analytics]  再認証 ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定 ](data-source-settings.md)
>* [ 付録 – 利用可能  [!DNL Google Analytics]  指標 ](data-source-ga-metrics.md)
