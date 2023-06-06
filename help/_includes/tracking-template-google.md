---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 0%

---
# Google Ads エンティティの「トラッキングテンプレート」フィールド

<!-- Search CRUD and bulk edit of Google entity settings -->

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

