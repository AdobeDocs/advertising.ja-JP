---
source-git-commit: 287e8bd0c2a3c3aedbf5f1f9551823b0c4586a57
workflow-type: tm+mt
source-wordcount: '524'
ht-degree: 0%

---
# スニペット

## [!DNL Google Ads] エンティティのトラッキングテンプレートフィールド {#tracking-template-google}

<!-- Duplicated from include file because one file has multiple occurrences, which ExL doesn't support. -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページのURLを[!DNL ValueTrack] パラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceは自動的に独自のリダイレクトコードとトラッキングコードの先頭に付けられます。

* サポートされているパラメーターを使用して最終的なURLを埋め込む場合は、サポートされている[[!DNL Google Ads] 形式 [!DNL ValueTrack] の](https://support.google.com/google-ads/answer/6305348) ドキュメントを参照してください。 （「使用可能な[!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ」パラメーターに移動します）。

* 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターをアンパサンド（&amp;）で区切って含めることができます（{lpurl}?matchtype={matchtype}&amp;device={device}など）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* 並列追跡を有効にするソースからのクリックに代わるものではないマクロの使用は避けてください。 広告主がマクロを使用する必要がある場合は、Adobe アカウントチームがカスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンク、またはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 承認のために広告を再送信することなく、アカウントレベル、キャンペーンレベル、広告グループレベルでトラッキングテンプレートを更新できます。

## [!DNL Microsoft Advertising] エンティティのトラッキングテンプレートフィールド {#tracking-template-microsoft}

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページのURLをパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceは自動的に独自のリダイレクトコードとトラッキングコードの先頭に付けられます。

* サポートされているパラメーターに最終的なURLを埋め込む場合は、パラメーターに関する[[!DNL Microsoft Advertising]  ドキュメントを参照して、最終的なURL](https://help.ads.microsoft.com/#apex/3/en/56799)を示してください。

* 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターをアンパサンド（&amp;）で区切って含めることができます（{lpurl}?matchtype={matchtype}&amp;device={device}など）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 承認のために広告を再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。

## テキスト広告テンプレート – 動的パラメーターの挿入方法を説明するメモ {#inventory-feed-template-insert-dynamic-parameter}

列名または修飾子グループを動的パラメーターとして挿入するには、入力フィールドをクリックし、列リストの列名または修飾子リストの[修飾子名](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md)をクリックします。 [!DNL Param1]または[!DNL Param2]変数を挿入するには、値`{param1:default text}`または`{param2:default text}`を入力します。ここで、「デフォルトテキスト」は、フィードファイルのパラメーター列が広告行に対して空の場合に使用されるテキストです。

## テキスト広告テンプレート – 広告カスタマイザーの挿入方法を説明するメモ {#inventory-feed-template-insert-ad-customizer}

広告カスタマイザーを挿入するには、次の形式を使用します。ここで、`Default text`は、フィードファイルに有効な値が含まれていない場合に挿入するオプション値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}` （例：`{CUSTOMIZER.Discount:10%}`）

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}` （例：`{CUSTOMIZER.Discount:10%}`）
