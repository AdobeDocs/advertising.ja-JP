---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定の「トラッキングレベル」フィールド

**[!UICONTROL Tracking Level]:** ( の [!UICONTROL EF Redirect] ただ、アカウントレベルとキャンペーンレベルで使用可能（並列追跡が有効な広告ネットワークに適用できない）リダイレクトを追加し（関連する場合）、関連する URL にパラメーターを追加することで、クリック数と売上高を追跡する必要があるレベル。

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡する。

* *[!UICONTROL Ad]:* 広告レベルでのみデータを追跡する場合。

   **注意：** 既存のキャンペーンをこの設定に変更すると、既存のキーワードトラッキング ID がすべて削除されます。 また、1 つの広告に複数のランディングページを使用して多変量分析テストを実行する場合は、バルクシートファイルを作成し、必要なコンポーネントに対して編集します。

* *[!UICONTROL Keyword and Ad]:* キーワードレベルと広告レベルの両方でデータを追跡する。

**メモ：**

* 「[!UICONTROL Keyword]」は [!DNL Naver].
* 「[!UICONTROL Ad]」は [!DNL Yandex].
