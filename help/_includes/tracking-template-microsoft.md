---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Microsoft Advertising エンティティのトラッキングテンプレートフィールド

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** （オプション。すべてのエンティティで使用できるわけではありません） トラッキングテンプレートまたはトラッキング URL。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれる場合に適用されるAdobe Advertisingコンバージョントラッキングの場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的に設定されます。

* 最終 URL を埋め込むためにサポートされているパラメーターについては、[[!DNL Microsoft Advertising]  パラメーターに関するドキュメントを参照して最終 URL を示します &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799)。

* オプションで、{lpurl}?matchtype={matchtype}&amp;device={device} のようにアンパサンド（&amp;）で区切られた URL パラメーターと、キャンペーンに定義されたカスタムパラメーターを含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* 広告を承認用に再送信しなくても、任意のレベルでトラッキングテンプレートを更新できます。
