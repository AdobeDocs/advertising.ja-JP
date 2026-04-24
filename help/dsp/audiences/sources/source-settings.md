---
title: オーディエンスソースの設定
description: オーディエンスソースの設定について説明します。
feature: DSP Audiences
exl-id: 274ea502-ad15-4d3d-922a-17caddb87f69
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: '374'
ht-degree: 0%

---

# オーディエンスソースの設定

*Beta機能*

**[!UICONTROL Data Visibility Level]:** アカウント （*[!UICONTROL Advertiser]*）へのアクセス権を持つ単一の広告主またはアカウント *[!UICONTROL Account]*&#x200B;へのアクセス権を持つすべての広告主がセグメントを利用できるかどうか。

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ） セグメントを利用できる広告主。 アカウントへのアクセス権を持つ広告主のリストから1つを選択します。

**[!UICONTROL Enter IMS Org Id]:** （[!DNL Real-Time CDP] ソースのみ） [!DNL Adobe Experience Platform] アカウントのAdobe CX Enterprise組織ID。

**[!UICONTROL Convert PII to the following IDs]:**&#x200B;個人を特定できる情報（PII）を変換するID タイプ。 複数のタイプを選択した場合、生成されたセグメントには、選択した各ID タイプの値が入力されます（例えば、メールアドレスごとに[!DNL RampID]と[!DNL Unified ID2.0]）。 データ料金はそれに応じて適用されます。

[!DNL RampID]と[!DNL Unified ID2.0]の場合、ベンダーは各メールアドレスを検索して、IDが既に存在するかどうかを確認し、使用可能な場合はアドレスを一致するIDに変換します。 アドレスにIDが存在しない場合、新しいIDが作成されます。

>[!NOTE]
>
>1つのプレースメントでターゲットできるIDのタイプは1つだけです。 ID タイプ別にパフォーマンスをテストするには、[&#x200B; セグメント内のID タイプごとに個別のプレースメント &#x200B;](/help/dsp/campaign-management/placements/placement-create.md)を作成します。

* *[!DNL RampID]:* PIIを[!DNL RampID]に変換します。 ログインユーザーのリターゲティングと[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)の測定には、[!DNL RampIDs]を使用できます。

* *[!DNL Unified ID2.0]（Beta）:* ログイン ユーザーのリターゲティング用にPIIを[Unified ID 2.0](https://unifiedid.com) IDに変換するには、次の手順を実行します。

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** PIIをユニバーサル IDに変換するための利用条件。 お客様またはDSP アカウント内の他のユーザーは、データを新しいID タイプに変換する前に、条件に1回同意する必要があります。 マネージドサービス契約を締結しているお客様には、Adobeアカウントチームが同意を得て、組織の代わりに条件に同意します。 条件を読むには、**>**&#x200B;をクリックします。 条件に同意するには、条件の一番下までスクロールして「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Source Key]:** （読み取り専用；自動生成） Customer Data Platformで宛先接続を作成してオーディエンスをAdvertising DSPにプッシュするために使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定またはファイルにペーストできます。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [&#x200B; ファーストパーティのオーディエンスソースについて](source-about.md)
>* [認証済みセグメントを [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)から手動でインポートします
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html?lang=ja)
>* [&#x200B; オーディエンス管理について](/help/dsp/audiences/audience-about.md)
