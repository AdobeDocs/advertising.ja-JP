---
title: Cookie ベースのクリック追跡の設定
description: クリックトラッキングタグの設定と検証方法について説明します。
exl-id: 3f2b09bc-9794-41d1-89fc-0d239bad2fb1
feature: Search Tracking
TQID: https://experienceleague.adobe.com/cs39NoKUXfx4PdrzULocZEOW0SUGtXrpmO4I3IXefwA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 542
ht-degree: 0%

---

# Cookie ベースのクリック追跡の設定

Search, Social, &amp; Commerceでクリックをトラッキングするには、次の要素を設定して検証する必要があります。

1. （Adobe Account Team）広告主をピクセルカスタマーとして設定します。

1. [広告主の広告ネットワークアカウントとキャンペーンごとに正しいトラッキングオプションを指定](#set-up-click-tracking-options)。

1. 必要に応じて、[ トラッキング URLを生成し、一部のキャンペーン要素に](#generate-upload-tracking-urls) アップロードします。

1. [いくつかのクリックトラッキング URLの形式を検証し、それらをテストして、正しいランディングページが開くことを検証します](#validate-tracking-urls)。

## 広告ネットワークアカウントとキャンペーンのトラッキングオプションを設定する {#set-up-click-tracking-options}

*代理店アカウントマネージャー、[!DNL Adobe] アカウントマネージャー、管理者ユーザーの役割のみ*

1. 広告ネットワークアカウントごとに、次の操作を行います。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Accounts]**&#x200B;をクリックします。

   1. アカウント名の上にカーソルを置き、![ メニューアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ")をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

   1. **[!UICONTROL Set Account Tracking]**&#x200B;をクリックします。

   1. [!UICONTROL Tracking Type]設定で、**[!UICONTROL EF Redirect]**&#x200B;を選択します。

   1. （Search、Social、およびCommerceでAdobe Analyticsとデータを交換したり、[!DNL Apple Safari]で発生したコンバージョンをトラッキングしたりできるようにするには）「[!UICONTROL Redirect Type]」オプション「**[!UICONTROL Token]**」を選択します。

   1. （オプション）「**[!UICONTROL Auto Upload]**」オプションをオンにすると、Search、Social、およびCommerceが次回に同期したときに、新しいトラッキング URLが自動的にアドネットワークにアップロードされます。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

1. キャンペーンごとに、次の操作を行います。

   1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Campaigns]**&#x200B;をクリックします。

   1. キャンペーン名の上にカーソルを置き、![ メニューアイコン ](/help/search-social-commerce/assets/arrow-dropdown-menu.png " メニューアイコン ")をクリックし、**[!UICONTROL Edit]**&#x200B;を選択します。

   1. **[!UICONTROL Set Campaign Tracking]**&#x200B;をクリックします。 次に、オプションを&#x200B;**[!UICONTROL Override Account Tracking]**&#x200B;に選択します。

   1. [!UICONTROL Tracking Type]設定で、**[!UICONTROL EF Redirect]**&#x200B;を選択します。

   1. （Search、Social、およびCommerceでAdobe Analyticsとデータを交換したり、[!DNL Apple Safari]で発生したコンバージョンをトラッキングしたりできるようにするには）「[!UICONTROL Redirect Type]」オプション「**[!UICONTROL Token]**」を選択します。

   1. （オプション）「**[!UICONTROL Auto Upload]**」オプションをオンにすると、Search、Social、およびCommerceが次回に同期したときに、新しいトラッキング URLが自動的にアドネットワークにアップロードされます。 この値は、アカウント内のすべてのキャンペーンのデフォルトとして継承されますが、キャンペーンレベルで上書きできます。

## トラッキング URLの生成とアップロード {#generate-upload-tracking-urls}

「[ クリックトラッキング URLを生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)」を参照してください。

### クリックトラッキング URLの形式をテストする {#validate-tracking-urls}

クリックトラッキング URLに対して正しいランディングページが開くことを検証します。

1. 広告主のステージング環境にトラフィックを送信して、広告クリックを模倣します。

   1. テキストエディターで、クリックトラッキング URLを貼り付け、ランディングページ URLを広告主のステージング環境内の同じページを指すように変更し、ブラウザーのアドレスバーに新しいURLを貼り付けて、**[!DNL Enter]** キーを押します。

   1. ブラウザーに保存されているCookieを探します。

   1. ステージングサイトでトランザクションを完了し、成功ページで正しいピクセルが起動することを確認します。 ピクセルでトラッキングされる実際のパラメーターは、広告主とトラッキング URLによって異なります。 次の例では、広告主は新しいアプリケーションの数と新しい収益の量を追跡したいと考えています。

      新しいエンドユーザー（新しいCookieを使用）の場合は、次のピクセルを起動する必要があります。

      `< img width="1" height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_new_application=1&ev_new_amount=<loanamount>" / >`

      Cookieが更新されていない場合は、次のピクセルを起動する必要があります。

      `< img width="1"height="1" src="http://pixel-user-everesttech.net/<Advertising_Cloud_UserID>/p?ev_transid=<applicationid>&ev_previous_application=1&ev_new_amount=<loanamount>" / >`


1. ドメイン内の複数のクリックトラッキング URLに対して、この操作を繰り返します。

1. ドメインごとに手順1を繰り返し、それに応じて異なるランディングページを使用します。

1. 必要に応じて、Search、Social、およびCommerceで、テスト中に生成されたトランザクション ID （`ev_transid`）のピクセルを確認できることを確認します。

>[!MORELIKETHIS]
>
>* [ クリックトラッキング URLを生成するタイミングと方法](/help/search-social-commerce/tracking/click-tracking-ways-to-generate.md)
