---
source-git-commit: 38d6d70d03c12aab1a7caee6e589a2fdeaf78ad4
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---
# Microsoft Advertising エンティティ用のトラッキングテンプレートフィールド

<!-- Search CRUD and bulk edit of Microsoft entity settings -->

**[!UICONTROL Tracking Template]:** （オプション。すべてのエンティティに使用できません）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL です。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

Adobe Advertisingコンバージョントラッキングの場合。これは、キャンペーン設定で「[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。

* 最終的な URL を埋め込むためにサポートされているパラメーターについては、 [[!DNL Microsoft Advertising] 最終 URL を示すパラメーターに関するドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799).

* オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます。例えば、 {lpurl}?matchtype={matchtype}&amp;device={device}.

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

<!-- Some entities may need additional/different notes. Try to keep this applicable to all MS entities. -->

>[!NOTE]
>
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* 広告を承認用に再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。
