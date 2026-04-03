---
title: ライブ体験用の広告エクスペリエンスタグの書き出しと実装
description: 広告エクスペリエンスタグを書き出し、オプションでAdvertising DSP キャンペーンにアップロードする方法について説明します。
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
TQID: https://experienceleague.adobe.com/tge8P1-b1I21jxKui3KgSjgXCKtZCRSO94knTkWlNW0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 635
ht-degree: 0%

---

# ライブ体験用の広告エクスペリエンスタグの書き出しと実装

特定のクリエイティブサイズまたはビデオのデュレーションに対応する広告タグを[&#x200B; ライブ &#x200B;](experience-about.md#experience-statuses)体験で使用できるようになったら、そのタグをJavaScript、iframe、ビデオ形式で生成してコピーし、Advertising DSPまたはその他のDSPに実装できます。 DSPのタグには、DSPに必要なすべてのマクロが含まれています。

Advertising DSPを使用している広告主は、オプションとして、広告タイプ「標準ディスプレイ」または「ユニバーサルビデオ」を含む広告として、タグをAdvertising DSP キャンペーンに直接アップロードできます。

>[!NOTE]
>
>* 決定木ターゲティングでエクスペリエンスを作成する場合、[!DNL Creative]は、該当するクリエイティブサイズ（ビデオ以外のクリエイティブ）またはビデオのデュレーション（ビデオのクリエイティブ）ごとに自動的に広告タグを作成します。
>* 決定木ターゲティングを使用しないエクスペリエンスを作成する場合、該当するクリエイティブサイズ（ビデオ以外のクリエイター）またはビデオのデュレーション（ビデオのクリエイター）ごとに、[手動で広告タグ &#x200B;](experience-tag-create-manually.md)を作成する必要があります。
>* エクスペリエンスのタグは動的です。 エクスペリエンスを編集する場合、タグを更新する必要はありません。
>* 広告エクスペリエンスを実装するキャンペーンには、エクスペリエンスと互換性のあるターゲティングが含まれていることを確認します。 階層的なターゲティングの動作は、DSPによって異なる場合があります。 Advertising DSPでは、広告レベルのターゲティングは、プレースメントレベルのターゲティングの上に適用されます（代わりに）。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います：<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、![広告タグの書き出し](/help/creative/assets/export.png "広告タグの書き出し") **[!UICONTROL Export ad tags]**&#x200B;または&#x200B;**[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]**&#x200B;のいずれかをクリックします。

>[!NOTE]
>
>標準的なビデオ広告エクスペリエンスの場合は、[!UICONTROL Tag Status]列に「[!UICONTROL Ready]」と表示され、エクスペリエンス内のすべてのビデオがトランスコードされたことを示すまで待ちます。 すべてのビデオクリエイティブはDSPによって自動的にトランスコードされますが、オプションで[別のDSPのトランスコードを任意のビデオ広告エクスペリエンスタグに適用できます](experience-tag-video-transcoding.md)。

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. （オプション）「[!UICONTROL Macros]」タブで、タグに含めるカスタムマクロを5つまで指定します。 以下を含める各マクロについて：

   1. チェックボックスを選択します。<!-- Explain more -->

   1. カスタムマクロを入力します。<!-- Explain more -->

1. 右上の&#x200B;**[!UICONTROL Next]**&#x200B;をクリックするか、左側のメニューの&#x200B;**[!UICONTROL Generate ad tags]**&#x200B;をクリックします。

1. タグタイプを選択します。

   * （ビデオ以外のエクスペリエンス）**&#x200B; *JavaScript* &#x200B;** または&#x200B;*Iframe* **&#x200B;**&#x200B;使用できます。

   * （ビデオ エクスペリエンス） **&#x200B; *ビデオ* &#x200B;**。

1. [!UICONTROL Destinations] リストで、エクスペリエンスの広告を作成する場所を選択します。

   * *汎用：*&#x200B;他のDSPで作成する広告。 **メモ：**&#x200B;必要に応じて、[追加のマクロ &#x200B;](/help/creative/creative-macros.md)を手動で含める必要がある場合があります。

   * *Adobe AdCloud:* Advertising DSPで作成する広告の場合。

   * *Google CM360:* [!DNL Google Campaign Manager 360]で作成する広告の場合。 **メモ：**&#x200B;必要に応じて、[追加のマクロ &#x200B;](/help/creative/creative-macros.md)を手動で含める必要がある場合があります。

1. **[!UICONTROL Generate tags]**&#x200B;をクリックします。

1. タグをコピーまたはダウンロードします。

   * 1つの広告サイズ（ビデオ以外の広告）またはデュレーション（ビデオ広告）のタグをコピーするには、タグ行を展開し、行の上にカーソルを置いて、![&#x200B; コピー](/help/creative/assets/copy.png " コピー")**[!UICONTROL Copy]**&#x200B;をクリックします。<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * 生成されたすべてのタグをブラウザーのデフォルトのダウンロード場所にファイルとしてダウンロードするには、「![&#x200B; タグをダウンロード &#x200B;](/help/creative/assets/download.png " タグをダウンロード ")」をクリックします。

   テキストエディターでファイルを開いて、各タグをコピーできます。 JavaScript タグの場合、タグは`<script></script>`および`<noscript></noscript>` タグで囲まれます。 iframe タグの場合、タグは`<iframe></iframe>` タグで囲まれます。

1. 関連するDSPのタグを実装します。

   * Advertising DSP以外のDSPの場合は、DSP内で広告を制作する人全員にタグを提供します。

   * Advertising DSP用：

      1. 右上の&#x200B;**[!UICONTROL Next]**&#x200B;をクリックするか、左側のメニューの&#x200B;**[!UICONTROL DSP link]**&#x200B;をクリックします。

      1. 広告タグをアップロードするキャンペーンを選択します。

      1. **[!UICONTROL Assign Tags]**&#x200B;をクリックします。

         選択したキャンペーンの[!UICONTROL Ads] ビューがDSPで開きます。

      1. [!UICONTROL Create ads] ビューで、広告タグを確認し、広告を作成する各タグを選択して、**[!UICONTROL Create]**&#x200B;をクリックします。

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!--
 Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [該当するクリエイティブサイズの広告タグを手動で作成する](experience-tag-create-manually.md)
>* [&#x200B; ターゲティングせずにエクスペリエンス用の広告タグにクリエイターを割り当てる](experience-tag-assign-creatives.md)
>* [広告タグの名前を変更](experience-tag-rename.md)
>* [&#x200B; ビデオ広告エクスペリエンスタグのトランスコーディングオプションをカスタマイズ &#x200B;](experience-tag-video-transcoding.md)
