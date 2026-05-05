---
title: DSPで広告主のコンバージョン指標を管理します。
description: Adobe AdvertisingがDSP広告主に追跡するコンバージョン指標の使用方法について説明します。
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '528'
ht-degree: 0%

---

# 広告主のコンバージョン指標の管理

広告主のコンバージョン指標は、Adobe Advertising全体で使用されます。

* Advertising DSPでは、キャンペーン管理ビュー、カスタム目標、カスタムレポートにコンバージョン指標を含めることができます。 また、広告主のコンバージョン指標を使用して[&#x200B; カスタム目標](/help/dsp/admin/custom-objectives-manage.md)を作成し、パッケージの最適化に使用することもできます。

* （Advertising Search, Social, &amp; Commerceの広告主） Search, Social, &amp; Commerceでは、コンバージョン指標のデータを、キャンペーンビュー、ポートフォリオおよび客観的な管理ビューとレポートの列に表示できます。 十分なアクセス権限を持つユーザーは、コンバージョン指標を使用して目的を作成し、ポートフォリオの最適化に使用することもできます。

<!--
The conversion metrics that Adobe Advertising tracks for an advertiser &mdash; including [conversion and site engagement metrics synced from Adobe Analytics](/help/integrations/analytics/analytics-data-in-advertising.md), [site events synced from Adobe Customer Journey Analytics](/help/integrations/customer-journey-analytics/overview.md), and custom feeds &mdash; are used throughout Advertising DSP. You can include conversion metrics in campaign management views, custom objectives, and custom reports. You can also use conversion metrics to create [custom objectives](/help/dsp/admin/custom-objectives-manage.md), which are used to optimize packages.

By default, none of an advertiser's conversion metrics are available for campaign management views, custom objectives, and reports. They are available only when you specifically make them available. When you make a conversion metric available, you can either use the metric name exactly as it is spelled in the retrieved data or change the display name that's shown in column headings for readability.

From the list of visible metrics, each user with access to the advertiser's data can customize the metrics they see for campaign management views, objectives, and reports by including or omitting specific metrics. Users with sufficient access privileges can also optimize for specific metrics by associating them with DSP package-level custom goals.

-->

DSP ユーザーで追跡される指標の種類は次のとおりです。

* Adobe Advertisingが広告主向けに追跡するコンバージョン指標。

* [&#x200B; コンバージョンとサイトエンゲージメントの指標がAdobe Analyticsから同期されました](/help/integrations/analytics/analytics-data-in-advertising.md)。

* [&#x200B; サイトイベントがAdobe Customer Journey Analyticsから同期されました](/help/integrations/customer-journey-analytics/overview.md)。

* カスタムフィードからのコンバージョン。

利用可能なコンバージョン指標のリストから、広告主のデータへのアクセス権を持つ各ユーザーは、管理ビューやレポートで利用できる指標（選択した特定の指標を含む）をカスタマイズできます。 取得したデータのスペルと正確に一致する指標の名前を使用するか、列見出しに表示される名前を変更して読みやすくすることができます。

>[!IMPORTANT]
>
>デフォルトでは、広告主のコンバージョン指標は、キャンペーン管理ビュー、カスタム目標、カスタムレポートに含めることはできません。 コンバージョン指標を使用できるようにするには、コンバージョン指標を明示的に使用できるようにする必要があります。

>[!TIP]
>
>広告主（または広告ネットワーク）がコンバージョン指標の収集を停止すると、過去データの表示に使用しない限り、[管理表示とレポート &#x200B;](#conversion-metrics-change-available)から非表示にします。

## 広告主が追跡したコンバージョン指標の表示

* メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**&#x200B;をクリックします。

広告主向けに収集されたすべてのコンバージョン指標と、それらに割り当てられたさまざまな表示名が一覧表示されます。 各指標の行には、指標のソースが含まれます。

## コンバージョン指標の表示名の変更

例えば、*reg*&#x200B;という名前の変換指標を使用して登録データを収集する場合、オプションで表示名を変更して、「登録」として表示されるようにすることができます。

既存の表示名は削除できません。

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Conversions Beta]**&#x200B;をクリックします。

1. 行の上にカーソルを置き、**[!UICONTROL Edit Display Name]**&#x200B;をクリックします。

1. 表示する名前を入力し、**[!UICONTROL Save]**&#x200B;をクリックします。

   表示名は一意である必要があり、次の特殊文字を含めることはできません：`\"<'>&`

## キャンペーン管理ビュー、カスタム目標、カスタムレポートで利用できるコンバージョン指標を変更します {#change-the-conversion-metrics-available-in-ui}

1. メインメニューで、**[!UICONTROL Settings]>[!UICONTROL Conversions]**&#x200B;をクリックします。

   広告主向けに収集されたすべてのコンバージョン指標と、表示用に指定されたさまざまな名前が一覧表示されます。

1. （オプション）リストをフィルタリングします。

   1. リストの上にある「![&#x200B; フィルター](/help/dsp/assets/filter.png " フィルター")」をクリックします。

   1. フィルターを指定し、**[!DNL Apply]**&#x200B;をクリックします。

      AMO クライアント ID、指標がUIで表示または非表示になっているかどうか、およびデータソースによって、指標をフィルタリングできます。

1. 管理ビューとレポートで使用できるコンバージョン指標を変更します。

   * 指標を表示するには、行の上にカーソルを置き、**[!UICONTROL Show in UI and Reports]**&#x200B;をクリックします。

   * 指標を非表示にするには、行の上にカーソルを置き、**[!UICONTROL Hide in UI and Reports]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーンデータビューの管理](/help/dsp/campaign-management/reports/campaign-data-views-manage.md)
>* [&#x200B; カスタム目標の管理](/help/dsp/admin/custom-objectives-manage.md)
