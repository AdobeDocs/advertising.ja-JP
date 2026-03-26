---
title: オーディエンスソースを管理して、ユニバーサル ID オーディエンスをアクティブ化する
description: ソースを作成および管理して、顧客データプラットフォームからオーディエンスをインポートし、ユニバーサル IDを含むセグメントに変換する方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# オーディエンスソースを管理して、ユニバーサル ID オーディエンスをアクティブ化する

*Beta機能*

Adobe DSPで、Customer Data Platformの各ファーストパーティオーディエンス用のソースを作成します。このソースを、指定したユニバーサル ID タイプを含むセグメントに変換します。 セグメントは、組織のDSP アカウントまたは広告主アカウントにインポートできます。 選択したユニバーサル ID タイプに基づいて、データ料金が適用されます。 ソースを作成したら、各顧客データプラットフォームからオーディエンスを取り込むために、さらに手順を追加する必要があります。 ソースを作成するには、手順の最後にあるメモを参照してください。

後で、ソースオーディエンスが翻訳されるユニバーサル ID タイプを変更し、変更のログを表示できます。

ソースを削除することもできます。

## オーディエンスソースの作成

<!--
 Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**&#x200B;をクリックします。

1. **[!UICONTROL Add Source]**&#x200B;をクリックします。

1. [!UICONTROL Select a Type] メニューで、[顧客データプラットフォーム ](source-about.md)を選択します。

   * *[!UICONTROL RT-CDP]*: [!DNL Adobe Real-Time CDP]。

   * *[!UICONTROL ActionIQ]*: [!DNL ActionIQ]顧客データプラットフォーム。

   * *[!UICONTROL Amperity]*: [!DNL Amperity]顧客データプラットフォーム。

   * *[!UICONTROL Optimizely]*: [!DNL Optimizely]顧客データプラットフォーム。

   * *[!UICONTROL Tealium CDP]*: （設定されたユーザーのみ）顧客データプラットフォーム [!DNL Tealium]。

1. [!UICONTROL Data Visibility Level]を指定します：*[!UICONTROL Advertiser]*&#x200B;または&#x200B;*[!UICONTROL Account]*。

1. 残りの[ ソース設定](#source-settings)を入力します。

   生成された[!UICONTROL Source Key]のコピーを保持します。 後で値が必要になります。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

>[!NOTE]
>
>顧客データプラットフォームのソースを作成したら、オーディエンスをインポートするためのさらなる手順を完了する必要があります。 [の [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md) ワークフロー、<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), -->、[の [!DNL Amperity]](source-amperity.md) ワークフロー、[の [!DNL Optimizely]](source-optimizely.md) ワークフロー、[の [!DNL Tealium]](source-tealium.md) ワークフローを参照してください。

## オーディエンスソースのID タイプの変更

<!-- Clarify this:

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses that you shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we don't delete any historical IDs of that type from the segments shared through the source.

-->

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**&#x200B;をクリックします。

1. ソース行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. ソース [に対して選択した](#source-settings)IDを変更します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## オーディエンスソースの削除

ソースを削除すると、ソースを介して翻訳されたセグメントが削除されます。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**&#x200B;をクリックします。

1. ソース行の上にカーソルを置き、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## オーディエンスソースの変更ログの表示

オーディエンスソースレコードの変更に関する詳細を表示したり、オプションでログにメモを添付したりできます。

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL Sources]**&#x200B;をクリックします。

1. ソース行の上にカーソルを置き、**[!UICONTROL Change log]**&#x200B;をクリックします。

1. （オプション）変更ログにメモを添付するには、次の手順を実行します。

   1. ソース行の上にカーソルを置き、**[!UICONTROL Add Notes]**&#x200B;をクリックします。

   1. メモを入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

      最大長は256文字です。

1. （オプション）より大きな詳細画面でログを開くには、ソース行の上にカーソルを置いて「**[!UICONTROL View Details]**」をクリックします。

## オーディエンスソースの設定 {#source-settings}

**[!UICONTROL Data Visibility Level]:** アカウント （*[!UICONTROL Advertiser]*）へのアクセス権を持つ単一の広告主またはアカウント *[!UICONTROL Account]*&#x200B;へのアクセス権を持つすべての広告主がセグメントを利用できるかどうか。

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ） セグメントを利用できる広告主。 アカウントへのアクセス権を持つ広告主のリストから1つを選択します。

**[!UICONTROL Enter IMS Org Id]:** （[!DNL Real-Time CDP] ソースのみ） [!DNL Adobe Experience Platform] アカウントのAdobe Experience Cloud組織ID。

**[!UICONTROL Convert PII to the following IDs]:**&#x200B;個人を特定できる情報（PII）を変換するID タイプ。 複数のタイプを選択した場合、生成されたセグメントには、選択した各ID タイプの値が入力されます（例えば、メールアドレスごとに[!DNL RampID]と[!DNL Unified ID2.0]）。 データ料金はそれに応じて適用されます。

[!DNL RampID]と[!DNL Unified ID2.0]の場合、ベンダーは各メールアドレスを検索して、IDが既に存在するかどうかを確認し、使用可能な場合はアドレスを一致するIDに変換します。 アドレスにIDが存在しない場合、新しいIDが作成されます。

>[!NOTE]
>
>1つのプレースメントでターゲットできるIDのタイプは1つだけです。 ID タイプ別にパフォーマンスをテストするには、[ セグメント内のID タイプごとに個別のプレースメント ](/help/dsp/campaign-management/placements/placement-create.md)を作成します。

* *[!DNL RampID]:* PIIを[!DNL RampID]に変換します。 ログインユーザーのリターゲティングと[!DNL RampIDs]の測定には、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を使用できます。

* *[!DNL Unified ID2.0]（Beta）:* ログイン ユーザーのリターゲティング用にPIIを[Unified ID 2.0](https://unifiedid.com) IDに変換するには、次の手順を実行します。

<!--
 Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** PIIをユニバーサル IDに変換するための利用条件。 お客様またはDSP アカウント内の他のユーザーは、データを新しいID タイプに変換する前に、条件に1回同意する必要があります。 マネージドサービス契約を締結しているお客様には、Adobeアカウントチームが同意を得て、組織の代わりに条件に同意します。 条件を読むには、**>**&#x200B;をクリックします。 条件に同意するには、条件の一番下までスクロールして「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Source Key]:** （読み取り専用；自動生成） Customer Data Platformで宛先接続を作成してオーディエンスをAdvertising DSPにプッシュするために使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定またはファイルにペーストできます。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](source-about.md)
>* [ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ ユーザーIDを [!DNL Adobe Real-Time CDP] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [ ユーザーIDを [!DNL Amperity] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-amperity.md)
>* [ ユーザーIDを [!DNL Optimizely] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-optimizely.md)
>* [ ユーザーIDを [!DNL Tealium] からユニバーサル IDに変換](/help/dsp/audiences/sources/source-tealium.md)
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
