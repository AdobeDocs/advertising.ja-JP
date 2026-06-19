---
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: '137'
ht-degree: 0%

---
# [!DNL LY Ads] エンティティのトラッキングテンプレートフィールド

<!-- Search CRUD and bulk edit of LY Ads entity settings -->

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページのURLをパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 パラメーター`!{lpurl}`を使用して、ランディングページ URLを示します。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceは自動的に独自のリダイレクトコードとトラッキングコードの先頭に付けられます。

>[!NOTE]
>
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 承認のために広告を再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。
