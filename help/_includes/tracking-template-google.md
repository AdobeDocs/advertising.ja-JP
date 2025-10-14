---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Google Ads エンティティのトラッキングテンプレートフィールド

<!-- Search CRUD and bulk edit of Google entity settings -->

**[!UICONTROL Tracking Template]:** （任意） トラッキングテンプレートまたはトラッキング URL。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL を [!DNL ValueTrack] パラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的に設定されます。

* 最終的な URL を埋め込むためのサポート対象パラメーターについては、[[!DNL Google Ads]  サポート対象の形式に関するドキュメント  [!DNL ValueTrack]  を参照してください &#x200B;](https://support.google.com/google-ads/answer/6305348)。 （「使用可能なテンプレートのパラメーター」のセクションの「トラッキングテンプレー [!DNL ValueTrack] のみ」パラメーターに移動します。）

* オプションで、{lpurl}?matchtype={matchtype}&amp;device={device} のようにアンパサンド（&amp;）で区切られた URL パラメーターと、キャンペーンに定義されたカスタムパラメーターを含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* マクロを使用しないでください。このマクロは、並列トラッキングを有効にするソースからのクリックに代わるものではありません。 広告主がマクロを使用する必要がある場合、Adobeアカウントチームはカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告、サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。
