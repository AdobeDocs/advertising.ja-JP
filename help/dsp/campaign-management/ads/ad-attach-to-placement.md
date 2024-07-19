---
title: プレースメントに広告を添付
description: プレースメントに広告を添付する方法を説明します。
feature: DSP Ads
exl-id: bca590c9-e0d0-41e6-96b1-26ea5b2f842f
source-git-commit: 86acfaecdf761adc7c6585a49dbcdf4490290a8c
workflow-type: tm+mt
source-wordcount: '901'
ht-degree: 0%

---

# プレースメントに広告を添付

[!UICONTROL Ad Tools] ビューを使用して、プレースメントに広告を添付し、広告にサードパーティのトラッキングピクセルを添付し、広告から既存のサードパーティのトラッキングピクセルを分離します。

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオプレースメントにのみ添付できます。

## [!UICONTROL Ad Tools] ビューを開く {#ad-tools-open}

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. 次のいずれかの方法で [!UICONTROL Ad Tools] ビューを開きます。

   * （[!UICONTROL Packages]、[!UICONTROL Placements] または [!UICONTROL Ads] ビューから）右上の **[!UICONTROL ...]**/**[!UICONTROL Ad Tools]** をクリックします。

   * （[!UICONTROL Placements] ビューから）プレースメント名の横にある **[!UICONTROL ...]** > **[!UICONTROL Attach Ads]をクリックします。**

   * （[!UICONTROL Ads] ビューから）広告名の横で、**[!UICONTROL ...]**/**[!UICONTROL Add to Placements]** をクリックします。

   「[!UICONTROL Attach Ads]」タブがデフォルトで選択されています。

## プレースメントに広告を添付 {#attach-ads-campaign}

1. [[!UICONTROL Ad Tools] ビューを開きます ](#ad-tools-open)。

1. [!UICONTROL Edit] サブビューで、プレースメントに添付する広告のグループごとに次の操作を行います。

   1. （任意）次のいずれかの方法で、特定のプレースメントおよび広告を見つけます。

      * 左側のテーブルの上にある ![ フィルター ](/help/dsp/assets/filter.png) をクリックして、パッケージ、プレースメントのタイプ、プレースメントのステータス、広告のタイプ、広告のステータスでリストをフィルタリングします。

      * 左右のテーブルの上で、プレースメント名と広告名に含まれる特定のテキスト文字列を検索します。

   1. 左側のテーブルで、広告を添付する各配置の横にあるチェックボックスをオンにします。

   1. 右側のテーブルで、選択した配置に添付する各広告の横にあるチェックボックスを選択します。

      プレースメントタイプに適用可能で、選択したプレースメントにまだ添付されていない広告のみを選択できます。

   1. 右下の [**[!UICONTROL Attach]**] をクリックします。

1. （任意）キャンペーンの詳細ビューに戻るには、[!UICONTROL Ad Tools] の左側にある ![ フォルダーに戻る ](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る ") をクリックし、キャンペーン名を選択します。

## プレースメントに添付された広告を表示 {#view-ads-campaign}

<!-- should be a separate page, combined with "List the Placements Associated with an Ad" (although that pertains to a single ad only), or maybe just rename this topic -->

1. [[!UICONTROL Ad Tools] ビューを開きます ](#ad-tools-open)。

1. 右上の「**[!UICONTROL View]**」オプションに切り替えます。

1. （オプション）必要に応じて、特定のプレースメントと広告を見つけます。

   * 左側のテーブルの上にある ![ フィルター ](/help/dsp/assets/filter.png) をクリックして、パッケージ、プレースメントのタイプ、プレースメントのステータス、広告のタイプ、広告のステータスでリストをフィルタリングします。

   * 左右のテーブルで、プレースメントまたは広告名に含まれる特定のテキスト文字列を検索します。

1. 左側のテーブルの任意の配置行をクリックして、右側のテーブルに添付された広告を表示します。

1. （任意）キャンペーンのプレースメントにさらに広告を添付するには、右上の **[!UICONTROL Edit]** ビューに切り替えます。 手順については、前の手順の手順 2 「[ プレースメントに広告を添付 ](#attach-ads-campaign)」を参照してください。

## プレースメントの広告にサードパーティのトラッキングピクセルを添付 {#attach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます ](#ad-tools-open)。

1. 「**[!UICONTROL Attach Pixels]**」タブをクリックします。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティのピクセルを見つけます。

      * 左側のテーブルの上にある「![ フィルター ](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

      * 左右のテーブルの上で、広告名とピクセル名に含まれる特定のテキスト文字列を検索します。

   1. （キャンペーンにサードパーティのトラッキングピクセルが存在しない場合）ピクセルを作成します。

      1. 右側のテーブルで、「**[!UICONTROL Create pixel]**」をクリックします。

      1. 次の設定を指定します。

         **[!UICONTROL Integration Event]:** *[!UICONTROL Impression]* や *[!UICONTROL Click-through]* など、実行するピクセルをトリガーするイベント。

         **[!UICONTROL Pixel Type]:** ピクセルが *[!UICONTROL IMG URL]* （1x1 ピクセルの画像ファイル）、*[!UICONTROL HTML]*、*[!UICONTROL JavaScript URL]* のどれであるかを示します。

         **[!UICONTROL Pixel URL or Code]:** ピクセル画像の URL。指定したピクセルタイプに適した形式です。

         **[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを識別しやすい名前を使用します。

         **[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]* または *[!UICONTROL IAS]*。

      1. 「**[!UICONTROL Save]**」をクリックします。

   1. 左側の表で、サードパーティのトラッキングピクセルを添付する各広告の横にあるチェックボックスを選択します。

   1. 右側の表で、選択した広告に添付する各サードパーティトラッキングピクセルの横にあるチェックボックスを選択します。

      選択した広告にまだ関連付けられていないピクセルのみを選択できます。

   1. 右下の [**[!UICONTROL Attach]**] をクリックします。

1. （任意）キャンペーンの詳細ビューに戻るには、[!UICONTROL Ad Tools] の左側にある ![ フォルダーに戻る ](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る ") をクリックし、キャンペーン名を選択します。

## プレースメントの広告からサードパーティのトラッキングピクセルを分離 {#detach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます ](#ad-tools-open)。

1. 「**[!UICONTROL Attach Pixels]**」タブをクリックします。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティのピクセルを見つけます。

      * 左側のテーブルの上にある「![ フィルター ](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

      * 左右のテーブルの上で、広告名とピクセル名に含まれる特定のテキスト文字列を検索します。

   1. 左側の表で、サードパーティのトラッキングピクセルを分離する各広告の横にあるチェックボックスを選択します。

   1. 右側の表で、選択した広告から分離する各サードパーティトラッキングピクセルの横にあるチェックボックスを選択します。

      選択したすべての広告に関連付けられているピクセルのみを選択できます。

   1. 右下の [**[!UICONTROL Detach]**] をクリックします。

1. （任意）キャンペーンの詳細ビューに戻るには、[!UICONTROL Ad Tools] の左側にある ![ フォルダーに戻る ](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る ") をクリックし、キャンペーン名を選択します。

## 広告に添付されたピクセルを表示 {#view-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます ](#ad-tools-open)。

1. 「**[!UICONTROL Attach Pixels]**」タブをクリックします。

1. 右上の「**[!UICONTROL View]**」オプションに切り替えます。

1. （オプション）必要に応じて、広告とサードパーティのピクセルを見つけます。

   * 左側のテーブルの上にある「![ フィルター ](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

   * 左右のテーブルの上で、広告名とピクセル名に含まれる特定のテキスト文字列を検索します。

1. 左側の表の任意の広告行をクリックして、右側の表に添付されているピクセルを確認します。

1. （オプション）広告にピクセルを追加するには、右上の **[!UICONTROL Edit]** ビューに切り替えます。 手順については、前の手順「[ プレースメントの広告にサードパーティのトラッキングピクセルを添付する ](#attach-pixels-ads)」の手順 3 を参照してください。

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ 複数のサードパーティ広告の作成 ](ad-create-multiple.md)
>* [ 広告の編集 ](ad-edit.md)
>* [ 広告に関連付けられたプレースメントのリスト ](ad-list-placements.md)
>* [ プレースメントの広告スケジュールの編集 ](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [ ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
