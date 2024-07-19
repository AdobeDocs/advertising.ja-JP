---
title: オーディエンスについて
description: オーディエンスを追跡、作成、管理および管理するためのオプショ  [!DNL Google Ads]  について説明  [!DNL Microsoft Advertising]  ます。
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 検索、ソーシャル、Commerceでの [!DNL Google Ads] オーディエンスおよび [!DNL Microsoft Advertising] オーディエンスの管理について

*[!DNL Google Ads]と [!DNL Microsoft Advertising] のみ*

オーディエンスライブラリには、[!DNL Google Ads] の顧客データベース、市場内、類似のオーディエンスと、[!DNL Microsoft Advertising] のリマーケティングおよび動的リマーケティング、カスタム、顧客一致、市場内および類似のオーディエンスがすべて一覧表示されます。 任意の [!DNL Google Ads] オーディエンスをキャンペーンレベルお [!DNL Google Ads] び広告グループレベルのターゲットおよび除外として使用できます。また、任意の [!DNL Microsoft Advertising] オーディエンスを [!DNL Microsoft Advertising] キャンペーンレベルおよび広告グループレベルのターゲットおよび（動的リマーケティングオーディエンスのみ）除外として使用できます。 任意のオーディエンスターゲットの入札調整を追加または編集できます。

また、既存のAdobe Experience Cloud オーディエンスのセグメントや電子メールリスト、および顧客関係管理（CRM）システムの様々な種類の顧客データを使用して、オーディエンスを作成および管理することもできます。

* **Adobeオーディエンスセグメント：** オプトインのAdobe Audience ManagerまたはAdobe Analytics アカウントを持つ広告主は、[!DNL Adobe] セグメントからカスタマーマッチオーディエンス [!DNL Google Ads] 作成できます。

   * （Audience Managerを持たない [!DNL Analytics] アカウントを持つ広告主）Adobe Experience Cloudと共有されるセグメントのユーザー ID を使用して [!DNL Google Ads] カスタマーマッチオーディエンス [!DNL Analytics] 作成できます。

   * （Audience Managerアカウントを持つ広告主）検索、ソーシャル、Commerceを宛先 [!DNL Google Ads] するAudience Managerセグメントのユーザー ID を使用して、カスタマーマッチオーディエンスを作成できます。 これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントや、Adobe Experience Cloud オーディエンスライブラリを使用して作成されたセグメントが含まれる場合があります。

  顧客一致オーディエンスを作成するには、広告主の [!DNL Google Ads] アカウントが [ カスタム一致の対象 ](https://support.google.com/adspolicy/answer/6299717) であり、[ ユーザー ID セグメント ](https://support.google.com/google-ads/answer/9199250) でオプトインされている必要があります。 また、検索、ソーシャル、Commerceの広告主アカウントも、カスタマーマッチオーディエンスを作成できるように設定する必要があります。

  顧客デ [!DNL Adobe] タベースのオーディエンスのセグメントデータと cookie 同期ファイルは、毎日 [!DNL Google Ads] に同期されます。

* **Adobe Campaignの電子メールリスト：** Adobeアカウントチームは、[!DNL Campaign] 内の電子メールリストから [!DNL Google Ads] カスタマーマッチオーディエンスを作成および更新するワークフローの設定を支援します。

* **顧客データリスト：** 顧客一致の対象となる [!DNL Google Ads] アカウントまたは [!DNL Microsoft Advertising] アカウントを持つ広告主は、広告ネットワーク固有の顧客データベースのオーディエンスを作成および更新できます &lt;! – または動的リマーケティングオーディエンス – 顧客データベースのオーディエンスに含めます（少なくとも [!DNL Google Ads]?—> の場合）。プライマリ識別子を含む CSV ファイルをアップロードします。

* **動的リマーケティングリスト：** [!DNL Microsoft Advertising] アカウントを持つ広告主は、動的リマーケティングオーディエンスを作成および管理できます。このオーディエンスを使用して、複数の方法（製品ビューアや過去の購入者など）のいずれかで製品を最近操作した潜在的な顧客をリターゲティングできます。 動的リマーケティングオーディエンスでは、web ページで広告ネットワークのJavaScript コンバージョンタグとオーディエンストラッキングタグを使用する必要があります。 検索ネットワークとオーディエンスネットワークのショッピングキャンペーンで動的リマーケティングリストを使用してオーディエンスを製品広告でリターゲティングしたり、検索キャンペーンでテキスト広告と動的検索広告でオーディエンスをリターゲティングしたりします。<!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動的リマーケティングオーディエンスターゲットの入札修飾子は、「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定のポートフォリオでは最適化されません。

>[!NOTE]
>
>検索、ソーシャル、Commerceには、アップロードした顧客データや、[!DNL Google Ads] ーザーまたは [!DNL Microsoft Advertising] オーディエンスの作成または編集に使用された [!DNL Adobe] セグメントの顧客データは格納されません。

>[!MORELIKETHIS]
>
>* [ オーディエ  [!DNL Google Ads]  スからの顧客一致オーディエ  [!DNL Adobe]  スの作成 ](google-audience-from-adobe-audience.md)
>* [Adobe Campaign [!DNL Google Ads]  メールリストからカスタマーマッチオーディエンスを作成 ](google-audience-from-campaign-email-list.md)
>* [ 顧客データリストを使用したカスタマーマッチオーディエンスの管理 ](audience-from-customer-data-list.md)
>* [ 動的リマーケティングオーディエンスの管理 ](audience-dynamic-remarketing-manage.md)
>* [ キャンペーンおよび広告グループのオーディエンスターゲットの管理 ](audience-targets-manage.md)
>* [ キャンペーンおよび広告グループのオーディエンス除外の管理 ](audience-exclusions-manage.md)
