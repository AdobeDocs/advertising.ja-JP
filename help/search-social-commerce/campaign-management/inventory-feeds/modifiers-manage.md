---
title: 修飾子の管理
description: 在庫データフィード用の広告テンプレートの修飾子を設定および管理する方法について説明します。
exl-id: ade1472d-10e3-454e-8095-c579b48cfc01
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 0%

---

# 修飾子の管理

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

修飾子とは、基本的な文の構造を変えることなく、文に追加したり、文から削除したりできる形容詞または副詞です。 修飾子のグループを作成して、フィードデータテンプレートの様々なデータフィールドで変数として使用できます。 アカウント構造（キャンペーンおよび広告グループ）のフィールド、キーワード、ベース URL、広告に修飾子を含めることで、関連付けられた修飾子の値ごとに 1 つの値を作成できます。 例えば、広告のヘッドラインで修飾子グループ変数を使用し、修飾子グループに 3 つの修飾子（「安価」、「割引」、「手頃な価格」）が含まれる場合、データフィードの各データ行に対して 3 つの異なる広告が作成されます。 同様に、広告グループのベース URL に複数の値を持つ修飾子グループを含めると、結果として得られるベース URL ごとに 1 つのキーワードセットが作成されます。

各モディファイヤグループには、必要な数のモディファイヤを含めることができます。 各テンプレートで使用できるモディファイヤグループは 1 つだけです。

## モディファイアグループを作成する

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Modifiers]**.

1. 修飾子グループのリストの上にある **[!UICONTROL Create]**.

1. モディファイアグループの設定を指定します。

   **[!UICONTROL Name]:** モディファイアグループの名前。

   **[!UICONTROL Modifiers]:** グループの修飾子の値（1 行に 1 つ）。

1. クリック **[!UICONTROL Save]**.

## モディファイアグループを編集する

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Modifiers]**.

1. モディファイア・グループのリストで、モディファイア・グループ名をクリックします。

1. モディファイヤグループの設定を編集します。

   **[!UICONTROL Name]:** モディファイアグループの名前。

   **[!UICONTROL Modifiers]:** グループの修飾子の値（1 行に 1 つ）。

1. クリック **[!UICONTROL Save]**.

## モディファイアグループの削除

>[!IMPORTANT]
>
>モディファイヤグループを削除すると、そのモディファイヤグループのすべての変数 ( `<modifier_group_name>`) を既存のテンプレートのフィールドから削除します。 存在しない修飾子の変数を使用してテンプレートにデータを伝播しようとすると、ジョブは fail1 になります。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**.

1. データテーブルの上にあるツールバーで、 **[!UICONTROL Modifiers]**.

1. 削除する各モディファイヤグループの横にあるチェックボックスをオンにします。

1. 修飾子グループのリストの上にある **[!UICONTROL Delete]**.

1. 確認メッセージで、 **[!UICONTROL Yes]**.

1. （必要に応じて） [修飾子への参照を削除](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md) 該当するすべてのテンプレートから。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [広告テンプレートの管理](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
