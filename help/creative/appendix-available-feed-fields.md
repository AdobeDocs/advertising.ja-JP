---
title: 動的広告フィードファイルで使用可能なフィールド
description: 動的広告の作成に使用するフィードファイルに含めることができるフィールドについて説明します。
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
source-git-commit: 5bf0474f49160775d31dff0d434ba1e069f27959
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 付録：動的広告フィードファイルで使用可能なフィールド

次のフィードフィールドをAdvertising Creative バックエンドで使用できます。 組織固有のフィールド名を使用する [ フィードファイル ](/help/creative/feeds/asset-manage.md) をアップロードできます。 ただし、フィードファイルから [ カタログ ](/help/creative/feeds/catalog-manage.md) を作成する前に、フィードファイルの各フィールドを、カタログの作成に使用する [ フィードテンプレート ](/help/creative/feeds/feed-template-manage.md) の次のいずれかのフィールドにマッピングする必要があります。

フィードファイルに同等の機能が必要なフィールドは、`PART_NUM` のみです。

<!-- Questions:

What are these?
Rank
PROFILE_FILTER fields



Do geo fields need be populated as follows:
Country: 2 Letter country code (example: US)
State: state code_2 letter country code (example: CA_US)
City: City name_State code_2 letter country code (example: San Jose_CA_US)
DMA: DMA _2 letter country code (example: 201_US)
Zipcode: Zip code_2 letter country code (example: 94086_US)


TRUE?   GEO fields(Country/State/City/DMA/Zip), UT fields (UT1/UT2/UT3/UT4/UT5) [do we have an equivalent now?], Filtering fields(F1/F2/F3/F4/F5) can have comma separated values. We can have upto 2K characters.

TRUE FOR CSV AND TSV? character encoding on text format files should be UTF-8 -- If yes, then add that with feed file requirements.

-->

| フィールド名 | データタイプ | 必須？ |
|------------|-----------|-----------|
| 広告サイズ | varchar （32） | 不可 |
| ADDITIONAL_PRICE_1 | decimal （10,2） | 不可 |
| ADDITIONAL_PRICE_2 | decimal （10,2） | 不可 |
| ADDITIONAL_PRICE_3 | decimal （10,2） | 不可 |
| AREA_CODE | text | 不可 |
| AUDIENCE_SEGMENT | text | 不可 |
| AUDIO_1 | varchar （1024） | 不可 |
| AUDIO_2 | varchar （1024） | 不可 |
| AUDIO_3 | varchar （1024） | 不可 |
| AUDIO_4 | varchar （1024） | 不可 |
| AUDIO_5 | varchar （1024） | 不可 |
| 市区町村 | text | 不可 |
| 国 | text | 不可 |
| CREATIVE_ATTRIBUTE_1 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_2 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_3 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_4 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_5 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_6 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_7 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_8 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_9 | varchar （256） | 不可 |
| CREATIVE_ATTRIBUTE_10 | varchar （256） | 不可 |
| DATAPASS_FILTER_1 | text | 不可 |
| DATAPASS_FILTER_2 | text | 不可 |
| DATAPASS_FILTER_3 | text | 不可 |
| DATAPASS_FILTER_4 | text | 不可 |
| DATAPASS_FILTER_5 | text | 不可 |
| DISCOUNT_PRICE | decimal （10,2） | 不可 |
| DMA | text | 不可 |
| 画像 | varchar （1024） | 不可 |
| IMAGE_1 | varchar （1024） | 不可 |
| IMAGE_2 | varchar （1024） | 不可 |
| IMAGE_3 | varchar （1024） | 不可 |
| IMAGE_4 | varchar （1024） | 不可 |
| IMAGE_5 | varchar （1024） | 不可 |
| IMAGE_6 | varchar （1024） | 不可 |
| IMAGE_7 | varchar （1024） | 不可 |
| IMAGE_8 | varchar （1024） | 不可 |
| IMAGE_9 | varchar （1024） | 不可 |
| IMAGE_10 | varchar （1024） | 不可 |
| IMAGE_HEIGHT | int | 不可 |
| IMAGE_WIDTH | int | 不可 |
| IS_DEFAULT | 列挙 | 不可 |
| 言語 | text | 不可 |
| PART_NUM | varchar （64） | はい |
| 価格 | decimal （10,2） | 不可 |
| 製品_名前 | text | 不可 |
| PRODUCT_URL | text | 不可 |
| PROFILE_FILTER_1 | text | 不可 |
| PROFILE_FILTER_2 | text | 不可 |
| PROFILE_FILTER_3 | text | 不可 |
| PROFILE_FILTER_4 | text | 不可 |
| PROFILE_FILTER_5 | text | 不可 |
| ランク | int | 不可 |
| 状態 | text | 不可 |
| TEXT_1 | text | 不可 |
| TEXT_2 | text | 不可 |
| TEXT_3 | text | 不可 |
| TEXT_4 | text | 不可 |
| TEXT_5 | text | 不可 |
| TEXT_6 | text | 不可 |
| TEXT_7 | text | 不可 |
| TEXT_8 | text | 不可 |
| TEXT_9 | text | 不可 |
| TEXT_10 | text | 不可 |
| TEXT_11 | text | 不可 |
| TEXT_12 | text | 不可 |
| TEXT_13 | text | 不可 |
| TEXT_14 | text | 不可 |
| TEXT_15 | text | 不可 |
| VIDEO_1 | varchar （1024） | 不可 |
| VIDEO_2 | varchar （1024） | 不可 |
| VIDEO_3 | varchar （1024） | 不可 |
| VIDEO_4 | varchar （1024） | 不可 |
| VIDEO_5 | varchar （1024） | 不可 |
| 郵便番号 | text | 不可 |

>[!MORELIKETHIS]
>
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ アセットファイルの管理 ](/help/creative/feeds/asset-manage.md)
>* [ フィードテンプレートの管理 ](/help/creative/feeds/feed-template-manage.md)
>* [ カタログの管理 ](/help/creative/feeds/catalog-manage.md)
