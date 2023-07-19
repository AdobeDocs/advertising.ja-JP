---
title: 世帯レポートに関する FAQ
description: レポートデータに関する詳細情報 ( [!UICONTROL Household] レポートは他のレポートやトラブルシューティングとは異なります。
exl-id: aaaf6f6d-b133-4cda-8fc6-bd686b3b1ebb
source-git-commit: 05f7d9c7a120828bda46d4f79796dfb419cca242
workflow-type: tm+mt
source-wordcount: '907'
ht-degree: 0%

---

# 世帯レポートに関する FAQ

## この [!UICONTROL Household Reach & Frequency] レポート

### 機能 [!UICONTROL Household Reach & Frequency] 他のカスタムレポートとは異なるレポートを表示するか。

この [!UICONTROL Household Reach & Frequency] レポートは、IP アドレスに基づいて、世帯レベルで、様々なディメンションにわたるリーチ、インプレッション、頻度を測定します。 その他のカスタムレポートは、デバイスまたは cookie レベルで生成されます。

例えば、1 つのインプレッションが 1 世帯内の 3 つのデバイスに提供された場合でも、ユニーク世帯到達指標は 1 です。

#### サポートされるDimension

この [!UICONTROL Household Reach & Frequency] レポートは [次の寸法](/help/dsp/reports/report-columns.md):&quot;[!UICONTROL Campaign],&quot; &quot;[!UICONTROL Package],&quot; &quot;[!UICONTROL Placement],&quot; &quot;[!UICONTROL Site/Apps]」（重複指標へのアクセスを提供しない）[!UICONTROL Media Type],&quot; &quot;[!UICONTROL Feed Type],&quot; &quot;[!UICONTROL Device],&quot; &quot;[!UICONTROL Publisher],&quot; &quot;[!UICONTROL Audience],&quot; &quot;[!UICONTROL Creative Length],」およびユーザー作成の配置&quot;[!UICONTROL Tags].&quot; |

#### サポートされる指標

この [利用可能な指標](/help/dsp/reports/report-columns.md) 次を含む：

* 重複指標： [!UICONTROL Frequency Overlap], [!UICONTROL Measurable Impressions (Overlap)]、および [!UICONTROL Unique Household (Overlap)].

  重複指標は、レポートされたディメンションまたはディメンションの組み合わせに対してのみ発生する値で、他のディメンションに対して発生する値ではありません。 <!-- For example, it might show the ?? -->

* 重複しない指標： [!UICONTROL Frequency], [!UICONTROL Incremental Household Reached], [!UICONTROL % Incremental Household Reached], [!UICONTROL Impressions], [!UICONTROL Measurable Impressions]、および [!UICONTROL Unique Household Reached]

コンバージョン指標とカスタム目標はサポートされていません。

### 重複指標と非重複指標の違いは何ですか？

次の図は、3 つのキャンペーン (A、B、C) の 3 つの指標 ( ユニーク世帯到達、増分世帯到達、増分世帯増分世帯（重複）) を示しています。

![世帯間重複指標の図](/help/dsp/assets/household-overlap-metrics-illustration.png "世帯間重複指標の図")

* Unique Household Reached (Total) は、各キャンペーンが到達したユニーク世帯、または各サークルの合計領域を示します。 図では、A が達成したユニーク世帯= A + (A+B) + (A+C) +(A+B+C) が達成した増分世帯

* 「Incremental Household Reached」は、キャンペーンでのみ到達されたユニーク世帯です。 図では、A、B、C が到達した増分世帯は、それぞれ A、B、C が到達した増分世帯です。

* 増分世帯（重複）は、キャンペーンまたはキャンペーンの組み合わせで到達した個別世帯です。 図では、A が到達した増分世帯は、C は A+C です。

### ワークフロー

通常の手順に従って、 [カスタムレポートの作成](report-create.md).

この [!UICONTROL Household Reach & Frequency] レポートに含めることができるディメンションは 1 つだけです。 また、a) サイト/アプリを除く任意のディメンションによる重複指標または b) 重複しない指標のどちらかを含めることもできますが、両方を含めることはできません。

### のいくつかの制限事項 [!UICONTROL Household Reach & Frequency] レポート？

重複指標を持つレポートは、最大 3 つの値の交差を出力します。 例えば、 [!UICONTROL Unique Household (Overlap)] 10 個の配置の場合、個々の配置で達した個別の世帯、2 つの配置の組み合わせで達した共通の世帯、3 つの配置の組み合わせで達した共通の世帯が表示されます。 4 つ以上の配置によってリーチされた一般的な世帯は表示されません。

キャンペーン、パッケージ、配置以外のディメンションの場合、レポートは各ディメンションで最大 10 個の値をサポートします。 例えば、 [!UICONTROL Unique Household Reached] レポート [!UICONTROL Audience] ディメンションに値を指定する場合、一意のオーディエンスの数は 10 以下にする必要があります。 10 を超える個別オーディエンスを含めると、空のレポートが生成されます。

### 頻度とユニークリーチの値が [!UICONTROL Custom] レポートおよび [!UICONTROL Household Reach & Frequency] レポート？

以下の指標： [!UICONTROL Household] レポートは、実際の IP アドレス数を使用して計算されますが、 [!UICONTROL Custom] レポートでは、モデルを使用して計算された推定数値が使用されます。 しかし、食い違いは 10%未満であるはずです。

### レポートを [!UICONTROL Placement Tags] ディメンション？

配置のタグを作成するには、次の手順を実行します。 [配置設定を開く](/help/dsp/campaign-management/placements/placement-edit.md) 値を [配置タグフィールド](/help/dsp/campaign-management/placements/placement-settings.md).

配置に複数のタグが含まれる場合、レポートは文字列全体を 1 つのタグと見なします。 レポートには、一意の文字列ごとに 1 行が含まれます。

## この [!UICONTROL Household Conversions] レポート

### でサポートされているアトリビューションメソッドのタイプは何ですか。 [!UICONTROL Household Conversions] レポート？

次の 2 種類のアトリビューションメソッドがサポートされています。

* ユニーク：ディメンション値（デバイスや配置など）がコンバージョンへのパス上にあった回数をカウントします。

* MTA（マルチタッチアトリビューション）:コンバージョンへのパスでのディメンション値（デバイスや配置など）の発生頻度に基づいて、各コンバージョンのクレジットを配分します。 例えば、コンバージョン前に合計 10 件のインプレッションがあり、CTV で 8 件、モバイルで 2 件があった場合、クレジットの 80%(0.8) が CTV 画面に、0.2 がモバイルに割り当てられます。

### 家計コンバージョンレポートは、Adobe Analyticsの CTV ビュースルーレポートとどのように異なりますか。

での CTV ビュースルーデータ [!DNL Analytics] は電源が入っています [!DNL Analytics] トラッキングおよび世帯コンバージョンデータは、Adobe Advertisingコンバージョントラッキングを使用して収集されたデータを使用します。 また、DSPのアトリビューションロジック ( [!DNL Analytics] は最後のイベントのみを使用しますが、世帯コンバージョンレポートは 2 つの異なるアトリビューション方法をサポートします。一意と MTA。

### CTV ビュースルーデータを [!DNL Analytics for Advertising] カスタムレポートで

広告主（なし） [!DNL Analytics for Advertising] は、世帯コンバージョンレポートに対してのみ世帯コンバージョンレポートを使用できます。

組織が [!DNL Analytics for Advertising]を使用する場合は、両方のタイプのレポートを一緒に使用します。 CTV のビュースルーレポートは、幅広いチャネル分析やサイトでの行動などに適していますが、カスタムレポートでは、コンバージョン率を引き起こす要因を示す詳細な情報（メディアタイプ、発行者などで分類されたデータ）が得られます。

## [!UICONTROL Household Reach & Frequency] および [!UICONTROL Household Conversions] レポートとデータの比較 [!DNL Advanced Measurement Services]

世帯ベースのリーチと頻度またはコンバージョンに関する高度なレポートについては、 [[!DNL Strategic Advertising Consulting] チーム](/help/dsp/introduction/advanced-measurement-services.md) では、高度にカスタマイズ可能なレポートを包括的な戦略的推奨事項と共に提供できます。 詳しくは、 [!DNL Advanced Measurement Services]の担当者は、Adobeアカウントチームにお問い合わせください。

### 既に [!DNL Advanced Measurement Services]を使用する理由 [!UICONTROL Household Reach & Frequency] および [!UICONTROL Household Conversions] レポート？

この [!UICONTROL Household Reach & Frequency] および [!UICONTROL Household Conversions] レポートを使用すると、クライアントは、それぞれリアルタイムで自律的に世帯レベルのリーチ指標、頻度指標、コンバージョン指標を引き出すことができます。

### 両方を使用できますか？ [!UICONTROL Household Reach & Frequency] および [!UICONTROL Household Conversions] レポートと [!DNL Advanced Measurement Services]?

理想的な使用例は、 [!UICONTROL Household] レポートおよび [!DNL Advanced Measurement Services] レポートとコンサルティングサービスを一緒に使用する。 次の点を考慮してください。 [!UICONTROL Household] トランザクションとしてレポートし、日々の最適化を導き出し、 [!DNL Advanced Measurement Services] より戦略的で、包括的なビジネス目標に結び付いた総合的な知識と留意点を伝えることを目的としています。

>[!MORELIKETHIS]
>
>* [カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポートの編集](/help/dsp/reports/report-edit.md)
>* [カスタムレポート設定](/help/dsp/reports/report-settings.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
