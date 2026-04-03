---
title: キャンペーンと広告グループのオーディエンスターゲットの管理
description: ' [!DNL Google Ads] および [!DNL Microsoft Advertising]  キャンペーンと広告グループのオーディエンスターゲットを設定および管理する方法について説明します。'
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/U0RHQhkBYus7SwgN-gXKht4-MSV5VMy8nVTiKgGz1wY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 771
ht-degree: 0%

---

# [!DNL Google Ads]および[!DNL Microsoft Advertising]のキャンペーンと広告グループのオーディエンスターゲットを管理します

*[!DNL Google Ads]と[!DNL Microsoft Advertising]のみ*

[!DNL Google Ads]個のキャンペーンと広告グループ、および[!DNL Microsoft Advertising]個の広告グループは、同じ広告ネットワークから特定のオーディエンスをターゲットにできます。 広告ネットワークは、ターゲティングできるオーディエンスの規模を決定します。

>[!NOTE]
>
>除外は常にインクルージョン/ターゲットを上書きします。

オーディエンスターゲットを設定したり、オーディエンスターゲットの入札修飾子を編集したり、オーディエンスターゲットのステータスを変更したりできます。

## オーディエンスターゲティングの設定

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワークとアカウント名を選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. 特定のキャンペーンと広告グループのオーディエンスターゲットを設定します。

   1. 指定した広告ネットワークに該当するオーディエンスを選択します。

      オプションで、3文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスの場合は、**[!UICONTROL Include]**&#x200B;をクリックして選択します。

      [!DNL Google Ads]人の顧客マッチオーディエンスは、検索およびショッピングキャンペーンでのみ使用できます。

   1. ターゲットを指定します。

      1. （オプション）キャンペーンの子の広告グループを展開するには、キャンペーン名をクリックします。

      1. （オプション）キャンペーンリストまたは広告グループリストを、名前に含まれるテキスト文字列でフィルタリングするには、![ フィルター](/help/search-social-commerce/assets/filter.png " フィルター")をクリックし、テキスト文字列を入力フィールドに入力または貼り付け、**[!UICONTROL Enter]** キーを押します。

      1. 青いチェックマーク（![選択](/help/search-social-commerce/assets/include.png "選択")）が表示されるように、隣接する空の円をクリックして、指定された広告ネットワークの各キャンペーンと広告グループのターゲットを指定します。

      親キャンペーンと子広告グループ（自動的にターゲットを使用）の両方にターゲットを設定することはできません。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

1. （オプション） [!UICONTROL Targets] ビューから、次のいずれかの方法でターゲットの入札調整を設定します。

   * **[!UICONTROL Bid Adjustment]**&#x200B;列をクリックし、値を入力します。

   * ターゲット行の横にあるチェックボックスをオンにします。 ツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックし、入札修飾子を入力して、**[!UICONTROL Post]**&#x200B;をクリックします。

   値には、次の項目を含めることができます。

   * *0%:*&#x200B;このオーディエンスの広告の入札額を調整しない場合。

   * /[*その他の値（–90%から900%*/]）：このオーディエンスの広告の入札額を増減するには、次の操作を行います。 例えば、キーワードレベルの入札が1米ドルで、特定のオーディエンスのターゲットの入札調整が50%の場合、そのオーディエンスの入札は1.50米ドルに増加します。

## オーディエンスターゲットの入札修飾子の編集

市場内のオーディエンスを除く、すべてのオーディエンスタイプの入札修飾子とオーディエンスターゲットのステータスを変更できます。

>[!NOTE]
>
>Search, Social, &amp; Commerceでは、親キャンペーンがCPC入札戦略を使用し、オーディエンスターゲットの入札調整値を自動最適化するように設定されたポートフォリオ内にある場合、入札修飾子が自動的に最適化されます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 1つのターゲットの入札修飾子を編集するには、**[!UICONTROL Bid Adjustment]**&#x200B;列をクリックし、入札調整を編集します。

   * 1つ以上のターゲットの入札修飾子を編集するには、次の操作を行います。

      1. 編集する各ターゲットの横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

      1. **[!UICONTROL Bid Modifier]**&#x200B;および/または&#x200B;**[!UICONTROL Status]** フィールドを編集します。

         [!UICONTROL Bid Modifier] フィールドには、既存の値を指定した値に変更するか、指定した割合または金額で金額を増減するか、制限を設けるかを選択できます。

         設定された値の場合、値には次を含めることができます。

         * *0%:*&#x200B;このオーディエンスの広告の入札額を調整しない場合。

         * /[*その他の値（–90%から900%*/]）：このオーディエンスの広告の入札額を増減するには、次の操作を行います。 例えば、キーワードレベルの入札が1米ドルで、特定のオーディエンスのターゲットの入札調整が50%の場合、そのオーディエンスの入札は1.50米ドルに増加します。

         複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。

      1. （オプション）「**[!UICONTROL Additional Details]**」をクリックし、必要に応じてプロジェクト名と説明を入力します。

      1. **[!UICONTROL Post]**&#x200B;をクリックします。

## オーディエンスターゲティングのステータスの変更

アクティブなオーディエンスターゲットを一時停止して、入札を無効にできます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブまたは一時停止した検索オーディエンスターゲットを削除することもできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**&#x200B;をクリックします。

1. （オプション）特定のオーディエンスターゲットを含めるようにリストをフィルタリングします。

1. ステータスを変更する各オーディエンスターゲットの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. ツールバーで、ステータスボタンをクリックします。

   * 行をアクティブ化するには、![ アクティブ化](/help/search-social-commerce/assets/activate.png " アクティブ化")をクリックします。

   * 行を一時停止するには、![一時停止](/help/search-social-commerce/assets/pause.png "一時停止")をクリックします。

   * 行を削除するには、![その他のアクション ](/help/search-social-commerce/assets/more.png "その他のアクション ")をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて](audience-about.md)
>* [ キャンペーンと広告グループのオーディエンス除外の管理](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
