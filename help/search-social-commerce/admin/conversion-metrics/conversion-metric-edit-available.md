---
title: 管理ビューおよびレポートで使用可能なコンバージョン指標の変更
description: 管理ビューおよびレポートでコンバージョン指標を使用できるようにする方法を説明します。
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 0%

---

# 管理ビューおよびレポートで使用可能なコンバージョン指標の変更

Adobe Advertisingがを追跡する場合 [変換](/help/search-social-commerce/glossary.md#c-d) 広告主の場合、指標は最初ポートフォリオ目標、レポート、管理ビューから除外されます。 コンバージョン指標を表示するには、明示的に使用可能にし、オプションで、表示される名前であるデフォルトの表示名を変更する必要があります。 唯一の例外は、によって追跡されるコンバージョンです。 [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグは、自動的に使用可能になり表示されます。

同様に、ポートフォリオの目標、レポート、管理ビューからコンバージョン指標を非表示にすることができます。 以前に表示されていたコンバージョン指標を非表示にすると、コンバージョン指標を含む派生指標から削除されます。

使用可能なコンバージョン指標のリストから、広告主のデータにアクセスできる各ユーザーは、表示される指標をカスタマイズして管理ビューおよびレポートを表示できます（選択した特定の指標を含めるか除外するかを選択できます）。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

   広告主向けに収集されたすべてのコンバージョン指標と、表示用に指定された別の名前が一覧表示されます。

1. （オプション）リストをフィルタリングします。

   * 特定の指標名または表示名を検索するには、 ![検索](/help/search-social-commerce/assets/search.png "検索")を選択し、入力フィールドに単語または文字列を入力して、 **[!DNL Enter]** キー。

     フレーズ内の任意の場所（最初の文字や最後の 3 文字など）に表示される文字列を検索できますが、検索語句は検索できません [大文字と小文字を区別](/help/search-social-commerce/glossary.md#c-d).

   * 管理ビューおよびレポートで使用可能なコンバージョン指標を検索するには、以下をクリックします。 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター")で、フィルターを選択します。 **[!UICONTROL Show in UI and Reports]**. 次に、次のいずれかを選択します **[!UICONTROL Show]** （レポートおよび管理ビューに含めることができるコンバージョン指標を表示するには） **[!UICONTROL Hide]** （レポートおよび管理ビューで使用できないコンバージョン指標を表示するため）。

1. 管理ビューおよびレポートで使用可能なコンバージョン指標を変更します。

   * 単一の指標を表示または非表示にするには、 **[!UICONTROL Show in UI and Reports]** 設定を変更する列。

   * 複数の指標を表示または非表示にするには、次の手順を実行します。

      1. 各コンバージョン指標の横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

      1. データ テーブルの上にあるツールバーで、 ![表示](/help/search-social-commerce/assets/show.png "表示") 指標を表示または ![Hide](/help/search-social-commerce/assets/hide.png "Hide") 指標を非表示にします。

      1. （指標を非表示にするには）確認メッセージで、 **[!UICONTROL Yes]** 指標を含む派生指標からの削除など、指標の非表示。

1. （オプション） [列見出しに表示される名前を変更する](conversion-metric-edit-display-name.md) 任意のコンバージョン指標の。

   表示される各コンバージョン指標のデフォルトの表示名は、取得したデータでつづられているような指標名です。

>[!NOTE]
>
>Adobe Advertisingが新しいコンバージョン指標のデータを収集する場合、によって追跡されたコンバージョンを除き、新しい指標が収集されます。 [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグ – 含めるまで、管理ビューおよびレポートから自動的に除外されます。 が追跡する新しいコンバージョン [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグは、常に自動的に使用できます。

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](conversion-metric-about.md)
>* [広告主について追跡されたコンバージョン指標の表示](conversion-metric-view-tracked.md)
>* [コンバージョン指標の表示名の変更](conversion-metric-edit-display-name.md)
