---
title: URL リストの管理
description: プレースメントターゲティング用のURL リストを作成および管理する方法について説明します。
feature: DSP Placements
exl-id: 57c715b3-9a13-4890-a3b8-03fa6adb44eb
TQID: https://experienceleague.adobe.com/evxwpbMXExxa30xpsojzTxcRfAxrozOSmwoJuCHPVPw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 694
ht-degree: 0%

---

# URL リストの管理

プレースメントターゲティング用のweb サイトとアプリのURLのリストを作成および管理できます。 プレースメント設定内の特定のURL リストをターゲットまたは除外します。

## URL リストの表示

1. メインメニューで、**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**&#x200B;をクリックします。

1. リスト名をクリックします。

1. （オプション）選択したリストをXLSX （[!DNL Microsoft Excel] スプレッドシート）形式で書き出すには、「![書き出し](/help/dsp/assets/export.png "書き出し") **[!UICONTROL Export]**」をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## URL リストの作成

1. メインメニューで、**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**&#x200B;をクリックします。

1. 右上の&#x200B;**[!UICONTROL Create].**&#x200B;をクリックします

1. **[!UICONTROL List name]**&#x200B;を入力し、**[!UICONTROL Create].**&#x200B;をクリックします

1. 次のいずれかの操作を行います。

   * 追加するURLを手動で入力または貼り付けるには：

      1. **[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

      1. 1行に各URLを含めて、最大10,000個のURLを入力または貼り付けます。

      1. 「**[!UICONTROL Validate]**」をクリックして、URLが有効かどうかを確認します。

         無効なURLが識別されます。 続行する場合は、有効なURLのみが追加されます。

      1. **[!UICONTROL Add to list]**&#x200B;をクリックします。

   * ファイルからURLを追加するには：

      1. **[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Import File]**&#x200B;をクリックします。

      1. URLを含むローカルのCSV ファイルをドラッグ&amp;ドロップし、各URLを別々の行に置きます。

         ファイルには、列ヘッダー行のないデータ列を1つだけ含める必要があります。 既存のリストを書き出して行を編集した場合は、ファイルを再インポートする前に、ヘッダー行と2番目と3番目の列を削除します。 無効な値を持つ行は、続行しても追加されません。

      1. **[!UICONTROL Add to list]**&#x200B;をクリックします。

         通知メッセージは、タスクがいつ完了したかを示します。 ページを更新して、更新されたリストを表示します。

      1. 追加されたURLの数や失敗した値の数など、タスクのステータスを確認するには、次の手順を実行します。

         1. 上部メニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。

         1. （行が追加されていない場合）失敗した値を含むエラーファイルをダウンロードするには、ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

            ファイルはブラウザーのダウンロードフォルダーに保存されます。

   * 特定のURLを削除するには、次のいずれかの操作を行います。

      * 削除するURLを選択するには：

         1. リストから削除する各取引の横にあるチェックボックスをオンにします。

         1. **[!UICONTROL Remove from List]**&#x200B;をクリックします。

         1. 確認メッセージで、**[!UICONTROL Remove]**&#x200B;をクリックします。

      * 削除するURLを入力または貼り付けるには：

         1. **[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

         1. 1行に各URLを含めて、最大10,000個のURLを入力または貼り付けます。

         1. 「**[!UICONTROL Validate]**」をクリックして、URLが有効であり、現在リストに含まれているかどうかを確認します。

         1. **[!UICONTROL Remove from list]**&#x200B;をクリックします。

   * すべてのURLを削除するには：

      1. **[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

      1. **[!UICONTROL Remove All URLs]**&#x200B;をクリックします。

      1. **[!UICONTROL Remove]**&#x200B;をクリックします。

## URL リストの編集

1. メインメニューで、**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**&#x200B;をクリックします。

1. リスト名をクリックします。

1. 次のいずれかの操作を行います。

   * 追加するURLを手動で入力または貼り付けるには：

      1. **[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

      1. 1行に各URLを含めて、最大10,000個のURLを入力または貼り付けます。

      1. 「**[!UICONTROL Validate]**」をクリックして、URLが有効かどうかを確認します。

         無効なURLが識別されます。 続行する場合は、有効なURLのみが追加されます。

      1. **[!UICONTROL Add to list]**&#x200B;をクリックします。

   * ファイルからURLを追加するには：

      1. **[!UICONTROL Bulk Add URLs]** > **[!UICONTROL Import File]**&#x200B;をクリックします。

      1. URLを含むローカルのCSV ファイルをドラッグ&amp;ドロップし、各URLを別々の行に置きます。

         ファイルには、列ヘッダー行のないデータ列を1つだけ含める必要があります。 既存のリストを書き出して行を編集した場合は、ファイルを再インポートする前に、ヘッダー行と2番目と3番目の列を削除します。 無効な値を持つ行は、続行しても追加されません。

      1. **[!UICONTROL Add to list]**&#x200B;をクリックします。

         通知メッセージは、タスクがいつ完了したかを示します。

      1. 追加されたURLの数や失敗した値の数など、タスクのステータスを確認するには、次の手順を実行します。

         1. 上部メニューバーの右側にある「![ ジョブ ](/help/dsp/assets/downloads.png)」をクリックします。

         1. （行が追加されていない場合）失敗した値を含むエラーファイルをダウンロードするには、ジョブの横にある「**[!UICONTROL Download]**」をクリックします。

            ファイルはブラウザーのダウンロードフォルダーに保存されます。

   * 特定のURLを削除するには、次のいずれかの操作を行います。

      * 削除するURLを選択するには：

         1. リストから削除する各取引の横にあるチェックボックスをオンにします。

         1. **[!UICONTROL Remove from List]**&#x200B;をクリックします。

         1. 確認メッセージで、**[!UICONTROL Remove]**&#x200B;をクリックします。

      * 削除するURLを入力または貼り付けるには：

         1. **[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

         1. 1行に各URLを含めて、最大10,000個のURLを入力または貼り付けます。

         1. 「**[!UICONTROL Validate]**」をクリックして、URLが有効であり、現在リストに含まれているかどうかを確認します。

         1. **[!UICONTROL Remove from list]**&#x200B;をクリックします。

   * すべてのURLを削除するには：

      1. **[!UICONTROL Bulk Remove URLs]** > **[!UICONTROL Copy/Paste URLs]**&#x200B;をクリックします。

      1. **[!UICONTROL Remove All URLs]**&#x200B;をクリックします。

      1. **[!UICONTROL Remove]**&#x200B;をクリックします。

## URL リストの書き出し

1. メインメニューで、**[!UICONTROL Resources]** > **[!UICONTROL URL Lists]**&#x200B;をクリックします。

1. リスト名をクリックします。

1. 「![書き出し](/help/dsp/assets/export.png "書き出し") **[!UICONTROL Export]**」をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってXLSX （[!DNL Microsoft Excel] スプレッドシート）形式でダウンロードされます。

>[!MORELIKETHIS]
>
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [ アカウントレベルおよび広告主レベルのブロックされたサイトリストについて](/help/dsp/admin/blocked-sites-list-about.md)
>* [ アカウントレベルまたは広告主レベルのブロック済みサイトリストを編集](/help/dsp/admin/blocked-sites-list-edit.md)
