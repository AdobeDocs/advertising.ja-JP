---
title: Adobe AnalyticsとのAdobe Advertising統合
description: Adobe AdvertisingがAdobe Analyticsとデータを交換する方法、および検索、ソーシャル、コマース内でのデータの使用方法について説明します。
feature: Integration with Adobe Analytics
exl-id: 5b0ecb82-fb5c-48c5-a599-15b548f59461
source-git-commit: 78f69587771d9e72eb137f1e0866d782ed5c4d01
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# Adobe AnalyticsとのAdobe Advertising統合

次の方法でAdobe Advertisingを Analytics と統合できます。

## 次の間でデータを交換 [!DNL Analytics] およびAdobe Advertising

### プル [!DNL Analytics] データからAdobe Advertisingへ

を使用 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md),[!DNL Search, Social, & Commerce] とDSPのプルイン：

* **[!DNL Analytics]セグメント：**  で作成されたすべての広告主または代理店のセグメントのメタデータ、階層データ、一意のオーディエンスデータ [!DNL Analytics] Experience Cloudに公開

* **[!DNL Analytics]サイトエンゲージメント指標**

* **[!DNL Analytics]標準、カスタム、予約済みの指標**

### にAdobe Advertisingデータを送信 [!DNL Analytics]

* **Adobe Advertisingからのトラフィック指標**

* **Dimension元Adobe Advertising**

>[!NOTE]
>
>の場合 [!DNL Search, Social, & Commerce]の場合、この機能は、ほとんどの広告ネットワークとキャンペーンタイプでサポートされます。 詳しくは、 [!DNL Search, Social, & Commerce] ガイドを参照してください。<!-- add link when that's published in ExL -->

### 用途 [!DNL Analytics] 作成するセグメント [!DNL Google Ads Audiences] {#audience-manager-google-audiences}

*次を使用してオプトインした広告主 [!DNL Advertising Search, Social, & Commerce] のみ*

<!-- Verify all -->

Within [!DNL Search, Social, & Commerce]を使用する場合、 [!DNL Google Ads] 既存のを使用して、Googleの顧客一致オーディエンスをユーザー ID から取得 [!DNL Analytics] セグメント。 これには、Adobe Experience Cloudに公開されたAdobe Analyticsセグメントや、Adobe Experience Cloudを使用して作成されたセグメントが含まれます [!DNL Audience Library]. 詳しくは、[作成 [!DNL Google Ads] 次のオーディエンスをカスタマーマッチさせる [!DNL Adobe] audiences](/help/search-social-commerce/campaign-management/campaigns/google-audience-from-adobe-audience.md).&quot;

[ユーザー ID からの顧客一致オーディエンス](https://support.google.com/google-ads/answer/9199250) は web サイトのタグベースのオーディエンスと同様に機能しますが、一意のオーディエンスメンバーには、標準の顧客一致や web サイトのタグベースのオーディエンスよりも明確なメリットを得るために、PII 以外の ID が割り当てられます。

必要なユーザー ID を作成するには、 JavaScript タグを使用するAdobe Advertisingが必要です <!-- with a user ID parameter -->を Web サイト上でクリックします。 詳しくは、Adobeアカウントチームにお問い合わせください。

![セグメント作成プロセス](/help/integrations/assets/ad_search_user_id_pic.png)

オーディエンスを作成したら、 [!DNL Google Ads] キャンペーンとして [キャンペーンレベルまたは広告グループレベルのターゲットまたは除外](#audience-manager-targets).

### 用途 [!DNL Analytics] 広告のターゲットにする、または広告を除外するセグメント {#analytics-targets}

* ( 次を持つオプトイン広告主 [!DNL Search, Social, & Commerce]) 任意の [!DNL Google Ads] オーディエンス： [次を使用して作成 [!DNL Analytics] セグメント](#audience-manager-google-audiences) キャンペーンレベルまたは広告グループレベルのターゲットまたは除外として [!DNL Google Ads] キャンペーン。

* (DSPの広告主 ) 既存の [!DNL Analytics] セグメントを、広告プレースメントのターゲットとして使用します。 オプションで、セグメントを再利用可能なオーディエンスに含めることができます。このオーディエンスは、複数の配置のターゲットまたは除外として使用できます。

* (Advertising Creativeを持つ広告主 ) 既存の [!DNL Analytics] セグメントを、広告エクスペリエンスの特定のクリエイティブのターゲットとして使用します。
