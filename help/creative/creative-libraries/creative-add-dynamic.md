---
title: クリエイティブライブラリへのダイナミッククリエイティブの追加
description: クリエイティブライブラリにダイナミッククリエイティブを追加する方法を説明します。
feature: Creative Dynamic Creatives
source-git-commit: 76e3ae8369fda1c4d95c06ecb085a8669dcf142b
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# クリエイティブライブラリへのダイナミッククリエイティブの追加

動的な [ad エクスペリエンス ](creative-library-manage.md) で使用するには、動的なクリエイティブを [ クリエイティブライブラリ ](/help/creative/experiences/experience-about.md) に追加します。 1 つの広告テンプレートから 1 つの静的HTML5 広告または動的HTML5 広告を作成できます。 動的HTML5 広告の場合は、フィードファイルから作成された指定のカタログのアセットを使用します。

>[!PREREQUISITES]
>
>ダイナミッククリエイティブをクリエイティブライブラリに追加する前に、広告テンプレートの作成、アセットのアップロード、（dynamic HTML5 広告）フィードテンプレートとカタログの作成など、他の手順を実行する必要があります。 「[ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)」を参照してください。

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

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. ライブラリ名をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、**[!UICONTROL Create]**/**[!UICONTROL Creatives]**/**[!UICONTROL Dynamic Ad]** をクリックします。

1. [ 動的広告設定 ](/help/creative/creative-libraries/creative-settings-dynamic.md) を指定します。

   1. 広告の基本詳細を指定します。

   1. クリエイティブに使用する広告テンプレートを選択します。

   1. 広告を作成するカタログを選択します。

   1. カタログ行で広告の作成に使用する条件を選択します。

   1. 指定した広告テンプレートの各属性（動的広告フィールド）を、指定したフィードファイル（カタログラベル）の列にマッピングします。

   1. 「**[!UICONTROL Continue]**」をクリックして、生成するクリエイティブをプレビューします。

      特定のクリエイティブをプレビューするには、行のチェックボックスをオンにします。 必要に応じて、カタログ、フィルター値 <!-- explain more--> 広告サイズでクリエイティブをフィルタリングします。

1. クリエイティブを保存します。

   * 広告を保存してライブラリの [ クリエイティブバンドル ](/help/creative/creative-libraries/bundle-manage.md) に追加するには：

      1. 「**[!UICONTROL Save and Attach to Bundle]**」をクリックします。

      1. 「**[!UICONTROL Save]**」をクリックして、広告を保存します。

      1. バンドルを選択し、「選 **[!UICONTROL Attach Creative to Bundles]**」をクリックします。

   * 広告を保存して設定を終了するには、[**[!UICONTROL Save]**] をクリックし、もう一度 [**[!UICONTROL Save]**] をクリックします。

>[!MORELIKETHIS]
>
>* [ 動的クリエイティブ設定 ](creative-settings-dynamic.md)
>* [ クリエイティブライブラリでの動的クリエイティブの編集 ](creative-edit-dynamic.md)
>* [ 動的広告のワークフロー ](/help/creative/introduction/workflow-dynamic-ads.md)
