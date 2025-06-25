---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 0%

---
# テキスト広告テンプレート – キャンペーンレベルのネガティブキーワードの設定

**[!UICONTROL Delete negative keywords when omitted from list]:** （Yandex を除くすべての広告ネットワーク。オプション）以下のリストで指定されていないテンプレートを使用して以前に作成した既存のキャンペーンレベルのネガティブキーワードを削除します。 **メモ：** 他の手段（プレーンバルクシート、[!UICONTROL Campaigns] ビュー、広告ネットワークの広告エディターなど）で作成されたネガティブキーワードが、テンプレートを使用して削除されることはありません。

**[!UICONTROL Set negative keywords by campaign name condition]:** （Yandex；オプションを除くすべての広告ネットワーク）名前に指定の文字列が含まれるキャンペーンの負のキーワードを指定できます。 このオプションを選択した場合は、最大 3 つのキャンペーン名文字列と対応するキーワードを追加できます。

各文字列に対して「**[!UICONTROL Add (Up to 3)]**」をクリックし、次の情報を入力します。

* **[!UICONTROL If campaign name contains]:** キャンペーン名の中で検索するテキスト文字列。 クエリでは大文字と小文字が区別されます（例えば、「[!DNL Car]」はキャンペーン名「[!DNL Car Parts]」に一致しますが、「[!DNL INTERIOR CAR ACCESSORIES]」には一致しません）。

* **[!UICONTROL Apply these negatives]:** 名前に指定した文字列が含まれるキャンペーンに追加する、静的なキャンペーンレベルのネガティブキーワード。 同じキーワードに対して複数のキーワードまたは複数の一致タイプを指定するには、別々の行に入力します。 マイナス記号を使用せずに、次の構文を使用します。

   * 負の部分一致：`keyword` （[!DNL Microsoft Advertising] ではサポートされていません）
   * 負の語句の一致：`"keyword"`
   * 完全一致が負の数：`[keyword]`

フレーズと完全一致のタイプの慣習的な構文は、テンプレートを通じてフィードデータを伝播する際に生成されるバルクシートで使用されます。 **メモ：** 負のキーワードは、「[!UICONTROL Keywords]」タブまたは [!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] 表示には表示されません。

**[!UICONTROL All other campaigns: Apply these negatives]:** （[!DNL Yandex] を除くすべての広告ネットワーク。オプション）名前が指定した文字列に一致しないキャンペーンに追加する、静的なキャンペーンレベルのネガティブキーワード。 同じキーワードに対して複数のキーワードまたは複数の一致タイプを指定するには、別々の行に入力します。 マイナス記号を使用せずに、次の構文を使用します。

* 負の部分一致：`keyword` （[!DNL Microsoft Advertising] ではサポートされていません）
* 負の語句の一致：`"keyword"`
* 完全一致が負の数：`[keyword]`

フレーズと完全一致のタイプの慣習的な構文は、テンプレートを通じてフィードデータを伝播する際に生成されるバルクシートで使用されます。 **メモ：** 負のキーワードは、「[!UICONTROL Keywords]」タブまたは [!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] 表示には表示されません。
