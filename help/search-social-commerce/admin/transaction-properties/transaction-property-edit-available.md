---
title: 管理ビューとレポートで使用可能なトランザクションプロパティの変更
description: 管理ビューとレポートでトランザクションプロパティを使用可能にする方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '493'
ht-degree: 0%

---

# 管理ビューとレポートで使用可能なトランザクションプロパティの変更

Adobe広告が [取引財産](/help/search-social-commerce/glossary.md#s-t) 広告主の場合、最初はポートフォリオの目標、レポート、管理ビューから除外されます。 プロパティを表示するには、そのプロパティを明示的に使用可能にしてから、必要に応じて既定の表示名（表示名）を変更する必要があります。 唯一の例外は、コンバージョンが [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグは自動的に使用可能になり、表示されます。

同様に、ポートフォリオの目標、レポート、管理ビューでプロパティを非表示にすることもできます。 以前に表示されていたプロパティを非表示にすると、そのプロパティを含む派生指標からそのプロパティが削除されます。

使用可能なプロパティのリストから、広告主のデータにアクセスできる各ユーザーは、管理ビューとレポートに表示されるプロパティをカスタマイズできます。このプロパティには、選択した特定のプロパティを含めたり省略したりできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Transaction Properties]**.

   広告主に対して収集されたすべてのトランザクションプロパティと、表示用に指定された異なる名前が一覧表示されます。

1. （オプション）リストをフィルターします。

   * 特定のプロパティ名または表示名を検索するには、 ![検索](/help/search-social-commerce/assets/search.png "検索")をクリックし、入力フィールドに単語または文字列を入力して、 **[!DNL Enter]** キー。

      フレーズ内の任意の場所に出現する文字列（最初の文字や最後の 3 文字など）を検索でき、検索語句が [大文字と小文字を区別](/help/search-social-commerce/glossary.md#c-d).

   * 管理ビューとレポートでプロパティを使用可能な状態で検索するには、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター")をクリックし、フィルターを選択します。 **[!UICONTROL Show in UI and Reports]**. 次に、 **[!UICONTROL Show]** （レポートおよび管理ビューに含めることができるプロパティを表示する）または **[!UICONTROL Hide]** （Reports and Management ビューで使用できないプロパティを表示する場合）。

1. 管理ビューおよびレポートで使用できるプロパティを変更します。

   * 単一のプロパティの表示/非表示を切り替えるには、 **[!UICONTROL Show in UI and Reports]** 列を使用して設定を変更します。

   * 複数のプロパティを表示または非表示にするには、次の操作を行います。

      1. 各プロパティの横にあるチェックボックスをオンにします。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![表示](/help/search-social-commerce/assets/show.png "表示") プロパティまたは ![を隠す](/help/search-social-commerce/assets/hide.png "を隠す") プロパティを非表示にします。

      1. （プロパティを非表示にするには）確認メッセージで、 **[!UICONTROL Yes]** プロパティを非表示にする（プロパティを含む派生指標から削除するなど）。

1. （オプション） [列見出しに表示される名前を変更する](transaction-property-edit-display-name.md) の任意のプロパティ。

   各表示プロパティのデフォルトの表示名は、取得したデータでのスペルに応じたプロパティ名です。

>[!NOTE]
>
>Adobe広告が新しいプロパティのデータを収集する場合、新しいプロパティは（で追跡されるコンバージョンを除く）となります。 [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグ — 管理ビューとレポートから、それらを含めるまで自動的に除外されます。 次の条件で追跡された新しいコンバージョン [!DNL Google Ads], [!DNL Google Analytics]、および [!DNL Microsoft® Advertising] ユニバーサルイベントトラッキングタグは、常に自動的に使用可能になります。

>[!MORELIKETHIS]
* [広告主のトランザクションプロパティの管理について](transaction-property-about.md)
* [広告主でトラッキングされているトランザクションプロパティの表示](transaction-property-view-tracked.md)
* [トランザクションプロパティの表示名を変更する](transaction-property-edit-display-name.md)

