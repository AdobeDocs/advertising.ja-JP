---
title: プレースメントの広告スケジュールの編集
description: プレースメントにアタッチされた広告の広告スケジュールを変更する方法について説明します。
feature: DSP Placements
exl-id: 4c981d57-032f-4cde-858a-e9ac2bf2e6f2
TQID: https://experienceleague.adobe.com/-5TLojZnwpnYonGlRARUUljuNMd2ZDGpnU9u1jzsHyw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 442
ht-degree: 0%

---

# プレースメントの広告スケジュールの編集

## 1つ以上のプレースメントの広告スケジュールの編集

[!DNL Microsoft Excel] スプレッドシートを使用して、複数のプレースメントに添付された広告のスケジュールされたフライト日と広告ローテーションを変更できます。 各広告は、複数のフライト中にアクティブになることができます。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]**&#x200B;をクリックします。

1. ダウンロードする広告データを持つ各プレースメントの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL ...]** > **[!UICONTROL Download Custom Ad Schedule Sheet]**&#x200B;をクリックします。

1. ファイルが使用可能になったら、ブラウザーページの上部にある通知の&#x200B;**[!UICONTROL Download]**&#x200B;をクリックして、ブラウザーの通常の手順に従って（XLSX形式の）ワークシートファイルをダウンロードします。

   ![ ダウンロード準備完了の通知](/help/dsp/assets/download-ready.png " ダウンロード準備完了の通知")

1. ダウンロードしたファイルを開き、フライトに含める各広告行のフライト情報フィールドを編集し、更新したファイルを保存します。

   * **[!UICONTROL Flight N Start Date]** / **[!UICONTROL Flight N End Date]** （[!UICONTROL Flight 1 Start Date]や[!UICONTROL Flight 1 End Date]など）: フライトの最初と最後の日付。 各日付にYYYY-MM-DDの形式を使用します。 フライト日フィールドが空の広告は、非参加広告として扱われます。

   * **[!UICONTROL Flight N Weight]** （[!UICONTROL Flight 1 Weight]など）：フライトの広告を回転させる方法。 値を入力：

      * フライトの広告を均等に回転させるには、`[!UICONTROL Even]`と入力します。

      * フライトの広告を不均等に回転させるには、各広告を回転させる相対的な重みをパーセントで入力します（例：`40`、40%）。 フライトの総重みは100に等しくなければなりません。

1. 編集した広告スケジュール テンプレートをアップロードします。

   1. 該当する各配置の横にあるチェックボックスをオンにします。

   1. 一括操作ツールバーで、**[!UICONTROL ...]** > **[!UICONTROL Upload Custom Ad Schedule Sheet]**&#x200B;をクリックし、アップロードするファイルを指定します。

## 1つのプレースメントの広告スケジュールの編集

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- just simple ad serving placements (PG ones seem okay)? And anything else? -->

プレースメントにアタッチされた広告のスケジュールされたフライト日と広告ローテーションを変更できます。 各広告は、複数のフライト中にアクティブになることができます。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]**&#x200B;をクリックします。

1. プレースメント名の横で、**[!UICONTROL ...]** > **[!UICONTROL Ads]** > **[!UICONTROL Ad schedule]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * フライトを追加するには、**[!UICONTROL Add Flight]**&#x200B;をクリックし、開始日と終了日を指定します。

   * 既存のフライトを広告に追加するには、フライト列の広告行の&#x200B;**[!UICONTROL +]**&#x200B;をクリックします。

   * 広告から既存のフライトを削除するには、フライト列の広告行の&#x200B;**[!UICONTROL x]**&#x200B;をクリックします。

      * （複数の広告に同じフライトがある場合）広告を不均等に回転させるには、フライト情報の&#x200B;**[!UICONTROL Even Rotation]**&#x200B;をクリックし、各広告を回転させる相対的な重みをパーセント単位で入力します。

        重みの合計は100に等しくなければなりません。

1. 右上の「**[!UICONTROL Continue]**」をクリックします。

1. フライトの詳細を確認し、**[!UICONTROL Save & Finish]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのプレースメント管理について](placement-about.md)
>* [ プレースメントを編集](placement-edit.md)
>* [ プレースメントの変更ログを表示](placement-change-log.md)
>* [配置の設定](placement-settings.md)
