---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '104'
ht-degree: 0%

---
# 一部の広告設定で「パス 1」フィールドと「パス 2」フィールドを表示

**[!UICONTROL Display Path 1]**、**[!UICONTROL Display Path 2]:** （任意）最終的な URL から自動的に抽出された、表示 URL に追加されるテキスト。 URL 内の各パスの前には、スラッシュ（`/`）が付きます。 パスには、スラッシュ（`/`）や改行（`\n`）を含めることはできません。 各パスの最大長は 15 文字または 7 つの 2 バイト文字です。

広告カスタマイズ機能を挿入するには、次の形式を使用します（`Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です）。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

例えば、[!UICONTROL Display Path 1] が「deals」、[!UICONTROL Display Path 2] が「local」の場合、表示 URL は `<display URL>/deals/local` になります（例：www.example.com/deals/local）。
