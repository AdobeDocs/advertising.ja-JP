---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定の「パラメーターを追加」フィールド

**[!UICONTROL Append Parameters]:** （任意）ベース URL に追加する追加のトラッキングパラメーター。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->。 広告主レベルの追加パラメーターは、デフォルトでアカウントレベルとキャンペーンレベルに含まれていますが、どちらかを上書きできます。

サードパーティトラッキングパラメーターを含む任意の静的テキスト文字列、または任意の [ サポートされているトラッキングパラメーター ](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md) を使用できます。これらのパラメーターは、ベース URL に適切なデータ値を挿入します。

複数のパラメーターは、コンマまたはアンパサンド（&amp;）で区切ります。 入れ子になった角括弧はサポートされていません。

**注：**

* 追加パラメーターの変更は、[!UICONTROL Auto Upload] オプションでは制御されません。 既存のベース URL の追加パラメーターを変更した場合、新しい URL は自動的には生成されません。 アカウントまたはキャンペーンのバルクシートファイルをダウンロードし、[!UICONTROL Base URL/Final URL] のフィールドを更新してから、バルクシートをアップロードして投稿することで、新しいパラメーターを追加します。

* （並列トラッキングを使用する広告ネットワーク）並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

* （Adobe AdvertisingとAdobe Analyticsの統合を使用する広告主）検索、ソーシャル、Commerceのデータを [!DNL Analytics] に送信する AMO ID パラメーターを含めるには、[ 広告ネットワーク固有の形式 ](/help/integrations/analytics/ids.md#amo-id-formats) を参照してください。 サーバーサイド AMO ID 実装を使用して、[!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのパラメーターを手動で追加する必要はありません。
