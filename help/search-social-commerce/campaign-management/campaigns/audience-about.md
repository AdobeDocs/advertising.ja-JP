---
title: オーディエンスについて
description: '[!DNL Google Ads]および[!DNL Microsoft Advertising]個のオーディエンスを追跡、作成、管理するオプションについて説明します。'
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
TQID: 'https://experienceleague.adobe.com/B77S28vEpSkrgNmhc-Ekn7PXh3W-y2g9et2y3gCQPK8'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 0%
---
# Search, Social, &amp; Commerceでの[!DNL Google Ads]および[!DNL Microsoft Advertising] オーディエンスの管理について

*[!DNL Google Ads]と[!DNL Microsoft Advertising]のみ*

オーディエンスライブラリには、[!DNL Google Ads]の顧客データベース、市場内、類似オーディエンスおよび[!DNL Microsoft Advertising]のリマーケティングと動的リマーケティング、カスタム、顧客照合、市場内、類似オーディエンスがすべて一覧表示されます。 [!DNL Google Ads]個のオーディエンスのいずれかを[!DNL Google Ads]個のキャンペーンレベルおよび広告グループレベルのターゲットおよび除外として使用できます。また、[!DNL Microsoft Advertising]個のオーディエンスのいずれかを[!DNL Microsoft Advertising]個のキャンペーンレベルおよび広告グループレベルのターゲットおよび（動的リマーケティングオーディエンスのみ）除外として使用できます。 任意のオーディエンスターゲットに対して入札調整を追加または編集できます。

また、既存のAdobe CX Enterpriseオーディエンスのセグメントやメールリストを活用したり、CRM （顧客関係管理）システムの様々な顧客データを利用して、オーディエンスを構築および管理することもできます。

* オプトインしたAdobe Audience ManagerまたはAdobe Analytics アカウントを持つ&#x200B;**Adobe オーディエンスセグメント：**&#x200B;の広告主は、次の[!DNL Adobe] セグメントから[!DNL Google Ads]のカスタマーマッチオーディエンスを作成できます。

  * （Audience Managerを持っていない[!DNL Analytics]人のアカウントを持つ広告主）Adobe CX Enterpriseと共有されている[!DNL Analytics] セグメントのユーザーIDを使用して、[!DNL Google Ads]人の顧客マッチオーディエンスを作成できます。

  * （Audience Manager アカウントを持つ広告主）検索、ソーシャル、およびCommerceを宛先とするAudience Manager セグメントのユーザーIDを使用して、[!DNL Google Ads]人のカスタマーマッチオーディエンスを作成できます。 これには、Adobe CX Enterpriseに公開されるAdobe Analytics セグメントや、Adobe CX Enterprise Audience Libraryを使用して作成されたセグメントが含まれます。

  顧客一致オーディエンスを作成するには、広告主の[!DNL Google Ads] アカウントが[&#x200B; カスタムマッチ &#x200B;](https://support.google.com/adspolicy/answer/6299717)の対象となり、[&#x200B; ユーザーID セグメント &#x200B;](https://support.google.com/google-ads/answer/9199250)に対してオプトインしている必要があります。 また、検索、ソーシャル、およびCommerceの広告主アカウントは、カスタマーマッチオーディエンスの作成を許可するように設定する必要があります。

  顧客データベースのオーディエンスの[!DNL Adobe]個のセグメントデータとcookie同期ファイルは、毎日[!DNL Google Ads]個に同期されます。

* **Adobe Campaignのメールリスト：** Adobe アカウントチームは、[!DNL Campaign]内のメールリストから[!DNL Google Ads]のカスタマーマッチオーディエンスを作成および更新するワークフローを設定できます。

* **顧客データリスト：**&#x200B;顧客マッチの対象となる[!DNL Google Ads]または[!DNL Microsoft Advertising] アカウントを持つ広告主は、少なくとも&lt;ph=&#39;266&#39;/>?—>の場合、顧客データベースのオーディエンスに含まれる広告ネットワーク固有の顧客データベースのオーディエンス &lt;! – または動的リマーケティングオーディエンスを作成および更新できます。プライマリ識別子を含むCSV ファイルをアップロードします。[!DNL Google Ads]

* **動的リマーケティングリスト：** [!DNL Microsoft Advertising] アカウントを持つ広告主は、動的リマーケティングオーディエンスを作成および管理できます。このオーディエンスを使用すると、複数の方法（製品ビューアーや過去の購入者など）で製品と最近接触した潜在顧客をリターゲティングできます。 動的なリマーケティングオーディエンスを活用するには、web ページで広告ネットワークのJavaScriptコンバージョンタグとオーディエンストラッキングタグを使用する必要があります。 検索連動型リマーケティングリストを使用して、検索連動型およびオーディエンスネットワーク上のショッピングキャンペーンを使用して、商品広告でオーディエンスをリターゲティングします。また、検索連動型キャンペーンを使用して、テキスト広告や動的検索広告でオーディエンスをリターゲティングします。<!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動的リマーケティングオーディエンスターゲットの入札修飾子が、「[!UICONTROL Auto-optimize Bid Adjustment Values]」設定のポートフォリオで最適化されていません。

>[!NOTE]
>
>Search, Social, &amp; Commerceには、[!DNL Google Ads]または[!DNL Microsoft Advertising]のオーディエンスの作成または編集に使用した[!DNL Adobe] セグメントからアップロードした顧客データは保存されません。

>[!MORELIKETHIS]
>
>* [顧客マッチオーディエンスを [!DNL Adobe]  オーディエンス &#x200B;](google-audience-from-adobe-audience.md)から [!DNL Google Ads] 作成
>* [Adobe Campaignのメールリストから [!DNL Google Ads] 顧客マッチオーディエンスを作成](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
>* [&#x200B; キャンペーンと広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
>* [&#x200B; キャンペーンと広告グループのオーディエンス除外の管理](audience-exclusions-manage.md)
