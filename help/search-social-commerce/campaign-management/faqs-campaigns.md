---
title: キャンペーンに関する FAQ
description: キャンペーン管理とキャンペーンデータビューに関する質問への回答を参照してください。
exl-id: b5975869-4bc3-461d-8cb7-eeefab157137
feature: Search Campaign Management
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '1472'
ht-degree: 0%

---

# キャンペーン管理に関する FAQ

## 一般情報

+++キャンペーンとコンポーネントを別のアカウントに移動させることはできますか？

一意の ID を持つキャンペーンまたはキャンペーンコンポーネントを、別のアカウント ID を持つアカウントに移動またはコピーしないでください。 これを行うと、データエラーが発生します。
+++

+++クリックデータは広告ネットワークからいつ更新されますか？

前日のクリックデータを検索エンジンから取り込むプロセスは、広告主のタイムゾーンの 06:00 に開始されます。

さらに、 [!DNL Google Ads] 現在の日付の検索ネットワーク上のキャンペーンレベルのパフォーマンス指標は、広告主のタイムゾーンの 08:00 および 16:00 に取り込まれます。
+++

+++キーワードおよび広告が履歴を失う原因となるアクションは何ですか？

>[!NOTE]
>
>（ポートフォリオを持つ広告主）新しいキーワードと一致タイプの組み合わせは、不安定なパフォーマンスを期待し、Search、Social、および Commerce でデータを収集して新しいモデルを作成します。

**Adobe Analytics の [!UICONTROL Search] > [!UICONTROL Campaigns] 表示、一括送信シートの投稿プロセスおよび広告ネットワーク独自のエディターで：**

既存のキーワードまたは広告は削除され、次の場合に別のキーワードまたは広告が作成されます。

* ([!DNL Baidu], [!DNL Google Ads]、および [!DNL Yandex]) キーワード名を編集します。

* ([!DNL Google Ads], [!DNL Microsoft Advertising]、および [!DNL Yandex]) キーワードの一致タイプを変更します。

* キーワードを広告グループ間で移動します。

* ([!DNL Google Ads] 動的検索広告、 [!DNL Microsoft Advertising] 拡張テキスト広告と、他のサポートされている広告ネットワーク上のすべての広告タイプ ) 広告コピー（ヘッドライン/タイトルまたは説明）または広告イメージを編集します。

* 広告を広告グループ間で移動します。

**製品在庫フィード転記プロセスのイベント：**

既存の広告またはキーワードは次の場合に削除され、別の広告またはキーワードが作成されます。

* フィードファイルには、広告バリエーションで使用される列の新しい値が含まれます。

* 広告のテンプレート設定は、最後の伝播以降に変更されました。

* 新しいフィードファイルには、前のファイルにある広告またはキーワードの行 (a) が、その後、省略され、フィードデータの設定に従って一時停止または削除された行が含まれます。

に応じて [フィードデータ設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings)、以下の場合に、既存の広告またはキーワードが削除される可能性があります。

* 新しいフィードファイルには、既存の広告やキーワードの行が含まれていません。

* 投稿されたフィードファイルのコンポーネントに対する予定終了日が発生します。

* 品目の在庫レベルは、フィードデータ設定で指定された最小値を下回って低下します。
+++

+++([!DNL Google Ads] campaigns) 自分の表示名の変更 [!DNL Google]-tracked conversions は元に戻されました。

検索、ソーシャル、コマースでのコンバージョン指標の表示名を変更すると、変更内容が [!DNL Google Ads]. 内で名前を変更します。 [!DNL Google Ads].
+++

+++(Google Ads キャンペーン ) ポートフォリオ内のキャンペーンに共有予算を使用できますか。

最適な結果を得るには、を追加しないでください [!DNL Google Ads] キャンペーンの [!DNL Google Ads] 共有予算 (「[!UICONTROL Auto adjust campaign budget limits].&quot; もしそうなら [!DNL Google Ads] は、検索、ソーシャル、コマースに最適化されたキャンペーン予算を上書きします。これにより、入札の非効率性が高まる可能性があります。
+++

+++([!DNL Google Ads] キャンペーン ) モバイルユーザーとモバイル以外のユーザーを異なるランディングページに送信することはできますか？

以下を使用すると、 [!DNL Google Ads] [!DNL ValueTrack] パラメーター `{ifmobile}` および `{ifnotmobile}` を使用して、サイトに適した 2 つの方法のいずれかでランディングページのドメイン名を特定するには、次の手順を実行します。

* 次を使用して、モバイルの宛先をホストサーバーとして含めます。 `{ifmobile:m}{ifnotmobile:www}`.

  例： `http://{ifmobile:m}{ifnotmobile:www}.example.com` はモバイルユーザーをm.example.comに、非モバイルユーザーはwww.example.comに移動します。

* 次を使用してモバイル指定をトップレベルドメインに含めます。 `{ifmobile:mobi}{ifnotmobile:com}`.

  例： `http://www.example.{ifmobile:mobi}{ifnotmobile:com}` はモバイルユーザーをwww.example.mobi に、非モバイルユーザーはwww.example.comに移動します。

どちらの場合も、検索、ソーシャル、コマースのトラッキング機能を持つベース URL には、エンコードされていない `{}` タグおよびベース URL に追加された追加のパラメーター。

>[!NOTE]
>
>ifnotmobile および ifmobile パラメータの値には、完全な URL を使用しないでください。URL の変数部分（「m」と「www」、「mobi」と「com」など）のみを使用します。

+++

+++([!DNL Google Ads] （検索ネットワーク上のキャンペーン）今日はどのデータが表示されますか。

[!DNL Google Ads] 現在の日付の検索ネットワーク上のキャンペーンレベルのパフォーマンス指標は、広告主のタイムゾーンの 08:00 および 16:00 に取り込まれます。

Adobe Analytics の [!UICONTROL Campaigns] タブ [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示と [!UICONTROL Optimization] > [!UICONTROL Portfolios] 表示、次の項目に関するレポートを作成する [!UICONTROL Today] または、現在の日付を含むカスタム日付範囲の場合、データには最近取り込まれたデータが含まれます。

>[!NOTE]
>
>クリック数、インプレッション数およびコンバージョン数のデータは、3 時間遅れ、次のデータが取り込まれるまで完了しません。

+++

+++([!DNL Google Ads] および [!DNL Microsoft Advertising]) 検索、ソーシャル、コマースは、 [!DNL Google Ads] または [!DNL Microsoft Advertising]?

並列トラッキングでは、顧客を広告から最終的な URL に直接送信し、トラッキングテンプレートの URL（クリック指標を使用）がバックグラウンドに読み込まれるので、ランディングページの読み込みがより迅速になります。

Search, Social, &amp; Commerce は、広告ネットワークのクリック識別子 (`msclkid` 対象： [!DNL Microsoft Advertising]; `gclid` 対象： [!DNL Google Ads]) をクリックします。 を使用します。 [アカウントレベル](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md#account-settings) または [キャンペーンレベル](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md) [!UICONTROL Landing Page Suffix] ( 呼び出し名：[!DNL final URL suffix]」 （広告ネットワーク内）に追加され、並列追跡をサポートするブラウザーからの子広告のクリック数を追跡するためのランディングページ URL に追加されます。 詳しくは、 [必要なサフィックス形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) および [必要なサフィックス形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).

並列追跡をサポートしないブラウザーで広告を表示した場合、広告ネットワークは順次追跡を使用します。顧客は最初にトラッキングテンプレートの URL に送信され、顧客を最終的な URL にリダイレクトする前に中間トラッキングサーバーにリダイレクトできます。 広告ネットワークアカウントのすべてのトラッキングテンプレートに、 [!UICONTROL Landing Page Suffix]. 詳しくは、 [のトラッキングテンプレート形式 [!DNL Google Ads]](/help/search-social-commerce/tracking/formats-click-tracking-google.md) そして [のトラッキングテンプレート形式 [!DNL Microsoft Advertising]](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md).
+++

+++広告のトラッキング URL に「`&EV_HASH={<hash>}`?」

を使用して広告をアップロードする場合 [製品在庫フィード](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md) 検索、ソーシャル、コマースのピクセルリダイレクトを含むアカウントで、キーワードおよびクリエイティブレベルの追跡を含む場合、検索、ソーシャル、コマースは、ハッシュパラメーターと値を広告のトラッキングテンプレートまたは宛先 URL に追加し、在庫フィード機能を使用して作成したことを識別します。
+++

## 在庫フィード

+++（製品在庫フィード）古い広告や、在庫レベルが指定された最小値を下回る製品の広告を一時停止または削除する必要がありますか。

広告主のビジネス要件によって異なります。

広告を一時停止すると、同じ広告を再送信するか、在庫レベルが最小値を超えると、広告が再アクティブ化されます。 これにより、広告の履歴を保持できます。

広告を削除して再送信すると、新しい広告が作成され、履歴データを蓄積する必要があります。 ただし、削除された広告を再送信しない場合は、履歴データを持つことは重要ではありません。
+++

+++（製品在庫フィード）広告テンプレートを削除してから新しい同一のテンプレートを作成した場合、（フィードファイルの設定で一時停止された）次のフィードファイルに項目が見つかりませんか。

次のフィードファイルに行項目がなく、以前のフィードファイルを使用して新しいテンプレートからこれらの行項目を以前に投稿したことがない場合、見つからない行項目は「見つからない」と認識されないので、作成されません。 これを回避するには、新しいテンプレートを通じて前のフィードファイルを伝播し、新しいファイルからデータを伝播および投稿する前に、データを投稿します。
+++

+++（製品在庫フィード）広告の品質スコアに影響を与えることなく、製品の価格を更新できますか。

の場合 [!DNL Google Ads] キャンペーン（はい）: [!DNL Google Ads] `{Param 1}` および `{Param 2}` 変数を使用すると、広告を削除したり再作成したりせずに、結果として品質スコアに影響を与えることなく、広告バリエーションに数値を動的に挿入できます。

次の手順で `{Param 1}` または `{Param 2}` 変数を価格データ用に作成し、データファイルの価格列を適切なフィードテンプレートでその変数にマッピングして、変数を広告バリエーションテンプレートに含めます。

例えば、列の名前が「Price」の場合、広告を作成するフィードテンプレートを開き、の横にある入力フィールドをクリックします。 **[!UICONTROL Param 1]**&#x200B;をクリックし、 **[!UICONTROL Price]** 列の [!UICONTROL Feeds/Available Columns] リスト。挿入される `[Price]` の価値として [!UICONTROL Param 1]. 次に、フィードテンプレートの下部にある広告バリエーションテンプレートで、 `{param1:default text}`（「default text」は、フィードファイル内のパラメーター列が広告行で空の場合に使用するテキストです）。

データを送信する際に、 [!UICONTROL Param1] および [!UICONTROL Param2] 列には、数値データ、通貨記号および通貨コードを含む、最大 25 文字までの文字と、次の数値以外の文字を含めることができます。 `, . % + - /`
+++

+++在庫フィードから生成されたキャンペーンに、多くの孤立したトランザクションが含まれています。

次の場合、 [フィードデータ設定](/help/search-social-commerce/campaign-management/inventory-feeds/feed-settings-manage.md#feed-data-settings) は、様々な状況で広告を削除するように設定され、広告のクリック後に発生する遅延コンバージョンは、 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p). 広告を削除する代わりに一時停止することをお勧めします。 長い期間も広告が売上高を受け取っていない場合は、バルクシートまたは広告管理ビューを使用して削除できます。
+++

## アカウントおよびキャンペーンに関するパフォーマンスの問題

+++一部のキャンペーンがキャンペーン予算より多かれ少なかれ費やしています。

* これは、「[!UICONTROL Auto-adjust campaign budget limits]&quot;オプション。 このオプションを有効にした場合、最大で *N* 各キャンペーンの予算の時間 *N* は、[!UICONTROL Multiple]&quot;設定中です。 このオプションを使用すると、最適化機能で、必要に応じて個々のキャンペーンの支出を調整し、ポートフォリオ全体をターゲットに合わせて操作できます。
* 次の場合 [!DNL Google Ads] キャンペーンで共有予算を使用し、 [!DNL Google Ads] は、共有予算全体を費やすために必要に応じて、個々のキャンペーンの支出を調整します。
+++
