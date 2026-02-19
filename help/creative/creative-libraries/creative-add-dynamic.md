---
title: クリエイティブライブラリへのダイナミッククリエイティブの追加
description: クリエイティブライブラリにダイナミッククリエイティブを追加する方法を説明します。
feature: Creative Dynamic Creatives
exl-id: 26162314-bdaa-4d1c-b0c2-696ec6dbb138
source-git-commit: 2a89d5f3997345c051728d41af865dc0e75541f5
workflow-type: tm+mt
source-wordcount: '509'
ht-degree: 0%

---

# クリエイティブライブラリへのダイナミッククリエイティブの追加

動的な [ad エクスペリエンス &#x200B;](creative-library-manage.md) で使用するには、動的なクリエイティブを [&#x200B; クリエイティブライブラリ &#x200B;](/help/creative/experiences/experience-about.md) に追加します。 1 つの広告テンプレートから 1 つの静的HTML5 広告または動的HTML5 広告を作成できます。 動的HTML5 広告の場合は、フィードファイルから作成された指定のカタログのアセットを使用します。

>[!PREREQUISITES]
>
>ダイナミッククリエイティブをクリエイティブライブラリに追加する前に、広告テンプレートの作成、アセットのアップロード、（dynamic HTML5 広告）フィードテンプレートとカタログの作成など、他の手順を実行する必要があります。 [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md) を参照してください。

<!-- This does't work for me 9/24 -- I still have to select a catalog:

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

## 動的なHTML5 広告テンプレートを使用した動的なクリエイティブの追加

1. 次のいずれかの操作をおこないます。

   * クリエイティブライブラリから：

      1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

      1. ライブラリ名をクリックします。

      1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Dynamic Ad]** をクリックします。

   * 広告テンプレートから：

      1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Ad Templates]** をクリックします。

      1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Create Dynamic Ad]** をクリックします。

1. [&#x200B; 動的広告設定 &#x200B;](/help/creative/creative-libraries/creative-settings-dynamic.md) を指定します。

   1. クリエイティブタイプを含む基本広告の詳細を指定します。

   1. クリエイティブに使用する広告テンプレートを選択します。

      ディスプレイ広告にはHTML5 広告テンプレートを、ビデオ広告にはビデオ広告テンプレートを使用します。

   1. 広告を作成するカタログを選択します。

   1. カタログ行で広告の作成に使用する条件を選択します。

   1. 指定した広告テンプレートの各属性（動的広告フィールド）を、指定したフィードファイル（カタログラベル）の列にマッピングするか、静的な値を入力します。

   1. 「**[!UICONTROL Continue]**」をクリックして、生成するクリエイティブをプレビューします。 プレビュー内で次のいずれかの操作を行うことができます。

      * カタログ、フィルター値 <!-- explain more--> 広告サイズでクリエイティブをフィルタリングするには、プレビューエリアの上にあるフィルターを使用します。

      * プレビューエリアの下の検索フィールドで、一意の ID で製品を検索するには、次のようにします。

      * 表示される列を変更するには、プレビュー領域の下にある ![&#x200B; 列フィルター &#x200B;](/help/creative/assets/custom-columns.png " 列フィルター ") をクリックします。

      * 特定のクリエイティブをプレビューするには、行のチェックボックスをオンにします。

      * コンテンツを変更します。

         * （広告を表示のみ）テーブル内のセルの値を編集するには、セル内をクリックして値を編集します。 セルの外側をクリックするか、**[!DNL Enter]** キーを押して変更を保存します。

         * 1 つの製品をデフォルトとしてマークするには <!--Explain what this means. --> 行の上にカーソルを置き、**[!UICONTROL ...]**/**[!UICONTROL Set as Default]** をクリックします。

         * （広告に複数のオファーが含まれる場合）複数の製品をデフォルトとしてマークするには、行（オファーの数を上限とする）を選択し、一括アクションツールバーの「**[!UICONTROL Set as Default]**」をクリックします。

      * カタログから製品を削除するには、行の上にカーソルを置き、**[!UICONTROL ...]**/**[!UICONTROL Delete Row]** をクリックします。

      * （広告に複数のオファーが含まれる場合）カタログから複数の製品を削除するには、一括アクションのツールバーで、行（オファーの数を上限とする）を選択し **[!UICONTROL Delete Row]** クリックします。

1. クリエイティブを保存します。

   * 広告を保存してライブラリの [&#x200B; クリエイティブバンドル &#x200B;](/help/creative/creative-libraries/bundle-manage.md) に追加するには：

      1. 「**[!UICONTROL Save and Attach to Bundle]**」をクリックします。

      1. 「**[!UICONTROL Save]**」をクリックして、広告を保存します。

      1. バンドルを選択し、「選 **[!UICONTROL Attach Creative to Bundles]**」をクリックします。

   * 広告を保存して設定を終了するには、[**[!UICONTROL Save]**] をクリックし、もう一度 [**[!UICONTROL Save]**] をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; 動的クリエイティブ設定 &#x200B;](creative-settings-dynamic.md)
>* [&#x200B; クリエイティブライブラリでの動的クリエイティブの編集 &#x200B;](creative-edit-dynamic.md)
>* [&#x200B; 動的広告のワークフロー &#x200B;](/help/creative/introduction/workflow-dynamic-ads.md)
