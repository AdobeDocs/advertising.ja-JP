---
title: クリエイティブライブラリでの標準クリエイティブの編集
description: クリエイティブライブラリで標準（非ダイナミック）クリエイティブの設定を変更する方法を説明します。
feature: Creative Standard Creatives
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# クリエイティブライブラリでの標準クリエイティブの編集

*クローズドベータ版*

標準クリエイティブのタイプごとに、いくつかの設定を編集できます。 同じクリエイティブタイプの複数のクリエイティブ（ランディングページが 1 つだけのシンプルなHTML5、複数のランディングページがある静的HTML5、フレキシブルHTML5、画像、サードパーティ <!-- , or dynamic -->）の <!-- or creative variations --> のみを編集できます。

フレキシブルHTML5 と静的HTML5 のクリエイティブの場合、レイアウトは異なるものの属性名が同じ新しいテンプレートファイルをアップロードできます。 シンプルなHTML5 のクリエイティブの場合、新しい属性または画像を含む新しいテンプレートをアップロードすることで、任意の属性を編集したり、画像を追加したりできます。 すべての場合、テンプレートは、最大 2 MB の ZIP 形式のローカルファイルである必要があります。

バンドルに含まれるクリエイティブ <!-- or creative variation --> ージを編集すると、変更内容はバンドルを含むすべてのエクスペリエンスに自動的に適用されます。ただし、エクスペリエンスレベルで指定されたカスタムランディングページとトラッキング URL は、そのエクスペリエンスに添付されたバンドルにも引き続き適用されます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Libraries]** をクリックします。

1. （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のライブラリを含めます。

1. ライブラリ名をクリックします。

1. **[!UICONTROL Creatives]** / **[!UICONTROL Standard Ads]** タブで、クリエイティブを選択します。

   * （任意） [ ビューをカスタマイズ ](/help/creative/introduction/customize-data-views.md) して、特定のクリエイティブを含めます。

   * 単一のクリエイティブを編集するには：

      * カード表示で、クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Edit]**」をクリックします。

      * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL Edit]** をクリックします。

   * 1 つ以上のクリエイティブを編集するには、編集する各クリエイティブのチェックボックスをオンにします。 一括アクションツールバーで、「**[!UICONTROL Edit]**」をクリックします。

     すべての行を選択するには、左上の「グローバル」チェック・ボックスを選択します。

1. [ 画像クリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-image)、[HTML5 クリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-html5)、[ フレキシブルHTML5 クリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-flexible-html5) または [ サードパーティクリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md#creative-settings-third-party) を編集します。<!-- , or [dynamic creative settings](/help/creative/creative-libraries/creative-settings-dynamic.md) -->

   複数のクリエイティブを同時に編集する場合：

   * 各クリエイティブの設定は、同時にまたは個別に編集できます。 デフォルトでは、選択したすべてのクリエイティブが選択され、指定した設定は選択したすべてのクリエイティブに適用されます。 特定のクリエイティブの設定を編集するには、フィールドを編集する前に、適用できない各クリエイティブの選択を解除します。必要に応じて、追加のクリエイティブに対して繰り返します。

   * 一部の設定は、選択したすべてのクリエイティブに適用されます。

   >[!NOTE]
   >
   >* （フレキシブルHTML5 のクリエイティブのみ） 1 つのクリエイティブの属性のみを編集できます。<!-- Also, when you update the template for a parent creative with child variations, the variations are updated with any changes to the template layout, but the attribute values for the variation aren't changed. -->

<!-- Not there as of 1/16/25. If we do add it, verify the applicable ad types:   
1. (Flexible HTML5 [or third-party should be possible, but not so] creatives; optional) Once you've made your changes, click ![]() to preview the new creative. 
-->

1. **保存** をクリックします。

<!-- Not there as of 1/16/25. If we do add it, add back in:
1. (Flexible HTML5 or third-party creatives; optional) Regenerate the thumbnail within the table view or cards view if the change isn't visible immediately.
-->

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリへの標準クリエイティブの追加 ](creative-add-standard.md)
>* [ 標準のクリエイティブ設定 ](/help/creative/creative-libraries/creative-settings-standard.md)
>* [ クリエイティブのプレビュー ](/help/creative/creative-libraries/creative-preview.md)
>* [ 重複クリエイティブ ](/help/creative/creative-libraries/creative-duplicate.md)
>* [ クリエイティブを削除 ](/help/creative/creative-libraries/creative-delete.md)
