---
title: オーディエ  [!DNL Google Ads]  スからの顧客一致オーディエ  [!DNL Adobe]  スの作成
description: 既存のAdobe Analytics オーディエンスおよびAudience Manager オーディエンスから  [!DNL Google Ads]  カスタマーマッチオーディエンスを作成する方法を説明します。
exl-id: 7de95ebb-24b0-459f-83c0-7b85b0c0576d
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '566'
ht-degree: 0%

---

# Adobe Analytics オーディエンス [!DNL Google Ads]Audience Manager オーディエンスからカスタマーマッチオーディエンスを作成

顧客一致の対象となるアカウントの *[!DNL Google Ads]定*

*Adobe AdvertisingとAdobe Audience ManagerまたはAdobe AdvertisingとAdobe Analyticsの統合を使用する広告主のみ*

オプトインされた広告主は [!DNL Google Ads]a） Adobe Experience Cloudと共有されるセグメントと b） Adobe Experience Cloudに公開される [!DNL Analytics] 検索、ソーシャル、Commerceを宛先とするAudience Managerの各セグメント（Adobe Experience Cloud Audience Library で作成される [!DNL Analytics] のセグメントを含む）のユーザー ID を使用してカスタマーマッチオーディエンスを作成できます。 検索、ソーシャル、Commerceでは、オーディエンスを追跡できるように、[!DNL Google] トラッキング URL が各 [!DNL Analytics] またはAudience Manager セグメントに自動的にプッシュされ [!DNL Google] す。

各 [!DNL Adobe] オーディエンスは、1 つの [!DNL Google] オーディエンスに対してのみ使用できます。

新しい [!DNL Google] オーディエンスはそれぞれ、元の [!DNL Adobe] オーディエンスと同じ名前です。 ターゲティ [!DNL Google] グ可能にするオーディエンスの大きさを決定します。

>[!TIP]
>
>リアルタイムのセグメント化には、Audience Managerで作成されたオーディエンスを使用します。 [!DNL Analytics] で作成されAdobe Experience Cloudに同期されたセグメントは、毎日同期されるだけなので、母集団が小さくなる場合があります。セグメントの対象となるサーファーは、翌日までセグメントに含まれない場合があります。 [!DNL Analytics] のセグメントのデータソースは「レポートスイート –」です。

>[!NOTE]
>
>検索、ソーシャル、Commerceには、[!DNL Google] オーディエンスの作成や編集に使用される [!DNL Adobe] セグメントの顧客データは格納されません。

1. 必要に応じて、次の前提条件を満たします。

   1. （ユーザー ID リマーケティングリストオーディエンスを作成するには） [!DNL Adobe] 管理者ユーザーまたはアカウントマネージャーは、広告主レベルの設定を選択して、顧客一致オーディエンスを有効にする必要があります。

   1. [Adobe Experience Platform ID サービス ](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=ja) バージョン 2.0 以降を実装します。

   1. オーディエンスの追跡元となる広告主の web ページに、次のタグをできるだけ高くデプロイします

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      ここで、`Advertising_Cloud_UserID` は広告主に割り当てられた一意の数値ユーザー ID です。

      例：`<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （完了していない場合）承認済みユーザーは、[Adobe Experience Cloudで広告主の組織アカウントと同期する ](/help/search-social-commerce/admin/sync-adobe-audiences.md) ように広告主のアカウントを設定する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワークとアカウント名を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. オーディエンス情報を指定します。

   1. **[!UICONTROL Data Source]** メニューで、「**[!UICONTROL Adobe Audience]**」を選択します。

   1. [!DNL Google] オーディエンスのベースとなる [!UICONTROL Adobe Audience] を選択します。

      >[!NOTE]
      >
      >別 [!DNL Adobe][!DNL Google] オーディエンスに既に使用されているオーディエンスは使用できません。

      オプションで、3 文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスがある場合は、「**[!UICONTROL Include]**」をクリックして選択します。

      複数の [!DNL Adobe] オーディエンスを選択した場合は、個別の [!DNL Google] オーディエンスが作成されます。

   1. 作成する **[!UICONTROL Audience Type]** を選択します：**[!UICONTROL Customer List_User ID]**。

      広告主の [!DNL Google Ads] アカウントは [ カスタム一致の対象 ](https://support.google.com/adspolicy/answer/6299717) であり、[ ユーザー ID のリマーケティング ](https://support.google.com/google-ads/answer/9199250) にオプトインされている必要があります。

   1. [!DNL Adobe] および広告ネットワークのプライバシーポリシーの条項に同意することを示すチェックボックスをオンにします。

   1. **[!UICONTROL Membership Days]** 数を指定します。これは、ユーザーの Cookie がオーディエンスに残る日数です。

      広告がユーザーに関連すると予想される時間の長さを使用します。 リマーケティングリストの最大期間は 540 日です。 顧客リストには最大期間はありません。cookie の有効期限がないことを示すには、10000 を入力します。

   1. 「**[!UICONTROL Post]**」をクリックします。

>[!NOTE]
>
>* ファイルの処理に最大 24 時間かかる場 [!DNL Google] があります。
>
>* [[!DNL Google Ads]  カスタマーマッチの仕組みと制限事項に関するドキュメント ](https://support.google.com/displayvideo/answer/9539301) を参照してください。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて ](audience-about.md)
>* [Adobe Campaign [!DNL Google Ads]  メールリストからカスタマーマッチオーディエンスを作成 ](google-audience-from-campaign-email-list.md)
>* [ 顧客データリストを使用したカスタマーマッチオーディエンスの管理 ](audience-from-customer-data-list.md)
>* [ 動的リマーケティングオーディエンスの管理 ](audience-dynamic-remarketing-manage.md)
