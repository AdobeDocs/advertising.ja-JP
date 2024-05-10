---
title: '''[!DNL Microsoft Advertising] コンバージョンデータ'
description: タイプについて説明します [!DNL Microsoft Advertising] – 検索、ソーシャル、Commerceで利用できる、トラッキングされたコンバージョンデータ。
feature: Search Campaign Management, Conversions
exl-id: 0ebc70a0-1fb7-48db-b45d-7409e8bb6f64
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '629'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 検索、ソーシャル、Commerceのコンバージョンデータ

検索、ソーシャル、Commerceでは、で追跡されたすべてのコンバージョンが自動的に同期されます [[!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET）タグ](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) レポートおよび最適化を目的とした web サイトコンバージョン（ビュースルーコンバージョンを含む）

すべての指標は、キャンペーン管理ビューや基本レポートで自動的に使用でき、 [!DNL Microsoft Advertising] キャンペーン。

## 使用可能なコンバージョンデータ

「」に該当するコンバージョンのデータを検索、ソーシャル、Commerce同期[!DNL Include in 'Conversions']「」オプションが有効になっている場合は、過去 35 日間のデータを取り込んだ後、09 までに毎日データに対する変更を取り込みます:00-10:広告主のタイムゾーンでは 00。 クリックごとに新しいコンバージョンが追跡されるので、履歴データは日ごとに変更される可能性があります。

それぞれに 2 つの指標 [[!DNL Microsoft Advertising] – トラッキングされたコンバージョン](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) （で設定） [!DNL Microsoft Advertising]）は、で設定したコンバージョン名を使用して、検索、ソーシャル、Commerceで自動的に使用できます [!DNL Microsoft Advertising]. 各コンバージョンの指標は次のとおりです。

* `<conversion-name>` — キーワードのコンバージョン値（購入など）。

  >[!TIP]
  >
  >次のようなポートフォリオの目的に、このタイプのコンバージョン指標を使用します [!DNL Microsoft Advertising] 最大コンバージョン値とターゲット ROAS 入札戦略を持つキャンペーン。

* `CT_<conversion-name>`  – 「CT_」プレフィックスで始まるコンバージョンの数（カウント）（CT_Purchase など）。

  >[!TIP]
  >
  >次のようなポートフォリオの目的に、このタイプのコンバージョン指標を使用します [!DNL Microsoft Advertising] 最大コンバージョン数とターゲット CPA 入札戦略を使用するキャンペーン。

クリック時間と、アカウントで機能が有効になった日付からのコンバージョン/トランザクション時間に基づいて、データを利用できます。

[!DNL Microsoft Advertising] 各コンバージョンを次の基準で記録 [入札単位](/help/search-social-commerce/glossary.md#a-b)、デバイスおよびクリック日（コンバージョン日ではありません）。 アトリビューションは、の各指標のデフォルトのアトリビューション設定に基づいています [!DNL Microsoft Advertising]。クリックイベントレベルのデータを使用できないので、Adobe Advertisingアトリビューションは考慮されません。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe Advertisingにコンバージョン名が重複する場合があります。 この場合、 [表示名の変更](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-edit-display-name.md) の重複指標の 1 つに対して [!UICONTROL Admin] > [!UICONTROL Conversions]. 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、広告ネットワーク内のデータと同じレベルで一致します。 ただし、上位レベルの広告ネットワーク独自のコンバージョンデータには、子入札単位に起因しない追加のコンバージョンが含まれる場合があります。 検索、ソーシャルおよびCommerceのデータは、常に入札単位レベルからロールアップされるので、例えば、キャンペーンレベルのレポートと広告ネットワークのキャンペーンレベルのレポートの合計が異なる場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない日の遅い時間よりも朝の同期後の時間が短くなります。 午前中にデータを検証することをお勧めします。
>* データはオーディエンス レベルや地理的な場所レベルでは使用できないので、RLSA と場所の入札調整を自動最適化するためには使用されません。

## でのコンバージョンデータの比較方法 [!DNL Microsoft Advertising] 検索、ソーシャル、Commerceのデータを使用

次のレポート設定を使用して、同等のデータを検証します。

### で使用するレポート設定 [!DNL Microsoft Advertising]

選択したコンバージョンアクションのレポートを日別に生成し、すべての広告ステータスのデータを含めます。

### 検索、ソーシャル、Commerceで使用するレポート設定

検索、ソーシャル、Commerceでは、「表示」または「レポート」オプションを使用して、（取引日ではなく）クリック日に基づくコンバージョンを表示できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Create Report]**&#x200B;にカーソルを合わせます **[!UICONTROL Basic Reports]**&#x200B;を選択し、 **[!UICONTROL Search Engine Account Report]**.

1. が含まれる [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. が含まれる **[!UICONTROL Conversions Based]** セクションで、を選択します **[!UICONTROL Click date]**.

   1. に使用したのと同じ日付範囲を指定します [!DNL Microsoft Advertising] レポート。

   1. が含まれる **[!UICONTROL Search/Content]** セクションで選択 **[!UICONTROL Search Only]**.

   1. が含まれる **[!UICONTROL Search Engine Hierarchy]** セクションで、 [!UICONTROL Microsoft Advertising] セクションとアカウントを選択します。

   1. を開きます [!UICONTROL Columns] タブをクリックして、を追加します。 [!DNL Microsoft Advertising] 比較する指標。

1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスを監視および管理](monitor-performance-campaigns.md)
>* [広告主について追跡されたコンバージョン指標の表示](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-view-tracked.md)
