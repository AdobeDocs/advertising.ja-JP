---
title: 利用可能 [!DNL Google Analytics] 指標
description: 参照先 [!DNL Google Analytics] 指標がデータソースで使用できる。
role: User, Admin
exl-id: f7ac93e3-1aed-4165-ae65-7966ca192c84
source-git-commit: ec7d7f5531c038eb772339a36d13208fc97d2728
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 付録 — 利用可能 [!DNL Google Analytics] 指標

以下の指標は、特に記載の除外を除き、 [!DNL Google Analytics].

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| カテゴリ | 除外済み | コメント |
| ---- | ---- | ---- |
| \[ すべて\] | データタイプが「PERCENT」の指標 | 割合として表示される指標は、常に除外されます。 |
| ユーザー | ga:1dayUsers, ga:7dayUsers, ga:14dayUsers, ga:28dayUsers, ga:sessionsPerUser | — |
| セッション | ga:uniqueDimensionCombinations | — |
| 目標コンバージョン | — | — |
| ページトラッキング | ga:entrices, ga:timeOnPage, ga:exits | — |
| 内部検索 | — | 内部検索のすべての指標のわかりやすい名前の前には、値「InternalSearch:&quot; |
| イベント追跡 | — | — |
| e コマース | — | — |
| ソーシャルインタラクション | — | — |
| 例外 | — | — |
| カスタム変数または列 | ga:calcMetric_* | 計算指標は常に除外されます。 |

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics] コンバージョン指標](data-source-about.md)
>* [の設定の前提条件 [!DNL Google Analytics] データソース](data-source-prerequisites.md)
>* [の設定 [!DNL Google Analytics] データソースとして表示](data-source-configure.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [の再認証 [!DNL Google Analytics] データソース](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] データソース設定](data-source-settings.md)
