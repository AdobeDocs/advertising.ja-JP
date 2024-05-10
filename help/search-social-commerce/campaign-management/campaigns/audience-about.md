---
title: オーディエンスについて
description: 追跡、作成、管理するオプションについて説明します [!DNL Google Ads] および [!DNL Microsoft Advertising] オーディエンス。
exl-id: f85cbc82-ddbc-4ecd-a17b-b4cb4808cfbc
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# の管理について [!DNL Google Ads] および [!DNL Microsoft Advertising] 検索、ソーシャル、Commerceのオーディエンス

*[!DNL Google Ads]および [!DNL Microsoft Advertising] のみ*

Audiences ライブラリには、以下のすべてに関する情報が表示されます [!DNL Google Ads] 顧客データベース、市場内、および類似のオーディエンスと [!DNL Microsoft Advertising] リマーケティング、動的リマーケティング、カスタム、顧客一致、市場内などのオーディエンス。 以下のいずれかを使用できます [!DNL Google Ads] オーディエンスの種類 [!DNL Google Ads] キャンペーンレベルおよび広告グループレベルのターゲットと除外。次のいずれかを使用できます [!DNL Microsoft Advertising] オーディエンスの種類 [!DNL Microsoft Advertising] キャンペーンレベルおよび広告グループレベルのターゲットと（動的リマーケティングオーディエンスのみ）除外。 任意のオーディエンスターゲットの入札調整を追加または編集できます。

また、既存のAdobe Experience Cloud オーディエンスのセグメントや電子メールリスト、および顧客関係管理（CRM）システムの様々な種類の顧客データを使用して、オーディエンスを作成および管理することもできます。

* **Adobeオーディエンスセグメント：** オプトインのAdobe Audience ManagerまたはAdobe Analytics アカウントを持つ広告主は、 [!DNL Google Ads] のカスタマーマッチオーディエンス [!DNL Adobe] セグメント :

   * （広告主 [!DNL Analytics] Audience Managerを持っていないアカウント）を作成できます [!DNL Google Ads] のユーザー ID を使用したカスタマーマッチオーディエンス [!DNL Analytics] Adobe Experience Cloudと共有されるセグメント。

   * （Audience Managerアカウントを持つ広告主）以下を作成できます [!DNL Google Ads] 検索、ソーシャル、Commerceを宛先として持つAudience Managerセグメントのユーザー ID を使用して、オーディエンスをカスタマーマッチさせます。 これには、Adobe Experience Cloudに公開されるAdobe Analytics セグメントや、Adobe Experience Cloud オーディエンスライブラリを使用して作成されたセグメントが含まれる場合があります。

  顧客一致オーディエンスを作成する場合、広告主のは [!DNL Google Ads] アカウントは [カスタム一致の対象](https://support.google.com/adspolicy/answer/6299717) で以下をオプトイン [ユーザー ID セグメント](https://support.google.com/google-ads/answer/9199250). また、検索、ソーシャル、Commerceの広告主アカウントも、カスタマーマッチオーディエンスを作成できるように設定する必要があります。

  [!DNL Adobe] 顧客データベースのオーディエンスのセグメントデータと cookie 同期ファイルは、に同期されます [!DNL Google Ads] 毎日。

* **Adobe Campaignのメールリスト：** Adobeアカウントチームは、を作成および更新するワークフローの設定を支援します [!DNL Google Ads] 内のメールリストからの顧客一致オーディエンス [!DNL Campaign].

* **顧客データリスト：** を使用した広告主 [!DNL Google Ads] または [!DNL Microsoft Advertising] カスタマーマッチの対象となるアカウントは、広告ネットワーク固有の顧客データベースのオーディエンスを作成および更新できます &lt;!>顧客データベースのオーディエンスに含まれる、または動的リマーケティングオーディエンス。少なくとも以下に該当： [!DNL Google Ads]プライマリ識別子を含む CSV ファイルをアップロードする

* **動的リマーケティングリスト：** を使用した広告主 [!DNL Microsoft Advertising] アカウントは、動的リマーケティングオーディエンスを作成および管理できます。このオーディエンスを使用すれば、複数の方法（製品ビューアや過去の購入者など）のいずれかで製品を最近操作した潜在的な顧客をリターゲティングできます。 動的リマーケティングオーディエンスでは、web ページで広告ネットワークの JavaScript コンバージョンおよびオーディエンストラッキングタグを使用する必要があります。 検索ネットワークとオーディエンスネットワークのショッピングキャンペーンで動的リマーケティングリストを使用してオーディエンスを製品広告でリターゲティングしたり、検索キャンペーンでテキスト広告と動的検索広告でオーディエンスをリターゲティングしたりします。 <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動的リマーケティングオーディエンスターゲットの入札修飾子が、のポートフォリオで最適化されない[!UICONTROL Auto-optimize Bid Adjustment Values]」設定です。

>[!NOTE]
>
>検索、ソーシャル、Commerceには、アップロードまたはアップロード元の顧客データは格納されません [!DNL Adobe] の作成または編集に使用するセグメント [!DNL Google Ads] または [!DNL Microsoft Advertising] オーディエンス。

>[!MORELIKETHIS]
>
>* [作成 [!DNL Google Ads] のカスタマーマッチオーディエンス [!DNL Adobe] オーディエンス](google-audience-from-adobe-audience.md)
>* [を作成 [!DNL Google Ads] Adobe Campaign メールリストからのカスタマーマッチオーディエンス](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用したカスタマーマッチオーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
>* [キャンペーンおよび広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
>* [キャンペーンおよび広告グループのオーディエンス除外の管理](audience-exclusions-manage.md)
