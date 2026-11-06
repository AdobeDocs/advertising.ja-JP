---
title: （新しいUI）目的の作成
description: 目的を作成する方法、または既存の目的を複製する方法を説明します。
feature: Search Objectives, Search Optimization
hide: true
exl-id: 21516197-d005-4703-8735-c789107dc3c4
autotag-review: '2026-04-13T23:57:03.010Z'
TQID: 'https://experienceleague.adobe.com/z6aWMsPgU5YScIkdoKILRbZhOo2PTvJBIXxcyOXybgw'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 2d3f1df6-4c6c-545b-abf7-bec5f20fd636
    internal-label: Search Objectives
  - id: ae57d55f-b168-5358-b114-c3974b1b3d77
    internal-label: Search Optimization
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
    internal-label: Admin
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
topic_v2:
  - id: c2296997-5d79-4905-b32e-99b5aa892429
    internal-label: Search optimization
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
    internal-label: Optimization
source-git-commit: 5d7cc4088d2fbb3cb8dcaf5e6c349565030a8b08
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%
---
# （新しいUI）目的の作成

<!-- Needs V2 subfeature tags for Search Objectives, Search Optimization. Right now, using cross-product topics for optimization, which I'm not sure is enough. -->

*Beta機能*

>[!NOTE]
>
>目標をポートフォリオに関連付けるには、[&#128279;](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-create.md)&#x200B; ポートフォリオを作成するか、[&#x200B; ポートフォリオ設定の変更](/help/search-social-commerce/new-ui/manage/portfolios/portfolio-edit.md)までに行います。 &#x200B;複数のポートフォリオに対して同じ目的を使用できます。

## 目標の設定

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Objectives]**&#x200B;をクリックします。

1. 右上の「**[!UICONTROL Create Objective]**」または「![追加](/help/search-social-commerce/assets/add-new.png "追加")」をクリックします。

   表示されるボタンは、ブラウザーの幅によって異なります。

1. 目的の設定を入力します。

手順については、検索、ソーシャル、およびCommerce内から入手できるユーザーインターフェイスまたは最適化ガイドのヘルプを参照してください。

1. 設定の下部にある「**[!UICONTROL Save]**」をクリックします。

Advertising DSP パッケージで使用する目的の先頭に「`ADSP_`」を付けます（大文字と小文字は区別しません）。この目的は、2日以内にDSP内のカスタム目標として使用できます。

## 目標の複製 {#objective-duplicate}

目的を複製して、同じ設定で新しい目的を作成します。 オプションで、新しい目的のデフォルト名を変更し、必要に応じて目的の設定を編集できます。 当初の目的は変わりません。

目標を複製するには、[!UICONTROL Edit Objectives]権限が必要です。 既定の[!UICONTROL Maximize Clicks] オブジェクトは複製できません。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Objectives]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 目的の行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Duplicate]**&#x200B;をクリックします。

   * 目的の横にあるチェックボックスをオンにします。 一括操作ツールバーで、![複製](/help/search-social-commerce/assets/duplicate.png "複製") **[!UICONTROL Duplicate]**&#x200B;をクリックします。

     複数の目標が選択されている場合、[!UICONTROL Duplicate]は使用できません。

1. 目的の設定を編集します。

   デフォルトでは、新しい目的名は「Revenue_Copy」など、`<original objective name>_Copy`です。 元の名前が既に`_Copy`で終わっている場合、新しい名前には「Revenue_Copy （1）」などのカウンターが含まれます。 提案された名前が既に存在する場合は、一意の&#x200B;**[!UICONTROL Name]**&#x200B;を入力します。

   手順については、検索、ソーシャル、およびCommerce内から入手できるユーザーインターフェイスまたは最適化ガイドのヘルプを参照してください。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

   警告ダイアログが表示された場合は、警告を確認し、**[!UICONTROL Save]**&#x200B;をクリックして続行します。

>[!MORELIKETHIS]
>
>* [目標について](objective-about.md)
>* [目標を編集](objective-edit.md)
>* [目標に重み付けの推奨事項を適用](objective-apply-weight-recommendations.md)
>* [目標の設定](objective-settings.md)
>* [目的の設定を書き出し](objective-export.md)
>* [目的のパフォーマンスデータをダウンロード &#x200B;](objective-download-performance-data.md)
