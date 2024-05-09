---
title: 間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising
description: 間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '3212'
ht-degree: 0%

---

# 間で予期されるデータの相違 [!DNL Analytics] とAdobe Advertising

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

を使用した広告主 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 統合は、Adobe AdvertisingとAdobe Analyticsを通じて有料広告を追跡します。 複数のシステムを使用してメディア、キャンペーン、チャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Adobe Advertisingを通じてトラフィックが発生したメディアのデータを、メディアがトラッキングされる様々なシステムのデータと比較する方法について説明します [!DNL Analytics].

>[!NOTE]
>
>このドキュメントでは、Adobe Advertisingと分析に重点を置いていますが、重要な点の多くは、他のトラッキングソリューションにも転送できます。

## 類似レポートにおけるアトリビューションの違い

### 潜在的に異なるルックバックウィンドウとアトリビューションモデル

この [!DNL Analytics for Advertising] の統合には、次の 2 つの変数を使用します（[!DNL eVars] または [!DNL rVars] \[ 予約済み [!DNL eVars]]\）を使用して、 [EF ID と AMO ID](ids.md). これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーが関連付けられる期間）とアトリビューションモデルを使用して設定されます。 特に指定がない限り、変数は、Adobe Advertisingのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、 [!DNL eVars]）と入力し、Adobe Advertisingで指定します。 さらに、Adobe Advertisingすると、アトリビューションモデルは、広告主レベル（入札最適化の場合）だけでなく、個々のデータビューおよびレポート（レポート目的の場合のみ）でも設定できます。 例えば、ある組織が最適化のために偶数分布アトリビューションモデルを使用し、Advertising DSPまたは [!DNL Advertising Search, Social, & Commerce]. アトリビューションモデルを変更すると、アトリビューションコンバージョンの数が変更されます。

レポートルックバックウィンドウまたはアトリビューションモデルが一方の製品で変更され、もう一方の製品では変更されていない場合、各システムの同じレポートに異なるデータが表示されます。

* **様々なルックバックウィンドウによって発生する不一致の例：**

  Adobe Advertisingに 60 日間のクリックのルックバックウィンドウがあり、 [!DNL Analytics] には、30 日間のルックバックウィンドウがあります。 あるユーザーが、Adobe Advertisingが追跡した広告を通じてサイトを訪問し、離脱した後、45 日目に戻り、コンバージョンを行ったとします。 Adobe Advertisingでは、コンバージョンが 60 日間のルックバックウィンドウ内で発生したため、コンバージョンは最初の訪問に関連付けられます。 [!DNL Analytics]ただし、は、コンバージョンが 30 日のルックバックウィンドウの有効期限が切れた後に発生したため、コンバージョンを最初の訪問に関連付けることはできません。 この例では、Adobe Advertisingは、次よりも多くのコンバージョン数をレポートします [!DNL Analytics] 可能性あり。

  ![Adobe Advertisingは起因するが起因しないコンバージョンの例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **様々なアトリビューションモデルによって生じる不一致の例：**

  ユーザーがコンバージョンする前に、売上高をコンバージョンタイプとして、3 つの異なるAdobe Advertising広告を操作したとします。 Adobe Advertisingレポートでアトリビューションに偶数配分モデルを使用する場合、売上高はすべての広告に均等に関連付けられます。 次の場合 [!DNL Analytics] はラストタッチ アトリビューションモデルを使用しますが、売上高は最後の広告に関連付けられます。 次の例では、3 つのAdobe Advertisingのそれぞれに取り込まれた売上高 30 USD のうち 10 USD までがの属性となります [!DNL Analytics] ユーザーが閲覧した最後の広告までのすべての 30 USD の売上高を属性にします。 Adobe Advertisingのレポートとを比較する場合 [!DNL Analytics]アトリビューションの違いの影響を確認できると思います。

  ![Adobe Advertisingとに起因する異なる収益 [!DNL Analytics] 様々なアトリビューションモデルに基づく](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>ベストプラクティスは、Adobe Advertisingと両方で同じルックバックウィンドウとアトリビューションモデルを使用することです。 [!DNL Analytics]. 必要に応じてAdobeアカウントチームと協力して、現在の設定を特定し、設定を同期させます。

これらの同じ概念は、異なるルックバックウィンドウまたはアトリビューションモデルを使用する、他の類似チャネルに適用されます。

#### ビュースルートラッキング用の異なるルックバックウィンドウ {#impression-lookback}

Adobe Advertisingでは、アトリビューションはクリック数とインプレッション数に基づいており、クリック数とインプレッション数に異なるルックバックウィンドウを設定できます。 対象： [!DNL Analytics]ただし、アトリビューションはクリックスルーとビュースルーに基づいているので、クリックスルーとビュースルーに異なるアトリビューションウィンドウを設定するオプションはありません。それぞれのトラッキングは、最初のサイト訪問の際に開始されます。 インプレッションは、ビュースルーが発生する同じ日または数日前に発生する可能性があり、これは、各システムのアトリビューションウィンドウの開始位置に影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分は、両方のシステムがクレジットを属性にするのに十分な速さで発生します。 ただし、一部のコンバージョンは、Adobe Advertisingインプレッションのルックバックウィンドウ以外で、 [!DNL Analytics] ルックバックウィンドウ。このようなコンバージョンはでのビュースルーに関連付けられます。 [!DNL Analytics] しかし、Adobe Advertisingの印象にはありません。

次の例では、訪問者が 1 日目に広告を受け取り、2 日目にビュースルー訪問（つまり、以前に広告をクリックせずに広告のランディングページを訪問）を実行し、45 日目にコンバージョンを行ったとします。 この場合、Adobe Advertisingは 1～14 日目からユーザーを追跡します（14 日間のルックバックを使用）。 [!DNL Analytics] は、2～61 日目からユーザーを（60 日間のルックバックを使用して）追跡し、45 日目のコンバージョンは内の広告に関連付けられます [!DNL Analytics] ただし、Adobe Advertising内ではありません。

![で起因するビュースルーコンバージョンの例 [!DNL Analytics] ただし、Adobe Advertisingではありません](/help/integrations/assets/a4adc-viewthrough-example.png)

その他の不一致の原因として、Adobe Advertisingでは、ビュースルーコンバージョンをカスタムに割り当てることができることがあります *ビュースルーの重み付け* これは、クリックベースのコンバージョンに起因する重み付けに対する相対的な関係です。 デフォルトのビュースルーの重み付けは 40% です。つまり、ビュースルーのコンバージョンは、クリックベースのコンバージョンの値の 40% としてカウントされます。 [!DNL Analytics] ビュースルーコンバージョンのそのような重み付けを提供しません。 例えば、100 米ドルの売上高の注文は次の場所でキャプチャされます。 [!DNL Analytics] デフォルトのビュースルーの重み付けを使用している場合、のAdobe Advertisingでは 40 USD に割引されます。この差は 60 USD です。

Adobe Advertisingとの間のビュースルーコンバージョンを比較する際は、次の違いを考慮してください [!DNL Analytics] レポート。

#### 使用可能なアトリビューションモデル

| Adobe Advertising属性 | [!DNL Analytics] 帰属 | [!DNL eVar]/[!DNL rVar] 配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 該当なし | 該当なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>使用不可* |
| [!UICONTROL Weight Last Event More] | 該当なし | 該当なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 該当なし |
| 該当なし | [!UICONTROL J-Shaped] | 該当なし |
| 該当なし | [!UICONTROL Inverse-J] | 該当なし |
| 該当なし | [!UICONTROL Custom] | 該当なし |
| 該当なし | [!UICONTROL Participation] | 該当なし |
| 該当なし | [!UICONTROL Algorithmic] | 該当なし |

>[!NOTE]
>
>線形配分の場合、 [!DNL Analytics] 成功イベントをすべてに均等に関連付ける [!DNL eVar] 1 回の訪問内の値なので、 [!DNL eVar] 「訪問」の有効期限。 ただし、広告では、線形アトリビューションを使用すると、真に線形ではない配分や、理想的でないレポートにつながる。 例えば、訪問者が 3 つの個別の訪問でコンバージョンを行う前に 3 つの広告を操作した場合、3 つの広告すべてではなく、最後の訪問で表示された広告のみがコンバージョンに関連付けられます。
>
>また、コンバージョン配分を「線形」と切り替えると、履歴データが表示されなくなり、レポートに誤ったデータが表示される可能性があります。 例えば、線形配分では、売上高をいくつかの異なる数に分割する場合があります [!DNL eVar] 値。 配分を「最新」に変更すると、その売上高の 100% が最新の単一の値に関連付けられます。 この関連付けにより、誤った結論が導かれる可能性があります。
>
>混乱を防ぐため、 [!DNL Analytics] レポートインターフェイスで履歴データを使用できないようにします。 を変更すると、履歴データを表示できます [!DNL eVar] 変更はできませんが、初期配分設定に戻ります [!DNL eVar] 配分の設定は、履歴データにアクセスするためのものです。 Adobeでは、新しいを使用することをお勧めします [!DNL eVar] の配分設定を変更するのではなく、既に記録されているデータに新しい配分設定を適用したい場合 [!DNL eVar] それはすでに相当量の履歴データを持っています。

のリストを参照 [!DNL Analytics] アトリビューションモデルとその定義： [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

にログインしている場合 [!DNL Search, Social, & Commerce]リストが表示されます。

* （北米のユーザー） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （他のすべてのユーザー） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertisingでのイベント日付の属性

Adobe Advertisingとして、コンバージョンデータは、関連するクリック日/イベント日（クリックまたはインプレッションイベントの日付）または取引日（コンバージョン日）のいずれかでレポートできます。 クリック/イベント日付レポートの概念は、に存在しません [!DNL Analytics]。で追跡されたすべてのコンバージョン [!DNL Analytics] トランザクション日別にレポートされます。 その結果、同じコンバージョンが、Adobe Advertisingが異なる日付でレポートされる場合や、 [!DNL Analytics]. 例えば、1 月 1 日に広告をクリックし、1 月 5 日にコンバージョンを行ったユーザーについて考えます。 コンバージョンデータをイベント日別にAdobe Advertisingで表示している場合は、クリックが発生した 1 月 1 日にコンバージョンがレポートされます。 対象： [!DNL Analytics]、1 月 5 日も同じコンバージョンが報告されています。

![異なる日付に起因するコンバージョンの例](/help/integrations/assets/a4adc-conversions-based-on.png)

## アトリビューション : [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] レポート](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) では、ヒット情報の異なる側面に基づいて様々なマーケティングチャネルを識別するルールを設定できます。 Adobe Advertisingトラッキング対象チャネル（[!UICONTROL Display Click Through], [!UICONTROL Display View Through]、および [!UICONTROL Paid Search]）を次として [!DNL Marketing Channels] を使用する `ef_id` チャネルを識別するクエリ文字列パラメーター。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> しかし、にもかかわらず [!DNL Marketing Channels] レポートではAdobe Advertisingチャネルをトラッキングできます。データがAdobe Advertisingレポートと一致しない理由はいくつかあります。 詳しくは、次の節を参照してください。

>[!NOTE]
>
> 次の中心概念は、Adobe Advertisingでトラッキングされないキャンペーンを含む、あらゆるマルチチャネルトラッキングにも当てはまります（例：） [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 変数（「トラッキングコード」ディメンションまたは「」とも呼ばれます）[!DNL eVar] 0&quot;）とカスタム [!DNL eVar] トラッキング。

### で異なる可能性があるアトリビューションモデル [!DNL Marketing Channels]

Most [!DNL Marketing Channels] レポートは次の機能で設定されています [!UICONTROL Last Touch] 前回マーケティングチャネルが検出されたアトリビューションには、コンバージョン値の 100% が割り当てられます。 用の様々なアトリビューションモデルの使用 [!DNL Marketing Channels] レポートとAdobe Advertisingレポートは、アトリビューションコンバージョンで不一致が生じます。

### での潜在的に異なるルックバックウィンドウ [!DNL Marketing Channels]

のルックバックウィンドウ [!DNL Marketing Channels] はカスタマイズできます。 Adobe Advertising、クリックルックバックウィンドウは設定可能ですが、一般的に、固定の 60 日間のウィンドウもあります。 2 つの製品で異なるルックバックウィンドウを使用している場合は、データの不一致が発生する可能性があります。

### での異なるチャネルアトリビューション [!DNL Marketing Channels]

Adobe Advertisingレポートでは、Adobe Advertisingを通じてトラフィックされた有料メディアのみを取り込みます（有料検索： [!DNL Advertising Search, Social, & Commerce] 広告（および Advertising DSP広告用のディスプレイ）とは対照的に、 [!DNL Marketing Channels] レポートでは、すべてのデジタルチャネルをトラッキングできます。 そのため、コンバージョンが関連付けられるチャネルに不一致が生じる可能性があります。

例えば、有料検索チャネルと自然検索チャネルは共生関係にあることが多く、各チャネルが互いに支援し合っています。 この [!DNL Marketing Channels] レポートでは、自然検索を追跡しないため、Adobe Advertisingで追跡できない自然検索へのコンバージョンが一部あります。

また、ディスプレイ広告を表示し、有料検索広告をクリックし、メールメッセージ内をクリックして、30 USD の注文を行った顧客についても考えてみます。 たとえAdobe Advertisingで [!DNL Marketing Channels] どちらもラストタッチアトリビューションモデルを使用しますが、コンバージョンはそれぞれ異なる属性になります。 Adobe Advertisingはへのアクセス権を持っていません [!UICONTROL Email] チャネルを使用すると、コンバージョンの有料検索にクレジットが付与されます。 [!DNL Marketing Channels]ただし、には 3 つのチャネルすべてにアクセスできるので、クレジットが生まれます [!UICONTROL Email] 変換する。

![とAdobe Advertisingで異なるコンバージョンアトリビューションの例 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

指標が変化する理由の詳細については、「」を参照してください[チャネルデータがAdobe Advertisingによって異なる可能性がある理由 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).」と入力します。

## Adobe Analyticsにおけるデータの違い [!DNL Paid Search Detection]

この [レガシー [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) の機能 [!DNL Analytics] 企業に次の許可 [有料およびオーガニック検索トラフィックをトラッキングするルールの定義](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) （指定した検索エンジン用）。 この [!DNL Paid Search Detection] ルールでは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 この [!DNL Paid Search Detection] レポートは、大きなグループの一部です [検索方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) レポート。指定したイベント（買い物かごのチェックアウトなど）が発生するか、訪問が終了すると有効期限が切れます。

以下は、を作成するためのインターフェイスです。 [!DNL Paid Search Detection] ルールセット：

![で設定された有料検索検知ルールの例 [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

結果の [!DNL Paid Search Detection] レポートには次が含まれます [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]、および [!UICONTROL Natural Search Keywords] レポート。

のデータに関しては次の 2 つの制限事項があります [!DNL Paid Search Detection] レポート：

* この [!UICONTROL Paid Search Keywords] および [!UICONTROL Natural Search Keywords] レポートには、ユーザーが入札したキーワードではなく、参照 URL で識別される検索クエリが表示されます。 Adobe Advertisingと [!DNL Analytics] レポートには実際のキーワードが表示されるので、 [!DNL Paid Search Detection] キーワードレポート。

* いつ [!DNL Paid Search Detection] この機能は当初、元の検索クエリ（ユーザーが検索エンジンの検索バーに入力した文字列）が、参照 URL を介して広告主が利用しやすくなったためです。 現在、検索エンジンは検索クエリを大幅に難読化し、 [!DNL Paid Search Detection] ほとんどのクエリデータが「未指定」に該当するので、キーワードレポートの値は限られています。

  （を使用） [!DNL Analytics for Advertising]広告主は、で有料キーワードを引き続き追跡できます [!DNL Analytics]. 参照ドメインは、どの検索エンジンがトラフィックを駆動したかをエンジンに通知する。 広告主固有のアカウント情報は参照ドメインに関連付けられていないので、すべてのトラフィックが検索エンジンの下に表示されます。 同じ検索エンジンで複数のアカウントを持つ広告主は、Adobe Advertisingまたはを参照する必要があります [!DNL Analytics] アカウント固有のレポートのレポート。

### 設定する理由 [!DNL Paid Search Detection]?

この [!DNL Paid Search Detection] レポートを使用すると、内の自然検索トラフィックを [[!DNL Analytics Marketing Channels] 報告書](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 有料検索トラフィックと自然検索トラフィックを分離することは、自然検索がマーケティングエコシステム全体にもたらす価値を理解するための優れた方法です。

## のクリックスルーのデータ検証 [!DNL Analytics for Advertising] {#data-validation}

統合では、クリックスルーデータを検証して、サイト上のすべてのページがクリックスルーを適切にトラッキングしていることを確認する必要があります。

対象： [!DNL Analytics]、を検証する最も簡単な方法の 1 つ [!DNL Analytics for Advertising] トラッキングでは、「クリック数」を使用して、クリック数をインスタンスと比較します [!UICONTROL AMO ID Instances]計算指標」と表示されます。計算指標は次のように計算されます。

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] は、の回数を表します [AMO ID](ids.md) サイト上で追跡されます。 広告がクリックされるたびに、AMO ID （`s_kwcid`） パラメーターがランディングページの URL に追加されます。 次の数 [!UICONTROL AMO ID Instances]そのため、はクリック数に似ており、実際の広告クリックに対して検証できます。 通常、の一致率は 80% と表示されます。 [!DNL Search, Social, & Commerce] に対して 30% の一致率 [!DNL DSP] トラフィック（クリックスルーのみを含めるようにフィルタリングする場合） [!UICONTROL AMO ID Instances]）に設定します。 検索と表示の期待値の違いは、期待されるトラフィック動作によって説明できます。 検索は目的をキャプチャし、そのため、ユーザーは通常、クエリから検索結果をクリックしようとします。 ただし、ディスプレイやオンラインのビデオ広告を表示したユーザーが、意図せずに広告をクリックした後にサイトからバウンスしたり、ページアクティビティがトラッキングされる前に読み込まれる新しいウィンドウを放棄したりする可能性が高くなります。

Adobe Advertisingレポートでは、「」を使用して、クリックをインスタンスと同様に比較できます[!UICONTROL ef_id_instances]の代わりに「指標」 [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

AMO ID と EF ID の間の一致率は高いと想定すべきですが、AMO ID と EF ID は基本的に異なるデータを追跡するので、100% のパリティは期待しないでください。この違いにより、合計にわずかな違いが生じる可能性があります [!UICONTROL AMO ID Instances] および [!UICONTROL EF ID Instances]. 合計 [!UICONTROL AMO ID Instances] 。対象： [!DNL Analytics] ～と異なる [!UICONTROL EF ID Instances] ただし、Adobe Advertisingが 1% を超える場合は、Adobeアカウントチームにお問い合わせください。

AMO ID と EF ID について詳しくは、を参照してください。 [Analytics が使用するAdobe Advertising ID](ids.md).

以下は、インスタンスに対するクリックを追跡するワークスペースの例です。

![インスタンスへのクリックを追跡するワークスペースの例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## のデータセットの比較 [!DNL Analytics for Advertising] とAdobe Advertising内

この [AMO ID](ids.md) （s_kwcid クエリ文字列パラメーター）は、でレポートに使用されます [!DNL Analytics]、および [EF ID](ids.md) は、Adobe Advertisingでのレポートに使用されます。 これらは個別の値なので、ある値が破損しているか、ランディングページに追加されない可能性があります。

例えば、次のランディングページがあるとします。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

ここで、EF ID は&#39;&#39;`test_ef_id`」で、AMO ID は「」です`test_amo_id`.」と入力します。

サイトサイドのリダイレクトが発生した場合、URL は次のようになります。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

ここで、EF ID は&#39;&#39;`test_ef_id`」で、AMO ID は「」です`test_amo_id#redirectAnchorTag`.」と入力します。

この例では、アンカータグを追加すると、AMO ID に予期しない文字が追加され、その結果、Analytics で認識されない値が生じます。 この AMO ID は分類されず、関連付けられたコンバージョンは「」に該当します[!UICONTROL unspecified]「または」[!UICONTROL none]」に含まれます [!DNL Analytics] レポート。

幸いにも、このような問題は一般的ですが、通常は高い割合で不一致が生じることはありません。 ただし、の AMO ID 間に大きな不一致がある場合は、 [!DNL Analytics] Adobe Advertising中の EF ID については、Adobeアカウントチームにお問い合わせください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

類似しているように見えますが、クリック数と訪問数は異なるデータを表します。

* **クリック：** [!DNL DSP] または、検索エンジンが、訪問者が発行者の web サイト上の広告をクリックした際のクリックを記録します。

* **アクセス：** [!DNL Analytics] は、 [訪問](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) ユーザーによる一連のページビューとして、いくつかの条件（30 分間無操作状態など）のいずれかに従って終了します。

定義として、クリックは複数の訪問につながる可能性があります。

次の例を考えてみましょう。ユーザー 1 とユーザー 2 は両方とも、Adobe Advertising広告をクリックしてサイトにアクセスします。 ユーザー 1 は 4 ページを表示して、その日のうちに離れるので、最初のクリックは 1 回の訪問となります。 ユーザー 2 は 2 ページを表示し、45 分間の昼食に残して戻り、さらに 2 ページを表示してから離れます。この場合、最初のクリックで 2 回の訪問が発生します。

![クリック数と訪問数の違いの例](/help/integrations/assets/a4adc-visits-example.png)

### クリックとクリックスルーの違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、次の 2 つの異なる指標です。

* **クリック：** [!DNL DSP] または、検索エンジンが、訪問者が発行者の web サイト上の広告をクリックした際のクリックを記録します。

* **クリックスルー：** [!DNL Analytics] は、訪問者が宛先 web サイトにアクセスした際、ランディングページが読み込まれた際、および [!DNL Analytics] ページ下部にあるリクエストによって、データがに送信されます。 [!DNL Analytics].

誤った広告クリックが原因で、クリックとクリックスルーが大きく異なる場合があります。 ディスプレイ広告のほとんどのクリックは誤ってクリックされ、これらの誤った訪問者はランディングページが読み込まれる前に「戻る」ボタンを押します [!DNL Analytics] クリックスルーを記録できません。 これは、モバイル広告、ビデオ広告、画面いっぱいに表示され、ユーザーがページを表示する前に閉じる必要がある広告など、誤ってクリックする可能性が高い広告に特に当てはまります。

また、モバイルデバイスに読み込まれるサイトは、帯域幅や利用可能な処理能力が低いため、クリックスルーが発生する可能性が低く、ランディングページの読み込みに時間がかかります。 クリックの 50～70% がクリックスルーに至らないことは珍しくありません。 モバイル環境では、ブラウザーの速度が低下し、ユーザーがページ内をスクロールしたり広告を閉じようとしたりしているときに、誤って広告をクリックする可能性が高くなるので、90% も違いが生じる可能性があります。

クリックデータは、現在のトラッキングメカニズムではクリックスルーを記録できない環境（モバイルアプリに着信する、またはモバイルアプリから発信するクリックなど）や、広告主が 1 つのトラッキングアプローチのみをデプロイした環境（例えば、ビュースルー JavaScript アプローチでは、サードパーティ cookie をブロックするブラウザーはクリックを追跡しますが、クリックスルーは追跡しません）にも記録される場合があります。 Adobe クリック URL トラッキングとビュースルー JavaScript トラッキングの両方のアプローチをデプロイすることをお勧めする主な理由は、トラッキング可能なクリックスルーの範囲を最大限に広げることです。

### 非Adobe AdvertisingDimensionに対するAdobe Advertisingトラフィック指標の使用

Adobe Advertisingは Analytics に次を提供します [広告固有のトラフィック指標と関連するディメンション [!DNL DSP] および [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Adobe Advertising提供の指標は指定されたAdobe Advertisingディメンションにのみ適用され、データはの他のディメンションでは使用できません [!DNL Analytics].

例えば、 [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] Adobe Advertisingディメンションであるアカウント別指標に合計が表示されます [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] アカウント別。

![Adobe Advertisingディメンションを使用したレポートのAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、を表示した場合は、 [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] オンページディメンション（ページなど）別の指標で、Adobe Advertisingがデータを提供しない場合、次に [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] 各ページの値はゼロ（0）になります。

![サポートされていないディメンションを使用したレポートのAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] as a 非Adobe AdvertisingDimensionでのクリックの代用

使用できないので [!UICONTROL AMO Clicks] オンサイトディメンションでは、クリックに相当するを見つけたい場合があります。 訪問回数を代用として使用したくなるかもしれませんが、各訪問者が複数の訪問回数を持つ可能性があるので、これらは最適な選択肢ではありません。 （「」を参照）[クリック数と訪問数の違い](#clicks-vs-visits).」と入力します。 代わりに、を使用することをお勧めします [!UICONTROL AMO ID Instances]、AMO ID がキャプチャされた回数です。 While [!UICONTROL AMO ID Instances] 一致しない [!UICONTROL AMO Clicks] 正確には、サイト上のクリックトラフィックを測定するための最適なオプションです。 詳しくは、「」を参照してください[のクリックスルーのデータ検証 [!DNL Analytics for Advertising]](#data-validation).」と入力します。

![例 [!UICONTROL AMO ID Instances] の代わりに [!UICONTROL Adobe Advertising Clicks] サポートされていないディメンションの場合](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概要 [!DNL Analytics for Advertising]](overview.md)
>* [が使用するAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising内のデータ](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Adobe Advertisingと環境でデータが異なる可能性がある理由 [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
