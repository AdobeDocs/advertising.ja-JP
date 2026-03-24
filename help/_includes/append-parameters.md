---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '214'
ht-degree: 0%

---
# アカウントおよびキャンペーン設定の「パラメーターを追加」フィールド

**[!UICONTROL Append Parameters]:** （オプション）ベース URLに追加する追加のトラッキングパラメーター。<!-- When account uses setting append_param_to_tt_fus, then we add append parameters to the tracking templates OR the landing page suffixes instead (not sure how we determine which) -->。 広告主レベルの追加パラメーターは、デフォルトでアカウントレベルとキャンペーンレベルに含まれていますが、どちらかを上書きできます。

サードパーティのトラッキングパラメーターを含む任意の静的テキスト文字列、またはベース URLに適切なデータ値を挿入する[&#x200B; サポートされているトラッキングパラメーター](/help/search-social-commerce/tracking/click-tracking-urls-optional-parameters.md)のいずれかを使用できます。

複数のパラメーターは、コンマまたはアンパサンド（&amp;）で区切ります。 ネストされた角括弧はサポートされていません。

**メモ：**

* 追加パラメーターの変更は、[!UICONTROL Auto Upload] オプションでは制御されません。 既存のベース URLの追加パラメーターを変更した場合、新しいURLは自動的に生成されません。 アカウントまたはキャンペーンのバルクシート ファイルをダウンロードし、[!UICONTROL Base URL/Final URL] フィールドを更新し、バルクシートをアップロードして投稿することで、新しいパラメーターを追加します。

* （並列追跡を備えた広告ネットワーク）並列追跡を有効にするソースからのクリックに代わられないマクロの使用を避けます。 広告主がマクロを使用する必要がある場合は、Adobe アカウントチームがカスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。

* （Adobe AdvertisingとAdobe Analyticsの統合を持つ広告主）検索、ソーシャル、およびCommerce データを[!DNL Analytics]に送信するためのAMO ID パラメーターを含めるには、[広告ネットワーク固有の形式](https://experienceleague.adobe.com/ja/docs/analytics/components/dimensions/amo-id#dimension-items)を参照してください。 サーバーサイド AMO ID実装を使用して、[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのパラメーターを手動で追加する必要はありません。
