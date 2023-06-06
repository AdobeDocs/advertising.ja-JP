---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---
# テキスト広告テンプレート — 広告グループレベルの除外キーワード設定

**[!UICONTROL Delete negative keywords when omitted from list]:** (Yandex を除くすべての広告ネットワーク。（オプション）以下のリストに指定されていないテンプレートを使用して以前に作成した、既存の広告グループレベルの除外キーワードを削除します。 **注意：** 他の方法（プレーンバルクシートの場合など）を使用して作成された除外キーワード [!UICONTROL Campaigns] 表示や広告ネットワークの広告エディターで ) は、テンプレートを使用して削除されることはありません。

**[!UICONTROL Apply these negatives]:** ( 以下を除くすべての広告ネットワーク [!DNL Yandex];（オプション）追加する静的な広告グループレベルの除外キーワード。 同じキーワードに複数のキーワードまたは複数の一致タイプを指定するには、それぞれを別々の行に入力します。 マイナス記号を付けずに、次の構文を使用します。

* 負の部分一致： `keyword` ( ではサポートされていません。 [!DNL Microsoft Advertising])
* 否定的なフレーズ一致： `"keyword"`
* 負の完全一致： `[keyword]`

フレーズおよび完全一致タイプの通常の構文は、フィードデータをテンプレートを介して伝達する際に生成されるバルクシートで使用されます。 **注意：** 除外キーワードは [!UICONTROL Keywords] タブまたは [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] 表示
