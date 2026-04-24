---
title: ' [!DNL Adobe] 件のオーディエンスから [!DNL Google Ads] 顧客マッチオーディエンスを作成'
description: 既存のAdobe AnalyticsおよびAudience Manager オーディエンスから [!DNL Google Ads]  カスタマーマッチオーディエンスを作成する方法について説明します。
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/Ep3X-eo2kcGlW3NsV3CJEKBkEapa-oAv0HLexc1xnhM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 586
ht-degree: 0%

---

# Adobe AnalyticsおよびAudience Manager オーディエンスから[!DNL Google Ads]件のカスタマーマッチオーディエンスを作成

顧客の一致のみ&#x200B;*の対象となる*[!DNL Google Ads] アカウント

*Adobe AdvertisingとAdobe Audience ManagerまたはAdobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

オプトインした広告主は、a） Adobe CX Enterpriseと共有される[!DNL Analytics]個のセグメントとb） Adobe CX Enterpriseに公開される[!DNL Analytics]個のセグメントとAudience Manager Audience Libraryを使用して作成されるセグメントを含む、Search, Social, &amp; Commerceを宛先として持つAdobe CX Enterprise セグメントのa） 個のユーザーIDを使用して[!DNL Google Ads]個のカスタマーマッチオーディエンスを作成できます。 Search, Social, &amp; Commerceは、[!DNL Google] トラッキング URLを各[!DNL Analytics]またはAudience Manager セグメントに自動的にプッシュして、[!DNL Google]がオーディエンスをトラッキングできるようにします。

各[!DNL Adobe] オーディエンスは、1つの[!DNL Google] オーディエンスにのみ使用できます。

新しい[!DNL Google] オーディエンスは、元の[!DNL Adobe] オーディエンスと同じ名前になります。 [!DNL Google]は、ターゲティング可能なオーディエンスの規模を決定します。

>[!TIP]
>
>リアルタイムのセグメンテーションには、Audience Managerで作成したオーディエンスを利用できます。 [!DNL Analytics]で作成され、Adobe CX Enterpriseに同期されたセグメントは、毎日のみ同期されるため、母集団が少ない可能性があります。セグメントの資格を持つサーファーは、翌日までセグメントに含まれない可能性があります。 [!DNL Analytics]のセグメントには、「レポートスイート – 」というデータソースがあります。

>[!NOTE]
>
>Search, Social, &amp; Commerceでは、[!DNL Google] オーディエンスの作成または編集に使用した[!DNL Adobe] セグメントの顧客データは保存されません。

1. 必要に応じて前提条件を満たします。

   1. （ユーザーID リマーケティングリストのオーディエンスを作成するには） [!DNL Adobe]管理者ユーザーまたはアカウントマネージャーは、顧客一致オーディエンスを有効にするために、広告主レベルの設定を選択する必要があります。

   1. [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html) バージョン 2.0以降を実装します。

   1. オーディエンスを追跡する必要がある広告主のweb ページに、次のタグをできるだけ高くデプロイします

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      ここで、`Advertising_Cloud_UserID`は、広告主に割り当てられた一意の数値ユーザーIDです。

      例：`<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （まだ完了していない場合）承認済みユーザーは、広告主のアカウントを[Adobe CX Enterpriseの広告主の組織アカウントと同期するように設定する必要があります](/help/search-social-commerce/admin/sync-adobe-audiences.md)。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワークとアカウント名を選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. オーディエンス情報を指定します。

   1. **[!UICONTROL Data Source]** メニューで、**[!UICONTROL Adobe Audience]**&#x200B;を選択します。

   1. [!DNL Google] オーディエンスのベースとなる[!UICONTROL Adobe Audience]を選択します。

      >[!NOTE]
      >
      >別の[!DNL Google] オーディエンスに既に使用されている[!DNL Adobe] オーディエンスは使用できません。

      オプションで、3文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスの場合は、**[!UICONTROL Include]**&#x200B;をクリックして選択します。

      複数の[!DNL Adobe] オーディエンスを選択した場合、それぞれに対して個別の[!DNL Google] オーディエンスが作成されます。

   1. 作成する&#x200B;**[!UICONTROL Audience Type]**&#x200B;を選択：**[!UICONTROL Customer List_User ID]**。

      広告主の[!DNL Google Ads] アカウントは[&#x200B; カスタムマッチの対象](https://support.google.com/adspolicy/answer/6299717)で、[&#x200B; ユーザーID リマーケティング &#x200B;](https://support.google.com/google-ads/answer/9199250)にオプトインしている必要があります。

   1. 「[!DNL Adobe]」および広告ネットワークのプライバシーポリシーの条件に同意することを示すチェックボックスをオンにします。

   1. ユーザーのCookieがオーディエンスに滞在する日数である&#x200B;**[!UICONTROL Membership Days]**&#x200B;の数を指定します。

      広告がユーザーに適していると期待される期間を使用します。 リマーケティングリストの最大期間は540日です。 顧客リストには最大期間がありません。Cookieの有効期限が切れないことを示すには、10000と入力します。

   1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!NOTE]
>
>* [!DNL Google]は、ファイルの処理に最大24時間かかる場合があります。
>
>* 顧客の一致の仕組みと制限に関する[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/displayvideo/answer/9539301)を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスについて](audience-about.md)
>* [Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
