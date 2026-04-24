---
title: Set up data collection, data transfer, and reporting
description: Learn how to set up data collection, data transfer, and reporting.
feature: Integration with Adobe Customer Journey Analytics
exl-id: a955e2b0-ea1b-4b5c-937b-f8c66603cd36
TQID: https://experienceleague.adobe.com/u6xL6FuW-TwqAkse3VTS3zcyt-10Cv-ADTZLJTiWWT8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1792
ht-degree: 0%

---

# Set up data collection, data transfer, and reporting

*Beta機能*

The following tasks are required to view Advertising Cloud data in Customer Journey Analytics.

1. (Your organization&#39;s web analyst; optional) [Collect historical data for AMO IDs and EF IDs](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}.

   この手順は、[!DNL Analytics for Advertising]の広告主にのみ適用されます。

1. （組織のAdobe Experience Platform サイト管理者） [Experience Platformでデータ収集を設定し、コンバージョン トラッキング タグを実装する](#data-collection)。

1. （組織のCustomer Journey Analytics サイト管理者） [Customer Journey AnalyticsでExperience Platform データセットへの接続を作成](#dataset-connection)。

1. （組織のweb アナリスト） [Customer Journey Analyticsでデータビューを設定する](#cja-data-views)。

1. （組織のweb アナリスト） [Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定します](#cja-reports)。

以下の節では、詳細な手順を示します。これには、統合に必要なタスクと設定が含まれますが、ワークフロー内で使用可能なすべての機能を説明するものではありません。 詳しくは、リンクされたリソースを参照してください。

## Adobe Experience Platformとweb サイトでのデータ収集の設定 {#data-collection}

Experience Platformでデータ収集を設定し、コンバージョントラッキングタグを実装するには、次のタスクが必要です。 組織のExperience Platform サイト管理者は、これらのタスクを実行できますが、組織のIT部門がトラッキングタグのデプロイを支援する必要がある場合があります。

### Adobe Adobe AdvertisingからExperience Platform Edge Networkに、データセットとしてデータを収集して送信します

1. Experience Platformでは、[Experience Data Model （XDM）を使用して収集するデータの手動スキーマ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas)を定義します。

   * [!UICONTROL Schema Details]で、サイトイベントをキャプチャするスキーマのベースクラスとして&#x200B;**[!UICONTROL Experience Event]**&#x200B;を選択します。 スキーマに名前を付けて、**[!UICONTROL Finish]**&#x200B;をクリックします。

   * 左側のパネルで、フィールドグループ [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)を追加して、Adobe Advertisingに固有のフィールドを追加します。 最低でも、[AMO IDとEF ID](ids.md)を含む`trackingCode`および`trackingIdentities` プロパティを持つconversionDetails オブジェクトを含めてください。 その他のフィールドはオプションです。

   * （オプション）必要に応じてフィールドグループを追加し、データフィールドをAdobe Advertising データに接続します。

   **注意：**&#x200B;複数のスキーマを作成できますが、次の手順で作成するスキーマは、データセットごと、およびデータストリームごとに1つしか使用できません。

1. [&#x200B; スキーマに基づいてデータセット &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create)を作成し、イベントデータの収集を保存および管理します。

   * **[!UICONTROL Create dataset from schema]**&#x200B;のオプションを選択し、スキーマを選択します。

     Adobe Advertisingは、イベントデータセットに基づいて、関連する概要指標データ（コンバージョン値など）とルックアップデータ（ディメンション/分類メタデータ、Adobe Advertising キャンペーン名など）の追加データセットを作成します。 データセットのデータは、毎日Experience Platformに入力されます。

1. [&#x200B; スキーマのデータストリーム &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)を作成します。

   * [!UICONTROL Mapping schema]設定で、スキーマを選択します。

   * Add and enable the services `Adobe Advertising` and `Adobe Experience Platform` to the datastream.

     These services enable the Edge Network to store the dataset and to route it to Adobe Advertising.

   * For the [!UICONTROL Event dataset] setting, select your dataset.

     Each datastream can insert data into only one dataset.

### Send your organization&#39;s website data to your Experience Platform datastream

1. Use Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) (formerly known as [!DNL Launch]) to generate a JavaScript tag to send your organization&#39;s website data to the datastream.

   * Create a tag property, which is the container for the tag configuration.

   * For your property, [install the extension &quot;Adobe Experience Platform Web SDK&quot;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) from the extensions catalog.

     This extension sends data from your web properties to Adobe CX Enterprise via the Experience Platform Edge Network.

     Don&#39;t use the Adobe Advertising extension.

   * Create a [custom Web SDK build](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build):

      * In the [!UICONTROL Custom build components] section, enable the **Advertising** component.

        This component includes all JavaScript code needed for Adobe Advertising in the tag. It also adds an &quot;Advertising&quot; setting in tag rules (which are optional) to define how advertising data is used for attribution measurement.

        You can optionally enable additional components as needed.

      * In the [!UICONTROL SDK Instances] section:

         * In the [!UICONTROL Datastreams] settings, select the datastream to use for each of your web environments (production, staging, development).

         * (Organizations with Adobe Advertising DSP only) In the [[!UICONTROL Adobe Advertising] settings](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising), enable **[!UICONTROL Adobe Advertising DSP]** to permit view-through tracking and specify the advertisers for which to enable view-through tracking. You can optionally collect IDs from universal IDs.

           If your advertisers aren&#39;t listed, then enter the advertiser ID for each advertiser.

         * Save the build.

   * (Optional) [Create rules](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules) as needed to determine when Web SDK should send data to the Edge Network.

      * For `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` actions, use the [[!UICONTROL Advertising] setting](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising) to define how advertising data is used for attribution measurement. This setting is helpful when the rule includes a sequence of multiple actions and is available only when you&#39;ve selected the &quot;[!UICONTROL Advertising]&quot; component for the custom build component.

   * Create [data elements](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) as needed to map variables on your website to the structure of the XDM schema you created previously.

1. [Publish the tag](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) to a test environment in which you can iterate on the development of tags.

1. Validate delivery of the datasets, and then [publish the tag to your live production environment](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow).

   Your organization&#39;s IT department or other group may need to schedule, or be informed about, the tag deployment.

## Create a connection to your Experience Platform datasets in Customer Journey Analytics {#dataset-connection}

Follow these steps to pull Adobe Advertising data from your Experience Platform datasets into Customer Journey Analytics. Your organization&#39;s site administrator for Customer Journey Analytics can perform these tasks.

1. In Customer Journey Analytics, [create a connection](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection) that includes your Experience Platform datasets and schema.

   **Note:** Currently, you must send data for all DSP and Search, Social, &amp; Commerce accounts to a single Experience Platform instance and sandbox.

   * Add your Experience Platform event (metrics) dataset, summary (metrics) dataset, and dimensions (classifications/metadata) dataset.

     Your team created the event dataset, and Adobe Advertising created the summary and dimensions datasets based on your event dataset.

     You can optionally include additional datasets as needed.

   * Map the dimensions dataset to the events dataset:

      1. Open the settings for the dimension dataset.

         The heading on the settings page is &quot;[!UICONTROL Lookup Dataset],&quot; which indicates that you can join your dimensions dataset with one of your metric-specific datasets.

      1. In the [!UICONTROL Adobe Advertising Dimensions] section, map the dimensions dataset to the events dataset:

         1. For the [!UICONTROL Key] field, select the field to use as the key for the dimensions dataset: `Adobe Advertising ID` (which is same as the `trackingCode` field in the schema).

         1. For the [!UICONTROL Matching key] field, select the field to use as the matching key for the events dataset. The available field names include the dataset name in parentheses. For example, if you&#39;re mapping your dimensions dataset to your events dataset, select `Tracking Code (Event datasets)`.

         Later, you&#39;ll also map the events dataset to the summary dataset when you set up your data view(#cja-data-views).

1. After a couple of hours, verify that the data is available in Customer Journey Analytics.

   1. In Customer Journey Analytics, go to **[!UICONTROL Connections]** and select your connection.

   1. In the list of data sets displayed, verify that the &quot;[!UICONTROL Number of Records]&quot; report shows that data was added.

## Set up data views in Customer Journey Analytics {#cja-data-views}

In Customer Journey Analytics, create one or more data views to define the metrics and dimensions for reporting. web アナリストはこれらのタスクを実行できます。

1. Customer Journey Analyticsで、[&#x200B; データビューを作成](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 次の情報を含めるようにビューを設定します。

   * Adobe Analytics アカウントをお持ちの場合は、「[!UICONTROL Configure]」タブの「[!UICONTROL Calendar]」セクションにある「[!DNL Analytics]」アカウントの「[!UICONTROL Time Zone]」を使用してください。

   * 「[!UICONTROL Components]」タブ：

      * ディメンション、イベント、概要データセットを追加します。

      * イベント（指標）データセットとディメンション（分類/メタデータ）データセットから指標を選択して、データビューに含めます。

        これらの2つのデータセットは、最後の[手順](#dataset-connection)で作成した接続に既に結合されています。

      * イベントデータセットを、まだ何にも結合されていないサマリーデータセットに結合します。

         * Customer Journey Analyticsで使用可能にする概要データを含むディメンションごとに、[派生フィールドを作成](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields)。

           例えば、キャンペーンの概要データを表示するには、ディメンション `Adobe Advertising Campaign`の派生フィールドを作成します。

           一致するキー`trackingCode` （Adobe Advertising IDのスキーマフィールド）を使用して、2つのデータセットをリンクします。

            * 派生ルールビルダーの[!UICONTROL Lookup] セクションで、次の操作を行います。

               * **[!UICONTROL Value]** フィールドで、指標の概要データセットから「[!UICONTROL Tracking Code]」を選択します。

               * **[!UICONTROL Lookup dataset]** フィールドで、ディメンション データセット（「Adobe Advertising Classification」など）を選択します。

               * **[!UICONTROL Matching Key]** フィールドの分類データセットから「[!UICONTROL Tracking Code]」を選択します。

               * **[!UICONTROL Values to return]** フィールドで、分類データセットからディメンション （「[!UICONTROL Adobe Advertising Campaign]」など）を選択します。

           派生フィールド名には「（DF）」が追加されます（例：`Adobe Advertising Campaign(DF)`）。

         * 派生フィールドごとに：

            * [!UICONTROL Included components] セクションで、派生フィールドを追加します。

              同じディメンションに2つの名前が一覧表示されるようになりました（例：「Adobe Advertising Campaign （DF）」（派生フィールド）と「Adobe Advertising Campaign」（サマリーデータセットのフィールド））。

            * サマリーデータセット内のディメンション（「Adobe Advertising Campaign」など）を選択し、データセットの設定を編集します。

              設定は右側で開きます。

               * 「データグループの概要」セクションで、「**[!UICONTROL Create grouping]**」オプションを選択します。

               * **[!UICONTROL Dimension]** フィールドで、「Adobe Advertising Campaign （DF）」など「（DF）」が付加された派生フィールドを選択します。

               * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

## Set up reports and visualizations in Customer Journey Analytics Workspace {#cja-reports}

In Customer Journey Analytics Workspace, follow these steps to configure reports and visualizations. web アナリストはこれらのタスクを実行できます。

1. [Create a project](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) in Workspace to build reports and visualizations based on the dimensions and metrics configured within the data view.

1. (If you have data from [!DNL Google Ads] or [!DNL Microsoft Advertising]) Create a report of publisher-tracked conversions using fields for ad network-specific metrics, which are grouped as `googleConversions` and `microsoftConversions`.

>[!MORELIKETHIS]
>
>* [Overview](overview.md)
>* [Prerequisites](prerequisites.md)
>* [Adobe Advertising IDs used by [!DNL Customer Journey Analytics]](ids.md)
>* [Adobe Advertising metrics and dimensions in Customer Journey Analytics](advertising-data-in-cja.md)
>* [Collect historical data for AMO IDs and EF IDs for use in Adobe Customer Journey Analytics](/help/integrations/analytics/rvars-to-evars.md).
>* [Customer Journey Analytics Guide](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [User guide for Adobe Analytics users](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
