---
title: EF ID を使用したデータフィードのデータ要件
description: EF ID を使用したデータフィードのデータ要件を参照します。
exl-id: 507ed42c-349f-4311-af61-8f7a27794162
feature: Search Tracking
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# EF ID を使用したデータフィードのデータ要件

ヘッダーフィールドと、フィードファイルのタイプごとに必要な対応するデータフィールドを次に示します。

>[!NOTE]
>* 後続の行のデータが同じ順序に従う限り、ヘッダーは任意の順序になります。 ヘッダーを含めない場合、データ行の順序は各フィードファイルと一致している必要があります。
>* フィードファイルの各行には、1 つのトランザクションのデータが含まれている必要があり、トランザクションはAdobe Advertisingが生成した ef_id （トークン）によって識別される必要があります。

| ヘッダーフィールド/列名 | タイプ | 説明 |
| ---- | ---- | ---- |
| EF ID | 大文字と小文字を区別する文字列 | トランザクションのクリック時にキャプチャした ef_id （トークン）です。このトークンは、サーファー ID、クリック時間、ネットワークタイプで構成されます。 値を変更しないでください。 |
| トランザクション ID | 大文字と小文字を区別する文字列 | （オプションですが推奨）広告主が生成したトランザクション ID。 リダイレクト時にトランザクションを追跡するために ef_id が使用される場合でも、ベストプラクティスはトランザクションごとにこれを含めることです。 |
| トランザクション日 | 日時 | トランザクションの日付。 形式は、トランザクションごとに一貫している必要があります。 |
| クライアント固有の変換 | 文字列 | 追跡中のコンバージョン （トランザクションのタイプや金額など）。 フィードを開始する前に、含めるコンバージョンについてAdobe Advertising導入チームと話し合ってください。 |

## 例

次のファイルのサンプルには、2 つのコンバージョン指標（製品と売上高）のデータが含まれています。

```
EF ID,Client Transaction ID, Transaction Date,Product,Revenue
TIl4VQqoEEQAAG8CU5EAAACY:20100217062449:s,04896325,2010-02-17,Coffee,15.00
SOl5PRKlPEILDG6CL3QYENOI:20100217065632:s,04896490,2010-02-17,Tea,42.00
TRl4BEtoTPMBEW4SU5ZUMEPIE:20100217065804:s,04896552,2010-02-17,Coffee,22.00
```

>[!MORELIKETHIS]
>
>* [ 変換フィードファイルのファイル要件 ](feed-file-requirements.md)
>* [EF ID フィードを使用したコンバージョントラッキング ](/help/search-social-commerce/tracking/feed-efid.md)
