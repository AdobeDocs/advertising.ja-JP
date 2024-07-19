---
title: 動的リマ  [!DNL Microsoft Advertising]  ケティングオーディエンスの管理
description: 動的リマーケティングオーディエンスを作成および管理  [!DNL Microsoft Advertising]  る方法について説明します。
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 動的リマ [!DNL Microsoft Advertising] ケティングオーディエンスの管理

*[!DNL Microsoft Advertising]アカウントのみ*

Web ページで検索エンジンのJavaScript コンバージョンタグとオーディエンストラッキングタグを使用する場合は、[!DNL Microsoft Advertising] の動的リマーケティングオーディエンスを作成できます。 各オーディエンスは、ユーザーがオーディエンスを構成する web ページに含まれる指定したタグを使用して作成されます。 同じトラッキングタグで複数のオーディエンスを作成できます。 また、既存のオーディエンスの名前とデータソースを変更したり、既存のオーディエンスを削除したりすることもできます。

動的リマーケティングオーディエンスのオーディエンスタイプは「[!UICONTROL Dynamic Remarketing] \&lt; 訪問者タイプ\>」です（「動的リマーケティングの過去の購入者」など）。

動的リマーケティングと必要なJavaScript タグの実装方法について詳しくは、[[!DNL Microsoft Advertising]  動的リマーケティングのドキュメント ](https://help.ads.microsoft.com/#apex/ads/en/56910) を参照してください。

## 動的なリマーケティングオーディエンスの作成

>[!NOTE]
>
>[!DNL Microsoft Advertising] アカウントの場合、JavaScript タグには [ 商品 ID およびページタイプパラメーター ](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) を含める必要があります。

1. オーディエンスの作成元の Web ページに含まれる [!DNL Microsoft Advertising] Universal Event Tracking （UET）タグの名前を識別します。

   後の手順で、タグ名が必要になります。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワークとアカウント名を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. オーディエンス情報を指定します。

   1. **[!UICONTROL Data Source]** メニューで、「**[!UICONTROL Dynamic Remarketing List]**」を選択します。

   1. **[!UICONTROL Audience Name]** を入力します。

   1. 検索エンジンアカウントで使用可能なすべてのタグのリストから、ユーザーがオーディエンスを構成する web ページに含まれる [!DNL Microsoft Advertising] UET タグの名前を選択します。

   1. オーディエンスの訪問者のタイプを選択します。これは、関連する web ページの訪問者アクション（*[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]* または *[!UICONTROL Shopping Cart Abandoners]*）に基づいています。

   1. **[!UICONTROL Membership Days]** 数を指定します。これは、ユーザーの Cookie がオーディエンスに残る日数です。 値の範囲は 1 ～ 180 です。

      広告がユーザーに関連すると予想される時間の長さを使用します。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!NOTE]
>
>[!DNL Microsoft Advertising] の動的リマーケティングリストには、300 人以上のユーザーが含まれると、ターゲティングを行うことができます。

## 動的リマーケティングオーディエンスの編集

[!DNL Microsoft Advertising] しい動的リマーケティングオーディエンスの名前とデータソースを変更できます。 [!UICONTROL Membership Days] 設定の値は編集できません。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. オーディエンス情報を編集します。

   1. 「**[!UICONTROL Data Source]**」セクションで、「![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ") をクリックします。

   1. （任意） **[!UICONTROL Audience Name]** を変更します。

   1. （オプション）広告ネットワークアカウントで使用可能なすべてのタグのリストから、ユーザーがオーディエンスを構成する web ページに含まれる [!DNL Microsoft Advertising] UET タグの名前を変更します。

   1. （任意）関連する web ページでの訪問者アクション（*[!UICONTROL General Visitors]*、*[!UICONTROL Product Searchers]*、*[!UICONTROL Product Viewers]*、*[!UICONTROL Past Buyers]*、*[!UICONTROL Shopping Cart Abandoners]*）に基づく、オーディエンスの訪問者タイプの変更。

   1. 「**[!UICONTROL Post]**」をクリックします。

## 動的リマーケティングオーディエンスの削除

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. （任意）特定のオーディエンスを含めるようにリストをフィルタリングします。

1. 削除する各オーディエンスの横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて ](audience-about.md)
>* [ オーディエ  [!DNL Google Ads]  スからの顧客一致オーディエ  [!DNL Adobe]  スの作成 ](google-audience-from-adobe-audience.md)
>* [Adobe Campaign [!DNL Google Ads]  メールリストからカスタマーマッチオーディエンスを作成 ](google-audience-from-campaign-email-list.md)
>* [ 顧客データリストを使用したカスタマーマッチオーディエンスの管理 ](audience-from-customer-data-list.md)
