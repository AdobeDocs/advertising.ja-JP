---
title: ' [!DNL Google Analytics]  データソースの再認証'
description: 関連するパスワードを変更するか、証明書の有効期限が切れる場合に [!DNL Google Analytics]  データソースを再認証する方法について説明します。
role: User, Admin
exl-id: 624f0f0e-3f2f-45b1-b3dc-c1b107b4736f
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/1xjaqEk70Yr2rAcR95CteZ46OTG--xSao09B3CdCvCo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2:
  - id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 238
ht-degree: 0%

---

# [!DNL Google Analytics] データソースの再認証

*代理店の管理者、代理店のアカウントマネージャー、Adobeのアカウントマネージャー、および管理者のみ*

データソースに使用する電子メールアカウントのパスワードを変更した場合、またはアカウントの[!DNL OAuth]証明書が期限切れになった場合、電子メールアカウントに対して開いているすべての接続が閉じられ、再認証してデータの同期を再開する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**&#x200B;をクリックします。

1. 再認証するデータソースの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. [&#x200B; データソース設定](data-source-settings.md)を編集します。

   1. 「[!UICONTROL Connect to Google Analytics]」セクションで、次の操作を行います。

      1. （必要に応じて）このデータソースのデータへのアクセスに使用する新しいメールアドレスを入力します。 メールアドレスは[!DNL Google] アカウントに登録し、[!DNL Google Analytics] アカウントに「読み取りと分析」権限を持っている必要があります。 [&#x200B; [!DNL Google Analytics]でユーザー権限を割り当てる方法については、](https://support.google.com/analytics/answer/9305587)の手順を参照してください。

         >[!TIP]
         >
         >Search, Social, &amp; Commerce内で特定の[!DNL Google Analytics]個のプロパティとビューのみを使用できるようにするには、それらのプロパティとビューのみにアクセスできるメールアドレスを使用してログインします。

   1. このチェックボックスをオンにすると、Search、Social、およびCommerceでアカウントの指標にアクセスできるようになります。

   1. **[!UICONTROL Re-Authenticate]**&#x200B;をクリックします。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics]  コンバージョン指標](data-source-about.md)
>* [&#x200B; データソースを設定するための前提条件 [!DNL Google Analytics] &#x200B;](data-source-prerequisites.md)
>* [&#x200B; データソースとして [!DNL Google Analytics]  ビューを設定](data-source-configure.md)
>* [&#x200B; データソースの編集 [!DNL Google Analytics] &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期を一時停止](data-source-pause.md)
>* [[!DNL Google Analytics]  データソース設定](data-source-settings.md)
>* [付録 – 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
