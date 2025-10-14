---
title: URL リストの管理
description: プレースメントターゲティング用の URL リストを作成および管理する方法について説明します。
feature: DSP Placements
source-git-commit: ea33d6fa7612f1c9631c223e5bf0ec80bb5f8d96
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# URL リストの管理

プレースメントターゲティング用の web サイトおよびアプリ URL のリストを作成および管理できます。 プレースメント設定内で特定の URL リストをターゲットに設定したり、除外したりできます。

## URL リストの表示

1. メインメニューで、**[!UICONTROL Resources]**/**[!UICONTROL URL Lists]** をクリックします。

1. リスト名をクリックします。

1. （オプション）選択したリストを XLSX （[!DNL Microsoft Excel] スプレッドシート）形式に書き出すには、「![&#x200B; 書き出し &#x200B;](/help/dsp/assets/export.png " 書き出し ")」 **[!UICONTROL Export]** タンをクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## URL リストの作成

1. メインメニューで、**[!UICONTROL Resources]**/**[!UICONTROL URL Lists]** をクリックします。

1. 右上で「**[!UICONTROL Create].**」をクリックします。

1. **[!UICONTROL List name]** を入力し、「**[!UICONTROL Create].**」をクリックします

1. 次のいずれかの操作をおこないます。

   * 追加する URL を手動で入力または貼り付けるには：

      1. **[!UICONTROL Bulk Add URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

      1. 最大 10,000 個の URL を入力または貼り付け、各 URL を別々の行に配置します。

      1. 「**[!UICONTROL Validate]**」をクリックして、URL が有効かどうかを確認します。

         無効な URL が特定されます。 続行すると、有効な URL のみが追加されます。

      1. 「**[!UICONTROL Add to list]**」をクリックします。

   * ファイルから URL を追加するには：

      1. **[!UICONTROL Bulk Add URLs]**/**[!UICONTROL Import File]** をクリックします。

      1. URL を含むローカル CSV ファイルをドラッグ&amp;ドロップします。各 URL は別々の行に配置されます。

         ファイルには、データ列を 1 つだけ含め、列ヘッダー行は含めないでください。 既存のリストを書き出して行を編集した場合は、ヘッダー行、2 列目、3 列目を削除してから、ファイルを再度読み込みます。 続行すると、無効な値を含む行は追加されません。

      1. 「**[!UICONTROL Add to list]**」をクリックします。

         タスクが完了すると、通知メッセージが表示されます。 ページを更新して、更新されたリストを表示します。

      1. 追加された URL の数や失敗した値の数など、タスクのステータスを確認するには、次の手順を実行します。

         1. 上部メニューバーの右側にある「![&#x200B; ジョブ &#x200B;](/help/dsp/assets/downloads.png)」をクリックします。

         1. （追加されていない行がある場合）失敗した値を含むエラーファイルをダウンロードするには、ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

            ファイルはブラウザーのダウンロードフォルダーに保存されます。

   * 特定の URL を削除するには、次のいずれかを実行します。

      * 削除する URL を選択するには：

         1. リストから削除する各取引の横にあるチェックボックスをオンにします。

         1. 「**[!UICONTROL Remove from List]**」をクリックします。

         1. 確認メッセージで、「**[!UICONTROL Remove]**」をクリックします。

      * 削除する URL を入力または貼り付けるには：

         1. **[!UICONTROL Bulk Remove URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

         1. 最大 10,000 個の URL を入力または貼り付け、各 URL を別々の行に配置します。

         1. **[!UICONTROL Validate]** をクリックして、URL が有効で、現在リストに含まれているかどうかを確認します。

         1. 「**[!UICONTROL Remove from list]**」をクリックします。

   * すべての URL を削除するには：

      1. **[!UICONTROL Bulk Remove URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

      1. 「**[!UICONTROL Remove All URLs]**」をクリックします。

      1. 「**[!UICONTROL Remove]**」をクリックします。

## URL リストの編集

1. メインメニューで、**[!UICONTROL Resources]**/**[!UICONTROL URL Lists]** をクリックします。

1. リスト名をクリックします。

1. 次のいずれかの操作をおこないます。

   * 追加する URL を手動で入力または貼り付けるには：

      1. **[!UICONTROL Bulk Add URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

      1. 最大 10,000 個の URL を入力または貼り付け、各 URL を別々の行に配置します。

      1. 「**[!UICONTROL Validate]**」をクリックして、URL が有効かどうかを確認します。

         無効な URL が特定されます。 続行すると、有効な URL のみが追加されます。

      1. 「**[!UICONTROL Add to list]**」をクリックします。

   * ファイルから URL を追加するには：

      1. **[!UICONTROL Bulk Add URLs]**/**[!UICONTROL Import File]** をクリックします。

      1. URL を含むローカル CSV ファイルをドラッグ&amp;ドロップします。各 URL は別々の行に配置されます。

         ファイルには、データ列を 1 つだけ含め、列ヘッダー行は含めないでください。 既存のリストを書き出して行を編集した場合は、ヘッダー行、2 列目、3 列目を削除してから、ファイルを再度読み込みます。 続行すると、無効な値を含む行は追加されません。

      1. 「**[!UICONTROL Add to list]**」をクリックします。

         タスクが完了すると、通知メッセージが表示されます。

      1. 追加された URL の数や失敗した値の数など、タスクのステータスを確認するには、次の手順を実行します。

         1. 上部メニューバーの右側にある「![&#x200B; ジョブ &#x200B;](/help/dsp/assets/downloads.png)」をクリックします。

         1. （追加されていない行がある場合）失敗した値を含むエラーファイルをダウンロードするには、ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

            ファイルはブラウザーのダウンロードフォルダーに保存されます。

   * 特定の URL を削除するには、次のいずれかを実行します。

      * 削除する URL を選択するには：

         1. リストから削除する各取引の横にあるチェックボックスをオンにします。

         1. 「**[!UICONTROL Remove from List]**」をクリックします。

         1. 確認メッセージで、「**[!UICONTROL Remove]**」をクリックします。

      * 削除する URL を入力または貼り付けるには：

         1. **[!UICONTROL Bulk Remove URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

         1. 最大 10,000 個の URL を入力または貼り付け、各 URL を別々の行に配置します。

         1. **[!UICONTROL Validate]** をクリックして、URL が有効で、現在リストに含まれているかどうかを確認します。

         1. 「**[!UICONTROL Remove from list]**」をクリックします。

   * すべての URL を削除するには：

      1. **[!UICONTROL Bulk Remove URLs]**/**[!UICONTROL Copy/Paste URLs]** をクリックします。

      1. 「**[!UICONTROL Remove All URLs]**」をクリックします。

      1. 「**[!UICONTROL Remove]**」をクリックします。

## URL リストのエクスポート

1. メインメニューで、**[!UICONTROL Resources]**/**[!UICONTROL URL Lists]** をクリックします。

1. リスト名をクリックします。

1. 「![&#x200B; エクスポート &#x200B;](/help/dsp/assets/export.png " エクスポート ")」をクリッ **[!UICONTROL Export]** します。

   ファイルは、ブラウザーの通常の手順に従って、XLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードされます。

>[!MORELIKETHIS]
>
>* [&#x200B; プレースメント設定 &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; アカウントレベルと広告主レベルのブロックされたサイトリストについて &#x200B;](/help/dsp/admin/blocked-sites-list-about.md)
>* [&#x200B; アカウントレベルまたは広告主レベルのブロックされたサイトリストの編集 &#x200B;](/help/dsp/admin/blocked-sites-list-edit.md)
