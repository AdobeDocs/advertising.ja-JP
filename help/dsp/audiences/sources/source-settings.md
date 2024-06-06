---
title: オーディエンスソース設定
description: オーディエンスソースの設定について説明します。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '357'
ht-degree: 0%

---

# オーディエンスソース設定

*ベータ版機能*

**[!UICONTROL Data Visibility Level]:** アカウントへのアクセス権を持つ単一の広告主がセグメントを使用できるかどうか（*[!UICONTROL Advertiser]*）または、アカウントにアクセスできるすべての広告主に送信します。 *[!UICONTROL Account]*.

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ）セグメントを利用できる広告主。 アカウントにアクセスできる広告主のリストから 1 つ選択します。

**[!UICONTROL Enter IMS Org Id]:** （[!DNL Real-Time CDP] （ソースのみ）のAdobe Experience Cloud組織 ID [!DNL Adobe Experience Platform] アカウント。

**[!UICONTROL Convert PII to the following IDs]:** 個人情報（PII）の変換先の ID タイプ。 複数のタイプを選択した場合、生成されたセグメントには、選択した各 ID タイプの値（など）が入力されます。 [!DNL RampID] および [!DNL Unified ID2.0] （メールアドレスごとに）。 データ料金はそれに応じて適用されます。

の場合 [!DNL RampID] および [!DNL Unified ID2.0]を使用すると、ベンダーは各メールアドレスを検索して ID が既に存在するかどうかを確認し、可能な場合はアドレスを一致する ID に変換します。 アドレスの ID が存在しない場合は、新しい ID が作成されます。

>[!NOTE]
>
>1 つのプレースメントでターゲットにできる ID のタイプは 1 つだけです。 ID タイプでパフォーマンスをテストするには、次の手順に従います。 [別のプレースメントの作成](/help/dsp/campaign-management/placements/placement-create.md) （セグメントの各 ID タイプ）。

* *[!DNL RampID]:* PII をに変換するには [!DNL RampID]. 次を使用できます [!DNL RampIDs] リターゲティング：ログインユーザーおよびの [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 測定。

* *[!DNL Unified ID2.0]（ベータ版）:* PII をに変換するには [統合 ID 2.0](https://unifiedid.com) ログインユーザーをリターゲティングするための ID。

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** PII をユニバーサル ID に変換するためのサービス契約の条件。 データを新しい ID タイプに変換するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、 **>**. 条件に同意するには、条件の下部までスクロールし、をクリックします **[!UICONTROL Accept]**.

**[!UICONTROL Source Key]:** （読み取り専用、自動生成）オーディエンスを Advertising DSPにプッシュするカスタマーデータプラットフォームで宛先接続を作成する際に使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定またはファイルに貼り付けることができます。

>[!MORELIKETHIS]
>
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [ファーストパーティオーディエンスソースについて](source-about.md)
>* [認証済みセグメントの手動インポート： [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
