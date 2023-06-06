---
title: クリック追跡 URL のオプションのトラッキングパラメーター
description: オプションの検索、ソーシャル、コマースのトラッキングパラメーターと、クリックトラッキング URL に追加できるネットワーク固有のトラッキングパラメーターについて説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '1211'
ht-degree: 0%

---

# クリック追跡 URL のオプションのトラッキングパラメーター

*Google Ads、Microsoft Advertising および Yahoo! 日本のみ*

最終的な URL またはリンク先 URL に対して標準のトラッキングパラメーターのみを使用する代わりに、広告ネットワークアカウントの特定のデータを追跡するためのパラメーターをさらに追加することもできます。 次のパラメーターの任意の組み合わせをアカウント設定またはキャンペーン設定に追加できます。

* 任意の静的テキスト文字列を、アカウント/キャンペーンのベース URL のパラメーターとして追加できます。

* アカウント/キャンペーンのベース URL にAdobe広告および広告ネットワーク固有のパラメーターを追加して、さらに多くのデータを追跡できます。

   * Adobe広告パラメーターは半静的です。 Adobe広告は、ベース URL を広告ネットワークにアップロードする際に、データ値を挿入します。 例えば、 `campaign={ef_campaign}` をベース URL に追加すると、Adobe広告は `{ef_campaign}` を実際のキャンペーン名（「新学期のキャンペーン」など）に置き換えます。

      **注意：** 値が挿入されても、値は静的なままです。 キーワードまたは広告を別の広告グループに移動したり、広告グループを別のキャンペーンに移動した場合、{ef_adgroup} または {ef_campaign} パラメーターは自動的に更新されないので、新しいリンク先 URL またはベース（最終）URL を手動で生成する必要があります。

   * 広告のネットワーク固有のパラメーターは動的で、ユーザーが広告をクリックすると、検索エンジンはデータ値を挿入します。 例えば、 `{param1}` をベース URL に設定すると、エンドユーザーが広告をクリックすると、広告ネットワークによってその値が実際の {param1} 値に置き換えられます。

>[!NOTE]
>
>* 複数のパラメーターを使用する場合は、コンマまたはアンパサンド (`&`) をクリックします。
>* 次のパラメーターでは、大文字と小文字が区別されません。
>* 追加されたパラメーター内の特殊文字は、生成される宛先 URL またはベース（最終）URL で次のように置き換えられます。
>  * `=` は次の値で置き換えられます。 `%3D`
>  * `?` は次の値で置き換えられます。 `%26`
>  * 空のスペースは `%2B`

   >  例えば、 `campaign={ef_campaign}` をキーワードのベース URL http://www.example.comに追加すると、そのキーワードのベース URL は `http://www.example.com/campaign%3D{ef_campaign}`.


## Search、Social および Commerce の静的トラッキングパラメーター

次のパラメーターは、任意の広告ネットワーク上のアカウントに使用でき、必要に応じて特定の広告ネットワークのパラメーターと組み合わせることができます。 これらのパラメーターの一部は、アカウントのトラッキングメソッドが「[!UICONTROL EF Direct].&quot;

次のパラメーターはすべて、キーと値のペアとして指定する必要があります。1 つの値のペアに複数のパラメーターを含めることができます。 例えば、キャンペーン名を挿入するには、 `<your_parameter_name>={ef_campaign}`例： `campaign={ef_campaign}`. 指定した一致タイプ名を使用して一致タイプを挿入するには、 `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`例： `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. 該当しない一致タイプは、結果の URL に表示されません。

| パラメータ | 説明 |
| ---- | ---- |
| {custom_code}</code> | アップロードしたバルクシートファイルの「カスタム URL パラメーター」列のデータをトラッキング URL に挿入する場合。 {custom_code} は、トラッキング URL の 1 つ以上のキーと値のペアの値の最後でのみ使用できます。 例：a={custom_code}</code>;a={ef_campaignid}{custom_code}</code>;a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b> バルクシートファイルのカスタム値をトラッキング URL に挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードします。 一括シートファイルの使用の詳細については、[バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).&quot; |
| {ef_uniqueid}</code> | Adobe広告で作成された一意の ID を挿入する。 トラッキングメソッドが「EF Redirect」の場合に自動的に追加されます。 |
| {ef_userid}</code> | 広告主に割り当てる一意のAdobeID を挿入する。 |
| {ef_sid}</code> | Search、Social および Commerce が広告ネットワークに割り当てる数値 ID を挿入するには、次の手順を実行します。 <i>[!UICONTROL 3]</i> 対象 [!DNL Google Ads], <i>[!UICONTROL 10]</i> 対象 [!DNL Microsoft® Advertising], <i>[!UICONTROL 45]</i> 対象 [!DNL Meta], <i>[!UICONTROL 86]</i> 対象 [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> 対象 [!DNL Naver], <i>[!UICONTROL 88]</i> 対象 [!DNL Baidu], <i>[!UICONTROL 90]</i> 対象 [!DNL Yandex], <i>[!UICONTROL 94]</i> 対象 [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> 対象 [!DNL Yahoo Native] （非推奨）または <i>[!UICONTROL 106]</i> 対象 [!DNL Pinterest] （非推奨）。 |
| {ef_searchengine}</code> | 広告ネットワーク名を挿入するには。 |
| {ef_campaign}</code> | キャンペーン名を挿入します。 |
| {ef_campaignid}</code> | キャンペーン ID を挿入します。 <b>注意：</b> 新しいキャンペーンの ID は、キャンペーンが広告ネットワークに投稿されるまで作成されません。 アカウントで「EF Redirect」および「AutoUpload」オプションが使用されている場合、Adobe広告はキャンペーン ID を関連する宛先 URL または翌日に最終 URL に自動的に挿入します。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されず、関連する宛先 URL または最終 URL にキャンペーン ID を挿入する場合は、キャンペーンを作成する必要があります。「トラッキング URL の生成」オプションを使用して、新しいキャンペーン用のバルクシートファイルをダウンロードし、そのファイルを広告ネットワークに投稿します。 |
| {ef_adgroup}</code> | 広告グループ名を挿入するには： |
| {ef_adgroupid}</code> | 広告グループ ID を挿入するには： <b>注意：</b> 新しい広告グループの ID は、広告グループが広告ネットワークに投稿されるまで作成されません。 アカウントで「EF Redirect」および「AutoUpload」オプションが使用されている場合、Adobe広告は、翌日に、関連するリンク先 URL または最終 URL に広告グループ ID を自動的に挿入します。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されず、関連する宛先 URL または最終 URL に広告グループ ID を挿入する場合は、広告グループを作成する必要があります。「トラッキング URL の生成」オプションを使用して、新しい広告グループ用のバルクシートファイルをダウンロードし、そのファイルを広告ネットワークに投稿します。 |
| {ef_keyword}</code> | キーワードを挿入するには、次の手順に従います。 |
| {ef_keywordid}</code> | キーワード ID を挿入するには、をクリックします。 <b>注意：</b> 新しいキーワードの ID は、そのキーワードが広告ネットワークに投稿されるまで作成されません。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されている場合、Adobe広告は、次の日に、関連する宛先 URL または最終 URL にキーワード ID を自動的に挿入します。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されず、関連する宛先 URL または最終 URL にキーワード ID を挿入する場合は、キーワードを作成する必要があります。「トラッキング URL の生成」オプションを使用して、新しいキーワードのバルクシートファイルをダウンロードし、そのファイルを広告ネットワークに投稿します。 |
| {ef_matchtype}</code> | キーワード一致タイプを「部分一致」、「完全一致」または「フレーズ」として挿入するには、次のように指定します。 「EF Redirect」トラッキングメソッドを使用したGoogle Ads およびMicrosoft Advertising に対して自動的に含まれます。 |
| {ef_adid}</code> | 広告 ID を挿入します。 <b>注意：</b> 新しい広告の ID は、広告が広告ネットワークに投稿されるまで作成されません。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されている場合、Adobe広告は、翌日に、関連する宛先 URL または最終 URL に広告 ID を自動的に挿入します。 アカウントで「EF Redirect」および「Auto Upload」オプションが使用されず、関連する宛先 URL または最終 URL に広告 ID を挿入する場合は、広告を作成する必要があります。「トラッキング URL の生成」オプションを使用して、新しい広告のバルクシートファイルをダウンロードし、そのファイルを広告ネットワークに投稿します。 |

## Google Ads 動的トラッキングパラメーター

詳しくは、 [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## Microsoft Advertising 動的トラッキングパラメーター

詳しくは、 [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo ネイティブ動的トラッキングパラメーター

詳しくは、 [https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters](https://developer.yahoo.com/nativeandsearch/guide/resources/dynamic-parameters).

## Yahoo! Japan Ads 動的トラッキングパラメーター

詳しくは、 [https://help.marketing.yahoo.co.jp/en/?p=115](https://help.marketing.yahoo.co.jp/en/?p=115).

## Yandex 動的トラッキングパラメーター

詳しくは、 [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Adobe広告コンバージョントラッキングサービスのクリック追跡 URL の形式について](/help/search-social-commerce/tracking/formats-click-tracking-about.md)

