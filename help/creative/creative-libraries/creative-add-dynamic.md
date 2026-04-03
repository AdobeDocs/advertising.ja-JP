---
title: クリエイティブライブラリへの動的クリエイターの追加
description: クリエイティブライブラリに動的なクリエイティブを追加する方法について説明します。
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
TQID: https://experienceleague.adobe.com/OGBJ2IszfF6kv86wYyEvbU5UxJmwxEo6MNjCM9n6Cws
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 516
ht-degree: 0%

---

# クリエイティブライブラリへの動的クリエイターの追加

動的なクリエイティブを[&#x200B; クリエイティブライブラリ &#x200B;](creative-library-manage.md)に追加して、動的な[広告エクスペリエンス &#x200B;](/help/creative/experiences/experience-about.md)で使用します。 1つの静的なHTML5広告または1つの広告テンプレートから動的なHTML5広告を作成できます。 動的なHTML5広告の場合は、フィードファイルから作成された指定されたカタログ内のアセットを使用します。

>[!PREREQUISITES]
>
>クリエイティブライブラリに動的クリエイティブを追加する前に、広告テンプレートの作成、アセットのアップロード、（動的なHTML5広告）フィードテンプレートとカタログの作成など、その他の手順を完了する必要があります。 「[動的な広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)」を参照してください。

<!--
 This does't work for me 9/24 -- I still have to select a catalog:

## Add dynamic creatives using a static HTML5 ad template

1. In the main menu, click **[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**.

1. Click the library name.

1. On the **[!UICONTROL Creatives]** tab, click **[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**.

1. Specify the [dynamic ad settings](/help/creative/creative-libraries/creative-settings-dynamic.md#dynamic-ad-settings-static-html5):

   1. On the [!UICONTROL Basic Details] tab, specify the ad details and the clickURL.

   1. Click **[!UICONTROL Process]**.

   1. On the [!UICONTROL Attributes Details] tab, specify the dynamic ad attributes.

1. Click **[!UICONTROL Save]**.

-->

## ダイナミックなHTML5広告テンプレートを使用して、ダイナミックなクリエイティブを追加する

1. 次のいずれかの操作を行います。

   * クリエイティブライブラリから：

      1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

      1. ライブラリ名をクリックします。

      1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Create]** > **[!UICONTROL Creatives]** > **[!UICONTROL Dynamic Ad]**&#x200B;をクリックします。

   * 広告テンプレートから：

      1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

      1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Create Dynamic Ad]**&#x200B;をクリックします。

1. [動的広告設定](/help/creative/creative-libraries/creative-settings-dynamic.md)を指定します。

   1. クリエイティブの種類など、基本的な広告の詳細を指定します。

   1. クリエイティブに使用する広告テンプレートを選択します。

      ディスプレイ広告にはHTML 5広告テンプレートを、ビデオ広告にはビデオ広告テンプレートを使用します。

   1. 広告を作成するカタログを選択します。

   1. 広告の作成に使用するカタログ行の基準を選択します。

   1. 指定された広告テンプレートの各属性（動的な広告フィールド）を、指定されたフィード ファイル（カタログラベル）の列にマッピングするか、静的値を入力します。

   1. 生成するクリエイティブをプレビューするには、**[!UICONTROL Continue]**&#x200B;をクリックします。 プレビュー内で次のいずれかを実行できます。

      * カタログ、フィルター値<!-- explain more-->、広告サイズでクリエイティブをフィルタリングするには、プレビュー領域の上にあるフィルターを使用します。

      * プレビュー領域の下にある検索フィールドで、製品を一意のIDで検索する。

      * 表示される列を変更するには、プレビュー領域の下にある![列フィルター](/help/creative/assets/custom-columns.png "列フィルター")をクリックします。

      * 特定のクリエイティブをプレビューするには、行のチェックボックスをオンにします。

      * コンテンツを変更する：

         * （表示広告のみ）表内のセルの値を編集するには、セル内をクリックして値を編集します。 セルの外側をクリックするか、**[!DNL Enter]** キーを押して変更を保存します。

         * 1つの商品をデフォルト <!--Explain what this means. -->としてマークするには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Set as Default]**&#x200B;をクリックします。

         * （広告に複数のオファーが含まれる場合）複数の商品をデフォルトとしてマークするには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Set as Default]**」をクリックします。

      * 商品をカタログから削除するには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete Row]**&#x200B;をクリックします。

      * （広告に複数のオファーが含まれる場合）カタログから複数の商品を削除するには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Delete Row]**」をクリックします。

1. クリエイターを救う：

   * 広告を保存し、ライブラリの[&#x200B; クリエイティブバンドル &#x200B;](/help/creative/creative-libraries/bundle-manage.md)に追加するには：

      1. **[!UICONTROL Save and Attach to Bundle]**&#x200B;をクリックします。

      1. **[!UICONTROL Save]**&#x200B;をクリックして広告を保存します。

      1. バンドルを選択し、**[!UICONTROL Attach Creative to Bundles]**&#x200B;をクリックします。

   * 広告を保存して設定を終了するには、**[!UICONTROL Save]**&#x200B;をクリックし、もう一度&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [動的なクリエイティブ設定](creative-settings-dynamic.md)
>* [&#x200B; クリエイティブライブラリでの動的クリエイティブの編集](creative-edit-dynamic.md)
>* [&#x200B; クリエイティブの変更ログを表示](/help/creative/creative-libraries/creative-view-change-log.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
