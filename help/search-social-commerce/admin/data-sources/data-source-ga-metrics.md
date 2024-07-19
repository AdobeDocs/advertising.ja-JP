---
title: Available [!DNL Google Analytics] metrics
description: データソースで使用可能な  [!DNL Google Analytics]  指標を参照します。
role: User, Admin
exl-id: 434c569d-7869-4874-90a5-5af18bc8157e
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 0%

---

# 付録 – 使用可能な [!DNL Google Analytics] 指標

次の指標は、[!DNL Google Analytics] でお客様の実装で有効になっている場合は、記載されている除外を除いて使用できます。

<!-- Notes as FYI to self:
>[!NOTE]
>
>* For some of these metrics, [!DNL Google] assigns the friendly name, and the name is consistent. For some metrics, the advertiser assigns the friendly name in [!DNL Google Analytics], and the name has a dynamic value.
>* Some metrics are assigned at the property level, and others are assigned at the view level.
-->

| カテゴリ | 除外済み | コメント |
| ---- | ---- | ---- |
| \[ すべて\] | データタイプが「PERCENT」の指標 | パーセンテージとして表示される指標は、常に除外されます。 |
| ユーザー | ga:1dayUsers、ga:7dayUsers、ga:14dayUsers、ga:28dayUsers、ga:sessionsPerUser | — |
| Session | ga:uniqueDimensionCombinations | — |
| 目標コンバージョン | — | — |
| ページトラッキング | ga：エントリ，ga:timeOnPage, ga:exits | — |
| 内部検索 | — | 内部検索のすべての指標のわかりやすい名前の前には、「InternalSearch:」という値が追加されます。 |
| イベントの追跡 | — | — |
| E コマース | — | — |
| ソーシャルインタラクション | — | — |
| 例外 | — | — |
| カスタム変数または列 | ga:calcMetric_* | 計算指標は常に除外されます。 |

>[!MORELIKETHIS]
>
>* [ 同期  [!DNL Google Analytics]  コンバージョン指標について ](data-source-about.md)
>* [ データソースを設定するため  [!DNL Google Analytics]  前提条件 ](data-source-prerequisites.md)
>* [ データソースとして  [!DNL Google Analytics]  ビューを設定する ](data-source-configure.md)
>* [ データソース  [!DNL Google Analytics]  編集 ](data-source-edit.md)
>* [ データソースの同期の一時停止 ](data-source-pause.md)
>* [ データソース  [!DNL Google Analytics]  再認証 ](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定 ](data-source-settings.md)
