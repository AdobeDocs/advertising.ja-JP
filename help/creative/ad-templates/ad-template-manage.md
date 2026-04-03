---
title: 動的広告テンプレートの管理
description: 動的広告テンプレートを管理し、そのテンプレートから広告を作成する方法について説明します。
feature: Creative Templates
exl-id: 248f1467-ebd3-47f2-a24c-043bbfadcc6e
TQID: https://experienceleague.adobe.com/-kYWprVYmg-AsTH-L--U08dnlESVQx-f2TYTDohc1jc
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 453
ht-degree: 0%

---

# 動的広告テンプレートの管理

必要な広告フォーマットを含む圧縮されたHTML5 ファイルをアップロードすることで、広告タイプ（静的HTML5または動的HTML5）と広告サイズの組み合わせごとに個別の広告テンプレートを作成できます。 動的なHTML5広告の場合は、広告属性<!-- more clarification? -->を含むファイルもアップロードします。

<!-- add this where/how?: You can use the same feed template for multiple ad templates. -->

<!-- EXPLAIN MORE:  Is this like repropagating a feed file through a template, or can you just change some things? Is generating an ad template a one-time thing, using the existing feed file, but you might later update the file and re-propagation doesn't happen automatically? Clarify the use cases for each.-->

## 動的広告テンプレートの作成

>[!NOTE]
>
>[動的なクリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-dynamic.md)すると、動的な広告テンプレートをアップロードすることもできます。 そこで作成した広告テンプレートは、今後の使用のために[!UICONTROL Ad Templates] ビュー内で使用できるようになります。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

1. 右上の&#x200B;**[!UICONTROL Create Ad Template]**&#x200B;をクリックします

1. [広告テンプレート設定を指定](#ad-template-settings)

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## 動的広告テンプレートの編集

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [広告テンプレート設定](#ad-template-settings)を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 動的広告テンプレートのダウンロード

<!-- Explain more about what this contains and the format:  Downloaded ad templates are compressed (zipped) files that include XXX as TDF files and the uploaded HTML5 (and attributes?) data. You can open the TDF file in a text editor. -->

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Download]**&#x200B;をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

## 動的広告テンプレートの削除

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## 広告テンプレートからの動的広告の作成

>[!NOTE]
>
>また、クリエイティブライブラリ内から[動的なクリエイティブをクリエイティブライブラリに追加](/help/creative/creative-libraries/creative-add-dynamic.md)することもできます。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Ad Templates]**&#x200B;をクリックします。

1. 広告テンプレート行の上にカーソルを置き、**[!UICONTROL Create Dynamic Ad]**&#x200B;をクリックします。

   [!UICONTROL New Dynamic Ad]画面では、[!UICONTROL Ad Template Size]、[!UICONTROL Ad Template Type]、[!UICONTROL Ad Template] フィールドが自動的に選択され、読み取り専用になります。

1. 動的な広告設定を指定して[動的な広告を作成](/help/creative/creative-libraries/creative-add-dynamic.md)します。

## 広告テンプレート設定 {#ad-template-settings}

### 広告テンプレートの詳細

**[!UICONTROL Advertiser]**: （既存のテンプレートの読み取り専用）広告を生成する広告主。

**[!UICONTROL Ad Template Name]**：広告主の一意の広告テンプレート名。

**[!UICONTROL Ad Template Type]**: （既存のテンプレートの読み取り専用）広告テンプレートの形式：*静的HTML5*&#x200B;または&#x200B;*動的HTML5*。

**[!UICONTROL Ad Template Size]**: （既存のテンプレートの読み取り専用） テンプレートで作成された広告のディメンション。

**[!UICONTROL Description]**: （オプション）広告テンプレートを使用しているすべてのユーザーに役立つ情報。

### （静的なHTML 5広告テンプレート）クリックタグ

**\[ クリックタグパラメーター\]**：広告テンプレートを使用して作成された広告からのクリックトラッキングリダイレクトを許可するクリックタグパラメーター。 パラメーターを追加するには、**[!UICONTROL + Add More]**&#x200B;をクリックし、追加のパラメーターを入力します。 最大5つのパラメーターを含めることができます。

### HTML5 zip

目的の広告フォーマットを含む圧縮されたHTML5 ファイル。 既にファイルをアップロードしている場合は、ファイル名が表示されます。

[HTML5 クリエイティブ仕様](/help/creative/creative-libraries/html5-creative-specification.md)を参照してください。

ファイルをアップロードするには：

1. **[!UICONTROL Upload HTML5 zip]**&#x200B;をクリックします。

1. デバイスまたはネットワーク上のファイルを探します。

### （Dynamic HTML 5広告テンプレート）属性ファイル

<!-- EXPLAIN and ad specs below for this file type -->広告テンプレートの属性を含むファイル。 既にファイルをアップロードしている場合は、ファイル名が表示されます。

ファイルをアップロードするには：

1. **[!UICONTROL Upload Attributes File]**&#x200B;をクリックします。

1. デバイスまたはネットワーク上のファイルを探します。

>[!MORELIKETHIS]
>
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
>* [ アセットファイルの管理](/help/creative/feeds/asset-manage.md)
>* [ フィード テンプレートの管理](/help/creative/feeds/feed-template-manage.md)
>* [ カタログの管理](/help/creative/feeds/catalog-manage.md)
>* [ クリエイティブライブラリに動的なクリエイティブを追加](/help/creative/creative-libraries/creative-add-dynamic.md)
