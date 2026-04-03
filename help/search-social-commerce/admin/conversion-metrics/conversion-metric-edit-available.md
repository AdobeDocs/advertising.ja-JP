---
title: 管理ビューとレポートで使用できるコンバージョン指標の変更
description: コンバージョン指標を管理ビューとレポートで利用できるようにする方法について説明します。
feature: Conversions
exl-id: de3d288a-5fec-4479-92cf-7754390e21bb
TQID: https://experienceleague.adobe.com/o50AN9pYkuuP-M1e4IAkQOLWSsg584T6TtWnrawAnUU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 506
ht-degree: 0%

---

# 管理ビューとレポートで使用できるコンバージョン指標の変更

Adobe Advertisingが広告主の[ コンバージョン ](/help/search-social-commerce/glossary.md#c-d)指標を追跡する場合、最初はポートフォリオ目標、レポート、管理ビューから除外されます。 コンバージョン指標を表示するには、指標を明示的に使用可能にし、オプションでデフォルトの表示名（表示されている名前）を変更する必要があります。 唯一の例外は、[!DNL Google Ads]、[!DNL Google Analytics]、[!DNL Microsoft Advertising]のユニバーサルイベントトラッキングタグによってトラッキングされたコンバージョンが、自動的に使用可能で表示されることです。

同様に、ポートフォリオ目標、レポート、管理ビューからコンバージョン指標を非表示にすることもできます。 以前に表示されていたコンバージョン指標を非表示にすると、コンバージョン指標を含む派生指標から削除されます。

利用可能なコンバージョン指標のリストから、広告主のデータへのアクセス権を持つ各ユーザーは、特定の指標の選択を含むか省略するなど、管理ビューやレポートに表示される指標をカスタマイズできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックします。

   広告主向けに収集されたすべてのコンバージョン指標と、表示用に指定されたさまざまな名前が一覧表示されます。

1. （オプション）リストをフィルタリングします。

   * 特定の指標名または表示名を検索するには、![検索](/help/search-social-commerce/assets/search.png "検索")をクリックし、入力フィールドに単語または文字列を入力して、**[!DNL Enter]** キーを押します。

     フレーズ内の任意の場所（最初の文字や最後の3文字など）に表示される文字列を検索できますが、検索語は[大文字と小文字を区別しません](/help/search-social-commerce/glossary.md#c-d)。

   * 管理ビューとレポートの可用性でコンバージョン指標を検索するには、![ フィルター](/help/search-social-commerce/assets/filter.png " フィルター")をクリックし、フィルター&#x200B;**[!UICONTROL Show in UI and Reports]**&#x200B;を選択します。 次に、**[!UICONTROL Show]** （レポートと管理ビューに含めることができるコンバージョン指標を表示する場合）または&#x200B;**[!UICONTROL Hide]** （レポートと管理ビューで使用できないコンバージョン指標を表示する場合）を選択します。

1. 管理ビューとレポートで使用できるコンバージョン指標を変更します。

   * 1つの指標を表示または非表示にするには、**[!UICONTROL Show in UI and Reports]**&#x200B;列のスイッチをクリックして、設定を変更します。

   * 複数の指標を表示または非表示にするには、次の操作を行います。

      1. 各コンバージョン指標の横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. データテーブルの上にあるツールバーで、![表示](/help/search-social-commerce/assets/show.png "表示")をクリックして指標を表示するか、![非表示](/help/search-social-commerce/assets/hide.png "非表示")をクリックして指標を非表示にします。

      1. （指標を非表示にするには）確認メッセージで「**[!UICONTROL Yes]**」をクリックし、指標を含む派生指標から指標を削除するなど、指標を非表示にします。

1. （オプション） [任意のコンバージョン指標の列見出し](conversion-metric-edit-display-name.md)に表示される名前を変更します。

   表示される各変換指標のデフォルトの表示名は、取得したデータにスペルが設定されている指標の名前です。

>[!NOTE]
>
>Adobe Advertisingが新しいコンバージョン指標のデータを収集する場合、[!DNL Google Ads]、[!DNL Google Analytics]、[!DNL Microsoft Advertising]のユニバーサルイベントトラッキングタグによってトラッキングされるコンバージョンを除く、新しい指標は、管理ビューとレポートから自動的に除外されます。 [!DNL Google Ads]、[!DNL Google Analytics]および[!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグによってトラッキングされる新しいコンバージョンは、常に自動的に利用可能です。

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](conversion-metric-about.md)
>* [広告主に対して追跡されたコンバージョン指標を表示](conversion-metric-view-tracked.md)
>* [ コンバージョン指標の表示名を変更](conversion-metric-edit-display-name.md)
