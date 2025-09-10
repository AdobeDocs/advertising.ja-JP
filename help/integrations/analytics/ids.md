---
title: 使用するAdobe Advertising ID [!DNL Analytics]
description: 使用するAdobe Advertising ID [!DNL Analytics]
feature: Integration with Adobe Analytics
exl-id: ff20b97e-27fe-420e-bd55-8277dc791081
source-git-commit: e24cc514018ee67c485e884c4d57d051293ebf6a
workflow-type: tm+mt
source-wordcount: '864'
ht-degree: 0%

---

# [!DNL Analytics] が使用するAdobe Advertising ID

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

*Advertising DSPおよび[!DNL Advertising Search, Social, & Commerce]* に適用

Adobe Advertisingは、オンサイトのパフォーマンストラッキングに *EF ID* と *AMO ID* の 2 つの ID を使用します。

広告インプレッションが発生すると、Adobe Advertisingは AMO ID と EF ID の値を作成して保存します。 広告を見た訪問者が広告をクリックせずにサイトに入ると、[!DNL Analytics] ではこれらの値をAdobe Advertisingから [!DNL Analytics for Advertising] JavaScript コードを通じて呼び出します。 ビュースルートラフィックの場合、[!DNL Analytics] は追加の ID （`SDID`）を生成します。これは、EF ID と AMO ID を [!DNL Analytics] にステッチするために使用されます。 クリックスルートラフィックの場合、これらの ID は、`ef_id` および `s_kwcid` （AMO ID の）クエリ文字列パラメーターを使用して、ランディングページ URL に含まれます。

Adobe Advertisingは、次の条件を使用して、web サイトに対するクリックスルーまたはビュースルーエントリを区別します。

* ビュースルーエントリは、ユーザーが広告を表示したがクリックしなかった後にサイトを訪問した際に取得されます。 [!DNL Analytics] は、次の 2 つの条件を満たした場合にビュースルーを記録します。

   * [!DNL DSP] クリックルックバックウィンドウ [!DNL Search, Social, & Commerce] の間、訪問者が [ または ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 広告のクリックスルーを行うことはありません。

   * 訪問者は、[!DNL DSP] インプレッションルックバックウィンドウ [ 中に少なくとも 1 つの ](/help/integrations/analytics/prerequisites.md#lookback-a4adc) 広告を確認しました。 最後のインプレッションがビュースルーとして渡されます。

* クリックスルーのエントリは、サイト訪問者がサイトに入る前に広告をクリックした際にキャプチャされます。 [!DNL Analytics] は、次のいずれかの状況が発生した場合にクリックスルーをキャプチャします。

   * URL には、Adobe Advertisingによってランディングページ URL に追加された EF ID と AMO ID が含まれます。

   * URL にはトラッキングコードが含まれていませんが、Adobe Advertising JavaScript コードは過去 2 分以内にクリックを検出します。

![Adobe Advertisingのビューベースの [!DNL Analytics] 統合 ](/help/integrations/assets/a4adc-view-through-process.png)

*図 1:Adobe Advertisingのビューベースの [!DNL Analytics] 統合*

![Adobe Advertisingで URL ベースの [!DNL Analytics] 統合をクリック ](/help/integrations/assets/a4adc-click-through-process.png)

*図 2:Adobe Advertisingのクリックの URL ベースの [!DNL Analytics] 統合*

<!-- ## Adobe Advertising EF IDs -->

{{$include /help/_includes/ef-id.md}}

### [!DNL Analytics] の EF ID Dimension

[!DNL Analytics] レポートでは、[!UICONTROL EF ID] ディメンションを検索して [!UICONTROL EF ID Instance] 指標を使用することで、EF ID データを見つけることができます。

EF ID は、Analysis Workspaceで 500,000 個の ID 制限の対象となります。 500,000 の値に達すると、すべての新しいトラッキングコードが、1 行項目タイトル「[!UICONTROL Low Traffic]」の下にレポートされます。 レポートの忠実性が失われる可能性があるため、EF ID は分類されず、セグメントや [!DNL Analytics] でのレポートに使用しないでください。

<!-- ## ## Adobe Advertising AMO IDs {#amo-id} -->

{{$include /help/_includes/amo-id.md}}

### AMO ID を実装する方法 {#amo-id-implement}

パラメーターは、次のいずれかの方法でトラッキング URL に追加されます。

* （推奨） サーバーサイド挿入機能を実装する場合。

   * DSPのお客様：Pixel Server は、エンドユーザーがAdobe Advertising ピクセルを使用してディスプレイ広告を表示する際に、ランディングページサフィックスに s_kwcid パラメーターを自動的に追加します。

   * 検索、ソーシャル、Commerceのお客様：

      * アカウントまたはキャンペーンに対して [!DNL Google Ads] 設定が有効な [!DNL Microsoft Advertising] および [!UICONTROL Auto Upload] アカウントの場合、エンドユーザーがAdobe Advertising ピクセルで広告をクリックすると、ピクセルサーバーは s_kwcid パラメーターをランディングページサフィックスに自動的に追加します。

      * 他の広告ネットワーク、または [!DNL Google Ads] 設定が無効の [!DNL Microsoft Advertising] および [!UICONTROL Auto Upload] アカウントの場合は、[ アカウントレベルの追加パラメーター ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} にパラメーターを手動で追加して、ベース URL に追加します。

* サーバーサイド挿入機能が実装されていない場合：

   * DSPのお客様：[JavaScript コード ](javascript.md) は、クリックスルーとビュースルーを自動的に記録します。 ブラウザーがサードパーティ cookie をサポートしていない場合でも、次の広告タイプのクリックベースのコンバージョンを追跡できます。

      * [!DNL Flashtalking] の広告タグの場合は、「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Flashtalking]  広告タグに ](/help/integrations/analytics/macros-flashtalking.md)」ごとに手動で追加マクロを挿入します。 **注意：** 組織が [!DNL Flashtalking] と直接関係があり、データパスマクロを使用して `s_kwcid` および `ef_id` のトラッキングパラメーターを追跡する場合、[!DNL Flashtalking] サポートドキュメント （[https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros](https://support.flashtalking.com/hc/en-us/articles/4409808166419-Accessing-Data-Pass-Macros) に記載されている必要はありません。

      * [!DNL Google Campaign Manager 360] の広告タグの場合は、「[ 追加  [!DNL Analytics for Advertising]  マクロを  [!DNL Google Campaign Manager 360]  広告タグに ](/help/integrations/analytics/macros-google-campaign-manager.md)」ごとに手動で追加マクロを挿入します。

   * 検索、ソーシャル、Commerceのお客様：

      * （[!DNL Google Ads] および [!DNL Microsoft Advertising]）広告の場合、個々のアカウントコンポーネントに異なるトラッキングが必要な場合を除き、ランディングページのサフィックスに AMO ID パラメーターを手動で（理想的には [ アカウントレベル ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} 追加します。

      * その他のすべての広告ネットワークの広告の場合は、AMO ID パラメーターを [ アカウントレベルの追加パラメーター ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md){target="_blank"} に手動で追加し、ベース URL に追加します。

サーバーサイドの挿入機能を実装する、またはビジネスに最適なオプションを判断するには、Adobe アカウントチームにお問い合わせください。

### [!DNL Analytics] での AMO ID Dimension

Analytics レポートでは、[!UICONTROL AMO ID] ディメンションを検索して [!UICONTROL AMO ID Instances] 指標を使用することで、AMO ID データを見つけることができます。 [!UICONTROL AMO ID] ディメンションには、取得したすべての AMO ID 値が格納されます。[!UICONTROL AMO ID Instances] 指標は、AMO ID 値がサイトによって取得された頻度を示します。 例えば、同じ検索広告を 4 回クリックしても、Analytics で 7 つのサイトエントリをトラッキングした場合、[!UICONTROL AMO ID Instances] は 7 回、[!UICONTROL Clicks] は 4 回になります。

[!DNL Analytics] 内のレポートや監査の場合、ベストプラクティスは AMO ID を対応するインスタンスと共に使用することです。 詳しくは、「[ とAdobe Advertisingの間で予想されるデータの相違」の  [!DNL Analytics for Advertising]](data-variances.md#data-validation) のクリックスルー [!DNL Analytics] データの検証」を参照してください。

## Analytics 分類について

[!DNL Analytics] えば、[ 分類 ](https://experienceleague.adobe.com/docs/analytics/components/classifications/c-classifications.html?lang=ja) は、アカウント、キャンペーン、広告などの特定のトラッキングコードのメタデータの一部です。 Adobe Advertisingでは、レポートの生成時に様々な方法（広告タイプ別やキャンペーン別など）でデータを表示できるように、分類を使用して生のAdobe Advertising データを分類します。 分類は、[!DNL Analytics] でのAdobe Advertising レポートの基礎となるもので、[!UICONTROL Adobe Advertising Cost]、[!UICONTROL Adobe Advertising Impressions]、[!UICONTROL AMO Clicks] などの AMO 指標や、[!UICONTROL Visits]、[!UICONTROL Leads]、[!UICONTROL Orders]、[!UICONTROL Revenue] などのカスタムおよび標準のオンサイトイベントで使用できます。

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [ とAdobe Advertisingの間で予想されるデ  [!DNL Analytics]  タの相違 ](data-variances.md)
