---
title: オーディエンスについて
description: トラッキング、作成、管理のオプションについて説明します [!DNL Google Ads] および [!DNL Microsoft® Advertising] オーディエンス。
exl-id: 34169650-9820-4b7d-9ae6-09ff8a8c6f2e
feature: Search Campaign Management
source-git-commit: 9f30518efbbe29f976298fe1fcd962182285679f
workflow-type: tm+mt
source-wordcount: '534'
ht-degree: 0%

---

# 管理について [!DNL Google Ads] および [!DNL Microsoft® Advertising] 検索、ソーシャル、コマースのオーディエンス

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] のみ*

オーディエンスライブラリには、 [!DNL Google Ads] 顧客データベースの、市場での、同様のオーディエンスと [!DNL Microsoft® Advertising] リマーケティングおよび動的リマーケティング、カスタム、顧客一致、市場内、同様のオーディエンス。 任意の [!DNL Google Ads] オーディエンス： [!DNL Google Ads] キャンペーンレベルおよび広告グループレベルのターゲットと除外。 [!DNL Microsoft® Advertising] オーディエンス： [!DNL Microsoft® Advertising] キャンペーンレベルおよび広告グループレベルのターゲットおよび（動的リマーケティングオーディエンスのみ）除外に含めることができます。 任意のオーディエンスターゲットの入札調整を追加または編集できます。

また、既存のAdobe Experience Cloudオーディエンスのセグメントや電子メールリストを使用し、顧客関係管理 (CRM) システムの様々な種類の顧客データから、オーディエンスを作成および管理することもできます。

* **Adobeオーディエンスセグメント：** オプトインしたAdobe Audience ManagerまたはAdobe Analyticsアカウントを持つ広告主は、 [!DNL Google Ads] 顧客と一致するオーディエンス [!DNL Adobe] セグメント：

   * ( [!DNL Analytics] Audience Managerも持たないアカウント ) [!DNL Google Ads] のユーザー ID を使用してオーディエンスに一致させる [!DNL Analytics] Adobe Experience Cloudと共有されるセグメント。

   * (Audience Managerアカウントを持つ広告主 ) [!DNL Google Ads] 顧客は、検索、ソーシャル、コマースを宛先とするAudience Managerセグメントのユーザー ID を使用して、オーディエンスを照合します。 これには、Adobe Experience Cloudに公開されるAdobe Analyticsセグメントや、Adobe Experience Cloudオーディエンスライブラリを使用して作成されたセグメントが含まれる場合があります。

  顧客一致オーディエンスを作成するには、 [!DNL Google Ads] アカウントは次の条件を満たす必要があります [カスタムマッチの条件を満たす](https://support.google.com/adspolicy/answer/6299717) をオプトインし、 [ユーザー ID セグメント](https://support.google.com/google-ads/answer/9199250). また、検索、ソーシャル、コマースの広告主アカウントは、顧客一致のオーディエンスを作成できるように設定する必要があります。

  [!DNL Adobe] 顧客データベースのオーディエンスのセグメントデータと cookie 同期ファイルは、 [!DNL Google Ads] 毎日。

* **Adobe Campaign E メールリスト：** Adobeアカウントチームが、 [!DNL Google Ads] 内の電子メールリストからの顧客一致オーディエンス [!DNL Campaign].

* **顧客データリスト：** 次を持つ広告主 [!DNL Google Ads] または [!DNL Microsoft® Advertising] カスタマーマッチを利用できるアカウントは、広告ネットワーク固有の顧客データベースのオーディエンスを作成および更新できます &lt;!> — または動的リマーケティングオーディエンス — 少なくともの場合は、顧客データベースのオーディエンスに含まれます。 [!DNL Google Ads]?—> プライマリ ID を持つ CSV ファイルをアップロードする。

* **動的リマーケティングリスト：** 次を持つ広告主 [!DNL Microsoft® Advertising] アカウントでは、動的なリマーケティングオーディエンスを作成および管理できます。これを使用して、最近製品でやり取りした見込み客（製品閲覧者や過去の購入者など）を複数の方法でリターゲティングできます。 動的リマーケティングオーディエンスでは、Web ページで広告ネットワークの JavaScript コンバージョンタグとオーディエンストラッキングタグを使用する必要があります。 動的リマーケティングリストを検索およびオーディエンスネットワーク上のショッピングキャンペーンと共に使用して、製品広告でオーディエンスをリターゲティングし、検索キャンペーンと共にテキスト広告と動的検索広告でオーディエンスをリターゲティングします。 <!--[For [!DNL Google Ads], these are technically included in a customer data-based audience, so word this all carefully when we add support for them.]-->

  >[!NOTE]
  >
  >動的リマーケティングオーディエンスターゲットの入札修飾子が、「[!UICONTROL Auto-optimize Bid Adjustment Values]&quot;設定中です。

>[!NOTE]
>
>Search、Social、および Commerce では、アップロードした顧客データや [!DNL Adobe] 作成または編集に使用されるセグメント [!DNL Google Ads] または [!DNL Microsoft® Advertising] オーディエンス。

>[!MORELIKETHIS]
>
>* [作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](google-audience-from-adobe-audience.md)
>* [の作成 [!DNL Google Ads] Adobe Campaign電子メールリストからの顧客一致オーディエンス](google-audience-from-campaign-email-list.md)
>* [顧客データリストを使用した顧客一致オーディエンスの管理](audience-from-customer-data-list.md)
>* [動的リマーケティングオーディエンスの管理](audience-dynamic-remarketing-manage.md)
>* [キャンペーンおよび広告グループのオーディエンスターゲットの管理](audience-targets-manage.md)
>* [キャンペーンおよび広告グループのオーディエンスの除外の管理](audience-exclusions-manage.md)
