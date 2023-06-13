---
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '100'
ht-degree: 0%

---
# 一部の広告設定で、「パス 1 」と「パス 2 を表示」フィールドを表示します

**[!UICONTROL Display Path 1]**, **[!UICONTROL Display Path 2]:** （オプション）最終的な URL から自動的に抽出される表示 URL に追加されるテキスト。 各パスの前には URL のスラッシュ (`/`) をクリックします。 パスにスラッシュ (`/`) または改行 (`\n`) 文字を使用します。 各パスの最大長は 15 文字または 2 バイト文字 7 文字です。

広告カスタマイズ機能を挿入するには、次の形式を使用します。 `Default text` は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。

* [!DNL Google Ads]: `{CUSTOMIZER.AdCustomizerName:Default text}, such as {CUSTOMIZER.Discount:10%}`

* [!DNL Microsoft Advertising]: `{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`

例えば、 [!UICONTROL Display Path 1] は「契約」で、 [!UICONTROL Display Path 2] が「local」の場合、表示 URL は `<display URL>/deals/local`www.example.com/deals/localなど。
