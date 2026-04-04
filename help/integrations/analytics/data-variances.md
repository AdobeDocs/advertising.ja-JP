---
title: ' [!DNL Analytics] とAdobe Advertisingの間の予想されるデータの差異'
description: ' [!DNL Analytics] とAdobe Advertisingの間の予想されるデータの差異'
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
TQID: https://experienceleague.adobe.com/rTwYQgWuhRefe4R9FahGydneNVpv9mP7pqhOeDQwP34
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 3359
ht-degree: 0%

---

# [!DNL Analytics]とAdobe Advertisingの間の予想されるデータの差異

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

[!DNL Analytics for Advertising] <!-- (A4AdC) -->統合を持つ広告主は、Adobe AdvertisingとAdobe Analyticsを通じて有料広告を追跡します。 複数のシステムを使用してメディア、キャンペーン、チャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Adobe Advertisingを通じてトラフィックされるメディアのデータを、[!DNL Analytics]内でメディアが追跡される様々なシステムのデータと比較する方法について説明します。

>[!NOTE]
>
>このドキュメントでは、Adobe AdvertisingとAnalyticsに焦点を当てていますが、重要なポイントの多くは他のトラッキングソリューションにも引き継ぐことができます。

## 類似レポートのアトリビューションの違い

### 異なるルックバックウィンドウやアトリビューションモデルが

[!DNL Analytics for Advertising]統合では、2つの変数（[!DNL eVars]または[!DNL rVars] \[reserved [!DNL eVars]]\）を使用して、[EF IDとAMO ID](ids.md)を取得します。 これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーが帰属する時間）とアトリビューションモデルで設定されます。 特に指定しない限り、変数は、Adobe Advertisingのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、Analytics （[!DNL eVars]経由）とAdobe Advertisingの両方で設定できます。 さらに、Adobe Advertisingでは、アトリビューションモデルは、広告主レベル（入札最適化のため）だけでなく、個々のデータビューやレポート内（レポート目的のみ）でも設定可能です。 例えば、企業は、Advertising DSPまたは[!DNL Advertising Search, Social, & Commerce]のレポートに対して、均等ディストリビューションアトリビューションモデルを最適化に使用し、ラストタッチアトリビューションを使用することを好む場合があります。 アトリビューションモデルを変更すると、帰属を示すコンバージョン数が変化します。

レポートのルックバックウィンドウまたはアトリビューションモデルが、一方の製品で変更され、もう一方の製品で変更されない場合、各システムからの同じレポートには異なるデータが表示されます。

* **異なるルックバックウィンドウによって発生する不一致の例：**

  Adobe Advertisingに60日間のクリックルックバックウィンドウがあり、[!DNL Analytics]に30日間のルックバックウィンドウがあるとします。 例えば、オーディエンスがAdobe Advertisingで追跡された広告を通じてサイトにアクセスし、サイトを離れた後、45日目に戻ってコンバージョンに至ったとします。 Adobe Advertisingは、コンバージョンが60日間のルックバックウィンドウ内で発生したため、コンバージョンを最初の訪問にアトリビューションします。 ただし、[!DNL Analytics]は、30日間のルックバックウィンドウの有効期限が切れた後にコンバージョンが発生したため、コンバージョンを初回訪問に関連付けることはできません。 この例では、Adobe Advertisingは、[!DNL Analytics]よりもコンバージョン数が多いと報告しています。

  ![Adobe Advertisingに属するが[!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)ではないコンバージョンの例

* **異なるアトリビューションモデルによって生じる不一致の例：**

  例えば、オーディエンスがコンバージョンする前に3つの異なるAdobe Advertising広告を操作し、売上をコンバージョンタイプとして指定したとします。 Adobe Advertisingレポートで均等な配信モデルを使用してアトリビューションを実施する場合、あらゆる広告で均等に売上をアトリビューションします。 ただし、[!DNL Analytics]がラストタッチアトリビューションモデルを使用する場合、収益は最後の広告にアトリビューションされます。 次の例では、Adobe Advertisingは3つの広告のそれぞれに対して獲得した30 USDの収益のうち10 USDを帰属させるのに対し、[!DNL Analytics]は30 USDの収益すべてをユーザーが最後に閲覧した広告に帰属させています。 Adobe Advertisingと[!DNL Analytics]のレポートを比較すると、アトリビューションの違いの影響を確認できます。

  ![異なるアトリビューションモデルに基づいて、Adobe Advertisingと[!DNL Analytics]に起因する異なる売上](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>Adobe Advertisingと[!DNL Analytics]の両方で、同じルックバックウィンドウとアトリビューションモデルを使用することをお勧めします。 必要に応じてAdobe アカウントチームと協力して、現在の設定を特定し、設定を同期させます。

同様の概念は、異なるルックバックウィンドウやアトリビューションモデルを使用する他のチャネルにも適用されます。

#### ビュースルーのトラッキング用の異なるルックバックウィンドウ {#impression-lookback}

Adobe Advertisingでは、アトリビューションはクリック数とインプレッション数に基づいています。また、クリック数とインプレッション数に応じて異なるルックバックウィンドウを設定できます。 ただし、[!DNL Analytics]では、アトリビューションはクリックスルーとビュースルーに基づいています。クリックスルーとビュースルーに対して異なるアトリビューションウィンドウを設定するオプションはありません。各アトリビューションのトラッキングは、最初のサイト訪問から開始されます。 インプレッションは、ビュースルーが発生する同じ日または複数日前に発生する可能性があり、各システムでアトリビューションウィンドウが開始されるタイミングに影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分は、両方のシステムが貢献度を割り当てるのに十分な速度で発生します。 ただし、一部のコンバージョンは、Adobe Advertising インプレッションのルックバックウィンドウの外で[!DNL Analytics] ルックバックウィンドウ内で発生する可能性があります。このようなコンバージョンは、[!DNL Analytics]のビュースルーに起因するもので、Adobe Advertisingのインプレッションに起因するものではありません。

次の例では、1日目に訪問者に広告が配信され、2日目にビュースルー訪問（つまり、以前に広告をクリックせずに広告のランディングページを訪問）を実行し、45日目にコンバージョンしたとします。 この場合、Adobe Advertisingは1～14日目（14日間のルックバックを使用）からユーザーをトラッキングし、[!DNL Analytics]は2～61日目（60日間のルックバックを使用）からユーザーをトラッキングし、45日目のコンバージョンは[!DNL Analytics]内の広告に起因しますが、Adobe Advertising内には起因しません。

![&#x200B; ビュースルーコンバージョンの例（[!DNL Analytics]に属するが、Adobe Advertising](/help/integrations/assets/a4adc-viewthrough-example.png)には属さない）

不一致のさらに大きな原因は、Adobe Advertisingでは、クリックベースのコンバージョンに起因するウェイトに関連するカスタム *ビュースルーのウェイト*&#x200B;をビュースルーコンバージョンに割り当てることができることです。 デフォルトのビュースルーの重みは40%です。つまり、ビュースルーコンバージョンは、クリックベースのコンバージョンの値の40%としてカウントされます。 [!DNL Analytics]には、ビュースルーコンバージョンの重み付けはありません。 例えば、デフォルトのビュースルーの重み付けを使用している場合、[!DNL Analytics]でキャプチャされた100 USDの収益注文は、Adobe Advertisingで40 USDに割引されます（差は60 USD）。

Adobe Advertisingと[!DNL Analytics] レポート間のビュースルーコンバージョンを比較する際には、次の違いを考慮してください。

#### 利用可能なアトリビューションモデル

| Adobe Advertising Attribution | [!DNL Analytics] アトリビューション | [!DNL eVar]/[!DNL rVar]配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | なし | なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>使用しない* |
| [!UICONTROL Weight Last Event More] | なし | なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | なし |
| なし | [!UICONTROL J-Shaped] | なし |
| なし | [!UICONTROL Inverse-J] | なし |
| なし | [!UICONTROL Custom] | なし |
| なし | [!UICONTROL Participation] | なし |
| なし | [!UICONTROL Algorithmic] | なし |

>[!NOTE]
>
>線形配分の場合、[!DNL Analytics]は1回の訪問で[!DNL eVar]個の値すべてに対して均等に成功イベントを属性するので、「訪問」の有効期限が[!DNL eVar]の線形配分を使用します。 しかし、広告にとって、直線的なアトリビューションを利用することは、真に直線的ではない配分や、理想的でないレポートにつながります。 例えば、訪問者が3回の別々の訪問でコンバージョンする前に3つの広告とインタラクションした場合、最後の訪問で表示された広告のみがコンバージョンに起因し、3つの広告すべてではないことが示されます。
>
>さらに、コンバージョン割り当てを「線形」に切り替えると、履歴データが表示されず、レポートに誤ったデータが表示される可能性があります。 たとえば、線形配分では、収益を複数の異なる[!DNL eVar]値に分けることができます。 配分を「最新」に変更すると、その収益の100%が最新の単一の値に関連付けられます。 この関連付けにより、誤った結論につながる可能性があります。
>
>混乱を防ぐために、[!DNL Analytics]はレポート インターフェイスで履歴データを使用できなくなります。 [!DNL eVar]を初期割り当て設定に戻すと、履歴データを表示できますが、[!DNL eVar]割り当て設定を変更して履歴データにアクセスすることはできません。 既に大量の履歴データを持つ[!DNL eVar]の配分設定を変更するのではなく、既に記録されているデータに新しい配分設定を適用する場合は、新しい[!DNL eVar]を使用することをお勧めします。

[!DNL Analytics]個のアトリビューションモデルとその定義のリスト（[https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/attribution/models](https://experienceleague.adobe.com/ja/docs/analytics/analyze/analysis-workspace/attribution/models)）を参照してください。

[!DNL Search, Social, & Commerce]にログインしている場合は、リストを見つけることができます

* （北米のユーザー） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （その他のすべてのユーザー） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### Adobe Advertisingのイベント日アトリビューション

Adobe Advertisingでは、関連するクリック日/イベント日（クリック日またはインプレッションイベント日）または取引日（コンバージョン日）によって、コンバージョンデータをレポートできます。 クリック/イベント日レポートの概念が[!DNL Analytics]に存在しません。[!DNL Analytics]で追跡されたすべてのコンバージョンは、トランザクション日ごとにレポートされます。 その結果、同じコンバージョンがAdobe Advertisingと[!DNL Analytics]で異なる日付で報告される場合があります。 例えば、1月1日に広告をクリックし、1月5日にコンバージョンしたオーディエンスを考えてみましょう。 Adobe Advertisingのイベント日別のコンバージョンデータを表示している場合は、クリックが発生した1月1日にコンバージョンが報告されます。 [!DNL Analytics]では、1月5日に同じコンバージョンが報告されます。

![異なる日付に起因するコンバージョンの例](/help/integrations/assets/a4adc-conversions-based-on.png)

## [!DNL Analytics Marketing Channels]のアトリビューション

[[!DNL Analytics Marketing Channels]  レポート &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=ja)を使用すると、ヒット情報の異なる側面に基づいて異なるマーケティングチャネルを識別するルールを設定できます。 [!UICONTROL Display Click Through] クエリ文字列パラメーターを使用して、Adobe Advertisingで追跡されたチャネル （[!UICONTROL Display View Through]、[!UICONTROL Paid Search]および[!DNL Marketing Channels]）を`ef_id`として追跡できます。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. -->ただし、[!DNL Marketing Channels] レポートはAdobe Advertising チャネルを追跡できますが、いくつかの理由により、データがAdobe Advertising レポートと一致しない場合があります。 詳しくは、次の節を参照してください。

>[!NOTE]
>
> 次のコアコンセプトは、[`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html?lang=ja)変数（「トラッキングコード」ディメンションまたは「[!DNL eVar] 0」とも呼ばれます）やカスタム [!DNL eVar] トラッキングなど、Adobe Advertisingでトラッキングされていないキャンペーンを含むマルチチャネルトラッキングにも適用されます。

### [!DNL Marketing Channels]で異なる可能性のあるアトリビューションモデル

ほとんどの[!DNL Marketing Channels] レポートには[!UICONTROL Last Touch] アトリビューションが設定されており、最後に検出されたマーケティングチャネルにはコンバージョン値の100%が割り当てられています。 [!DNL Marketing Channels] レポートとAdobe Advertising レポートに異なるアトリビューションモデルを使用すると、アトリビューションコンバージョンが異なります。

### [!DNL Marketing Channels]のルックバックウィンドウが異なる可能性があります

[!DNL Marketing Channels]のルックバックウィンドウはカスタマイズできます。 Adobe Advertisingでは、クリックルックバックウィンドウは設定可能ですが、60日間の固定ウィンドウが一般的です。 2つの製品で異なるルックバックウィンドウを使用する場合、データの不一致が発生する可能性があります。

### [!DNL Marketing Channels]の別のチャネルアトリビューション

Adobe Advertising レポートでは、Adobe Advertisingを通じて売買された有料メディア（[!DNL Advertising Search, Social, & Commerce]広告の有料検索およびAdvertising DSP広告のディスプレイ）のみをキャプチャしますが、[!DNL Marketing Channels]件のレポートでは、すべてのデジタルチャネルをトラッキングできます。 これは、コンバージョンの原因となるチャネルの不一致につながる可能性があります。

例えば、有料検索と自然検索のチャネルは、多くの場合、相互に影響を及ぼし合っています。両者の連携により、各チャネル間の連携を促進します。 [!DNL Marketing Channels] レポートでは、一部のコンバージョンが自然検索に属しており、Adobe Advertisingでは自然検索がトラッキングされていないため、このコンバージョンは発生していません。

ディスプレイ広告を閲覧し、有料検索広告をクリックし、メールメッセージ内をクリックして30米ドルの注文をおこなった顧客も考慮してください。 Adobe Advertisingと[!DNL Marketing Channels]の両方がラストタッチアトリビューションモデルを使用している場合でも、コンバージョンの貢献度はそれぞれ異なります。 Adobe Advertisingは[!UICONTROL Email] チャネルにアクセスできないため、コンバージョンの有料検索にクレジットが割り当てられます。 ただし、[!DNL Marketing Channels]は3つのチャネルすべてにアクセスできるため、コンバージョンに対して[!UICONTROL Email]を割り当てます。

![Adobe Advertisingのコンバージョンアトリビューションと[!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)の比較の例

指標が異なる理由について詳しくは、「[Adobe Advertisingと [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md)でチャネルデータが異なる理由」を参照してください。

## Adobe Analytics [!DNL Paid Search Detection]のデータの違い

[の [!DNL Paid Search Detection] レガシー](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html?lang=ja) [!DNL Analytics]機能を使用すると、指定した検索エンジンに対する有料およびオーガニック検索トラフィック [を追跡するルールを](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html?lang=ja)定義できます。 [!DNL Paid Search Detection] ルールでは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 [!DNL Paid Search Detection]件のレポートは、[検索方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html?lang=ja)件のレポートの大きなグループの一部であり、指定されたイベント（カートのチェックアウトなど）が発生するか、訪問が終了すると有効期限が切れます。

[!DNL Paid Search Detection] ルール セットを作成するためのインターフェイスを次に示します。

![[!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)で設定された有料検索検出ルールの例

[!DNL Paid Search Detection]件のレポートには、[!UICONTROL Paid Search Engine]、[!UICONTROL Paid Search Keywords]、[!UICONTROL Natural Search Engine]および[!UICONTROL Natural Search Keywords]件のレポートが含まれます。

[!DNL Paid Search Detection] レポートのデータには、次の2つの制限があります。

* [!UICONTROL Paid Search Keywords]および[!UICONTROL Natural Search Keywords] レポートには、ユーザーが入札するキーワードではなく、参照URLによって識別された検索クエリが表示されます。 Adobe Advertisingおよび[!DNL Analytics]件のレポートには実際のキーワードが表示されているため、[!DNL Paid Search Detection]件のキーワードレポートと一致すると思わないでください。

* [!DNL Paid Search Detection]機能が最初に作成されたとき、元の検索クエリ（ユーザーが検索エンジンの検索バーに入力した文字列）は、参照URLを介して広告主がより簡単に利用できるようになりました。 今日では、検索エンジンは検索クエリをほとんど難読化しており、ほとんどのクエリデータが「未指定」に該当するため、[!DNL Paid Search Detection] キーワードレポートの価値は限られています。

  [!DNL Analytics for Advertising]では、広告主は[!DNL Analytics]の有料キーワードを引き続き追跡できます。 参照ドメインは、どの検索エンジンがトラフィックを促進したかをエンジンレポートに通知します。 広告主固有のアカウント情報は参照ドメインに関連付けられていないので、あらゆるトラフィックが検索エンジンの下に一覧表示されます。 同じ検索エンジンに複数のアカウントを持つ広告主は、アカウント固有のレポートについて、Adobe Advertisingまたは[!DNL Analytics]のレポートを参照する必要があります。

### [!DNL Paid Search Detection]を設定する理由

[!DNL Paid Search Detection] レポートを使用すると、[[!DNL Analytics Marketing Channels]  レポート &#x200B;](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html?lang=ja)で自然検索トラフィックを特定できます。 有料検索トラフィックと自然検索トラフィックを分離することは、自然検索がマーケティングエコシステム全体にもたらす価値を理解する優れた方法です。

## [!DNL Analytics for Advertising]のクリックスルーデータ検証 {#data-validation}

統合をおこなうには、クリックスルー情報を検証し、サイト上のすべてのページがクリックスルーを適切に追跡していることを確認する必要があります。

[!DNL Analytics]では、[!DNL Analytics for Advertising]追跡を検証する最も簡単な方法の1つは、「AMO ID インスタンスからクリックへの比較」計算指標を使用してインスタンスをクリックに比較することです。計算指標は次のように計算されます。

```
AMO ID Instances to Clicks = ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

[!UICONTROL AMO ID Instances]は、[AMO ID](ids.md)がサイトで追跡される回数を表します。 広告をクリックするたびに、AMO ID （`s_kwcid`） パラメーターがランディングページ URLに追加されます。 したがって、[!UICONTROL AMO ID Instances]の数はクリック数に類似しており、実際の広告クリック数に対して検証できます。 通常、[!DNL Search, Social, & Commerce]の一致率は85%、[!DNL DSP] トラフィックの一致率は30%になります（クリックスルー[!UICONTROL AMO ID Instances]のみを含めるようにフィルタリングした場合）。 検索と表示の期待値の違いは、予想されるトラフィック動作によって説明できます。 検索は意図をキャプチャし、そのため、ユーザーは通常、クエリから検索結果をクリックしようとします。 一方、ディスプレイ広告やオンライン動画広告を目にする利用者は、意図せずにその広告をクリックし、サイトから離れたり、ページアクティビティが追跡される前に読み込まれる新しいウィンドウを放棄したりする可能性が高くなります。

Adobe Advertising レポートでは、同様に、[!UICONTROL EF ID Instances]ではなく「[!UICONTROL AMO ID Instances]」指標を使用してインスタンスをクリックと比較できます。

```
EF ID Instances to Clicks = ([!UICONTROL EF ID Instances] / [!UICONTROL Adobe Advertising Clicks])
```

AMO IDとEF IDの間に高い一致率が期待される必要がありますが、AMO IDとEF IDは基本的に異なるデータを追跡するため、100%のパリティは期待できません。この違いにより、合計[!UICONTROL AMO ID Instances]と[!UICONTROL EF ID Instances]にわずかな違いが生じる可能性があります。 ただし、[!UICONTROL AMO ID Instances]の合計[!DNL Analytics]がAdobe Advertisingの[!UICONTROL EF ID Instances]と1%以上異なる場合は、Adobe アカウントチームにお問い合わせください。

AMO IDとEF IDについて詳しくは、[Analyticsで使用されるAdobe Advertising ID](ids.md)を参照してください。

<!--
  Need to create a new report to show tracking instances to clicks, instead of clicks to instances as shown, and replace this screenshot.

The following is an example of a workspace to track clicks to instances.

![Example of a workspace to track clicks to instances to clicks](/help/integrations/assets/a4adc-clicks-to-instances-example.png)
-->

### クリックとインスタンス間の相違のトラブルシューティング

[!UICONTROL EF ID Instances]対クリックの比率が85%未満の場合は、次の点を確認してください。

* アカウントまたは任意のサブレベルでクリックトラッキングが欠落しているか、または重複したクリックトラッキング（アカウントレベルとキャンペーンレベルの両方など）がありますか？

  Search, Social, &amp; Commerceで、[&#x200B; アカウントのバルクシートをダウンロード &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-download.md)して、トラッキング URLを確認します。

  また、[!DNL Analytics]では、次のように計算された「[!DNL AMO ID] ～ [!DNL EF ID]」計算指標を使用して、AMO IDとEF IFが一貫して追加されているかどうかを確認できます。

  ```
  [!DNL AMO ID] to [!DNL EF ID] = ([!UICONTROL AMO ID] / [!DNL EF ID])
  ```

  100%を超える値は、AMO IDよりも多くのEF IDが見つからないことを示します。

* AMO IDとEF IDがキャプチャされないように、ランディングページの読み込みに問題がありますか？

* AMO IDとEF IDが失われるように、ランディングページのURLがリダイレクトされますか？

* すべてのランディングページは、設定されたレポートスイートを使用しますか？

>[!NOTE]
>
>理論的には、1つのインスタンスに複数のクリックがある可能性があります。 さまざまなデバイス（デスクトップ、モバイル、タブレットなど）でクリック数を確認してください。

## [!DNL Analytics for Advertising]とAdobe Advertisingのデータセットの比較

[AMO ID](ids.md) （s_kwcid クエリ文字列パラメーター）は[!DNL Analytics]のレポートに使用され、[EF ID](ids.md) （ef_id クエリ文字列パラメーター）はAdobe Advertisingのレポートに使用されます。 これらの値は個別の値であるため、1つの値が壊れているか、ランディングページに追加されない可能性があります。

例えば、次のランディングページがあるとします。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

ef IDは&quot;`test_ef_id`&quot;、AMO IDは&quot;`test_amo_id`&quot;です。

サイト側のリダイレクトが発生した場合、URLは次のようになります。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

ef IDは&quot;`test_ef_id`&quot;、AMO IDは&quot;`test_amo_id#redirectAnchorTag`&quot;です。

この例では、アンカータグを追加すると、AMO IDに予期しない文字が追加され、Analyticsが認識しない値が生成されます。 このAMO IDは分類されず、それに関連付けられているコンバージョンは、[!UICONTROL unspecified]件のレポートで「[!UICONTROL none]」または「[!DNL Analytics]」に該当します。

幸いなことに、このような問題は一般的ですが、一般的にそれほど大きな割合で食い違いがあるわけではありません。 ただし、[!DNL Analytics]のAMO IDとAdobe AdvertisingのEF IDの間に大きな相違が見られる場合は、Adobe アカウントチームにお問い合わせください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

両者は類似しているように思えますが、クリック数と訪問数でデータは異なります。

* **クリック：** [!DNL DSP]または検索エンジンは、訪問者がパブリッシャーのweb サイト上の広告をクリックしたときにクリックを記録します。

* **訪問：** [!DNL Analytics]は、[訪問](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html?lang=ja)をユーザーによる一連のページビューとして定義し、30分間の非アクティブな状態など、いくつかの条件のいずれかに従って終了します。

定義によれば、ワンクリックで複数の訪問につながる可能性があります。

次の例を考えてみましょう。ユーザー1とユーザー2は、両方ともAdobe Advertising広告をクリックしてサイトにアクセスします。 ユーザー1は4 ページを表示し、その日に移動するので、最初のクリックは1回の訪問になります。 ユーザー2は2 ページを表示し、45分間のランチを残し、戻り、さらに2 ページを表示してから退出します。この場合、最初のクリックは2回の訪問になります。

![&#x200B; クリック数と訪問数の違いの例](/help/integrations/assets/a4adc-visits-example.png)

### クリックスルーとクリックスルーの違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、次のふたつの指標です。

* **クリック：** [!DNL DSP]または検索エンジンは、訪問者がパブリッシャーのweb サイト上の広告をクリックしたときにクリックを記録します。

* **クリックスルー：** [!DNL Analytics]は、訪問者が目的のweb サイトにアクセスし、ランディングページが読み込まれ、ページの下部にある[!DNL Analytics] リクエストが[!DNL Analytics]にデータを送信したときに、クリックスルーを記録します。

クリック数とクリック数は、誤って広告がクリックされたために大きく異なる場合があります。 ディスプレイ広告のほとんどのクリックは誤ったクリックであり、これらの偶発的な訪問者はランディングページが読み込まれる前に「戻る」ボタンを押したので、[!DNL Analytics]はクリックを記録できません。 特に、モバイル広告、動画広告、画面に表示される広告など、意図しないクリックが発生する可能性が高く、オーディエンスがページを表示する前に広告を閉じる必要がある広告では、その傾向が顕著です。

モバイルデバイスで読み込まれたサイトは、帯域幅が狭かったり、処理能力が利用可能であったりするため、クリックスルーの可能性が低く、ランディングページの読み込みに時間がかかったりします。 クリックの50～70%がクリックスルーにつながらないことは珍しくありません。 モバイル環境では、動作の遅いブラウザーと、ユーザーがページをスクロールしたり広告を閉じようとしたりしているときに誤って広告をクリックする可能性が高いため、その差は90%に達します。

また、クリックデータは、現在のトラッキングメカニズム（モバイルアプリに入る、またはモバイルアプリから入るクリックなど）でのクリックスルーを記録できない環境や、広告主が1つのトラッキングアプローチ（ビュースルーJavaScriptアプローチでは、サードパーティのCookieをブロックするブラウザーはクリックをトラッキングしますが、クリックスルーを行わない）のみをデプロイした環境でも記録される場合があります。 Adobeが、クリック URL トラッキングとビュースルーJavaScript トラッキングの両方のアプローチをデプロイすることを推奨する主な理由は、追跡可能なクリックスルーのカバレッジを最大化することです。

### Adobe Advertising以外のディメンションに対するAdobe Advertising トラフィック指標の使用

Adobe Advertisingは、[広告固有のトラフィック指標と [!DNL DSP] および [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md)の関連ディメンションをAnalyticsに提供します。 Adobe Advertisingが提供する指標は、指定したAdobe Advertising ディメンションにのみ適用され、[!DNL Analytics]の他のディメンションではデータを使用できません。

例えば、Adobe Advertising ディメンションである[!UICONTROL Adobe Advertising Clicks]および[!UICONTROL Adobe Advertising Cost]指標をアカウント別に表示すると、合計[!UICONTROL Adobe Advertising Clicks]および[!UICONTROL Adobe Advertising Cost]がアカウント別に表示されます。

![Adobe Advertising ディメンションを使用したレポート内のAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、Adobe Advertisingがデータを提供しないページ上のディメンション（ページなど）で[!UICONTROL Adobe Advertising Clicks]と[!UICONTROL Adobe Advertising Cost]指標を表示する場合、各ページの[!UICONTROL Adobe Advertising Clicks]と[!UICONTROL Adobe Advertising Cost]はゼロ（0）になります。

![&#x200B; サポートされていないディメンションを使用するレポート内のAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### Adobe Advertising以外のディメンションを含むクリックの代わりに[!UICONTROL AMO ID Instances]を使用

オンサイトのディメンションでは[!UICONTROL AMO Clicks]を使用できないので、クリックに相当するものを見つけることをお勧めします。 訪問を代わりに使用したいと思うかもしれませんが、各訪問者には複数の訪問がある可能性があるため、最適なオプションではありません。 （「[&#x200B; クリック数と訪問数の違い](#clicks-vs-visits)」を参照してください。」 代わりに、AMO IDがキャプチャされる回数である[!UICONTROL AMO ID Instances]を使用することをお勧めします。 [!UICONTROL AMO ID Instances]は[!UICONTROL AMO Clicks]と正確には一致しませんが、サイトのクリックトラフィックを測定するには最適なオプションです。 詳しくは、「[のクリックスルーデータ検証」を参照してください。 [!DNL Analytics for Advertising]](#data-validation)

サポートされていないディメンション ![の[!UICONTROL AMO ID Instances]ではなく[!UICONTROL Adobe Advertising Clicks]の例](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [様が使用している [!DNL Analytics]](/help/integrations/analytics/ids.md)Adobe Advertising ID
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* Adobe Advertisingの[[!DNL Analytics]  データ &#x200B;](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Adobe Advertisingと [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)でチャネルデータが異なる理由
