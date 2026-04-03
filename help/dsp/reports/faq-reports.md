---
title: カスタムレポートに関するFAQ
description: 世帯レポートやコンバージョンパス分析レポートなど、カスタムレポートについて詳しく説明します。
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
TQID: https://experienceleague.adobe.com/3AN4vKu3BF-c4jwMusI402Z7lTLY0Nf30uwLZWBUE1E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1170
ht-degree: 0%

---

# カスタムレポートに関するFAQ

## 世帯レポート

### [!UICONTROL Household Reach & Frequency] レポート

#### [!UICONTROL Household Reach & Frequency] レポートは他のカスタムレポートとどのように異なりますか？

[!UICONTROL Household Reach & Frequency] レポートは、IP アドレスに基づいて、様々なディメンションのリーチ、インプレッション、頻度を世帯レベルで測定します。 その他のカスタムレポートは、デバイスレベルまたはCookie レベルで生成されます。

たとえば、1つのインプレッションが1世帯内の3つのデバイスに提供される場合でも、「ユニーク世帯到達数」指標は1です。

##### サポートされているディメンション

[!UICONTROL Household Reach & Frequency] レポートでは、「[次のディメンション &#x200B;](/help/dsp/reports/report-columns.md): &quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]&quot; （重複する指標へのアクセス権を提供しません）、&quot;[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length]&quot;、ユーザー作成のプレースメント &quot;[!UICONTROL Tags]&quot;がサポートされています。

##### サポートされる指標

使用可能な指標[は次のとおりです。](/help/dsp/reports/report-columns.md)

* 重複指標：[!UICONTROL Frequency Overlap]、[!UICONTROL Measurable Impressions (Overlap)]、[!UICONTROL Unique Household (Overlap)]。

  重なり指標は、レポートされるディメンションまたはディメンションの組み合わせに対してのみ発生する値で、他のディメンションに対しては発生しません。<!-- For example, it might show the ?? -->

* 重複のない指標：[!UICONTROL Frequency]、[!UICONTROL Incremental Household Reached]、[!UICONTROL % Incremental Household Reached]、[!UICONTROL Impressions]、[!UICONTROL Measurable Impressions]および[!UICONTROL Unique Household Reached]

コンバージョン指標とカスタム目標はサポートされていません。

#### 重複指標と非重複指標の違いは何ですか？

次の図は、3つのキャンペーン（A、B、C）の3つの指標（ユニーク世帯リーチ、増分世帯リーチ、増分世帯（重複））を示しています。

![世帯の重複指標のイラストレーション &#x200B;](/help/dsp/assets/household-overlap-metrics-illustration.png "世帯の重複指標のイラストレーション ")

* ユニーク世帯到達数（合計）は、各キャンペーンで到達したユニーク世帯または各サークルの合計面積を提供します。 図では、Aがリーチしたユニーク世帯= A + （A+B） + （A+C） + （A+B+C）がリーチした増分世帯

* Incremental Household Reachedは、キャンペーンによってのみリーチされたユニーク世帯です。 図では、A、B、Cがリーチした増分世帯は、それぞれA、B、Cがリーチした増分世帯です。

* 増分世帯（重複）とは、キャンペーンまたはキャンペーンの組み合わせによってリーチしたユニーク世帯のことです。 図では、Aが到達した増分世帯、CはA+Cです。

#### ワークフロー

[&#x200B; カスタムレポートを作成するには、通常の手順に従います](report-create.md)。

[!UICONTROL Household Reach & Frequency] レポートには、1つのディメンションのみを含めることができます。 また、サイト/アプリを除く任意のディメンションによるa）重複指標またはb）重複以外の指標を含めることもできますが、両方を含めることはできません。

#### [!UICONTROL Household Reach & Frequency] レポートの制限事項を教えてください。

重なり指標を含むレポートでは、最大3つの値の積集合が出力されます。 例えば、10件の配置に対して指標[!UICONTROL Unique Household (Overlap)]を使用すると、個々の配置で到達したユニーク世帯、任意の2つの配置の組み合わせで到達した一般的な世帯、および任意の3つの配置の組み合わせで到達した一般的な世帯を確認できます。 4つ以上のプレースメントに達した一般的な世帯を表示することはできません。

キャンペーン、パッケージまたはプレースメント以外のディメンションの場合、各ディメンションで最大10個の値をサポートします。 例えば、[!UICONTROL Unique Household Reached] ディメンションの[!UICONTROL Audience] レポートを生成するには、一意のオーディエンスの数が10個以下である必要があります。 10個を超える固有オーディエンスを含めると、空白のレポートが生成されます。

#### [!UICONTROL Custom] レポートと[!UICONTROL Household Reach & Frequency] レポートの間で、頻度と一意のリーチ値が異なるのはなぜですか？

[!UICONTROL Household] レポートのこれらの指標は、実際のIP アドレス数を使用して計算されますが、[!UICONTROL Custom] レポートの指標は、モデルを使用して計算された推定値を使用します。 ただし、その差は10%未満である必要があります。

#### [!UICONTROL Placement Tags] ディメンションのレポートを設定するにはどうすればよいですか？

プレースメントのタグを作成するには、[&#x200B; プレースメント設定](/help/dsp/campaign-management/placements/placement-edit.md)を開き、[[!UICONTROL Placement Tags] フィールド &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)に値を入力します。

プレースメントに複数のタグが含まれている場合、レポートでは文字列全体が1つのタグと見なされます。 レポートには、一意の文字列ごとに1行が含まれます。

### [!UICONTROL Household Conversions] レポート

#### [!UICONTROL Household Conversions] レポートでサポートされているアトリビューション方法はどれですか？

次の2種類のアトリビューション方法がサポートされています。

* [!UICONTROL Unique]: ディメンション値（デバイスやプレースメントなど）がコンバージョンに至るまでのパス上にある回数をカウントします。

* [!UICONTROL Multi-Touch Attribution (MTA)]: コンバージョンへのパス上のディメンション値（デバイスやプレースメントなど）の発生頻度に基づいて、各コンバージョンのクレジットを分配します。 例えば、コンバージョンまでにCTVで8つ、モバイルで2つの、合計10のインプレッションがあった場合、クレジット（0.8）はCTV スクリーン、0.2はモバイルに割り当てられます。

#### 世帯のコンバージョンレポートは、Adobe AnalyticsのCTV ビュースルーレポートとどのように異なりますか？

* [!DNL Analytics]では、[!DNL CTV View-Through Conversion] レポートには、CTV インプレッションがコンバージョン前の最後のタッチポイントであったコンバージョンの数が表示されます。 対照的に、DSP [!UICONTROL Household Conversions] レポートは、コンバージョン前に定義されたルックバックウィンドウ内の任意の時点でCTV インプレッションにさらされたユニーク世帯の数を示します。

* [!DNL Analytics]では、アトリビューションロジックにより、Adobe Advertisingの最後のタッチポイントにのみコンバージョンが割り当てられます。 対照的に、DSP [!UICONTROL Household Conversions] レポートでは、*[!UICONTROL Unique]*&#x200B;と&#x200B;*[!UICONTROL Multi-Touch Attribution (MTA)]*&#x200B;のアトリビューションモデルがサポートされています。

* [!DNL Analytics]件のレポートデータは、マーケティングチャネルやサイトエンゲージメント指標などで分析するのに特に価値があります。 DSP [!UICONTROL Household Conversions] レポートでは、コンバージョンデータをメディアタイプやパブリッシャーなどのさまざまなディメンションで分割できるようにすることで、より詳細なインサイトを提供します。

### [!UICONTROL Household Reach & Frequency]および[!UICONTROL Household Conversions]件のレポートと[!DNL Advanced Measurement Services]件のデータの比較

世帯ベースのリーチと頻度またはコンバージョンに関する高度なレポートを作成するために、[[!DNL Strategic Advertising Consulting]  チーム &#x200B;](/help/dsp/introduction/advanced-measurement-services.md)は、高度にカスタマイズ可能なレポートと包括的な戦略的レコメンデーションを提供できます。 [!DNL Advanced Measurement Services]の詳細については、Adobe アカウント チームにお問い合わせください。

#### 既に[!DNL Advanced Measurement Services]を使用している場合、[!UICONTROL Household Reach & Frequency]と[!UICONTROL Household Conversions]のレポートを使用する必要があるのはなぜですか？

[!UICONTROL Household Reach & Frequency] レポートと[!UICONTROL Household Conversions] レポートは、各世帯レベルのリーチ、頻度、およびコンバージョンの指標をリアルタイムで自律的に引き出すためにクライアントを支援します。

#### [!UICONTROL Household Reach & Frequency]と[!UICONTROL Household Conversions]の両方のレポートと[!DNL Advanced Measurement Services]を使用できますか？

理想的な使用例は、[!UICONTROL Household] レポートと[!DNL Advanced Measurement Services] レポートおよびコンサルティング サービスの両方を一緒に使用することです。 [!UICONTROL Household]報告書は取引関係で、日々の最適化に役立てることを目的とし、[!DNL Advanced Measurement Services]はより戦略的で、全体的なビジネス目標に関連する全体的な知見と教訓を伝えることを目的としていると考えてください。

## コンバージョンパス分析レポート

### [!UICONTROL Path to Conversion] レポートは、[!DNL Advanced Measurement Services]およびAdobe Analytics Analysis Workspaceで作成されたレポートとどのように比較されますか？

| | [!UICONTROL Path to Conversion] レポート | 高度な測定サービスによる検索レポートへのハロー効果 | Analysis Workspaceのレポート |
| --- | --- | --- |---|
| 顧客価値と | セルフサービスのカスタムレポートを生成し、広告ジャーニーのどの経路がより多くのコンバージョンにつながったのかを把握して、最適化を促進します | コネクテッド TV （CTV）戦略が検索クリックに与える影響を把握する | 包括的なAdobe Adobe Advertisingへの投資が、他のマーケティングチャネルとともに検索クリックに与える影響を把握しましょう |
| 世帯レベル | はい | はい | いいえ |
| CTVはサポートされていますか？ | はい | はい | はい |
| アトリビューション手法 | ラストタッチイベント（インプレッションまたはクリック）は、ルックブックウィンドウ内に存在する必要があります。 | ユニーク | ラストタッチ |
| | コンバージョンパスでは、ラストタッチイベントの30日以上前のインタラクションポイントが考慮されます。 | （CTVは、ユーザーのクリックパスのどこでCTV露出が発生したかにかかわらず、クレジットを受け取ります） | （インプレッションがルックバックウィンドウの最後のイベントであり、CTV露出の前または後に他の形式からの有料クリックがない場合、CTVはクレジットを取得します） |
| レポートのレベル | Granular | Granular | 幅広い |
| | （チャネルタイプ、Creative/広告、キーワード、パス、長さ、コンバージョンまでの時間） | （CTV Tactic, CTV App/Publisher） | （Adobe Advertisingなどのマーケティングチャネル） |
| マーケティングチャネル | DSP +検索（検索、ソーシャル、Commerceから） | DSP +検索（検索、ソーシャル、Commerceから） | Adobe AdvertisingのクリックスルーEF IDで追跡されないマーケティングチャネル（オーガニック検索、オーガニックソーシャル、電子メール、アフィリエイトなど） |
| コンバージョン指標のサポート | Adobe Advertising イベントピクセル（AMO ID）とAdobe Analytics トラッキングを使用してトラッキングされる指標 | クリック数（コンバージョンなし） | Adobe Analytics トラッキングを使用して追跡された指標 |

検索レポートでの高度な測定サービスのハロー効果について詳しくは、「[高度な測定ソリューション &#x200B;](/help/dsp/introduction/advanced-measurement-services.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [&#x200B; カスタムレポートを作成](/help/dsp/reports/report-create.md)
>* [&#x200B; カスタムレポートを編集](/help/dsp/reports/report-edit.md)
>* [&#x200B; カスタムレポート設定](/help/dsp/reports/report-settings.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
