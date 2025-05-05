---
title: とAdobe Advertisingの間で予期されるデータ  [!DNL Analytics]  相違
description: とAdobe Advertisingの間で予期されるデータ  [!DNL Analytics]  相違
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: 6470ed471c60477bf19cf9b125f0250136f31511
workflow-type: tm+mt
source-wordcount: '3358'
ht-degree: 0%

---

# [!DNL Analytics] とAdobe Advertisingの間で予期されるデータの相違

*Adobe AdvertisingとAdobe Analyticsの統合のみを行う広告主*

[!DNL Analytics for Advertising] <!-- (A4AdC) --> の統合を利用する広告主は、Adobe AdvertisingとAdobe Analyticsを通じて有料広告をトラッキングします。 複数のシステムを使用してメディア、キャンペーン、チャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Adobe Advertisingを通じてトラフィックが発生したメディアのデータを、[!DNL Analytics] 内でメディアがトラッキングされる様々なシステムのデータと比較する方法について説明します。

>[!NOTE]
>
>このドキュメントでは、Adobe Advertisingと分析に重点を置いていますが、重要な点の多くは、他のトラッキングソリューションにも転送できます。

## 類似レポートにおけるアトリビューションの違い

### 潜在的に異なるルックバックウィンドウとアトリビューションモデル

[!DNL Analytics for Advertising] の統合では、2 つの変数（[!DNL eVars] または [!DNL rVars] \[reserved [!DNL eVars]]\）を使用して [EF ID と AMO ID](ids.md) をキャプチャします。 これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーが関連付けられる期間）とアトリビューションモデルを使用して設定されます。 特に指定がない限り、変数は、Adobe Advertisingのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、（[!DNL eVars] を介して） Analytics とAdobe Advertisingの両方で設定できます。 さらに、Adobe Advertisingすると、アトリビューションモデルは、広告主レベル（入札最適化の場合）だけでなく、個々のデータビューおよびレポート（レポート目的の場合のみ）でも設定できます。 例えば、ある組織が最適化のために偶数分布アトリビューションモデルを使用し、Advertising DSPまたは [!DNL Advertising Search, Social, & Commerce] のレポートにはラストタッチアトリビューションを使用する場合があります。 アトリビューションモデルを変更すると、アトリビューションコンバージョンの数が変更されます。

レポートルックバックウィンドウまたはアトリビューションモデルが一方の製品で変更され、もう一方の製品では変更されていない場合、各システムの同じレポートに異なるデータが表示されます。

* **様々なルックバックウィンドウによって発生する不一致の例：**

  Adobe Advertisingに 60 日間のクリックのルックバックウィンドウがあり、[!DNL Analytics] に 30 日間のルックバックウィンドウがあるとします。 あるユーザーが、Adobe Advertisingが追跡した広告を通じてサイトを訪問し、離脱した後、45 日目に戻り、コンバージョンを行ったとします。 Adobe Advertisingでは、コンバージョンが 60 日間のルックバックウィンドウ内で発生したため、最初の訪問へのコンバージョンが属性化されます。 [!DNL Analytics] だし、は、30 日のルックバックウィンドウの有効期限が切れた後にコンバージョンが発生したので、コンバージョンを最初の訪問に関連付けることはできません。 この例では、Adobe Advertisingでレポートされるコンバージョンの数が [!DNL Analytics] よりも多くなっています。

  ![Adobe Advertisingで属性が設定されているが [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png) が設定されていないコンバージョンの例

* **異なるアトリビューションモデルによって発生する不一致の例：**

  ユーザーがコンバージョンする前に、売上高をコンバージョンタイプとして、3 つの異なるAdobe Advertising広告を操作したとします。 Adobe Advertisingレポートでアトリビューションに偶数配分モデルを使用する場合、売上高はすべての広告に均等に関連付けられます。 ただし、ラストタッチ アトリビューションモデルを使用する [!DNL Analytics] 合は、売上高は最後の広告に関連付けられます。 次の例では、Adobe Advertisingが 3 つの広告のそれぞれに取り込んだ 30 USD の売上高のうち 10 USD でもアトリビューションするのに対して、[!DNL Analytics] では、ユーザーが最後に閲覧した広告に 30 USD の売上高をすべて関連付けています。 Adobe Advertisingと [!DNL Analytics] のレポートを比較すると、アトリビューションの違いの影響を確認できます。

  ![ 異なるアトリビューションモデルに基づくAdobe Advertisingと [!DNL Analytics] に起因する異なる売上高 ](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>ベストプラクティスは、Adobe Advertisingと [!DNL Analytics] の両方で同じルックバックウィンドウとアトリビューションモデルを使用することです。 必要に応じてAdobeアカウントチームと協力して、現在の設定を特定し、設定を同期させます。

これらの同じ概念は、異なるルックバックウィンドウまたはアトリビューションモデルを使用する、他の類似チャネルに適用されます。

#### ビュースルートラッキング用の異なるルックバックウィンドウ {#impression-lookback}

Adobe Advertisingでは、アトリビューションはクリック数とインプレッション数に基づいており、クリック数とインプレッション数に異なるルックバックウィンドウを設定できます。 ただし、[!DNL Analytics] ではアトリビューションはクリックスルーとビュースルーに基づいているので、クリックスルーとビュースルーに異なるアトリビューションウィンドウを設定するオプションはありません。それぞれのアトリビューションのトラッキングは、最初のサイト訪問の際に開始されます。 インプレッションは、ビュースルーが発生する同じ日または数日前に発生する可能性があり、タイミングは、各システムのアトリビューションウィンドウの開始位置に影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分は、両方のシステムがクレジットを属性にするのに十分な速さで発生します。 ただし、一部のコンバージョンは、Adobe Advertisingインプレッションのルックバックウィンドウ外で、[!DNL Analytics] のルックバックウィンドウ内で発生する場合があります。このようなコンバージョンは、[!DNL Analytics] のビュースルーに関連付けられますが、Adobe Advertisingのインプレッションには関連付けられません。

次の例では、訪問者に 1 日目に広告が配信され、2 日目にビュースルー訪問（つまり、以前に広告をクリックせずに広告のランディングページを訪問）を実行し、45 日目にコンバージョンが行われたとします。 この場合、Adobe Advertisingは（14 日間のルックバックを使用して） 1 日目から 14 日目までユーザーを追跡 [!DNL Analytics]、2 日目から 61 日目まで（60 日間のルックバックを使用）を追跡し、45 日目のコンバージョンはAdobe Advertising内ではなく [!DNL Analytics] 日以内の広告に関連付けられます。

![Adobe Advertisingではなく [!DNL Analytics] に起因するビュースルーコンバージョンの例 ](/help/integrations/assets/a4adc-viewthrough-example.png)

その他の不一致の原因として、Adobe Advertisingでは、ビュースルーコンバージョンに、クリックベースのコンバージョンに起因する重み付けを基準としたカスタム *ビュースルーの重み付け* を割り当てることができることがあります。 デフォルトのビュースルーの重み付けは 40% です。つまり、ビュースルーのコンバージョンは、クリックベースのコンバージョンの値の 40% としてカウントされます。 [!DNL Analytics] では、ビュースルーコンバージョンのそのような重み付けは提供していません。 例えば、[!DNL Analytics] で取得した 100 USD の売上高の注文に対して、デフォルトのビュースルー重み付けを使用している場合、Adobe Advertisingとして 40 USD が割り引かれます。この差は 60 USD です。

Adobe Advertisingレポートと [!DNL Analytics] レポートレポートのビュースルーコンバージョンを比較する際は、次の違いを考慮してください。

#### 使用可能なアトリビューションモデル

| Adobe Advertising属性 | [!DNL Analytics] Attribution | [!DNL eVar]/[!DNL rVar] 配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 該当なし | 該当なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br> 使用不可* |
| [!UICONTROL Weight Last Event More] | 該当なし | 該当なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 該当なし |
| 該当なし | [!UICONTROL J-Shaped] | 該当なし |
| 該当なし | [!UICONTROL Inverse-J] | 該当なし |
| 該当なし | [!UICONTROL Custom] | 該当なし |
| 該当なし | [!UICONTROL Participation] | 該当なし |
| 該当なし | [!UICONTROL Algorithmic] | 該当なし |

>[!NOTE]
>
>線形配分の場合、[!DNL Analytics] は 1 回の訪問ですべての [!DNL eVar] 値にわたって成功イベントを等しく属性するので、「訪問」の有効期限が [!DNL eVar] い線形配分を使用します。 ただし、広告では、線形アトリビューションを使用すると、真に線形ではない配分や、理想的でないレポートにつながる。 例えば、訪問者が 3 つの個別の訪問でコンバージョンを行う前に 3 つの広告を操作した場合、3 つの広告すべてではなく、最後の訪問で表示された広告のみがコンバージョンに関連付けられます。
>
>また、コンバージョン配分を「線形」と切り替えると、履歴データが表示されなくなり、レポートに誤ったデータが表示される可能性があります。 例えば、線形配分では、売上高を様々な [!DNL eVar] 値に分割する場合があります。 配分を「最新」に変更すると、その売上高の 100% が最新の単一の値に関連付けられます。 この関連付けにより、誤った結論が導かれる可能性があります。
>
>混乱を防ぐため、[!DNL Analytics] では、レポートインターフェイスで履歴データを使用できないようにしています。 [!DNL eVar] ータを初期配分設定に戻すと、履歴データを表示できますが、履歴データにアクセスするためだけに配分設定 [!DNL eVar] 変更しないでください。 Adobeでは、大量の履歴データが既にある [!DNL eVar] ータの配分設定を変更するのではなく、既に記録されているデータに新しい配分設定を適用する場合に新しい [!DNL eVar] を使用することをお勧めします。

[!DNL Analytics] アトリビューションモデルとその定義のリストについては、[https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/attribution/models) を参照してください。

[!DNL Search, Social, & Commerce] にログインしている場合は、次のリストを見つけることができます

* （北米のユーザー） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （その他すべてのユーザー） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertisingでのイベント日付の属性

Adobe Advertisingとして、コンバージョンデータは、関連するクリック日/イベント日（クリックまたはインプレッションイベントの日付）または取引日（コンバージョン日）のいずれかでレポートできます。 クリック/イベント日レポートの概念は [!DNL Analytics] には存在しません。[!DNL Analytics] で追跡されるすべてのコンバージョンは、トランザクションの日付ごとにレポートされます。 その結果、同じコンバージョンが、Adobe Advertisingと [!DNL Analytics] で異なる日付でレポートされる場合があります。 例えば、1 月 1 日に広告をクリックし、1 月 5 日にコンバージョンを行ったユーザーについて考えます。 コンバージョンデータをイベント日別にAdobe Advertisingで表示している場合は、クリックが発生した 1 月 1 日にコンバージョンがレポートされます。 [!DNL Analytics] 年 1 月 5 日も同じコンバージョンが報告されています。

![ 異なる日付に起因するコンバージョンの例 ](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels] のアトリビューション

[[!DNL Analytics Marketing Channels]  レポート ](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=ja) を使用すると、ヒット情報の異なる側面に基づいて様々なマーケティングチャネルを識別するルールを設定できます。 `ef_id` のクエリ文字列パラメーターを使用してチャンネルを特定することで、Adobe Advertisingがトラッキングするチャンネル（[!UICONTROL Display Click Through]、[!UICONTROL Display View Through]、[!UICONTROL Paid Search]）を [!DNL Marketing Channels] のようにトラッキングできます。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> ただし、[!DNL Marketing Channels] レポートではAdobe Advertisingチャネルをトラッキングできますが、いくつかの理由で、データがAdobe Advertisingレポートと一致しない場合があります。 詳しくは、次の節を参照してください。

>[!NOTE]
>
> 次の中心概念は、[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=ja) 変数（「トラッキングコード」ディメンションまたは「[!DNL eVar] 0」とも呼ばれます）やカスタムトラッ [!DNL eVar] ングなど、Adobe Advertisingでトラッキングされないキャンペーンを含むマルチチャネルトラッキングにも当てはまります。

### [!DNL Marketing Channels] で異なる可能性があるアトリビューションモデル

ほとんどの [!DNL Marketing Channels] レポートには、[!UICONTROL Last Touch] のアトリビューションが設定されており、このアトリビューションについて、最後に検出されたマーケティングチャネルには、コンバージョン値の 100% が割り当てられます。 アトリビューションレポートとAdobe Advertisingレポートに異なるアトリビューションモデルを使用すると、[!DNL Marketing Channels] トリビューションコンバージョンに不一致が生じます。

### [!DNL Marketing Channels] での潜在的に異なるルックバックウィンドウ

[!DNL Marketing Channels] のルックバックウィンドウはカスタマイズできます。 Adobe Advertising、クリックルックバックウィンドウは設定可能ですが、一般的に、固定の 60 日間のウィンドウもあります。 2 つの製品で異なるルックバックウィンドウを使用している場合は、データの不一致が発生する可能性があります。

### [!DNL Marketing Channels] で異なるチャネルアトリビューション

Adobe Advertisingレポートは、Adobe Advertising（[!DNL Advertising Search, Social, & Commerce] 広告の有料検索、Advertising DSP広告の表示）を通じてトラフィックに送信された有料メディアのみを取り込みますが、[!DNL Marketing Channels] のレポートはすべてのデジタルチャネルをトラッキングできます。 そのため、コンバージョンが関連付けられるチャネルに不一致が生じる可能性があります。

例えば、有料検索チャネルと自然検索チャネルは共生関係にあることが多く、各チャネルが互いに支援し合っています。 [!DNL Marketing Channels] レポートでは、一部のコンバージョンは自然検索を追跡しないため、Adobe Advertisingで追跡できない自然検索に関連付けられます。

また、ディスプレイ広告を表示し、有料検索広告をクリックし、メールメッセージ内をクリックして、30 USD の注文を行った顧客についても考えてみます。 Adobe Advertisingと [!DNL Marketing Channels] の両方でラストタッチアトリビューションモデルが使用されている場合でも、コンバージョンのアトリビューションは各アトリビューションとは異なる属性になります。 Adobe Advertisingは [!UICONTROL Email] チャネルにアクセスできないので、コンバージョンの有料検索にクレジットが与えられます。 ただし、[!DNL Marketing Channels] は 3 つのチャネルすべてにアクセスできるので、コンバージョンに対するクレジットは [!UICONTROL Email] になります。

![Adobe Advertisingと [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png) で異なるコンバージョンアトリビューションの例

指標が変化する理由の詳細については、「Adobe Advertisingとでチャネルデータが変化する理由 [ を参照してくだ  [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md) い。

## Adobe Analytics [!DNL Paid Search Detection] におけるデータの違い

[!DNL Analytics] の [ レガシー  [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=ja) 機能を使用すると、企業は指定した検索エンジンの [ 有料検索トラフィックとオーガニック検索トラフィックを追跡するルールを定義 ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=ja) できます。 [!DNL Paid Search Detection] ルールでは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 [!DNL Paid Search Detection] レポートは、多数の [ 検索方法 ](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=ja) レポートの一部であり、指定したイベント（買い物かごのチェックアウトなど）が発生するか、訪問が終了すると有効期限が切れます。

[!DNL Paid Search Detection] しいルールセットを作成するためのインターフェイスを次に示します。

![[!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png) の有料検索検知ルールセットの例

結果として生成される [!DNL Paid Search Detection] レポートには、[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]、[!UICONTROL Natural Search Keywords] の各レポートが含まれます。

レポート内のデータに関しては、次の 2 つの制限事項 [!DNL Paid Search Detection] 注意してください。

* [!UICONTROL Paid Search Keywords] および [!UICONTROL Natural Search Keywords] レポートには、ユーザーが入札したキーワードではなく、参照 URL で識別される検索クエリが表示されます。 Adobe Advertisingレポートと [!DNL Analytics] レポートには実際のキーワードが表示されるので、[!DNL Paid Search Detection] キーワードレポートと一致するとは限りません。

* [!DNL Paid Search Detection] 機能を最初に作成したとき、元の検索クエリ（ユーザーが検索エンジンの検索バーに入力した文字列）は、参照 URL を介して広告主がより簡単に使用できるようになりました。 現在、検索エンジンは検索クエリを大部分が難読化しており、ほとんどのクエリデータが「未指定」に該当するので、[!DNL Paid Search Detection] キーワードレポートの価値は限られています。

  [!DNL Analytics for Advertising] を使用すると、広告主は [!DNL Analytics] で有料キーワードを引き続き追跡できます。 参照ドメインは、どの検索エンジンがトラフィックを駆動したかをエンジンに通知する。 広告主固有のアカウント情報は参照ドメインに関連付けられていないので、すべてのトラフィックが検索エンジンの下に表示されます。 同じ検索エンジンで複数のアカウントを持つ広告主は、アカウント固有のレポートについて、Adobe Advertisingまたは [!DNL Analytics] レポートを参照する必要があります。

### [!DNL Paid Search Detection] を設定する理由

[!DNL Paid Search Detection] レポートを使用すると、[[!DNL Analytics Marketing Channels] reports](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=ja) 内の自然な検索トラフィックを識別できます。 有料検索トラフィックと自然検索トラフィックを分離することは、自然検索がマーケティングエコシステム全体にもたらす価値を理解するための優れた方法です。

## [!DNL Analytics for Advertising] のクリックスルーのデータ検証 {#data-validation}

統合では、クリックスルーデータを検証して、サイト上のすべてのページがクリックスルーを適切にトラッキングしていることを確認する必要があります。

ま [!DNL Analytics]、[!DNL Analytics for Advertising] トラッキングを検証する最も簡単な方法の 1 つは、「AMO ID インスタンスとクリック数」の計算指標を使用してインスタンスとクリック数を比較することです。計算指標は、次のように計算されます。

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances] は、サイトで [AMO ID](ids.md) がトラッキングされた回数を表します。 広告がクリックされるたびに、AMO ID （`s_kwcid`）パラメーターがランディングページの URL に追加されます。 そのため、[!UICONTROL AMO ID Instances] の数はクリック数と類似しており、実際の広告クリック数に対して検証できます。 通常、[!DNL Search, Social, & Commerce] の一致率は 85%、[!DNL DSP] トラフィックの一致率は 30% です（クリックスルー [!UICONTROL AMO ID Instances] のみを含めるようにフィルタリングした場合）。 検索と表示の期待値の違いは、期待されるトラフィック動作によって説明できます。 検索は目的をキャプチャし、そのため、ユーザーは通常、クエリから検索結果をクリックしようとします。 ただし、ディスプレイやオンラインのビデオ広告を表示したユーザーが、意図せずに広告をクリックした後にサイトからバウンスしたり、ページアクティビティがトラッキングされる前に読み込まれる新しいウィンドウを放棄したりする可能性が高くなります。

Adobe Advertisingレポートでは、[!UICONTROL AMO ID Instances] の代わりに「[!UICONTROL EF ID Instances]」指標を使用して、インスタンスをクリックと同様に比較できます。

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

AMO ID と EF ID の間の一致率は高いものと思われますが、AMO ID と EF ID は基本的に異なるデータを追跡するので、100% のパリティは期待しないでください。この違いにより、[!UICONTROL AMO ID Instances] と [!UICONTROL EF ID Instances] の合計にわずかな違いが生じる可能性があります。 ただし、[!DNL Analytics] の合計 [!UICONTROL AMO ID Instances] がAdobe Advertisingの [!UICONTROL EF ID Instances] と 1% 以上異なる場合は、Adobeアカウントチームにお問い合わせください。

AMO ID および EF ID について詳しくは、[Analytics で使用されるAdobe Advertising ID](ids.md) を参照してください。

<!--  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### クリックとインスタンス間の不一致のトラブルシューティング

クリック [!UICONTROL EF ID Instances] 率が 85% を下回る場合は、次の点を確認してください。

* アカウントまたは任意のサブレベルのクリック追跡が欠落していないか、重複しているクリック追跡はありますか（例えば、アカウントレベルとキャンペーンレベルの両方で）?

  検索、ソーシャル、Commerceで、アカウントの [ バルクシートをダウンロード ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md) してトラッキング URL を確認します。

  また、[!DNL Analytics] では、次のように計算される「[!DNL AMO ID] to [!DNL EF ID]」計算指標を使用して、AMO ID と EF IF が一貫して追加されているかどうかを確認できます。

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  100% を超える値は、欠落している EF ID が AMO ID よりも多いことを示します。

* ランディングページに読み込みの問題があるので、AMO ID と EF ID は取り込まれていませんか？

* ランディングページ URL は、AMO ID と EF ID が失われるようにリダイレクトされますか？

* 設定済みのレポートスイートは、すべてのランディングページで使用されますか？

>[!NOTE]
>
>理論上、1 つのインスタンスが複数のクリックを持つ可能性があります。 様々なデバイス（デスクトップ、モバイル、タブレットなど）でのクリックを確認します。

## [!DNL Analytics for Advertising] でのデータセットとAdobe Advertisingでのデータセットの比較

[AMO ID](ids.md) （s_kwcid クエリ文字列パラメーター）は [!DNL Analytics] でのレポートに、[EF ID](ids.md) （ef_id クエリ文字列パラメーター）はAdobe Advertisingでのレポートに使用されます。 これらは個別の値なので、ある値が破損しているか、ランディングページに追加されない可能性があります。

例えば、次のランディングページがあるとします。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

ここで、EF ID は「`test_ef_id`」、AMO ID は「`test_amo_id`」です。

サイトサイドのリダイレクトが発生した場合、URL は次のようになります。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

ここで、EF ID は「`test_ef_id`」、AMO ID は「`test_amo_id#redirectAnchorTag`」です。

この例では、アンカータグを追加すると、AMO ID に予期しない文字が追加され、その結果、Analytics で認識されない値が生じます。 この AMO ID は分類されず、それに関連付けられたコンバージョンは [!DNL Analytics] レポートの「[!UICONTROL unspecified]」または「[!UICONTROL none]」に該当します。

幸いにも、このような問題は一般的ですが、通常は高い割合で不一致が生じることはありません。 ただし、[!DNL Analytics] の AMO ID とAdobe Advertisingの EF ID の間に大きな不一致に気付いた場合は、Adobeアカウントチームにお問い合わせください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

類似しているように見えますが、クリック数と訪問数は異なるデータを表します。

* **クリック：** [!DNL DSP] または検索エンジンは、訪問者がパブリッシャーの web サイト上の広告をクリックした際のクリックを記録します。

* **訪問：** [!DNL Analytics] は、ユーザーによる一連のページビューとして [ 訪問 ](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=ja) を定義し、30 分間無操作状態など、いくつかの条件のいずれかに従って終了します。

定義として、クリックは複数の訪問につながる可能性があります。

次の例を考えてみましょう。ユーザー 1 とユーザー 2 は両方とも、Adobe Advertising広告をクリックしてサイトにアクセスします。 ユーザー 1 は 4 ページを表示して、その日のうちに離れるので、最初のクリックは 1 回の訪問となります。 ユーザー 2 は 2 ページを表示し、45 分間の昼食に残して戻り、さらに 2 ページを表示してから離れます。この場合、最初のクリックで 2 回の訪問が発生します。

![ クリック数と訪問数の違いの例 ](/help/integrations/assets/a4adc-visits-example.png)

### クリックとクリックスルーの違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、次の 2 つの異なる指標です。

* **クリック：** [!DNL DSP] または検索エンジンは、訪問者がパブリッシャーの web サイト上の広告をクリックした際のクリックを記録します。

* **クリックスルー：** [!DNL Analytics] は、訪問者が宛先の web サイトにアクセスした際のクリックスルーを記録します。ランディングページが読み込まれ、ページ下部の [!DNL Analytics] リクエストによってデータが [!DNL Analytics] に送信されます。

誤った広告クリックが原因で、クリックとクリックスルーが大きく異なる場合があります。 ディスプレイ広告のほとんどのクリックは偶然のクリックであり、これらの偶然の訪問者はランディングページが読み込まれる前に「戻る」ボタンを押 [!DNL Analytics] ので、クリックスルーを記録できません。 これは、モバイル広告、ビデオ広告、画面いっぱいに表示され、ユーザーがページを表示する前に閉じる必要がある広告など、誤ってクリックする可能性が高い広告に特に当てはまります。

また、モバイルデバイスに読み込まれるサイトは、帯域幅や利用可能な処理能力が低いため、クリックスルーが発生する可能性が低く、ランディングページの読み込みに時間がかかります。 クリックの 50～70% がクリックスルーに至らないことは珍しくありません。 モバイル環境では、ブラウザーの速度が低下し、ユーザーがページ内をスクロールしたり広告を閉じようとしたりしているときに、誤って広告をクリックする可能性が高くなるので、90% も違いが生じる可能性があります。

また、クリックデータは、現在のトラッキングメカニズムでのクリックスルーを記録できない環境（モバイルアプリに着信するクリックや、モバイルアプリからのクリックなど）や、広告主が 1 つのトラッキングアプローチのみをデプロイした環境（例えば、ビュースルーJavaScript アプローチでは、サードパーティ cookie がクリックを追跡するが、クリックスルーは追跡しないブラウザー）に記録される場合もあります。 Adobeがクリック URL トラッキングとビュースルーJavaScript トラッキングアプローチの両方をデプロイすることをお勧めする主な理由は、トラッキング可能なクリックスルーの範囲を最大限に広げることです。

### 非Adobe AdvertisingDimensionに対するAdobe Advertisingトラフィック指標の使用

Adobe Advertisingは、Analytics に [ 広告固有のトラフィック指標と、からの関連ディメンション  [!DNL DSP]  および  [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md) を提供します。 Adobe Advertisingが提供する指標は、指定されたAdobe Advertisingディメンションにのみ適用され、[!DNL Analytics] の他のディメンションではデータを使用できません。

例えば、[!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] 指標を勘定科目別に表示した場合（Adobe Advertising次元）、[!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] の合計が勘定科目別に表示されます。

![Adobe Advertisingディメンションを使用したレポートのAdobe Advertising指標の例 ](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、Adobe Advertisingがデータを提供しないオンページディメンション（ページなど）で [!UICONTROL Adobe Advertising Clicks] と [!UICONTROL Adobe Advertising Cost] の指標を表示した場合、各ページの [!UICONTROL Adobe Advertising Clicks] と [!UICONTROL Adobe Advertising Cost] はゼロ（0）になります。

![ サポートされていないディメンションを使用したレポートのAdobe Advertising指標の例 ](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Adobe Advertising以外のDimensionを使用したクリックの代用としての [!UICONTROL AMO ID Instances] の使用

オンサイトディメンションでは [!UICONTROL AMO Clicks] を使用できないので、クリックに相当するを見つける必要がある場合があります。 訪問回数を代用として使用したくなるかもしれませんが、各訪問者が複数の訪問回数を持つ可能性があるので、これらは最適な選択肢ではありません。 （「クリック数と訪問数の違い [ を参照し ](#clicks-vs-visits) ください。 代わりに、[!UICONTROL AMO ID Instances] を使用することをお勧めします。これは、AMO ID がキャプチャされた回数です。 [!UICONTROL AMO ID Instances] は完全には一致しませんが、サイト上のクリックトラフィックを測定する [!UICONTROL AMO Clicks] めの最適なオプションです。 詳しくは、「[ のクリックスルー・データ検証  [!DNL Analytics for Advertising]](#data-validation) を参照してください。

![ サポートされていないディメンションに対する、[!UICONTROL Adobe Advertising Clicks] ではなく [!UICONTROL AMO ID Instances] の例 ](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [ 使用Adobe AdvertisingID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis WorkspaceのAdobe Advertising指標 ](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] Adobe Advertising内データ ](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Adobe Advertisingによってデータが異なる可能性がある理由  [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
