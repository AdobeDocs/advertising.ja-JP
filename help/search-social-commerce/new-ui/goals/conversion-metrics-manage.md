---
title: 広告主のコンバージョン指標の管理
description: Adobe Advertisingが広告主に対して追跡するコンバージョン指標の使用方法について説明します。
feature: Conversions
source-git-commit: e2746d58fa512f032a1e4ff851d23876cd63fc93
workflow-type: tm+mt
source-wordcount: '665'
ht-degree: 0%

---

# 広告主のコンバージョン指標の管理

広告主の[ コンバージョン ](/help/search-social-commerce/glossary.md#c-d)指標は、Adobe Advertising全体で使用されます。

* Search, Social, &amp; Commerceでは、コンバージョン指標のデータを、キャンペーンビュー、ポートフォリオビュー、客観的な管理ビューおよびレポートの列に表示できます。 十分なアクセス権限を持つユーザーは、コンバージョン指標を使用して目的を作成し、ポートフォリオの最適化に使用することもできます。

* （Advertising DSPを使用する広告主） DSPでは、キャンペーン管理ビュー、カスタム目標、カスタムレポートにコンバージョン指標を含めることができます。 コンバージョン指標を使用して[ カスタム目標](/help/dsp/admin/custom-objectives-manage.md)を作成し、パッケージの最適化に使用することもできます。

利用できる指標は次のとおりです。

* Adobe Advertisingが広告主向けに追跡するコンバージョン指標。

* [ コンバージョンとサイトエンゲージメントの指標がAdobe Analyticsから同期されました](/help/integrations/analytics/analytics-data-in-advertising.md)。

* [ サイトイベントがAdobe Customer Journey Analyticsから同期されました](/help/integrations/customer-journey-analytics/overview.md)。

* [!DNL Google Ads]様が追跡したコンバージョンと、[!DNL Microsoft Advertising]件のユニバーサル イベント トラッキング タグが追跡したコンバージョンです。

* （[ アカウント、プロパティ、およびビューの組み合わせを検索、ソーシャル、およびCommerceのデータソース ](/help/search-social-commerce/admin/data-sources/data-source-about.md)として設定した場合） [!DNL Google Analytics]によって追跡されたコンバージョン。 [!DNL Google Analytics] 

* カスタムフィードからのコンバージョン。

利用可能なコンバージョン指標のリストから、広告主のデータへのアクセス権を持つ各ユーザーは、管理ビューやレポートで利用できる指標（選択した特定の指標を含む）をカスタマイズできます。 取得したデータのスペルと正確に一致する指標の名前を使用するか、列見出しに表示される名前を変更して読みやすくすることができます。

>[!IMPORTANT]
>
>デフォルトでは、広告主のコンバージョン指標（ユニバーサルイベント追跡タグ [!DNL Google Ads]、[!DNL Google Analytics]、[!DNL Microsoft Advertising]によって追跡されるコンバージョンを除く）は、キャンペーンおよびポートフォリオ管理ビュー、目的、レポートに含めることができません。 コンバージョン指標を使用できるようにするには、コンバージョン指標を明示的に使用できるようにする必要があります。
>
>[!DNL Google Ads]、[!DNL Google Analytics]および[!DNL Microsoft Advertising] ユニバーサルイベントトラッキングタグによってトラッキングされる新しいコンバージョンは、常に自動的に利用可能です。

>[!TIP]
>
>広告主（または広告ネットワーク）がコンバージョン指標の収集を停止すると、過去データの表示に使用しない限り、[管理表示とレポート ](#conversion-metrics-change-available)から非表示にします。

## 広告主が追跡したコンバージョン指標の表示

* メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

広告主向けに収集されたすべてのコンバージョン指標と、それらに割り当てられたさまざまな表示名が一覧表示されます。 各指標の行には、指標のソースが含まれます。

## コンバージョン指標の表示名の変更

例えば、*reg*&#x200B;という名前の変換指標を使用して登録データを収集する場合、オプションで表示名を変更して、「登録」として表示されるようにすることができます。

既存の表示名は削除できません。

>[!NOTE]
>
> [!DNL Google Analytics]](/help/search-social-commerce/admin/data-sources/data-source-about.md)からの[指標の場合、統合を更新または再認証すると、表示名に対する手動での変更はすべて上書きされます。 同様に、[!DNL Google Analytics]内の名前の変更は、統合を[更新](/help/search-social-commerce/admin/data-sources/data-source-edit.md)または[再認証](/help/search-social-commerce/admin/data-sources/data-source-reauthenticate.md)しない限り無視されます。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. リスト [をツールバー](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)または[列の見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からフィルタリングします。

1. 指標の&#x200B;**[!UICONTROL Conversion Display Name]**&#x200B;列で、指標の名前の上にカーソルを置き、**...** > **[!UICONTROL Rename]**&#x200B;をクリックします。

1. 表示する名前を入力し、**[!UICONTROL Apply]**&#x200B;をクリックします。

   表示名は一意である必要があり、次の特殊文字を含めることはできません：`\"<'>&`

## 管理ビュー、目的、レポートで使用できるコンバージョン指標を変更します {#conversion-metrics-change-available}

>[!NOTE]
>
>以前に使用可能だったコンバージョン指標を非表示にすると、コンバージョン指標を含む派生指標から削除されます。

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

   広告主向けに収集されたすべてのコンバージョン指標と、表示用に指定されたさまざまな名前が一覧表示されます。

1. （オプション）ツールバー](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md)または[列の見出し](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-column-heading.md)からリスト [をフィルタリングします。

1. 管理ビューとレポートで使用できるコンバージョン指標を変更します。

   * 1つの指標を表示または非表示にするには、**[!UICONTROL Visibility]**&#x200B;列のスイッチをクリックして、設定を変更します。

   * 複数の指標を表示または非表示にするには、次の操作を行います。

      1. 各コンバージョン指標の横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. バルクアクションツールバーで、![表示](/help/search-social-commerce/assets/visible.png "表示")をクリックして指標を表示するか、![表示オフ](/help/search-social-commerce/assets/visibility-off.png "表示オフ")をクリックして指標を非表示にします。

      1. （指標を非表示にするには）確認メッセージで「**[!UICONTROL Confirm]**」をクリックし、指標を含む派生指標から指標を削除するなど、指標を非表示にします。

<!--
>[!MORELIKETHIS]
>
>* 
-->
