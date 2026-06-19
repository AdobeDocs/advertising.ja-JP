---
title: クリックトラッキング URLのオプションのトラッキングパラメーター
description: オプションの検索、ソーシャル、およびCommerce トラッキングパラメーターと、クリックトラッキング URLに追加できる広告ネットワーク固有のトラッキングパラメーターについて説明します。
exl-id: df53bb8c-63ad-47f9-af44-57bd4bd58d71
feature: Search Tracking
TQID: https://experienceleague.adobe.com/6T2yZGYK-Mp97D0YRqPoS7Qyb5gp8jX-boK6KQjHB2E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 1113
ht-degree: 0%

---

# クリックトラッキング URLのオプションのトラッキングパラメーター

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]および[!DNL Yandex] アカウントのみ*

最終的なURLまたは宛先URLに対して標準のトラッキングパラメーターのみを使用する代わりに、広告ネットワークアカウントの特定のデータを追跡するためにより多くのパラメーターを追加できます。 アカウント設定またはキャンペーン設定では、次のパラメーターの任意の組み合わせを追加できます。

* 任意の静的テキスト文字列を、アカウント/キャンペーンのベース URLのパラメーターとして追加できます。

* アカウント/キャンペーンのベース URLにAdobe Advertising固有および広告ネットワーク固有のパラメーターを追加して、より多くのデータをトラッキングできます。

   * Adobe Advertising パラメーターは半静的です。 Adobe Advertisingは、ベース URLをアドネットワークにアップロードするときにデータ値を挿入します。 例えば、ベース URLに`campaign={ef_campaign}`を追加すると、URLをアップロードするときに、Adobe Advertisingは`{ef_campaign}`を実際のキャンペーン名（「Back-to-school-Campaign」など）に置き換えます。

     **メモ：**&#x200B;値を挿入すると、静的なままになります。 キーワードまたは広告を別の広告グループに移動する場合、または広告グループを別のキャンペーンに移動する場合、{ef_adgroup}または{ef_campaign} パラメーターは自動的に更新されないため、新しい宛先URLまたはベース（最終） URLを手動で生成する必要があります。

   * 広告ネットワーク固有のパラメーターは動的であり、ユーザーが広告をクリックすると、検索エンジンがデータ値を挿入します。 例えば、ベース URLに`{param1}`を追加すると、エンドユーザーが広告をクリックしたときに、広告ネットワークは実際の{param1}値に置き換えます。

>[!NOTE]
>
>* コンマまたはアンパサンド （`&`）で複数のパラメーターを区切ります。
>* 次のパラメーターでは、大文字と小文字は区別されません。
>* 追加されたパラメーター内の特殊文字は、生成された宛先URLまたはベース（最終） URLで次のように置換されます。
>  * `=`は`%3D`に置換されています
>  * `?`は`%26`に置換されています
>  * 空のスペースは`%2B`で置き換えられます
>  例えば、キーワードのベース URL http://www.example.comにパラメーター`campaign={ef_campaign}`を追加すると、そのキーワードのベース URLは`http://www.example.com/campaign%3D{ef_campaign}`として生成されます。

## Search, Social, &amp; Commerceの静的トラッキングパラメーター

任意の広告ネットワーク上のアカウントに対して次のパラメーターを使用でき、必要に応じて特定の広告ネットワークのパラメーターと組み合わせることができます。 これらのパラメーターの一部は、アカウントのトラッキング方法が「[!UICONTROL EF Direct]」の場合に特定の広告ネットワークに自動的に追加されるパラメーターを複製します。

次のすべてのパラメーターは、キーと値のペアとして指定する必要があります。1つの値のペアに複数のパラメーターを含めることができます。 例えば、キャンペーン名を挿入するには、`campaign={ef_campaign}`など`<your_parameter_name>={ef_campaign}`を使用します。 指定された一致タイプ名を使用して一致タイプを挿入するには、`matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`など`<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`を使用します。 該当しない一致タイプは、結果のURLに表示されません。

| パラメーター | 説明 |
| ---- | ---- |
| <code>{custom_code}</code> | アップロードされたバルクシートファイルの「カスタム URL パラメーター」列のデータをトラッキング URLに挿入するには、次の手順を実行します。 {custom_code}は、トラッキング URLの1つ以上のキーと値のペアの値の末尾でのみ使用できます。 例：<code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b> バルクシート ファイルのカスタム値をトラッキング URLに挿入するには、「トラッキング URLを生成」オプションを使用してバルクシート ファイルをアップロードします。 バルクシート ファイルの使用について詳しくは、「[&#x200B; バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)」を参照してください。 |
| <code>{ef_uniqueid}</code> | Adobe Advertisingで作成された一意のIDを挿入します。 トラッキング方法が「EF リダイレクト」の場合に自動的に追加されます。 |
| <code>{ef_userid}</code> | Adobe Advertisingが広告主に割り当てる一意のユーザーIDを挿入します。 |
| <code>{ef_sid}</code> | Search, Social, &amp; Commerceが広告ネットワークに割り当てる数値IDを挿入するには：<i>[!UICONTROL 3]</i> for [!DNL Google Ads], <i>[!UICONTROL 10]</i> for [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> for [!DNL Meta], <i>[!UICONTROL 86]</i> for [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> for [!DNL Naver], [!DNL Baidu], <i>[!UICONTROL 88]</i>, <i>[!UICONTROL 90]</i> for [!DNL Yandex], <i>[!UICONTROL 94]</i> for [!DNL LY Ads] （旧称[!DNL Yahoo! Japan Ads]）, <i>[!UICONTROL 105]</i> for [!DNL Yahoo Native] （非推奨）, <i>[!UICONTROL 106]</i> （非推奨）。[!DNL Pinterest] |
| <code>{ef_searchengine}</code> | 広告ネットワーク名を挿入します。 |
| <code>{ef_campaign}</code> | キャンペーン名を挿入します。 |
| <code>{ef_campaignid}</code> | キャンペーン IDを挿入します。 <b>注意：</b>新しいキャンペーンのIDは、キャンペーンが広告ネットワークに投稿されるまで作成されません。 アカウントが「[!UICONTROL EF Redirect]」および「自動アップロード」オプションを使用している場合、Adobe Advertisingは関連する宛先URLまたは最終版URLにキャンペーン IDを翌日に自動的に挿入します。 アカウントで「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションが使用されておらず、キャンペーン IDを関連する宛先URLまたは最終的なURLに挿入する場合は、キャンペーンを作成し、「トラッキング URLを生成」オプションを使用して新しいキャンペーンのバルクシート ファイルをダウンロードしてから、ファイルを広告ネットワークに投稿する必要があります。 |
| <code>{ef_adgroup}</code> | 広告グループ名を挿入します。 |
| <code>{ef_adgroupid}</code> | 広告グループ IDを挿入します。 <b>注意：</b>新しい広告グループのIDは、広告グループが広告ネットワークに投稿されるまで作成されません。 アカウントが「[!UICONTROL EF Redirect]」および「自動アップロード」オプションを使用している場合、Adobe Advertisingは関連する宛先URLまたは最終的なURLに広告グループ IDを翌日に自動的に挿入します。 アカウントで[!UICONTROL EF Redirect] オプションと[!UICONTROL Auto Upload] オプションが使用されておらず、関連する宛先URLまたは最終的なURLに広告グループ IDを挿入する場合は、広告グループを作成し、「トラッキング URLを生成」オプションを使用して新しい広告グループのバルクシート ファイルをダウンロードしてから、ファイルを広告ネットワークに投稿する必要があります。 |
| <code>{ef_keyword}</code> | キーワードを挿入します。 |
| <code>{ef_keywordid}</code> | キーワード IDを挿入します。 <b>注意：</b>新しいキーワードのIDは、キーワードが広告ネットワークに投稿されるまで作成されません。 アカウントが「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用している場合、Adobe Advertisingは関連する宛先URLまたは最終版URLにキーワード IDを自動的に挿入します。 アカウントが「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用しておらず、関連する宛先URLまたは最終的なURLにキーワード IDを挿入する場合は、キーワードを作成し、「トラッキング URLを生成」オプションを使用して新しいキーワードのバルクシート ファイルをダウンロードしてから、ファイルを広告ネットワークに投稿する必要があります。 |
| <code>{ef_matchtype}</code> | キーワード一致タイプを「Broad」、「Exact」、「Phrase」として挿入するには、次の手順を実行します。 「[!UICONTROL EF Redirect]」トラッキングメソッドを使用して、[!DNL Google Ads]と[!DNL Microsoft Advertising]に対して自動的に含まれます。 |
| <code>{ef_adid}</code> | 追加する必要があります。 <b>注意：</b>新しい広告のIDは、広告が広告ネットワークに投稿されるまで作成されません。 アカウントが「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用している場合、Adobe Advertisingは関連する宛先URLまたは最終版URLに広告IDを自動的に挿入します。 アカウントが「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」オプションを使用しておらず、広告IDを関連する宛先URLまたは最終的なURLに挿入する場合は、広告を作成する必要があります。新しい広告のバルクシート ファイルをダウンロードし、「トラッキング URLを生成」オプションを使用して、ファイルを広告ネットワークに投稿します。 |

## 動的トラッキングパラメーター[!DNL Google Ads]

[https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447)を参照してください。

## 動的トラッキングパラメーター[!DNL LY Ads]

[https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US)を参照してください。

## 動的トラッキングパラメーター[!DNL Microsoft Advertising]

[https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2)を参照してください。

## 動的トラッキングパラメーター[!DNL Yandex]

[https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html)を参照してください。

>[!MORELIKETHIS]
>
>* [Adobe Advertising コンバージョントラッキングサービスのクリックトラッキング URL形式について](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
