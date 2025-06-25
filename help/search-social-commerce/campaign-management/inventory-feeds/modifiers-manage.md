---
title: 修飾子の管理
description: 在庫データフィードの広告テンプレートの修飾子を設定および管理する方法について説明します。
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 修飾子の管理

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

修飾子は、基本的な文の構造を変更せずに、文に追加したり文から削除したりできる形容詞または副詞です。 修飾子のグループを作成して、フィードデータテンプレートの様々なデータフィールドの変数として使用できます。 アカウント構造（キャンペーンおよび広告グループ）フィールド、キーワード、ベース URL、広告に修飾子を含めることで、関連する修飾子値ごとに 1 つの値を作成できます。 例えば、広告のヘッドラインに修飾子グループ変数を使用し、修飾子グループに 3 つの修飾子（「安い」、「割引」、「手頃な価格」）が含まれる場合、データフィードのデータ行ごとに 3 つの個別の広告が作成され、修飾子ごとに 1 つ作成されます。 同様に、広告グループのベース URL に複数の値を持つ修飾子グループを含める場合、結果として得られる各ベース URL に対して 1 つのキーワードセットが作成されます。

各モディファイヤ グループには、必要な数のモディファイヤを含めることができます。 各テンプレートで使用できるモディファイヤ グループは 1 つだけです。

## モディファイヤ グループを作成する

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Modifiers]**] をクリックします。

1. モディファイヤ グループのリストの上にある [**[!UICONTROL Create]**] をクリックします。

1. モディファイヤ グループの設定を指定します。

   **[!UICONTROL Name]:** モディファイヤ グループの名前。

   **[!UICONTROL Modifiers]:** グループのモディファイア値（ラインごとに 1 つ）。

1. 「**[!UICONTROL Save]**」をクリックします。

## モディファイヤ グループを編集する

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Modifiers]**] をクリックします。

1. モディファイヤ グループのリストで、モディファイヤ グループ名をクリックします。

1. モディファイヤ グループの設定を編集します。

   **[!UICONTROL Name]:** モディファイヤ グループの名前。

   **[!UICONTROL Modifiers]:** グループのモディファイア値（ラインごとに 1 つ）。

1. 「**[!UICONTROL Save]**」をクリックします。

## モディファイヤ グループを削除

>[!IMPORTANT]
>
>モディファイア・グループを削除する場合は、そのモディファイア・グループのすべての変数（`<modifier_group_name>`）を既存テンプレートのフィールドから削除します。 存在しない修飾子の変数を使用してテンプレートを介してデータを伝播しようとすると、ジョブ fail1 が発生します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Advanced (ACM)]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Modifiers]**] をクリックします。

1. 削除する各モディファイア・グループの横にあるチェック・ボックスを選択します。

1. モディファイヤ グループのリストの上にある [**[!UICONTROL Delete]**] をクリックします。

1. 確認メッセージで、「**[!UICONTROL Yes]**」をクリックします。

1. （必要に応じて） [ 適用可能なすべてのテンプレートから ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) 修飾子への参照を削除します。

>[!MORELIKETHIS]
>
>* [ 在庫フィードについて ](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [ 広告テンプレートの管理 ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
