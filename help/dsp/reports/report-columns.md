---
title: 使用可能なレポート列
description: カスタムレポートで使用可能な列の説明を参照してください。
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: 917441d02d8e8b43911da44e19fcc2b7a64fc301
workflow-type: tm+mt
source-wordcount: '2947'
ht-degree: 0%

---

# 使用可能なレポート列

<!--
 Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

使用可能なレポート列は、レポートタイプによって異なります。 次に、すべてのレポートタイプの列のスーパーセットを示します。

| 指標タイプ | サブタイプ | 列名 | 説明 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | 外部広告サーバーによって割り当てられた広告ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | DSPの広告の一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | ユーザーによって割り当てられた広告の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | 広告のフォーマット。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | 広告の分類は、ユーザーによって変更されるか、日付入力によって示されます：*[!UICONTROL live]*、*[!UICONTROL scheduled]*、*[!UICONTROL completed]*、または&#x200B;*[!UICONTROL archived]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | 広告主の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | キャンペーンにユーザーが割り当てた総予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | キャンペーンの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | DSPのキャンペーンの一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | ユーザーによって割り当てられたキャンペーンの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | キャンペーンの最初の日付。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | コンテンツ/映画タイトル。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | コンテンツシリーズ。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | コンテンツのジャンル： |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | [the [!DNL IAB Technology Laboratory]](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)で定義されている実稼動品質。 値には、`Unknown`、`Professionally Produced`、`Prosumer`または`User Generated`を指定できます。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | [the [!DNL IAB Technology Laboratory]](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md)で定義されているコンテンツのタイプ。 値には、`Video,` `Game`、`Music`、`Application`、`Text`、`Other`または`Unknown`を含めることができます。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | PGやRなどのコンテンツレーティング。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | 広告がライブストリームに表示されたかどうか：`Not Live`または`Live`。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | コンテンツの長さ（秒単位）。通常、ビデオまたはオーディオに使用されます。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | ISO-639-1-alpha-2を使用したコンテンツの言語。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | 年、月、日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | 日[!UICONTROL of Week] | [!UICONTROL Monday]や[!UICONTROL Tuesday]などの特定の日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | 年、月、日、時間。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | 月と年。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | 0 ～ 23の時間です。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | 日曜日から土曜日までの関連する週の日付範囲。 例：2021-02-18 ～ 2021-03-07 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | 広告が表示されたブラウザーのベンダー（GoogleやMozillaなど）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | 広告が表示されたブラウザーのバージョン （[!UICONTROL Safari 4.3]または[!UICONTROL Chrome 7.0]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | 広告が表示されたブラウザー（[!UICONTROL Chrome]または[!UICONTROL Firefox]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Device Environment] | プレースメントがターゲットとするデバイス環境：（*[!UICONTROL Desktop]*、*[!UICONTROL Mobile]*&#x200B;および/または&#x200B;*[!UICONTROL Connected TV]）*。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | 広告が表示されたデバイスの種類（[!UICONTROL Set Top Box]または[!UICONTROL Mobile Phone]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | 広告が表示されたデバイスの製造元（[!UICONTROL Samsung]、[!UICONTROL Lenovo]、または[!UICONTROL Apple]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | 広告が表示されたデバイスのモデル （[!UICONTROL iPhone XS]または[!UICONTROL Galaxy Note 7]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | 広告が表示されたオペレーティングシステムのベンダー（[!UICONTROL Microsoft]または[!UICONTROL Apple]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | 広告が表示されたオペレーティングシステムのバージョン （[!UICONTROL Windows 10]または[!UICONTROL iOS Mojave]など） |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | 広告が表示されたオペレーティング システム （[!UICONTROL Apple iOS]または[!UICONTROL Android]など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | DSPに入力された、取引のユーザー割り当て名。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | 取引が&#x200B;*[!UICONTROL Guaranteed]*&#x200B;か&#x200B;*[!UICONTROL Non-Guaranteed]*&#x200B;かです。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | インベントリの分類：*[!UICONTROL Private]、*、*[!UICONTROL On Demand]、*&#x200B;または&#x200B;*[!UICONTROL Public]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | 外部供給パートナーを介してプライベート取引に割り当てられた一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | インベントリを提供する供給側パートナー。 通常、これはパブリッシャーですが、SSPでもあります。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | メディアの帰属を示すサプライサイドパートナー（SSP）。 |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | 一意のCookieまたはデバイス IDに基づいて、デバイスが広告を受信した回数。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | 報告されたデータの帰属を示す都市。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | 報告されたデータが帰属する国。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | 報告されたデータが帰属する指定市場地域（DMA）。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | 報告されたデータの帰属を示す郵便番号（PIN）コード。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | 報告されたデータの帰属を示す状態。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | オーディエンス： このレポートは最大10の独自オーディエンスをサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | クリエイティブの長さ。 このレポートは、最大10個のクリエイティブな長さをサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | デバイス： このレポートでは、最大10個の一意のデバイスをサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | フィードの種類。 このレポートでは、最大10種類の一意のフィードをサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | メディアタイプ： このレポートでは、最大10種類の固有メディアをサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | 発行者： このレポートでは、最大10社のユニーク媒体企業をサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | パッケージ。<!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | プレースメント。<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | 広告インプレッションが配信されたサイトまたはアプリ。 このレポートは、最大10個の個別のサイトまたはアプリをサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | プレースメントのカスタム IDとして使用されるプレースメントタグ。 このレポートでは、最大10個の一意のプレースメントタグをサポートしています。<!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | オーディエンス： |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | クリエイティブの長さ。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | デバイス： （CTV、デスクトップなど） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | メディアタイプ： （ディスプレイ、オーディオなど） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | 発行者： |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | 配置。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | パッケージフライトの予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | パッケージフライトの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | パッケージフライトの繰り越し予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | パッケージフライトの開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | パッケージの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | パッケージのペーシング目標量。 この金額は、支出またはインプレッションのいずれかになります。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | DSPのパッケージの一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | パッケージの名前 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | パッケージ開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | プレースメント終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | （非推奨）DSPによって従来の[!DNL TubeMogul] コンバージョンイベントに割り当てられたコンバージョン ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | （非推奨）従来の[!DNL TubeMogul]個のコンバージョンイベントに割り当てられたコンバージョン名。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | DSPのプレースメントの一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | ユーザーによって割り当てられたプレースメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | プレースメント予算： |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | プレースメントの最大入札額。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | プレースメント終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | プレースメント開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | プレースメントのカスタム IDとして使用されるプレースメントタグ。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | 請求可能セグメントに関連付けられている説明。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | 請求可能なセグメントに関連付けられた一意のキー。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | 請求可能なセグメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | データプロバイダーが提供するセグメントに関連付けられた説明。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | セグメントに関連付けられた一意のキー。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | セグメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | セグメントに関連付けられているデータプロバイダーの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | DSPのサイトまたはアプリの一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | サイトの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Traffic Type] | 広告が&#x200B;*[!UICONTROL sites]*&#x200B;または&#x200B;*[!UICONTROL Apps]*&#x200B;に表示されたかどうか。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | アップロード後に処理されるビデオの長さ。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | DSPのビデオクリエイティブの一意のID。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | ユーザーによって割り当てられたクリエイティブの名前。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | [!UICONTROL App/Site Distinct Uniques]を[!UICONTROL App/Site Uniques]で割りました。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | このアプリでのみ到達したデバイスの合計数です。 複数のパブリッシャーにまたがる広告に公開されたビューアーは、この値に含まれません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | [!UICONTROL Total Spend]を[!UICONTROL App/Site Distinct Uniques]で割りました。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | [!UICONTROL Total Spend]を[!UICONTROL App/Site Uniques]で割りました。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | 暴露を受けたターゲット世帯ユニバースの推定パーセンテージ。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | ユニークに表示されるインプレッションの平均数。 一部のインベントリでは、パブリッシャーはデバイス識別子を渡さず、これらのインプレッションはこの値に含まれません。 [!UICONTROL Frequency (by App/Site)] レポートには同様の指標がありますが、その指標は推定されていません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | （[!UICONTROL Frequency (by Impression)] レポートに含まれる）特定の頻度ブレークアウトの推定インプレッション数。 DSPの推定値は、インプレッションのサンプルにもとづいています。 一部のインベントリでは、パブリッシャーはデバイス識別子を渡さず、これらのインプレッションはこの値に含まれません。 [!UICONTROL Frequency (by App/Site)] レポートには同様の指標がありますが、その指標は推定されていません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | （[!UICONTROL Frequency (by Impression)] レポートに含まれる）特定の頻度に記録された一意のブラウザーまたはデバイスの数。 DSPの推定値は、インプレッションのサンプルにもとづいています。 一部の在庫では、デバイス IDを渡さないでください。また、これらのインプレッションはこの値に含まれません。 [!UICONTROL Frequency (by App/Site)] レポートには同様の指標がありますが、その指標は推定されていません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | DSP （オークション）が日付範囲内に見たユニーク世帯の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | 人物ベースのクロスデバイス ターゲティングにデバイスグラフを使用した結果として提供されたインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | 1世帯当たりのインプレッション数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | ディメンションの最大3つの値の交差を含め、報告されたディメンションのみで世帯にリーチする頻度。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々のプレースメントで到達した頻度、任意の2つのプレースメントの組み合わせで到達した頻度、および任意の3つのプレースメントの組み合わせで到達した頻度を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | 報告されたディメンションのみによってリーチされた世帯数。報告されたディメンションのみによってリーチされた<code>[IP アドレス ] - [他のディメンションによってリーチされたIP アドレス ]として計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | 報告されたディメンションのみがリーチした世帯の割合。ディメンションがリーチしたIP アドレスの割合<code>[他のディメンションがリーチしたIP アドレスの割合] - [他のディメンションがリーチしたIP アドレスの割合]として計算</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | 提供された広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | 表示可能性のために測定されたインプレッションの合計数です。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | ディメンションの最大3つの値の交差を含め、報告されたディメンションのみで提供される測定可能なインプレッションの合計数。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々の配置によって到達した測定可能なインプレッション数、任意の2つの配置の組み合わせによって到達した測定可能なインプレッション数、および任意の3つの配置の組み合わせによって到達した測定可能なインプレッション数を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | 総支出額。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | 合計一意の世帯（個別のIP アドレス）に到達しました。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | ディメンションの最大3つの値の交差を含め、報告されたディメンションによってのみ到達した合計一意の世帯（個別のIP アドレス）です。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々の配置で到達したユニーク世帯、任意の2つの配置の組み合わせで到達した一般的な世帯、および任意の3つの配置の組み合わせで到達した一般的な世帯を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | 総支出を増分世帯リーチで割った値です。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | 総支出を「ユニーク世帯リーチ」で割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | 1世帯当たりのインプレッション数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | 報告されたディメンションのみによってリーチされた世帯数。報告されたディメンションのみによってリーチされた[IP アドレス ] - [他のディメンションによってリーチされたIP アドレス ]として計算されます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | 報告されたディメンションのみでリーチされた世帯の割合。ディメンションでリーチされたIP アドレスの割合[他のディメンションでリーチされたIP アドレスの割合] - [として計算されます。] |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | 提供された広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | 表示可能性のために測定されたインプレッションの合計数です。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | 総支出額。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | 合計一意の世帯（個別のIP アドレス）に到達しました。 |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | ターゲットにするIDのタイプ。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | Max CPMで入札された合計入札額の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | 顧客獲得当たりの平均総費用（<code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric]で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | 広告クリックあたりの平均総費用（<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks]別）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | 完了済みビデオ表示あたりの平均コストは、<code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions]によって計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | 広告エンゲージメントあたりの平均総費用（<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Engagements]別）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Impressions]で計算された、広告インプレッションあたりの平均総費用</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | 1000 インプレッションあたりの平均コストは、<code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000で計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Views]によって計算されたビデオ表示当たりの平均コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>ここで、[!UICONTROL Custom Goal]は、カスタム目標に添付されたすべてのコンバージョンの目標の重みです。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | 表示可能なインプレッション 1000個あたりの平均コストは、<code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000で計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | 広告クリックあたりの平均正味コストは、<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks]によって計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | 完了済みビデオビューあたりの平均正味費用（<code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions]別）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | 広告インプレッションあたりの平均正味コストは、<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Impressions]によって計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | 1000 インプレッションあたりの平均正味コスト （単位：<code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | <code>[!UICONTROL Net Spend] / [!UICONTROL Views]で計算された、ビデオビューあたりの平均正味費用</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | 表示可能なインプレッション 1000個あたりの平均正味費用（単位：<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | DSPがプレースメントに入札する個別ユーザーの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | 代理店手数料について。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | Adobe Creativeから配信された広告の総費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | DSPを通じて請求されるオーディエンスセグメントデータ料金の正味費用の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | DSPを通じて請求される、請求可能メディアの合計正味費用（技術料金を含む）。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | DSPを通じて請求される他のサービス料金（サードパーティの検証パートナー、広告配信など）の合計費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | Adobe Creativeから提供される広告に対する推定税。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | サードパーティのオーディエンスセグメントとデータサービスに対する推定税。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | DSPのメディア費用請求および技術手数料サービスに適用される税を含むメディアに対する推定税。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | その他のサービス料金（サードパーティの検証パートナー、トピックターゲティングなどを含む）に対する税金の見積もりは、DSPを通じて請求されます。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | 総支出です。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | （マージン管理が有効になっている場合） マージンの割合。計算式は<code> （[!UICONTROL Gross Spend] - [!UICONTROL Net Spend]） / [!UICONTROL Gross Spend]です</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | テクノロジー料金なしで、請求不可および請求可能なメディアコストの合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | 表示可能なインプレッション 1000個あたりの平均正味費用（単位：<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | Adobe Creativeを通じて請求されない広告の総費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | DSPを通じて請求されないオーディエンスセグメントデータ料金の正味費用の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | DSPを通じて請求されないテクノロジー料金を含む、請求不可メディアの正味総費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | DSPを通じて請求されない他のサービス料金（サードパーティの検証パートナー、広告配信など）の総費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | [!UICONTROL Billable Spend (Media)]、[!UICONTROL Billable Spend (Data)]および[!UICONTROL Billable Spend (Other)]の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | Adobe Creativeから配信される広告の1000 インプレッションあたりの平均正味メディアコスト。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | Adobe Creativeから配信された広告に対する請求可能および請求不可の総支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | 1000 インプレッションあたりの平均正味データコスト （単位：<code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | オーディエンスセグメントデータ料金の正味費用の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | 1000 インプレッションあたりの平均正味メディアコスト （単位：<code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | 技術コストを含むメディアの総純費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | [!UICONTROL Net Spend (Media)]、[!UICONTROL Net Spend (Data)]および[!UICONTROL Net Spend (Other)]の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | [!UICONTROL Non-billable Spend (Media)]、[!UICONTROL Non-billable Spend (Data)]および[!UICONTROL Non-billable Spend (Other)]の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | 他の手数料に対する1000 インプレッションあたりの平均正味費用は、<code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000で計算されます</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | その他のサービス料金（サードパーティの検証パートナー、広告配信など）の正味費用の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Clicks] | 合計クリック数： |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL CTR] | クリック数の割合をインプレッションで割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Engagements] | 配信された広告のインタラクション数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Engagement Rate] | 配信された広告におけるインタラクションの割合を、インプレッションで割った割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Impressions] | 全体的なインプレッション。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Media Match Rate] | クリエイティブが意図したメディア/インベントリまたはオーディエンスに一致したインプレッション（またはイベント）の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Clicks] | 特定の製品に関連付けられた合計クリック数。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Conversions] | 特定の製品に起因するコンバージョンの合計数。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Conversion Rate] | [!UICONTROL Product Conversions]を[!UICONTROL Product Impressions]で割って、特定の商品に関連付けています。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product CTR] | [!UICONTROL Product Clicks]を[!UICONTROL Product Impressions]で割って、特定の商品に関連付けています。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Impressions] | 特定の製品に対する総インプレッション数。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Product Revenue] | 特定の製品に対する総売上。 クリエイターが複数の製品（カルーセル広告など）を表示し、製品別にレポートを作成する場合に使用します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard] | [!UICONTROL Revenue] | 総収入。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | 広告全体を視聴した閲覧数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | 広告全体を視聴した閲覧数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | 広告全体を視聴した表示可能なインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | 広告の少なくとも1つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | 広告の少なくとも1つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | 広告の少なくとも2つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | 広告の少なくとも2つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | 広告の少なくとも2つの四分位数を視聴した表示可能なインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | 広告の少なくとも3つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | 広告の少なくとも3つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | 広告が完了するまで監視された平均割合。すべてのビューを考慮します。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | 広告オーバーレイとバナーのクリック数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | クリック数の割合を広告インプレッションで割った割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | クリック数の割合をビデオビューで割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | コンパニオンバナーのクリック数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | クリック率をコンパニオンバナーインプレッションで割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | コンパニオンバナーインプレッションの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | 広告の表示に使用されたインターネット接続のタイプ（Wifiまたは4g LTEなど）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 配信された広告のインタラクション数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | 配信されたインプレッションのうち、動画を視聴した割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | ビデオビューの平均デュレーション（秒単位）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | 広告の全クリックの合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | ビデオ広告が表示された合計分数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | ビデオ広告の合計再生回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completion Rate] | （カスタム Creative レポート）広告全体を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 100% Completions] | （カスタム Creative レポート）広告全体を視聴したビュー数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completion Rate] | （カスタム Creative レポート）広告の少なくとも1つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 25% Completions] | （カスタム Creative レポート）広告の少なくとも1つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completion Rate] | （カスタム Creative レポート）広告の少なくとも2つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 50% Completions] | （カスタム Creative レポート）広告の少なくとも2つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completion Rate] | （カスタム Creative レポート）広告の少なくとも3つの四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL 75% Completions] | （カスタム Creative レポート）広告の少なくとも3つの四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Avg Percent Viewed] | （カスタム Creative レポート）広告が完了するまで監視された平均割合。すべてのビューを考慮します。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Play Rate] | （カスタム Creative レポート）配信されたインプレッションのうち、ビデオ視聴に至った割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Playtime per View] | （カスタム Creative レポート）ビデオビューの平均所要時間（秒単位）。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Mute] | （カスタム Creative レポート）ビデオがミュートされた合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Pause] | （カスタム Creative レポート）ビデオが一時停止された合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Resume] | （カスタム Creative レポート）一時停止した後にビデオが再開された合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Rewind] | （カスタム Creative レポート）ビデオが巻き戻された合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Start] | （カスタム Creative レポート）ビデオが開始された合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Video Unmute] | （カスタム Creative レポート）ビデオのミュート解除の合計回数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Viewed Minutes] | （カスタム Creative レポート）ビデオ広告が表示された合計分数。 |
| [!UICONTROL Metrics] | [!UICONTROL Video] | [!UICONTROL Views] | （カスタム Creative レポート）ビデオ広告の合計表示数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | プレイヤーの平均身長と幅。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | 表示可能性のために測定されたインプレッションの合計数です。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | 表示可能性を測定できるインプレッションの割合（<code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions]として計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | 互換性のないiFrameが原因で、表示可能性に対して測定できないインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | 広告ユニットでサポートされていない視認性トラッキングが原因で、視認性に対して測定できないインプレッションの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | 他の理由により、視認性に関して測定できないインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | 広告インプレッションの数は、ビューアビリティでは測定できません。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | 広告インプレッションの割合。ビューアビリティでは測定できません。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | この広告ユニットでサポートされていないビューアビリティトラッキングが原因で、ビューアビリティに対して測定できないインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | すべての測定可能なインプレッションのうち、表示可能なインプレッションの割合（<code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions]として計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | 表示可能と見なされる広告インプレッションの数。 |
| [!UICONTROL Conversion Metrics] | [ レポート設定で広告主別にグループ化] | [広告主固有のコンバージョン ] | 指定された広告主固有のコンバージョン指標またはAdobe Analytics イベントの合計。 |
| [!UICONTROL Custom Goals] | [ レポート設定で広告主別にグループ化] | [広告主固有のカスタム目標] | 指定された[&#x200B; カスタム目標](/help/dsp/optimization/custom-goal.md)に含まれるすべてのコンバージョンの重み付け合計。 |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [&#x200B; カスタムレポートについて](/help/dsp/reports/report-about.md)
>* [&#x200B; カスタムレポートを作成](/help/dsp/reports/report-create.md)
>* [&#x200B; カスタムレポートを複製](/help/dsp/reports/report-copy.md)
>* [&#x200B; カスタムレポートを編集](/help/dsp/reports/report-edit.md)
>* [&#x200B; カスタムレポート設定](/help/dsp/reports/report-settings.md)
