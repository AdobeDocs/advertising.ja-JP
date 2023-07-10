---
title: '[!DNL Microsoft Advertising] コンバージョンデータ'
description: 次のタイプについて説明します。 [!DNL Microsoft Advertising] — 検索、ソーシャル、コマースで使用できるコンバージョンデータ。
source-git-commit: f48706edc1ab25f7c2396159d420bc2cfa849bbb
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] 検索、ソーシャル、コマースのコンバージョンデータ

検索、ソーシャル、コマースは、 [Microsoft Advertising ユニバーサルイベントトラッキング (UET) タグ](https://about.ads.microsoft.com/solutions/tools/universal-event-tracking) 。ビュースルーコンバージョンを含む web サイトコンバージョンの場合は、レポートおよび最適化を行います。

すべての指標は、キャンペーン管理ビューと基本レポートで自動的に使用でき、Microsoft Advertising キャンペーンの最適化のために、ポートフォリオ目標でも使用できます。

## 使用可能なコンバージョンデータ

検索、ソーシャル、コマースの各データを同期し、「[!DNL Include in 'Conversions']「 」オプションが有効になり、過去 35 日間のデータをプルした後、09 までに毎日データに変更をプルする:00-10:広告主のタイムゾーンの 00。 履歴データは、クリックごとに新しいコンバージョンが追跡されるので、日々変化する場合があります。

各 [[!DNL Microsoft Advertising]追跡されたコンバージョン](https://help.ads.microsoft.com/apex/index/3/en-us/n5012) ( [!DNL Microsoft Advertising]) は、検索、ソーシャル、コマースで、 [!DNL Microsoft Advertising]. 各コンバージョンのトランザクションプロパティには、次のものがあります。

* `<conversion-name>`  — キーワードのコンバージョン値（Purchase など）。

  >[!TIP]
  >
  >このタイプのプロパティを、 [!DNL Microsoft Advertising] キャンペーンを作成します。

* `CT_<conversion-name>` — 「CT_」プレフィックスで始まるコンバージョンの数（カウント）（CT_Purchase など）。

  >[!TIP]
  >
  >このタイプのプロパティを、 [!DNL Microsoft Advertising] キャンペーンを作成し、Max Conversions と Target CPA の入札戦略に従ってください。

データは、クリック時間に基づき、アカウントで機能が有効になった日からのコンバージョン/トランザクション時間に基づいて使用できます。

<!-- verify below/ if equivalent

[!DNL Microsoft Advertising] records each conversion by [bid unit](/help/search-social-commerce/glossary.md#a-b), device, and click date (not conversion date). Attribution is based on the default attribution setting for each metric in [!DNL Microsoft Advertising]; Adobe Advertising attribution isn't factored in because click event-level data isn't available.
-->

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe広告に重複したコンバージョン名が表示されることがあります。 この場合、 [表示名を変更する](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) の指標が重複している場合は、 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、同じレベルの広告ネットワーク内のデータと一致します。 ただし、高いレベルの広告ネットワーク独自のコンバージョンデータには、子の入札単位に関連付けられない追加のコンバージョンが含まれる場合があります。 検索、ソーシャル、コマースのデータは、常に入札単位レベルからロールアップされるので、例えば、キャンペーンレベルのレポートは、広告ネットワークのキャンペーンレベルのレポートと同じ合計にならない場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない場合の、午前の同期後の方が、当日の後半よりも少なくなります。 データの検証は、午前中におこなうことをお勧めします。
>* データは、オーディエンスまたは地理的な場所レベルでは使用できないので、RLSA や場所の入札調整を自動最適化するためには使用されません。

## でのコンバージョンデータの比較方法 [!DNL Microsoft Advertising] 検索、ソーシャル、コマースのデータを含む

次のレポート設定を使用して、同等のデータを検証します。

### で使用するレポート設定 [!DNL Microsoft Advertising]

選択したコンバージョンアクションのレポートを日別に生成し、すべての広告ステータスのデータを含めます。

### 検索、ソーシャル、コマースで使用するレポート設定

Social および Commerce の検索で、「表示」または「レポート」オプションを使用して、（トランザクション日ではなく）クリック日に基づいてコンバージョンを表示します。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Create Report]**&#x200B;をクリックし、 **[!UICONTROL Basic Reports]**&#x200B;をクリックし、 **[!UICONTROL Search Engine Account Report]**.

1. 内 [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. 内 **[!UICONTROL Conversions Based]** 「 」セクションで、「 」を選択します。 **[!UICONTROL Click date]**.

   1. 次の期間に使用したのと同じ日付範囲を指定します： [!DNL Microsoft Advertising] レポート。

   1. 内 **[!UICONTROL Search/Content]** セクション、選択 **[!UICONTROL Search Only]**.

   1. 内 **[!UICONTROL Search Engine Hierarchy]** セクションで、 [!UICONTROL Microsoft Advertising] 」セクションでアカウントを選択します。

   1. を開きます。 [!UICONTROL Columns] タブをクリックし、 [!DNL Microsoft Advertising] 指標を比較します。

1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスの監視と管理](monitor-performance-campaigns.md)
>* [広告主でトラッキングされているトランザクションプロパティの表示](/help/search-social-commerce/admin/transaction-properties/transaction-property-view-tracked.md)
