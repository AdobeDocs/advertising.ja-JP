---
title: '[!DNL Google Ads] コンバージョンデータ'
description: Search, Social, & Commerceで利用できる [!DNL Google Ads]追跡されたコンバージョンデータの種類について説明します。
exl-id: a4634410-446b-4e2e-a52f-22a494f731f9
feature: Search Campaign Management, Conversions
TQID: https://experienceleague.adobe.com/7qqQKfVhueHMc7hJDEac86la9dp36hwtrLF5ikxJzJM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 661
ht-degree: 0%

---

# Search, Social, &amp; Commerceの[!DNL Google Ads] コンバージョンデータ

Search, Social, &amp; Commerceは、[!DNL Google Ads]の検索およびショッピングネットワーク上のすべてのキャンペーンに関する[!DNL Google Ads]追跡されたコンバージョンデータを、レポートと最適化のためにSearch, Social, &amp; Commerceに自動的に同期します。

すべての指標は、キャンペーン管理ビューと基本レポートで自動的に使用でき、最適化のためにポートフォリオ目標でも使用できます。

## 利用可能なコンバージョンデータ

「[!DNL Include in 'Conversions']」オプションが有効になっているコンバージョンのSearch, Social, &amp; Commerceはデータを同期し、過去35日間のデータを引き出した後、広告主のタイムゾーンの09:00-10:00までに毎日データに変更を引き出します。 過去のデータは、クリックごとに新しいコンバージョンを追跡するため、日々変化します。

[[!DNL Google Ads]で追跡されたコンバージョン ](https://support.google.com/google-ads/answer/4677036)ごとに最大3つの指標（[!DNL Google Ads]で設定）が、検索、ソーシャル、およびCommerceで、[!DNL Google Ads]で設定されたコンバージョン名を使用して自動的に使用できます。 各コンバージョンの指標には、次のようなものがあります。

<!--

* `<conversion-name>` &mdash; (When you track it) The conversion value for the keyword, beginning with the "GGL" prefix (such as GGL Purchase).

`CT_<conversion-name>` &mdash; The number (count) of conversions, beginning with the "GGL_CT" prefix (such as GGL_CT_Purchase).

* `XD_<conversion-name>` &mdash; (When available for the conversion type, when you track them) The number (count) of cross-device conversions, as measured by Google, beginning with the "GGL_XD_CT_" prefix (such as GGL_XD_CT_Purchase).

-->

* `GGL*` — （トラッキングする場合） 「GGL」プレフィックスで始まるキーワードのコンバージョン値（GGL Purchaseなど）。

* `GGL_CT*` — 「GGL_CT」接頭辞（GGL_CT_Purchaseなど）で始まるコンバージョンの数（カウント）。

* `GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合、トラッキングする場合）クロスデバイスのコンバージョン数（カウント）。Googleで測定され、「GGL_XD_CT_」接頭辞（GGL_XD_CT_Purchaseなど）で始まります。

[!DNL Google Ads]は、各コンバージョンを[入札単位](/help/search-social-commerce/glossary.md#a-b)、デバイス、クリック日（コンバージョン日ではなく）で記録します。 アトリビューションは、[!DNL Google Ads]の各指標のデフォルトのアトリビューション設定に基づいています。クリックイベントレベルのデータが利用できないため、Adobe Advertising アトリビューションは考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingでコンバージョン名が重複する場合があります。 この問題が発生した場合は、[ > ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md)の重複する指標の1つに対して、[!UICONTROL Admin]表示名[!UICONTROL Conversions]を変更します。 2つの異なる指標が同じ名前を持つ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、同じレベルの[!DNL Google Ads]のデータと一致します。 ただし、上位レベルの[!DNL Google Ads]独自のコンバージョンデータには、子入札単位に起因しない追加のコンバージョンが含まれる場合があります。 Search, Social, &amp; Commerceのデータは常に入札単位レベルからロールアップされるため、例えば、キャンペーンレベルのレポートは、Google Adsのキャンペーンレベルのレポートと同じ合計が得られない場合があります。
>* 通常、追加のコンバージョンがまだ同期されていない場合、朝の同期後よりもデータの分散が少なくなります。 午前中にデータを検証することをお勧めします。
>* コンバージョンデータは、[!DNL Google Display Network]、[!DNL Gmail]、[!DNL Mobile App]、[!DNL YouTube]の広告では利用できません。 [!DNL Google Ads]のデータをSearch, Social, &amp; Commerceのデータと比較する際に、これらのタイプの広告をフィルタリングします。
>* [!DNL Google Ads] コンバージョンのデータは、オーディエンスレベルまたは地理的ロケーションレベルでは利用できないため、RLSAとロケーション入札調整の自動最適化には使用されません。

## [!DNL Google Ads]のコンバージョンデータをSearch, Social, &amp; Commerceのデータと比較する方法

Search、Social、およびCommerceのデータと[!DNL Google Ads]のデータを比較する場合は、「表示」または「レポート」オプションを使用して、クリック日（取引日ではなく）に基づいてコンバージョンを表示します。

次のレポート設定を使用して、同等のデータを検証します。

### [!DNL Google Ads]で使用するレポート設定

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

### Search, Social, &amp; Commerceで使用するレポート設定

Search, Social, &amp; Commerceでは、「表示」または「レポート」オプションを使用して、クリック日（取引日ではなく）に基づいてコンバージョンを表示します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで「**[!UICONTROL Create Report]**」をクリックし、**[!UICONTROL Basic Reports]**&#x200B;にカーソルを合わせ、**[!UICONTROL Search Engine Account Report]**&#x200B;をクリックします。

1. [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. セクションの&#x200B;**[!UICONTROL Conversions Based]**&#x200B;で、**[!UICONTROL Click date]**&#x200B;を選択します。

   1. [!DNL Google Ads] レポートに使用したのと同じ日付範囲を指定してください。

   1. **[!UICONTROL Search/Content]** セクションで、**[!UICONTROL Search Only]**&#x200B;を選択します。

   1. **[!UICONTROL Search Engine Hierarchy]** セクションで、[!UICONTROL Google Adwords] セクションを展開し、アカウントを選択します。

   1. [!UICONTROL Columns] タブを開き、比較する[!DNL Google Ads]指標（「GGL」で始まる）を追加します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスを監視および管理](monitor-performance-campaigns.md)
>* [広告主に対して追跡されたコンバージョン指標を表示](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
>* [ [!DNL Google Ads]](/help/search-social-commerce/admin/conversion-metrics/conversion-tag-google.md)のコンバージョンタグを作成
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
