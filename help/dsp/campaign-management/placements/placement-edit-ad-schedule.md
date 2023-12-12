---
title: 配置の広告スケジュールの編集
description: 配置に関連付けられた広告の広告スケジュールを変更する方法を説明します。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: 0b89d346aa7d1443e50605e1300a6a3645fe9b21
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---

# 配置の広告スケジュールの編集

<!--

## Edit the Ad Schedules for One or More Placements

You can change the scheduled flight dates and ad rotation for the ads attached to multiple placements using a [!DNL Microsoft Excel] spreadsheet. Each ad can be active during multiple flights.

1. In the main menu, click **[!UICONTROL Campaigns]**.

1. Click the name of the campaign.

1. In the submenu, click **[!UICONTROL Placements]**.

1. Select the check box next to each placement whose ad data you want to download.

1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. When the file is available, click **[!UICONTROL Download]** in the notification at the top of the browser page to download a worksheet file (in XLSX format) according to your browser's normal procedure..

   ![Download Ready notification](/help/dsp/assets/download-ready.png "Download Ready notification")

1. Open the downloaded file and edit the flight dates as needed.

1. Upload the edited ad schedule template:

   1. Select the check box next to each applicable placement.

   1. In the bulk actions toolbar, click **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**, and specify the file to upload.

-->

## 単一プレースメントの広告スケジュールの編集

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

配置に関連付けられた広告に対して、スケジュールされたフライト日と広告のローテーションを変更できます。 各広告は、複数のフライトでアクティブにできます。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. 配置名の横にある  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

   1. 次のいずれかの操作を行います。

      * フライトを追加するには、 **[!UICONTROL Add Flight]**&#x200B;をクリックし、開始日と終了日を指定します。

      * 広告に既存のフライトを追加するには、 **[!UICONTROL +]** （「flight」列の広告行）

      * 広告から既存のフライトを削除するには、 **[!UICONTROL x]** （「flight」列の広告行）

      * （複数の広告が同じフライトを持つ場合）広告を不均等に回転させるには、 **[!UICONTROL Even Rotation]** フライト情報を入力し、各広告を回転させる相対的な重みをパーセンテージで入力します。

        重みの合計は 100 にする必要があります。

   1. 右上で、 **[!UICONTROL Continue]**.

   1. フライトの詳細を確認し、 **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [配置管理について](placement-about.md)
>* [配置の編集](placement-edit.md)
>* [配置の変更ログの表示](placement-change-log.md)
>* [配置設定](placement-settings.md)
