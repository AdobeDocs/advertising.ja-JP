---
title: A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe Advertising
description: A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe Advertising
feature: Integration with Adobe Analytics
exl-id: 66b49881-bda1-49ef-ab8a-61399b8edd0f
source-git-commit: e564ea441e5ea0d25ee7f99962e72192750c5c40
workflow-type: tm+mt
source-wordcount: '3265'
ht-degree: 0%

---

# A と B の間で予想されるデータの相違 [!DNL Analytics] およびAdobe Advertising

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

次を持つ広告主 [!DNL Analytics for Advertising] <!-- (A4AdC) --> 統合では、Adobe AdvertisingとAdobe Analyticsを通じて有料広告を追跡します。 複数のシステムを介してメディア、キャンペーン、チャネルを追跡する場合、異なるシステムの同じデータセットが完全に一致することはほとんどありません。 このドキュメントでは、Adobe Advertisingを通じてトラフィックされるメディアのデータを、そのメディアがトラッキングされる様々なシステムのデータと比較する方法について説明します [!DNL Analytics].

>[!NOTE]
>
>このドキュメントはAdobe Advertisingと Analytics に焦点を当てていますが、主なポイントの多くは他のトラッキングソリューションにも移行できます。

## 類似したレポートでのアトリビューションの違い

### 潜在的に異なるルックバックウィンドウとアトリビューションモデル

The [!DNL Analytics for Advertising] 統合では、2 つの変数 ([!DNL eVars] または [!DNL rVars] \[ 予約済み [!DNL eVars]]\) をキャプチャします。 [EF ID と AMO ID](ids.md). これらの変数は、単一のルックバックウィンドウ（クリックスルーとビュースルーの属性が割り当てられる時間）とアトリビューションモデルを使用して設定されます。 特に指定のない限り、変数は、Adobe Advertisingのデフォルトの広告主レベルのクリックルックバックウィンドウとアトリビューションモデルに一致するように設定されます。

ただし、ルックバックウィンドウとアトリビューションモデルは、Analytics の両方で ( [!DNL eVars]) とAdobe Advertising また、Adobe Advertisingでは、アトリビューションモデルは、広告主レベル（入札の最適化用）でのみならず、個々のデータビューおよびレポート内（レポート目的のみ）で設定できます。 例えば、最適化のために偶数配分アトリビューションモデルを使用し、Advertising DSPのレポートにラストタッチアトリビューションを使用したい場合や [!DNL Advertising Search, Social, & Commerce]. アトリビューションモデルを変更すると、アトリビューションコンバージョンの数が変更されます。

レポートのルックバックウィンドウまたはアトリビューションモデルが 1 つのプロダクトで変更され、他のプロダクトでは変更されない場合、各システムと同じレポートに個別のデータが表示されます。

* **様々なルックバックウィンドウが原因で生じる不一致の例を次に示します。**

  Adobe Advertisingに 60 日間のクリックルックバックウィンドウがあり、 [!DNL Analytics] には、30 日間のルックバックウィンドウがあります。 また、ユーザーがAdobe Advertising追跡された広告を通じてサイトにアクセスし、離れてから、45 日目に戻ってコンバージョンをおこなったとします。 Adobe Advertisingは、60 日間のルックバックウィンドウ内でコンバージョンが発生したので、初回訪問に対してコンバージョンを関連付けます。 [!DNL Analytics]ただし、は、30 日間のルックバックウィンドウの有効期限が切れた後にコンバージョンが発生したので、初回訪問にコンバージョンを関連付けることはできません。 この例では、Adobe Advertisingは、 [!DNL Analytics] そうです。

  ![Adobe Advertisingに属するが属さないコンバージョンの例 [!DNL Analytics]](/help/integrations/assets/a4adc-lookback-example.png)

* **様々なアトリビューションモデルが原因で生じる不一致の例：**

  コンバージョンをおこなう前に、ユーザーが 3 つの異なるAdobe Advertising広告を操作し、コンバージョンタイプに売上高を指定したとします。 Adobe Advertisingレポートで、アトリビューションに偶数配分モデルを使用する場合、すべての広告の売上高を均等にアトリビューションします。 次の場合 [!DNL Analytics] はラストタッチ属性モデルを使用しますが、その後、売上高は最後の広告に属性付けされます。 次の例では、Adobe Advertisingは、3 つの広告のそれぞれに対して取り込まれた売上高の 30 米ドルのうち、10 米ドルを偶数の広告の属性にします。 [!DNL Analytics] は、ユーザーが閲覧した最後の広告に対する売上高の 30 USD すべてを属性にします。 Adobe Advertisingと [!DNL Analytics]の場合は、アトリビューションの違いの影響を確認できます。

  ![Adobe Advertisingと [!DNL Analytics] 様々なアトリビューションモデルに基づく](/help/integrations/assets/a4adc-attribution-example.png)

>[!IMPORTANT]
>
>ベストプラクティスは、Adobe Advertisingと [!DNL Analytics]. 必要に応じてAdobeアカウントチームと協力し、現在の設定を特定し、設定を同期させます。

これらの同じ概念は、異なるルックバックウィンドウやアトリビューションモデルを使用する他のチャネルなどにも当てはまります。

#### ビュースルートラッキングのための異なるルックバックウィンドウ {#impression-lookback}

Adobe Advertisingでは、アトリビューションはクリック数とインプレッション数に基づいており、クリック数およびインプレッション数に対して様々なルックバックウィンドウを設定できます。 In [!DNL Analytics]ただし、アトリビューションはクリックスルー数とビュースルー数に基づいており、クリックスルー数とビュースルー数に異なるアトリビューションウィンドウを設定するオプションはありません。最初のサイト訪問で開始する各アトリビューションのトラッキング。 インプレッションは、ビュースルーが発生する同じ日または複数日前に発生する可能性があり、各システムでアトリビューションウィンドウが開始する場合に影響を与える可能性があります。

通常、ビュースルーコンバージョンの大部分はすぐに発生し、両方のシステムがクレジットを考慮に入れます。 ただし、一部の変換は、Adobe Advertisingインプレッションのルックバックウィンドウ以外で、 [!DNL Analytics] ルックバックウィンドウ。このような変換は、 [!DNL Analytics] しかしAdobe Advertisingの印象には

次の例では、訪問者が Day 1 に広告を提供し、ビュースルー訪問（つまり、広告を以前にクリックせずに広告のランディングページを訪問）を実行し、Day 2 に変換したとします。その後、 45 に変換したとします。 この場合、Adobe Advertisingは、1 ～ 14 日（14 日間のルックバックを使用）のユーザーを追跡します。 [!DNL Analytics] では 2 ～ 61 日（60 日間のルックバックを使用）のユーザーを追跡し、45 日目のコンバージョンは内の広告に関連付けられます [!DNL Analytics] しかしAdobe Advertising内では

![に属するビュースルーコンバージョンの例 [!DNL Analytics] しかしAdobe Advertisingではない](/help/integrations/assets/a4adc-viewthrough-example.png)

不一致のさらなる原因は、Adobe Advertisingで、ビュースルーコンバージョンをカスタム *ビュースルーの重み* クリックベースのコンバージョンに起因する重みに対する相対的な値。 デフォルトのビュースルーの重み付けは 40%です。つまり、ビュースルーのコンバージョンは、クリックベースのコンバージョンの値の 40%としてカウントされます。 [!DNL Analytics] では、ビュースルーコンバージョンに対して、このような重み付けは行われません。 例えば、 [!DNL Analytics] は、デフォルトのビュースルーの重み付け（60 USD の違い）を使用している場合、Adobe Advertisingで 40 USD に割引されます。

Adobe Advertisingとの間のビュースルーコンバージョンを比較する際には、次の違いを考慮してください [!DNL Analytics] レポート。

#### 使用可能なアトリビューションモデル

| Adobe Advertising属性 | [!DNL Analytics] 帰属 | [!DNL eVar]/[!DNL rVar] 配分 |
|--- |--- |--- |
| [!UICONTROL Last Event] | [!UICONTROL Last Touch] | [!UICONTROL Most Recent] |
| [!UICONTROL First Event] | [!UICONTROL First Touch] | [!UICONTROL Original Value] |
| [!UICONTROL Weight First Event More] | 該当なし | 該当なし |
| [!UICONTROL Even Distribution] | [!UICONTROL Linear] | [!UICONTROL Linear]<br><br>使用しない* |
| [!UICONTROL Weight Last Event More] | 該当なし | 該当なし |
| [!UICONTROL U-Shaped] | [!UICONTROL U-Shaped] | 該当なし |
| 該当なし | [!UICONTROL J-Shaped] | 該当なし |
| 該当なし | [!UICONTROL Inverse-J] | 該当なし |
| 該当なし | [!UICONTROL Custom] | 該当なし |
| 該当なし | [!UICONTROL Participation] | 該当なし |
| 該当なし | [!UICONTROL Algorithmic] | 該当なし |

>[!NOTE]
>
>線形配分の場合、 [!DNL Analytics] すべての [!DNL eVar] 値を 1 回の訪問で設定する場合は、線形配分を [!DNL eVar] 「訪問」の有効期限。 ただし、広告の場合、線形アトリビューションを使用すると、配分が実際には線形ではなく、理想的でないレポートになります。 例えば、訪問者が 3 つの広告を操作してから 3 回の個別の訪問にコンバージョンした場合、3 つの広告のすべてではなく、最後の訪問で表示された広告のみがコンバージョンに関連付けられます。
>
>また、コンバージョンの配分を「線形」に切り替えたり、「線形」から切り替えたりすると、履歴データが表示されなくなり、レポートに誤ったデータが表示される可能性があります。 例えば、線形配分では売上高を異なる [!DNL eVar] 値。 配分を「最新」に変更すると、その売上高の 100%が最新の単一の値に関連付けられます。 この関連付けは、誤った結論に導く可能性があります。
>
>混乱を避けるために、 [!DNL Analytics] は、レポートインターフェイスで履歴データを使用できなくします。 履歴データは、 [!DNL eVar] 最初の配分設定に戻りますが、 [!DNL eVar] 割り当て設定を使用して、履歴データにアクセスするだけで済みます。 Adobeは、新しい [!DNL eVar] 既に記録されているデータに対して新しい割り当て設定を適用する場合。 [!DNL eVar] 既に大量の履歴データを持っている

次のリストを参照： [!DNL Analytics] アトリビューションモデルとその定義 ( ) [https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-workspace/attribution/models.html).

ログインしている場合 [!DNL Search, Social, & Commerce]を使用すると、リストを検索できます

* （北米の利用者） [`https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-na.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

* （その他すべてのユーザ） [`https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm`](https://enterprise-intl.efrontier.com/CMDashboard/help/external/tracking/r_appendix_-_how_attribution_rules_are_calculated.htm)

#### イベント日属性のAdobe Advertising

Adobe Advertisingでは、関連するクリック日/イベント日（クリックイベントまたはインプレッションイベントの日付）またはトランザクション日（コンバージョン日）に基づいてコンバージョンデータをレポートできます。 クリック/イベント日レポートの概念がに存在しません [!DNL Analytics]；で追跡されたすべてのコンバージョン。 [!DNL Analytics] はトランザクション日別にレポートされます。 その結果、異なる日付のコンバージョンが、Adobe Advertisingと [!DNL Analytics]. 例えば、1 月 1 日に広告をクリックして 1 月 5 日にコンバージョンするユーザーがいるとします。 Adobe Advertisingでイベント日別のコンバージョンデータを表示している場合、クリックが発生した 1 月 1 日にコンバージョンがレポートされます。 In [!DNL Analytics]同じコンバージョンが 1 月 5 日に報告されます。

![異なる日付に属するコンバージョンの例](/help/integrations/assets/a4adc-conversions-based-on.png)

## の属性 [!DNL Analytics Marketing Channels]

[[!DNL Analytics Marketing Channels] レポート](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html) では、ヒット情報の個々の側面に基づいて様々なマーケティングチャネルを識別するルールを設定できます。 Adobe Advertising追跡されたチャネル ([!UICONTROL Display Click Through], [!UICONTROL Display View Through]、および [!UICONTROL Paid Search]) として [!DNL Marketing Channels] を使用して、 `ef_id` チャネルを識別するクエリー文字列パラメーター。 <!-- Move most of the above text to "Marketing Channels" chapter once it's created, and add link here. --> ただし、 [!DNL Marketing Channels] レポートでAdobe Advertisingチャネルを追跡できますが、いくつかの理由でデータがAdobe Advertisingレポートと一致しない場合があります。 詳しくは、次の節を参照してください。

>[!NOTE]
>
> 以下のコア概念は、Adobe Advertisingで追跡されないキャンペーン ( [`campaign`](https://experienceleague.adobe.com/docs/analytics/implementation/vars/page-vars/campaign.html) 変数 (「トラッキングコード」ディメンションまたは「[!DNL eVar] 0&quot;) およびカスタム [!DNL eVar] トラッキング。

### では様々なアトリビューションモデルが生成される可能性がある [!DNL Marketing Channels]

最も多い [!DNL Marketing Channels] レポートは、 [!UICONTROL Last Touch] アトリビューション。最後に検出されたマーケティングチャネルに、コンバージョン値の 100%が割り当てられます。 に対する様々なアトリビューションモデルの使用 [!DNL Marketing Channels] レポートとAdobe Advertisingレポートでは、属性コンバージョンの相違が生じます。

### の別のルックバックウィンドウ [!DNL Marketing Channels]

のルックバックウィンドウ [!DNL Marketing Channels] カスタマイズ可能です。 Adobe Advertisingでは、クリックのルックバックウィンドウは設定できますが、60 日間の固定ウィンドウは一般的です。 2 つの製品で異なるルックバックウィンドウが使用されている場合、データの相違が生じる可能性があります。

### での様々なチャネルアトリビューション [!DNL Marketing Channels]

Adobe Advertisingレポートは、Adobe Advertising( [!DNL Advertising Search, Social, & Commerce] 広告、および Advertising DSP広告用のディスプレイ ) を表示するのに対して、 [!DNL Marketing Channels] レポートでは、すべてのデジタルチャネルを追跡できます。 これは、コンバージョンが属するチャネルに矛盾が生じる可能性があります。

例えば、有料検索や自然検索のチャネルは、多くの場合共生関係にあり、各チャネルが相互に支援します。 The [!DNL Marketing Channels] レポートでは、Adobe Advertisingが自然検索を追跡しないので、自然検索に対するコンバージョンの一部が考慮されます。

また、ディスプレイ広告を表示し、有料検索広告をクリックし、電子メールメッセージ内をクリックして、30 米ドルの注文をするお客様も考えてみましょう。 たとえAdobe Advertisingでも [!DNL Marketing Channels] 両方ともラストタッチアトリビューションモデルを使用しているので、コンバージョンの属性はそれぞれ異なります。 Adobe Advertisingは、 [!UICONTROL Email] チャネルに送信されるので、有料検索にコンバージョンのクレジットが付与されます。 [!DNL Marketing Channels]ただし、は 3 つのチャネルすべてにアクセスできるので、 [!UICONTROL Email] を呼び出します。

![Adobe Advertisingとコンバージョンでの様々なコンバージョンアトリビューションの例 [!DNL Analytics Marketing Channels]](/help/integrations/assets/a4adc-channel-example.png)

指標が異なる理由について詳しくは、[チャネルとの間でチャネルデータが異なる理由 [!DNL Marketing Channels]](marketing-channels/mc-data-variances.md).&quot;

## Adobe Analyticsのデータの違い [!DNL Paid Search Detection]

The [レガシー [!DNL Paid Search Detection]](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/manage-report-suites/edit-report-suite/report-suite-general/paid-search-detection/paid-search-detection.html) ～の特徴 [!DNL Analytics] 企業が [有料検索トラフィックとオーガニック検索トラフィックを追跡するルールを定義する](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/paid-search-detection/t-paid-search-detection.html) を参照してください。 The [!DNL Paid Search Detection] ルールでは、クエリ文字列と参照ドメインの両方を使用して、有料検索トラフィックと自然検索トラフィックを識別します。 The [!DNL Paid Search Detection] レポートは、 [検索方法](https://experienceleague.adobe.com/docs/analytics/admin/admin-tools/finding-methods.html) レポート。指定したイベント（買い物かごのチェックアウトなど）が発生したとき、または訪問が終了したときに期限切れになります。

次に、 [!DNL Paid Search Detection] ルールセット：

![有料検索検知ルールの例 ( [!DNL Analytics]](/help/integrations/assets/a4adc-paid-search-detection.png)

結果 [!DNL Paid Search Detection] レポートには、 [!UICONTROL Paid Search Engine], [!UICONTROL Paid Search Keywords], [!UICONTROL Natural Search Engine]、および [!UICONTROL Natural Search Keywords] レポート。

のデータに関する次の 2 つの制限に注意してください。 [!DNL Paid Search Detection] レポート：

* The [!UICONTROL Paid Search Keywords] および [!UICONTROL Natural Search Keywords] レポートには、ユーザーが入札するキーワードではなく、参照 URL で識別された検索クエリが表示されます。 Adobe Advertisingと [!DNL Analytics] レポートには実際のキーワードが表示されるので、 [!DNL Paid Search Detection] キーワードレポート。

* 次の場合に [!DNL Paid Search Detection] もともとの機能は作成されたので、元の検索クエリ（ユーザーが検索エンジンの検索バーに入力した文字列）は、参照 URL を使用して、より簡単に広告主に提供されるようになりました。 現在、検索エンジンは検索クエリをほとんど不明化し、 [!DNL Paid Search Detection] ほとんどのクエリデータは「未指定」に分類されるので、キーワードレポートの値は制限されます。

  を使用 [!DNL Analytics for Advertising]を使用して、広告主は有料キーワードを引き続き追跡できます [!DNL Analytics]. 参照ドメインは、トラフィックを駆動した検索エンジンをエンジンレポートに通知します。 広告主固有のアカウント情報は参照ドメインに結び付けられないので、すべてのトラフィックは検索エンジンの下に表示されます。 同じ検索エンジンに複数のアカウントを持つ広告主は、Adobe Advertisingまたは [!DNL Analytics] レポートを作成することをお勧めします。

### を設定する理由 [!DNL Paid Search Detection]?

The [!DNL Paid Search Detection] レポートでは、 [[!DNL Analytics Marketing Channels] レポート](https://experienceleague.adobe.com/docs/analytics/components/marketing-channels/analyze-mc.html). 有料検索トラフィックと自然検索トラフィックを区別することは、自然検索が完全なマーケティングエコシステムにもたらす価値を理解するうえで役立ちます。

## 次のクリックスルーデータ検証： [!DNL Analytics for Advertising] {#data-validation}

統合の場合は、クリックスルーデータを検証して、サイト上のすべてのページがクリックスルーを適切に追跡していることを確認する必要があります。

In [!DNL Analytics]（を検証する最も簡単な方法の 1 つ） [!DNL Analytics for Advertising] の追跡は、「クリック数」を使用してインスタンスとクリック数を比較することで、 [!UICONTROL AMO ID Instances]」計算指標は次のように計算されます。

```
Clicks to [!UICONTROL AMO ID Instances] = ([!UICONTROL AMO ID Instances] / Adobe Advertising Clicks)
```

[!UICONTROL AMO ID Instances] の回数を表します [AMO ID](ids.md) がサイトで追跡されます。 広告がクリックされるたびに、AMO ID(`s_kwcid`) パラメーターがランディングページの URL に追加されました。 次の数 [!UICONTROL AMO ID Instances]したがって、はクリック数に似ており、実際の広告クリックに対して検証できます。 のマッチ率は通常 80%です。 [!DNL Search, Social, & Commerce] との 30%の一致率 [!DNL DSP] トラフィック（クリックスルーのみを含めるようにフィルタリングした場合） [!UICONTROL AMO ID Instances]) をクリックします。 検索と表示の期待値の違いは、予想されるトラフィック動作によって説明できます。 検索は目的をキャプチャし、そのため、ユーザーは通常、クエリの検索結果をクリックする予定です。 ただし、ディスプレイ広告やオンラインビデオ広告を見たユーザーは、意図せず広告をクリックした後、サイトからバウンスするか、ページアクティビティが追跡される前に読み込まれる新しいウィンドウを破棄する可能性が高くなります。

Adobe Advertisingレポートでは、同様に、「[!UICONTROL ef_id_instances]「 」指標 ( [!UICONTROL AMO ID Instances]:

```
Clicks to [EF ID Instances = (ef_id_instances / Clicks)
```

AMO ID と EF ID の間で高い一致率が予想されますが、AMO ID と EF ID は基本的に異なるデータを追跡するので、100%のパリティは想定しないでください。この違いにより、合計の差がわずかに生じる可能性があります [!UICONTROL AMO ID Instances] および [!UICONTROL EF ID Instances]. 合計 [!UICONTROL AMO ID Instances] in [!DNL Analytics] ～とは異なる [!UICONTROL EF ID Instances] ただし、Adobe Advertisingに 1%以上の割合がある場合は、Adobeのアカウントチームにお問い合わせください。

AMO ID と EF ID について詳しくは、 [Analytics で使用されるAdobe AdvertisingID](ids.md).

以下は、インスタンスに対するクリック数を追跡するワークスペースの例です。

![インスタンスに対するクリック数を追跡するワークスペースの例](/help/integrations/assets/a4adc-clicks-to-instances-example.png)

## でのデータセットの比較 [!DNL Analytics for Advertising] とのAdobe Advertising

The [AMO ID](ids.md) （s_kwcid クエリー文字列パラメーター）は、 [!DNL Analytics]、および [EF ID](ids.md) は、Adobe Advertisingのレポートに使用されます。 異なる値なので、1 つの値が破損しているか、ランディングページに追加されていない可能性があります。

例えば、次のランディングページがあるとします。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id
```

ここで、EF ID は「`test_ef_id`」と入力し、AMO ID は「`test_amo_id`.&quot;

サイト側のリダイレクトが発生した場合、URL は次のようになります。

```
www.adobe.com/?ef_id=test_ef_id&s_kwcid=test_amo_id#redirectAnchorTag
```

ここで、EF ID は「`test_ef_id`」と入力し、AMO ID は「`test_amo_id#redirectAnchorTag`.&quot;

この例では、アンカータグを追加すると、AMO ID に予期しない文字が追加されるので、Analytics では値を認識できません。 この AMO ID は分類されず、関連付けられたコンバージョンは「[!UICONTROL unspecified]&quot;または&quot;[!UICONTROL none]」内 [!DNL Analytics] レポート。

幸いにも、このような問題は一般的ですが、一般的には大きな相違は生じません。 ただし、 [!DNL Analytics] および EF ID をAdobe Advertisingで使用する場合は、Adobeアカウントチームにお問い合わせください。

## その他の指標に関する考慮事項

### クリック数と訪問数の違い {#clicks-vs-visits}

これらは似ているようですが、クリック数と訪問数は異なるデータを表します。

* **クリック：** [!DNL DSP] または、訪問者が投稿者の Web サイトで広告をクリックした場合に、クリックが記録されます。

* **訪問：** [!DNL Analytics] を定義します。 [訪問](https://experienceleague.adobe.com/docs/analytics/components/metrics/visits.html) を使用して、30 分間の無操作状態など、いくつかの条件のいずれかに従って終了する一連のページビュー数として指定できます。

定義によると、1 回のクリックで複数の訪問が発生する場合があります。

次の例を考えてみましょう。ユーザー 1 とユーザー 2 の両方が、Adobe Advertising広告をクリックしてサイトにアクセスします。 ユーザー 1 は 4 つのページを表示し、その日を退出したので、最初のクリックは 1 回の訪問になります。 ユーザー 2 は、2 つのページを表示し、45 分のランチを終了し、戻り、さらに 2 つのページを表示し、その後離れます。この場合、最初のクリックは、2 回の訪問となります。

![クリック数と訪問数の違いの例](/help/integrations/assets/a4adc-visits-example.png)

### クリック数とクリックスルー数の違い

<!-- Rob to let me know if we should remove this and add more info. to the section on AMO Instances etc. -->

クリック数とクリックスルー数は、次の 2 つの異なる指標です。

* **クリック：** [!DNL DSP] または、訪問者が投稿者の Web サイトで広告をクリックした場合に、クリックが記録されます。

* **クリックスルー：** [!DNL Analytics] は、訪問者が宛先 Web サイトに到着したときのクリックスルーを記録し、ランディングページが読み込まれて、 [!DNL Analytics] ページ下部のリクエストは、データをに送信します。 [!DNL Analytics].

誤った広告クリック数のため、クリック数とクリックスルー数は大きく異なる場合があります。 ディスプレイ広告でのほとんどのクリックは誤ってクリックされるもので、これらの誤って訪問者がランディングページを読み込む前に「戻る」ボタンを押したことがわかっています。 [!DNL Analytics] クリックスルーを記録できない。 これは特に、モバイル広告、ビデオ広告、広告など、誤ってクリックした可能性が高い広告で特に当てはまります。広告は、画面を埋め、ユーザーがページを表示する前に閉じる必要があります。

また、モバイルデバイスに読み込まれたサイトでは、帯域幅が低く処理能力が高く、ランディングページの読み込みに時間がかかるので、クリックスルーが発生する可能性が低くなります。 50 ～ 70%のクリックがクリックスルーにつながらないことは珍しくありません。 モバイル環境では、差が 90%まで高くなる可能性があります。これは、ブラウザーの速度が遅くなると、ページをスクロールしたり広告を閉じようとしたときにユーザーが誤って広告をクリックする可能性が高くなるからです。

クリックデータは、現在の追跡メカニズム（モバイルアプリに送信されるクリック数、モバイルアプリからのクリック数など）でクリックスルーを記録できない環境や、広告主が 1 つの追跡手法のみを導入した環境（JavaScript のビュースルー手法では、サードパーティ cookie をブロックするブラウザー）でも記録できます。 Adobeがクリック URL の追跡とビュースルー JavaScript の追跡の両方の方法をデプロイすることを推奨する主な理由は、追跡可能なクリックスルーを最大限に活用できるようにすることです。

### Adobe Advertising以外のDimensionでのAdobe Advertisingトラフィック指標の使用

Adobe Advertisingは、Analytics に [広告固有のトラフィック指標および関連ディメンション [!DNL DSP] および [!DNL Search, Social, & Commerce]](advertising-metrics-in-analytics.md). Adobe Advertisingが提供する指標は、指定したAdobe Advertisingのディメンションにのみ適用でき、また、 [!DNL Analytics].

例えば、 [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] Adobe Advertising別の指標（指標ディメンション）を選択すると、合計が表示されます [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] アカウント別。

![Adobe Advertisingディメンションを使用したレポート内のAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-supported-dimension.png)

ただし、 [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] 指標をページ上のディメンション（ページなど）で指定し、Adobe Advertisingがデータを提供しない場合は、 [!UICONTROL Adobe Advertising Clicks] および [!UICONTROL Adobe Advertising Cost] 各ページの値は、0（ゼロ）です。

![サポートされていないディメンションを使用するレポート内のAdobe Advertising指標の例](/help/integrations/assets/a4adc-traffic-unsupported-dimension.png)

### 使用 [!UICONTROL AMO ID Instances] 非Adobe AdvertisingDimensionでのクリック数の代わりとして

を使用できないので、 [!UICONTROL Adobe Advertising Clicks] オンサイトディメンションを使用すると、クリック数に相当するものを見つけることができます。 訪問回数を代わりに使用したいと考えるかもしれませんが、各訪問者が複数回訪問する場合があるので、これらは最適な選択肢ではありません。 (「[クリック数と訪問数の違い](#clicks-vs-visits).&quot; 代わりに、 [!UICONTROL AMO ID Instances]:AMO ID が取得された回数です。 While [!UICONTROL AMO ID Instances] 一致しない [!UICONTROL Adobe Advertising Clicks] 正確には、これらはサイトでのクリックトラフィックを測定する最適なオプションです。 詳しくは、[のデータ検証 [!DNL Analytics for Advertising]](#data-validation).&quot;

![の例 [!UICONTROL AMO ID Instances] の代わりに [!UICONTROL Adobe Advertising Clicks] サポートされていないディメンションの](/help/integrations/assets/a4adc-amo-id-instances.png)

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [Analysis WorkspaceのAdobe Advertising指標](/help/integrations/analytics/advertising-metrics-in-analytics.md)
>* [[!DNL Analytics] データのAdobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
>* [Adobe Advertisingと [!DNL Marketing Channels]](/help/integrations/analytics/marketing-channels/mc-data-variances.md)
