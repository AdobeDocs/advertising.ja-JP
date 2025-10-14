---
title: データソース  [!DNL Google Analytics]  再認証
description: 関連付けられたパスワードを変更した場合や証明書の有効期限が切れた場合に、データ  [!DNL Google Analytics]  ースを再認証する方法について説明します。
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '238'
ht-degree: 0%

---

# [!DNL Google Analytics] データソースの再認証

*代理店管理者、代理店担当営業、Adobe担当営業および管理者専用*

データソースに使用されているメールアカウントのパスワードを変更した場合、またはアカウントの [!DNL OAuth] 証明書が期限切れになった場合、メールアカウントへのすべての開いている接続は閉じられるので、データの同期を再開するには再認証する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Admin]/[!UICONTROL Data Source Setup]** をクリックします。

1. 再認証するデータソースの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[![&#x200B; 編集 &#x200B;](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. [&#x200B; データソース設定 &#x200B;](data-source-settings.md) を編集します。

   1. [!UICONTROL Connect to Google Analytics] セクションで、次の操作を行います。

      1. （必要な場合）このデータソースのデータへのアクセスに使用する新しいメールアドレスを入力します。 メールアドレスは、[!DNL Google] アカウントに登録され、[!DNL Google Analytics] アカウントの「読み取りと分析」権限を持っている必要があります。 [&#x200B; のユーザー権限の割り当て手順  [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587) を参照してください。

         >[!TIP]
         >
         >検索、ソーシャル、Commerce内で特定の [!DNL Google Analytics] プロパティおよびビューのみを使用できるようにするには、これらのプロパティおよびビューにのみアクセスできるメールアドレスを使用してログインします。

   1. チェックボックスをオンにして、「検索」、「ソーシャル」、「Commerce」を認証し、アカウントの指標へのアクセスを許可します。

   1. 「**[!UICONTROL Re-Authenticate]**」をクリックします。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; 同期  [!DNL Google Analytics]  コンバージョン指標について &#x200B;](data-source-about.md)
>* [&#x200B; データソースを設定するため  [!DNL Google Analytics]  前提条件 &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースとして  [!DNL Google Analytics]  ビューを設定する &#x200B;](data-source-configure.md)
>* [&#x200B; データソース  [!DNL Google Analytics]  編集 &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期の一時停止 &#x200B;](data-source-pause.md)
>* [[!DNL Google Analytics]  データソース設定 &#x200B;](data-source-settings.md)
>* [&#x200B; 付録 – 利用可能  [!DNL Google Analytics]  指標 &#x200B;](data-source-ga-metrics.md)
