---
title: データ収集、データ転送、レポートの設定
description: データ収集、データ転送、レポートの設定方法について説明します。
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
source-git-commit: a93c33ee47bd1a8df137a69598b367e985def4ee
workflow-type: tm+mt
source-wordcount: 1802
ht-degree: 0%

---

# データ収集、データ転送、レポートの設定

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]*&#x200B;の広告主

[!DNL Analytics for Advertising]のみ&#x200B;*を持たない*&#x200B;広告主

[Adobe Experience Platform [!DNL Web SDK]](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html)を使用してAdobe AdvertisingとCustomer Journey Analytics間でデータをネイティブに交換するには、次のタスクが必要です。 データの転送とアトリビューションはローンチ後に開始されます。履歴データは含まれません。

これらのタスクは、[!DNL Analytics for Advertising]を持つ広告主には必要ありません。

1. （組織のAdobe Experience Platform サイト管理者） [Experience Platformでデータ収集を設定し、コンバージョン トラッキング タグを実装する](#data-collection)。

1. （組織のCustomer Journey Analytics サイト管理者） [Customer Journey AnalyticsでExperience Platform データセットへの接続を作成](#dataset-connection)。

1. （組織のweb アナリスト） [Customer Journey Analyticsでデータビューを設定する](#cja-data-views)。

1. （組織のweb アナリスト） [Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定します](#cja-reports)。

以下の節では、詳細な手順を示します。これには、統合に必要なタスクと設定が含まれますが、ワークフロー内で使用可能なすべての機能を説明するものではありません。 詳しくは、リンクされたリソースを参照してください。

## Adobe Experience Platformとweb サイトでのデータ収集の設定 {#data-collection}

Experience Platformでデータ収集を設定し、コンバージョントラッキングタグを実装するには、次のタスクが必要です。 組織のExperience Platform サイト管理者は、これらのタスクを実行できますが、組織のIT部門がトラッキングタグのデプロイを支援する必要がある場合があります。

### Adobe Adobe AdvertisingからExperience Platform Edge Networkに、データセットとしてデータを収集して送信します

この手順には、スキーマの作成が含まれます。 オプションで、代わりに既存のスキーマを編集できます。その場合、データセットやデータストリームを作成する必要はありません。

1. Experience Platformでは、[Experience Data Model （XDM）を使用して収集するデータの手動スキーマ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas)を定義します。

   * [!UICONTROL Schema Details]で、サイトイベントをキャプチャするスキーマのベースクラスとして&#x200B;**[!UICONTROL Experience Event]**&#x200B;を選択します。 スキーマに名前を付けて、**[!UICONTROL Finish]**&#x200B;をクリックします。

   * 左側のパネルで、フィールドグループ [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)を追加して、Adobe Advertisingに固有のフィールドを追加します。 最低でも、[AMO IDとEF ID](ids.md)を含む`trackingCode`および`trackingIdentities` プロパティを持つconversionDetails オブジェクトを含めてください。 その他のフィールドはオプションです。 他の設定は必要ありません。

   * （オプション）必要に応じてフィールドグループを追加し、データフィールドをAdobe Advertising データに接続します。

   **注意：**&#x200B;複数のスキーマを作成できますが、次の手順で作成するスキーマは、データセットごと、およびデータストリームごとに1つしか使用できません。

1. [&#x200B; スキーマに基づいてデータセット &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create)を作成し、イベントデータの収集を保存および管理します。 これは&#x200B;*イベントデータセット*&#x200B;になります。 データセットを使用して既存のスキーマを編集する場合は、この手順をスキップできます。

   * **[!UICONTROL Create dataset from schema]**&#x200B;のオプションを選択し、スキーマを選択します。

     イベントデータセットに基づいて、Adobe Advertisingは、関連する概要データ（クリック数の集約やインプレッション数の集約など）を含む&#x200B;*概要データセット*&#x200B;と、*参照データセット* （ディメンション/分類メタデータを含むAdobe Advertising キャンペーン名など）の2つの追加データセットを作成します。 データセットのデータは、毎日Experience Platformに入力されます。

   >[!TIP]
   >
   >実稼動データセットを使用する前に、まずダミーイベントデータセットを作成してデータフローを検証します。

1. [&#x200B; データストリーム &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)を作成して、web サイトまたはアプリからデータを送信する場所と、受信データの処理方法を指定します。

   * [!UICONTROL Mapping schema]設定で、スキーマを選択します。

   * サービス `Adobe Advertising`および`Adobe Experience Platform`をデータストリームに追加して有効にします。

     [!UICONTROL Adobe Advertising] サービスは、広告露出をペイロードに関連付けることを有効にし、[!UICONTROL Adobe Experience Platform]は、Edge Networkがデータセットを保存し、それをAdobe Advertisingにルーティングすることを可能にします。

   * [!UICONTROL Event dataset]設定で、イベントデータセットを選択します。

     各データストリームは、1つのデータセットにのみデータを挿入できます。

### 組織のweb サイトデータをExperience Platform データストリームに送信する

Adobe TagsでAdobe Experience Platform Web SDK拡張機能を使用して、組織のweb サイトデータをExperience Platform データストリームに送信します。

>[!NOTE]
>
>Adobe タグのみがサポートされています。 スタンドアロンのExperience Platform Web SDK （`alloy.js`）またはサードパーティのタグマネージャーはサポートを利用できません。

1. Experience Platform [tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) （旧称[!DNL Launch]）を使用して、JavaScript タグを生成し、組織のweb サイトデータをデータストリームに送信します。

   * タグ設定のコンテナであるタグプロパティを作成します。

   * プロパティの場合は、拡張機能カタログから拡張機能「Adobe Experience Platform Web SDK」 [&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration)を インストールします。

     この拡張機能は、web プロパティからExperience Platform Edge Networkを介してAdobe CX Enterpriseにデータを送信します。

     Adobe Advertising拡張機能は使用しないでください。

   * [&#x200B; カスタム Web SDK ビルド &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build)を作成します。

      * [!UICONTROL Custom build components] セクションで、**Advertising** コンポーネントを有効にします。

        このコンポーネントには、Adobe Advertisingに必要なすべてのJavaScript コードがタグに含まれており、Advertising DSPとAdvertisingの検索、ソーシャル、Commerceのお客様の両方に必要です。 このコンポーネントは、アトリビューション測定に広告データを使用する方法を定義するために、タグルール（オプション）に「Advertising」設定も追加します。

        必要に応じて、追加のコンポーネントを有効にすることもできます。

      * [!UICONTROL SDK Instances] セクション：

         * [!UICONTROL Datastreams]設定で、各web環境（実稼動、ステージング、開発）で使用するデータストリームを選択します。

         * （Adobe Advertising DSPを持つ組織のみ） [[!UICONTROL Adobe Advertising]設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)で、**[!UICONTROL Adobe Advertising DSP]**&#x200B;を有効にしてビュースルートラッキングを許可し、ビュースルートラッキングを有効にする広告主を指定します。 オプションとして、組織のID5 パートナーIDや組織の[!DNL LiveRamp RampID] JavaScript コード （ats.js）へのパスを追加することで、ユニバーサル IDからIDを収集できます。

           広告主がリストにない場合は、各広告主の広告主IDを入力します。 必要に応じて、AdobeのアカウントチームにIDを確認します。

           [!DNL RampID] JavaScript パスの例：`https://launchpad-wrapper.privacymanager.io/<customer-specific-id>/launchpad-liveramp.js`

         * ビルドを保存します。

   * （オプション） Web SDKがEdge Networkにデータを送信するタイミングを決定するために、必要に応じて[&#x200B; ルール &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)を作成します。

      * `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` アクションの場合、[[!UICONTROL Advertising]設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising)を使用して、広告データをアトリビューション測定に使用する方法を定義します。 この設定は、ルールに複数のアクションのシーケンスが含まれており、カスタムビルドコンポーネントの「[!UICONTROL Advertising]」コンポーネントを選択した場合にのみ使用できます。

   * Web サイト上の変数を以前に作成したXDM スキーマの構造にマッピングするために、必要に応じて[&#x200B; データ要素](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements)を作成します。

1. [&#x200B; タグ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)をテスト環境に公開して、タグの開発を繰り返し行うことができます。

1. [3つのデータセットのそれぞれのアクティビティを確認して](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/user-guide#view-datasets)配信を検証します。

1. [&#x200B; タグをライブ実稼動環境に公開します](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)。

   組織のIT部門またはその他のグループは、タグのデプロイメントをスケジュールする必要があるか、情報を得る必要がある場合があります。

## Customer Journey AnalyticsでExperience Platform データセットへの接続を作成する {#dataset-connection}

Experience Platform データセットからAdobe Advertising データをCustomer Journey Analyticsに取り込むには、次の手順に従います。 組織のCustomer Journey Analytics サイト管理者は、これらのタスクを実行できます。

オプションで、同じ情報を持つ既存の接続を編集することもできます。

1. Customer Journey Analyticsで、[Experience Platform データセットとスキーマを含む接続](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection)を作成または編集します。

   <!-- **Note:** You must send data for all DSP and Search, Social, & Commerce accounts to a single Experience Platform instance and sandbox.  -->

   * 正しいサンドボックスが選択されていることを確認します。

   * 1日の平均イベント数（ほとんどの組織で100万件未満）を計算します。

   * Experience Platform イベント指標データセット（タイプ：`Event`）、<!-- Adobe Advertising --> イベント概要メトリックデータセット（タイプ：`Event`）、および<!-- Adobe Advertising --> ディメンション（分類/メタデータ）データセット（タイプ：`Lookup`）を追加します。

     チームがイベントデータセットを作成し、Adobe Advertisingがイベントデータセットに基づいて概要とディメンションのデータセットを作成しました。

     必要に応じて、追加のデータセットを含めることもできます。

   * データセット設定を設定します。

      * [!UICONTROL Event Dataset]設定の場合：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Use primary identity namespace]:**&#x200B;設定を有効にする

         * **[!UICONTROL Data Source Type]:** `Web Data > Others` <!-- I don't see "Others" in the screen shot example -->

         * **[!UICONTROL Import all new data]:**&#x200B;設定を有効にする

      * [!UICONTROL Lookup Dataset]設定の場合、ディメンションデータセットをイベントデータセットにマッピングします。

         * **[!UICONTROL Key]** （ディメンション データセットのキーとして使用するフィールド）: `Tracking Code` （スキーマの`trackingCode` フィールドと同じ）。

         * **[!UICONTROL Matching key]** （イベントデータセットの一致キーとして使用するフィールド）: `Tracking Code (Event datasets)`。

         * **[!UICONTROL Import all new data]:**&#x200B;設定を有効にする

      * [!UICONTROL Metrics Dataset]設定の場合：

         * **[!UICONTROL Person ID]:** `Identity Map`

         * **[!UICONTROL Timestamp]:**&#x200B;値を確認してください

         * **[!UICONTROL Import all new data]:**&#x200B;設定を有効にする

2. 3時間以内に、Customer Journey Analyticsでデータが利用可能であることを確認します。

   1. Customer Journey Analyticsで、**[!UICONTROL Connections]**&#x200B;に移動し、接続を選択します。

   2. 表示されるデータセットのリストで、「[!UICONTROL Number of Records]」レポートにデータが追加されたことを確認します。

## Customer Journey Analyticsでのデータビューの設定 {#cja-data-views}

Customer Journey Analyticsで、1つ以上のデータビューを作成して、レポートの指標とディメンションを定義します。 web アナリストはこれらのタスクを実行できます。

1. Customer Journey Analyticsで、[&#x200B; データビューを作成](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 次の情報を含めるようにビューを設定します。

   * Adobe Analytics アカウントをお持ちの場合は、「[!UICONTROL Configure]」タブの「[!UICONTROL Calendar]」セクションにある「[!DNL Analytics]」アカウントの「[!UICONTROL Time Zone]」を使用してください。

   * 「[!UICONTROL Components]」タブ：

      * ルックアップデータセット（ディメンション/分類データ）、イベントデータセット（イベントレベルのデータ）、概要データセット（クリックなどの他の指標）を追加できます。

      * イベントデータセットとルックアップデータセットから指標を選択し、データビューに含めます。

      * 「[!UICONTROL Tracking Code]」（スキーマパス `_experience.adcloud.conversionDetails.trackingCode`を持つイベントデータセットの一部）を検索します。<!-- and do what with it? Add it? Or is that what you --> **[!UICONTROL Persistence]**&#x200B;を&#x200B;*[!UICONTROL Most Recent]*&#x200B;に設定します。

<!--

Seems to not be necessary now:


       You already joined these two datasets in the connection that you created in the [last procedure](#dataset-connection).
     
     *  Join the events dataset to the summary dataset, which isn't yet joined to anything:
     
       * For each dimension with summary data that you want to be available in Customer Journey Analytics, [create a derived field](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/derived-fields).

         For example, to view summary data for campaigns, create a derived field for the dimension `Adobe Advertising Campaign`.
         
         You'll link the two datasets using the matching key `trackingCode` (which is the schema field for the Adobe Advertising ID).
       
         * In the [!UICONTROL Lookup] section of the derived rule builder:
         
           * For the **[!UICONTROL Value]** field, select "[!UICONTROL Tracking Code]" from the metrics summary dataset.

           * For the **[!UICONTROL Lookup dataset]** field, select the dimensions dataset (such as "Adobe Advertising Classification").

           * For the **[!UICONTROL Matching Key]** field, select "[!UICONTROL Tracking Code]" from the classification dataset.

           * For the **[!UICONTROL Values to return]** field, select the dimension (such as "[!UICONTROL Adobe Advertising Campaign]")" from the classification dataset.
         
         The derived field name is appended with "(DF)", such as `Adobe Advertising Campaign(DF)`. 
         
       * For each derived field:
       
         * In the [!UICONTROL Included components] section, add the derived field.
         
           Two names are now listed for the same dimension (for example, "Adobe Advertising Campaign(DF)" (the derived field) and "Adobe Advertising Campaign" (the field in the summary dataset)).

         * Select the dimension in the summary dataset (such as "Adobe Advertising Campaign") and edit the settings for the dataset.

           The settings open on the right.

           * In the the Summary Data Group section, select the option to **[!UICONTROL Create grouping]**.

           * For the **[!UICONTROL Dimension]** field, select the derived field (which is appended with "(DF)," such as "Adobe Advertising Campaign(DF)").
         
           * Select the option to **[!UICONTROL Hide in reporting]**, which hides the derived field name in Workspace.

-->

## Customer Journey Analytics Workspaceでのレポートとビジュアライゼーションの設定 {#cja-reports}

Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定するには、次の手順に従います。 web アナリストはこれらのタスクを実行できます。

1. Workspaceで[&#x200B; プロジェクト &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)を作成し、データビュー内で設定されたディメンションと指標に基づいてレポートとビジュアライゼーションを作成します。

1つのフリーフォームテーブルで同じディメンションを使用して、概要指標とイベントデータの両方を分類できます。

1. （データが[!DNL Google Ads]または[!DNL Microsoft Advertising]の場合）広告ネットワーク固有の指標のフィールドを使用して、発行者が追跡したコンバージョンのレポートを作成します。このフィールドは`googleConversions`および`microsoftConversions`としてグループ化されます。

>[!TIP]
>
>サマリーイベントは、通常、レポートに少量の追加データを追加します。例えば、少数の追加イベント、1日に1回の追加セッション、レポートごとに1人の追加データなどが含まれます。これらの追加機能は、標準的なweb イベントと比較すると無視できます。ただし、ダミーの人物ID `00000000-0000-0000-0000-000000000000`のデータを除外することで、この追加の概要イベントデータを除外できます。
>![人物IDを使用してデータを除外する例](/help/integrations/assets/cja-report-with-person-id.png "人物IDを使用してデータを除外する例")

![&#x200B; データセットがCustomer Journey Analyticsでどのように表示されるか](/help/integrations/assets/cja-report-example.png " データセットがCustomer Journey Analyticsでどのように表示されるか")

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>* [前提条件](prerequisites.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集します](/help/integrations/analytics/rvars-to-evars.md)。
>* [&#x200B; トラブルシューティング &#x200B;](troubleshooting.md)
>* [Customer Journey Analytics ガイド &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Adobe Analytics ユーザー向けユーザーガイド &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
