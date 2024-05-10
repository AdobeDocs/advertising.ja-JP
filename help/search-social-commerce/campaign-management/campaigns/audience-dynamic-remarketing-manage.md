---
title: 管理 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス
description: を作成および管理する方法を学ぶ [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス。
exl-id: 52faab75-e723-4e59-aac6-b4d0c4c1cf60
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '508'
ht-degree: 0%

---

# 管理 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス

*[!DNL Microsoft Advertising]アカウントのみ*

以下を作成できます [!DNL Microsoft Advertising] web ページで検索エンジンの JavaScript コンバージョンタグとオーディエンストラッキングタグを使用する場合の、動的リマーケティングオーディエンス。 各オーディエンスは、ユーザーがオーディエンスを構成する web ページに含まれる指定したタグを使用して作成されます。 同じトラッキングタグで複数のオーディエンスを作成できます。 また、既存のオーディエンスの名前とデータソースを変更したり、既存のオーディエンスを削除したりすることもできます。

動的リマーケティングオーディエンスのオーディエンスタイプは「」です[!UICONTROL Dynamic Remarketing] \&lt;visitor type=&quot;&quot;>「」（「過去の購入者の動的リマーケティング」など）。

動的リマーケティングと必要な JavaScript タグの実装方法について詳しくは、以下を参照してください [[!DNL Microsoft Advertising] 動的リマーケティングに関するドキュメント](https://help.ads.microsoft.com/#apex/ads/en/56910).

## 動的なリマーケティングオーディエンスの作成

>[!NOTE]
>
>の場合 [!DNL Microsoft Advertising] アカウント。JavaScript タグには、 [製品 ID とページタイプパラメーター](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85).

1. の名前を指定します [!DNL Microsoft Advertising] オーディエンスの作成元の web ページに含まれるユニバーサルイベントトラッキング（UET）タグ。

   後の手順で、タグ名が必要になります。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. データ テーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. オーディエンス情報を指定します。

   1. が含まれる **[!UICONTROL Data Source]** メニュー、選択 **[!UICONTROL Dynamic Remarketing List]**.

   1. を入力 **[!UICONTROL Audience Name]**.

   1. 検索エンジンアカウントで使用可能なすべてのタグのリストから、の名前を選択します [!DNL Microsoft Advertising] ユーザーがオーディエンスを構成する web ページに含まれる UET タグ。

   1. オーディエンスの訪問者のタイプを選択します。これは、関連する web ページの訪問者アクションに基づきます。 *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*、または *[!UICONTROL Shopping Cart Abandoners]*.

   1. 次の数を指定 **[!UICONTROL Membership Days]**：ユーザーの cookie がオーディエンスに残る日数です。 値の範囲は 1 ～ 180 です。

      広告がユーザーに関連すると予想される時間の長さを使用します。

1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>あなたの [!DNL Microsoft Advertising] 動的リマーケティングリストは、300 人以上のユーザーを含めると、ターゲティングの対象になります。

## 動的リマーケティングオーディエンスの編集

の名前とデータソースを変更できます。 [!DNL Microsoft Advertising] 動的リマーケティングオーディエンス。 の値は編集できません [!UICONTROL Membership Days] の設定値。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. 編集するオーディエンスの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. オーディエンス情報を編集します。

   1. が含まれる **[!UICONTROL Data Source]** セクションで、をクリック ![編集](/help/search-social-commerce/assets/edit.png "編集").

   1. （任意）を変更します **[!UICONTROL Audience Name]**.

   1. （オプション）広告ネットワークアカウントで使用可能なすべてのタグのリストから、の名前を変更します [!DNL Microsoft Advertising] ユーザーがオーディエンスを構成する web ページに含まれる UET タグ。

   1. （任意）関連する web ページの訪問者アクションに基づいて、オーディエンスの訪問者タイプを変更します。 *[!UICONTROL General Visitors]*, *[!UICONTROL Product Searchers]*, *[!UICONTROL Product Viewers]*, *[!UICONTROL Past Buyers]*、または *[!UICONTROL Shopping Cart Abandoners]*.

   1. クリック **[!UICONTROL Post]**.

## 動的リマーケティングオーディエンスの削除

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. （任意）特定のオーディエンスを含めるようにリストをフィルタリングします。

1. 削除する各オーディエンスの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

1. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [作成 [!DNL Google Ads] のカスタマーマッチオーディエンス [!DNL Adobe] オーディエンス](google-audience-from-adobe-audience.md)
>* [を作成 [!DNL Google Ads] Adobe Campaign メールリストからのカスタマーマッチオーディエンス](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用したカスタマーマッチオーディエンスの管理](audience-from-customer-data-list.md)
