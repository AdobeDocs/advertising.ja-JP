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
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1587
ht-degree: 0%

---

# データ収集、データ転送、レポートの設定

*Beta機能*

Customer Journey AnalyticsでAdvertising Cloud データを表示するには、次のタスクが必要です。

1. （組織のweb アナリスト、オプション） [AMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}。

   この手順は、[!DNL Analytics for Advertising]の広告主にのみ適用されます。

1. （組織のAdobe Experience Platform サイト管理者） [Experience Platformでデータ収集を設定し、コンバージョン トラッキング タグを実装する](#data-collection)。

1. （組織のCustomer Journey Analytics サイト管理者） [Customer Journey AnalyticsでExperience Platform データセットへの接続を作成](#dataset-connection)。

1. （組織のweb アナリスト） [Customer Journey Analyticsでデータビューを設定する](#cja-data-views)。

1. （組織のweb アナリスト） [Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定します](#cja-reports)。

以下の節では、詳細な手順を示します。これには、統合に必要なタスクと設定が含まれますが、ワークフロー内で使用可能なすべての機能を説明するものではありません。 詳しくは、リンクされたリソースを参照してください。

## Adobe Experience Platformとweb サイトでのデータ収集の設定 {#data-collection}

Experience Platformでデータ収集を設定し、コンバージョントラッキングタグを実装するには、次のタスクが必要です。 組織のExperience Platform サイト管理者は、これらのタスクを実行できますが、組織のIT部門がトラッキングタグのデプロイを支援する必要がある場合があります。

### Adobe Adobe AdvertisingからExperience Platform Edge Networkに、データセットとしてデータを収集して送信します

1. Experience Platformでは、[Experience Data Model （XDM）を使用して収集するデータの手動スキーマ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/xdm/ui/resources/schemas)を定義します。

   * [!UICONTROL Schema Details]で、サイトイベントをキャプチャするスキーマのベースクラスとして&#x200B;**[!UICONTROL Experience Event]**&#x200B;を選択します。 スキーマに名前を付けて、**[!UICONTROL Finish]**&#x200B;をクリックします。

   * 左側のパネルで、フィールドグループ [Adobe Advertising Cloud ExperienceEvent Full Extension](https://experienceleague.adobe.com/ja/docs/experience-platform/xdm/field-groups/event/advertising-full-extension)を追加して、Adobe Advertisingに固有のフィールドを追加します。 最低でも、`trackingCode`AMO IDとEF ID`trackingIdentities`を含む[および](ids.md) プロパティを持つconversionDetails オブジェクトを含めてください。 その他のフィールドはオプションです。

   * （オプション）必要に応じてフィールドグループを追加し、データフィールドをAdobe Advertising データに接続します。

   **注意：**&#x200B;複数のスキーマを作成できますが、次の手順で作成するスキーマは、データセットごと、およびデータストリームごとに1つしか使用できません。

1. [&#x200B; スキーマに基づいてデータセット &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create)を作成し、イベントデータの収集を保存および管理します。

   * **[!UICONTROL Create dataset from schema]**&#x200B;のオプションを選択し、スキーマを選択します。

     Adobe Advertisingは、イベントデータセットに基づいて、関連する概要指標データ（コンバージョン値など）とルックアップデータ（ディメンション/分類メタデータ、Adobe Advertising キャンペーン名など）の追加データセットを作成します。 データセットのデータは、毎日Experience Platformに入力されます。

1. [&#x200B; スキーマのデータストリーム &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/datastreams/configure)を作成します。

   * [!UICONTROL Mapping schema]設定で、スキーマを選択します。

   * サービス `Adobe Advertising`および`Adobe Experience Platform`をデータストリームに追加して有効にします。

     これらのサービスにより、Edge Networkはデータセットを保存し、Adobe Advertisingにルーティングできます。

   * [!UICONTROL Event dataset]設定で、データセットを選択します。

     各データストリームは、1つのデータセットにのみデータを挿入できます。

### 組織のweb サイトデータをExperience Platform データストリームに送信する

1. Experience Platform [tags](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/home) （旧称[!DNL Launch]）を使用して、JavaScript タグを生成し、組織のweb サイトデータをデータストリームに送信します。

   * タグ設定のコンテナであるタグプロパティを作成します。

   * プロパティの場合は、拡張機能カタログから拡張機能「Adobe Experience Platform Web SDK」 [を](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) インストールします。

     この拡張機能は、web プロパティからExperience Platform Edge Networkを介してExperience Cloudにデータを送信します。

     Adobe Advertising拡張機能は使用しないでください。

   * [&#x200B; カスタム Web SDK ビルド &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration#custom-build)を作成します。

      * [!UICONTROL Custom build components] セクションで、**Advertising** コンポーネントを有効にします。

        このコンポーネントには、Adobe Advertisingに必要なすべてのJavaScript コードがタグに含まれます。 また、タグルール（オプション）に「Advertising」設定を追加して、広告データをアトリビューション測定に使用する方法を定義します。

        必要に応じて、追加のコンポーネントを有効にすることもできます。

      * [!UICONTROL SDK Instances] セクション：

         * [!UICONTROL Datastreams]設定で、各web環境（実稼動、ステージング、開発）で使用するデータストリームを選択します。

         * （Adobe Advertising DSPを持つ組織のみ） [[!UICONTROL Adobe Advertising]設定](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)で、**[!UICONTROL Adobe Advertising DSP]**&#x200B;を有効にしてビュースルートラッキングを許可し、ビュースルートラッキングを有効にする広告主を指定します。 オプションで、ユニバーサル IDからIDを収集できます。

           広告主がリストにない場合は、各広告主の広告主IDを入力します。

         * ビルドを保存します。

   * （オプション） Web SDKがEdge Networkにデータを送信するタイミングを決定するために、必要に応じて[&#x200B; ルール &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/ui/rules)を作成します。

      * `[sendEvent](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/actions/send-event)` アクションの場合、[[!UICONTROL Advertising]設定](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/action-types#advertising)を使用して、広告データをアトリビューション測定に使用する方法を定義します。 この設定は、ルールに複数のアクションのシーケンスが含まれており、カスタムビルドコンポーネントの「[!UICONTROL Advertising]」コンポーネントを選択した場合にのみ使用できます。

   * Web サイト上の変数を以前に作成したXDM スキーマの構造にマッピングするために、必要に応じて[&#x200B; データ要素](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/ui/data-elements)を作成します。

1. [&#x200B; タグ &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/publish/publishing-flow)をテスト環境に公開して、タグの開発を繰り返し行うことができます。

1. データセットの配信を検証し、[実稼働環境にタグを公開します](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/publish/publishing-flow)。

   組織のIT部門またはその他のグループは、タグのデプロイメントをスケジュールする必要があるか、情報を得る必要がある場合があります。

## Customer Journey AnalyticsでExperience Platform データセットへの接続を作成する {#dataset-connection}

Experience Platform データセットからAdobe Advertising データをCustomer Journey Analyticsに取り込むには、次の手順に従います。 組織のCustomer Journey Analytics サイト管理者は、これらのタスクを実行できます。

1. Customer Journey Analyticsで、[Experience Platform データセットとスキーマを含む接続](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-connections/create-connection)を作成します。

   **メモ：**&#x200B;現在、すべてのDSP アカウントとSearch、Social、およびCommerce アカウントのデータを1つのExperience Platform インスタンスとサンドボックスに送信する必要があります。

   * Experience Platform イベント（指標）データセット、概要（指標）データセット、ディメンション（分類/メタデータ）データセットを追加します。

     チームがイベントデータセットを作成し、Adobe Advertisingがイベントデータセットに基づいて概要とディメンションのデータセットを作成しました。

     必要に応じて、追加のデータセットを含めることもできます。

   * ディメンションデータセットをイベントデータセットにマッピングします。

      1. ディメンション データセットの設定を開きます。

         設定ページの見出しは「[!UICONTROL Lookup Dataset]」です。これは、ディメンションデータセットを指標固有のデータセットのいずれかに結合できることを示します。

      1. [!UICONTROL Adobe Advertising Dimensions] セクションで、ディメンションデータセットをイベントデータセットにマッピングします。

         1. [!UICONTROL Key] フィールドで、ディメンション データセットのキーとして使用するフィールドを選択します：`Adobe Advertising ID` （スキーマの`trackingCode` フィールドと同じです）。

         1. [!UICONTROL Matching key] フィールドで、イベントデータセットの一致キーとして使用するフィールドを選択します。 使用可能なフィールド名には、データセット名が括弧で囲まれています。 例えば、ディメンションデータセットをイベントデータセットにマッピングする場合は、`Tracking Code (Event datasets)`を選択します。

         後で、データビュー（#cja-data-views）を設定する際に、イベントデータセットをサマリーデータセットにマッピングします。

1. 数時間後、データがCustomer Journey Analyticsで使用可能であることを確認します。

   1. Customer Journey Analyticsで、**[!UICONTROL Connections]**&#x200B;に移動し、接続を選択します。

   1. 表示されるデータセットのリストで、「[!UICONTROL Number of Records]」レポートにデータが追加されたことを確認します。

## Customer Journey Analyticsでのデータビューの設定 {#cja-data-views}

Customer Journey Analyticsで、1つ以上のデータビューを作成して、レポートの指標とディメンションを定義します。 web アナリストはこれらのタスクを実行できます。

1. Customer Journey Analyticsで、[&#x200B; データビューを作成](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-dataviews/create-dataview)。

1. 次の情報を含めるようにビューを設定します。

   * Adobe Analytics アカウントをお持ちの場合は、「[!UICONTROL Time Zone]」タブの「[!DNL Analytics]」セクションにある「[!UICONTROL Calendar]」アカウントの「[!UICONTROL Configure]」を使用してください。

   * 「[!UICONTROL Components]」タブ：

      * ディメンション、イベント、概要データセットを追加します。

      * イベント（指標）データセットとディメンション（分類/メタデータ）データセットから指標を選択して、データビューに含めます。

        これらの2つのデータセットは、最後の[手順](#dataset-connection)で作成した接続に既に結合されています。

      * イベントデータセットを、まだ何にも結合されていないサマリーデータセットに結合します。

         * Customer Journey Analyticsで使用可能にする概要データを含むディメンションごとに、[派生フィールドを作成](https://experienceleague.adobe.com/ja/docs/analytics-platform/using/cja-dataviews/derived-fields)。

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

               * Workspaceで派生フィールド名を非表示にする&#x200B;**[!UICONTROL Hide in reporting]**&#x200B;にオプションを選択します。

## Customer Journey Analytics Workspaceでのレポートとビジュアライゼーションの設定 {#cja-reports}

Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定するには、次の手順に従います。 web アナリストはこれらのタスクを実行できます。

1. Workspaceで[&#x200B; プロジェクト &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects)を作成し、データビュー内で設定されたディメンションと指標に基づいてレポートとビジュアライゼーションを作成します。

1. （データが[!DNL Google Ads]または[!DNL Microsoft Advertising]の場合）広告ネットワーク固有の指標のフィールドを使用して、発行者が追跡したコンバージョンのレポートを作成します。このフィールドは`googleConversions`および`microsoftConversions`としてグループ化されます。

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>* [前提条件](prerequisites.md)
>* [様が使用している [!DNL Customer Journey Analytics]](ids.md)Adobe Advertising ID
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集します](/help/integrations/analytics/rvars-to-evars.md)。
>* [Customer Journey Analytics ガイド &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics [Adobe Analytics ユーザー向けユーザーガイド &#x200B;](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
