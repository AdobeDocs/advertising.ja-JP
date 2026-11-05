---
title: オーディエンスの管理
description: オーディエンスライブラリと、Google AdsおよびMicrosoft Advertisingでサポートされているオーディエンスを管理する方法について説明します。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
    internal-label: Privacy
source-git-commit: 7e7dcde9fb195e04025a1a8d89e792ff562b053f
workflow-type: tm+mt
source-wordcount: '630'
ht-degree: 0%
---
# オーディエンスの管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

オーディエンスは、[&#x200B; ターゲット &#x200B;](audience-targets-manage.md)または[除外](audience-exclusions.md)として、同じ広告ネットワークでサポートされているキャンペーンと広告グループに使用できるユーザーグループです。 広告ネットワークは、ターゲティングできるオーディエンスの規模を決定します。

## [!UICONTROL Library] ビューについて {#audience-view-about}

[!UICONTROL Targeting] > [!UICONTROL Audiences] > [!UICONTROL Library] ビューには、選択した広告主のオーディエンスが一覧表示されます。 [!DNL Google Ads]と[!DNL Microsoft Advertising]のオーディエンスを表示するには、**[!UICONTROL Network]** メニューから&#x200B;**[!UICONTROL All Other Network]**&#x200B;を選択します。

ライブラリには、[!DNL Google Ads]個の顧客データベース、市場内、類似オーディエンスと[!DNL Microsoft Advertising]個のリマーケティング、動的リマーケティング、カスタム、顧客照合、市場内、類似オーディエンスが含まれています。

データを表示するには、[!UICONTROL View Audiences]権限が必要です。 行を選択し、サポートされているオーディエンスを削除するには、[!UICONTROL Edit Audience Library]権限が必要です。

### 使用可能なアクション

<!--
Restricted to internal beta users:

* [Create a customer match audience from a customer data list](#audience-customer-list-create)

* [Create a Google Ads audience from Adobe audiences](#audience-adobe-create)

* [Create a Microsoft Advertising dynamic remarketing audience](#audience-dynamic-create)

* [Update a customer match audience using a customer data list](#audience-customer-list-edit)

* [Edit a dynamic remarketing audience](#audience-dynamic-edit)
-->

* [動的リマーケティングオーディエンスの削除](#audience-delete)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

## オーディエンスデータソース {#audience-data-sources}

次のデータソースに基づいてオーディエンスを使用できます。

* **Adobe オーディエンスセグメント：** オプトインしたAdobe Audience ManagerまたはAdobe Analytics アカウントを持つ広告主は、既存の[!DNL Adobe] セグメントに基づいて[!DNL Google Ads]人の顧客マッチオーディエンスを使用できます。

  * [!DNL Analytics] アカウントを持つ広告主で、Audience Managerを持っていない場合、オーディエンスはAdobe CX Enterpriseと共有された[!DNL Analytics] セグメントのユーザーIDを使用します。

  * Audience Manager アカウントを持つ広告主の場合、オーディエンスは、Search、Social、およびCommerceを宛先とするAudience Manager セグメントのユーザーIDを使用します。 これには、Adobe CX Enterpriseに公開された[!DNL Analytics]個のセグメントと、Adobe CX Enterprise Audience Libraryを使用して作成されたセグメントが含まれます。

  [!DNL Google Ads] アカウントは、[顧客の一致](https://support.google.com/adspolicy/answer/6299717)の対象で、[&#x200B; ユーザーID セグメント &#x200B;](https://support.google.com/google-ads/answer/9199250)に対してオプトインしている必要があります。 Search, Social, &amp; Commerceの広告主アカウントも、カスタマーマッチオーディエンスの作成を許可するように設定する必要があります。 この機能を有効にするには、Adobe アカウントチームにお問い合わせください。

  顧客データベースのオーディエンスの[!DNL Adobe]個のセグメントデータとcookie同期ファイルは、毎日[!DNL Google Ads]個に同期されます。

* **Adobe Campaignのメールリスト：** Adobe アカウントチームは、[!DNL Campaign]のメールリストから[!DNL Google Ads]のカスタマーマッチオーディエンスを作成および更新するワークフローを設定できます。 ワークフローは、オーディエンスライブラリではなく、[!DNL Campaign]で設定されています。 「[Adobe Campaign メールリストからカスタマーマッチオーディエンスを作成](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-campaign-email-list.md)」を参照してください。

* **顧客データリスト：**&#x200B;対象アカウントが[!DNL Google Ads]または[!DNL Microsoft Advertising]の広告主は、顧客関係管理（CRM）システムのプライマリ IDを含むCSV ファイルに基づいて、顧客照合オーディエンスを使用できます。

* **動的リマーケティングリスト：** [!DNL Microsoft Advertising] アカウントを持つ広告主は、製品の閲覧者や過去の購入者など、最近製品を操作したユーザーに基づいてオーディエンスを使用できます。 これらのオーディエンスを活用するには、関連するweb ページに広告ネットワークのJavaScriptコンバージョンタグとオーディエンストラッキングタグが必要です。

  動的リマーケティングオーディエンスは、検索連動型およびオーディエンスネットワーク上のショッピングキャンペーンと共に、商品広告によるユーザーのリターゲティングを行い、検索キャンペーンと共にテキスト広告と動的検索広告によるユーザーのリターゲティングを行うことができます。

  >[!NOTE]
  >
  >動的リマーケティングオーディエンスターゲットの入札修飾子は、[!UICONTROL Auto-optimize Bid Adjustment Values]設定のポートフォリオでは最適化されません。

>[!NOTE]
>
>Search, Social, &amp; Commerceには、オーディエンスの作成や編集に使用した[!DNL Adobe] セグメントからアップロードした顧客データや顧客データは保存されません。

<!--
Restricted to internal beta users: audience creation and library editing.

## Create a customer match audience from a customer data list {#audience-customer-list-create}

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts that are eligible for customer match only*

For [!DNL Microsoft Advertising], the file can include email addresses. For [!DNL Google Ads], the file can include email addresses, mailing addresses, telephone numbers, user IDs, or mobile device IDs.

Creating and editing library audiences requires the [!UICONTROL Edit Audience Library] permission in addition to internal beta access.

1. Prepare a CSV file with the customer data in the required format.

   First and last names, email addresses, and telephone numbers must be hashed using SHA-256. Follow the network's formatting requirements for the selected identifier type. See the [Google Ads formatting guidelines](https://support.google.com/google-ads/answer/7476159) or the [Microsoft Advertising instructions for preparing customer match lists](https://help.ads.microsoft.com/#apex/ads/en/56921).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select the ad network and account.

1. In **[!UICONTROL Data Source]**, select the customer-list option.

1. Enter the **[!UICONTROL Audience Name]** and select the **[!UICONTROL Data Upload Type]**:

   * ([!DNL Microsoft Advertising]) **[!UICONTROL Emails]**.

   * ([!DNL Google Ads]) **[!UICONTROL Emails, Phones, and/or Mailing Addresses]**, **[!UICONTROL User IDs]**, or **[!UICONTROL Mobile Device IDs]**.

     User ID lists are available only to eligible [!DNL Google Ads] advertisers in the U.S. who are opted in for user ID segments.

1. (Mobile device ID lists only) Select the **[!UICONTROL OS Type]** and enter the **[!UICONTROL App ID]**.

   For an Android app, use its package name in [!DNL Google Play], such as `com.example.game` from `https://play.google.com/store/apps/details?id=com.example.game`. For an iOS app, use its application ID from the [!DNL App Store], such as `id284882215`. Your development team can provide the ID.

1. In **[!UICONTROL Select File]**, select the CSV file from your device or network.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. ([!DNL Google Ads]; optional) If you do business in the European Economic Area (EEA) or United Kingdom (UK) and have collected all required user consents, select the consent check box to send the consent status as **[!UICONTROL GRANTED]** for advertising and ad personalization.

   If you leave the check box unselected, the consent status is sent as **[!UICONTROL UNSPECIFIED]**. [!DNL Google Ads] ignores data for EEA and UK users with an unspecified consent status, which can cause data discrepancies and performance issues.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Membership days specify how long a user's cookie stays in the audience. Use the length of time for which you expect the ad to remain relevant. Customer lists don't expire unless you enter a value.

1. Click **[!UICONTROL Review and Save]**.

1. Review the settings. To change a setting, click **[!UICONTROL Edit]** in the applicable section.

1. Click **[!UICONTROL Create]**.

The ad network may take up to 24 hours to process the file. See the [Google Ads documentation on customer match and its limitations](https://support.google.com/displayvideo/answer/9539301).

## Create Google Ads customer match audiences from Adobe audiences {#audience-adobe-create}

*Advertisers with an Adobe Advertising-Adobe Audience Manager or Adobe Advertising-Adobe Analytics integration only*

Each [!DNL Adobe] audience can be used for only one [!DNL Google Ads] audience. Each new audience has the same name as the original [!DNL Adobe] audience.

1. Complete the prerequisites:

   1. Ask an [!DNL Adobe] administrator or account manager to enable customer match audiences for the advertiser.

   1. Implement the [Adobe Experience Platform Identity Service](https://experienceleague.adobe.com/docs/id-service/using/home.html){target="_blank"} version 2.0 or higher.

   1. Deploy the following tag as high as possible on the advertiser's webpages from which the audience should be tracked:

      `<script src="//pixel.everesttech.net/rlsa/<Advertising_Cloud_UserID>" type="text/javascript"> </script>`

      Replace `Advertising_Cloud_UserID` with the advertiser's unique numeric user ID.

   1. Have an authorized user [configure synchronization with the advertiser's organization account in Adobe CX Enterprise](/help/search-social-commerce/admin/sync-adobe-audiences.md).

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Google Ads] and the account.

1. In **[!UICONTROL Data Source]**, select the Adobe audience option.

1. In **[!UICONTROL Adobe Audience]**, select one or more available segments. You can search the list.

   Segments already used for another [!DNL Google Ads] audience aren't available. If you select multiple segments, a separate audience is created for each segment.

1. Select the available customer list user ID option in **[!UICONTROL Audience Type]**.

1. Select the check box to indicate that you agree with the [!DNL Adobe] and ad network privacy policies.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available.

   Remarketing lists have a maximum duration of 540 days. Customer lists don't have a maximum duration; enter 10000 to indicate that the cookie never expires.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Search, Social, & Commerce automatically pushes a [!DNL Google] tracking URL back to each source segment so that [!DNL Google] can track the audience. [!DNL Google] may take up to 24 hours to process the audience.

>[!TIP]
>
>For real-time segmentation, use Audience Manager-created audiences. [!DNL Analytics] segments synced to Adobe CX Enterprise may have smaller populations because they're synced daily. Users who qualify for a segment may not be included until the next day.

## Create a Microsoft Advertising dynamic remarketing audience {#audience-dynamic-create}

You can create multiple dynamic remarketing audiences using the same tracking tag.

1. Implement the [Microsoft Advertising universal event tracking (UET) tag with the required product ID and page type parameters](https://help.ads.microsoft.com/#apex/ads/en/56910/1/#exp85) on the relevant webpages. Identify the tag's name.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu, and then click **[!UICONTROL Create Audience]**.

1. In **[!UICONTROL Basic Settings]**, select [!DNL Microsoft Advertising] and the account.

1. In **[!UICONTROL Data Source]**, select the dynamic remarketing list option.

1. Enter the **[!UICONTROL Audience Name]**.

1. In **[!UICONTROL Tag Name]**, select the UET tag on the webpages whose users comprise the audience.

1. In **[!UICONTROL Whom to add to your audience]**, select **[!UICONTROL General Visitors]**, **[!UICONTROL Product Searchers]**, **[!UICONTROL Product Viewers]**, **[!UICONTROL Past Buyers]**, or **[!UICONTROL Shopping Cart Abandoners]**.

1. Configure any remaining audience settings, including **[!UICONTROL Membership Days]** when available. For dynamic remarketing audiences, membership can range from 1-180 days.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Create]**.

Dynamic remarketing audiences are eligible for targeting once they include at least 300 users.

## Update a customer match audience using a customer data list {#audience-customer-list-edit}

You can update customer match audiences created from data files, but not [!DNL Google Ads] audiences created from [!DNL Adobe] audiences. You can add or delete members, or replace all existing members. You can't edit multiple library audiences at once.

1. Prepare a CSV file in the required format, using the same data type as the original list. For mobile device IDs, use the same app and operating system.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. In **[!UICONTROL Select Action]**, select:

   * **[!UICONTROL Add]:** Add members from the uploaded file who aren't already in the audience.

   * **[!UICONTROL Delete]:** Remove members in the uploaded file from the audience.

   * **[!UICONTROL Replace]:** Replace all existing audience members with the uploaded data.

1. In **[!UICONTROL Select File]**, select the CSV file, accept the privacy policies, and configure the applicable consent setting.

1. Click **[!UICONTROL Upload File]** and wait for the upload to finish.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.

The ad network may take a while to process audience updates.

## Edit a dynamic remarketing audience {#audience-dynamic-edit}

You can change a [!DNL Microsoft Advertising] dynamic remarketing audience's name, UET tag, and visitor type. You can't change its membership duration or edit multiple library audiences at once.

1. In the main menu, click **[!UICONTROL Targeting] > [!UICONTROL Audiences]**, and then click the **[!UICONTROL Library]** tab.

1. Select **[!UICONTROL All Other Network]** from the **[!UICONTROL Network]** menu.

1. Select the check box next to one dynamic remarketing audience, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.

1. Edit the **[!UICONTROL Audience Name]**, **[!UICONTROL Tag Name]**, or **[!UICONTROL Whom to add to your audience]**.

1. Click **[!UICONTROL Review and Save]**, review the settings, and then click **[!UICONTROL Update]**.
-->

## 動的リマーケティングオーディエンスの削除 {#audience-delete}

[!DNL Microsoft Advertising]個の動的リマーケティングオーディエンスを1つずつ削除できます。 ライブラリから他の[!DNL Google Ads]または[!DNL Microsoft Advertising]個のオーディエンスタイプを削除することはできません。

1. メインメニューで、**[!UICONTROL Targeting]>[!UICONTROL Audiences]**&#x200B;をクリックし、**[!UICONTROL Library]** タブをクリックします。

1. **[!UICONTROL Network]** メニューから&#x200B;**[!UICONTROL All Other Network]**&#x200B;を選択します。

1. 1つの動的リマーケティングオーディエンスの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンと広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
>* [&#x200B; キャンペーンと広告グループのオーディエンス除外の管理](audience-exclusions.md)
