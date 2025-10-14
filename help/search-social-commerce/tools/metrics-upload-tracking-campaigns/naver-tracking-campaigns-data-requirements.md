---
title: トラッキング専用アカウントのトラフィックおよびコンバージョン指標  [!DNL Naver]  関するデータ要件
description: トラッキング専用アカウントのデータ  [!DNL Naver]  ップロード要件を参照します。
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 0%

---

# トラッキング専用アカウント [!DNL Naver] 指標データ要件

トラッ [!DNL Naver] ング専用アカウントのトラフィックおよびコンバージョン指標のデータ要件を次に示します。

データファイルは、TSV、CSV、TXT のいずれかの形式にする必要があります。

次のヘッダーフィールドは必須かつオプションです。 各データ行には、少なくとも 1 つの指標フィールドの日次集計値が含まれている必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| 期間 | 日時 | データが適用される日付を、`YYYY.MM.DD.` の形式（`2019.11.15.` など）で指定します。 |
| キャンペーン | 大文字と小文字を区別する文字列 | キャンペーン名。 |
| Adgroup （1 つの単語として） | 大文字と小文字を区別する文字列 | 広告グループ名。 |
| キーワード | 大文字と小文字を区別する文字列 | （キーワード広告）広告を生成したキーワード。 |
| [ 指標 ] | 整数 | （任意）指標が測定している [ 数値 ]。</br><br> 標準指標には、インプレッション数、コスト、クリック数が含まれます。 広告ネットワークから必要な追加の指標を含めることができます。 各指標を別々の列に含めます。<br><br><b> 注：</b><ul><li>コストの列ヘッダーは「コスト （KRW）」にする必要があります。</li><li>ブランド広告のコスト（KRW）を含めるには、固定月額コストを広告グループレベルで手動で日で割ります。</li><li>標準の指標値からすべてのコンマを削除します。 例えば、1,000 の代わりに 1000 を使用します。</li><li>null 値の場合は、0 を使用します。</li></ul> |

>[!MORELIKETHIS]
>
>* [&#x200B; 実装  [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [&#x200B; 付録 – アカウントに必要なバルクシート  [!DNL Naver]  デ &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md) タ）
>* [&#x200B; トラッキング専用アカウントのトラフィックおよびコ  [!DNL Naver]  バージョン指標のアップロード &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
