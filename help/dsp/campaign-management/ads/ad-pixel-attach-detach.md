---
title: 広告からのピクセルの添付と削除
description: 広告からサードパーティのトラッキングピクセルを添付および削除する方法について説明します。
feature: DSP Ads
exl-id: 7b386a58-5300-49cf-9de8-4ce982a5181d
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: c012de69-a374-5a5d-aeff-0c0f44255fd2
    internal-label: DSP Ads
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 0%
---
# 広告からのピクセルの添付と削除

広告からサードパーティのトラッキングピクセルをアタッチおよびアタッチ解除できます。

## [!UICONTROL Ad Tools] ビューを開く {#ad-tools-open}

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックします。

1. 次のいずれかの方法で[!UICONTROL Ad Tools] ビューを開きます。

   * （[!UICONTROL Campaigns] ビューから）キャンペーン名の横にある「**[!UICONTROL ...]** > **[!UICONTROL Ad Tools]」をクリックします。**

   * （[!UICONTROL Packages]、[!UICONTROL Placements]、または[!UICONTROL Ads] ビューから）右上の「**[!UICONTROL ...]**」 > 「**[!UICONTROL Ad Tools]**」をクリックします。

## プレースメント内の広告にサードパーティのトラッキングピクセルを添付する {#attach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビュー](#ad-tools-open)を開きます。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティピクセルを探します。

      * 左側のテーブルの上にある「![&#x200B; フィルター](/help/dsp/assets/filter.png)」をクリックし、広告のステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

      * 左右の表の上で、広告名とピクセル名で特定のテキスト文字列を検索します。

   1. （キャンペーンにサードパーティのトラッキングピクセルが存在しない場合）ピクセルを作成します。

      1. 右側のテーブルで、**[!UICONTROL Create pixel]**&#x200B;をクリックします。

      1. 設定を指定します。

         **[!UICONTROL Integration Event]:** *[!UICONTROL Impression]*&#x200B;や&#x200B;*[!UICONTROL Click-through]*&#x200B;など、ピクセルをトリガーするイベント。

         **[!UICONTROL Pixel Type]:** ピクセルが&#x200B;*[!UICONTROL IMG URL]* （1x1 ピクセル画像ファイル）、*[!UICONTROL HTML]*、または&#x200B;*[!UICONTROL JavaScript URL]*&#x200B;のいずれであるか。

         **[!UICONTROL Pixel URL or Code]:**&#x200B;指定したピクセルタイプに適した形式のピクセル画像のURL。

         **[!UICONTROL Pixel Name]:** ピクセル名。 ピクセルを簡単に識別できる名前を使用します。

         **[!UICONTROL Pixel Provider]:** ピクセルプロバイダー：*[!UICONTROL None]*、*[!UICONTROL Comscore]*、*[!UICONTROL WhiteOps]*、または&#x200B;*[!UICONTROL IAS]*。

      1. **[!UICONTROL Save]**&#x200B;をクリックします。

   1. 左側の表で、サードパーティのトラッキングピクセルをアタッチする各広告の横にあるチェックボックスをオンにします。

   1. 右側の表で、選択した広告に添付する各サードパーティトラッキングピクセルの横にあるチェックボックスをオンにします。

      選択した広告にまだアタッチされていないピクセルのみが選択可能です。

   1. 右下の「**[!UICONTROL Attach]**」をクリックします。

1. （オプション）キャンペーンの詳細ビューに戻るには、![&#x200B; フォルダーに戻る](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る")を[!UICONTROL Ad Tools]の左側にクリックし、キャンペーン名を選択します。

## プレースメント内の広告からサードパーティのトラッキングピクセルを切り離す {#detach-pixels-ads}

1. [[!UICONTROL Ad Tools] ビュー](#ad-tools-open)を開きます。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. [!UICONTROL Edit] サブビューで：

   1. （オプション）次のいずれかの方法で、広告とサードパーティピクセルを探します。

      * 左側のテーブルの上にある「![&#x200B; フィルター](/help/dsp/assets/filter.png)」をクリックし、広告のステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

      * 左右の表の上で、広告名とピクセル名で特定のテキスト文字列を検索します。

   1. 左側の表で、サードパーティのトラッキングピクセルを切り離す各広告の横にあるチェックボックスを選択します。

   1. 右側の表で、選択した広告から切り離す各サードパーティトラッキングピクセルの横にあるチェックボックスを選択します。

      選択したすべての広告に添付されているピクセルのみが選択可能です。

   1. 右下の「**[!UICONTROL Detach]**」をクリックします。

1. （オプション）キャンペーンの詳細ビューに戻るには、![&#x200B; フォルダーに戻る](/help/dsp/assets/breadcrumb-return.png " フォルダーに戻る")を[!UICONTROL Ad Tools]の左側にクリックし、キャンペーン名を選択します。

## 広告に添付されたピクセルを表示 {#view-pixels-ads}

1. [[!UICONTROL Ad Tools] ビュー](#ad-tools-open)を開きます。

   「**[!UICONTROL Attach Pixels]**」タブが開きます。

1. 右上の&#x200B;**[!UICONTROL View]** オプションに切り替えます。

1. （オプション）必要に応じて、広告とサードパーティのピクセルを探します。

   * 左側のテーブルの上にある「![&#x200B; フィルター](/help/dsp/assets/filter.png)」をクリックし、広告のステータス、広告タイプ、ピクセル統合イベント、ピクセルタイプでリストをフィルタリングします。

   * 左右の表の上で、広告名とピクセル名で特定のテキスト文字列を検索します。

1. 左側の表の任意の広告行をクリックすると、右側の表に添付されたピクセルが表示されます。

1. （オプション）広告にさらにピクセルを追加するには、右上の&#x200B;**[!UICONTROL Edit]** ビューに切り替えます。 手順については、前の手順「[&#x200B; プレースメント内の広告にサードパーティのトラッキングピクセルを添付](#attach-pixels-ads)」の手順3を参照してください。

>[!MORELIKETHIS]
>
>* [Advertising DSPの広告管理について](ad-about.md)
>* [広告をプレースメントに添付](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)
>* [単一の広告を作成](ad-create.md)
>* [複数のサードパーティ広告を作成](ad-create-multiple.md)
>* [広告を編集](ad-edit.md)
>* [広告に関連付けられているプレースメントを一覧表示](ad-list-placements.md)
>* [&#x200B; プレースメントの広告スケジュールを編集](/help/dsp/campaign-management/placements/placement-edit-ad-schedule.md)
>* [&#x200B; ユニバーサルビデオに関するFAQ](/help/dsp/campaign-management/faq-universal-video.md)
