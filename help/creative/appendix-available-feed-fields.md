---
title: 動的な広告フィードファイルに使用できるフィールド
description: 動的広告の作成に使用するフィードファイルに含めることができるフィールドについて説明します。
feature: Creative Dynamic Creatives
exl-id: 9cd3fa29-d4db-4e9f-9ffd-87b44b62a3e2
TQID: https://experienceleague.adobe.com/oBlhGgChyoHBSkfx4gqlC-mnleraVrtf3lMzper7vgY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 391
ht-degree: 0%

---

# 付録：動的な広告フィード ファイルの使用可能なフィールド

Advertising Creative バックエンドでは、次のフィード フィールドを使用できます。 組織固有のフィールド名を使用する[ フィードファイル ](/help/creative/feeds/asset-manage.md)をアップロードできます。 ただし、フィード ファイルから[ カタログ ](/help/creative/feeds/catalog-manage.md)を作成する前に、フィード ファイルの各フィールドを、カタログの作成に使用する[ フィード テンプレート ](/help/creative/feeds/feed-template-manage.md)の次のいずれかのフィールドにマッピングする必要があります。

フィード ファイルに同等のフィールドを含める必要があるのは`PART_NUM`のみです。

<!--
 Questions:

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

| フィールド名 | データタイプ | 必要ですか？ |
|------------|-----------|-----------|
| AD_SIZE | varchar （32） | いいえ |
| ADDITIONAL_PRICE_1 | decimal （10,2） | いいえ |
| ADDITIONAL_PRICE_2 | decimal （10,2） | いいえ |
| ADDITIONAL_PRICE_3 | decimal （10,2） | いいえ |
| AREA_CODE | テキスト | いいえ |
| AUDIENCE_SEGMENT | テキスト | いいえ |
| AUDIO_1 | varchar （1024） | いいえ |
| AUDIO_2 | varchar （1024） | いいえ |
| AUDIO_3 | varchar （1024） | いいえ |
| AUDIO_4 | varchar （1024） | いいえ |
| AUDIO_5 | varchar （1024） | いいえ |
| 市区町村 | テキスト | いいえ |
| 国 | テキスト | いいえ |
| CREATIVE_ATTRIBUTE_1 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_2 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_3 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_4 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_5 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_6 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_7 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_8 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_9 | varchar （256） | いいえ |
| CREATIVE_ATTRIBUTE_10 | varchar （256） | いいえ |
| DATAPASS_FILTER_1 | テキスト | いいえ |
| DATAPASS_FILTER_2 | テキスト | いいえ |
| DATAPASS_FILTER_3 | テキスト | いいえ |
| DATAPASS_FILTER_4 | テキスト | いいえ |
| DATAPASS_FILTER_5 | テキスト | いいえ |
| DISCOUNT_PRICE | decimal （10,2） | いいえ |
| DMA | テキスト | いいえ |
| 画像 | varchar （1024） | いいえ |
| IMAGE_1 | varchar （1024） | いいえ |
| IMAGE_2 | varchar （1024） | いいえ |
| IMAGE_3 | varchar （1024） | いいえ |
| IMAGE_4 | varchar （1024） | いいえ |
| IMAGE_5 | varchar （1024） | いいえ |
| IMAGE_6 | varchar （1024） | いいえ |
| IMAGE_7 | varchar （1024） | いいえ |
| IMAGE_8 | varchar （1024） | いいえ |
| IMAGE_9 | varchar （1024） | いいえ |
| IMAGE_10 | varchar （1024） | いいえ |
| IMAGE_HEIGHT | int | いいえ |
| IMAGE_WIDTH | int | いいえ |
| IS_DEFAULT | 列挙 | いいえ |
| 言語 | テキスト | いいえ |
| PART_NUM | varchar （64） | はい |
| 価格 | decimal （10,2） | いいえ |
| PRODUCT_NAME | テキスト | いいえ |
| PRODUCT_URL | テキスト | いいえ |
| PROFILE_FILTER_1 | テキスト | いいえ |
| PROFILE_FILTER_2 | テキスト | いいえ |
| PROFILE_FILTER_3 | テキスト | いいえ |
| PROFILE_FILTER_4 | テキスト | いいえ |
| PROFILE_FILTER_5 | テキスト | いいえ |
| ランク | int | いいえ |
| 都道府県 | テキスト | いいえ |
| TEXT_1 | テキスト | いいえ |
| TEXT_2 | テキスト | いいえ |
| TEXT_3 | テキスト | いいえ |
| TEXT_4 | テキスト | いいえ |
| TEXT_5 | テキスト | いいえ |
| TEXT_6 | テキスト | いいえ |
| TEXT_7 | テキスト | いいえ |
| TEXT_8 | テキスト | いいえ |
| TEXT_9 | テキスト | いいえ |
| TEXT_10 | テキスト | いいえ |
| TEXT_11 | テキスト | いいえ |
| TEXT_12 | テキスト | いいえ |
| TEXT_13 | テキスト | いいえ |
| TEXT_14 | テキスト | いいえ |
| TEXT_15 | テキスト | いいえ |
| VIDEO_1 | varchar （1024） | いいえ |
| VIDEO_2 | varchar （1024） | いいえ |
| VIDEO_3 | varchar （1024） | いいえ |
| VIDEO_4 | varchar （1024） | いいえ |
| VIDEO_5 | varchar （1024） | いいえ |
| ZIP | テキスト | いいえ |

>[!MORELIKETHIS]
>
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ アセットファイルの管理](/help/creative/feeds/asset-manage.md)
>* [ フィード テンプレートの管理](/help/creative/feeds/feed-template-manage.md)
>* [ カタログの管理](/help/creative/feeds/catalog-manage.md)
