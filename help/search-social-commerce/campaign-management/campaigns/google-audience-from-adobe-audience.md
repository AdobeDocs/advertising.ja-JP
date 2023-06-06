---
title: 作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences
description: 作成方法を学ぶ [!DNL Google Ads] 既存のAdobe AnalyticsおよびAudience Managerオーディエンスのオーディエンスに一致する顧客。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '589'
ht-degree: 0%

---

# 作成 [!DNL Google Ads] Adobe AnalyticsおよびAudience Managerオーディエンスからのオーディエンスに一致する顧客

*[!DNL Google Ads]カスタマーマッチの条件を満たすアカウント*

*AdobeAdvertising-Adobe Audience ManagerまたはAdobeAdvertising-Adobe Analyticsの統合のみを使用する広告主*

オプトインした広告主が [!DNL Google Ads] (a) のユーザー ID を使用したオーディエンスの顧客一致 [!DNL Analytics] Adobe Experience Cloudおよび b) 検索、ソーシャル、コマースを宛先として持つAudience Managerセグメント（を含む） [!DNL Analytics] Adobe Experience Cloudに公開されたセグメントと、Adobe Experience Cloud Audience Library を使用して作成されたセグメント。 検索、ソーシャル、コマースは、 [!DNL Google] 各 [!DNL Analytics] またはAudience Managerセグメントで [!DNL Google] オーディエンスを追跡できます。

各 [!DNL Adobe] オーディエンスは 1 つにのみ使用できます [!DNL Google] オーディエンス。

新規 [!DNL Google] オーディエンスは元の [!DNL Adobe] オーディエンス。 [!DNL Google] は、オーディエンスがターゲティング可能である必要があるサイズを決定します。

>[!TIP]
>
>リアルタイムセグメント化の場合は、Audience Managerが作成したオーディエンスを使用します。 で作成されたセグメント [!DNL Analytics] とは 1 日にしか同期されないので、Adobe Experience Cloudと同期された母集団は少ない場合があります。セグメントの対象となるサーファーは、次の日までセグメントに含まれない場合があります。 セグメント元 [!DNL Analytics] のデータソースは「report suite - 」です。

>[!NOTE]
>
>検索、ソーシャル、コマースでは、 [!DNL Adobe] 作成または編集に使用されるセグメント [!DNL Google] オーディエンス。

1. 必要に応じて前提条件を満たします。

   1. （ユーザー ID リマーケティングリストのオーディエンスを作成するには） [!DNL Adobe] 管理者ユーザーまたはアカウントマネージャーは、顧客一致オーディエンスを有効にする広告主レベルの設定を選択する必要があります。 設定は、Audience Managerの広告主と [!DNL Analytics] のみ。

   1. の実装 [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html?lang=en) バージョン 2.0 以降。

   1. オーディエンスのトラッキング元となる広告主の Web ページに、できる限り高い位置に次のタグをデプロイします

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      場所 `Advertising_Cloud_UserID` は、広告主に割り当てられる一意のユーザー ID です。 例：  `<script src="//pixel.everesttech.net/rlsa/1234" type="text/javascript"> </script>`

   1. （まだ完了していない場合）許可されたユーザーは、次のように広告主のアカウントを設定する必要があります。 [Adobe Experience Cloudの広告主の組織アカウントとの同期](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Library]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. オーディエンス情報を指定します。

   1. 内 **[!UICONTROL Data Source]** メニュー、選択 **[!UICONTROL Adobe Audience]**.

   1. を選択します。 [!UICONTROL Adobe Audience] 基地となる [!DNL Google] オーディエンス。

      >[!NOTE]
      >
      >[!DNL Adobe] 別のオーディエンスに既に使用されている [!DNL Google] オーディエンスを使用できません。

      オプションで、3 文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスの場合、 **[!UICONTROL Include]** をクリックして選択します。

      複数の [!DNL Adobe] オーディエンスを作成し、別の [!DNL Google] オーディエンスはそれぞれに対して作成されます。

   1. を選択します。 **[!UICONTROL Audience Type]** 次を作成します。 **[!UICONTROL Customer List_User ID]**.

      広告主の [!DNL Google Ads] アカウントは [カスタムマッチの対象となる](https://support.google.com/adspolicy/answer/6299717) を選択し、 [ユーザー ID リマーケティング](https://support.google.com/google-ads/answer/9199250).

   1. 「 」チェックボックスを選択して、の利用条件に同意したことを示します [!DNL Adobe] および広告ネットワークのプライバシーポリシー。

   1. 次の数を指定： **[!UICONTROL Membership Days]**：ユーザーの Cookie がオーディエンスに残る日数です。

      広告がユーザーに関連すると予想される時間の長さを使用します。 リマーケティングリストの期間は最大 540 日です。 顧客リストに最大期間がありません。cookie の有効期限が切れないことを示すには、「10000」と入力します。

   1. クリック **[!UICONTROL Post]**.

>[!NOTE]
>
>* [!DNL Google] は、ファイルの処理に最大 24 時間かかる場合があります。
>
>* 詳しくは、 [[!DNL Google Ads] カスタマーマッチの仕組みと制限に関するドキュメント](https://support.google.com/displayvideo/answer/9539301).


>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)

