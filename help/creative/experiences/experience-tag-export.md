---
title: ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装
description: 広告エクスペリエンスタグをエクスポートし、オプションでAdvertising DSP キャンペーンにアップロードする方法を説明します。
feature: Creative Experiences
exl-id: 4ae05142-8319-4329-96d7-f87d77f02745
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '635'
ht-degree: 0%

---

# ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装

特定のクリエイティブサイズまたはビデオ期間の広告タグが [ ライブ ](experience-about.md#experience-statuses) エクスペリエンスで使用可能になったら、JavaScript、iframe およびビデオ形式でタグを生成してコピーし、Advertising DSPまたは他の DSP に実装できます。 DSPのタグには、DSPに必要なすべてのマクロが含まれます。

Advertising DSPを使用する広告主は、オプションで、広告タイプが「標準ディスプレイ」または「ユニバーサルビデオ」の広告として、タグをAdvertising DSP キャンペーンに直接アップロードできます。

>[!NOTE]
>
>* デシジョンツリーのターゲット設定でエクスペリエンスを作成すると、該当す [!DNL Creative] クリエイティブサイズ（非ビデオクリエイティブ）またはビデオデュレーション（ビデオクリエイティブ）ごとに自動的に広告タグが作成されます。
>* デシジョンツリーのターゲット設定を使用せずにエクスペリエンスを作成する場合は、該当するクリエイティブサイズ（非ビデオクリエイティブ）またはビデオデュレーション（ビデオクリエイティブ）ごとに [ 手動で広告タグを作成 ](experience-tag-create-manually.md) する必要があります。
>* エクスペリエンスタグは動的です。 エクスペリエンスを編集する場合、タグを更新する必要はありません。
>* 広告エクスペリエンスを実装するキャンペーンに、エクスペリエンスと互換性のあるターゲティングが含まれていることを確認してください。 階層ターゲティングの動作は、DSPによって異なる場合があります。 Advertising DSPでは、広告レベルのターゲティングは、プレースメントレベルのターゲティングの上（ではなく）に適用されます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。<!-- I see multiselect, but it's not actually working for me as of 2/3 so I don't know how exporting multiple tags works.-->

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、![ 広告タグの書き出し ](/help/creative/assets/export.png " 広告タグの書き出し ")**[!UICONTROL Export ad tags]** または&#x200B;**[!UICONTROL ... More] > &#x200B;** [!UICONTROL Export ad tags]** のいずれかをクリックします。

>[!NOTE]
>
>標準のビデオ広告エクスペリエンスの場合は、[!UICONTROL Tag Status] 列に「[!UICONTROL Ready]」が表示されるまで待ちます。これは、エクスペリエンス内のすべてのビデオがトランスコードされたことを示します。 すべてのビデオクリエイティブは、DSPによって自動的にトランスコードされますが、任意のビデオ広告エクスペリエンスタグに対して [ 別のDSP用のトランスコード ](experience-tag-video-transcoding.md) をオプションで適用することもできます。

<!-- Tag Manager has only a list view, but no card view, as of 2/2. -->

1. （オプション）「[!UICONTROL Macros]」タブで、タグに含めるカスタムマクロを最大 5 つ指定します。 含めるマクロごとに、次の操作を行います。

   1. チェックボックスをオンにします。<!-- Explain more -->

   1. カスタムマクロを入力します。<!-- Explain more -->

1. 右上の「**[!UICONTROL Next]**」をクリックするか、左側のメニューの「**[!UICONTROL Generate ad tags]**」をクリックします。

1. タグタイプを選択します。

   * （ビデオ以外のエクスペリエンス） **&#x200B; *JavaScript* &#x200B;** または **&#x200B; *Iframe* &#x200B;**。

   * （ビデオエクスペリエンス）***ビデオ***。

1. [!UICONTROL Destinations] リストで、エクスペリエンスの広告を作成する場所を選択します。

   * *汎用：* 他の DSP で作成する広告の場合。 **メモ：** 必要に応じて、手動で [ 追加マクロ ](/help/creative/creative-macros.md) を含める必要がある場合があります。

   * *Adobe AdCloud:* 広告の場合は、Advertising DSPで作成します。

   * *Google CM360:* 広告については、[!DNL Google Campaign Manager 360] で作成します。 **メモ：** 必要に応じて、手動で [ 追加マクロ ](/help/creative/creative-macros.md) を含める必要がある場合があります。

1. 「**[!UICONTROL Generate tags]**」をクリックします。

1. タグをコピーまたはダウンロードします。

   * 1 つの広告サイズ（非ビデオ広告）またはデュレーション（ビデオ広告）のタグをコピーするには、タグ行を展開し、行の上にカーソルを置いて ![ コピー ](/help/creative/assets/copy.png " コピー ") **[!UICONTROL Copy]** をクリックします。<!-- why diff than "Copy to clipboard icon used to copy macros for creatives? -->

   * 生成されたすべてのタグをファイルとしてブラウザーのデフォルトのダウンロード場所にダウンロードするには、「![ タグをダウンロード ](/help/creative/assets/download.png " タグをダウンロード ")」をクリックします。

   ファイルをテキストエディターで開いて、各タグをコピーできます。 JavaScript タグの場合、タグは `<script></script>` および `<noscript></noscript>`tags で囲まれます。 iframe タグの場合、タグは `<iframe></iframe>` タグで囲まれます。

1. 関連するDSPのタグを実装します。

   * Advertising DSP以外の DSP の場合は、DSP内で広告を作成するユーザーにタグを提供します。

   * Advertising DSP用：

      1. 右上の「**[!UICONTROL Next]**」をクリックするか、左側のメニューの「**[!UICONTROL DSP link]**」をクリックします。

      1. 広告タグをアップロードするキャンペーンを選択します。

      1. 「**[!UICONTROL Assign Tags]**」をクリックします。

         DSPが開き、選択したキャンペーンの [!UICONTROL Ads] ビューが表示されます。

      1. [!UICONTROL Create ads] ビューで、広告タグを確認し、広告を作成する各タグを選択して、[**[!UICONTROL Create]**] をクリックします。

<!-- no way to get back to the Creative Tag Manager -- you have to click back through the main menu -->

<!-- Add this info, with descriptions:

## Ad tag formats

### JavaScript

### Iframe

-->

>[!MORELIKETHIS]
>
>* [ 該当するクリエイティブサイズの広告タグを手動で作成 ](experience-tag-create-manually.md)
>* [ ターゲティングを行わないエクスペリエンスの広告タグへのクリエイティブの割り当て ](experience-tag-assign-creatives.md)
>* [ 広告タグの名前を変更 ](experience-tag-rename.md)
>* [ ビデオ広告エクスペリエンスタグのトランスコーディングオプションのカスタマイズ ](experience-tag-video-transcoding.md)
