---
title: コネクテッド TV リーチプランの設定
description: コネクテッド TV リーチプランの設定の説明を参照してください。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
TQID: https://experienceleague.adobe.com/IDfRNpdLmCqxU2TSuRiueLn1DpIzEH23qiorfW5DeLs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# コネクテッド TV リーチプランの設定

<!-- Move out of table for consistency at some point. -->

| パラメーター | 説明 | 必要ですか？ |
| --- | --- | --- |
| [!UICONTROL Name] | プランを識別する名前。 | はい |
| [!UICONTROL Advertiser] | プランを作成するアカウント内の特定の広告主。 | はい |
| [!UICONTROL Media Type] | プランに含めるメディアのタイプ。<br><br>現在、[!UICONTROL Connected TV]のみが利用できます。 | はい |
| [!UICONTROL Date Range] | プランの開始日と終了日。<br><br>開始日を現在の日付より前にすることはできません。 日付範囲は90日を超えることはできません。 | はい |
| [!UICONTROL Goal Type] | プランで考慮する目標のタイプ（[!UICONTROL Budget]など）。<br><br>現在、[!UICONTROL Budget]のみが利用できます。 | はい |
| [!UICONTROL Goal Value] | 予測の目標値。 より正確な予測結果を得るには、5,000米ドルを超える値を使用します。 | はい |
| [!UICONTROL Max Bid] | 1000 インプレッションに対して支払う最大の金額。 [!UICONTROL Connected TV] メディアタイプが選択されている場合は、10 USD以上の値を入力してください。 | はい |
| [!UICONTROL Frequency Cap] | 一意の世帯に広告を配信する回数。<br><br> プランを実装し、複数のプレースメントを作成する必要がある場合は、適切な配信を確保するために、プレースメントレベルではなくパッケージレベルで頻度キャップ設定を適用します。 | はい |
| [!UICONTROL Geo-Targeting] | ターゲットとして含める、または除外する場所。 オプションは次のとおりです。<ul><li>国、都市、州：「**[!UICONTROL Country/State/City]**」タブをクリックします。エリアが&#x200B;*国*、*州*、または&#x200B;*都市*&#x200B;のいずれであるかを選択します。オプションで、任意の場所を展開してサブコンポーネントを表示し、その場所の横にある&#x200B;**[!UICONTROL Include]**&#x200B;または&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。</li><li>米国の指定市場地域（DMA）:「**[!UICONTROL DMA]**」タブをクリックします。オプションで、任意の状態を展開してDMAを表示し、場所の横にある「**[!UICONTROL Include]**」または「**[!UICONTROL Exclude]**」をクリックします。</li><li>郵便番号：次のいずれかを実行できます。<ul><li>「**[!UICONTROL Search postal code]**」タブをクリックし、国を選択し、都市名に含まれる完全な都市名または文字を入力してから、**[Enter]** キーを押し、正しい都市名をクリックして都市のすべての郵便番号を表示し、正しい郵便番号をクリックしてから、**[!UICONTROL Include]**&#x200B;または&#x200B;**[!UICONTROL Exclude]**&#x200B;をクリックします。</li><li>「**[!UICONTROL Paste postal code]**」タブをクリックし、国を選択し、コンマ区切りの値を入力または貼り付け、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;をクリックします。</li></ul></li></ul> | はい |
| [!UICONTROL Inventory Targeting] | 目標として含めるか除外するインベントリのソース。 フィードまたはソースを少なくとも1つ選択してください。 | はい |
| [!UICONTROL Site/App Targeting] | ターゲットとして含める、または除外するweb サイトとアプリ。 1行につき1つのURLを入力し、**[!UICONTROL Include All]**&#x200B;または&#x200B;**[!UICONTROL Exclude All]**&#x200B;をクリックします。 | いいえ |
| [!UICONTROL Audience Targeting] | ターゲットとして含める、または除外するオーディエンス。 | いいえ |
| [!UICONTROL Ad duration] | プランで考慮する広告の期間。 | いいえ |

>[!MORELIKETHIS]
>
>* [DSP [!UICONTROL Planner] ツールについて](planner-about.md)
>* [ コネクテッド TV リーチ プランの作成](planner-create.md)
>* [ コネクテッド TV リーチ プランを複製](planner-duplicate.md)
>* [ コネクテッド TV リーチ プランの編集](planner-edit.md)
>* [ コネクテッド TV リーチ プランの書き出し](planner-export.md)
>* [ コネクテッド TV リーチ プランの予測を再生成](planner-forecast.md)
>* [ コネクテッド TV リーチ プランのアーカイブ ](planner-archive.md)
