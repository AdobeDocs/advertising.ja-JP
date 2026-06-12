---
title: トランザクション IDを使用したデータフィードのデータ要件
description: トランザクション IDを使用して、データフィードのデータ要件を参照します。
exl-id: 055b1417-3185-4081-83f0-9f4798058c04
feature: Search Tracking
TQID: https://experienceleague.adobe.com/TONScPVaJyxsORRD-sOrYXwEzO9rsa6ERPUo8oSRono
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 0%

---

# トランザクション IDを使用したデータフィードのデータ要件

以下は、フィードファイルの各タイプに必要なヘッダーフィールドと対応するデータフィールドです。

>[!NOTE]
>* ヘッダーは、後続の行のデータが同じ順序に従う限り、任意の順序で指定できます。 ヘッダーを含まない場合、データ行の順序は各フィードファイルと一致している必要があります。
>* フィードファイルの各行には、1つのトランザクションのデータを含める必要があり、トランザクションはトランザクション IDで識別する必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| トランザクション ID （ev_transid） | 大文字と小文字を区別する文字列 | トランザクションに関連付けられた広告主が生成した識別子。 Adobe Advertising コンバージョントラッキングタグはトランザクションのオンライン部分に使用されるので、これはトランザクションの前の部分にAdobe Advertisingが提供したトランザクション ID （ev_transid）と同じである必要があります。 つまり、トランザクションのオンライン部分のコンバージョンタグには、一意のトランザクション IDのコンバージョン指標を含める必要があります。<br><br>**注意：** Adobe Advertisingは、IDを使用して古いトランザクションデータを検索し、合意された挿入モードに従って更新します（既存のデータを置き換えたり、新しいデータで拡張したりするなど）。 |
| 取引日 | DateTime | トランザクションの日付。 形式は、各トランザクションで一貫している必要があります。 |
| クライアント固有のコンバージョン | 文字列 | トラッキング対象のコンバージョン（取引タイプや金額など）。 フィードを開始する前に、Adobe Advertising実装チームに含めるコンバージョンについて話し合います。 |

## 例

次のサンプルファイルには、2つのコンバージョン指標（製品と収益）のデータが含まれています。

```
Transaction ID,Transaction Date,Product,Revenue
12345,2010-02-17,Coffee,15.00
12346,2010-02-17,Tea,42.00
12347,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [変換フィード ファイルの必要ファイル数](feed-file-requirements.md)
>* [&#x200B; トランザクション ID フィードを使用したコンバージョン追跡](/help/search-social-commerce/tracking/feed-transaction-id.md)
