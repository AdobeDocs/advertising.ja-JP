---
title: 管理 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス
description: 作成および管理方法を学ぶ [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス。
exl-id: 6f0cb6a0-36cc-4a07-82a8-247191b6c4f5
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '517'
ht-degree: 0%

---

# 管理 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス

*[!DNL Microsoft Advertising]アカウントのみ*

次の項目を作成できます。 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンスを使用する必要があります。 各オーディエンスは、ユーザーがオーディエンスを構成する Web ページに含まれる指定したタグを使用して作成されます。 同じトラッキングタグを使用して、複数のオーディエンスを作成できます。 また、既存のオーディエンスの名前やデータソースを変更したり、既存のオーディエンスを削除したりすることもできます。

動的リマーケティングオーディエンスのオーディエンスタイプは「[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>&quot; （「Dynamic Remarketing Past Buyers」など）

動的リマーケティングの概要と必要な JavaScript タグの実装方法について詳しくは、 [[!DNL Microsoft Advertising] 動的リマーケティングに関するドキュメント](https://help.ads.microsoft.com/#apex/ads/en/56910).

## 動的リマーケティングオーディエンスの作成

>[!NOTE]
>
>の場合 [!DNL Microsoft Advertising] アカウントの場合、JavaScript タグには [製品 ID およびページタイプパラメーター](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. 次の名前を指定： [!DNL Microsoft Advertising] オーディエンスの作成元となる Web ページに含まれるユニバーサルイベントトラッキング (UET) タグ。

   後の手順でタグ名が必要になります。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. オーディエンス情報を指定します。

   1. Adobe Analytics の **[!UICONTROL Data Source]** メニュー、選択 **[!UICONTROL Dynamic Remarketing List]**.

   1. 次を入力します。 **[!UICONTROL Audience Name]**.

   1. 検索エンジンアカウントで使用可能なすべてのタグのリストから、 [!DNL Microsoft Advertising] ユーザーがオーディエンスを構成する Web ページに含まれる UET タグ。

   1. オーディエンスの訪問者タイプを選択します。このタイプは、関連する Web ページでの訪問者のアクションに基づいています。 *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*&#x200B;または *[!UICONTROL Shopping Cart Abandoners]*.

   1. 次の数を指定： **[!UICONTROL Membership Days]**：ユーザーの Cookie がオーディエンスに残る日数です。 値の範囲は 1 ～ 180 です。

      広告がユーザーに関連すると予想される時間の長さを使用します。

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>お使いの [!DNL Microsoft Advertising] 動的リマーケティングリストは、少なくとも 300 人のユーザーが含まれればターゲティングの対象となります。

## 動的リマーケティングオーディエンスの編集

名前とデータソースは、 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス。 この [!UICONTROL Membership Days] 設定。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 編集するオーディエンスの横にあるチェックボックスを選択します。

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. オーディエンス情報を編集します。

   1. Adobe Analytics の **[!UICONTROL Data Source]** セクションで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

   1. （オプション） **[!UICONTROL Audience Name]**.

   1. （オプション）広告ネットワークアカウントで使用可能なすべてのタグのリストから、 [!DNL Microsoft Advertising] ユーザーがオーディエンスを構成する Web ページに含まれる UET タグ。

   1. （オプション）関連する Web ページでの訪問者のアクションに基づいて、オーディエンスの訪問者タイプを変更します。 *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*&#x200B;または *[!UICONTROL Shopping Cart Abandoners]*.

   1. クリック **[!UICONTROL Post]**.

## 動的リマーケティングオーディエンスの削除

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. （オプション）リストをフィルタリングして、特定のオーディエンスを含めます。

1. 削除する各オーディエンスの横にあるチェックボックスを選択します。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
