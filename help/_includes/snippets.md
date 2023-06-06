---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '537'
ht-degree: 0%

---
# スニペット

## Google Ads エンティティの「トラッキングテンプレート」フィールド {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL を [!DNL ValueTrack] パラメーター。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。

* 最終的な URL を埋め込むためにサポートされているパラメーターについては、 [[!DNL Google Ads] documentation for the supported [!DNL ValueTrack] 形式](https://support.google.com/google-ads/answer/6305348). （「利用可能な値追跡パラメーター」の節の「追跡テンプレートのみ」パラメーターに移動）。

* オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます（例：{lpurl}?matchtype={matchtype}&amp;device={device}）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* 並列追跡を有効にするソースからのクリック数に代わられないマクロの使用は避けてください。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* 広告、サイトリンク、またはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告が再送信され、レビューが必要になります。 広告を承認用に再送信しなくても、アカウント、キャンペーンまたは広告グループレベルでトラッキングテンプレートを更新できます。


## Microsoft Advertising エンティティ用のトラッキングテンプレートフィールド {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。

* 最終的な URL を埋め込むためにサポートされているパラメーターについては、 [[!DNL Microsoft Advertising] 最終 URL を示すパラメーターに関するドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799).

* オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます（例：{lpurl}?matchtype={matchtype}&amp;device={device}）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* 広告を承認用に再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。


## テキスト広告テンプレート — 動的パラメーターの挿入方法を説明する注意事項 {#inventory-feed-template-insert-dynamic-parameter}

列名または修飾子グループを動的パラメータとして挿入するには、入力フィールドをクリックし、列リスト内の列名または [修飾子名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) を選択します。 次の手順で [!DNL Param1] または [!DNL Param2] 変数に値を入力するには、 `{param1:default text}` または `{param2:default text}`(「default text」は、フィードファイル内のパラメーター列が広告行で空の場合に使用されるテキストです。

## テキスト広告テンプレート — 広告カスタマイズ機能を挿入する方法を説明するメモ {#inventory-feed-template-insert-ad-customizer}

広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}`例： `{CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}`例： `{CUSTOMIZER.Discount:10%}`
