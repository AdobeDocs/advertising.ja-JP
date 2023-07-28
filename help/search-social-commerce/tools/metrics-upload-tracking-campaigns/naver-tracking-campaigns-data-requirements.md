---
title: のトラフィック指標とコンバージョン指標のデータ要件 [!DNL Naver] トラッキング専用アカウント
description: 次のデータアップロード要件を参照します。 [!DNL Naver] トラッキング専用のアカウント。
exl-id: 6f79730b-f8d6-4a7f-9d31-f42fe63e6b5d
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 0%

---

# 次の指標データ要件： [!DNL Naver] トラッキング専用アカウント

以下は、のデータ要件です。 [!DNL Naver] トラッキング専用アカウントのトラフィック指標とコンバージョン指標。

データファイルは TSV、CSV、TXT 形式である必要があります。

次のヘッダーフィールドは必須およびオプションです。 各データ行には、1 つ以上の指標フィールドに対する日別の集計値を含める必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| 期間 | DateTime | データを適用する日付（形式） `YYYY.MM.DD.` ( 例： `2019.11.15.`（日の後の期間） |
| Campaign | 大文字と小文字を区別する文字列 | キャンペーン名。 |
| Adgroup（1 語） | 大文字と小文字を区別する文字列 | 広告グループ名。 |
| キーワード | 大文字と小文字を区別する文字列 | （キーワード広告）広告を生成したキーワード。 |
| [指標] | 整数 | （オプション） [指標が何を測定していても].</br><br>標準指標には、インプレッション数、コストおよびクリック数が含まれます。 広告ネットワークから必要な指標を追加できます。 各指標を別々の列に含めます。<br><br><b>メモ：</b><ul><li>コストの列見出しは「Cost (KRW)」にする必要がある。</li><li>ブランド広告のコスト (KRW) を含めるには、固定月額コストを広告グループレベルで日別に手動で割ります。</li><li>標準指標の値からすべてのコンマを削除します。 例えば、1,000 ではなく、1000 を使用します。</li><li>null 値の場合は、0 を使用します。</li></ul> |

>[!MORELIKETHIS]
>
>* [実装方法 [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [付録 — の必須バルクシートデータ [!DNL Naver] アカウント](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md))
>* [次のトラフィック指標とコンバージョン指標をアップロード： [!DNL Naver] トラッキング専用アカウント](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
