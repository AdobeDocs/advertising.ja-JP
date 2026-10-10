---
title: クリエイティブライブラリでのダイナミッククリエイティブの編集
description: クリエイティブライブラリでダイナミッククリエイティブを編集する方法について説明します。
feature: Creative Dynamic Creatives
exl-id: b75b9aeb-ffd0-4b86-aa7a-bd6a22e7a8e4
TQID: 'https://experienceleague.adobe.com/QoQ5p4sFV-ARIMNDbPkp7axfqkVEC3sxJ6MTlPIG22Y'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d70c54b0-f069-4a3c-8056-7069a25e110c
    internal-label: Creative Dynamic Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: b7bf89dafd678490acc0749e2755ea7f0fec67f4
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 0%
---
# クリエイティブライブラリでのダイナミッククリエイティブの編集

## 新しいUIから

1. クリエイティブ設定を開きます。

   * クリエイティブライブラリから：

     1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

     1. 次のいずれかの方法でライブラリを開きます。

        * ライブラリ名をクリックします。

        * ライブラリ名の横にある「**[!UICONTROL ...]**」 > 「**[!UICONTROL Open]**」をクリックします。

     1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Edit]**」をクリックします。

   * [!UICONTROL Creative Studio]から：

     1. メインメニューで、**[!UICONTROL Creative]>[!UICONTROL Creative Studio]**&#x200B;をクリックします。

     1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックします。

        左側に広告プレビュー、右側に設定パネルが表示されたフルスクリーンエディターが開きます。

1. 「**[!UICONTROL Details]**」タブと「**[!UICONTROL Attribute Mapping]**」タブを使用して、クリエイティブ設定を編集します。

   **[!UICONTROL Details]** タブ：

   * **[!UICONTROL Advertiser]**、**[!UICONTROL Ad Library]**&#x200B;および&#x200B;**[!UICONTROL Ad template]**&#x200B;は読み取り専用です。
   * **[!UICONTROL Dynamic creative name]:** クリエイティブの表示名。
   * **[!UICONTROL Number of cards]:**&#x200B;各広告の組み合わせに含まれるカタログ オファーの数（1 ～ 50）。
   * （オプション） **[!UICONTROL Catalogs]**&#x200B;で、カタログの選択を更新します。
     * **[!UICONTROL Catalog template]**&#x200B;を使用して、使用可能なカタログをフィルタリングします。 必要に応じてテンプレートファイルをダウンロードするには、**[!UICONTROL Download feed template]**&#x200B;をクリックします。
     * リストからカタログを検索して選択するか、アップロードエリアにドラッグするか、**[!UICONTROL Browse Files]**&#x200B;をクリックして新しいカタログファイルをアップロードします（サポートされている形式：JPG、PNG、JPEG、XLS、XLSX、CSV、TSV、ZIP、MP4、最大25 MB、一度に1つのファイル）。 アップロードされたカタログは、チップリストに「**（アップロード）**」というラベルが付けられます。

     すべてのカタログは、同じカタログテンプレートファミリーに属している必要があります。

   **[!UICONTROL Attribute Mapping]** タブ：

   * **[!UICONTROL Targeting]**&#x200B;で、少なくとも1つのデータソースを選択してください：**[!UICONTROL Profile data]**、**[!UICONTROL Geographic data]**、**[!UICONTROL Data pass]**、または&#x200B;**[!UICONTROL Audience Segment]**。
   * **[!UICONTROL Attribute Mapping]**&#x200B;で、各テンプレートレイヤー名から対応するカタログ列ラベルへのマッピングを更新します。

1. **[!UICONTROL Update Creative]**&#x200B;をクリックします。

## レガシーUIから

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. **[!UICONTROL Switch to classic UI]**&#x200B;をクリックします。

1. ライブラリ名をクリックします。

1. クリエイティブ行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [動的広告設定](creative-settings-dynamic.md)を編集します。

1. 生成するクリエイティブをプレビューするには、**[!UICONTROL Continue]**&#x200B;をクリックします。 プレビュー内で次のいずれかを実行できます。

   * カタログ、フィルター値<!-- explain more-->、広告サイズでクリエイティブをフィルタリングするには、プレビュー領域の上にあるフィルターを使用します。

   * プレビュー領域の下にある検索フィールドで、製品を一意のIDで検索する。

   * 表示される列を変更するには、プレビュー領域の下にある![列フィルター](/help/creative/assets/custom-columns.png "列フィルター")をクリックします。

   * 特定のクリエイティブをプレビューするには、行のチェックボックスをオンにします。

   * コンテンツを変更する：

     * （表示広告のみ）表内のセルの値を編集するには、セル内をクリックして値を編集します。 セルの外側をクリックするか、**[!DNL Enter]** キーを押して変更を保存します。

     * 1つの商品をデフォルト <!--Explain what this means. -->としてマークするには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Set as Default]**&#x200B;をクリックします。

     * （広告に複数のオファーが含まれる場合）複数の商品をデフォルトとしてマークするには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Set as Default]**」をクリックします。

     * 商品をカタログから削除するには、行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete Row]**&#x200B;をクリックします。

     * （広告に複数のオファーが含まれる場合）カタログから複数の商品を削除するには、行（オファー数まで）を選択し、一括操作ツールバーの「**[!UICONTROL Delete Row]**」をクリックします。

1. クリエイターを救う：

   * 広告を保存し、ライブラリの[&#x200B; クリエイティブバンドル &#x200B;](bundle-manage.md)に追加するには：

     1. **[!UICONTROL Save and Attach to Bundle]**&#x200B;をクリックします。

     1. **[!UICONTROL Save]**&#x200B;をクリックして広告を保存します。

     1. バンドルを選択し、**[!UICONTROL Attach Creative to Bundles]**&#x200B;をクリックします。

   * 広告を保存して設定を終了するには、**[!UICONTROL Save]**&#x200B;をクリックし、もう一度&#x200B;**[!UICONTROL Save]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [動的なクリエイティブ設定](creative-settings-dynamic.md)
>* [&#x200B; クリエイティブライブラリに動的なクリエイティブを追加](creative-add-dynamic.md)
>* [&#x200B; クリエイティブの変更ログを表示](/help/creative/creative-libraries/creative-view-change-log.md)
>* [動的広告のワークフロー](/help/creative/introduction/workflow-dynamic-ads.md)
