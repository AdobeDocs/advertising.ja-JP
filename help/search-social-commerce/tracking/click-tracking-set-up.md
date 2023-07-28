---
title: cookie ベースのクリック追跡の設定
description: クリックトラッキングタグを設定および検証する方法について説明します。
exl-id: 340aec08-a1a5-4aa5-b666-9c819c1709d0
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# cookie ベースのクリック追跡の設定

検索、ソーシャル、コマースでクリックを追跡するには、次の要素を設定および検証する必要があります。

1. (Adobeアカウントチーム ) ピクセルを使用する顧客として広告主を設定します。

1. [広告主の広告ネットワークアカウントとキャンペーンごとに、適切なトラッキングオプションを指定します](#set-up-click-tracking-options).

1. 必要に応じて、 [トラッキング URL を生成してアップロードする](#generate-upload-tracking-urls) （一部のキャンペーン要素）

1. [いくつかのクリック追跡 URL の形式を検証し、それらをテストして、正しいランディングページが開くことを検証します。](#validate-tracking-urls).

## 広告ネットワークアカウントとキャンペーンのトラッキングオプションを設定します {#set-up-click-tracking-options}

*代理店のアカウントマネージャー [!DNL Adobe] アカウントマネージャー、管理者ユーザーロールのみ*

1. 各広告ネットワークアカウントに対して、次の操作を行います。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Accounts]**.

   1. アカウント名の上にカーソルを置き、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Edit]**.

   1. クリック **[!UICONTROL Set Account Tracking]**.

   1. の [!UICONTROL Tracking Type] 設定、選択 **[!UICONTROL EF Redirect]**.

   1. ( 検索、Social、およびコマースで、Adobe Analyticsとの間でデータのやり取りを許可したり、 [!DNL Apple Safari]) を選択します。 [!UICONTROL Redirect Type] オプション **[!UICONTROL Token]**.

   1. （オプション） **[!UICONTROL Auto Upload]** 」オプションを使用します。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

1. キャンペーンごとに、以下の手順を実行します。

   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Campaigns]**.

   1. キャンペーン名の上にカーソルを置いて、 ![メニューアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png "メニューアイコン")を選択し、 **[!UICONTROL Edit]**.

   1. クリック **[!UICONTROL Set Campaign Tracking]**. 次に、次のオプションを選択します。 **[!UICONTROL Override Account Tracking]**.

   1. の [!UICONTROL Tracking Type] 設定、選択 **[!UICONTROL EF Redirect]**.

   1. ( 検索、Social、およびコマースで、Adobe Analyticsとの間でデータのやり取りを許可したり、 [!DNL Apple Safari]) を選択します。 [!UICONTROL Redirect Type] オプション **[!UICONTROL Token]**.

   1. （オプション） **[!UICONTROL Auto Upload]** 」オプションを使用します。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

## トラッキング URL の生成とアップロード {#generate-upload-tracking-urls}

参照：[クリック追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md).&quot;

### クリック追跡 URL の形式のテスト {#validate-tracking-urls}

クリック追跡 URL に対して正しいランディングページが開いていることを検証します。

1. 広告主のステージング環境にトラフィックを送信して、広告クリックを模倣できます。

   1. テキストエディターにクリック追跡 URL を貼り付け、ランディングページの URL を広告主のステージング環境内の同じページを指すように変更して、新しい URL をブラウザーのアドレスバーに貼り付けて、 **[!DNL Enter]** キー。

   1. ブラウザーに保存されている cookie で cookie を探します。

   1. ステージングサイトでトランザクションを完了し、成功ページで正しいピクセルが実行されることを確認します。 ピクセルで追跡される実際のパラメーターは、広告主とトラッキング URL によって異なります。 次の例では、広告主は、新しいアプリの数と新しい売上高を追跡します。

      新しいエンドユーザー（新しい Cookie を持つ）の場合、次のピクセルを実行する必要があります。

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      cookie が新しくない場合は、次のピクセルを実行する必要があります。

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. ドメイン内の複数のクリック追跡 URL に対して繰り返します。

1. ドメインごとに異なるランディングページを使用して、手順 1 を繰り返します。

1. 必要に応じて、Search、Social、および Commerce がトランザクション ID(`ev_transid`) がテスト中に生成されました。

>[!MORELIKETHIS]
>
>* [クリック追跡 URL を生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
