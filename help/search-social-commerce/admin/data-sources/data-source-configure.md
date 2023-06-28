---
title: の設定 [!DNL Google Analytics] データソースとして表示
description: データソースを [!DNL Google Analytics] 表示
role: User, Admin
exl-id: 583cf9aa-861c-4faf-a707-1def4e983b93
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '576'
ht-degree: 0%

---

# の設定 [!DNL Google Analytics] データソースとして表示

*代理店管理者、代理店のアカウントマネージャ、Adobeのアカウントマネージャ、および管理者のみ*

データソースは、 [!DNL Google Analytics] アカウント、プロパティ、ビューの組み合わせ。

単一のプロパティに対して複数のプロパティの指標や複数の表示の指標を統合するには、それぞれに個別のデータソースを設定します。

1. [の統合に関するすべての前提条件を実行します。 [!DNL Google Analytics] アカウント](data-source-prerequisites.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 内 [!UICONTROL Deployment Prerequisites] ダイアログで、必要なカスタム寸法「ef_id」が [!DNL Google Analytics] アカウントを選択し、「 **[!UICONTROL Continue]**.

   一部の前提条件が、組織の他の役割によって実行されている可能性があります。 前提条件についてご質問がある場合は、Adobeアカウントチームにお問い合わせください。

1. 次を入力します。 [データソース設定](data-source-settings.md):

   1. 内 **[!UICONTROL Connect to [!DNL Google Analytics]]** セクションで、以下の操作を実行します。

      1. の数値 ID を入力します。 [!DNL Google Analytics] アカウント

      1. このデータソースのデータへのアクセスに使用する電子メールアドレスを入力します。 電子メールアドレスを [!DNL Google] アカウントに追加し、 [!DNL Google Analytics] アカウント 詳しくは、 [でのユーザー権限の割り当て手順 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >特定の [!DNL Google Analytics] プロパティとビューは、Adobe Advertising内で使用できます。プロパティとビューにのみアクセスできる電子メールアドレスを使用してログインします。

         >[!NOTE]
         >
         >後でこの電子メールアカウントのパスワードを変更すると、電子メールアカウントへのオープン接続はすべて閉じられます。 データの同期を再開するには、このページに戻り、 [再認証](data-source-reauthenticate.md).

      1. 「 」チェックボックスを選択して、Adobe広告がアカウントの指標にアクセスすることを許可します。

      1. クリック **[!UICONTROL Authenticate]**.

   1. 内 [!UICONTROL Account Details] 「 」セクションで、インポートする指標のプロパティと表示を指定します。 また、「ef_id」クエリー文字列パラメーターの値を使用して設定されるカスタムディメンションを指定します。

   1. 内 [!UICONTROL Import Metrics] セクションで、フィードに含める指標を指定します。

      削除できません [!UICONTROL Pageviews], [!UICONTROL Sessions], [!UICONTROL Bounces]または [!UICONTROL Session Duration]：自動的に含まれます。 データを含まない有効な指標または指標を最大 16 個追加できます。

      >[!WARNING]
      >
      >[!DNL Google Analytics] では、1 つのデータフィードで最大 10 個の指標を許可します。 検索、ソーシャル、コマースでは、合計 20 個の指標を持つ最大 2 つのフィードをサポートできますが、2 番目のフィードを使用すると、 [!DNL Google Analytics]. 指標が多い場合は、最適化の目的で使用する指標のみを選択します。 詳しくは、 [への API リクエストのクォータと呼び出し制限 [!DNL Google Analytics]](https://developers.google.com/analytics/devguides/reporting/core/v4/limits-quotas).

   1. 内 [!UICONTROL Metric Tag] 「 」セクションで、データソースの各指標に追加するタグの名前を入力します。

1. 右上で、 **[!UICONTROL Post]**.

   データソースの名前は「AccountName/PropertyName/ViewName」で、自動的にアクティブ化されます。 データソースを一時停止するには、[データソースからのフィードの一時停止](data-source-pause.md).&quot;

   指標は、毎日のデータ同期が完了した翌日に使用できます。この日のデータ同期は、広告主のタイムゾーンの 05:00 に開始されます。 指標が使用可能になると、 [[!UICONTROL Admin] > [!UICONTROL Transaction Properties]](/help/search-social-commerce/admin/transaction-properties/transaction-property-about.md). 新しいトランザクションプロパティの名前は、それぞれ「`ga:backEndMetricName_propertyID_viewID`、「 」（「backEndMetricName」は API で使用される指標名） 新しいトランザクションプロパティごとに表示名は「`friendlyMetricName_ga:MetricTag`(「friendlyMetricName」は、 [!DNL Google Analytics] と「MetricTag」は [!UICONTROL Metric Tag] データソース設定で定義されます。

   キャンペーン管理、ポートフォリオ管理のビュー、レポート、最適化の目標に指標を直接追加できます。

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics] コンバージョン指標](data-source-about.md)
>* [の設定の前提条件 [!DNL Google Analytics] データソース](data-source-prerequisites.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [の再認証 [!DNL Google Analytics] データソース](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] データソース設定](data-source-settings.md)
>* [付録 — 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
