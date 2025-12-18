---
title: 使用可能なレポート列
description: カスタムレポートで使用可能な列の説明を参照してください。
feature: DSP Custom Reports
exl-id: 6dc30603-8a45-4188-aca6-591f3422b74a
source-git-commit: ab5d16d5132be59d2e902533155502c830c04bea
workflow-type: tm+mt
source-wordcount: '2467'
ht-degree: 0%

---

# 使用可能なレポート列

<!-- Add when added:

|[!UICONTROL Dimension]|[!UICONTROL Feed]|[!UICONTROL Deal List]|The name of a user-created deal list for which an ad was shown.|

-->

| 指標タイプ | サブタイプ | 列名 | 説明 |
|-----------|-------|-----------|-----------|
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad External ID] | 外部広告サーバーによって割り当てられた広告 ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad ID] | DSPの広告の一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Name] | ユーザーによって割り当てられた広告の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Ad Type] | 広告の形式。 |
| [!UICONTROL Dimension] | [!UICONTROL Ad] | [!UICONTROL Status] | ユーザーによって変更された、または日付入力（*[!UICONTROL live]*、*[!UICONTROL scheduled]*、*[!UICONTROL completed]*、*[!UICONTROL archived]*）で示される広告の分類。 |
| [!UICONTROL Dimension] | [!UICONTROL Advertiser] | [!UICONTROL Advertiser Name] | 広告主の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Budget] | キャンペーンに対してユーザーによって割り当てられた予算の合計。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign End Date] | キャンペーンの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign ID] | DSPのキャンペーンの一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Name] | ユーザーによって割り当てられたキャンペーンの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Campaign] | [!UICONTROL Campaign Start Date] | キャンペーンの最初の日付。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Title] | コンテンツ/映画のタイトル。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Series] | コンテンツシリーズ。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Genre] | コンテンツのジャンル。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL ProdQ] | [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md) で定義される生産品質。 値には、`Unknown`、`Professionally Produced`、`Prosumer`、`User Generated` を使用できます。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Context] | [IAB Technology Laboratory](https://github.com/InteractiveAdvertisingBureau/AdCOM/blob/main/AdCOM%20v1.0%20FINAL.md) で定義されたコンテンツのタイプ。 値には、`Video,`、`Game`、`Music`、`Application`、`Text`、`Other` な `Unknown` があります。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Rating] | コンテンツのレーティング（PG、R など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Livestream] | 広告がライブストリームに表示されたかどうか（`Not Live` または `Live`）。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Content Length (in seconds)] | コンテンツの長さ（秒）。通常、ビデオまたはオーディオに使用されます。 |
| [!UICONTROL Dimension] | [!UICONTROL Content] | [!UICONTROL Language (as per ISO 639)] | ISO-639-1-alpha-2 を使用するコンテンツの言語。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Day (YYYY-MM-DD)] | 年、月、日。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | 日 [!UICONTROL of Week] | 特定の日（[!UICONTROL Monday]、[!UICONTROL Tuesday] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Hour (YYYY-MM-DD HH)] | 年、月、日、時間。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Month (YYYY-MM)] | 月と年 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Time of Day] | 0 から 23 までの時間。 |
| [!UICONTROL Dimension] | [!UICONTROL Date/Time] | [!UICONTROL Week (YYYY-MM-DD to YYYY-MM-DD)] | 該当する週の日曜日から土曜日の日付範囲。 例：2021-02-18 ～ 2021-03-07。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Vendor] | 広告が表示されたブラウザーのベンダー（Google、Mozilla など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser Version] | 広告が表示されたブラウザーのバージョン （[!UICONTROL Safari 4.3] や [!UICONTROL Chrome 7.0] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Browser] | 広告が表示されたブラウザー（[!UICONTROL Chrome] や [!UICONTROL Firefox] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Environment] | 広告が *[!UICONTROL sites]* または *[!UICONTROL Apps]* に表示されたかどうか。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Hardware] | 広告が表示されたデバイスのタイプ（[!UICONTROL Set Top Box] や [!UICONTROL Mobile Phone] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Manufacturer] | 広告が表示されたデバイスの製造元（[!UICONTROL Samsung]、[!UICONTROL Lenovo]、[!UICONTROL Apple] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Model] | 広告が表示されたデバイスのモデル （[!UICONTROL iPhone XS] や [!UICONTROL Galaxy Note 7] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Vendor] | 広告が表示されたオペレーティングシステムのベンダー（[!UICONTROL Microsoft] や [!UICONTROL Apple] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System Version] | 広告が表示されたオペレーティングシステムのバージョン （[!UICONTROL Windows 10] や [!UICONTROL iOS Mojave] など） |
| [!UICONTROL Dimension] | [!UICONTROL Device] | [!UICONTROL Operating System] | 広告が表示されたオペレーティングシステム（[!UICONTROL Apple iOS] や [!UICONTROL Android] など）。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Name] | DSPで入力された、ユーザーが割り当てた取引の名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Deal Type] | 取引が *[!UICONTROL Guaranteed]* か *[!UICONTROL Non-Guaranteed]* か。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Inventory Type] | 在庫の分類：*[!UICONTROL Private]、* *[!UICONTROL On Demand]、* または *[!UICONTROL Public]*。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Private Deal ID] | 外部供給パートナーを通じてプライベート取引に割り当てられた一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL Publisher] | 在庫を提供する供給側パートナー。 これは通常はパブリッシャーですが、SSP にすることもできます。 |
| [!UICONTROL Dimension] | [!UICONTROL Feed] | [!UICONTROL SSP] | メディアが属する供給側パートナー（SSP）。 |
| [!UICONTROL Dimension] | [!UICONTROL Frequency] | [!UICONTROL Frequency] | デバイスが広告を受け取った回数。一意の Cookie またはデバイス ID に基づきます。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL City] | レポートされたデータが関連付けられている市区町村。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Country] | レポートされたデータの帰属先の国。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL DMA] | レポートされたデータの帰属先となる指定マーケットエリア（DMA）。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL Pin Code] | レポートされたデータの属性付け先の郵便番号インデックス番号（PIN） コード。 |
| [!UICONTROL Dimension] | [!UICONTROL Geos] | [!UICONTROL State] | レポートされるデータの帰属先の状態。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Audience] | オーディエンス。 レポートでは、最大 10 個の一意のオーディエンスをサポートしています。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Creative Length] | クリエイティブの長さ。 このレポートは、最大 10 個の一意のクリエイティブ長をサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Device] | デバイス。 このレポートは、最大 10 台の一意のデバイスをサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Feed Type] | フィードのタイプ。 レポートでは、最大 10 個の一意のフィードタイプがサポートされます。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Media Type] | メディアタイプ。 レポートでは、最大 10 個の一意のメディアタイプをサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Publisher] | パブリッシャー。 レポートでは、最大 10 人の一意のパブリッシャーがサポートされます。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Package] | パッケージ。<!-- Note: The Package dimensions include another dimension called Package Name. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Placement] | プレースメント。<!-- Note: The Placement dimensions include another dimension called Placement Name --> |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Site/Apps] | 広告インプレッションが提供されたサイトまたはアプリ。 レポートは、最大 10 個の一意のサイトまたはアプリをサポートします。 |
| [!UICONTROL Dimension] | [!UICONTROL Household] | [!UICONTROL Tags] | プレースメントのカスタム識別子として使用されるプレースメント タグ。 このレポートでは、最大 10 個の一意のプレースメントタグがサポートされます。<!-- Note: The Placement dimensions include another dimension called Placement Tags. --> |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Audience] | オーディエンス。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Campaign] | キャンペーン。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Creative Length] | クリエイティブの長さ。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Device] | デバイス。 （CTV、デスクトップなど） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Media Type] | メディアタイプ。 （ディスプレイ、オーディオなど） |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Publisher] | パブリッシャー。 |
| [!UICONTROL Dimension] | [!UICONTROL Household Conversions] | [!UICONTROL Placement] | プレースメント。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Budget] | パッケージフライトの予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight End Date] | パッケージフライトの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Rollover] | パッケージフライトのロールオーバー予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Package Flight] | [!UICONTROL Package Flight Start Date] | パッケージフライトの開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package End Date] | パッケージの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Goal Type] | パッケージのペーシング目標量。 この金額は支出またはインプレッション数のいずれかです。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package ID] | DSPのパッケージの一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Name] | パッケージ名 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Package Start Date] | パッケージの開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Packages] | [!UICONTROL Placement End Date] | プレースメントの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion ID] | （非推奨）DSPによって従来のコンバージョンイベントに割り当てられたコンバージョン [!DNL TubeMogul]。 |
| [!UICONTROL Dimension] | [!UICONTROL Pixel] | [!UICONTROL Conversion Name] | （非推奨）従来の [!DNL TubeMogul] コンバージョンイベントに割り当てられたコンバージョン名。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement ID] | DSPのプレースメントの一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Name] | ユーザーによって割り当てられたプレースメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Budget] | プレースメントの予算。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Max Bid] | プレースメントの最大入札額。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Device Environment] | プレースメントのターゲットとなるデバイス環境：（*[!UICONTROL Desktop]*、*[!UICONTROL Mobile]*、*[!UICONTROL Connected TV]）*。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement End Date] | プレースメントの終了日。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Start Date] | プレースメントの開始日。 |
| [!UICONTROL Dimension] | [!UICONTROL Placement] | [!UICONTROL Placement Tags] | プレースメントのカスタム識別子として使用されるプレースメント タグ。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Description] | 請求可能セグメントに関連付けられた説明。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Key] | 請求可能なセグメントに関連付けられた一意のキー。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Billing Segment Name] | 請求可能セグメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Description] | データプロバイダーによって提供される、セグメントに関連付けられた説明。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Key] | セグメントに関連付けられた一意のキー。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Name] | セグメントの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Segment] | [!UICONTROL Segment Membership Provider Name] | セグメントに関連付けられたデータプロバイダーの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site ID] | DSPのサイトまたはアプリの一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Site] | [!UICONTROL Site Name] | サイトの名前。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Duration] | アップロード後に処理されるビデオの長さ。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video ID] | DSPのビデオクリエイティブの一意の ID。 |
| [!UICONTROL Dimension] | [!UICONTROL Video] | [!UICONTROL Video Name] | ユーザーによって割り当てられたクリエイティブの名前。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL % Distinct Uniques] | [!UICONTROL App/Site Distinct Uniques] を [!UICONTROL App/Site Uniques] で割ったもの。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL App/Site Distinct Uniques] | このアプリでのみ到達したデバイスの合計数。 複数のパブリッシャーの広告に公開されるビューアは、この値に含まれません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Distinct Unique] | [!UICONTROL Total Spend] を [!UICONTROL App/Site Distinct Uniques] で割ったもの。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Cost per Unique] | [!UICONTROL Total Spend] を [!UICONTROL App/Site Uniques] で割ったもの。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated % Reached] | 被ばくを受け取ったターゲットの世帯宇宙の推定割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Average Frequency] | ユニークに表示されるインプレッションの平均数。 一部のインベントリでは、パブリッシャーはデバイス ID を渡さず、それらのインプレッションはこの値に含まれません。 [!UICONTROL Frequency (by App/Site)] レポートにも同様の指標がありますが、その指標は推定されません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Impressions (Device/Browser)] | （[!UICONTROL Frequency (by Impression)] レポートに含まれる）特定の頻度のブレイクアウトに関する推定インプレッション数。 DSPの予測値は、インプレッション数のサンプルに基づいています。 一部のインベントリでは、パブリッシャーはデバイス ID を渡さず、それらのインプレッションはこの値に含まれません。 [!UICONTROL Frequency (by App/Site)] レポートにも同様の指標がありますが、その指標は推定されません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Uniques (Device/Browser)] | （[!UICONTROL Frequency (by Impression)] レポートに含まれる）特定の頻度で記録された一意のブラウザーまたはデバイスの数。 DSPの予測値は、インプレッション数のサンプルに基づいています。 一部の在庫では、デバイス識別子に沿ってを渡さないでください。それらのインプレッションはこの値には含まれません。 [!UICONTROL Frequency (by App/Site)] レポートにも同様の指標がありますが、その指標は推定されません。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Estimated Universe] | DSP（オークション）が日付範囲内で閲覧したユニーク世帯の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Frequency] | [!UICONTROL Extended Impressions] | 人物ベースのクロスデバイスターゲティングにデバイスグラフを使用した結果として提供されたインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency] | 世帯ごとのインプレッションの頻度。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Frequency Overlap] | ディメンションの最大 3 つの値の交差を含め、レポートされたディメンションのみによって世帯に到達する頻度。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々のプレースメントによって達成された頻度、2 つのプレースメントの組み合わせによって達成された頻度、および 3 つのプレースメントの組み合わせによって達成された頻度を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Incremental Household Reached] | レポートされたディメンションによってのみ到達した世帯の数。<code>[ レポートされたディメンションによってのみ到達した IP アドレス ] - [ 他のディメンションで到達した IP アドレスとして計算され ] す。</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL % Incremental Household Reached] | レポートされたディメンションのみによって到達した世帯の割合（<code>[ ディメンションによって到達した IP アドレスの割合 ] - [ 他のディメンションによって到達した IP アドレスの割合）として計算 ]</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Impressions] | 提供された広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions] | ビューアビリティの測定が可能な、提供されたインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Measurable Impressions (Overlap)] | ディメンションの最大 3 つの値の交差を含む、レポートされたディメンションによってのみ提供された測定可能インプレッションの合計数。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々のプレースメントによって到達した測定可能なインプレッション数、2 つのプレースメントの組み合わせによって到達した測定可能なインプレッション数、および 3 つのプレースメントの組み合わせによって到達した測定可能なインプレッション数を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Total Media Spend] | 総支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household Reached] | 一意の世帯の合計（個別の IP アドレス）に到達しました。 |
| [!UICONTROL Metrics] | [!UICONTROL Household] | [!UICONTROL Unique Household (Overlap)] | ディメンションの最大 3 つの値の交差を含む、レポートされたディメンションのみが到達した一意の世帯の合計（個別の IP アドレス）。 例えば、[!UICONTROL Placement] ディメンションを使用すると、個々のプレースメントによって到達した一意の世帯、2 つのプレースメントの組み合わせによって到達した一般的な世帯、3 つのプレースメントの組み合わせによって到達した一般的な世帯を確認できます。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Incremental HH] | 総支出を世帯の増分支出で割って到達しました。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Cost per Unique HH] | 総支出を、到達したユニーク世帯で割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Frequency] | 世帯ごとのインプレッションの頻度。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Incremental Household Reached] | 報告されたディメンションによってのみ到達した世帯の数。次のように計算されます [ 報告されたディメンションのみによって到達した IP アドレス ] - [ 他のディメンションによって到達した IP アドレス ]。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL % Incremental Household Reached] | レポートされたディメンションのみによって到達した世帯の割合（[ ディメンションによって到達した IP アドレスの割合 ] - [ 他のディメンションによって到達した IP アドレスの割合 ] として計算）。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Impressions] | 提供された広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Measurable Impressions] | ビューアビリティの測定が可能な、提供されたインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Total Media Spend] | 総支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Household Conversions] | [!UICONTROL Unique Household Reached] | 一意の世帯の合計（個別の IP アドレス）に到達しました。 |
| [!UICONTROL Metrics] | [!UICONTROL Identifier] | [!UICONTROL Identifier Type] | ターゲットとする ID のタイプ。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL % bid at Max CPM] | Max CPMで入札された合計入札の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPA] | <code>[!UICONTROL Gross Spend] / [!UICONTROL conversion metric] で計算された、獲得あたりの平均総原価</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPC] | 広告クリックあたりの平均総コスト（<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Clicks] で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPCV] | <code>[!UICONTROL Gross Spend] / [!UICONTROL 100% Completions] で計算された、完了したビデオビューあたりの平均コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPE] | 広告エンゲージメントあたりの平均総コスト（<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Engagements] で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPI] | 広告インプレッションあたりの平均総コスト（<code>[!UICONTROL Gross Spend] / [!UICONTROL Total Ad Impressions] で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPM] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Impressions] x 1000 で計算された、1000 インプレッションあたりの平均コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross CPV] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Views] で計算された、ビデオビューあたりの平均コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross Custom Goal CPA] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Custom Goal]</code>:[!UICONTROL Custom Goal] は、カスタム目標に関連付けられたすべてのコンバージョンの目標の重み付けです。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Gross vCPM] | <code>[!UICONTROL Gross Spend] / [!UICONTROL Viewable Impressions] x 1000 で計算された、表示可能インプレッション 1000 個あたりの平均コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPC] | 広告クリックあたりの平均正味コスト（<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Clicks] で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPCV] | <code>[!UICONTROL Net Spend] / [!UICONTROL 100% Completions] で計算された、完了したビデオビューあたりの平均正味コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPI] | 広告インプレッションあたりの平均正味コスト（<code>[!UICONTROL Net Spend] / [!UICONTROL Total Ad Impressions] で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPM] | <code>[!UICONTROL Net Spend] / [!UICONTROL Impressions] x 1000 で計算された、1000 インプレッションあたりの平均正味コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net CPV] | <code>[!UICONTROL Net Spend] / [!UICONTROL Views] で計算された、ビデオビューあたりの平均正味コスト</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Net vCPM] | 表示可能インプレッション 1000 件あたりの平均正味コスト（<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000 で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Performance] | [!UICONTROL Unique Users Bid On] | DSPがプレースメントに対して入札するユニークユーザーの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Agency Fee] | 代理店手数料。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Creative Spend] | Adobe Creativeから提供された広告の合計支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Data Spend] | DSPを通じて請求される、オーディエンスセグメントデータ料金の合計の正味費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Media Spend] | DSPを通じて請求される、技術料を含む、請求可能なメディアの合計の正味費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Billable Other Spend] | DSPを通じて請求されるその他のサービス料金（サードパーティの検証パートナー、広告サービスなど）の合計コスト。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Creative] | Adobe Creativeから提供される広告に対する推定税額。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Data] | サードパーティのオーディエンスセグメントとデータサービスに対する推定税額。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Media] | DSPのメディアコストの再請求および技術料サービスに適用される税を含む、メディアに対する推定税。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Estimated Tax on Other] | DSPを通じて請求されるその他のサービス料金（サードパーティの検証パートナーやトピックターゲティングなどを含む）の推定税額。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Gross Spend] | 総支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Margin %] | （利益管理が有効化されている場合） <code> （[!UICONTROL Gross Spend] - [!UICONTROL Net Spend]） / [!UICONTROL Gross Spend] で計算される利益率</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Media Cost] | テクニカル料金なしで請求および請求が可能なメディアコストの合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Net vCPM] | 表示可能インプレッション 1000 件あたりの平均正味コスト（<code>[!UICONTROL Net Spend] / [!UICONTROL Viewable Impressions] x 1000 で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non Billable Creative Spend] | Adobe Creativeを通じて請求されない広告の合計支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Data Spend] | DSPを通じて請求されない、オーディエンスセグメントデータ料金の合計正味費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Media Spend] | DSP経由で請求されない技術料を含む、請求対象外メディアの合計正味費用。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Non-Billable Other Net Spend] | DSPを通じて請求されない、その他のサービス料金（サードパーティの検証パートナー、広告サービスなど）の合計コスト。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Profit] | [!UICONTROL Gross Spend] - [!UICONTROL Net Spend] |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Billable Spend] | [!UICONTROL Billable Spend (Media)]、[!UICONTROL Billable Spend (Data)]、[!UICONTROL Billable Spend (Other)] の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative CPM] | Adobe Creativeから提供される広告の 1000 インプレッションあたりの平均正味メディアコスト。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Creative Spend] | Adobe Creativeから提供される広告の請求可能および請求不可の総支出。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data eCPM] | インプレッション 1000 件あたりの平均正味データコスト（<code>[!UICONTROL Net Spend (Data)] / [!UICONTROL Impressions] x 1000 で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Data Spend] | オーディエンスセグメントデータ料金の正味合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media CPM] | インプレッション 1000 件あたりの平均正味メディアコスト（<code>[!UICONTROL Net Spend (Media)] / [!UICONTROL Impressions] x 1000 で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Media Spend] | メディアの正味合計コスト （技術費を含む）。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Net Spend] | [!UICONTROL Net Spend (Media)]、[!UICONTROL Net Spend (Data)]、[!UICONTROL Net Spend (Other)] の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Non-Billable Net Spend] | [!UICONTROL Non-billable Spend (Media)]、[!UICONTROL Non-billable Spend (Data)]、[!UICONTROL Non-billable Spend (Other)] の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other eCPM] | その他の料金の 1000 インプレッションあたりの平均正味費用（<code>[!UICONTROL Net Spend (Other)] / [!UICONTROL Impressions] x 1000 で計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Spend] | [!UICONTROL Total Other Spend] | その他のサービス料金（サードパーティの検証パートナー、広告サービングなど）の純費用の合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completion Rate] | 広告全体を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Completions] | 広告全体を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 100% Viewable Completion (%)] | 広告全体を視聴したビューアブルインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completion Rate] | 広告の少なくとも 1 四分位数を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 25% Completions] | 広告の少なくとも 1 四分位数を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completion Rate] | 広告の 4 分の 2 以上を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Completions] | 広告の四分の一以上を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 50% Viewable Completion (%)] | 広告の 4 分の 2 以上を視聴したビューアブルインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completion Rate] | 広告の少なくとも 3 四分の 1 を視聴したビューの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL 75% Completions] | 広告の四分の三以上を視聴したビューの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Avg Percent Viewed] | すべてのビューを考慮した、広告が完了まで視聴された平均割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Banner and Overlay Clicks] | 広告オーバーレイとバナーのクリック数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Click Through Rate] | クリックの割合を広告インプレッション数で割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Clicks Per View Rate] | クリックの割合をビデオビューで割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Clicks] | コンパニオンバナーのクリック数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion CTR] | クリックの割合をコンパニオンバナーのインプレッションで割った値。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Companion Impressions] | コンパニオンバナーのインプレッションの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Connection] | 広告の表示に使用されたインターネット接続のタイプ （Wifi や 4g LTE など）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Engagements] | 提供された広告でのインタラクションの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Impressions] | 広告インプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Play Rate] | ビデオビューにつながったインプレッション数の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Playtime per View] | ビデオビューの平均時間（秒単位）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Total Ad Clicks] | 広告のすべてのクリックの合計。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Viewed Minutes] | ビデオ広告が表示された合計時間（分）。 |
| [!UICONTROL Metrics] | [!UICONTROL Standard Metrics] | [!UICONTROL Views] | ビデオ広告ビューの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Avg. Player Width x Height] | プレーヤーの平均の幅と高さ。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Impressions] | ビューアビリティの測定が可能な、提供されたインプレッションの合計数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Measurable Rate (%)] | ビューアビリティの測定が可能な、提供されたインプレッションの割合（<code>[!UICONTROL Measurable Impressions] x 1000 / [!UICONTROL Impressions] と計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - iFrame (%)] | 互換性のない iFrame が原因で、ビューアビリティで測定できないインプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Not Supported (%)] | 広告ユニットでビューアビリティのトラッキングがサポートされていないので、ビューアビリティのインプレッション数を測定できません。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable - Other (%)] | その他の理由により、ビューアビリティで測定できないインプレッション数の割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Impressions] | ビューアビリティでは測定できない広告インプレッションの数。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable Rate (%)] | ビューアビリティでは測定できない広告インプレッションの割合。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Unmeasurable rate (Not supported)] | この広告ユニットでサポートされていないビューアビリティ追跡が原因で、ビューアビリティについて測定できないインプレッションの割合です。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewability Rate (%)] | 測定可能なすべてのインプレッションの中で表示可能なインプレッションの割合（<code>[!UICONTROL Viewable Impressions] / [!UICONTROL Measurable Impressions] として計算）</code>。 |
| [!UICONTROL Metrics] | [!UICONTROL Viewability] | [!UICONTROL Viewable Impressions] | ビューアブルと見なされる広告インプレッションの数。 |
| [!UICONTROL Conversion Metrics] | [ レポート設定で広告主別にグループ化 ] | [ 広告主固有のコンバージョン ] | 指定した広告主固有のコンバージョン指標またはAdobe Analytics イベントの合計。 |
| [!UICONTROL Custom Goals] | [ レポート設定で広告主別にグループ化 ] | [ 広告主固有のカスタム目標 ] | 指定した [ カスタム目標 ](/help/dsp/optimization/custom-goal.md) に含まれるすべてのコンバージョンの重み付き合計。 |

{style="table-layout:auto"}

<!-- |Omitted|[!UICONTROL Performance]|Custom Goal ROAS|The average return on ad spend, calculated by <code>Custom goal / Gross spend</code> |-->

>[!MORELIKETHIS]
>
>* [ カスタムレポートについて ](/help/dsp/reports/report-about.md)
>* [ カスタムレポートの作成 ](/help/dsp/reports/report-create.md)
>* [ カスタムレポートの複製 ](/help/dsp/reports/report-copy.md)
>* [ カスタムレポートの編集 ](/help/dsp/reports/report-edit.md)
>* [ カスタムレポートの設定 ](/help/dsp/reports/report-settings.md)
