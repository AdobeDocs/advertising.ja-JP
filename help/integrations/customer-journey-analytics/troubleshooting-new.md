---
title: Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング
description: Customer Journey AnalyticsのAdobe Advertising データに関する問題のトラブルシューティングと解決方法について説明します。
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
source-git-commit: bf9cdd654131b619e3f650478f2f89afaaa625fd
workflow-type: tm+mt
source-wordcount: 2980
ht-degree: 0%

---

# Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング

次に潜在的な問題、それらの考えられる原因、および解決策を示します。

## すべての潜在的な症状のリスト

| 症状 | 詳細 |
| ------- | ---------------- |
| ブラウザーの「ネットワーク」タブにalloy （）呼び出しはありません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を参照してください |
| コンソールエラー：合金が定義されていません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」を参照してください> 「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を初期化しません |
| edge.adobedc.netに対するインタラクションまたは収集リクエストはありません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」を参照してください> 「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を初期化しません |
| リクエストはエッジに到達するが、400または500 エラーを返す | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| Adobe AnalyticsまたはAdobe Advertising レポートにデータが表示されない | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| ネットワーク応答のエラー：「データストリームが見つかりません」 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| ページ間で訪問者IDが変更される | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[IDとECIDの問題](#identity-and-ecid-issues)」の節を参照してください |
| Advertisingのオーディエンスセグメントが一致しない | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[IDとECIDの問題](#identity-and-ecid-issues)」の節を参照してください |
| デバッガーは、ルール条件が満たされていないことを示します | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」の「[&#x200B; ルールまたはイベントが実行されていません](#rules-or-events-aren't-firing)」の節を参照してください |
| [!UICONTROL Send Event] アクションは実行されません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」の「[&#x200B; ルールまたはイベントが実行されていません](#rules-or-events-aren't-firing)」の節を参照してください |
| [!DNL Tags]で行われた変更は、ライブサイトに反映されません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; ライブラリのビルドと公開の問題](#library-build-and-publishing-issues)」の節を参照してください |
| 拡張機能の更新が適用されましたが、古い動作は保持されます | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; ライブラリのビルドと公開の問題](#library-build-and-publishing-issues)」の節を参照してください |
| `alloy()`送信イベント呼び出しは成功しましたが（応答は200件）、Adobe Advertising コンバージョンデータがレポートに見つかりません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[Advertising フィールドのスキーマ検証の問題](#schema-validation-for-advertising-fields)」の節を参照してください |
| デバッガーのXDM ペイロードに`_experience.adcloud` オブジェクトが表示されません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[Advertising フィールドのスキーマ検証の問題](#schema-validation-for-advertising-fields)」の節を参照してください |
| web ページのビュースルーコンバージョンまたはクリックスルーコンバージョンは記録されません | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |
| クリックスルー用のExperience Data Model （XDM） ペイロードに`_experience.adcloud`がありません | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |
| コンバージョンはデバッガーツールで確認されますが、Adobe Advertising レポートには表示されません | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |

## インストールとセットアップの問題 {#issues-installation-setup}

### WebSDK拡張機能がを初期化しません{#websdk-extension-doesn&#39;t-initialize}

症状：

* ブラウザーの「ネットワーク」タブにalloy （）呼び出しはありません
* コンソールエラー：合金が定義されていません
* edge.adobedc.netに対するインタラクションまたは収集リクエストはありません

| 原因 | 修正 |
| ----- | --- |
| ライブラリが公開されていないか、ドラフト状態です | [公開フロー](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/publish/publishing-flow)に移動し、WebSDK拡張機能を含むライブラリが承認済み/公開済み状態であることを確認します。 |
| 埋め込みコード環境が見つからないか間違っています | Web ページの[!DNL Tags]埋め込みコードが正しい環境（開発/ステージ/実稼動）を参照していることを確認します。 `//assets.adobedtm.com/...` スクリプトタグの`<head>` タグで環境を探します。 |
| 非同期と同期読み込みの競合 | Web ページごとに[!DNL Tags]埋め込みコードが1つだけ存在することを確認してください。 重複した埋め込みコードが競合状態の原因となります。 |
| コンテンツセキュリティポリシー（CSP）によるブロック | CSP `connect-src`および`script-src` ディレクティブに`edge.adobedc.net` `and assets.adobedtm.com`を追加します。 |

### データストリームが設定されていないか、設定が正しくありません {#datastream-not-configured-or-misconfigured}

症状：

* リクエストはエッジに到達するが、400または500 エラーを返す
* Adobe AnalyticsまたはAdobe Advertising レポートにデータが表示されません<!-- It's not useful to organize this info by cause, not symptom -->
* ネットワーク応答のエラー：「データストリームが見つかりません」

| 原因 | 修正 |
| ----- | --- |
| タグプロパティのデータストリーム IDが見つからないか、正しくありません。 | <ol><li>[!DNL Tags]で、タグプロパティの[&#x200B; データストリーム設定設定](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)を開きます。</li><li>[!UICONTROL Datastream] フィールドが、各環境（開発、ステージング、実稼動）の正しいデータストリーム、および正しいスキーマとデータセットを指していることを確認します。<br><br>3つの環境すべてで1つのデータストリームを明示的に共有しない限り、各環境には独自のデータストリームが必要です。</li></ol> |
| タグプロパティに対してデータストリームサービスが有効になっていません。 | [&#x200B; データストリーム設定](https://experienceleague.adobe.com/ja/docs/experience-platform/datastreams/configure)を開き、次のサービスが有効になっていることを確認します。<ul><li>Adobe Advertising（コンバージョン/オーディエンス同期用）</li><li>Adobe Experience Platform（プロファイル取得用）</li></ul> |
| サンドボックスの不一致 | データストリームが、スキーマおよびデータセットと同じAdobe Experience Platform サンドボックスに属していることを確認します。 よくある間違いは、実稼動サンドボックスにデータストリームを作成する際に、開発サンドボックスにスキーマを指定することです。 |

### IDとECIDの問題 {#identity-and-ecid-issues}

症状：

* ページ間で訪問者IDが変更される
* Advertisingのオーディエンスセグメントが一致しない

| 原因 | 修正 |
| ----- | --- |
| サードパーティ Cookieはブロックされています | データストリームのエッジ設定でファーストパーティドメインを設定することで、ファーストパーティ CNAME データ収集に移行します。 |
| レガシー`s_ecid` Cookieが存在する間、`idMigrationEnabled`は`false`に設定されています | WebSDK ベース設定で`idMigrationEnabled: true`を設定して、既存のECIDを`s_ecid`または`AMCV_` Cookieから移行します。 |

### ルールまたはイベントが実行されない{#rules-or-events-aren&#39;t-firing}

症状：

* デバッガーは、ルール条件が満たされていないことを示します
* [!UICONTROL Send Event] アクションは実行されません

次の点を確認します。

* ルールが保存され、アクティブなライブラリビルドに含まれます。
* イベントタイプは、実際のページ動作（[!UICONTROL Library Loaded]対[!UICONTROL DOM Ready]対[!UICONTROL Window Loaded]など）と一致します。
* ルールの条件はそれほど制限されていません。 問題を特定するために、条件を一時的に削除してテストします。
* ルールの順序は正しいです。 複数のルールが同じイベントを共有する場合は、ルールの順序を確認します。
* ページの以前のJavaScript エラーで実行が停止することはありません。 ブラウザーコンソールで捕捉されない例外がないか確認します。

### ライブラリのビルドと公開の問題 {#library-build-and-publishing-issues}

症状：

* [!DNL Tags]で行われた変更は、ライブサイトに反映されません
* 拡張機能の更新が適用されましたが、古い動作は保持されます

| 原因 | 修正 |
| ----- | --- |
| 変更がライブラリに追加されませんでした | [!UICONTROL Publishing Flow]で、変更内容が開発環境のライブラリに追加されたことを確認します。 [!UICONTROL Libraries]に移動し、作業ライブラリを開き、**変更されたすべてのリソースを追加**&#x200B;を選択してから、**保存とビルド**&#x200B;を選択します。 |
| ブラウザーが古いライブラリをキャッシュしています | ハードリフレッシュ（Ctrl+Shift+RまたはCmd+Shift+R）を実行するか、シークレットウィンドウまたはプライベートウィンドウでページを開きます。 問題が解決しない場合は、ブラウザーのキャッシュを完全にクリアします。 |
| 埋め込みコードは環境が正しくありません | 実稼動動作をテストする場合は、ページの埋め込みコードが実稼動用埋め込みコードであることを確認します。 |
| ライブラリのビルドがサイレントに失敗しました | [!UICONTROL Publishing Flow]に移動し、ライブラリに[!UICONTROL Build Failed]状態が表示されているかどうかを確認します。 ライブラリを開き、ビルドログを確認します。一般的な原因は、無効なルール設定または拡張機能のバージョンの競合です。 |

### Advertising フィールドのスキーマ検証の問題 {#schema-validation-for-advertising-fields}

症状：

* `alloy()`送信イベント呼び出しは成功しましたが（応答は200件）、Adobe Advertising コンバージョンデータがレポートに見つかりません
* デバッガーのXDM ペイロードに`_experience.adcloud` オブジェクトが表示されません

#### 手順1: [!UICONTROL Advertising] フィールドグループがスキーマに追加されていることを確認する

1. Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas]に移動します。
1. データストリームで使用するスキーマを開きます。
1. [!UICONTROL Field Groups] パネルで、**Adobe Advertising Cloud ExperienceEvent Full Extension**&#x200B;がリストされていることを確認します。
1. 見つからない場合は、**追加**&#x200B;を選択し、**Adobe Advertising Cloud**&#x200B;を検索し、**Adobe Advertising Cloud ExperienceEvent Full Extension**&#x200B;を選択してから、**保存**&#x200B;を選択します。

>[!NOTE]
>スキーマの変更だけでは[!DNL Tags] ライブラリを再公開する必要はありませんが、新しいフィールドが追加された場合は、[!DNL Tags]でXDM データ要素を再マッピングする必要があります。

#### 手順2：必須のAdobe Advertising フィールドが`_experience.adcloud.conversionDetails`の下のスキーマに存在することを確認します

| フィールドパス | タイプ | 説明 |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | 文字列 | コンバージョンを元の広告クリックにマッピングします。 ランディングページ URLの`s_kwcid` クエリパラメーターから入力されました。 |
| `_experience.adcloud.conversionDetails.trackingIdentity` | 文字列 | 追跡されたビュースルーまたはクリックスルーのコンバージョンイベントの一意のIDおよびその他の詳細を保存します。 ランディングページ URLの`ef_id` クエリパラメーターから入力されました。 |

いずれかのフィールドが見つからない場合は、**Adobe Advertising Cloud ExperienceEvent Full Extension** フィールドグループがスキーマに保存されていることを確認してから、スキーマエディターを更新します。

#### 手順3：ランディングページ URLにクエリパラメーターが含まれていることを確認する

広告クリックスルーの場合、ランディングページのURLには、次のような両方のクエリパラメーターを含める必要があります。

`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`

| パラメーターがありません | 考えられる原因 |
| ----- | --- |
| `s_kwcid` | Adobe Advertising検索またはDSP キャンペーン設定では、自動タグ付けは有効になっていません。 |
| `ef_id` | ランディングページのURLがAdobe Advertisingで追跡されたリダイレクトを使用していないか、キャンペーン設定でEF IDの追加が有効になっていません。 |

#### 手順4：送信XDM ペイロードの検証

AEP Debuggerまたはブラウザー[!UICONTROL Network] タブを開き、`edge.adobedc.net`のフィルターを実行し、インタラクションリクエスト本文を調べます。 有効なクリックスルーペイロードは、次のようになります。

```json
{
  "events": [{
    "xdm": {
      "eventType": "advertising.clicks",
      "_experience": {
        "adcloud": {
          "conversionDetails": {
            "trackingCode": "AL!12345!3!abc123",
            "trackingIdentity": "abc123xyz:G:s"
          }
        }
      }
    }
  }]
}
```

`trackingCode`または`trackingIdentity`が空または見つからない場合：

* ルールが実行されたときに、クエリ パラメーターがページに存在しませんでした。 URLとルールのイベントタイミングを確認します。
* フィールドグループがスキーマにありません。 上記のスキーマ手順を再確認します。

## [!UICONTROL Advertising]拡張機能の設定に関する問題 {#advertising-extension-setup-issues}

症状：

* web ページのビュースルーコンバージョンまたはクリックスルーコンバージョンは記録されません。

  コンバージョンが記録されているかどうかを確認するには：

  1. URLに`ef_id=test&s_kwcid=test`が追加されたweb ページを開きます。
  1. ブラウザーのコード検査ツール（[!DNL Inspect]と呼ばれることが多い）を開き、「[!DNL Network]」タブを開き、Adobe Experience Platformのevent_type=&quot;advertising.enrichment_ct&quot;のインタラクティブ呼び出しを探します。
  1. データ収集インターフェイスで、[収集するweb サイト データのスキーマ定義](https://experienceleague.adobe.com/ja/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas)を開き、`xdm->_experience->adcloud->conversionDetails->trackingCode`と`trackingIdentities`に`ef_id`と`s_kwcid`が含まれていることを確認します。

* クリックスルー用のExperience Data Model （XDM） ペイロードに`_experience.adcloud`がありません。

* コンバージョンはデバッガーツールで確認されますが、Adobe Advertising レポートには表示されません

| 原因 | 修正 |
| ----- | --- |
| データストリームに`Adobe Advertising` サービスが有効になっていません | <ol><li>[!DNL Tags]で、タグプロパティの[&#x200B; データストリーム設定設定](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)を開きます。</li><li>次のサービスを有効にし、設定を保存します。<ul><li>Adobe Advertising（コンバージョン/オーディエンス同期用）</li><li>Adobe Experience Platform（プロファイル取得用）</li></ul></ol> |
| `Adobe Advertising` コンポーネントは[!UICONTROL WebSDK]拡張機能に対して有効になっていません | WebSDK拡張機能の`Adobe Advertising` コンポーネントはデフォルトで無効になっており、XDM スキーマまたはルールの設定方法に関係なく、Adobe Advertising クリックスルーまたはビュースルーのトラッキングが機能する前に、明示的に有効にする必要があります。<ol><li>[!DNL Tags]で、Adobe Experience Platform Web SDKの設定[&#128279;](https://experienceleague.adobe.com/ja/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components)で、プロパティの ビルドオプションを開きます。</li><li>**Advertising** コンポーネントを有効にし、設定を保存します。</li><li>ライブラリを再構築して再公開します。</li></ol> |
| クリックスルーコンバージョンのみが記録されます。ビュースルーコンバージョンは表示されません | これは期待されるデフォルトの動作です。 `Adobe Advertising` コンポーネントが有効になると、`s_kwcid`および`ef_id`のURL クエリパラメーターを使用して、クリックスルー追跡が自動的にアクティブになります。 ビュースルートラッキングはデフォルトで無効になっており、追加の設定が必要です。次の行を参照してください。 |
| ビュースルー追跡が有効になっていないか、設定されていません | <ol><li>Adobe Experience Platformの[!UICONTROL Data Collection] > [!UICONTROL Datastreams]に移動し、[!DNL Tags] プロパティで使用されているデータストリームを開きます。</li><li>**サービスを追加**&#x200B;を選択し、**Adobe Advertising**&#x200B;および&#x200B;**Adobe Experience Platform**&#x200B;を選択してから、**保存**&#x200B;を選択します。</li><li>[!DNL Tags]で、[!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure]に移動します。</li><li>「[!UICONTROL Advertiser]」セクションで、ドロップダウンから広告主を選択して有効にします。 複数の広告主を設定するには、**広告主を追加**&#x200B;を選択します。</li><li>AEP Debuggerで、インタラクトコールに`xdm.query` フィールドの下に`stitchId`が含まれていることを確認します。 ブラウザー[!UICONTROL Network] タブから、タイプ `advertising.enrichment`のイベントが発生し、`xdm.query`の下に`stitchId`が含まれていることを確認することもできます。</li></ol> ビュースルーコンバージョンは、訪問数に関係なく30分ごとに実行されます。インタラクション呼び出しが表示されない場合は、ブラウザーのキャッシュをクリアして、もう一度試してください。 |
| 広告主は、ドロップダウンから選択するのではなく、手動で入力されました | 広告主を手動で入力する代わりに、[!UICONTROL Advertiser] ドロップダウンから広告主を再選択します。 |
| ビュースルーインタラクティブコールでは、広告主IDは送信されません | WebSDK拡張機能の設定の[!UICONTROL Advertiser] セクションで広告主が設定され、有効になっていることを確認してから、ライブラリを再構築して再公開します。 |

[!UICONTROL Advertising]拡張機能の設定に関するサポートチケットを開く前に、次の点を確認してください。

* **Adobe Advertising**&#x200B;および&#x200B;**Adobe Experience Platform** サービスがデータストリームに追加されます。
* **Adobe Advertising** コンポーネントは、WebSDK拡張機能コンフィギュレーションで有効になっています。
* コンポーネントを有効にした後、ライブラリが再構築され、再公開されました。
* クリックスルー追跡の場合、ランディングページ URLには、広告クリック時に`s_kwcid`と`ef_id`が含まれます。
* ビュースルートラッキングの場合、広告主はAdobe Advertising DSPで正しい広告主IDで設定されます。
* WebSDK拡張機能は、バージョン 2.36.0以降です。

## 検証ツールとデバッグツール

### Adobe Experience Platform Debugger

[!DNL Chrome]の[!DNL Adobe Experience Platform Debugger]拡張機能をインストールします。 次のようなメリットがあります。

* すべてのWebSDK `alloy()`呼び出しのリアルタイム ビュー
* データストリーム IDと環境の検証
* XDM ペイロード検査
* Edge Networkのリクエストとレスポンスの詳細

デバッガーのキーチェック：

| Tab | 確認すべきこと |
| ----- | --- |
| [!UICONTROL Summary] | WebSDKが検出され、インストールされているバージョンが表示されることを確認します。 |
| [!UICONTROL AEP Web SDK] | 発生した各イベント、完全なXDM ペイロード、およびエッジ応答を表示します。 |
| [!UICONTROL Adobe Advertising] | AMO ID キャプチャとXDM インタラクション呼び出しを`advertising.enrichment` イベントタイプで確認します。 |

### 「ブラウザーネットワーク」タブ

`edge.adobedc.net`でフィルタリングして、生のエッジリクエストを検査します。

* リクエスト URL: `https://[org-id].data.adobedc.net/ee/v2/interact`
* メソッド：`POST`
* ステータス：`200` （正常）、`400` （不正なペイロード）、または`500` （サーバーまたはデータストリームエラー）

次のリクエストペイロードを確認します。

* 正しい`dataStreamId`
* 予期されたフィールドを持つ`xdm` オブジェクトの存在
* ECIDが入力された`identityMap`

### コンソールの検証

インストールされているWebSDKのバージョンを確認します。

```js
window.alloy.version
```

テストイベントを手動でトリガーする：

```js
alloy("sendEvent", {
  xdm: {
    eventType: "web.webpagedetails.pageViews",
    web: {
      webPageDetails: { name: "Test Page", URL: window.location.href }
    }
  }
}).then(result => console.log("Edge response:", result))
  .catch(err => console.error("Send event error:", err));
```

## クイックリファレンス

サポートチケットを開封する前に、次の点を確認してください。

* WebSDK拡張機能は最新バージョンです。
* ライブラリが公開され、埋め込みコードが環境に適しています。
* データストリーム IDは、開発、ステージング、実稼動用に正しく設定されます。
* 必要なすべてのデータストリームサービスが有効になります。
* [!UICONTROL Advertising] コンポーネントはWebSDK拡張機能の設定で有効になっており、DSP広告主IDが設定されています。
* XDM スキーマには、[!UICONTROL Advertising] フィールドグループが含まれています。
* [!UICONTROL Send Event] ルールにはID マップが含まれており、正しいイベントに対して実行されます。
* エッジリクエストをブロックしているCSPまたはブラウザープライバシー設定はありません。
* AEP Debuggerは、イベントがエッジに到達していることを確認します。
* ブラウザーコンソールで実行を停止しているJavaScript エラーはありません。
* **Adobe Advertising Cloud ExperienceEvent Full Extension** フィールドグループがスキーマに追加されます。
* `_experience.adcloud.conversionDetails.trackingCode`はスキーマに存在します。
* `_experience.adcloud.conversionDetails.trackingIdentity`はスキーマに存在します。
* ランディングページ URLには、クリックスルー時の`s_kwcid`と`ef_id`の両方が含まれています。
* AEP Debuggerは、`conversionDetails`がアウトバウンドペイロードに入力されていることを確認します。

## エスカレーションするタイミング

次の場合は、Adobe アカウントチームまたはエンジニアリングチームにエスカレーションします。

* Edge リクエストは、データストリームの検証後に永続的な`500` エラーを返します。
* [!UICONTROL Advertising]個のコンバージョンがデバッガーで確認されますが、24 ～ 48時間後にレポートに表示されません。
* WebSDK バージョンのアップデートでは、以前のバージョンには存在しなかった回帰が導入されます。 サポートチケットに特定のバージョン番号を含めます。

## レポートの問題

### 概要レポート

+++ Customer Journey Analytics for Advertising DSPまたはAdvertising Search, Social, &amp; Commerceでは、概要レポートデータは利用できません。

次の点を確認します。

* Customer Journey Analytics Workspaceが正しいデータビューを参照しています。

* Adobe AdvertisingからCustomer Journey Analyticsへのフィードが有効になっています。 Adobeのアカウントチームにお問い合わせください。

* Adobe Advertising ディメンション/分類/参照データセットとサマリーデータセットは、Customer Journey Analytics接続に含まれます。

* Adobe Advertisingのディメンションと概要指標は、Customer Journey Analytics データビューに含まれます。

上記のすべての設定を確認しても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。

+++

+++ 概要レポートデータは、Customer Journey Analytics for Advertiser 1では利用できますが、Advertiser 2では利用できません。

次の点を確認します。

* Adobe AdvertisingからCustomer Journey Analyticsへのフィードは、Advertiser 2で有効になっています。 Adobeのアカウントチームにお問い合わせください。

* 設定「[!UICONTROL Backfill all existing data]」は、Customer Journey Analytics接続の3つのデータセット（ディメンション/分類/ルックアップ、サマリー、イベント指標）に対して有効になっています。

上記の条件をすべて確認しても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。

+++

+++ （Search, Social, &amp; Commerce ユーザー）概要レポート データは、Customer Journey Analyticsで1つの[!DNL Google Ads]、[!DNL Meta Ads]、または[!DNL Microsoft Advertising] アカウントで利用できますが、別のアカウントでは利用できません。

Adobe AdvertisingからCustomer Journey Analyticsへのフィードが、特定の広告ネットワークアカウントに対して有効になっていることを確認します。 Adobeのアカウントチームにお問い合わせください。

フィードがアカウントに対して有効になっていても概要データが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。

+++

+++ Customer Journey Analytics Workspaceの概要レポートデータは、Advertising DSPまたはAdvertising Search, Social, &amp; Commerceのデータと異なり、一部のキャンペーンおよびキャンペーンエンティティの概要データが見つかりません。

次の点を確認します。

* [!DNL Workspace]とAdobe Advertising レポートの両方で同じ日付範囲を使用しています。

* [!DNL Workspace]とAdobe Advertising レポートに適用されているフィルターとセグメントは、データの違いを引き起こしません。

* Customer Journey Analytics データビューの[!UICONTROL Time Zone]は、Advertising DSP アカウントの[[!UICONTROL Default Timezone]と一致します](/help/dsp/admin/user-own-profile-edit.md)。

* 設定「[!UICONTROL Backfill all existing data]」は、Customer Journey Analytics接続の3つのデータセット（ディメンション/分類/ルックアップ、サマリー、イベント指標）に対して有効になっています。

データの相違が確認できる場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。 食い違いの証拠を示すには、スクリーンショットとスプレッドシートを含めます。 Adobe アカウントチームは、必要に応じてデータフィードを過去にさかのぼって修正し、差異を解決できます。

+++

### イベントレベルのレポート

+++ コンバージョンデータ （`Page Views`など）は、CJA Customer Journey Analytics Workspaceのレポートディメンション （`Campaign`など）では使用できません。

以下を確認します。最初に、検証障壁が最も少ない項目を確認します。

* 正しいデータビューを使用していること。

* 該当するコンバージョン指標は、web/オンラインイベントで、Adobe Advertisingはディメンションに関連付けることができます。

* Adobe Advertisingでは、該当するサイトのクリックスルーとビュースルーを追跡しています。<!-- Link to validation instructions in the user guide -->

* 分類データセットのCustomer Journey Analytics接続で、[!DNL Key]および[!DNL Matching Key]設定の値が正しいです：[!DNL Key]: `Tracking Code` （_customername.adLens2.trackingCode）、[!DNL Matching Key]: `Tracking Code` （event._experience.adcloud.conversionDetails.trackingCode）

* [!DNL Adobe Advertising] サービスがAdobe Experience Platform データストリームに追加され、データストリーム用にマッピングされたスキーマが`XDM ExperienceEvent Schema`になり、フィールドグループ `Adobe Advertising Cloud ExperienceEvent Full Extension`が`XDM ExperienceEvent` スキーマに追加されます。

* Adobe Advertisingの設定は、WebSDK拡張機能で正しく設定され、公開されます。

上記の設定をすべて確認しても、コンバージョンデータが表示されない場合は、[https://experienceleague.adobe.com/home?lang=ja#support](https://experienceleague.adobe.com/home?lang=ja&support-tab=home#support)で組織のサポートチケットを開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。

+++

<!--

+++ Question

Answer

+++

+++ Question

Answer

+++

+++ Question

Answer

+++

-->

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>*  [!DNL Customer Journey Analytics][&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [前提条件](prerequisites.md)
>* [&#x200B; データ収集、データ転送、レポートの設定](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md)。
