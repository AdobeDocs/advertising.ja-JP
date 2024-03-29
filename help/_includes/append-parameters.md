---
source-git-commit: 05b9a55e19c9f76060eedb35c41cdd2e11753c24
workflow-type: tm+mt
source-wordcount: '213'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定の「パラメーターを追加」フィールド

**[!UICONTROL Append Parameters]:** （オプション）ベース URL に追加する追加のトラッキングパラメーター。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->. 広告主レベルの追加パラメーターは、デフォルトでアカウントレベルとキャンペーンレベルで含まれますが、どちらかを上書きできます。

サードパーティのトラッキングパラメーターを含む任意の静的テキスト文字列、または任意の [サポートされるトラッキングパラメーター](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)：ベース URL に適切なデータ値を挿入します。

複数のパラメーターを使用する場合は、コンマまたはアンパサンド (&amp;) で区切ります。 入れ子になった角括弧はサポートされていません。

**メモ：**

* 追加パラメータの変更は、 [!UICONTROL Auto Upload] オプション。 既存のベース URL に追加パラメーターを変更した場合、新しい URL は自動的には生成されません。 アカウントまたはキャンペーンのバルクシートファイルをダウンロードし、 [!UICONTROL Base URL/Final URL] フィールドに貼り付け、バルクシートをアップロードして投稿します。

* （並列追跡を使用する広告ネットワーク）マクロの使用は避けます。マクロは、並列追跡を有効にするソースからのクリックに置き換えられません。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。

* (Adobe AdvertisingとAdobe Analyticsの統合を使用する広告主 ) 検索、ソーシャル、コマースのデータをに送信するための AMO ID パラメーターを含めるには [!DNL Analytics]を参照し、 [広告ネットワーク固有の形式](/help/integrations/analytics/ids.md#amo-id-formats). 次のパラメーターを手動で追加する必要はありません。 [!DNL Google Ads] および [!DNL Microsoft Advertising] サーバー側 AMO ID 実装を持つアカウント。
