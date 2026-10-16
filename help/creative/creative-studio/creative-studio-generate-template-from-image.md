---
title: AIを利用して、画像から広告テンプレートを生成
description: Creative StudioのAIを使用して、既存の静的ディスプレイ広告の画像を編集可能な広告テンプレートに変換する方法を説明します。
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: adc2fdc93f06b5459c19b08306d1e30ce00e7028
workflow-type: tm+mt
source-wordcount: '399'
ht-degree: 0%
---
# AIを利用して、画像から広告テンプレートを生成

*Beta機能*

[!UICONTROL Creative Studio]のAIを使用して、既存の静的ディスプレイ広告イメージを編集可能なディスプレイ広告テンプレートに変換します。 生成されたテンプレートを確認し、自然言語を使用して変更をリクエストし、テンプレートエディターを開いて手作業で変更し、テンプレートを保存します。

## 始める前に

Creative ライブラリに既存の静止画像の広告が必要です。 このワークフローでは、ライブラリから広告を選択します。生成ダイアログに新しい画像を直接アップロードすることはありません。

## テンプレートの生成とレビュー {#template-generate}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Templates]**」タブをクリックします。

1. （オプション）ページ上部の広告主リストから広告主を選択して、その広告主のライブラリを表示します。

1. **[!UICONTROL Use AI to Generate a New Display Ad Template]** ボックスで、**[!UICONTROL Generate]**&#x200B;をクリックします。

1. **[!UICONTROL Generate New Ad Template]** ダイアログで、まだ選択されていない場合は&#x200B;**[!UICONTROL Generate from Existing Standard Ad Image]**&#x200B;を選択します。

1. **[!UICONTROL Ad Library]** リストから画像広告を含むライブラリを選択します。

1. 画像の広告カードにカーソルを合わせ、**[!UICONTROL Use this Standard Ad]**&#x200B;をクリックします。

   選択した広告の幅と高さを使用して、生成が自動的に開始されます。

1. 生成が完了するのを待ってから、テンプレートのプレビューと&#x200B;**[!UICONTROL Layers]** パネルが利用可能な場合は確認します。

   テンプレートを使用する前に、テキスト、画像、レイアウトを確認します。 ここに示すレイヤーはレビュー用です。テンプレートエディターで手動で変更します。

1. （オプション）生成されたテンプレートへの変更をリクエストします。

   1. 「**[!UICONTROL Ask the AI for any changes]**」フィールドに、必要な変更を記述します。 例えば、`Change the headline to "Limited Time Offer" and the button text to "Shop Now"`と入力します。

   1. **[!UICONTROL Regenerate]**&#x200B;をクリックします。

   1. 更新されたプレビューを確認します。 必要に応じて繰り返します。

1. 続行する準備ができたら、**[!UICONTROL Use this Ad Template]**&#x200B;をクリックします。

   生成されたテンプレートが表示テンプレートエディターで開きます。

## テンプレートの編集と保存 {#template-save}

1. テンプレートエディターで、生成された要素を確認し、[ テンプレートエディターコントロール ](creative-studio-manage-templates.md#template-controls)を使用して残りの変更を行います。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. **[!UICONTROL Update Template]** ダイアログで、**[!UICONTROL Template name]**&#x200B;を入力または更新し、**[!UICONTROL Advertiser]**&#x200B;を選択し、オプションでタグを追加します。

1. **[!UICONTROL Update]**&#x200B;をクリックしてテンプレートを保存し、**[!UICONTROL Templates]** ビューに戻ります。

   別のコピーを保存するには、**[!UICONTROL Save As New]**&#x200B;をクリックします。

その後、テンプレートを使用して[広告バリエーションを生成](creative-studio-manage-templates.md#ad-variations-generate)できます。

## Adobe Experience Manager Sitesで {#troubleshooting}

* **ライブラリまたは画像広告が一覧表示されていません：**&#x200B;選択した広告主と&#x200B;**[!UICONTROL Ad Library]**&#x200B;を確認してください。 ライブラリに標準広告画像がない場合は、既存の静的画像広告を含む別のライブラリを選択します。

* **生成が失敗するか、画像を変換できません：**&#x200B;表示されたメッセージを確認し、**[!UICONTROL Back to library]**&#x200B;をクリックして、画像広告を選択し、再試行してください。

>[!MORELIKETHIS]
>
>* [Creative Studioで広告テンプレートを管理](creative-studio-manage-templates.md)
>* [Creative Studioで標準広告を管理](creative-studio-manage-standard-ads.md)