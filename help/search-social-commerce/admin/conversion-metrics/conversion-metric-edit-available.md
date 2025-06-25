---
title: 管理ビューおよびレポートで使用可能なコンバージョン指標の変更
description: 管理ビューおよびレポートでコンバージョン指標を使用できるようにする方法を説明します。
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 管理ビューおよびレポートで使用可能なコンバージョン指標の変更

Adobe Advertisingが広告主の [ コンバージョン ](/help/search-social-commerce/glossary.md#c-d) 指標を追跡すると、最初はポートフォリオ目標、レポート、管理ビューから除外されます。 コンバージョン指標を表示するには、明示的に使用可能にし、オプションで、表示される名前であるデフォルトの表示名を変更する必要があります。 唯一の例外は、[!DNL Google Ads]、[!DNL Google Analytics] および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグで追跡されるコンバージョンが、自動的に使用可能になり表示される点です。

同様に、ポートフォリオの目標、レポート、管理ビューからコンバージョン指標を非表示にすることができます。 以前に表示されていたコンバージョン指標を非表示にすると、コンバージョン指標を含む派生指標から削除されます。

使用可能なコンバージョン指標のリストから、広告主のデータにアクセスできる各ユーザーは、表示される指標をカスタマイズして管理ビューおよびレポートを表示できます（選択した特定の指標を含めるか除外するかを選択できます）。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Admin]/[!UICONTROL Conversions]** をクリックします。

   広告主向けに収集されたすべてのコンバージョン指標と、表示用に指定された別の名前が一覧表示されます。

1. （オプション）リストをフィルタリングします。

   * 特定の指標名または表示名を検索するには、![ 検索 ](/help/search-social-commerce/assets/search.png " 検索 ") をクリックし、入力フィールドに単語または文字列を入力して、**[!DNL Enter]** キーを押します。

     フレーズ内の任意の場所（最初の文字または最後の 3 文字など）に表示される文字列を検索でき、検索用語は [ 大文字と小文字を区別 ](/help/search-social-commerce/glossary.md#c-d) されません。

   * 管理ビューおよびレポートで使用可能な状態に応じてコンバージョン指標を検索するには、「![ フィルター ](/help/search-social-commerce/assets/filter.png " フィルター ")」をクリックし、フィルター **[!UICONTROL Show in UI and Reports]** を選択します。 次に、**[!UICONTROL Show]** （レポートおよび管理ビューに含めることができるコンバージョン指標を表示する）または **[!UICONTROL Hide]** （レポートおよび管理ビューに含めることができないコンバージョン指標を表示する）を選択します。

1. 管理ビューおよびレポートで使用可能なコンバージョン指標を変更します。

   * 1 つの指標を表示または非表示にするには、**[!UICONTROL Show in UI and Reports]** 列のスイッチをクリックして設定を変更します。

   * 複数の指標を表示または非表示にするには、次の手順を実行します。

      1. 各コンバージョン指標の横にあるチェックボックスをオンにします。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. データテーブルの上にあるツールバーで、![ 表示 ](/help/search-social-commerce/assets/show.png " 表示 ") をクリックして指標を表示するか、![Hide](/help/search-social-commerce/assets/hide.png "Hide") をクリックして指標を非表示にします。

      1. （指標を非表示にするには）確認メッセージで「**[!UICONTROL Yes]**」をクリックして、指標を非表示にします（指標を含む派生指標からの削除も含まれます）。

1. （任意） [ 列見出しに表示される名前を変更 ](conversion-metric-edit-display-name.md) 任意のコンバージョン指標について。

   表示される各コンバージョン指標のデフォルトの表示名は、取得したデータでつづられているような指標名です。

>[!NOTE]
>
>Adobe Advertisingが新しいコンバージョン指標のデータを収集すると、新しい指標（[!DNL Google Ads]、[!DNL Google Analytics] および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグで追跡されるコンバージョンを除く）は、追加するまで管理ビューおよびレポートから自動的に除外されます。 [!DNL Google Ads]、[!DNL Google Analytics] および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグで追跡される新しいコンバージョンは、常に自動的に使用可能になります。

>[!MORELIKETHIS]
>
>* [ 広告主のコンバージョン指標の管理について ](conversion-metric-about.md)
>* [ 広告主について追跡されたコンバージョン指標の表示 ](conversion-metric-view-tracked.md)
>* [ コンバージョン指標の表示名の変更 ](conversion-metric-edit-display-name.md)
