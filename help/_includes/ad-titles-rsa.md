---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '147'
ht-degree: 0%

---
# RSA 広告設定の「広告タイトル」フィールド

**[!UICONTROL Ad Titles]:** オプションの位置ピンを使用して、少なくとも 3 つの広告タイトル（ヘッドライン）と最大 15 の広告タイトル。 広告ネットワークには、最大 3 つのヘッドラインを持つ広告が表示されます。少なくとも 3 つ入力します。 各タイトルの最大長は、動的を含めて 30 文字です
テキスト（キーワードや広告カスタマイズ機能の値など）。

広告カスタマイズ機能を挿入するには、次の形式を使用します（`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です）。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

タイトルを特定の位置にピン留めするには、ピンオプション（「[!UICONTROL Pinned at position 1]」など）を選択します。 各職位に対して少なくとも 1 つのタイトルを使用できる必要があります。 複数のタイトルを同じ位置に固定した場合、最終的な広告には常に、指定した位置にこれらのタイトルの 1 つが含まれます。 位置 3 にピン留めされたタイトルは、広告では表示されない場合があります。

タイトルを追加するには、「**[!UICONTROL + Add]**」をクリックします。
