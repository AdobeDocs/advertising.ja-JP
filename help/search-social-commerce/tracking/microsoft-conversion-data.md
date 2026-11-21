---
title: '[!DNL Microsoft Advertising] コンバージョンデータ'
description: Search, Social, & Commerceで利用できる[!DNL Microsoft Advertising] トラッキングされたコンバージョンデータの種類について説明します。
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
TQID: 'https://experienceleague.adobe.com/ZK-uDqw0sThnMzX6bdR-d33gh-AlLTaytJr1fS7pdgs'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
  - id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
    internal-label: Conversion tracking
subfeature_v2:
  - id: d068b149-b9d1-421c-9033-a51495366ddc
    internal-label: Conversions
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
    internal-label: Reporting
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
    internal-label: Insights
source-git-commit: 76a8d8b448441e4d7380ebc4f007aa8b5a2ab5f5
workflow-type: tm+mt
source-wordcount: '652'
ht-degree: 0%
---
# Search, Social, &amp; Commerceの[!DNL Microsoft Advertising] コンバージョンデータ

Search, Social, &amp; Commerceは、[[!DNL Microsoft Advertising]  ユニバーサルイベントトラッキング（UET）タグ ](https://help.ads.microsoft.com/#apex/ads/en/53056)によって追跡されたすべてのコンバージョンを、ビュースルーコンバージョンを含むweb サイトコンバージョン用に自動的に同期し、レポートと最適化を行います。

すべての指標は、キャンペーン管理ビューと基本レポートで自動的に使用でき、ポートフォリオ目標で使用して[!DNL Microsoft Advertising] キャンペーンを最適化することもできます。

## 利用可能なコンバージョンデータ

「[!DNL Include in 'Conversions']」オプションが有効になっているコンバージョンのSearch, Social, &amp; Commerceはデータを同期し、過去35日間のデータを引き出した後、広告主のタイムゾーンの09:00-10:00までに毎日データに変更を引き出します。 過去のデータは、クリックごとに新しいコンバージョンを追跡するため、日々変化します。

[[!DNL Microsoft Advertising]で追跡されたコンバージョン ](https://help.ads.microsoft.com/apex/index/3/en-us/n5012)ごとに2つの指標（[!DNL Microsoft Advertising]で設定）が、Search, Social, &amp; Commerceで自動的に利用でき、[!DNL Microsoft Advertising]で設定されたコンバージョン名を使用します。 各コンバージョンの指標には、次のようなものがあります。

* `<conversion-name>` — キーワードのコンバージョン値（購入など）。

  >[!TIP]
  >
  >このタイプのコンバージョン指標は、最大コンバージョン値とターゲット ROAS入札戦略を含む[!DNL Microsoft Advertising] キャンペーンを含むポートフォリオの目的で使用します。

* `CT_<conversion-name>` — 「CT_」接頭辞（CT_Purchaseなど）で始まるコンバージョンの数（カウント）。

  >[!TIP]
  >
  >このタイプのコンバージョン指標は、最大コンバージョン数とターゲット CPA入札戦略を含む[!DNL Microsoft Advertising] キャンペーンを含むポートフォリオの目的で使用します。

クリック時間と、機能がアカウントに対して有効になっている日付からのコンバージョン/トランザクション時間に基づいて、データを利用できます。

[!DNL Microsoft Advertising]は、各コンバージョンを[入札単位](/help/search-social-commerce/glossary.md#a-b)、デバイス、クリック日（コンバージョン日ではなく）で記録します。 アトリビューションは、[!DNL Microsoft Advertising]の各指標のデフォルトのアトリビューション設定に基づいています。クリックイベントレベルのデータが利用できないため、Adobe Advertising アトリビューションは考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingでコンバージョン名が重複する場合があります。 この問題が発生した場合は、[!UICONTROL Goals] > [!UICONTROL Conversions]の重複する指標の1つに対して、[表示名](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#change-the-display-name-for-a-conversion-metric)を変更します。 2つの異なる指標が同じ名前を持つ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、広告ネットワークのデータと同じレベルのデータと一致します。 しかし、より高いレベルの広告ネットワーク独自のコンバージョンデータには、子入札単位に起因しない追加のコンバージョンが含まれる場合があります。 Search, Social, &amp; Commerceのデータは常に入札単位レベルからロールアップされるため、例えば、キャンペーンレベルのレポートは、広告ネットワークのキャンペーンレベルのレポートと同じ合計が表示されない場合があります。
>* 通常、追加のコンバージョンがまだ同期されていない場合、朝の同期後よりもデータの分散が少なくなります。 午前中にデータを検証することをお勧めします。
>* データはオーディエンスや地理的な場所レベルでは利用できないため、RLSAや場所の入札調整の自動最適化には使用されません。

## [!DNL Microsoft Advertising]のコンバージョンデータをSearch, Social, &amp; Commerceのデータと比較する方法

次のレポート設定を使用して、同等のデータを検証します。

### [!DNL Microsoft Advertising]で使用するレポート設定

選択したコンバージョンアクションのレポートを日別に生成し、すべての広告ステータスのデータを含めます。

### Search, Social, &amp; Commerceで使用するレポート設定

Search, Social, &amp; Commerceでは、「表示」または「レポート」オプションを使用して、クリック日（取引日ではなく）に基づいてコンバージョンを表示します。

1. メインメニューで、**[!UICONTROL Reports]>[!UICONTROL Reports]**&#x200B;をクリックします。

1. **[!UICONTROL Create Report]**&#x200B;をクリックし、左側のパネルの&#x200B;**[!UICONTROL Basic Reports]**&#x200B;をクリックして、**[!UICONTROL Search Engine Account Report]**&#x200B;を選択します。 **[!UICONTROL Proceed]**&#x200B;をクリックします。

1. [!UICONTROL Create Report] ウィンドウで、**[!UICONTROL Basic Settings]** タブを開き、次の[ レポート設定](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)を指定します。

   1. **[!UICONTROL Data Aggregation]**&#x200B;を&#x200B;**[!UICONTROL Daily]**&#x200B;に設定します。

   1. **[!UICONTROL Conversions Based on]**&#x200B;を&#x200B;**[!UICONTROL Click date]**&#x200B;に設定します。

   1. [!DNL Microsoft Advertising] レポートに使用したのと同じ日付範囲を指定してください。

   1. **[!UICONTROL Search/Content]**&#x200B;を&#x200B;**[!UICONTROL Search Only]**&#x200B;に設定します。

   1. **[!UICONTROL Filter By]**&#x200B;が表示されている場合は、**[!UICONTROL Search engine]**&#x200B;を選択します。

   1. **[!UICONTROL Search Engine Hierarchy]**&#x200B;で、[!DNL Microsoft Advertising]を展開し、比較するアカウントの横にあるチェックボックスを選択します。 **[!UICONTROL Add selected items]**&#x200B;をクリックして、アカウントを&#x200B;**[!UICONTROL Selected Filters]**&#x200B;に移動します。

1. 「**[!UICONTROL Columns]**」タブを開き、比較する[!DNL Microsoft Advertising]指標を追加します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンを設定](/help/search-social-commerce/getting-started/campaign-implementation-overview.md)
>* [ キャンペーンとポートフォリオの管理について](/help/search-social-commerce/manage/manage-about.md)
>* [広告主に対して追跡されたコンバージョン指標を表示](/help/search-social-commerce/goals/conversions/conversion-metrics-manage.md#view-the-conversion-metrics-tracked-for-an-advertiser)
