---
title: オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化
description: ソースを作成および管理して、顧客データプラットフォームからオーディエンスを読み込み、ユニバーサル ID を含むセグメントに変換する方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: e9ce180e302f619c85a3d6db813c83903e437d04
workflow-type: tm+mt
source-wordcount: '758'
ht-degree: 0%

---

# オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化

*Beta機能*

DSPで、顧客データプラットフォーム内のファーストパーティオーディエンスごとに、指定したユニバーサル ID タイプを含むセグメントに変換するソースを作成します。 セグメントは、組織のDSP アカウントまたは広告主アカウントに読み込むことができます。 データ料金は、選択したユニバーサル ID タイプに基づいて適用されます。 ソースを作成したら、各顧客データプラットフォームからオーディエンスを取り込むために、追加の手順が必要です。 ソースを作成するには、この手順の最後にあるメモを参照してください。

後でソースオーディエンスの翻訳先のユニバーサル ID タイプを変更し、変更のログを確認できます。

ソースを削除することもできます。

## オーディエンス Sourceの作成

<!-- Not sure about this

You can create one source for each combination of universal ID partner and data visibility level.

-->

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL Sources]** をクリックします。

1. 「**[!UICONTROL Add Source]**」をクリックします。

1. [!UICONTROL Select a Type] メニューで、[ 顧客データプラットフォーム ](source-about.md) を選択します。

   * *[!UICONTROL RT-CDP]*:[!DNL Adobe Real-Time CDP]。

   * *[!UICONTROL ActionIQ]*:[!DNL ActionIQ] 顧客データプラットフォーム。

   * *[!UICONTROL Amperity]*:[!DNL Amperity] 顧客データプラットフォーム。

   * *[!UICONTROL Optimizely]*:[!DNL Optimizely] 顧客データプラットフォーム。

   * *[!UICONTROL Tealium CDP]*: （設定されたユーザーのみ） [!DNL Tealium] 顧客データプラットフォーム。

1. *[!UICONTROL Advertiser]* または *[!UICONTROL Account]* の [!UICONTROL Data Visibility Level] を指定します。

1. 残りの [ ソース設定 ](#source-settings) を入力します。

   生成された [!UICONTROL Source Key] のコピーを保持します。 値は後で必要になります。

1. 「**[!UICONTROL Save]**」をクリックします。

>[!NOTE]
>
>顧客データプラットフォームのソースを作成したら、オーディエンスをインポートするための追加の手順を完了する必要があります。 [for [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)、<!-- the [workflow for [!DNL ActionIQ]](source-actioniq.md), -->for ワークフロー [、 [!DNL Amperity]](source-amperity.md)for ワークフロー [、 [!DNL Optimizely]](source-optimizely.md)for ワークフロー [ を参照してください  [!DNL Tealium]](source-tealium.md)

## Audience Sourceの ID タイプの変更

<!-- Clarify this:
All changes to universal IDs translated from the source are applied after you save the the source record. For example, if a new ID is added, any hashed email addresses shared before making the changes aren't converted. Similarly, if an ID is removed, we don't delete any historical data from the segments shared through the source.

OR 

All changes to universal IDs translated from the source are applied after you save the the source record. For example, if you add a new ID type, then we convert hashed email addresses shared before making the changes to the new ID type. Similarly, if you remove an ID type, then we delete any historical IDs of that type from the segments shared through the source.

-->

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL Sources]** をクリックします。

1. カーソルをソース行の上に置き、**[!UICONTROL Edit]** をクリックします。

1. ソースとして選択した [ID](#source-settings) を変更します。

1. 「**[!UICONTROL Save]**」をクリックします。

## オーディエンスのSourceの削除

ソースを削除すると、ソースを通じて翻訳されたセグメントが削除されます。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL Sources]** をクリックします。

1. カーソルをソース行の上に置き、**[!UICONTROL Delete]** をクリックします。

1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

## Audience Sourceの変更ログの表示

オーディエンスソースレコードに対する変更の詳細を表示したり、オプションでログにメモを添付したりできます。

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL Sources]** をクリックします。

1. カーソルをソース行の上に置き、**[!UICONTROL Change log]** をクリックします。

1. （オプション）変更ログにメモを添付するには、次の手順に従います。

   1. カーソルをソース行の上に置き、**[!UICONTROL Add Notes]** をクリックします。

   1. メモを入力し、[**[!UICONTROL Save]**] をクリックします。

      最大長は 256 文字です。

1. （オプション）ログをより詳細な画面で開くには、ソース行の上にカーソルを置いて「**[!UICONTROL View Details]**」をクリックします。

## Audience Sourceの設定 {#source-settings}

**[!UICONTROL Data Visibility Level]:** アカウント（*[!UICONTROL Advertiser]*）にアクセスできる単一の広告主に対してセグメントを使用できるか、アカウント *[!UICONTROL Account]* にアクセスできるすべての広告主に対してセグメントを使用できるか。

**[!UICONTROL Advertiser]:** （広告主レベルの表示のみ）セグメントを使用できる広告主。 アカウントにアクセスできる広告主のリストから 1 つ選択します。

**[!UICONTROL Enter IMS Org Id]:** （[!DNL Real-Time CDP] ソースのみ） [!DNL Adobe Experience Platform] アカウントのAdobe Experience Cloud組織 ID。

**[!UICONTROL Convert PII to the following IDs]:** 個人情報（PII）の変換先の ID タイプ。 複数のタイプを選択した場合、生成されたセグメントには、選択した各 ID タイプの値（メールアドレスごとの [!DNL RampID] や [!DNL Unified ID2.0] など）が入力されます。 データ料金はそれに応じて適用されます。

[!DNL RampID] と [!DNL Unified ID2.0] については、ベンダーは各メールアドレスを検索して ID が既に存在するかどうかを確認し、可能な場合はアドレスを一致する ID に変換します。 アドレスの ID が存在しない場合は、新しい ID が作成されます。

>[!NOTE]
>
>1 つのプレースメントでターゲットにできる ID のタイプは 1 つだけです。 ID タイプでパフォーマンスをテストするには、セグメント内の ID タイプごとに [ 個別のプレースメントを作成 ](/help/dsp/campaign-management/placements/placement-create.md) します。

* *[!DNL RampID]:* PII を [!DNL RampID] に変換します。 [!DNL RampIDs] は、ログインユーザーのリターゲティングや [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 測定に使用できます。

* *[!DNL Unified ID2.0]（Beta）:* ログインユーザーをリターゲティングするために、PII を [ 統合 ID 2.0](https://unifiedid.com) ID に変換する

<!-- Later
* *[!DNL ID5] (Beta):* To convert PII to an [!DNL ID5] ID. You can use [!DNL ID5] IDs for retargeting logging-in users and for [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) measurement.

-->

**[!UICONTROL Terms of Service]:** PII をユニバーサル ID に変換するためのサービス契約の条件。 データを新しい ID タイプに変換するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、「**>**」をクリックします。 条件に同意するには、条件の下部までスクロールし、「**[!UICONTROL Accept]**」をクリックします。

**[!UICONTROL Source Key]:** （読み取り専用、自動生成）オーディエンスをAdvertising DSPにプッシュするカスタマーデータプラットフォームで宛先接続を作成する際に使用できるソースキー。 値をクリップボードにコピーして、宛先接続設定またはファイルに貼り付けることができます。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](source-about.md)
>* [ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Adobe Real-Time CDP]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-adobe-rtcdp.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Amperity]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-amperity.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Optimizely]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-optimizely.md)
>* [ ユーザー ID をユニバーサル ID から  [!DNL Tealium]  ユニバーサル ID に変換 ](/help/dsp/audiences/sources/source-tealium.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
