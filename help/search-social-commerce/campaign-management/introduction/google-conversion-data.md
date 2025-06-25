---
title: '[!DNL Google Ads] コンバージョンデータ'
description: 検索、ソーシャル  [!DNL Google Ads] よびCommerceで使用できるトラッキング対象コンバージョンデータのタイプについて説明します。
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceでの [!DNL Google Ads] コンバージョンデータ

検索、ソーシャル、Commerceでは、サー [!DNL Google Ads] ス検索およびショッピングネットワーク上のすべてのキャンペーンについて、トラッキングされ [!DNL Google Ads] いコンバージョンデータを検索、ソーシャル、Commerceに自動的に同期し、レポートと最適化を行います。

すべての指標は、キャンペーン管理ビューや基本レポートで自動的に使用でき、最適化のポートフォリオ目標でも使用できます。

## 使用可能なコンバージョンデータ

「[!DNL Include in 'Conversions']」オプションが有効になっているコンバージョンのデータを検索、ソーシャル、Commerceで同期し、過去 35 日間のデータを取り込んでから、広告主のタイムゾーンで毎日 09:00-10:00 ずつデータへの変更を取り込みます。 クリックごとに新しいコンバージョンが追跡されるので、履歴データは日ごとに変更される可能性があります。

[!DNL Google Ads] で設定したコンバージョン名を使用して ](https://support.google.com/google-ads/answer/4677036)[[!DNL Google Ads] で追跡した各コンバージョンに対して最大 3 つの指標（[!DNL Google Ads] で設定）を検索、ソーシャル、Commerceで自動的に使用できます。 各コンバージョンの指標は次のとおりです。

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — （追跡する場合）「GGL」プレフィックスで始まるキーワードのコンバージョン値（GGL 購入など）。

* `GGL_CT*` — 「GGL_CT」プレフィックス（GGL_CT_Purchase など）で始まるコンバージョンの数（カウント）。

* `GGL_XD_CT*` — （コンバージョンタイプに使用可能な場合は、トラッキング時）Googleで測定された、クロスデバイスコンバージョンの数（カウント）。「GGL_XD_CT_」プレフィックスで始まる（GGL_XD_CT_Purchase など）。

[!DNL Google Ads] は、各コンバージョンを [ 入札単位 ](/help/search-social-commerce/glossary.md#a-b)、デバイス、およびクリック日（コンバージョン日ではなく）で記録します。 アトリビューションは、[!DNL Google Ads] の各指標のデフォルトのアトリビューション設定に基づいています。クリックイベントレベルのデータは利用できないので、Adobe Advertising アトリビューションは考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingに重複したコンバージョン名が表示されることがあります。 この場合は、[!UICONTROL Admin] > [!UICONTROL Conversions] のいずれかの重複する指標に対して [ 表示名を変更 ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) します。 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、同じレベルの [!DNL Google Ads] のデータと照合されます。 ただし、上位レベルの [!DNL Google Ads] 独自のコンバージョンデータには、子入札単位に関連付けられていない追加のコンバージョンが含まれる場合があります。 検索、ソーシャルおよびCommerceのデータは、入札単位レベルから常にロールアップされるので、例えば、キャンペーンレベルのレポートとGoogle Ads のキャンペーンレベルのレポートの合計が異なる場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない日の遅い時間よりも朝の同期後の時間が短くなります。 午前中にデータを検証することをお勧めします。
>* コンバージョンデータは、[!DNL Google Display Network]、[!DNL Gmail]、[!DNL Mobile App]、[!DNL YouTube] の広告には使用できません。 [!DNL Google Ads] のデータを検索、ソーシャル、Commerceのデータと比較する際に、これらのタイプの広告を除外できます。
>* [!DNL Google Ads] コンバージョンのデータは、オーディエンスまたは地理的な場所レベルでは使用できないので、RLSA と場所の入札調整を自動最適化するためには使用されません。

## [!DNL Google Ads] のコンバージョンデータを検索、ソーシャル、Commerceのデータと比較する方法

検索、ソーシャル、Commerceのデータと [!DNL Google Ads] のデータを比較する場合は、「表示」または「レポート」オプションを使用して、（取引日ではなく）クリック日に基づいてコンバージョンを表示できます。

次のレポート設定を使用して、同等のデータを検証します。

### [!DNL Google Ads] で使用するレポート設定

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

### 検索、ソーシャル、Commerceで使用するレポート設定

検索、ソーシャル、Commerceでは、「表示」または「レポート」オプションを使用して、（取引日ではなく）クリック日に基づくコンバージョンを表示できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Insights & Reports]/[!UICONTROL Reports]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Create Report]**] をクリックし、カーソルを **[!UICONTROL Basic Reports]** の上に置き、[**[!UICONTROL Search Engine Account Report]**] をクリックします。

1. [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. 「次の **[!UICONTROL Conversions Based]**」セクションで、「**[!UICONTROL Click date]**」を選択します。

   1. [!DNL Google Ads] レポートと同じ日付範囲を指定します。

   1. 「**[!UICONTROL Search/Content]**」セクションで、「**[!UICONTROL Search Only]**」を選択します。

   1. 「**[!UICONTROL Search Engine Hierarchy]**」セクションで、「[!UICONTROL Google Adwords]」セクションを展開し、アカウントを選択します。

   1. 「[!UICONTROL Columns]」タブを開き、比較する [!DNL Google Ads] 指標（「GGL」で始まる）を追加します。

1. 「**[!UICONTROL Create]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 広告ネットワークアカウントとキャンペーンの実装の概要 ](campaign-implemention-overview.md)
>* [ 広告ネットワークキャンペーンのパフォーマンスの監視と管理 ](monitor-performance-campaigns.md)
>* [ 広告主について追跡されたコンバージョン指標の表示 ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [ のコンバージョンタグの作成  [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化 ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
