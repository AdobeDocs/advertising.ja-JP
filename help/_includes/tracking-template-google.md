---
source-git-commit: 287e8bd0c2a3c3aedbf5f1f9551823b0c4586a57
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 0%

---
# [!DNL Google Ads] エンティティのトラッキングテンプレートフィールド

<!-- Search CRUD and bulk edit of Google entity settings -->

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
