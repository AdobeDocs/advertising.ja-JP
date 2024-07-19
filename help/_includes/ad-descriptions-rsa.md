---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 0%

---
# RSA 広告設定の「広告の説明」フィールド

**[!UICONTROL Ad Descriptions]:** 少なくとも 2 つ、最大 4 つの広告の説明（オプションの位置ピンを含む）。 広告ネットワークには、最大 2 つの説明を持つ広告が表示されます。少なくとも 2 つ入力します。 各説明の最大長は 90 文字で、動的テキスト（キーワードの値や広告カスタマイズ機能の値など）も含まれます。

広告カスタマイズ機能を挿入するには、次の形式を使用します（`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です）。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

説明を特定の位置にピン留めするには、ピンオプション（「[!UICONTROL Pinned at position 1]」など）を選択します。 各職位に対して少なくとも 1 つの説明を使用できる必要があります。 複数の説明を同じ位置にピン留めする場合、最終的な広告には常に、指定した位置にこれらの説明の 1 つが含まれます。 位置 2 にピン留めされた説明は、広告では表示されない場合があります。

説明を追加するには、「**[!UICONTROL + Add]**」をクリックします。
