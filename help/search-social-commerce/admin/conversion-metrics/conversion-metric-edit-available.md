---
title: 管理ビューおよびレポートで使用できるコンバージョン指標の変更
description: コンバージョン指標を管理ビューおよびレポートで使用できるようにする方法を説明します。
feature: Conversions
exl-id: a8f3a2d6-4203-42db-96cd-faf02d20d247
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 管理ビューおよびレポートで使用できるコンバージョン指標の変更

Adobe Advertisingが [コンバージョン](/help/search-social-commerce/glossary.md#c-d) 広告主の指標では、最初はポートフォリオの目標、レポート、管理ビューから除外されます。 コンバージョン指標を表示するには、明示的に使用可能にしてから、オプションでデフォルトの表示名（表示される名前）を変更する必要があります。 唯一の例外は、コンバージョンが [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグは自動的に使用可能になり、表示されます。

同様に、ポートフォリオの目標、レポート、管理ビューでコンバージョン指標を非表示にできます。 以前に表示されていたコンバージョン指標を非表示にすると、そのコンバージョン指標を含む派生指標からそのコンバージョン指標が削除されます。

使用可能なコンバージョン指標のリストから、広告主のデータにアクセスできる各ユーザーは、管理ビューとレポートに表示される指標をカスタマイズできます。特定の指標は、選択したとおりに使用したり、省略したりできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   広告主用に収集されたすべてのコンバージョン指標と、表示用に指定された異なる名前が一覧表示されます。

1. （オプション）リストをフィルターします。

   * 特定の指標名または表示名を検索するには、 ![検索](/help/search-social-commerce/assets/search.png "検索")」をクリックし、入力フィールドに単語または文字列を入力して、 **[!DNL Enter]** キー。

     フレーズ内の任意の場所に出現する文字列（最初の文字や最後の 3 文字など）を検索でき、検索語句が [大文字と小文字を区別](/help/search-social-commerce/glossary.md#c-d).

   * 管理ビューとレポートで使用可能なコンバージョン指標で検索するには、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター")をクリックし、フィルターを選択します。 **[!UICONTROL Show in UI and Reports]**. 次に、次のいずれかを選択します。 **[!UICONTROL Show]** （レポートおよび管理ビューに含めることができるコンバージョン指標を表示する場合）または **[!UICONTROL Hide]** （レポートおよび管理ビューで使用できないコンバージョン指標を表示する場合）。

1. 管理ビューおよびレポートで使用できるコンバージョン指標を変更します。

   * 単一の指標の表示/非表示を切り替えるには、 **[!UICONTROL Show in UI and Reports]** 列を使用して設定を変更します。

   * 複数の指標の表示/非表示を切り替えるには、以下の手順を実行します。

      1. 各コンバージョン指標の横にあるチェックボックスをオンにします。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![表示](/help/search-social-commerce/assets/show.png "表示") 指標を表示するには、または ![非表示](/help/search-social-commerce/assets/hide.png "非表示") をクリックして、指標を非表示にします。

      1. （指標を非表示にするには）確認メッセージで、 **[!UICONTROL Yes]** をクリックして非表示にします。指標を含む派生指標からの指標の削除も含まれます。

1. （オプション） [列見出しに表示される名前を変更する](conversion-metric-edit-display-name.md) 任意のコンバージョン指標用。

   表示される各コンバージョン指標のデフォルトの表示名は、取得したデータに記述されている指標名です。

>[!NOTE]
>
>Adobe Advertisingが新しいコンバージョン指標のデータを収集した場合は、新しい指標が表示されます（ただし、で追跡されるコンバージョンは除く）。 [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグ — 管理ビューとレポートから、それらを含めるまで自動的に除外されます。 次の条件で追跡された新しいコンバージョン [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグは、常に自動的に使用可能になります。

>[!MORELIKETHIS]
>
* [広告主のコンバージョン指標の管理について](conversion-metric-about.md)
* [広告主で追跡されているコンバージョン指標を表示する](conversion-metric-view-tracked.md)
* [コンバージョン指標の表示名の変更](conversion-metric-edit-display-name.md)
