---
title: Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング
description: Customer Journey AnalyticsのAdobe Advertising データに関する問題のトラブルシューティングと解決方法について説明します。
feature: Integration with Adobe Customer Journey Analytics
hide: true
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
    internal-label: Implementation
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: d3cdead0-685a-4489-9250-4bb709942f66
    internal-label: Data collection
source-git-commit: 1a6cdb8f0fcdeee2d223c644da7ded5789cacfd3
workflow-type: tm+mt
source-wordcount: '3428'
ht-degree: 0%
---
# Customer Journey AnalyticsでのAdobe Advertising データのトラブルシューティング

次に潜在的な問題、それらの考えられる原因、および解決策を示します。

## 潜在的な課題のリスト

| イシュー | 詳細 |
| ------- | ---------------- |
| ブラウザーのコード検査ツールの[!DNL Network] タブには、alloy （）呼び出しは表示されません。 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を参照してください |
| コンソールエラー：合金が定義されていません | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」を参照してください> 「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を初期化しません |
| edge.adobedc.netに対してインタラクションまたは収集リクエストは行われません。 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」を参照してください> 「[WebSDK拡張機能が](#websdk-extension-doesn't-initialize)」を初期化しません |
| リクエストはAdobe Experience Platform Edge Networkに到達しますが、400または500 エラーが返されます。 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| Adobe AnalyticsまたはAdobe Advertising レポートにはデータが表示されません。 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| ネットワーク応答のエラー：「データストリームが見つかりません」 | 「[&#x200B; インストールとセットアップの問題](#issues-installation-setup)」/「[&#x200B; データストリームが設定されていないか、設定が正しくありません](#datastream-not-configured-or-misconfigured)」を参照してください |
| web ページのビュースルーコンバージョンまたはクリックスルーコンバージョンは記録されません。 | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |
| クリックスルー用のExperience Data Model （XDM） ペイロードに`_experience.adcloud`がありません。 | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |
| コンバージョンはデバッガーツールで確認されますが、Adobe Advertising レポートには表示されません。 | 「[Advertising拡張機能の設定に関する問題](#advertising-extension-setup-issues)」を参照してください。 |
| ページ間で訪問者IDが変更されます。 | 「[IDとECIDの問題](#identity-and-ecid-issues)」を参照してください |
| Advertisingのオーディエンスセグメントが一致しない。 | 「[IDとECIDの問題](#identity-and-ecid-issues)」を参照してください |
| デバッガーは、ルール条件が満たされていないことを示します。 | 「[&#x200B; ルールまたはイベントが実行されていません](#rules-or-events-don't-fire)」の節を参照してください |
| [!UICONTROL Send Event] アクションは実行されません。 | 「[&#x200B; ルールまたはイベントが実行されていません](#rules-or-events-don't-fire)」の節を参照してください |
| [!DNL Tags]で行われた変更は、ライブサイトに反映されません。 | 「[&#x200B; ライブラリのビルドと公開の問題](#library-build-and-publishing-issues)」の節を参照してください |
| 拡張機能の更新が適用されましたが、古い動作は保持されます。 | 「[&#x200B; ライブラリのビルドと公開の問題](#library-build-and-publishing-issues)」の節を参照してください |
| `alloy()`送信イベント呼び出しは成功しましたが（応答は200）、Adobe Advertising コンバージョンデータがレポートにありません。 | 「[Advertising フィールドのスキーマ検証の問題](#schema-validation-for-advertising-fields)」の節を参照してください。 |
| デバッガーのXDM ペイロードに`_experience.adcloud` オブジェクトが表示されません。 | 「[Advertising フィールドのスキーマ検証の問題](#schema-validation-for-advertising-fields)」の節を参照してください。 |
| Customer Journey Analytics for Advertising DSPまたはAdvertising Search, Social, &amp; Commerceでは、概要レポートデータは利用できません。 | 「[問題の報告](#reporting-issues)」 > 「[概要レポート &#x200B;](#summary-reporting)」の節を参照してください |
| 概要レポートデータは、Customer Journey Analytics for Advertiser 1では利用できますが、Advertiser 2では利用できません。 | 「[問題の報告](#reporting-issues)」 > 「[概要レポート &#x200B;](#summary-reporting)」の節を参照してください |
| （Search, Social, &amp; Commerce ユーザー）概要レポート データは、Customer Journey Analyticsで1つの[!DNL Google Ads]、[!DNL Meta Ads]、または[!DNL Microsoft Advertising] アカウントで利用できますが、別のアカウントでは利用できません。 | 「[問題の報告](#reporting-issues)」 > 「[概要レポート &#x200B;](#summary-reporting)」の節を参照してください |
| Customer Journey Analytics Workspaceの概要レポートデータは、Advertising DSPまたはAdvertising Search, Social, &amp; Commerceのデータと異なり、一部のキャンペーンおよびキャンペーンエンティティの概要データが見つかりません。 | 「[問題の報告](#reporting-issues)」 > 「[概要レポート &#x200B;](#summary-reporting)」の節を参照してください |
| コンバージョンデータ （`Page Views`など）は、CJA Customer Journey Analytics Workspaceのレポートディメンション （`Campaign`など）では使用できません。 | 「[問題の報告](#reporting-issues)」 > 「[&#x200B; イベントレベルの報告](#event-level-reporting)」の節を参照してください |

## インストールとセットアップの問題 {#issues-installation-setup}

### WebSDK拡張機能がを初期化しません#websdk-extension-doesn&#39;t-initialize

#### 問題：

* ブラウザーのコード検査ツールの[!DNL Network] タブには、alloy （）呼び出しは表示されません。
* コンソールエラー：合金が定義されていません。
* edge.adobedc.netに対してインタラクションまたは収集リクエストは行われません。

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| ライブラリが公開されていないか、ドラフト状態です | [公開フロー](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/publishing-flow)に移動し、WebSDK拡張機能を含むライブラリが承認済み/公開済み状態であることを確認します。 |
| 埋め込みコード環境が見つからないか間違っています | Web ページの[[!DNL Tags] 埋め込みコード &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments)が正しい環境（開発/ステージ/実稼動）を参照していることを確認します。 `//assets.adobedtm.com/...` スクリプトタグの`<head>` タグで環境を探します。 |
| 非同期と同期読み込みの競合 | Web ページごとに[[!DNL Tags] 埋め込みコード &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/environments/environments)が1つだけ存在することを確認してください。 重複した埋め込みコードが競合状態の原因となります。 |
| コンテンツセキュリティポリシー（CSP）によるブロック | `edge.adobedc.net` `and assets.adobedtm.com`を[CSP `connect-src`および`script-src` ディレクティブ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/collection/use-cases/configuring-a-csp)に追加します。 |

### データストリームが設定されていないか、設定が正しくありません {#datastream-not-configured-or-misconfigured}

#### 問題：

* リクエストはAdobe Experience Platform Edge Networkに到達しますが、400または500 エラーが返されます。
* Adobe AnalyticsまたはAdobe Advertising レポートにはデータが表示されません。
* ネットワーク応答のエラー：「データストリームが見つかりません」

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| タグプロパティのデータストリーム IDが見つからないか、正しくありません。 | <ol><li>[!DNL Tags]で、タグプロパティの[&#x200B; データストリーム設定設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)を開きます。</li><li>[!UICONTROL Datastream] フィールドが、各環境（開発、ステージング、実稼動）の正しいデータストリーム、および正しいスキーマとデータセットを指していることを確認します。<br><br>3つの環境すべてで1つのデータストリームを明示的に共有しない限り、各環境には独自のデータストリームが必要です。</li></ol> |
| タグプロパティに対してデータストリームサービスが有効になっていません。 | [&#x200B; データストリーム設定](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)を開き、次のサービスが有効になっていることを確認します。<ul><li>Adobe Advertising（コンバージョン/オーディエンス同期用）</li><li>Adobe Experience Platform（プロファイル取得用）</li></ul> |
| サンドボックスの不一致 | データストリームが、スキーマおよびデータセットと同じ[Adobe Experience Platform サンドボックス &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/sandbox/home)に属していることを確認します。 よくある間違いは、実稼動サンドボックスにデータストリームを作成する際に、開発サンドボックスにスキーマを指定することです。 |

### [!UICONTROL Advertising]拡張機能の設定に関する問題 {#advertising-extension-setup-issues}

#### 問題：

* web ページのビュースルーコンバージョンまたはクリックスルーコンバージョンは記録されません。

  コンバージョンが記録されているかどうかを確認するには：

  1. URLに`ef_id=test&s_kwcid=test`が追加されたweb ページを開きます。
  1. ブラウザーのコード検査ツール（[!DNL Inspect]と呼ばれることが多い）を開き、「[!DNL Network]」タブを開き、Adobe Experience Platformのevent_type=&quot;advertising.enrichment_ct&quot;のインタラクティブ呼び出しを探します。
  1. データ収集インターフェイスで、[収集するweb サイト データのスキーマ定義](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas)を開き、`xdm->_experience->adcloud->conversionDetails->trackingCode`と`trackingIdentities`に`ef_id`と`s_kwcid`が含まれていることを確認します。

* クリックスルー用のExperience Data Model （XDM） ペイロードに`_experience.adcloud`がありません。

* コンバージョンはデバッガーツールで確認されますが、Adobe Advertising レポートには表示されません

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| データストリームに対して`Adobe Advertising` サービスが有効になっていません。 | <ol><li>[!DNL Tags]で、タグプロパティの[&#x200B; データストリーム設定設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/datastreams)を開きます。</li><li>次のサービスを有効にし、設定を保存します。<ul><li>Adobe Advertising（コンバージョン/オーディエンス同期用）</li><li>Adobe Experience Platform（プロファイル取得用）</li></ul></ol> |
| `Adobe Advertising` コンポーネントは[!UICONTROL WebSDK]拡張機能に対して有効になっていません。 | WebSDK拡張機能の`Adobe Advertising` コンポーネントはデフォルトで無効になっており、XDM スキーマまたはルールの設定方法に関係なく、Adobe Advertising クリックスルーまたはビュースルーのトラッキングが機能する前に、明示的に有効にする必要があります。<ol><li>[!DNL Tags]で、Adobe Experience Platform Web SDKの設定[&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/custom-build-components)で、プロパティの ビルドオプションを開きます。</li><li>**Advertising** コンポーネントを有効にし、設定を保存します。</li><li>ライブラリを再構築して再公開します。</li></ol> |
| クリックスルーコンバージョンのみが記録されます。ビュースルーコンバージョンは表示されません。 | これは期待されるデフォルトの動作です。 `Adobe Advertising` コンポーネントが有効になると、`s_kwcid`および`ef_id`のURL クエリパラメーターを使用して、クリックスルー追跡が自動的にアクティブになります。 ビュースルートラッキングはデフォルトで無効になっており、追加の設定が必要です。次の行を参照してください。 |
| ビュースルー追跡が有効になっていないか、設定されていません。 | <ol><li>データストリームのAdobe Advertising サービスを有効にする</li><ol><li>Adobe Experience Platformの[!UICONTROL Data Collection] > [!UICONTROL Datastreams]に移動し、[!DNL Tags] プロパティで使用されているデータストリームを開きます。</li><li>**サービスを追加**&#x200B;を選択し、**Adobe Advertising**&#x200B;および&#x200B;**Adobe Experience Platform**&#x200B;を選択してから、**保存**&#x200B;を選択します。</li></ol><li>Adobe Advertising DSPでの広告主の設定</li><ol><li>[!DNL Tags]で、[!UICONTROL Extensions] > [!UICONTROL Installed] > **Adobe Experience Platform Web SDK** > [!UICONTROL Configure]に移動します。</li><li>「[!UICONTROL Advertiser]」セクションで、ドロップダウンから広告主を選択して有効にします。 複数の広告主を設定するには、**広告主を追加**&#x200B;を選択します。</li></ol><li>ビュースルーコンバージョンピクセルが起動していることを確認します</li><ol><li>Adobe Experience Platform Debuggerで、`xdm.query` フィールドの下に`stitchId`が含まれていることを確認します。</li><li>ブラウザーのコード検査ツールの「[!DNL Network]」タブで、タイプ `advertising.enrichment`のイベントが発生し、`xdm.query`の下に`stitchId`が含まれていることを確認します。</li></ol></ol> ビュースルーコンバージョンは、訪問数に関係なく、30分ごとに実行されます。 インタラクション呼び出しが表示されない場合は、ブラウザーのキャッシュをクリアして、もう一度試してください。 |
| ビュースルーインタラクション呼び出し発生後、Experience Platformで使用できるビュースルーイベント領域がありません。 | WebSDK拡張機能の設定[&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/advertising)の[!UICONTROL Advertiser] セクションで、広告主が設定され、有効になっていることを確認します。 広告主が手動で入力された場合は、代わりに[!UICONTROL Advertiser] ドロップダウンから広告主を再選択します。 広告主を設定したら、ライブラリを再構築して再公開します。 |

[!UICONTROL Advertising]拡張機能の設定に関するサポートチケットを開く前に、次の点を確認してください。

* **Adobe Advertising**&#x200B;および&#x200B;**Adobe Experience Platform** サービスがデータストリームに追加されます。
* **Adobe Advertising** コンポーネントは、WebSDK拡張機能コンフィギュレーションで有効になっています。
* コンポーネントを有効にした後、ライブラリが再構築され、再公開されました。
* クリックスルー追跡の場合、ランディングページ URLには、広告クリック時に`s_kwcid`と`ef_id`が含まれます。
* ビュースルートラッキングの場合、広告主はAdobe Advertising DSPで正しい広告主IDで設定されます。
* WebSDK拡張機能は、バージョン 2.36.0以降です。

### IDとECIDの問題 {#identity-and-ecid-issues}

#### 問題：

* ページ間で訪問者IDが変更されます。
* Advertisingのオーディエンスセグメントが一致しない。

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| サードパーティ Cookieはブロックされています。 | [&#x200B; データストリームのEdge Network設定でファーストパーティ Cookie IDを設定することで、ファーストパーティ CNAME データ収集に移行します](https://experienceleague.adobe.com/en/docs/experience-platform/datastreams/configure)。 |
| レガシー`s_ecid` Cookieが存在する間、`idMigrationEnabled`は`false`に設定されます。 | [WebSDK ベース設定](https://experienceleague.adobe.com/en/docs/experience-platform/tags/extensions/client/web-sdk/configure/identity)で`idMigrationEnabled: true`を設定して、既存のECIDを`s_ecid`または`AMCV_` Cookieから移行します。 |

### ルールまたはイベントが実行されない#rules-or-events-don&#39;t-fire

#### 問題：

* デバッガーは、ルール条件が満たされていないことを示します。
* [!UICONTROL Send Event] アクションは実行されません。

#### 検証と解決

次の点を確認します。

* ルールが保存され、アクティブな[&#x200B; ライブラリビルド &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/builds)に含まれます。
* イベントタイプは、実際のページ動作（[!UICONTROL Library Loaded]対[!UICONTROL DOM Ready]対[!UICONTROL Window Loaded]など）と一致します。
* ルールの条件はそれほど制限されていません。 一時的に[条件を削除](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)してテストし、問題を分離します。
* ルールの順序は正しいです。 複数のルールが同じイベントを共有する場合は、[&#x200B; ルールの順序](https://experienceleague.adobe.com/en/docs/experience-platform/tags/ui/rules)を確認してください。
* ページの以前のJavaScript エラーで実行が停止することはありません。 ブラウザーコンソールで捕捉されない例外がないか確認します。

### ライブラリのビルドと公開の問題 {#library-build-and-publishing-issues}

#### 問題：

* [!DNL Tags]で行われた変更は、ライブサイトに反映されません。
* 拡張機能の更新が適用されましたが、古い動作は保持されます。

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| 変更はライブラリに追加されませんでした。 | 公開ワークフローで、変更内容が開発環境の[&#x200B; ライブラリ &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/libraries)に追加されたことを確認します。 [&#x200B; ライブラリに変更を加える](https://experienceleague.adobe.com/en/docs/experience-platform/tags/publish/libraries#manage-library-changes)場合は、リソースを追加してから、ライブラリを保存して構築します。 |
| ブラウザーが古いライブラリをキャッシュしています。 | ハードリフレッシュ（Ctrl+Shift+RまたはCmd+Shift+R）を実行するか、シークレットウィンドウまたはプライベートウィンドウでページを開きます。 問題が解決しない場合は、ブラウザーのキャッシュを完全にクリアします。 |
| 埋め込みコードは環境が間違っています。 | ページの埋め込みコードが正しい環境用であることを確認します。 例えば、実稼動動作をテストする場合、埋め込みコードが実稼動埋め込みコードであることを確認します。 |
| ライブラリのビルドがサイレントで失敗しました。 | 公開ワークフローで、ライブラリに[!UICONTROL Build Failed]状態が表示されているかどうかを確認します。 ライブラリを開き、ビルドログを確認します。ビルドエラーの一般的な原因は、無効なルール設定または拡張機能のバージョンの競合です。 |

### Advertising フィールドのスキーマ検証の問題 {#schema-validation-for-advertising-fields}

#### 問題：

* `alloy()`送信イベント呼び出しは成功しましたが（応答は200）、Adobe Advertising コンバージョンデータがレポートにありません。
* デバッガーのXDM ペイロードに`_experience.adcloud` オブジェクトが表示されません。

#### 考えられる原因と検証/解決

| 原因 | 修正 |
| ----- | --- |
| スキーマに[!UICONTROL Advertising] フィールドグループがありません。 | <ol><li>Adobe Experience Platform > [!UICONTROL Data Management] > [!UICONTROL Schemas]に移動します。</li><li>データストリームで使用するスキーマを開きます。</li><li>[!UICONTROL Field Groups] パネルで、**Adobe Advertising Cloud ExperienceEvent Full Extension**&#x200B;がリストされていることを確認します。</li><li>見つからない場合は、**追加**&#x200B;を選択し、**Adobe Advertising Cloud**&#x200B;を検索し、**Adobe Advertising Cloud ExperienceEvent Full Extension**&#x200B;を選択して、設定を保存します。</li></ol>スキーマの変更だけでは[!DNL Tags] ライブラリを再公開する必要はありませんが、新しいフィールドが追加された場合は、[!DNL Tags]でXDM データ要素を再マッピングする必要があります。 |
| 必須のAdobe Advertising フィールドがスキーマにありません。 | 必須のAdobe Advertising フィールドが`_experience.adcloud.conversionDetails`の[&#x200B; スキーマ &#x200B;](https://experienceleague.adobe.com/en/docs/platform-learn/implement-web-sdk/initial-configuration/configure-schemas)に存在することを確認してください。 「[参照：必須スキーマフィールド &#x200B;](#required-schema-fields)」を参照してください。<br><br>いずれかのフィールドが見つからない場合は、**Adobe Advertising Cloud ExperienceEvent Full Extension** フィールドグループがスキーマに保存されていることを確認してから、スキーマエディターを更新してください。 |
| ランディングページのURLには、必要なクエリパラメーターが含まれていません。 | ランディングページのURLに、必要なクエリパラメーターが含まれていることを確認します。 広告のクリックスルーでは、ランディングページのURLに、`s_kwcid`と`ef_id` パラメーター（`https://www.example.com/landing-page?s_kwcid=AL!12345!3!abc123&ef_id=abc123xyz:G:s`など）の両方のクエリを含める必要があります。 考えられる原因については、「[参照：見つからないクエリパラメーター](#missing-query-parameters)」を参照してください。 |
| XDM ペイロードの一部のパラメーターが見つからないか、空です。 | アウトバウンド XDM ペイロードを検証するには、ブラウザーのコード インスペクションツールの「Adobe Experience Platform Debugger」タブまたは「[!DNL Network]」タブを開き、`edge.adobedc.net`のフィルターを実行し、インタラクションのリクエスト本文を調べます（以下のペイロードの例を参照）。<br><br>もし`trackingCode`または`trackingIdentity`が空または見つからない場合、a） ルールが実行されたときにクエリパラメーターがページに存在しなかった（URLとルールのイベントタイミング確認）またはb）。 |

##### 参照：必須スキーマフィールド {#required-schema-fields}

| フィールドパス | タイプ | 説明 |
| ----- | --- | --- |
| `_experience.adcloud.conversionDetails.trackingCode` | 文字列 | コンバージョンを元の広告クリックにマッピングします。 ランディングページ URLの`s_kwcid` クエリパラメーターから入力されました。 |
| `_experience.adcloud.conversionDetails.trackingIdentity` | 文字列 | 追跡されたビュースルーまたはクリックスルーのコンバージョンイベントの一意のIDおよびその他の詳細を保存します。 ランディングページ URLの`ef_id` クエリパラメーターから入力されました。 |

##### 参照：クエリパラメーターがありません {#missing-query-parameters}

| パラメーターがありません | 考えられる原因 |
| ----- | --- |
| `s_kwcid` | Adobe Advertising検索またはDSP キャンペーン設定では、自動タグ付けは有効になっていません。 |
| `ef_id` | ランディングページのURLがAdobe Advertisingで追跡されたリダイレクトを使用していないか、キャンペーン設定でEF IDの追加が有効になっていません。 |

**クリックスルーのペイロードの例**

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

## Customer Journey Analytics Workspaceのレポートの問題

### 概要レポート

| イシュー | 検証と解決 |
| ----- | --- |
| Customer Journey Analytics for Advertising DSPまたはAdvertising Search, Social, &amp; Commerceでは、概要レポートデータは利用できません。 | <ol><li>Customer Journey Analytics Workspaceが正しいデータビューを参照していることを確認します。</li><li>Adobe AdvertisingからCustomer Journey Analyticsへのフィードが有効になっていることを確認します。 Adobeのアカウントチームにお問い合わせください。</li><li>Adobe Advertising ディメンション/分類/参照データセットとサマリーデータセットがCustomer Journey Analytics接続に含まれていることを確認します。</li><li>Adobe Advertisingのディメンションと概要指標がCustomer Journey Analytics データビューに含まれていることを確認します。</li></ol>上記のすべての設定を確認しても概要データが表示されない場合は、組織の[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support)を開きます。 |
| 概要レポートデータは、Customer Journey Analytics for Advertiser 1では利用できますが、Advertiser 2では利用できません。 | <ol><li>Adobe AdvertisingからCustomer Journey AnalyticsへのフィードがAdvertiser 2に対して有効になっていることを確認します。 Adobeのアカウントチームにお問い合わせください。</li><li>Customer Journey Analytics接続で3つのデータセット（ディメンション/分類/ルックアップ、サマリー、イベント指標）に対して設定「[!UICONTROL Backfill all existing data]」が有効になっていることを確認します。</li></ol>上記の条件をすべて確認しても概要データが表示されない場合は、組織の[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support)を開きます。 |
| （Search, Social, &amp; Commerce ユーザー）概要レポート データは、Customer Journey Analyticsで1つの[!DNL Google Ads]、[!DNL Meta Ads]、または[!DNL Microsoft Advertising] アカウントで利用できますが、別のアカウントでは利用できません。 | Adobe AdvertisingからCustomer Journey Analyticsへのフィードが、特定の広告ネットワークアカウントに対して有効になっていることを確認します。 Adobe アカウントチームにお問い合わせください。<br><br> フィードがアカウントに対して有効になっていても概要データが表示されない場合は、組織の[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support)を開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。 |
| Customer Journey Analytics Workspaceの概要レポートデータは、Advertising DSPまたはAdvertising Search, Social, &amp; Commerceのデータと異なり、一部のキャンペーンおよびキャンペーンエンティティの概要データが見つかりません。 | <ol><li>[!DNL Workspace]とAdobe Advertising レポートの両方で同じ日付範囲を使用していることを確認してください。</li><li>[!DNL Workspace]とAdobe Advertising レポートに適用されているフィルターとセグメントが、データの違いを引き起こしていないことを確認します。</li><li>Customer Journey Analytics データビューの[!UICONTROL Time Zone]が、[Advertising DSP アカウント &#x200B;](/help/dsp/admin/user-own-profile-edit.md)の[!UICONTROL Default Timezone]と一致することを確認してください。</li><li>Customer Journey Analytics接続で3つのデータセット（ディメンション/分類/ルックアップ、サマリー、イベント指標）に対して設定「[!UICONTROL Backfill all existing data]」が有効になっていることを確認します。</li></ol>データの相違が確認できる場合は、組織の[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support)を開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。 食い違いの証拠を示すには、スクリーンショットとスプレッドシートを含めます。 Adobe アカウントチームは、必要に応じてデータフィードを過去にさかのぼって修正し、差異を解決できます。 |

### イベントレベルのレポート

| イシュー | 検証と解決 |
| ----- | --- |
| コンバージョンデータ （`Page Views`など）は、Customer Journey Analytics Workspaceのレポートディメンション （`Campaign`など）では使用できません。 | 以下を確認します。最初に、検証障壁が最も少ない項目を確認します。<ul><li>正しいデータビューを使用していることを確認してください。</li><li>該当するコンバージョン指標がweb/オンラインイベントであり、Adobe Advertisingがディメンションに関連付けられていることを確認します。</li><li>Adobe Advertisingが、該当するサイトのクリックスルーとビュースルーを追跡していることを確認します。</li><li>分類データセットのCustomer Journey Analytics接続で、[!DNL Key]および[!DNL Matching Key]設定の値が正しいことを確認します：[!DNL Key]: `Tracking Code` （_customername.adLens2.trackingCode）、[!DNL Matching Key]: `Tracking Code` （event._experience.adcloud.conversionDetails.trackingCode）。</li><li>[!DNL Adobe Advertising] サービスがAdobe Experience Platform データストリームに追加されていること、データストリーム用にマッピングされたスキーマが`XDM ExperienceEvent Schema`であること、フィールドグループ `Adobe Advertising Cloud ExperienceEvent Full Extension`が`XDM ExperienceEvent` スキーマに追加されていることを確認します。</li><li>Adobe Advertisingの設定がWebSDK拡張機能で正しく設定され、公開されていることを確認します。</li></ul>上記のすべての設定を確認しても、コンバージョンデータが表示されない場合は、組織の[&#x200B; サポートチケット &#x200B;](https://experienceleague.adobe.com/home?support-tab=home#support)を開きます。 広告ネットワーク アカウントの[!UICONTROL Account ID]を含めます。 |

## 便利な検証ツールとデバッグツール

### Adobe Experience Platform Debugger

[!DNL Chrome]の[!DNL Adobe Experience Platform Debugger]拡張機能をインストールします：

* すべてのWebSDK `alloy()`呼び出しのリアルタイム ビュー
* データストリーム IDと環境の検証
* XDM ペイロード検査
* Edge Networkのリクエストとレスポンスの詳細

デバッガーのキーチェック：

| Tab | 確認すべきこと |
| ----- | --- |
| [!UICONTROL Summary] | WebSDKが検出され、インストールされているバージョンが表示されることを確認します。 |
| [!UICONTROL Adobe Experience Platform WebSDK] | 発生した各イベント、完全なXDM ペイロード、Edge Network応答を示します。 |
| [!UICONTROL Adobe Advertising] | AMO ID キャプチャとXDM インタラクション呼び出しを`advertising.enrichment` イベントタイプで確認します。 |

### ブラウザーのコード検査ツールの[!DNL Network] タブ

ブラウザーのコード検査ツール（「[!DNL Inspect]」と呼ばれることが多い）の「[!DNL Network]」タブを使用して、次の操作を行います。

生のEdge Network リクエストを調べるために`edge.adobedc.net`でフィルタリングします。

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

## サポートをリクエストする前に、クイックリファレンスチェックリストを参照する

サポートチケットを開封する前に、次の点を確認してください。

* WebSDK拡張機能は最新バージョンです。
* ライブラリが公開され、埋め込みコードが環境に適しています。
* データストリーム IDは、開発、ステージング、実稼動用に正しく設定されます。
* 必要なすべてのデータストリームサービスが有効になります。
* [!UICONTROL Advertising] コンポーネントはWebSDK拡張機能の設定で有効になっており、DSP広告主IDが設定されています。
* XDM スキーマには、[!UICONTROL Advertising] フィールドグループが含まれています。
* [!UICONTROL Send Event] ルールにはID マップが含まれており、正しいイベントに対して実行されます。
* Edge Network リクエストをブロックしているCSPまたはブラウザーのプライバシー設定はありません。
* Adobe Experience Platform Debuggerは、出来事がEdge Networkに到達していることを認める。
* ブラウザーコンソールで実行を停止しているJavaScript エラーはありません。
* `Adobe Advertising Cloud ExperienceEvent Full Extension` フィールドグループがスキーマに追加されます。
* `_experience.adcloud.conversionDetails.trackingCode`はスキーマに存在します。
* `_experience.adcloud.conversionDetails.trackingIdentity`はスキーマに存在します。
* ランディングページ URLには、クリックスルー時に`s_kwcid`と`ef_id`の両方のパラメーターが含まれています。
* Adobe Experience Platform Debuggerは、`conversionDetails`がアウトバウンドペイロードに入力されていることを確認します。

## 問題をエスカレーションするタイミング

次の場合は、Adobeのアカウントチームまたはエンジニアリングチームにお問い合わせください。

* Edge Network リクエストは、データストリームの検証後に永続的な`500` エラーを返します。
* [!UICONTROL Advertising]個のコンバージョンがデバッガーで確認されますが、24 ～ 48時間後にレポートに表示されません。
* WebSDK バージョンのアップデートでは、以前のバージョンには存在しなかった回帰が導入されます。 サポートチケットに特定のバージョン番号を含めます。

>[!MORELIKETHIS]
>
>* [概要](overview.md)
>*  [!DNL Customer Journey Analytics]&#x200B;[&#128279;](ids.md)様が使用しているAdobe Advertising ID
>* [前提条件](prerequisites.md)
>* [&#x200B; データ収集、データ転送、レポートの設定](set-up.md)
>* [Customer Journey AnalyticsのAdobe Advertising指標とディメンション &#x200B;](advertising-data-in-cja.md)
>* （Adobe Analytics ユーザー） [Adobe Customer Journey Analyticsで使用するAMO IDとEF IDの履歴データを収集](/help/integrations/analytics/rvars-to-evars.md)。
