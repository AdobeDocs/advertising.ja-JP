---
title: EF IDを使用したデータフィードのデータ要件
description: EF IDを使用してデータフィードのデータ要件を参照します。
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
TQID: https://experienceleague.adobe.com/p66X8xVlx-JwKjGgXxonJRRu78Q8F4109VkaIVtUbwU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 261
ht-degree: 0%

---

# EF IDを使用したデータフィードのデータ要件

以下は、フィードファイルの各タイプに必要なヘッダーフィールドと対応するデータフィールドです。

>[!NOTE]
>* ヘッダーは、後続の行のデータが同じ順序に従う限り、任意の順序で指定できます。 ヘッダーを含まない場合、データ行の順序は各フィードファイルと一致している必要があります。
>* フィードファイルの各行には1つのトランザクションのデータを含める必要があり、トランザクションはAdobe Advertisingで生成されたef_id （トークン）で識別する必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| EF ID | 大文字と小文字を区別する文字列 | トランザクションのクリック時にキャプチャしたef_id （トークン）。サーファーID、クリック時間、ネットワークタイプで構成されます。 値を変更しないでください。 |
| トランザクション ID | 大文字と小文字を区別する文字列 | （オプションですが推奨）広告主生成のトランザクション ID。 ef_idを使用してリダイレクト時にトランザクションを追跡する場合でも、これを各トランザクションに含めることがベストプラクティスです。 |
| 取引日 | DateTime | トランザクションの日付。 形式は、各トランザクションで一貫している必要があります。 |
| クライアント固有のコンバージョン | 文字列 | トラッキング対象のコンバージョン（取引タイプや金額など）。 フィードを開始する前に、Adobe Advertising実装チームに含めるコンバージョンについて話し合います。 |

## 例

次のサンプルファイルには、2つのコンバージョン指標（製品と収益）のデータが含まれています。

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [変換フィード ファイルの必要ファイル数](feed-file-requirements.md)
>* [EF ID フィードを使用したコンバージョンの追跡](/help/search-social-commerce/tracking/feed-efid.md)
