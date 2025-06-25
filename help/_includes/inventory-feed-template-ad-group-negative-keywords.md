---
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# テキスト広告テンプレート – 広告グループレベルの負のキーワード設定

**[!UICONTROL Delete negative keywords when omitted from list]:** （Yandex を除くすべての広告ネットワーク、オプション）以下のリストで指定されていないテンプレートを使用して以前に作成した既存の広告グループレベルの負のキーワードを削除します。 **メモ：** 他の手段（プレーンバルクシート、[!UICONTROL Campaigns] ビュー、広告ネットワークの広告エディターなど）で作成されたネガティブキーワードが、テンプレートを使用して削除されることはありません。

**[!UICONTROL Apply these negatives]:** （[!DNL Yandex] を除くすべての広告ネットワーク。オプション）追加する静的広告グループレベルの負のキーワード。 同じキーワードに対して複数のキーワードまたは複数の一致タイプを指定するには、別々の行に入力します。 マイナス記号を使用せずに、次の構文を使用します。

* 負の部分一致：`keyword` （[!DNL Microsoft Advertising] ではサポートされていません）
* 負の語句の一致：`"keyword"`
* 完全一致が負の数：`[keyword]`

フレーズと完全一致のタイプの慣習的な構文は、テンプレートを通じてフィードデータを伝播する際に生成されるバルクシートで使用されます。 **メモ：** 負のキーワードは、「[!UICONTROL Keywords]」タブまたは [!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns] 表示には表示されません。
