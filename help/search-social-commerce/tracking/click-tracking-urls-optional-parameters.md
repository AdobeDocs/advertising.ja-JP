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

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan]、および [!DNL Yandex] アカウントのみ*

最終的な URL または宛先 URL に標準のトラッキングパラメーターのみを使用する代わりに、広告ネットワークアカウントの特定のデータを追跡するパラメーターを追加できます。 アカウント設定またはキャンペーン設定で、次のパラメーターの任意の組み合わせを追加できます。

* アカウント/キャンペーンのベース URL のパラメーターとして、任意の静的テキスト文字列を追加できます。

* アカウント/キャンペーンのベース URL にAdobe Advertisingおよび広告ネットワーク固有のパラメーターを追加して、より多くのデータを追跡できます。

   * Adobe Advertisingパラメーターは半静的です。 Adobe Advertisingが広告ネットワークにベース URL をアップロードする際に、データ値を挿入します。 例えば、を追加する場合 `campaign={ef_campaign}` Adobe Advertisingは、をベース URL に置き換えます。 `{ef_campaign}` URL をアップロードする際の実際のキャンペーン名（「Back-to-school-Campaign」など）を指定します。

     **注意：** 値が挿入されると、値は静的なままになります。 キーワードまたは広告を別の広告グループに移動した場合、または広告グループを別のキャンペーンに移動した場合、  {ef_adgroup} または {ef_campaign} パラメーターは自動的に更新されないので、新しい宛先 URL またはベース（最終的） URL を手動で生成する必要があります。

   * 広告ネットワーク固有のパラメーターは動的であり、ユーザーが広告をクリックすると、検索エンジンによってデータ値が挿入されます。 例えば、を追加する場合 `{param1}` 広告ネットワークにより、ベース URL が実際の URL に置き換えられます {param1} エンドユーザーが広告をクリックしたときの値。

>[!NOTE]
>
>* 複数のパラメーターはコンマまたはアンパサンド（`&`）に設定します。
>* 次のパラメーターでは、大文字と小文字が区別されません。
>* 追加されたパラメーターの特殊文字は、生成された宛先 URL またはベース（最終） URL で次のように置き換えられます。
>  * `=` がに置き換えられます `%3D`
>  * `?` がに置き換えられます `%26`
>  * 空のスペースがで置き換えられます `%2B`
>  例えば、パラメーター `campaign={ef_campaign}` をキーワードのベース URL http://www.example.comに送信すると、そのキーワードのベース URL は次のように生成されます `http://www.example.com/campaign%3D{ef_campaign}`.

## 検索、ソーシャル、Commerceの静的トラッキングパラメーター

任意の広告ネットワーク上のアカウントに対して以下のパラメーターを使用し、必要に応じて特定の広告ネットワークのパラメーターと組み合わせることができます。 これらのパラメーターの一部は、アカウントのトラッキング方法が「」の場合に、特定の広告ネットワークに自動的に追加されるパラメーターと重複します[!UICONTROL EF Direct].」と入力します。

次のパラメーターはすべて、キーと値のペアとして指定する必要があります。1 つの値のペアに複数のパラメーターを含めることができます。 例えば、キャンペーン名を挿入するには、を使用します `<your_parameter_name>={ef_campaign}`（例：） `campaign={ef_campaign}`. 指定した一致タイプ名を使用して一致タイプを挿入するには、を使用します `<your_parameter_name>={ef_mt_broad:<value>}{ef_mt_exact:<value>}{ef_mt_phrase:<value>}`（例：） `matchtype={ef_mt_broad:<b>}{ef_mt_exact:<e>}{ef_mt_phrase:<p>}`. 適用されない一致タイプは、結果の URL には表示されません。

| パラメーター | 説明 |
| ---- | ---- |
| <code>{custom_code}</code> | アップロードしたバルクシートファイルの「カスタム URL パラメーター」列のデータをトラッキング URL に挿入します。 {custom_code} は、トラッキング URL の 1 つ以上のキーと値のペアの値の末尾でのみ使用できます。 例：  <code>a={custom_code}</code>; <code>a={ef_campaignid}{custom_code}</code>; <code>a={ef_campaignid}{custom_code}&amp;b={custom_code}</code><br><br><b>注意：</b> バルクシートファイルのカスタム値をトラッキング URL に挿入するには、「トラッキング URL を生成」オプションを使用してバルクシートファイルをアップロードします。 バルクシート ファイルの使用方法の詳細については、を参照してください。[バルクシートを使用した Campaign データの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).」と入力します。 |
| <code>{ef_uniqueid}</code> | Adobe Advertisingで作成された一意の ID を挿入します。 追跡方法が「EF リダイレクト」の場合に自動的に追加されます。 |
| <code>{ef_userid}</code> | 広告主に割り当てる一意のAdobe AdvertisingID を挿入する。 |
| <code>{ef_sid}</code> | 検索、ソーシャルおよびCommerceによって広告ネットワークに割り当てられる数値 ID を挿入するには： <i>[!UICONTROL 3]</i> （用） [!DNL Google Ads], <i>[!UICONTROL 10]</i> （用） [!DNL Microsoft Advertising], <i>[!UICONTROL 45]</i> （用） [!DNL Meta], <i>[!UICONTROL 86]</i> （用） [!DNL Yahoo! Display Network], <i>[!UICONTROL 87]</i> （用） [!DNL Naver], <i>[!UICONTROL 88]</i> （用） [!DNL Baidu], <i>[!UICONTROL 90]</i> （用） [!DNL Yandex], <i>[!UICONTROL 94]</i> （用） [!DNL Yahoo! Japan Ads], <i>[!UICONTROL 105]</i> （用） [!DNL Yahoo Native] （非推奨）、または <i>[!UICONTROL 106]</i> （用） [!DNL Pinterest] （非推奨）。 |
| <code>{ef_searchengine}</code> | 広告ネットワーク名を挿入します。 |
| <code>{ef_campaign}</code> | キャンペーン名を挿入します。 |
| <code>{ef_campaignid}</code> | キャンペーン ID を挿入します。 <b>注意：</b> 新しいキャンペーンの ID は、キャンペーンが広告ネットワークに投稿されるまで作成されません。 アカウントが「」を使用している場合[!UICONTROL EF Redirect]「」および「自動アップロード」オプションを選択すると、Adobe Advertisingは関連するリンク先 URL または最終 URL にキャンペーン ID を翌日自動的に挿入します。 アカウントで「」が使用されていない場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「オプションがあり、関連する宛先 URL または最終 URL にキャンペーン ID を挿入する場合は、キャンペーンを作成し、「トラッキング URL を生成」オプションを使用して新しいキャンペーンのバルクシートファイルをダウンロードした後、ファイルを広告ネットワークに POST する必要があります。 |
| <code>{ef_adgroup}</code> | 広告グループ名を挿入します。 |
| <code>{ef_adgroupid}</code> | 広告グループ ID を挿入します。 <b>注意：</b> 新しい広告グループの ID は、広告グループが広告ネットワークに投稿されるまで作成されません。 アカウントが「」を使用している場合[!UICONTROL EF Redirect]「」および「自動アップロード」オプションを選択すると、Adobe Advertisingは関連するリンク先 URL または最終的な URL に翌日、広告グループ ID を自動的に挿入します。 アカウントがを使用していない場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「オプションがあり、関連する宛先 URL または最終 URL に広告グループ ID を挿入する場合は、広告グループを作成し、「トラッキング URL を生成」オプションを使用して新しい広告グループのバルクシートファイルをダウンロードした後、ファイルを広告ネットワークに POST します。 |
| <code>{ef_keyword}</code> | キーワードを挿入します。 |
| <code>{ef_keywordid}</code> | キーワード ID を挿入します。 <b>注意：</b> 新しいキーワードの ID は、そのキーワードが広告ネットワークに投稿されるまで作成されません。 アカウントが「」を使用している場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「」オプションを選択すると、Adobe Advertisingは関連するリンク先 URL または最終的な URL に、翌日にキーワード ID を自動的に挿入します。 アカウントで「」が使用されていない場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「オプションがあり、関連する宛先 URL または最終 URL にキーワード ID を挿入する場合は、キーワードを作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しいキーワードのバルクシートファイルをダウンロードし、ファイルを広告ネットワークに POST します。 |
| <code>{ef_matchtype}</code> | キーワード一致を挿入するには、「部分一致」、「完全一致」、または「フレーズ」と入力します。 に自動的に含まれる [!DNL Google Ads] および [!DNL Microsoft Advertising] （が「[!UICONTROL EF Redirect]「トラッキング方法。 |
| <code>{ef_adid}</code> | 広告 ID を挿入します。 <b>注意：</b> 新しい広告の ID は、広告が広告ネットワークに投稿されるまで作成されません。 アカウントが「」を使用している場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「」オプションを選択すると、Adobe Advertisingは関連するリンク先 URL または最終的な URL に翌日、広告 ID を自動的に挿入します。 アカウントで「」が使用されていない場合[!UICONTROL EF Redirect]``と [!UICONTROL Auto Upload]「オプション」を選択し、関連する宛先 URL または最終 URL に広告 ID を挿入する場合は、広告を作成する必要があります。「トラッキング URL を生成」オプションを使用して、新しい広告のバルクシートファイルをダウンロードし、ファイルを広告ネットワークに POST します。 |

## [!DNL Google Ads] 動的トラッキングパラメーター

参照： [https://support.google.com/google-ads/answer/2375447](https://support.google.com/google-ads/answer/2375447).

## [!DNL Microsoft Advertising] 動的トラッキングパラメーター

参照： [https://help.bingads.microsoft.com/#apex/3/en/51091/2](https://help.bingads.microsoft.com/#apex/3/en/51091/2).

## Yahoo! 日本広告の動的トラッキングパラメーター

参照： [https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US](https://ads-help.yahoo-net.jp/s/article/H000044463?language=en_US).

## [!DNL Yandex] 動的トラッキングパラメーター

参照： [https://yandex.com/support/direct/statistics/url-tags.html](https://yandex.com/support/direct/statistics/url-tags.html).

>[!MORELIKETHIS]
>
>* [Adobe Advertisingコンバージョントラッキングサービスのクリックトラッキング URL 形式について](/help/search-social-commerce/tracking/formats-click-tracking-about.md)
