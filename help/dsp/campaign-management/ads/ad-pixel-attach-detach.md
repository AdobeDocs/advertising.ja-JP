---
title: 広告からのピクセルの添付と削除
description: 広告にサードパーティのトラッキングピクセルを追加および削除する方法を説明します。
feature: DSP Ads
source-git-commit: a3bd04da6c6f428fdb6e1f05187ea3de0174c9d7
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 0%

---

# 広告からのピクセルの添付と削除

広告にサードパーティのトラッキングピクセルを追加したり、広告から外したりできます。

## [!UICONTROL Ad Tools] ビューを開く {#ad-tools-open}

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. 次のいずれかの方法で [!UICONTROL Ad Tools] ビューを開きます。

   * （[!UICONTROL Campaigns] ビューで）キャンペーン名の横の **[!UICONTROL ...]**/**[!UICONTROL Ad Tools]をクリックします。**

   * （[!UICONTROL Packages]、[!UICONTROL Placements] または [!UICONTROL Ads] ビューから）右上の **[!UICONTROL ...]**/**[!UICONTROL Ad Tools]** をクリックします。

## プレースメントの広告にサードパーティのトラッキングピクセルを添付 {#attach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます &#x200B;](#ad-tools-open)。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティのピクセルを見つけます。

      * 左側のテーブルの上にある「![&#x200B; フィルター &#x200B;](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

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

1. （任意）キャンペーンの詳細ビューに戻るには、![&#x200B; の左側にある &#x200B;](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る ") フォルダーに戻る [!UICONTROL Ad Tools] をクリックし、キャンペーン名を選択します。

## プレースメントの広告からサードパーティのトラッキングピクセルを分離 {#detach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます &#x200B;](#ad-tools-open)。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティのピクセルを見つけます。

      * 左側のテーブルの上にある「![&#x200B; フィルター &#x200B;](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

      * 左右のテーブルの上で、広告名とピクセル名に含まれる特定のテキスト文字列を検索します。

   1. 左側の表で、サードパーティのトラッキングピクセルを分離する各広告の横にあるチェックボックスを選択します。

   1. 右側の表で、選択した広告から分離する各サードパーティトラッキングピクセルの横にあるチェックボックスを選択します。

      選択したすべての広告に関連付けられているピクセルのみを選択できます。

   1. 右下の [**[!UICONTROL Detach]**] をクリックします。

1. （任意）キャンペーンの詳細ビューに戻るには、![&#x200B; の左側にある &#x200B;](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る ") フォルダーに戻る [!UICONTROL Ad Tools] をクリックし、キャンペーン名を選択します。

## 広告に添付されたピクセルを表示 {#view-pixels-ads}

1. [[!UICONTROL Ad Tools] ビューを開きます &#x200B;](#ad-tools-open)。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. 右上の「**[!UICONTROL View]**」オプションに切り替えます。

1. （オプション）必要に応じて、広告とサードパーティのピクセルを見つけます。

   * 左側のテーブルの上にある「![&#x200B; フィルター &#x200B;](/help/dsp/assets/filter.png)」をクリックし、広告ステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

   * 左右のテーブルの上で、広告名とピクセル名に含まれる特定のテキスト文字列を検索します。

1. 左側の表の任意の広告行をクリックして、右側の表に添付されているピクセルを確認します。

1. （オプション）広告にピクセルを追加するには、右上の **[!UICONTROL Edit]** ビューに切り替えます。 手順については、前の手順「[&#x200B; プレースメントの広告にサードパーティのトラッキングピクセルを添付する &#x200B;](#attach-pixels-ads)」の手順 3 を参照してください。

>[!MORELIKETHIS]
>
>* [Ad Management について &#x200B;](ad-about.md)
>* [&#x200B; プレースメントへの広告の添付 &#x200B;](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [&#x200B; 単一の広告の作成 &#x200B;](ad-create.md)
>* [&#x200B; 複数のサードパーティ広告の作成 &#x200B;](ad-create-multiple.md)
>* [&#x200B; 広告の編集 &#x200B;](ad-edit.md)
>* [&#x200B; 広告に関連付けられたプレースメントのリスト &#x200B;](ad-list-placements.md)
>* [&#x200B; プレースメントの広告スケジュールの編集 &#x200B;](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [&#x200B; ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)

