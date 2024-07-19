---
title: クリックトラッキング URL 用のオプションのトラッキングパラメーター
description: クリックの追跡 URL に追加できる、オプションの検索、ソーシャル、Commerceのトラッキングパラメーターと広告ネットワーク固有のトラッキングパラメーターについて説明します。
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
source-git-commit: f633f2af545f034b08b378653b4b967710402a03
workflow-type: tm+mt
source-wordcount: '1097'
ht-degree: 0%

---

# クリックトラッキング URL 用のオプションのトラッキングパラメーター

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan] および [!DNL Yandex] アカウントのみ*

最終的な URL または宛先 URL に標準のトラッキングパラメーターのみを使用する代わりに、広告ネットワークアカウントの特定のデータを追跡するパラメーターを追加できます。 アカウント設定またはキャンペーン設定で、次のパラメーターの任意の組み合わせを追加できます。

* アカウント/キャンペーンのベース URL のパラメーターとして、任意の静的テキスト文字列を追加できます。

* アカウント/キャンペーンのベース URL にAdobe Advertisingおよび広告ネットワーク固有のパラメーターを追加して、より多くのデータを追跡できます。

   * Adobe Advertisingパラメーターは半静的です。 Adobe Advertisingが広告ネットワークにベース URL をアップロードする際に、データ値を挿入します。 例えば、ベース URL に `campaign={ef_campaign}` を追加すると、Adobe Advertisingは URL をアップロードする際に、`{ef_campaign}` を実際のキャンペーン名（「Back-to-school-Campaign」など）に置き換えます。

     **メモ：** 値が挿入されると、値は静的なままになります。 キーワードまたは広告を別の広告グループに移動する場合、または広告グループを別のキャンペーンに移動する場合、{ef_adgroup} または {ef_campaign} パラメーターは自動的には更新されないので、新しい宛先 URL またはベース（最終） URL を手動で生成する必要があります。

   * 広告ネットワーク固有のパラメーターは動的であり、ユーザーが広告をクリックすると、検索エンジンによってデータ値が挿入されます。 例えば、ベース URL に `{param1}` を追加すると、エンドユーザーが広告をクリックしたときに、広告ネットワークによって実際の {param1} 値に置き換えられます。

>[!NOTE]
>
>* 複数のパラメーターは、コンマまたはアンパサンド（`&`）で区切ります。
>* 次のパラメーターでは、大文字と小文字が区別されません。
>* 追加されたパラメーターの特殊文字は、生成された宛先 URL またはベース（最終） URL で次のように置き換えられます。
>  * `=` は `%3D` で置き換えられます
>  * `?` は `%26` で置き換えられます
>  * 空のスペースは `%2B` で置き換えられます
>  例えば、パラメーター `campaign={ef_campaign}` をキーワードのベース URL http://www.example.comに追加すると、そのキーワードのベース URL は `http://www.example.com/campaign%3D{ef_campaign}` として生成されます。

## 検索、ソーシャル、Commerceの静的トラッキングパラメーター

任意の広告ネットワーク上のアカウントに対して以下のパラメーターを使用し、必要に応じて特定の広告ネットワークのパラメーターと組み合わせることができます。 これらのパラメーターの一部は、アカウントのトラッキング方法が「[!UICONTROL EF Direct]」の場合に特定の広告ネットワークに自動的に追加されるパラメーターと重複します。

次のパラメーターはすべて、キーと値のペアとして指定する必要があります。1 つの値のペアに複数のパラメーターを含めることができます。 例えば、キャンペーン名を挿入するには、`campaign={ef_campaign}` のように `<your_parameter_name>={ef_campaign}` を使用します。 指定した一致タイプ名を使用して一致タイプを挿入するには、`matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}` などの `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}` を使用します。 適用されない一致タイプは、結果の URL には表示されません。

| パラメーター | 説明 |
| ---- | ---- |
| <code>{custom_code}</code> | アップロードしたバルクシートファイルの「カスタム URL パラメーター」列のデータをトラッキング URL に挿入します。 {custom_code} は、トラッキング URL の 1 つ以上のキーと値のペアの値の末尾でのみ使用できます。 例：<code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b> メモ：</b> バルクシートファイルのカスタム値をトラッキング URL に挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードします。 バルクシートファイルの使用について詳しくは、「[ バルクシートを使用した Campaign データの管理について ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を参照してください。 |
| <code>{ef_uniqueid}</code> | Adobe Advertisingで作成された一意の ID を挿入します。 追跡方法が「EF リダイレクト」の場合に自動的に追加されます。 |
| <code>{ef_userid}</code> | 広告主に割り当てる一意のAdobe AdvertisingID を挿入する。 |
| <code>{ef_sid}</code> | 検索、ソーシャル、およびCommerceによって広告ネットワークに割り当てられる数値 ID を挿入するには：[!DNL Google Ads] の場合は <i>[!UICONTROL 3]</i>、[!DNL Microsoft Advertising] の場合は <i>[!UICONTROL 10]</i>、[!DNL Meta] の場合は <i>[!UICONTROL 45]</i>、[!DNL Yahoo! Display Network]<i>[!UICONTROL 87]</i> の場合は <i>[!UICONTROL 86]</i>、[!DNL Naver] の場合は <i>[!UICONTROL 88]</i> [!DNL Baidu]、[!DNL Yandex] の場合は <i>[!UICONTROL 90]</i>、[!DNL Yahoo! Japan Ads]<i>[!UICONTROL 105]</i> の場合は <i>[!UICONTROL 94]</i>、[!DNL Yahoo Native] （非推奨）、[!DNL Pinterest] （非推奨）の場合は <i>[!UICONTROL 106]</i> です。 |
| <code>{ef_searchengine}</code> | 広告ネットワーク名を挿入します。 |
| <code>{ef_campaign}</code> | キャンペーン名を挿入します。 |
| <code>{ef_campaignid}</code> | キャンペーン ID を挿入します。 <b> メモ：</b> 新しいキャンペーンの ID は、キャンペーンが広告ネットワークに投稿されるまで作成されません。 アカウントで「[!UICONTROL EF Redirect]」および「AutoUpload」オプションを使用する場合、Adobe Advertisingは翌日、関連するリンク先 URL または最終 URL にキャンペーン ID を自動挿入します。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用せず、関連する宛先 URL または最終 URL にキャンペーン ID を挿入する場合は、キャンペーンを作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しいキャンペーンのバルクシートファイルをダウンロードし、ファイルを広告ネットワークに POST します。 |
| <code>{ef_adgroup}</code> | 広告グループ名を挿入します。 |
| <code>{ef_adgroupid}</code> | 広告グループ ID を挿入します。 <b> メモ：</b> 新しい広告グループの ID は、広告グループが広告ネットワークに投稿されるまで作成されません。 アカウントで「[!UICONTROL EF Redirect]」および「AutoUpload」オプションを使用している場合、Adobe Advertisingは関連するリンク先 URL または最終 URL に翌日、自動的に広告グループ ID を挿入します。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用せず、関連する宛先 URL または最終 URL に広告グループ ID を挿入する場合は、広告グループを作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しい広告グループのバルクシートファイルをダウンロードし、ファイルを広告ネットワークに POST します。 |
| <code>{ef_keyword}</code> | キーワードを挿入します。 |
| <code>{ef_keywordid}</code> | キーワード ID を挿入します。 <b> メモ：</b> 新しいキーワードの ID は、そのキーワードが広告ネットワークに投稿されるまで作成されません。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用している場合、Adobe Advertisingは関連するリンク先 URL または最終 URL に翌日、キーワード ID を自動的に挿入します。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用せず、関連する宛先 URL または最終 URL にキーワード ID を挿入する場合は、キーワードを作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しいキーワードのバルクシートファイルをダウンロードし、ファイルを広告ネットワークに POST します。 |
| <code>{ef_matchtype}</code> | キーワード一致を挿入するには、「部分一致」、「完全一致」、または「フレーズ」と入力します。 「[!UICONTROL EF Redirect]」トラッキング方式で [!DNL Google Ads] と [!DNL Microsoft Advertising] に自動的に含まれます。 |
| <code>{ef_adid}</code> | 広告 ID を挿入します。 <b> メモ：</b> 新規広告の ID は、広告が広告ネットワークに投稿されるまで作成されません。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用している場合、Adobe Advertisingは関連するリンク先 URL または最終的な URL に翌日、自動的に広告 ID を挿入します。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用せず、関連する宛先 URL または最終 URL に広告 ID を挿入する場合は、広告を作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しい広告のバルクシートファイルをダウンロードし、そのファイルを広告ネットワークに POST します。 |

## [!DNL Google Ads] 動的トラッキングパラメーター

[https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447) を参照してください。

## [!DNL Microsoft Advertising] 動的トラッキングパラメーター

[https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2) を参照してください。

## Yahoo! 日本広告の動的トラッキングパラメーター

[https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US) を参照してください。

## [!DNL Yandex] 動的トラッキングパラメーター

[https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html) を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について ](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
