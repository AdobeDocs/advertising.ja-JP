---
title: データ収集、データ転送およびレポートの設定
description: データ収集、データ転送、レポートの設定方法について説明します。
feature: Integration with Adobe Customer Journey Analytics
source-git-commit: 2d6cba8d5a3d966b272c5048404ac8fdf0185b74
workflow-type: tm+mt
source-wordcount: '1236'
ht-degree: 0%

---

# データ収集、データ転送およびレポートの設定

*Beta機能*

Customer Journey Analyticsで Advertising Cloud データを表示するには、次のタスクが必要です。

1. （組織の Web アナリスト。オプション） [AMO ID および EF ID の履歴データを収集 ](/help/integrations/analytics/rvars-to-evars.md){target="_blank"}。

   この手順は、[!DNL Analytics for Advertising] を使用する広告主にのみ適用されます。

1. （Experience Platformの組織サイト管理者） [Adobe Experience Platformでデータ収集を設定して、コンバージョントラッキングタグを実装する ](#data-collection)。

1. （組織のCustomer Journey Analytics サイト管理者） [Customer Journey AnalyticsでExperience Platform データセットへの接続を作成します ](#dataset-connection)。

1. （組織の Web アナリスト） [Customer Journey Analyticsでのデータビューの設定 ](#cja-data-views)。

1. （組織の Web アナリスト） [Customer Journey Analytics Workspaceでレポートとビジュアライゼーションを設定します ](#cja-reports)。

以降の節では、統合に必要なタスクと設定を含む詳細な手順を説明しますが、ワークフロー内で使用できるすべての機能については説明しません。 詳しくは、リンクされたリソースを参照してください。

## Adobe Experience Platformと web サイトでのデータ収集の設定 {#data-collection}

Experience Platformでデータ収集を設定し、コンバージョントラッキングタグを実装するには、次のタスクが必要です。 組織のExperience Platformのサイト管理者はこれらのタスクを実行できますが、組織の IT 部門はトラッキングタグのデプロイをサポートする必要がある場合があります。

1. Adobe AdvertisingからExperience Platform Edge Networkにデータセットとしてデータを収集して送信します。

   1. Experience Platformで、エクスペリエンスデータモデル（XDM）を使用して収集するデータの [ 手動スキーマを定義する ](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/ui/resources/schemas) を行います。

      * [!UICONTROL Schema Details] で、サイトイベントをキャプチャするスキーマの基本クラスとして **[!UICONTROL Experience Event]** を選択します。 スキーマに名前を付け、「**[!UICONTROL Finish]**」をクリックします。

      * 左側のパネルでフィールドグループ `Adobe Advertising Cloud ExperienceEvent Full Extension` を追加して、Adobe Advertising固有のフィールドを追加します。<!-- Add link once published --> 少なくとも、conversionDetails オブジェクトを `trackingCode` プロパティおよび `trackingIdentities` プロパティで含めます。このプロパティには、[AMO ID および EF ID](ids.html) が含まれます。 その他のフィールドはオプションです。

      * （オプション）必要に応じてフィールドグループを追加し、追加のデータフィールドをAdobe Advertising データに接続します。

      **メモ：** 複数のスキーマを作成できますが、次の手順で作成する、データセットごとおよびデータストリームごとに 1 つのスキーマのみを使用できます。

   1. スキーマに基づいて [ データセットを作成 ](https://experienceleague.adobe.com/en/docs/experience-platform/catalog/datasets/create) し、イベントデータの収集を保存および管理します。

      * **[!UICONTROL Create dataset from schema]** すオプションを選択し、スキーマを選択します。

        Adobe Advertisingは、イベントデータセットに基づいて、関連する概要指標データ（コンバージョン値など）およびルックアップデータ（ディメンション/分類メタデータ（Adobe Advertising キャンペーン名など））に対して追加のデータセットを作成します。 データセットのデータは、Experience Platformに毎日入力されます。

   1. スキーマの [ データストリームを作成 ](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure) します。

      * [!UICONTROL Mapping schema] 設定で、スキーマを選択します。

      * データストリームに `Adobe Advertising` および `Adobe Experience Platform` サービスを追加して有効にします。

        これらのサービスにより、Edge Networkはデータセットを保存し、Adobe Advertisingにルーティングできます。

      * [!UICONTROL Event dataset] 設定には、データセットを選択します。

        各データストリームでは、1 つのデータセットにのみデータを挿入できます。

1. 組織の web サイトデータをExperience Platform データストリームに送信します。

   1. Experience Platform[tags](https://experienceleague.adobe.com/en/docs/experience-platform/tags/home) （旧称：[!DNL Launch]）を使用して、JavaScript タグを生成し、組織の web サイトデータをデータストリームに送信します。

      * タグプロパティ（タグ設定のコンテナ）を作成します。

      * プロパティについては、拡張機能カタログから [ 拡張機能「Adobe Experience Platform Web SDK」をインストール ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration) ます。

        この拡張機能は、web プロパティからExperience Platform Edge Networkを介してExperience Cloudにデータを送信します。

        Adobe Advertising拡張機能を使用しないでください。

      * カスタム web SDK ビルドを作成します。

         * 「[!UICONTROL Custom build components]」セクションで、**Advertising** コンポーネントを有効にします。

           このコンポーネントには、タグ内のAdobe Advertisingに必要なすべてのJavaScript コードが含まれます。 また、タグルール（オプション）の「Advertising」設定を追加して、広告データがアトリビューション測定にどのように使用されるかを定義します。

           オプションで、必要に応じて追加のコンポーネントを有効にすることができます。

         * [!UICONTROL SDK Instances] のセクションで以下を実行します。

            * [!UICONTROL Datastreams] 設定で、web 環境（実稼働、ステージング、開発）ごとに使用するデータストリームを選択します。

            * （Adobe Advertising DSPを使用している組織のみ） [!UICONTROL Adobe Advertising] の設定を使用します。

               * **[!UICONTROL Adobe Advertising DSP]** 設定を有効にして、ビュースルートラッキングを有効にします。

               * ビュースルートラッキングを有効にする広告主を指定します。

               * （オプション） ID を収集する組織の ID5 パートナー ID を入力します。

               * （オプション）組織の [!DNL LiveRamp RampID] JavaScript コード（ats.js）のパスを入力して ID を収集します。

            * ビルドを保存します。

      * （オプション） [ ルールを作成 ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)Web SDKからEdge Networkにデータを送信するタイミングを決定する必要があります。

         * [!UICONTROL Advertising] 設定では、広告データがアトリビューション測定にどのように使用されるかを定義します。 この設定は、ルールに複数のアクションのシーケンスが含まれている場合に役立ち、カスタムビルドコンポーネントの「[!UICONTROL Advertising]」コンポーネントを選択した場合にのみ使用できます。 次のようなオプションがあります。

           *自動：* キャッシュ内のデータに基づいて、現在の `sendEvent` アクションの広告アトリビューションの測定に広告データを使用できるようにします。 この場合、広告公開イベントはチャンスを得たときに発生し、現在のイベントでは使用できない可能性があります。 例えば、購入チェックアウトイベントを実行し、キャッシュに広告露出データが利用できない場合、チェックアウトイベントは広告露出に関連付けられません。

           *待機：* 広告データがサーバーから正常に取得されて解決されるまで、呼び出しの実行を遅延させます。これにより、正確なアトリビューション測定が保証されます。 例えば、購入チェックアウトイベントを実行する前に、広告露出イベントが解決するのを待つ必要がある場合があります。 **注意：** ブラウザーと ID タイプによっては、ID の解決に数秒かかる場合があります。 現在の `sendEvent` アクションで数秒間の遅延に対応できる場合は、このオプションを使用します。

           *無効：* （デフォルト）トリガーするリクエストから広告データを除外し、アトリビューションまたは関連するトラッキングで使用できないようにします。

           *データ要素を指定：* データ要素を使用して、ページ読み込み中に広告データを含めたり、除外したりします。 データ要素の解決された値には、`automatic`、`wait`、`disabled` を含めることができます。 次の手順を参照してください。

        ルールを使用して `sendEvent` アクションを設定しない場合、広告データは別の広告宣伝エンリッチメントイベントとして送信されます。

      * 必要に応じて [ データ要素 ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/data-elements) を作成して、web サイト上の変数を、以前作成した XDM スキーマの構造にマッピングします。

   1. タグの開発を繰り返し実行できるテスト環境に [ タグを公開 ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) します。

   1. データセットの配信を検証してから [ タグを実稼動環境に公開 ](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow) します。

      組織の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールまたは通知する必要がある場合があります。

## Customer Journey AnalyticsでExperience Platform データセットへの接続を作成する {#dataset-connection}

次の手順に従って、Adobe Advertising データをExperience Platform データセットからCustomer Journey Analyticsに取り込みます。 Customer Journey Analyticsの組織のサイト管理者は、これらのタスクを実行できます。

*準備中*

## Customer Journey Analyticsでのデータビューの設定 {#cja-data-views}

Customer Journey Analyticsで、1 つ以上のデータビューを作成して、レポート用の指標およびディメンションを定義します。 Web アナリストは、これらのタスクを実行できます。

*準備中*

## Customer Journey Analytics Workspaceでのレポートとビジュアライゼーションの設定 {#cja-reports}

Customer Journey Analytics Workspaceでは、次の手順に従ってレポートとビジュアライゼーションを設定します。 Web アナリストは、これらのタスクを実行できます。

1. Workspaceで [ プロジェクトを作成 ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-workspace/build-workspace-project/create-projects) し、データビュー内で設定されたディメンションと指標に基づいてレポートとビジュアライゼーションを作成します。

1. （[!DNL Google Ads] または [!DNL Microsoft Advertising] のデータがある場合）広告ネットワーク固有の指標のフィールド（`googleConversions` および `microsoftConversions` としてグループ化）を使用して、発行者が追跡したコンバージョンのレポートを作成します。

>[!MORELIKETHIS]
>
>* [ 概要 ](overview.md)
>* [ 前提条件 ](prerequisites.md)
>* [ 使用するAdobe Advertising ID [!DNL Customer Journey Analytics]](ids.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標およびディメンション ](advertising-data-in-cja.md)
>* [Adobe Customer Journey Analyticsで使用する AMO ID および EF ID の履歴データを収集します ](/help/integrations/analytics/rvars-to-evars.md)。
>* [Customer Journey Analytics ガイド ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-landing)
>* Customer Journey Analytics[Adobe Analytics ユーザー向けユーザーガイド ](https://experienceleague.adobe.com/en/docs/analytics-platform/using/compare-aa-cja/aa-to-cja-user)
