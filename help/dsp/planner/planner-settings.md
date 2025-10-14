---
title: 接続されたテレビのリーチ プランの設定
description: 接続されたテレビのリーチ プランの設定の説明を参照してください。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 5d8d981f08eaea2b0a0bc553ab06bd47f1e88ac9
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 接続されたテレビのリーチ プランの設定

<!-- Move out of table for consistency at some point. -->

| パラメーター | 説明 | 必須？ |
| --- | --- | --- |
| [!UICONTROL Name] | プランを識別する名前。 | はい |
| [!UICONTROL Advertiser] | プランが作成されるアカウントの特定の広告主。 | はい |
| [!UICONTROL Media Type] | 計画に含めるメディアのタイプ。<br><br> 現在、[!UICONTROL Connected TV] のみが使用可能です。 | はい |
| [!UICONTROL Date Range] | 計画の開始日と終了日。<br><br> 開始日を現在の日付より前にすることはできません。 日付範囲は 90 日を超えることはできません。 | はい |
| [!UICONTROL Goal Type] | 計画について考慮する目標のタイプ（[!UICONTROL Budget] など）。<br><br> 現在、[!UICONTROL Budget] のみが使用可能です。 | はい |
| [!UICONTROL Goal Value] | 予測の目標値。 より正確な予測結果を得るには、5000 USD を超える値を使用します。 | はい |
| [!UICONTROL Max Bid] | 1000 インプレッションに対して支払う最大金額。 [!UICONTROL Connected TV] メディアタイプを選択した場合は、10 USD 以上の値を入力します。 | はい |
| [!UICONTROL Frequency Cap] | 一意の世帯が広告を提供される回数。<br><br> プランを実装し、複数のプレースメントを作成する必要がある場合、適切な配信を確保するために、プレースメントレベルではなくパッケージレベルでフリークエンシーキャップ設定を適用します。 | はい |
| [!UICONTROL Geo-Targeting] | ターゲットとして含める、または除外するロケーション。 次のようなオプションがあります。<ul><li>国、都市、州：「**[!UICONTROL Country/State/City]**」タブをクリックします。エリアを *国*、*州* または *市区町村* のどれにするかを選択します。必要に応じて場所を展開してそのサブコンポーネントを表示し、場所の横にある「**[!UICONTROL Include]**」または「**[!UICONTROL Exclude]**」をクリックします。</li><li>米国の指定されたマーケットエリア（DMA）: [**[!UICONTROL DMA]**] タブをクリックします。任意の州を展開して DMA を表示し、場所の横にある [**[!UICONTROL Include]**] または [**[!UICONTROL Exclude]**] をクリックします。</li><li>郵便番号：次のいずれかを実行できます。<ul><li>[**[!UICONTROL Search postal code]**] タブをクリックし、国を選択し、完全な市区町村名または市区町村名に含まれる文字を入力して **[Enter]** キーを押し、正しい市区町村名をクリックして市区町村のすべての郵便番号を表示します。次に、正しい郵便番号をクリックして、[**[!UICONTROL Include]**] または [**[!UICONTROL Exclude]**] をクリックします。</li><li>[**[!UICONTROL Paste postal code]**] タブをクリックし、国を選択し、コンマ区切りの値を入力または貼り付けて、[**[!UICONTROL Include All]**] または [**[!UICONTROL Exclude All]**] をクリックします。</li></ul></li></ul> | はい |
| [!UICONTROL Inventory Targeting] | ターゲットとして含めるか除外する在庫ソース。 1 つ以上のフィードまたはソースを選択してください。 | はい |
| [!UICONTROL Site/App Targeting] | ターゲットとして含める、または除外する web サイトおよびアプリ。 1 行に 1 つの URL を入力し、「**[!UICONTROL Include All]**」または「**[!UICONTROL Exclude All]**」をクリックします。 | 不可 |
| [!UICONTROL Audience Targeting] | ターゲットとして含める、または除外するオーディエンス。 | 不可 |
| [!UICONTROL Ad duration] | プランで考慮する広告の期間。 | 不可 |

>[!MORELIKETHIS]
>
>* [DSP プランナーツールについて &#x200B;](planner-about.md)
>* [&#x200B; 接続されたテレビのリーチプランを作成 &#x200B;](planner-create.md)
>* [&#x200B; 接続されたテレビのリーチ プランを複製 &#x200B;](planner-duplicate.md)
>* [&#x200B; 接続されたテレビのリーチ プランを編集する &#x200B;](planner-edit.md)
>* [&#x200B; 接続されたテレビのリーチ プランのエクスポート &#x200B;](planner-export.md)
>* [Connected TV Reach Plan の Forecast の再生成 &#x200B;](planner-forecast.md)
>* [&#x200B; 接続されたテレビのリーチ プランをアーカイブする &#x200B;](planner-archive.md)
