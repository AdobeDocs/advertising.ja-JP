---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定のトラッキングレベル フィールド

**[!UICONTROL Tracking Level]:** （[!UICONTROL EF Redirect] のみ。アカウントレベルおよびキャンペーンレベルで使用可能。並列トラッキングが有効になっている広告ネットワークには適用されません） リダイレクトを追加し（関連する場合）、関連する URL にパラメーターを追加することで、クリック数および売上高をトラッキングするレベル：

* *[!UICONTROL Keyword]:* キーワードレベルでのみデータを追跡します。

* *[!UICONTROL Ad]:* 広告レベルでのみデータを追跡します。

  **注意：** 既存のキャンペーンをこの設定に変更すると、既存のキーワードトラッキング ID がすべて削除されます。 また、広告に複数のランディングページを使用して多変量分析テストを実行する場合は、バルクシートファイルを作成し、必要なコンポーネントに合わせて編集します。

* *[!UICONTROL Keyword and Ad]:* キーワードと広告レベルの両方でデータを追跡します。

**注：**

* [!DNL Naver] では「[!UICONTROL Keyword]」のみ使用できます。
* [!DNL Yandex] では「[!UICONTROL Ad]」のみ使用できます。
