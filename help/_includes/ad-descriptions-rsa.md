---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '144'
ht-degree: 0%

---
# RSA 広告設定の「広告の説明」フィールド

**[!UICONTROL Ad Descriptions]:** オプションの位置ピンを備えた、少なくとも 2 つ、最大 4 つの広告の説明。 広告ネットワークには、最大 2 つの説明を持つ広告が表示されます。少なくとも 2 つを入力してください。 各説明の最大の長さは、任意の動的テキスト（キーワードの値や広告のカスタマイズ子など）を含む 90 文字です。

広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

特定の位置に説明を固定するには、ピンオプション ([!UICONTROL Pinned at position 1]&quot;) です。 各位置に対して、少なくとも 1 つの説明を使用できる必要があります。 複数の説明を同じ位置にピン留めすると、最終的な広告には、指定した位置にそれらの説明の 1 つが常に含まれます。 位置 2 に固定された説明は、広告と共に表示されない場合があります。

説明を追加するには、 **[!UICONTROL + Add]**.
