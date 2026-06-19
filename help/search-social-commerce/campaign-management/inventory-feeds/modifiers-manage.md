---
title: 修飾子の管理
description: 在庫データフィードの広告テンプレートの修飾子を設定および管理する方法について説明します。
exl-id: 74c9a7c7-0979-4f78-9225-43bc6c94acd7
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/kx5mrj2liqcxDBJG0zFS53urCLg6udHp7oaFSqwwIfA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 375
ht-degree: 0%

---

# 修飾子の管理

*[!DNL Google Ads]、[!DNL LY Ads] （削除操作のみ）、[!DNL Microsoft Advertising]、および[!DNL Yandex] アカウントのみ*

修飾子とは、基本的な文構造を変更することなく、文に追加したり文から削除したりできる形容詞または副詞です。 フィード データ テンプレートの様々なデータ フィールドで変数として使用する修飾子のグループを作成できます。 アカウント構造（キャンペーンと広告グループ）フィールド、キーワード、ベース URL、広告に修飾子を含めることで、関連付けられた各修飾子値に1つの値を作成できます。 例えば、広告の見出しで修飾子グループ変数を使用し、修飾子グループに3つの修飾子（「安い」、「割引」、「手頃な価格」）が含まれている場合、データフィードのデータ行ごとに3つの個別の広告が作成されます。各修飾子に1つずつ作成されます。 同様に、広告グループのベース URLに複数の値を持つ修飾子グループを含める場合、生成されるベース URLごとに1つのキーワード セットが作成されます。

各修飾子グループには、必要な数の修飾子を含めることができます。 各テンプレートで使用できる修飾子グループは1つだけです。

## 修飾子グループの作成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Modifiers]**&#x200B;をクリックします。

1. 修飾子グループのリストの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

1. 修飾子グループの設定を指定します。

   **[!UICONTROL Name]:**&#x200B;修飾子グループの名前。

   **[!UICONTROL Modifiers]:** グループの修飾子の値（行ごとに1つ）。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## モディファイヤ グループの編集

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Modifiers]**&#x200B;をクリックします。

1. モディファイア・グループのリストで、モディファイア・グループ名をクリックします。

1. 修飾子グループの設定を編集します。

   **[!UICONTROL Name]:**&#x200B;修飾子グループの名前。

   **[!UICONTROL Modifiers]:** グループの修飾子の値（行ごとに1つ）。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## モディファイヤ グループの削除

>[!IMPORTANT]
>
>修飾子グループを削除する場合は、既存のテンプレートのフィールドからその修飾子グループのすべての変数（`<modifier_group_name>`と呼ばれます）を削除します。 存在しない修飾子の変数を使用してテンプレートにデータを反映しようとすると、ジョブが失敗します1。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;をクリックします。

1. データテーブルの上のツールバーで、**[!UICONTROL Modifiers]**&#x200B;をクリックします。

1. 削除する各修飾子グループの横にあるチェックボックスをオンにします。

1. 修飾子グループのリストの上で、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Yes]**&#x200B;をクリックします。

1. （必要に応じて） [該当するすべてのテンプレートから修飾子](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)への参照を削除します。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](/help/search-social-commerce/campaign-management/inventory-feeds/inventory-feeds-about.md)
>* [広告テンプレートの管理](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/ad-template-manage.md)
