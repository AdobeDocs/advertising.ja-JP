---
source-git-commit: 92bf7768be91e75f029e1577c7f4e7e790c5a934
workflow-type: tm+mt
source-wordcount: '532'
ht-degree: 0%

---
# スニペット

## Google Ads エンティティのトラッキングテンプレートフィールド {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** （任意） トラッキングテンプレートまたはトラッキング URL。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL を [!DNL ValueTrack] パラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的に設定されます。

* 最終的な URL を埋め込むためのサポート対象パラメーターについては、[[!DNL Google Ads]  サポート対象の形式に関するドキュメント  [!DNL ValueTrack]  を参照してください ](https://support.google.com/google-ads/answer/6305348)。 （「使用可能なテンプレートのパラメーター」のセクションの「トラッキングテンプレー [!DNL ValueTrack] のみ」パラメーターに移動します。）

* オプションで、{lpurl}?matchtype={matchtype}&amp;device={device} のようにアンパサンド（&amp;）で区切られた URL パラメーターと、キャンペーンに定義されたカスタムパラメーターを含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* マクロを使用しないでください。このマクロは、並列トラッキングを有効にするソースからのクリックに代わるものではありません。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。

## [!DNL Microsoft Advertising] エンティティのトラッキングテンプレートフィールド {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** （任意） トラッキングテンプレートまたはトラッキング URL。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的に設定されます。

* 最終 URL を埋め込むためにサポートされているパラメーターについては、[[!DNL Microsoft Advertising]  パラメーターに関するドキュメントを参照して最終 URL を示します ](https://help.ads.microsoft.com/#apex/3/en/56799)。

* オプションで、{lpurl}?matchtype={matchtype}&amp;device={device} のようにアンパサンド（&amp;）で区切られた URL パラメーターと、キャンペーンに定義されたカスタムパラメーターを含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告を承認用に再送信しなくても、任意のレベルでトラッキングテンプレートを更新できます。

## テキストとテンプレート – 動的パラメーターの挿入方法を説明するメモ {#inventory-feed-template-insert-dynamic-parameter}

列名またはモディファイヤ グループを動的パラメータとして挿入するには、入力フィールド内をクリックし、列リスト内の列名または [ モディファイヤ ] リスト内の [ モディファイヤ名 ](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) をクリックします。 [!DNL Param1] または [!DNL Param2] 変数を挿入するには、値 `{param1:default text}` または `{param2:default text}` を入力します。「default text」は、広告行に対してフィードファイルのパラメーター列が空の場合に使用されるテキストです。

## テキスト広告テンプレート – 広告カスタマイザーの挿入方法を説明するメモ {#inventory-feed-template-insert-ad-customizer}

広告カスタマイズ機能を挿入するには、次の形式を使用します（`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です）。

* [!DNL Google Ads]:`{CUSTOMIZER.AdCustomizerName:Default text}` （`{CUSTOMIZER.Discount:10%}` など）

* [!DNL Microsoft Advertising]:`{CUSTOMIZER.Attribute name:Default text}` （`{CUSTOMIZER.Discount:10%}` など）
