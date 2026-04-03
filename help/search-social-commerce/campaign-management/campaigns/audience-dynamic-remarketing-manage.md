---
title: 動的リマーケティングオーディエンスを [!DNL Microsoft Advertising] 管理
description: '動的リマーケティングオーディエンスを作成および管理する方法について説明します。 [!DNL Microsoft Advertising] '
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/ev1y2UpkEHJhIgS3vQz8GRF0LNJwG9BHSxufQeeQAfA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 508
ht-degree: 0%

---

# [!DNL Microsoft Advertising]動的リマーケティングオーディエンスの管理

*[!DNL Microsoft Advertising]アカウントのみ*

web ページで検索エンジンのJavaScript コンバージョンおよびオーディエンストラッキングタグを使用すると、[!DNL Microsoft Advertising]動的リマーケティングオーディエンスを作成できます。 各オーディエンスは、オーディエンスを構成するユーザーが属するweb ページに含まれる、指定されたタグを使用して作成されます。 同じトラッキングタグを使用して、複数のオーディエンスを作成できます。 既存のオーディエンスの名前とデータソースを変更したり、既存のオーディエンスを削除したりすることもできます。

動的リマーケティングオーディエンスには、オーディエンスタイプ「[!UICONTROL Dynamic Remarketing] \&lt;訪問者タイプ\>」（「動的リマーケティングの過去の購入者」など）があります。

動的リマーケティングと必要なJavaScript タグの実装方法について詳しくは、[[!DNL Microsoft Advertising] 動的リマーケティングに関するドキュメント &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/56910)を参照してください。

## 動的リマーケティングオーディエンスの作成

>[!NOTE]
>
>[!DNL Microsoft Advertising] アカウントの場合、JavaScript タグには[製品IDとページタイプのパラメーター](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85)を含める必要があります。

1. オーディエンスの作成元となるweb ページに含まれる[!DNL Microsoft Advertising] ユニバーサル イベント トラッキング （UET） タグの名前を特定します。

   後の手順でタグ名が必要になります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワークとアカウント名を選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. オーディエンス情報を指定します。

   1. **[!UICONTROL Data Source]** メニューで、**[!UICONTROL Dynamic Remarketing List]**&#x200B;を選択します。

   1. **[!UICONTROL Audience Name]**&#x200B;を入力します。

   1. 検索エンジンアカウントで使用可能なすべてのタグのリストから、ユーザーがオーディエンスを構成するweb ページに含まれる[!DNL Microsoft Advertising] UET タグの名前を選択します。

   1. オーディエンスの訪問者タイプを選択します。このタイプは、関連するweb ページの訪問者アクション（*[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*、または&#x200B;*[!UICONTROL Shopping Cart Abandoners]*）に基づきます。

   1. ユーザーのCookieがオーディエンスに滞在する日数である&#x200B;**[!UICONTROL Membership Days]**&#x200B;の数を指定します。 値の範囲は1から180までです。

      広告がユーザーに適していると期待される期間を使用します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!NOTE]
>
>動的リマーケティングリスト [!DNL Microsoft Advertising]は、少なくとも300人のユーザーが含まれると、ターゲティングの対象となります。

## 動的リマーケティングオーディエンスの編集

[!DNL Microsoft Advertising]動的リマーケティングオーディエンスの名前とデータソースを変更できます。 [!UICONTROL Membership Days]設定の値は編集できません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. オーディエンス情報を編集します。

   1. **[!UICONTROL Data Source]** セクションで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

   1. （オプション） **[!UICONTROL Audience Name]**&#x200B;を変更します。

   1. （オプション）広告ネットワークアカウントで使用可能なすべてのタグのリストから、オーディエンスを構成するユーザーが含まれるweb ページに含まれる[!DNL Microsoft Advertising] UET タグの名前を変更します。

   1. （オプション）オーディエンスの訪問者タイプを変更します。オーディエンスは、関連するweb ページでの訪問者のアクションに基づいています（*[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*、または&#x200B;*[!UICONTROL Shopping Cart Abandoners]*）。

   1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 動的リマーケティングオーディエンスの削除

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. （オプション）特定のオーディエンスを含めるようにリストをフィルタリングします。

1. 削除する各オーディエンスの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスについて](audience-about.md)
>* [顧客マッチオーディエンスを [!DNL Google Ads]  オーディエンス  [!DNL Adobe] から](google-audience-from-adobe-audience.md)作成
>* [Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
