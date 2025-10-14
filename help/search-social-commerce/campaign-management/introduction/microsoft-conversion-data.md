---
title: '[!DNL Microsoft Advertising] コンバージョンデータ'
description: 検索、ソーシャルおよびCommerceで使用できる  [!DNL Microsoft Advertising] 追跡されたコンバージョンデータのタイプについて説明します。
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceでの [!DNL Microsoft Advertising] コンバージョンデータ

検索、ソーシャル、Commerceでは、Web サイトのコンバージョン（ビュースルーコンバージョンを含む）について、レポートや最適化を目的として [[!DNL Microsoft Advertising]  ユニバーサルイベントトラッキング（UET）タグ &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/53056) で追跡されたすべてのコンバージョンを自動的に同期します。

すべての指標は、キャンペーン管理ビューや基本レポートで自動的に使用できるほか、ポートフォリオ目標でも使用してキャンペーンの最適化を行うこと [!DNL Microsoft Advertising] できます。

## 使用可能なコンバージョンデータ

「[!DNL Include in 'Conversions']」オプションが有効になっているコンバージョンのデータを検索、ソーシャル、Commerceで同期し、過去 35 日間のデータを取り込んでから、広告主のタイムゾーンで毎日 09:00-10:00 ずつデータへの変更を取り込みます。 クリックごとに新しいコンバージョンが追跡されるので、履歴データは日ごとに変更される可能性があります。

[[!DNL Microsoft Advertising] でトラッキングされた各コンバージョンの 2 つの指標（[!DNL Microsoft Advertising] で設定）は &#x200B;](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) [!DNL Microsoft Advertising] で設定されたコンバージョン名を使用して、検索、ソーシャル、Commerceで自動的に使用できます。 各コンバージョンの指標は次のとおりです。

* `<conversion-name>` - キーワードのコンバージョン値（購入など）。

  >[!TIP]
  >
  >このタイプのコンバージョン指標は、最大コンバージョン値とターゲット ROAS 入札戦略を持つ [!DNL Microsoft Advertising] キャンペーンを含むポートフォリオの目的で使用します。

* `CT_<conversion-name>` — 「CT_」プレフィックス（CT_Purchase など）で始まるコンバージョンの数（カウント）。

  >[!TIP]
  >
  >このタイプのコンバージョン指標は、最大コンバージョン数とターゲット CPA 入札戦略を備えた [!DNL Microsoft Advertising] キャンペーンを含むポートフォリオの目的で使用します。

クリック時間と、アカウントで機能が有効になった日付からのコンバージョン/トランザクション時間に基づいて、データを利用できます。

[!DNL Microsoft Advertising] は、各コンバージョンを [&#x200B; 入札単位 &#x200B;](/help/search-social-commerce/glossary.md#a-b)、デバイス、およびクリック日（コンバージョン日ではなく）で記録します。 アトリビューションは、[!DNL Microsoft Advertising] の各指標のデフォルトのアトリビューション設定に基づいています。クリックイベントレベルのデータは利用できないので、Adobe Advertising アトリビューションは考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingに重複したコンバージョン名が表示されることがあります。 この場合は、[!UICONTROL Admin] > [!UICONTROL Conversions] のいずれかの重複する指標に対して [&#x200B; 表示名を変更 &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) します。 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、広告ネットワーク内のデータと同じレベルで一致します。 ただし、上位レベルの広告ネットワーク独自のコンバージョンデータには、子入札単位に起因しない追加のコンバージョンが含まれる場合があります。 検索、ソーシャルおよびCommerceのデータは、常に入札単位レベルからロールアップされるので、例えば、キャンペーンレベルのレポートと広告ネットワークのキャンペーンレベルのレポートの合計が異なる場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない日の遅い時間よりも朝の同期後の時間が短くなります。 午前中にデータを検証することをお勧めします。
>* データはオーディエンス レベルや地理的な場所レベルでは使用できないので、RLSA と場所の入札調整を自動最適化するためには使用されません。

## [!DNL Microsoft Advertising] のコンバージョンデータを検索、ソーシャル、Commerceのデータと比較する方法

次のレポート設定を使用して、同等のデータを検証します。

### [!DNL Microsoft Advertising] で使用するレポート設定

選択したコンバージョンアクションのレポートを日別に生成し、すべての広告ステータスのデータを含めます。

### 検索、ソーシャル、Commerceで使用するレポート設定

検索、ソーシャル、Commerceでは、「表示」または「レポート」オプションを使用して、（取引日ではなく）クリック日に基づくコンバージョンを表示できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Insights & Reports]/[!UICONTROL Reports]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Create Report]**] をクリックし、カーソルを **[!UICONTROL Basic Reports]** の上に置き、[**[!UICONTROL Search Engine Account Report]**] をクリックします。

1. [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. 「次の **[!UICONTROL Conversions Based]**」セクションで、「**[!UICONTROL Click date]**」を選択します。

   1. [!DNL Microsoft Advertising] レポートと同じ日付範囲を指定します。

   1. 「**[!UICONTROL Search/Content]**」セクションで、「**[!UICONTROL Search Only]**」を選択します。

   1. 「**[!UICONTROL Search Engine Hierarchy]**」セクションで、「[!UICONTROL Microsoft Advertising]」セクションを展開し、アカウントを選択します。

   1. 「[!UICONTROL Columns]」タブを開き、比較する [!DNL Microsoft Advertising] 指標を追加します。

1. 「**[!UICONTROL Create]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; 広告ネットワークアカウントとキャンペーンの実装の概要 &#x200B;](campaign-implemention-overview.md)
>* [&#x200B; 広告ネットワークキャンペーンのパフォーマンスの監視と管理 &#x200B;](monitor-performance-campaigns.md)
>* [&#x200B; 広告主について追跡されたコンバージョン指標の表示 &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
