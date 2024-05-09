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

次のいずれかをアップロードできます [!DNL DoubleClick] および [!DNL Flashtalking] 提供されたテンプレートを使用して、シートまたは手動で入力されたファイルにタグを付けます。

>[!TIP]
>
> ベストプラクティスは、HTTPS を使用して安全に提供されるサードパーティの広告を使用することです。 HTTPS を使用して提供される URL は、「https」で始まります。

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. 広告を含めるキャンペーンの名前をクリックします。

1. データ テーブルの上で、 **[!UICONTROL Create]**. メニューの「広告タイプ」セクションで、 **[!UICONTROL Bulk upload ads]**.

1. 広告がホストされている広告サーバーを選択： *[!UICONTROL DoubleClick]*, *[!UICONTROL Flashtalking]*、または *[!UICONTROL Other]*.

1. （[!DNL DoubleClick] および [!DNL Flashtalking] 広告）各ビデオアセットと各ディスプレイアセットに使用するタグタイプを選択します。 使用できるオプションは、広告サーバーによって異なります。

1. （を除くすべての広告サーバーの広告 [!DNL DoubleClick] および [!DNL Flashtalking]） クリック **[!UICONTROL Download this template]** でテンプレートをダウンロードするには [!DNL Microsoft Excel] 広告データを入力してローカルに保存できるスプレッドシート（XLSX）形式。 必須の列は次のとおりです [!UICONTROL Ad Name], [!UICONTROL VAST/VPAID URL or Ad Tag]、および [!UICONTROL Ad Types].

1. クリック **[!UICONTROL Upload]** さらに、デバイスまたはネットワークから.xlsx 形式または.xls 形式のファイルを選択します。

   の場合 [!DNL DoubleClick] および [!DNL Flashtalking] 件の広告をアップロードし、広告サーバーから編集されていないタグシートをアップロードします。 他の広告サーバーの場合は、手順 3 でダウンロードしたテンプレートを使用します。

1. アップロードが完了したら、 **[!UICONTROL Start Building Ads]**.

1. 各広告の詳細とステータスを確認します。

   1. （を使用したユニバーサルビデオ広告 [!DNL Google] または [!DNL Flashtalking] タグ）をクリックします **[!UICONTROL Ad Type]** フィールドと選択 **[!UICONTROL Universal Video]**.

   1. （ユニバーサルビデオ広告）新しい広告ごとに、 ![編集](/help/dsp/assets/edit.png)を選択し、 [適用可能なビデオ形式](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)を選択し、 **保存**.

   1. アップロードされたタグの検証チェックに基づいて、各広告のステータスを確認します。

   1. （オプション）各広告に対して次のいずれかの操作をおこないます。

      * 広告をプレビューするには、をクリックします。 ![play](/help/dsp/assets/play.png) 広告行

      * 広告の詳細を編集するには、 ![編集](/help/dsp/assets/edit.png)を選択し、詳細を編集して、 **保存**.

      * 広告を削除するには、をクリックします **[!UICONTROL X]** 広告行

1. クリック **[!UICONTROL Create *N *広告]**.

1. 次のいずれかの操作を行います。

   * クリック **[!UICONTROL Done]**.

   * （広告が却下された場合のオプション）広告レコードを編集して広告をレビュー用に再送信するには：

      1. 広告名をクリックします。

      1. 広告設定を編集します。

      1. クリック **[!UICONTROL Save & submit for review]**.

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオプレースメントにのみ添付できます。

>[!MORELIKETHIS]
>
>* [Ad Management について](ad-about.md)
>* [広告仕様](ad-specs.md)
>* [単一の広告を作成](ad-create.md)
>* [ビデオ：サードパーティの広告タグを一括アップロードする方法](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html)
>* [ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
