---
title: Audience Sourceの設定
description: オーディエンスソースの設定について説明します。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# Audience Sourceの設定

*Beta機能*

**[!UICONTROL Data Visibility Level]:** アカウント（*[!UICONTROL Advertiser]*）にアクセスできる単一の広告主に対してセグメントを使用できるか、アカウント *[!UICONTROL Account]* にアクセスできるすべての広告主に対してセグメントを使用できるか。

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ）セグメントを使用できる広告主。 アカウントにアクセスできる広告主のリストから 1 つ選択します。

**[!UICONTROL Enter IMS Org Id]:** （[!DNL Real-Time CDP] ソースのみ） [!DNL Adobe Experience Platform] アカウントのAdobe Experience Cloud組織 ID。

**[!UICONTROL Convert PII to the following IDs]:** 個人情報（PII）の変換先の ID タイプ。 複数のタイプを選択した場合、生成されたセグメントには、選択した各 ID タイプの値（メールアドレスごとの [!DNL RampID] や [!DNL Unified ID2.0] など）が入力されます。 データ料金はそれに応じて適用されます。

[!DNL RampID] と [!DNL Unified ID2.0] については、ベンダーは各メールアドレスを検索して ID が既に存在するかどうかを確認し、可能な場合はアドレスを一致する ID に変換します。 アドレスの ID が存在しない場合は、新しい ID が作成されます。

>[!NOTE]
>
>1 つのプレースメントでターゲットにできる ID のタイプは 1 つだけです。 ID タイプでパフォーマンスをテストするには、セグメント内の ID タイプごとに [&#x200B; 個別のプレースメントを作成 &#x200B;](/help/dsp/campaign-management/placements/placement-create.md) します。

* *[!DNL RampID]:* PII を [!DNL RampID] に変換します。 [!DNL RampIDs] は、ログインユーザーのリターゲティングや [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 測定に使用できます。

* *[!DNL Unified ID2.0]（Beta）:* ログインユーザーをリターゲティングするために、PII を [&#x200B; 統合 ID 2.0](https://unifiedid.com) ID に変換する

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** PII をユニバーサル ID に変換するためのサービス契約の条件。 データを新しい ID タイプに変換するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、「**>**」をクリックします。 条件に同意するには、条件の下部までスクロールし、「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Source Key]:** （読み取り専用、自動生成）オーディエンスをAdvertising DSPにプッシュするカスタマーデータプラットフォームで宛先接続を作成する際に使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定またはファイルに貼り付けることができます。

>[!MORELIKETHIS]
>
>* [&#x200B; ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 &#x200B;](source-manage.md)
>* [&#x200B; ファーストパーティオーディエンスソースについて &#x200B;](source-about.md)
>* [&#x200B; 認証済みセグメントの手動インポート  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP接続 &#x200B;](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=ja)
>* [Audience Management について &#x200B;](/help/dsp/audiences/audience-about.md)
