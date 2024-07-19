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

[!DNL Microsoft Excel] スプレッドシートを使用して、複数のプレースメントに添付された広告の予定フライト日と広告のローテーションを変更できます。 各広告は、複数のフライト中にアクティブにすることができます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]** をクリックします。

1. 広告データをダウンロードする各プレースメントの横にあるチェックボックスをオンにします。

1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Download Custom Ad Schedule Sheet]** をクリックします。

1. ファイルが使用可能になったら、ブラウザーページの上部にある通知で **[!UICONTROL Download]** をクリックして、ブラウザーの通常の手順に従って（XLSX 形式の）ワークシートファイルをダウンロードします。

   ![ ダウンロード準備完了の通知 ](/help/dsp/assets/download-ready.png " ダウンロード準備完了の通知 ")

1. ダウンロードしたファイルを開き、フライトに含める各広告行のフライト情報フィールドを編集し、更新したファイルを保存します。

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** （[!UICONTROL Flight 1 Start Date] や [!UICONTROL Flight 1 End Date] など）：フライトの最初の日付と最後の日付。 各日付には YYYY-MM-DD 形式を使用します。 フライト日フィールドが空の広告は、非参加広告として扱われます。

   * **[!UICONTROL Flight N Weight]** （[!UICONTROL Flight 1 Weight] など）：フライトの広告を回転させる方法。 値を入力：

      * フライトの広告を均等に回転するには、`[!UICONTROL Even]` と入力します。

      * フライトの広告を不均等に回転させるには、各広告の回転に使用する相対的な重みをパーセントで入力します（40% の `40` など）。 フライトの合計重量は 100 にする必要があります。

1. 編集した広告スケジュールテンプレートをアップロードします。

   1. 該当する各プレースメントの横にあるチェックボックスをオンにします。

   1. 一括アクションツールバーで、**[!UICONTROL ...]**/**[!UICONTROL Upload Custom Ad Schedule Sheet]** をクリックし、アップロードするファイルを指定します。

## 1 つのプレースメントの広告スケジュールの編集

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

プレースメントに添付された広告のスケジュールされたフライト日と広告のローテーションを変更できます。 各広告は、複数のフライト中にアクティブにすることができます。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]** をクリックします。

1. プレースメント名の横で、**[!UICONTROL ...]**/**[!UICONTROL Ad schedule]** をクリックします。

1. 次のいずれかの操作をおこないます。

   * フライトを追加するには、[**[!UICONTROL Add Flight]**] をクリックし、開始日と終了日を指定します。

   * 既存のフライトを広告に追加するには、フライト列の広告行の **[!UICONTROL +]** をクリックします。

   * 既存のフライトを広告から削除するには、フライト列の広告行の **[!UICONTROL x]** をクリックします。

      * （複数の広告が同じフライトを持つ場合）広告を不均等に回転させるには、フライト情報の **[!UICONTROL Even Rotation]** をクリックし、各広告を回転させる相対的な重みをパーセントで入力します。

        合計重量は 100 にする必要があります。

1. 右上で、「**[!UICONTROL Continue]**」をクリックします。

1. フライトの詳細を確認し、[**[!UICONTROL Save & Finish]**] をクリックします。

>[!MORELIKETHIS]
>
>* [ プレースメント管理について ](placement-about.md)
>* [ プレースメントを編集 ](placement-edit.md)
>* [ プレースメントの変更ログを表示 ](placement-change-log.md)
>* [ プレースメント設定 ](placement-settings.md)
