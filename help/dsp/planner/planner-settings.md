---
title: 接続済み TV リーチプランの設定
description: 接続された TV リーチプランの設定の説明を参照してください。
feature: DSP Planner
exl-id: 65edd6f5-557c-44d1-a0ed-8cd26d8a2f6e
source-git-commit: 8574d76fd322cb1cbc6aaaf316e7ad2f961a9f6c
workflow-type: tm+mt
source-wordcount: '289'
ht-degree: 0%

---

# 接続済み TV リーチプランの設定

| パラメーター | 説明 | 必須？ |
| --- | --- | --- |
| 名前 | プランを識別する名前。 | はい |
| 広告主 | プランを作成するアカウント内の特定の広告主。 | はい |
| メディアタイプ | プランに含めるメディアのタイプ。<br><br>現在は、 [!UICONTROL Connected TV] が使用可能です。 | はい |
| 日付範囲 | プランの開始日と終了日。<br><br>開始日を現在の日付より前にすることはできません。 日付範囲は 90 日以下にする必要があります。 | はい |
| 目標タイプ | 目標のタイプ ( [!UICONTROL Budget]) を使用して、計画について検討する必要があります。<br><br>現在は、 [!UICONTROL Budget] が使用可能です。 | はい |
| 目標値 | 予測の目標値。 より正確な予測結果を得るには、5000 USD を超える値を使用してください。 | はい |
| 最大入札額 | 1000 インプレッションに対して支払う最大金額。 次の場合、 [!UICONTROL Connected TV] メディアタイプが選択されている場合は、10 USD 以上の値を入力してください。 | はい |
| 頻度キャップ | 一意の世帯が広告を提供する回数。<br><br>プランを実装し、複数の配置を作成する必要がある場合は、配置レベルではなくパッケージレベルで頻度キャップ設定を適用して、適切な配信を確実におこないます。 | はい |
| GeoTargeting | ターゲットとして含めるまたは除外する場所。 | はい |
| 在庫のターゲティング | ターゲットとして含める、または除外する在庫ソース。 1 つ以上のフィードまたはソースを選択してください。 | はい |
| オーディエンスのターゲティング | ターゲットとして含める、または除外するオーディエンス。 | いいえ |
| 広告期間 | プランで考慮する広告の期間。 | いいえ |

>[!MORELIKETHIS]
>
>* [DSP Planner ツールについて](planner-about.md)
>* [接続済み TV リーチプランの作成](planner-create.md)
>* [接続済み TV リーチプランの複製](planner-duplicate.md)
>* [接続済み TV リーチプランの編集](planner-edit.md)
>* [接続済み TV リーチプランの書き出し](planner-export.md)
>* [接続された TV リーチプランの予測を再生成する](planner-forecast.md)
>* [接続された TV リーチプランをアーカイブ](planner-archive.md)
