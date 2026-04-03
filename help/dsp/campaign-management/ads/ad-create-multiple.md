---
title: 複数のサードパーティ広告の制作
description: 一度に複数のサードパーティ広告を作成する方法を説明します。
feature: DSP Ads
exl-id: be7c1cc4-3c17-4e37-aae7-c8601d2222a0
TQID: https://experienceleague.adobe.com/ZOJDY0mjhTFb-Kcw1hEkCaZ0ZLVYPxTcEmOj2yM2JZQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: d9510790-d834-436d-8423-8d69cd50464a
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 393
ht-degree: 0%

---

# 複数のサードパーティ広告の制作

サードパーティ広告サーバーでホストされているクリエイティブアセットを示すタグをアップロードすることで、一度に最大500個のサードパーティ広告を作成できます。 広告にトラッキングピクセルを含めることができます。<!-- The bulksheet template for other ad servers says you can include 200. Which is it: 200 or 500? -->

指定されたテンプレートを使用して、[!DNL DoubleClick]と[!DNL Flashtalking]のタグシートまたは手動入力ファイルのいずれかをアップロードできます。

>[!TIP]
>
> ベストプラクティスは、HTTPSを使用して安全に提供されるサードパーティの広告を使用することです。 HTTPSを使用して提供されるURLは、「https」で始まります。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 広告を含めるキャンペーンの名前をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。 メニューの「広告タイプ」セクションで、「**[!UICONTROL Bulk upload ads]**」をクリックします。

1. 広告がホストされている広告サーバー（*[!UICONTROL DoubleClick]*、*[!UICONTROL Flashtalking]*、または&#x200B;*[!UICONTROL Other]*）を選択します。

1. （[!DNL DoubleClick]広告と[!DNL Flashtalking]広告）各ビデオアセットと各表示アセットに使用するタグタイプを選択します。 使用可能なオプションは、広告サーバーによって異なります。

1. （広告[!DNL DoubleClick]と[!DNL Flashtalking]を除くすべての広告サーバーの広告） **[!UICONTROL Download this template]**&#x200B;をクリックして、[!DNL Microsoft Excel]のスプレッドシート （XLSX）形式でテンプレートをダウンロードします。この形式は、広告データを入力してローカルに保存できます。 必要な列には、[!UICONTROL Ad Name]、[!UICONTROL VAST/VPAID URL or Ad Tag]および[!UICONTROL Ad Types]が含まれます。

1. **[!UICONTROL Upload]**&#x200B;をクリックし、デバイスまたはネットワークから.xlsxまたは.xls形式のファイルを選択します。

   [!DNL DoubleClick]および[!DNL Flashtalking]件の広告の場合、未編集のタグシートを広告サーバーからアップロードします。 他の広告サーバーの場合は、手順3でダウンロードしたテンプレートを使用します。

1. アップロードが完了したら、**[!UICONTROL Start Building Ads]**&#x200B;をクリックします。

1. 各広告の詳細とステータスを確認します。

   1. （[!DNL Google]または[!DNL Flashtalking] タグを使用したユニバーサルビデオ広告）「**[!UICONTROL Ad Type]**」フィールドをクリックし、「**[!UICONTROL Universal Video]**」を選択します。

   1. （ユニバーサルビデオ広告）新しい広告ごとに、![編集](/help/dsp/assets/edit.png)をクリックし、[該当するビデオ形式](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)を選択して、**保存**&#x200B;をクリックします。

   1. アップロードしたタグの検証チェックにもとづいて、各広告のステータスを確認します。

   1. （オプション）各広告について、次のいずれかの操作を行います。

      * 広告をプレビューするには、広告行の![play](/help/dsp/assets/play.png)をクリックします。

      * 広告の詳細を編集するには、![編集](/help/dsp/assets/edit.png)をクリックして詳細を編集し、**保存**&#x200B;をクリックします。

      * 広告を削除するには、広告行の&#x200B;**[!UICONTROL X]**&#x200B;をクリックします。

1. **[!UICONTROL Create *N *個の広告]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * **[!UICONTROL Done]**&#x200B;をクリックします。

   * （広告が拒否された場合。オプション）広告レコードを編集し、レビュー用に広告を再送信するには、次の手順を実行します。

      1. 広告名をクリックします。

      1. 広告設定を編集します。

      1. **[!UICONTROL Save & submit for review]**&#x200B;をクリックします。

>[!NOTE]
>
>ユニバーサルビデオ広告は、ユニバーサルビデオの配置にのみ添付できます。

>[!MORELIKETHIS]
>
>* [Advertising DSPの広告管理について](ad-about.md)
>* [広告の仕様](ad-specs.md)
>* [単一の広告を作成](ad-create.md)
>* [&#x200B; ビデオ：サードパーティの広告タグを一括アップロードする方法](https://experienceleague.adobe.com/docs/advertising-learn/tutorials/dsp/bulk-upload-third-party-ad-tags.html?lang=ja)
>* [&#x200B; ユニバーサルビデオに関するFAQ](/help/dsp/campaign-management/faq-universal-video.md)
