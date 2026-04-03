---
title: 動的なクリエイティブ設定
description: 動的なクリエイティブの設定を参照します。
feature: Creative Dynamic Creatives
exl-id: 9dcd7245-fa02-4082-9abb-8c0792322a68
TQID: https://experienceleague.adobe.com/b7R-MWHypydFbqdZY2sVwvoaq4sxwK5Wcf-OJc5x0LM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# 動的なクリエイティブ設定

<!-- add a description -->

## 動的な広告設定<!-- for dynamic HTML5 ads {#dynamic-ad-settings-dynamic-html5}-->

<!-- add a description -->

### 基本の詳細

**[!UICONTROL Creative Type]:** クリエイティブが&#x200B;*[!UICONTROL Display]*&#x200B;広告（HTML5）か&#x200B;*[!UICONTROL Video]*&#x200B;広告かのどちらかです。

**[!UICONTROL Dynamic Display Ad Name]**&#x200B;または&#x200B;**[!UICONTROL Dynamic Video Ad Name]:** クリエイティブの一意の名前。

**[!UICONTROL Advertiser]:**&#x200B;広告を作成する広告主。 [!UICONTROL Creatives] > [!UICONTROL Creative Libraries]の範囲内で広告を作成する場合、広告主は既に選択されており、読み取り専用です。

**[!UICONTROL Library]:**&#x200B;広告を作成するクリエイティブ ライブラリ。 [!UICONTROL Creatives] > [!UICONTROL Creative Libraries]内から広告を作成する場合、ライブラリ名は既に選択されており、読み取り専用です。

## 広告テンプレート

**[!UICONTROL Ad Template]:**&#x200B;広告の作成元となる広告テンプレート。 既存の広告テンプレートを選択するか、新しい広告テンプレートをアップロードして、テンプレートタイプ （*静的*&#x200B;または&#x200B;*動的*）を選択します。 テンプレートはZIP形式で次を含んでいる必要があります：<!-- Need to add more specs for templates -->

* クリエイティブの表示：目的の広告フォーマットを含むHTML5 ファイルと、広告属性（.tdf）を含むファイル（動的HTML5 adsのみ）

* ビデオクリエイティブ：目的の広告フォーマットを含む.scene ファイル。 ZIP ファイルは最大512 MBです。

続行するには、**[!UICONTROL Select Ad Template]**&#x200B;をクリックします。

**[!UICONTROL Size]:** （動的ディスプレイ広告のみ、読み取り専用）選択した広告テンプレートの[広告ディメンション ](/help/creative/creative-libraries/creative-sizes.md)。広告の作成に使用されます。

**[!UICONTROL Card Count (Max 50)]:** （ディスプレイ広告のみ）カルーセルに表示する商品の数。

**[!UICONTROL Duration]:** （ビデオ広告のみ、読み取り専用）選択した広告テンプレートから派生したビデオのデュレーション。 各ビデオのデュレーションは1 ～ 90秒の間である必要があります。

## カタログ

**\[ カタログ\]**：広告の生成元となる1つ以上のカタログ。 既存のカタログを選択するか、既存のフィードテンプレートをダウンロードして新しいカタログを作成してアップロードすることで、新しいカタログを作成します。 **[!UICONTROL Select Catalog]**&#x200B;をクリックします。

アップロードするカタログはZIP形式で、次のものが含まれている必要があります。

* （動的ディスプレイ広告と動画広告） CSV、TSV、またはMicrosoft Excel スプレッドシート （XLSX）形式の1つ以上のフィードファイル。 最大ファイル サイズは512 MBです。<!-- Need to add more specs for the feed files -->

* （ディスプレイ広告）GIF、JPEG、JPG、またはPNG形式の画像アセット

* （動画広告） MP4、MOV、またはWEBM形式のビデオアセット。 対応している広告テンプレートには、開始カード、終了カード、上オーバーレイ、下オーバーレイ、L字型などがあります。 各ビデオのデュレーションは1 ～ 90秒の間である必要があります。

### [!UICONTROL Attributes Mapping]

**[!UICONTROL Enable targeting]**：広告を作成するために値が存在する必要があるフィードファイルの列のタイプ : *[!UICONTROL Profile data]*、*[!UICONTROL Geographic data]、*[!UICONTROL Data pass]、*[!UICONTROL Audience Segment]*。  **注：**&#x200B;これらの設定は、広告エクスペリエンス設定の詳細設定とは独立して機能します。<!-- Clarify what qualifies for each, and explain more -->

**[!UICONTROL Dynamic Ad Fields]** / **[!UICONTROL Maps to Catalog Labels]:**

指定された広告テンプレートの各属性（動的な広告フィールド）を、指定されたカタログ（カタログラベル）の列にマッピングするか、静的値を入力します。

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリに動的なクリエイティブを追加](creative-add-dynamic.md)
>* [ クリエイティブライブラリでの動的クリエイティブの編集](creative-edit-dynamic.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
