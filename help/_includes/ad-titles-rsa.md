---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---
# RSA 広告設定の「広告タイトル」フィールド

**[!UICONTROL Ad Titles]:** 少なくとも 3 つ、最大 15 の広告タイトル（ヘッドライン）、オプションの位置ピン付き。 広告ネットワークには、最大 3 つのヘッドラインを持つ広告が表示されます。3 つ以上の値を入力してください。 各タイトルの最大長は、任意の動的テキスト（キーワードの値や広告のカスタマイズ者など）を含む 30 文字です。

広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

タイトルを特定の位置に固定するには、ピンオプション ([!UICONTROL Pinned at position 1]&quot;) です。 各位置に少なくとも 1 つのタイトルを使用できる必要があります。 複数のタイトルを同じ位置に固定すると、最終的な広告には、指定した位置のタイトルの 1 つが常に含まれます。 位置 3 にピン留めされたタイトルは、広告と共に表示されない場合があります。

タイトルを追加するには、 **[!UICONTROL + Add]**.
