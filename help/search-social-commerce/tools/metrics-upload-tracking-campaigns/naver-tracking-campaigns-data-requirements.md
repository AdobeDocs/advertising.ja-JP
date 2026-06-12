---
title: ' [!DNL Naver]  トラッキング専用アカウントのトラフィックとコンバージョン指標のデータ要件'
description: ' [!DNL Naver]  トラッキング専用アカウントのデータアップロード要件を参照してください。'
exl-id: cc8ee5de-2bf2-48fd-9fa7-28421aed673f
feature: Search Tools
TQID: https://experienceleague.adobe.com/e4n2ab469CRIiEmqq5wd97pXSQZ9Dt-tehqJSp125GU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# [!DNL Naver]個のトラッキング専用アカウントの指標データ要件

トラッキング専用アカウントの[!DNL Naver] トラフィックとコンバージョン指標のデータ要件を次に示します。

データファイルは、TSV、CSV、またはTXT形式である必要があります。

次のヘッダーフィールドは必須およびオプションです。 各データ行には、少なくとも1つの指標フィールドの日別集計された値を含める必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| 期間 | DateTime | データが適用される日付（形式`YYYY.MM.DD.`、`2019.11.15.`など、日後の期間）。 |
| キャンペーン | 大文字と小文字を区別する文字列 | キャンペーン名。 |
| Adgroup （1語として） | 大文字と小文字を区別する文字列 | 広告グループ名。 |
| キーワード | 大文字と小文字を区別する文字列 | （キーワード広告）広告を生成したキーワード。 |
| [指標] | 整数 | （オプション）指標の測定値&rbrack;に対する&lbrack;の数。</br><br>標準指標には、インプレッション数、コスト数、クリック数などがあります。 広告ネットワークに追加する指標を含めることができます。 各指標を別の列に含めます。<br><br><b> メモ：</b><ul><li>コストの列ヘッダーは「コスト（KRW）」である必要があります。</li><li>ブランド広告のコスト（KRW）を含めるには、広告グループレベルで固定月額費用を日で手動で割ります。</li><li>標準指標の値からすべてのコンマを削除します。 例えば、1,000ではなく1000を使用します。</li><li>null値の場合は、0を使用します。</li></ul> |

>[!MORELIKETHIS]
>
>* [&#x200B; トラッキング専用アカウントを実装 [!DNL Naver] します](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [付録 –  [!DNL Naver]  アカウント &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-data-naver.md)に必要なバルクシート データ
>* [&#x200B; トラッキング専用アカウント  [!DNL Naver] のトラフィックとコンバージョン指標をアップロード &#x200B;](/help/search-social-commerce/tools/metrics-upload-tracking-campaigns/naver-tracking-campaigns-upload-metrics.md)
