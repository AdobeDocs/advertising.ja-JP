---
title: 使用可能な [!DNL Google Analytics] 指標
description: データソースで使用できる [!DNL Google Analytics] 指標を参照します。
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/hRYeNcQu4uUTCAHXcF9zaZfQm-mw6kDlqvs2AxZhED8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 131
ht-degree: 0%

---

# 付録 – 使用可能な[!DNL Google Analytics]指標

次の指標は、記載されている除外事項を除き、[!DNL Google Analytics]のお客様の実装で有効になっている場合に使用できます。

<!--
 Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| カテゴリ | 除外 | コメント |
| ---- | ---- | ---- |
| \[All\] | 「PERCENT」のデータタイプを持つ指標 | パーセンテージとして表示される指標は常に除外されます。 |
| ユーザー | ga:1dayUsers、ga:7dayUsers、ga:14dayUsers、ga:28dayUsers、ga:sessionsPerUser | — |
| セッション | ga:uniqueDimensionCombinations | — |
| 目標のコンバージョン | — | — |
| ページトラッキング | ga:entrances、ga:timeOnPage、ga:exits | — |
| 内部検索 | — | 内部検索のすべての指標のわかりやすい名前には、値「InternalSearch:」が先頭に付けられます |
| イベントトラッキング | — | — |
| e コマース | — | — |
| 社会的交流 | — | — |
| 例外 | — | — |
| カスタム変数または列 | ga :calcMetric_* | 計算指標は常に除外されます。 |

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics]  コンバージョン指標](data-source-about.md)
>* [&#x200B; データソースを設定するための前提条件 [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースとして [!DNL Google Analytics]  ビューを設定](data-source-configure.md)
>* [&#x200B; データソースの編集 [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期を一時停止](data-source-pause.md)
>* [&#x200B; データソースを再認証 [!DNL Google Analytics] します](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定](data-source-settings.md)
