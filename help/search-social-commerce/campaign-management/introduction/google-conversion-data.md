---
title: '[!DNL Google Ads] コンバージョンデータ'
description: 次のタイプについて説明します。 [!DNL Google Ads] — 検索、ソーシャル、コマースで使用できる追跡されたコンバージョンデータ。
exl-id: a7ee8e72-aa7d-4e90-b765-b7b01308762d
feature: Search Campaign Management
source-git-commit: b730716565dfae9cb32556eaede1c3f29f316ac7
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# [!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ

検索、ソーシャル、コマースは自動的に同期します [!DNL Google Ads] — 追跡したコンバージョンデータを [!DNL Google Ads] 検索およびショッピングネットワークを検索、ソーシャル、コマースに分割し、レポートと最適化を行います。

すべての指標は、キャンペーン管理ビューと基本レポートで自動的に使用でき、ポートフォリオ目標で使用して最適化することもできます。

## 使用可能なコンバージョンデータ

検索、ソーシャル、コマースの各データを同期し、「[!DNL Include in 'Conversions']「 」オプションが有効になり、過去 35 日間のデータをプルした後、09 までに毎日データに変更をプルする:00-10:広告主のタイムゾーンの 00。 履歴データは、クリックごとに新しいコンバージョンが追跡されるので、日々変化する場合があります。

それぞれ最大 3 つの指標 [[!DNL Google Ads] — 追跡されたコンバージョン](https://support.google.com/google-ads/answer/4677036) ( [!DNL Google Ads]) は、検索、ソーシャル、コマースで、 [!DNL Google Ads]. 各コンバージョンの指標は次のとおりです。

* `GGL*` — （追跡する場合）キーワードのコンバージョン値で、「GGL」プレフィックスで始まる値（GGL Purchase など）。

* `GGL_CT*` — 「GGL_CT」プレフィックス（GGL_CT_Purchase など）で始まるコンバージョンの数（カウント）。

* `GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合、追跡する場合）Googleが測定する、「GGL_XD_CT_」プレフィックス (GGL_XD_CT_Purchase など ) で始まる、クロスデバイスコンバージョンの数（カウント）。

[!DNL Google Ads] は、各コンバージョンを次のように記録します。 [入札単位](/help/search-social-commerce/glossary.md#a-b)、デバイス、クリック日（コンバージョン日ではなく） アトリビューションは、 [!DNL Google Ads];Adobe Advertising属性は、クリックイベントレベルのデータを使用できないので、考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingに重複したコンバージョン名が表示されることがあります。 これが発生した場合、 [表示名を変更する](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) の指標が重複している場合は、 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、 [!DNL Google Ads] 同じレベルで しかし、 [!DNL Google Ads]上位レベルの「独自のコンバージョンデータ」には、子入札単位に関連付けられない追加のコンバージョンが含まれる場合があります。 検索、ソーシャル、コマースのデータは、常に入札単位レベルからロールアップされるので、例えば、キャンペーンレベルのレポートは、Google Ads のキャンペーンレベルのレポートと同じ合計にならない場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない場合の、午前の同期後の方が、当日の後半よりも少なくなります。 データの検証は、午前中におこなうことをお勧めします。
>* ではコンバージョンデータを使用できません [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App]、および [!DNL YouTube] 広告。 でデータを比較する際に、これらのタイプの広告を除外する [!DNL Google Ads] 検索、ソーシャル、コマースのデータを含む
>* のデータ [!DNL Google Ads] コンバージョンは、オーディエンスまたは地理的な場所レベルでは利用できないので、RLSA や場所の入札調整を自動最適化するためには使用されません。

## でのコンバージョンデータの比較方法 [!DNL Google Ads] 検索、ソーシャル、コマースのデータを含む

検索、ソーシャル、コマースのデータを [!DNL Google Ads]の場合は、「表示」または「レポート」オプションを使用して、（トランザクション日ではなく）クリック日に基づいてコンバージョンを表示します。

次のレポート設定を使用して、同等のデータを検証します。

### で使用するレポート設定 [!DNL Google Ads]

選択したコンバージョンアクションのレポートを日別に生成し、すべての広告ステータスのデータを含めます。

<!-- 

1. In the main toolbar, select **[!DNL Reports] > [!DNL Report]**.

1. Select **[!DNL + Custom] > [!DNL Table]**.

1. From the left pane, specify the rows and columns in the report:
   
   1. Search for the **[!DNL Day]** field and it drag to the [!DNL Row] section.

   1. Search for the **[!DNL All conv].** field and it drag to the [!DNL Column] section.

   1. Search for the **[!DNL Conversion action]** field and it drag to the [!DNL Column] section.

1. In the report settings toolbar, select **[!DNL Filter] > [!DNL Ad status]**, and then select all boxes.

1. In the report settings toolbar, select **[!DNL Download] > [!DNL Excel .csv]**.

-->

### 検索、ソーシャル、コマースで使用するレポート設定

Social および Commerce の検索で、「表示」または「レポート」オプションを使用して、（トランザクション日ではなく）クリック日に基づいてコンバージョンを表示します。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Create Report]**、カーソルを上に置きます。 **[!UICONTROL Basic Reports]**&#x200B;をクリックし、 **[!UICONTROL Search Engine Account Report]**.

1. Adobe Analytics の [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. Adobe Analytics の **[!UICONTROL Conversions Based]** 「 」セクションで、「 」を選択します。 **[!UICONTROL Click date]**.

   1. 次の期間に使用したのと同じ日付範囲を指定します： [!DNL Google Ads] レポート。

   1. Adobe Analytics の **[!UICONTROL Search/Content]** セクション、選択 **[!UICONTROL Search Only]**.

   1. Adobe Analytics の **[!UICONTROL Search Engine Hierarchy]** セクションで、 [!UICONTROL Google Adwords] 」セクションでアカウントを選択します。

   1. を開きます。 [!UICONTROL Columns] タブをクリックし、 [!DNL Google Ads] （「GGL」で始まる）指標を比較します。

1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスの監視と管理](monitor-performance-campaigns.md)
>* [広告主でトラッキングされているトランザクションプロパティの表示](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
