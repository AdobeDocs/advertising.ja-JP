---
title: cookie ベースのクリックの追跡の設定
description: クリックトラッキングタグを設定および検証する方法について説明します。
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 0%

---

# cookie ベースのクリックの追跡の設定

検索、ソーシャル、Commerceでクリックをトラッキングするには、次の要素を設定し検証する必要があります。

1. （Adobe アカウントチーム）広告主をピクセル顧客として設定します。

1. [&#x200B; 広告主の広告ネットワークアカウントおよびキャンペーンごとに正しいトラッキングオプションを指定します &#x200B;](#set-up-click-tracking-options)。

1. 必要に応じて、一部のキャンペーン要素に対して [&#x200B; トラッキング URL を生成してアップロード &#x200B;](#generate-upload-tracking-urls) します。

1. [&#x200B; いくつかのクリックトラッキング URL の形式を検証し、テストして正しいランディングページが開いていることを検証します &#x200B;](#validate-tracking-urls)。

## 広告ネットワークアカウントおよびキャンペーンのトラッキングオプションの設定 {#set-up-click-tracking-options}

*エージェンシーアカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. 各広告ネットワークアカウントに対して、次の手順を実行します。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Accounts]** をクリックします。

   1. アカウント名の上にカーソルを置き、![&#x200B; メニューアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ") をクリックして、**[!UICONTROL Edit]** を選択します。

   1. 「**[!UICONTROL Set Account Tracking]**」をクリックします。

   1. [!UICONTROL Tracking Type] 設定で、「**[!UICONTROL EF Redirect]**」を選択します。

   1. （検索、ソーシャル、CommerceでAdobe Analyticsとデータを交換したり、[!DNL Apple Safari] で発生したコンバージョンを追跡したりできるようにするには、[!UICONTROL Redirect Type] オプションの **[!UICONTROL Token]** を選択します）。

   1. （オプション）「**[!UICONTROL Auto Upload]**」オプションをオンにすると、次回の検索、ソーシャル、Commerce同期時に新しいトラッキング URL を広告ネットワークに自動的にアップロードできます。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

1. キャンペーンごとに、次の操作を行います。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Campaigns]** をクリックします。

   1. キャンペーン名の上にカーソルを置き、![&#x200B; メニューアイコン &#x200B;](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ") をクリックして、**[!UICONTROL Edit]** を選択します。

   1. 「**[!UICONTROL Set Campaign Tracking]**」をクリックします。 次に、**[!UICONTROL Override Account Tracking]** すオプションを選択します。

   1. [!UICONTROL Tracking Type] 設定で、「**[!UICONTROL EF Redirect]**」を選択します。

   1. （検索、ソーシャル、CommerceでAdobe Analyticsとデータを交換したり、[!DNL Apple Safari] で発生したコンバージョンを追跡したりできるようにするには、[!UICONTROL Redirect Type] オプションの **[!UICONTROL Token]** を選択します）。

   1. （オプション）「**[!UICONTROL Auto Upload]**」オプションをオンにすると、次回の検索、ソーシャル、Commerce同期時に新しいトラッキング URL を広告ネットワークに自動的にアップロードできます。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

## トラッキング URL の生成とアップロード {#generate-upload-tracking-urls}

[&#x200B; クリックトラッキング URL を生成するタイミングと方法 &#x200B;](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md) を参照してください。

### クリックの追跡 URL の形式をテスト {#validate-tracking-urls}

クリックトラッキング URL に対して正しいランディングページが開いていることを確認します。

1. 広告主のステージング環境にトラフィックを送信して、広告クリックを模倣します。

   1. テキストエディターで、クリックトラッキング URL を貼り付け、ランディングページの URL を広告主のステージング環境内の同じページを指すように変更し、ブラウザーのアドレスバーに新しい URL を貼り付けて、**[!DNL Enter]** キーを押します。

   1. ブラウザーに保存されている Cookie で Cookie を検索します。

   1. ステージングサイトでトランザクションを完了し、成功ページで正しいピクセルが実行されていることを確認します。 ピクセルがトラッキングする実際のパラメーターは、広告主とトラッキング URL によって異なります。 次の例では、広告主は新規申込数と新規売上高をトラッキングしたいと考えています。

      （新しい cookie を使用する）新規エンドユーザーの場合、次のピクセルを起動する必要があります。

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      cookie が新しくない場合は、次のピクセルを呼び出す必要があります。

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. ドメイン内の複数のクリックトラッキング URL に対して繰り返します。

1. ドメインごとに異なるランディングページを使用して、手順 1 を繰り返します。

1. 必要に応じて、検索、ソーシャル、Commerceで、テスト中に生成されたトランザクション ID （`ev_transid`）のピクセルを確認できます。

>[!MORELIKETHIS]
>
>* [&#x200B; クリックトラッキング URL を生成するタイミングと方法 &#x200B;](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
