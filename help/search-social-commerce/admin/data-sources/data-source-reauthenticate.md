---
title: の再認証 [!DNL Google Analytics] データソース
description: の再認証方法を説明します。 [!DNL Google Analytics] データソースを設定します。
role: User, Admin
exl-id: 9233e004-8607-444a-ba99-f63cb83a8b7a
feature: Search Admin, Search Data Sources
source-git-commit: 9c4dcb19e386d8e1eea541776f5b92c9d500ae9f
workflow-type: tm+mt
source-wordcount: '241'
ht-degree: 0%

---

# の再認証 [!DNL Google Analytics] データソース

*代理店管理者、代理店のアカウントマネージャ、Adobeのアカウントマネージャ、および管理者のみ*

データソースに使用される電子メールアカウントのパスワードを変更した場合、または [!DNL OAuth] アカウントの証明書の有効期限が切れた後、電子メールアカウントへのオープン接続がすべて閉じられます。データの同期を再開するには、再認証が必要です。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Data Source Setup]**.

1. 再認証するデータソースの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [データソース設定](data-source-settings.md):

   1. Adobe Analytics の [!UICONTROL Connect to Google Analytics] 「 」セクションで、以下の操作を実行します。

      1. （必要に応じて）このデータソースのデータへのアクセスに使用する新しい電子メールアドレスを入力します。 電子メールアドレスを [!DNL Google] アカウントに追加し、 [!DNL Google Analytics] アカウント。 詳しくは、 [でのユーザー権限の割り当て手順 [!DNL Google Analytics]](https://support.google.com/analytics/answer/9305587).

         >[!TIP]
         >
         >特定の [!DNL Google Analytics] プロパティとビューは、Search、Social、および Commerce 内で使用でき、プロパティとビューのみにアクセスできる電子メールアドレスを使用してログインします。

   1. アカウントの指標にアクセスすることを許可する場合は、このチェックボックスを選択します。

   1. クリック **[!UICONTROL Re-Authenticate]**.

1. クリック **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics] コンバージョン指標](data-source-about.md)
>* [の設定の前提条件 [!DNL Google Analytics] データソース](data-source-prerequisites.md)
>* [の設定 [!DNL Google Analytics] データソースとして表示](data-source-configure.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [[!DNL Google Analytics] データソース設定](data-source-settings.md)
>* [付録 — 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
