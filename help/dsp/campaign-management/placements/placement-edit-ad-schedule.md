---
title: プレースメントの広告スケジュールの編集
description: プレースメントに添付された広告の広告スケジュールを変更する方法を説明します。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '439'
ht-degree: 0%

---

# プレースメントの広告スケジュールの編集

## 1 つ以上のプレースメントの広告スケジュールを編集

を使用して、複数のプレースメントに添付された広告の予定フライト日と広告のローテーションを変更できます。 [!DNL Microsoft Excel] スプレッドシート。 各広告は、複数のフライト中にアクティブにすることができます。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. 広告データをダウンロードする各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**.

1. ファイルが使用可能になったら、 **[!UICONTROL Download]** ブラウザーページの上部にある通知で、ブラウザーの通常の手順に従って（XLSX 形式の）ワークシートファイルをダウンロードします。

   ![ダウンロード準備完了の通知](/help/dsp/assets/download-ready.png "ダウンロード準備完了の通知")

1. ダウンロードしたファイルを開き、フライトに含める各広告行のフライト情報フィールドを編集し、更新したファイルを保存します。

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** （例： [!UICONTROL Flight 1 Start Date] および [!UICONTROL Flight 1 End Date]）：フライトの最初の日付と最後の日付。 各日付には YYYY-MM-DD 形式を使用します。 フライト日フィールドが空の広告は、非参加広告として扱われます。

   * **[!UICONTROL Flight N Weight]** （例： [!UICONTROL Flight 1 Weight]）：フライトの広告の回転方法。 値を入力：

      * フライトの広告を均等に回転するには、次のように入力します `[!UICONTROL Even]`.

      * フライトの広告を不均等に回転させるには、各広告の回転に使用する相対的な重みをパーセントで入力します（例： `40` （40% の場合）。 フライトの合計重量は 100 にする必要があります。

1. 編集した広告スケジュールテンプレートをアップロードします。

   1. 該当する各プレースメントの横にあるチェックボックスをオンにします。

   1. 一括アクションツールバーで、 **[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**&#x200B;を選択し、アップロードするファイルを指定します。

## 1 つのプレースメントの広告スケジュールの編集

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

プレースメントに添付された広告のスケジュールされたフライト日と広告のローテーションを変更できます。 各広告は、複数のフライト中にアクティブにすることができます。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. キャンペーンの名前をクリックします。

1. サブメニューで、 **[!UICONTROL Placements]**.

1. プレースメント名の横にある「」をクリックします  **[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**.

1. 次のいずれかの操作をおこないます。

   * フライトを追加するには、をクリックします **[!UICONTROL Add Flight]**&#x200B;を選択し、開始日と終了日を指定します。

   * 広告に既存のフライトを追加するには、をクリックします **[!UICONTROL +]** フライト列の広告行

   * 広告から既存のフライトを削除するには、をクリックします。 **[!UICONTROL x]** フライト列の広告行

      * （複数の広告が同じフライトを持つ場合）広告を不均等に回転するには、をクリックします **[!UICONTROL Even Rotation]** フライト情報で、各広告を回転させる相対的な重みをパーセントで入力します。

        合計重量は 100 にする必要があります。

1. 右上のをクリック **[!UICONTROL Continue]**.

1. フライトの詳細を確認し、 **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [プレースメント管理について](placement-about.md)
>* [プレースメントを編集](placement-edit.md)
>* [プレースメントの変更ログの表示](placement-change-log.md)
>* [プレースメント設定](placement-settings.md)
