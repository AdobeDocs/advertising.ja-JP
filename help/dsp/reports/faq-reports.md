---
title: カスタムレポートに関する FAQ
description: 世帯レポートやコンバージョンパス分析レポートなどのカスタムレポートについて詳しく説明します。
exl-id: 3ffd178e-de41-4663-b85f-bd8ce3eb0dad
source-git-commit: a1ece707f43af4a6a3fc5573e41c75622f9b502f
workflow-type: tm+mt
source-wordcount: '1178'
ht-degree: 0%

---

# カスタムレポートに関する FAQ

## Household Reports

### [!UICONTROL Household Reach & Frequency] レポート

#### [!UICONTROL Household Reach & Frequency] レポートと他のカスタムレポートの違いは何ですか？

[!UICONTROL Household Reach & Frequency] のレポートでは、IP アドレスに基づいて、様々なディメンションをまたいだリーチ、インプレッションおよび頻度を世帯レベルで測定します。 その他のカスタムレポートは、デバイスレベルまたは cookie レベルで生成されます。

例えば、1 つのインプレッションが 1 つの家庭内の 3 つのデバイスに提供された場合でも、到達した世帯のユニーク数指標は 1 です。

##### サポートされるディメンション

[!UICONTROL Household Reach & Frequency] レポートは、[&#128279;](/help/dsp/reports/report-columns.md)」、「[!UICONTROL Campaign]」、「[!UICONTROL Package]」、「[!UICONTROL Placement]」（重複指標へのアクセスを提供しない）、「[!UICONTROL Site/Apps]」、「[!UICONTROL Media Type]」、「[!UICONTROL Feed Type]」、「[!UICONTROL Device]」、「[!UICONTROL Publisher]」、「[!UICONTROL Audience]」およびユーザー作成のプレースメント「[!UICONTROL Creative Length]」をサポートします [!UICONTROL Tags]。 |

##### サポートされる指標

[&#x200B; 使用可能な指標 &#x200B;](/help/dsp/reports/report-columns.md) は次のとおりです。

* 重複指標：[!UICONTROL Frequency Overlap]、[!UICONTROL Measurable Impressions (Overlap)]、[!UICONTROL Unique Household (Overlap)]。

  重複指標とは、レポートされたディメンションまたはディメンションの組み合わせに対してのみ発生し、他のディメンションに対しては発生しない値のことです。<!-- For example, it might show the ?? -->

* 重複以外の指標：[!UICONTROL Frequency]、[!UICONTROL Incremental Household Reached]、[!UICONTROL % Incremental Household Reached]、[!UICONTROL Impressions]、[!UICONTROL Measurable Impressions] および [!UICONTROL Unique Household Reached]

コンバージョン指標とカスタム目標はサポートされていません。

#### 重複指標と重複以外の指標の違いは何ですか？

次の図は、3 つのキャンペーン（A、B、C）の 3 つの指標（ユニーク世帯、達した世帯の増分、世帯の増分（重複））を示しています。

![&#x200B; 世帯オーバーラップ指標の図 &#x200B;](/help/dsp/assets/household-overlap-metrics-illustration.png " 世帯オーバーラップ指標の図 ")

* ユニーク世帯リーチ（合計）は、各キャンペーンでリーチしたユニーク世帯または各サークルの合計面積を提供します。 次の図では、A によって達成された一意の世帯=A + （A+B） + （A+C） + （A+B+C）によって達成された増分世帯

* 到達した世帯の増分は、キャンペーンによってのみ到達した一意の世帯です。 図の A、B、C の累乗世帯は、それぞれ A、B、C の累乗世帯です。

* 増分世帯（重複）は、キャンペーンまたはキャンペーンの組み合わせによって達成された一意の世帯です。 図では、A、C によって達成された増分世帯は A+C です。

#### ワークフロー

通常の手順に従って [&#x200B; カスタムレポートを作成 &#x200B;](report-create.md) します。

[!UICONTROL Household Reach & Frequency] レポートには、ディメンションを 1 つだけ含めることができます。 また、a） サイト/アプリを除く任意のディメンションによる重複指標、または b）重複以外の指標を含めることもできますが、両方を含めることはできません。

#### [!UICONTROL Household Reach & Frequency] レポートの制限事項は何ですか。

重複指標を持つレポートでは、最大 3 つの値の交差が出力されます。 例えば、10 個のプレースメントに対して指標 [!UICONTROL Unique Household (Overlap)] を使用すると、個々のプレースメントによって到達した一意の世帯、2 つのプレースメントの組み合わせによって到達した一般的な世帯、3 つのプレースメントの組み合わせによって到達した一般的な世帯を確認できます。 4 つ以上のプレースメントによって到達した一般的な世帯は表示されません。

キャンペーン、パッケージまたは配置以外のディメンションの場合、レポートでは各ディメンションで最大 10 個の値がサポートされます。 例えば、[!UICONTROL Unique Household Reached] ディメンションの [!UICONTROL Audience] レポートを生成するには、ユニークオーディエンスの数を 10 以下にする必要があります。 10 を超える一意のオーディエンスを含める場合は、空のレポートが生成されます。

#### [!UICONTROL Custom] レポートと [!UICONTROL Household Reach & Frequency] レポートで頻度とユニークなリーチ値が異なるのはなぜですか？

これらのレポートの指標は、実際の IP アドレス数を使用して計算されます。一方、[!UICONTROL Household] のレポートの指標は、モデルを使用して計算された推定数を使用 [!UICONTROL Custom] ます。 ただし、その不一致は 10% 未満にする必要があります。

#### [!UICONTROL Placement Tags] ディメンションのレポートを設定するにはどうすればよいですか？

プレースメントのタグを作成するには、[&#x200B; プレースメント設定を開き &#x200B;](/help/dsp/campaign-management/placements/placement-edit.md) [&#x200B; プレースメント タグ フィールド &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md) に値を入力します。

プレースメントに複数のタグが含まれる場合、レポートは文字列全体を 1 つのタグと見なします。 レポートには、一意の文字列ごとに 1 行が含まれます。

### [!UICONTROL Household Conversions] レポート

#### レポートでサポートされているアトリビューショ [!UICONTROL Household Conversions] メソッドはどれですか？

次の 2 種類のアトリビューションメソッドがサポートされています。

* [!UICONTROL Unique]：ディメンション値（デバイスや配置など）がコンバージョンへのパス上にあった回数をカウントします。

* [!UICONTROL Multi-Touch Attribution (MTA)]：コンバージョンへのパス上でのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV に 8 件、モバイルに 2 件あった場合、クレジットの 80% （0.8）が CTV 画面に、0.2 がモバイルに与えられます。

#### 世帯コンバージョンレポートとAdobe Analyticsの CTV ビュースルーレポートの違い

* ま [!DNL Analytics]、[!DNL CTV View-Through Conversion] レポートは、CTV インプレッションがコンバージョン前の最後のタッチポイントであったコンバージョンの数を示します。 これに対し、DSP [!UICONTROL Household Conversions] レポートは、コンバージョン前に定義されたルックバックウィンドウ内の任意の時点で CTV インプレッションの対象となったユニーク世帯数を示します。

* ま [!DNL Analytics]、アトリビューションロジックは、Adobe Advertisingの最後のタッチポイントにのみコンバージョンを割り当てます。 これに対し、DSP [!UICONTROL Household Conversions] レポートでは、追加のアトリビューションモデル（*[!UICONTROL Unique]* および *[!UICONTROL Multi-Touch Attribution (MTA)]*）がサポートされます。

* レポートデータ [!DNL Analytics]、マーケティングチャネル別やサイトエンゲージメント指標別などに分析する際に特に役立ちます。 DSP [!UICONTROL Household Conversions] レポートでは、コンバージョンデータをメディアタイプやパブリッシャーなどの様々なディメンションで分割できるので、より詳細なインサイトが得られます。

### [!UICONTROL Household Reach & Frequency] および [!UICONTROL Household Conversions] レポートと [!DNL Advanced Measurement Services] のデータの比較

世帯ベースのリーチと頻度またはコンバージョンに関する高度なレポートについて、[[!DNL Strategic Advertising Consulting]  チーム &#x200B;](/help/dsp/introduction/advanced-measurement-services.md) は、全体的な戦略的レコメンデーションに加えて、カスタマイズ性の高いレポートを提供できます。 [!DNL Advanced Measurement Services] について詳しくは、Adobe アカウントチームにお問い合わせください。

#### 既に [!DNL Advanced Measurement Services] を使用している場合、[!UICONTROL Household Reach & Frequency] レポートと [!UICONTROL Household Conversions] レポートを使用する必要があるのはなぜですか？

[!UICONTROL Household Reach & Frequency] レポートと [!UICONTROL Household Conversions] レポートを使用すると、クライアントは、世帯レベルのリーチ、頻度、コンバージョン指標をそれぞれ自律的にリアルタイムで取り込むことができます。

#### [!UICONTROL Household Reach & Frequency] と [!UICONTROL Household Conversions] の両方のレポートと [!DNL Advanced Measurement Services] を使用できますか？

理想的なユースケースは、[!UICONTROL Household] レポートと、[!DNL Advanced Measurement Services] のレポートサービスおよびコンサルティングサービスの両方を一緒に使用することです。 [!UICONTROL Household] レポートをトランザクションとして考え、日々の最適化に情報を提供することを目的とし、より戦略的な [!DNL Advanced Measurement Services] めに、包括的なビジネス目標に関連する総合的な知識や留意点を提供することを目的としています。

## コンバージョンパス分析レポート

### コンバージョンレポートのパスは、[!DNL Advanced Measurement Services] およびAdobe Analytics Analysis Workspaceで作成されたレポートと比較してどうですか？

| | コンバージョンレポートのパス | 検索レポートに対する Advanced Measurement Services のハロー効果 | Analysis Workspaceのレポート |
| --- | --- | --- |---|
| 顧客価値 | セルフサービスのカスタムレポートを生成して、広告ジャーニーのどのパスが最適化を高めるためにより多くのコンバージョンにつながったかを把握します | 検索クリックに対するコネクテッド TV （CTV）戦術の影響を理解します | 検索クリックに対するAdobe Advertisingの総合的な投資が、他のマーケティングチャネルと共に与える影響を理解します |
| 世帯レベル | はい | はい | 不可 |
| CTV はサポートされていますか？ | はい | はい | はい |
| アトリビューション手法 | ラストタッチイベント（インプレッションまたはクリック）は、ルックブックウィンドウ内に配置する必要があります。 | ユニーク | ラストタッチ |
| | コンバージョンパスに対して、ラストタッチイベントの 30 日以上前のインタラクションポイントが考慮されます。 | （CTV は、ユーザーのクリック経路で CTV エクスポージャーが発生した場所に関係なく、クレジットを受け取ります） | （インプレッションがルックバックウィンドウの最後のイベントであり、CTV 公開の前または後に他のフォーマットからの有料クリックがない場合、CTV はクレジットを受け取ります） |
| レポートのレベル | 粒状 | 粒状 | 広い |
| | （チャネルタイプ、Creative/Ad、キーワード、パス、長さ、コンバージョンまでの時間） | （CTV 戦略、CTV アプリ/パブリッシャー） | （Adobe Advertisingおよびその他のマーケティングチャネル） |
| マーケティングチャネル | DSP +検索（検索、ソーシャル、Commerceから） | DSP +検索（検索、ソーシャル、Commerceから） | Adobe Advertisingのクリックスルー EF ID でトラッキングされないマーケティングチャネル（オーガニック検索、オーガニックソーシャル、メール、アフィリエイトなど） |
| サポートされるコンバージョン指標 | Adobe Advertising イベントピクセル（AMO ID）およびAdobe Analytics トラッキングを使用してトラッキングされる指標 | クリック数（コンバージョンなし） | Adobe Analyticsのトラッキングを使用して追跡される指標 |

Advanced Measurement Services の検索レポートへのハロー効果について詳しくは、「[Advanced Measurement Services](/help/dsp/introduction/advanced-measurement-services.md)」を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムレポートについて &#x200B;](/help/dsp/reports/report-about.md)
>* [&#x200B; カスタムレポートの作成 &#x200B;](/help/dsp/reports/report-create.md)
>* [&#x200B; カスタムレポートの編集 &#x200B;](/help/dsp/reports/report-edit.md)
>* [&#x200B; カスタムレポートの設定 &#x200B;](/help/dsp/reports/report-settings.md)
>* [&#x200B; 使用可能なレポート列 &#x200B;](/help/dsp/reports/report-columns.md)
