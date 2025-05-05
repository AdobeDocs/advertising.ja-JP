---
title: 複数のサードパーティ広告の作成
description: 一度に複数のサードパーティ広告を作成する方法を説明します。
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '390'
ht-degree: 0%

---

# 複数のサードパーティ広告の作成

サードパーティの広告サーバーでホストされているクリエイティブアセットを指すタグをアップロードすることで、一度に最大 500 個のサードパーティ広告を作成できます。 広告にトラッキングピクセルを含めることができます。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

[!DNL DoubleClick] および [!DNL Flashtalking] のタグシート、または提供されたテンプレートを使用して手動で入力されたファイルをアップロードできます。

>[!TIP]
>
> ベストプラクティスは、HTTPS を使用して安全に提供されるサードパーティの広告を使用することです。 HTTPS を使用して提供される URL は、「https」で始まります。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. 広告を含めるキャンペーンの名前をクリックします。

1. データ テーブルの上にある [**[!UICONTROL Create]**] をクリックします。 メニューの「広告タイプ」セクションで、「**[!UICONTROL Bulk upload ads]**」をクリックします。

1. 広告がホストされている広告サーバー（*[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*、*[!UICONTROL Other]*）を選択します。

1. （[!DNL DoubleClick] および [!DNL Flashtalking] 広告）各ビデオアセットと各ディスプレイアセットに使用するタグタイプを選択します。 使用できるオプションは、広告サーバーによって異なります。

1. （[!DNL DoubleClick] と [!DNL Flashtalking] を除くすべての広告サーバーの広告）「**[!UICONTROL Download this template]**」をクリックして、スプレッドシート（XLSX）形式のテンプレート [!DNL Microsoft Excel] ダウンロードします。このテンプレートには、広告データを入力し、ローカルに保存できます。 必須の列には、[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]、[!UICONTROL Ad Types] が含まれます。

1. 「**[!UICONTROL Upload]**」をクリックし、デバイスまたはネットワークから.xlsx または.xls 形式のファイルを選択します。

   [!DNL DoubleClick] および [!DNL Flashtalking] の広告については、編集されていないタグシートを広告サーバーからアップロードします。 他の広告サーバーの場合は、手順 3 でダウンロードしたテンプレートを使用します。

1. アップロードが完了したら、「**[!UICONTROL Start Building Ads]**」をクリックします。

1. 各広告の詳細とステータスを確認します。

   1. （[!DNL Google] または [!DNL Flashtalking] タグを使用したユニバーサルビデオ広告）「**[!UICONTROL Ad Type]**」フィールドをクリックし、「**[!UICONTROL Universal Video]**」を選択します。

   1. （ユニバーサルビデオ広告）新しい広告ごとに ![ 編集 ](/help/dsp/assets/edit.png) をクリックし、[ 該当するビデオ形式 ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) を選択して **保存** をクリックします。

   1. アップロードされたタグの検証チェックに基づいて、各広告のステータスを確認します。

   1. （オプション）各広告に対して次のいずれかの操作をおこないます。

      * 広告をプレビューするには、広告行にある ![ 再生 ](/help/dsp/assets/play.png) をクリックします。

      * 広告の詳細を編集するには、[![ 編集 ](/help/dsp/assets/edit.png)] をクリックし、詳細を編集して、[**保存**] をクリックします。

      * 広告を削除するには、広告行の **[!UICONTROL X]** をクリックします。

1. **[!UICONTROL Create *N *Ad （s）]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 「**[!UICONTROL Done]**」をクリックします。

   * （広告が却下された場合のオプション）広告レコードを編集して広告をレビュー用に再送信するには：

      1. 広告名をクリックします。

      1. 広告設定を編集します。

      1. 「**[!UICONTROL Save & submit for review]**」をクリックします。

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオプレースメントにのみ添付できます。

>[!MORELIKETHIS]
>
>* [Ad Management について ](ad-about.md)
>* [ 広告仕様 ](ad-specs.md)
>* [ 単一の広告の作成 ](ad-create.md)
>* [ ビデオ：サードパーティの広告タグを一括アップロードする方法 ](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html?lang=ja)
>* [ ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
