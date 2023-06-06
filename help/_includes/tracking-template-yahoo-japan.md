---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---
# Yahoo！の「トラッキングテンプレート」フィールド 日本の広告事業者

<!-- Search CRUD and bulk edit of Yahoo! Japan Ads entity settings -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 パラメーターの使用 `!{lpurl}` をクリックして、ランディングページの URL を指定します。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

Adobe広告コンバージョントラッキングの場合。これは、キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。

>[!NOTE]
>
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* 広告を承認用に再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。

