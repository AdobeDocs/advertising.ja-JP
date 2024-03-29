---
title: 配置の広告スケジュールの編集
description: 配置に関連付けられた広告の広告スケジュールを変更する方法を説明します。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: 02a643662b00e2aed6dccf80cf8eeaf04d3d5c34
workflow-type: tm+mt
source-wordcount: '440'
ht-degree: 0%

---

# 配置の広告スケジュールの編集

## 1 つ以上の配置の広告スケジュールの編集

複数のプレースメントに関連付けられた広告に対して、スケジュールされたフライト日と広告のローテーションは、 [!DNL Microsoft Excel] スプレッドシート。 各広告は、複数のフライトでアクティブにできます。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. 広告データをダウンロードする各プレースメントの横にあるチェックボックスをオンにします。

1. バルクアクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. ファイルが使用可能になったら、 **[!UICONTROL Download]** ブラウザーページの上部にある通知で、ブラウザーの通常の手順に従って（XLSX 形式で）ワークシートファイルをダウンロードします。

   ![ダウンロード準備完了通知](/help/dsp/assets/download-ready.png "ダウンロード準備完了通知")

1. ダウンロードしたファイルを開き、フライトに含める各広告行のフライト情報フィールドを編集し、更新したファイルを保存します。

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** ( 例： [!UICONTROL Flight 1 Start Date] および [!UICONTROL Flight 1 End Date])：フライトの最初と最後の日付。 各日付には YYYY-MM-DD 形式を使用します。 フライト日フィールドが空の広告は、参加していない広告として扱われます。

   * **[!UICONTROL Flight N Weight]** ( 例： [!UICONTROL Flight 1 Weight])：フライト用に広告を回転する方法。 値を入力：

      * フライトの広告を均等に回転させるには、 `[!UICONTROL Even]`.

      * フライトの広告を不均等に回転させるには、各広告を回転させる相対的な重みをパーセンテージ ( `40` (40%)。 フライトの重みの合計は 100 にする必要があります。

1. 編集した広告スケジュールテンプレートをアップロードします。

   1. 該当する各配置の横にあるチェックボックスを選択します。

   1. バルクアクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**&#x200B;をクリックし、アップロードするファイルを指定します。

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
