---
title: 接続されたテレビのリーチ プランの設定
description: 接続されたテレビのリーチ プランの設定の説明を参照してください。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 84cf49c9e366938479e9fea2ede55925f1cb3e51
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 0%

---

# 接続されたテレビのリーチ プランの設定

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
>* [DSP プランナーツールについて ](planner-about.md)
>* [ 接続されたテレビのリーチプランを作成 ](planner-create.md)
>* [ 接続されたテレビのリーチ プランを複製 ](planner-duplicate.md)
>* [ 接続されたテレビのリーチ プランを編集する ](planner-edit.md)
>* [ 接続されたテレビのリーチ プランのエクスポート ](planner-export.md)
>* [Connected TV Reach Plan の Forecast の再生成 ](planner-forecast.md)
>* [ 接続されたテレビのリーチ プランをアーカイブする ](planner-archive.md)
