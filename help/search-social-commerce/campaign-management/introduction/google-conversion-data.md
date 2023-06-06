---
title: '"[!DNL Google Ads] コンバージョンデータ»'
description: 次のタイプについて説明します。 [!DNL Google Ads] — 検索、ソーシャル、コマースで使用できるコンバージョンデータ。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '738'
ht-degree: 0%

---

# [!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ

検索、ソーシャル、コマースは自動的に同期します [!DNL Google Ads]- [!DNL Google Ads] 検索およびショッピングネットワークを検索、ソーシャル、コマースに分割し、レポートと最適化を行います。 検索、ソーシャル、コマースの各データを同期し、「[!DNL Include in 'Conversions']「 」オプションが有効になり、過去 30 日間のデータをプルしてから、毎日データに変更をプルする。

## 使用可能なコンバージョンデータ

それぞれに最大 3 つのトランザクションプロパティ [[!DNL Google Ads]追跡されたコンバージョン](https://support.google.com/google-ads/answer/4677036) ( [!DNL Google Ads]) は、検索、ソーシャル、コマースで、 [!DNL Google Ads]. 各コンバージョンのトランザクションプロパティには、次のものがあります。

* `GGL*` — （追跡する場合）「GGL」プレフィックスで始まる、キーワードのコンバージョン値の合計（GGL Purchase など）。

* `GGL_CT*` — 「GGL_CT」プレフィックス（GGL_CT_Purchase など）で始まるコンバージョンの数（カウント）。

* `GGL_XD_CT*` — （コンバージョンタイプで使用可能な場合、追跡する場合）Googleが測定する、「GGL_XD_CT_」プレフィックス (GGL_XD_CT_Purchase など ) で始まる、クロスデバイスコンバージョンの数（カウント）。

データは、アカウントに対してこの機能が有効になった日から利用でき、09 年までに毎日更新されます。:00-10:広告主のタイムゾーンの 00。

[!DNL Google Ads] は、各コンバージョンを次のように記録します。 [入札単位](/help/search-social-commerce/glossary.md#a-b)、デバイス、クリック日（コンバージョン日ではなく） アトリビューションは、 [!DNL Google Ads];Adobe広告属性は、クリックイベントレベルのデータを使用できないので、考慮されていません。 Search、Social、&amp;Commerce は、毎日過去 30 日間のコンバージョンデータを取り込み、前日以降の増分コンバージョンを計算します。計算には、次のクリック日が使用されます。 [!DNL Google Ads] 取引日として前日を指定する。 その結果、クリックごとに新しいコンバージョンが追跡されるので、履歴データが日々変化する場合があります。 検索、ソーシャル、コマースのデータを [!DNL Google Ads]を選択し、「[!UICONTROL Conversions by: Click date]&quot; （トランザクションの日付ではありません）

すべての指標は、キャンペーン管理ビューと基本レポートで自動的に使用でき、ポートフォリオ目標で使用して最適化することもできます。

>[!NOTE]
>
>* 同じコンバージョン名を持つ複数のアカウントがある場合、Adobe広告に重複したコンバージョン名が表示されることがあります。 この場合、 [表示名を変更する](/help/search-social-commerce/admin/transaction-properties/transaction-property-edit-display-name.md) の指標が重複している場合は、 [!UICONTROL Admin] > [!UICONTROL Transaction Properties]. 2 つの異なる指標の名前が同じ場合、レポートは正確ではありません。
>* 入札単位レベルのデータは、 [!DNL Google Ads] 同じレベルで しかし、 [!DNL Google Ads]上位レベルの「独自のコンバージョンデータ」には、子入札単位に関連付けられない追加のコンバージョンが含まれる場合があります。 検索、ソーシャル、コマースのデータは、常に入札単位レベルからロールアップされるので、例えば、キャンペーンレベルのレポートは、Google Ads のキャンペーンレベルのレポートと同じ合計にならない場合があります。
>* 通常、データの相違は、追加のコンバージョンがまだ同期されていない場合の、午前の同期後の方が、当日の後半よりも少なくなります。 データの検証は、午前中におこなうことをお勧めします。
>* ではコンバージョンデータを使用できません [!DNL Google Display Network], [!DNL Gmail], [!DNL Mobile App]、および [!DNL YouTube] 広告。 でデータを比較する際に、これらのタイプの広告を除外する [!DNL Google Ads] 検索、ソーシャル、コマースのデータを含む
>* のデータ [!DNL Google Ads] コンバージョンは、オーディエンスまたは地理的な場所レベルでは利用できないので、RLSA や場所の入札調整を自動最適化するためには使用されません。


## でのコンバージョンデータの比較方法 [!DNL Google Ads] 検索、ソーシャル、コマースのデータを含む

次のレポート設定を使用して、同等のデータを検証します。

### で使用するレポート設定 [!DNL Google Ads]

1. メインツールバーで、「 **[!DNL Reports]>[!DNL Report]**.

1. 選択 **[!DNL + Custom]>[!DNL Table]**.

1. 左側のウィンドウで、レポートの行と列を指定します。

   1. を検索します。 **[!DNL Day]** フィールドにドラッグし、 [!DNL Row] 」セクションに入力します。

   1. を検索します。 **[!DNL All conv].** フィールドにドラッグし、 [!DNL Column] 」セクションに入力します。

   1. を検索します。 **[!DNL Conversion action]** フィールドにドラッグし、 [!DNL Column] 」セクションに入力します。

1. レポート設定ツールバーで、 **[!DNL Filter]>[!DNL Ad status]**&#x200B;をクリックし、すべてのボックスを選択します。

1. レポート設定ツールバーで、 **[!DNL Download]>[!DNL Excel .csv]**.

### 検索、ソーシャル、コマースで使用するレポート設定

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Reports]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Create Report]**&#x200B;をクリックし、 **[!UICONTROL Basic Reports]**&#x200B;をクリックし、 **[!UICONTROL Search Engine Account Report]**.

1. 内 [!UICONTROL Report Settings] ウィンドウで、次のレポート設定を指定します。

   1. 内 **[!UICONTROL Conversions Based]** 「 」セクションで、「 」を選択します。 **[!UICONTROL Click date]**.

   1. 次の期間に使用したのと同じ日付範囲を指定します： [!DNL Google Ads] レポート。

   1. 内 **[!UICONTROL Search/Content]** セクション、選択 **[!UICONTROL Search Only]**.

   1. 内 **[!UICONTROL Search Engine Hierarchy]** セクションで、 [!UICONTROL Google Adwords] 」セクションでアカウントを選択します。

   1. を開きます。 [!UICONTROL Columns] タブをクリックし、 [!DNL Google Ads] （「GGL」で始まる）指標を比較します。

1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [検索、ソーシャル、コマースでのキャンペーン管理について](campaign-management-about.md)
>* [広告ネットワークアカウントとキャンペーンの実装の概要](campaign-implemention-overview.md)
>* [広告ネットワークキャンペーンのパフォーマンスの監視と管理](monitor-performance-campaigns.md)

