---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# テキスト広告テンプレート — キャンペーンレベルの除外キーワード設定

**[!UICONTROL Delete negative keywords when omitted from list]:** (Yandex を除くすべての広告ネットワーク。（オプション）以下のリストで指定されていないテンプレートを使用して以前に作成した、既存のキャンペーンレベルの除外キーワードを削除します。 **注意：** 他の方法（プレーンバルクシートの場合など）を使用して作成された除外キーワード [!UICONTROL Campaigns] 表示や広告ネットワークの広告エディターで ) は、テンプレートを使用して削除されることはありません。

**[!UICONTROL Set negative keywords by campaign name condition]:** (Yandex を除くすべての広告ネットワーク。（オプション）指定した文字列を名前に含むキャンペーンの除外キーワードを指定できます。 このオプションを選択すると、最大 3 つのキャンペーン名文字列と、対応するキーワードを追加できます。

各文字列に対して、 **[!UICONTROL Add (Up to 3)]** 次の情報を入力します。

* **[!UICONTROL If campaign name contains]:**  キャンペーン名内の任意の場所を検索するテキスト文字列。 クエリでは大文字と小文字が区別されます（例： ）。[!DNL Car]&quot;キャンペーン名&quot;に一致[!DNL Car Parts]&quot;は、&quot;[!DNL INTERIOR CAR ACCESSORIES]&quot;) です。

* **[!UICONTROL Apply these negatives]:**  指定した文字列を名前に含むキャンペーンに追加する、静的なキャンペーンレベルの除外キーワード。 同じキーワードに複数のキーワードまたは複数の一致タイプを指定するには、それぞれを別々の行に入力します。 マイナス記号を付けずに、次の構文を使用します。

   * 負の部分一致： `keyword` ( ではサポートされていません。 [!DNL Microsoft Advertising])
   * 否定的なフレーズ一致： `"keyword"`
   * 負の完全一致： `[keyword]`

フレーズおよび完全一致タイプの通常の構文は、フィードデータをテンプレートを介して伝達する際に生成されるバルクシートで使用されます。 **注意：** 除外キーワードは [!UICONTROL Keywords] タブまたは [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示

**[!UICONTROL All other campaigns: Apply these negatives]:** ( 以下を除くすべての広告ネットワーク [!DNL Yandex];（オプション）名前が指定の文字列と一致しないキャンペーンに追加する、静的なキャンペーンレベルの除外キーワード。 同じキーワードに複数のキーワードまたは複数の一致タイプを指定するには、それぞれを別々の行に入力します。 マイナス記号を付けずに、次の構文を使用します。

* 負の部分一致： `keyword` ( ではサポートされていません。 [!DNL Microsoft Advertising])
* 否定的なフレーズ一致： `"keyword"`
* 負の完全一致： `[keyword]`

フレーズおよび完全一致タイプの通常の構文は、フィードデータをテンプレートを介して伝達する際に生成されるバルクシートで使用されます。 **注意：** 除外キーワードは [!UICONTROL Keywords] タブまたは [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示
