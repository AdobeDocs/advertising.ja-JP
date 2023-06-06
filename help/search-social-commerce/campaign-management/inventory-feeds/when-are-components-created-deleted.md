---
title: アカウントコンポーネントは、いつ在庫フィードによって作成または削除されますか？
description: 在庫フィードを投稿する際に、アカウントコンポーネントを作成および削除する状況を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '855'
ht-degree: 0%

---

# アカウントコンポーネントは、いつ在庫フィードによって作成または削除されますか？

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

在庫フィードファイルがテンプレートを通じて伝搬されると、次のようにアカウントコンポーネントが作成および削除されます。

>[!NOTE]
>
>広告グループ内に重複した広告が作成されることはありません。

| シナリオ | 例 | アクション |
|----|----|----|
| フィードデータには、キャンペーン名、広告グループ名、キーワードまたは製品グループで使用される列の新しい値が含まれます。 | 前のファイル：<br>Campaign=Hats<br>Campaign=Gloves<br><br>新規ファイル：<br>Campaign=Shoes | 広告ネットワークにキャンペーンが存在しない場合は、新しいキャンペーン、広告グループ、キーワードまたは製品グループが作成されます。 |
| フィードデータには、広告で使用される列の新しい値が含まれます。 | 前のファイル：広告が含まれている価格=20<br><br>新規ファイル：同じ広告の場合、price=10 | 広告が [!DNL Microsoft® Advertising] 拡張テキスト広告、 [!DNL Yahoo! Japan ads]または [!DNL Yandex] 広告が変更され、既存の広告が削除されて、新しい広告が作成されます。<br><br>広告コピーが他の広告タイプに対して変更されたとき、または該当する列が [!DNL Google Ads] 広告内の広告パラメーター（{param1} または {param2}）が追加された場合、既存の広告が更新されます。 |
| 前回の伝播以降に変更されたキャンペーン、広告グループ、キーワードまたは製品グループのテンプレート設定。 | 前の設定：Keyword=[キーワード]<br><br>新しい設定：キーワード=&lt;color>[キーワード] | 広告ネットワークにキャンペーンが存在しない場合は、新しいキャンペーン、広告グループ、キーワードまたは製品グループが作成されます。 |
| 広告のテンプレート設定は、最後の伝播以降に変更されました。 | 以前の設定：広告の説明=&quot;購入 [カテゴリ] さあ」<br><br>新しい設定：広告の説明=&quot;購入 [ブランド] さあ」 | 広告が [!DNL Microsoft® Advertising] 拡張テキスト広告、 [!DNL Yahoo! Japan ads]または [!DNL Yandex] 広告が変更され、既存の広告が削除されて、新しい広告が作成されます。<br><br>他の広告タイプに対して広告のコピーが変更された場合、または変更が単一の広告タイプに対して使用される列の変更を反映した場合 [!DNL Google Ads] 広告内の広告パラメーター（{param1} または {param2}）が追加された場合、既存の広告が更新されます。 |
| 新しいフィードデータに、既存のキャンペーンまたは広告グループの行が含まれていません。 | 該当なし | 既存のキャンペーンおよび広告グループは、そのまま残ります。 |
| 新しいフィードデータに、既存の広告グループ、広告、キーワードまたは製品グループの行が含まれていません。 | 該当なし | 既存の広告グループ、広告、キーワードまたは製品グループは、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). |
| 既存の親製品グループの新しいフィードデータに、その既存の子製品グループの行が含まれていません。 | 該当なし | 既存の親製品グループは、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). <b>注意：</b> フィードデータ設定が、見つからない行項目を一時停止するように設定されている場合、製品グループを一時停止できないので、親製品グループは削除されたままになります。 |
| 新しいフィードデータには、以前のデータの広告グループ、広告、キーワードまたは製品グループの行 (a) が含まれますが、b) がそれ以降省略され、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). | 該当なし | 既存の広告グループ、広告、キーワードまたは製品グループが再アクティブ化され、履歴や品質スコアは失われません。 |
| 新しいフィードデータには、以前のデータの広告グループ、広告、キーワードまたは製品グループの行が含まれます。a) 以前のデータの行、b) はそれ以降省略され、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). | 該当なし | 新しい広告グループ、広告、キーワード、製品グループが作成されます。 |
| キャンペーンまたは広告のグループレベルオプションを「[!UICONTROL Delete negative keywords when omitted from list].&quot; | 否定的なキーワードのリストには、「coupe」と「sports car」が含まれます。<br><br>広告グループには、除外キーワード「SUV」が既に含まれています。 | リストにない既存の除外キーワードは、そのまま残ります。 |
| キャンペーンまたは広告グループレベルのオプション「[!UICONTROL Delete negative keywords when omitted from list]、」、およびリストにない除外キーワードが存在します。 | 否定的なキーワードのリストには、「coupe」と「sports car」が含まれます。<br><br>広告グループには、除外キーワード「SUV」が既に含まれています。 | テンプレートを使用して以前に作成された、指定されていない除外キーワードは、フィードファイルがテンプレートを通じて伝播されると削除されます。 ただし、他の方法（プレーンバルクシートの場合など）で作成された、指定されていない除外キーワードは、 [!UICONTROL Campaigns] 表示数、または広告ネットワークの広告エディター内 ) は、そのまま残ります。 |  | 投稿されたフィードファイルのコンポーネントの予定終了日が発生します。 | 該当なし | 既存のキャンペーンはそのまま残ります。 既存の広告グループ、広告、キーワードは、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). |
| 品目の在庫レベルは、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). | 前のファイル：stock=10<br><br>新規ファイル：stock=0 | 既存のキャンペーンはそのまま残ります。 既存の広告グループ、広告、キーワードおよび製品グループは、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). |
| 品目の在庫レベルが、 [フィードデータ設定](feed-settings-manage.md#feed-data-settings). | 前のファイル：stock=0<br><br> 新規ファイル：stock=10 | 既存の広告、キーワードまたは製品グループが一時停止されると、それらは再アクティブ化され、履歴や品質スコアは失われません。 広告、キーワードまたは製品グループが存在しない場合（例えば、在庫レベルが最小値を下回って以前に削除された場合）は、新しいグループが作成されます。 |

>[!MORELIKETHIS]
>
>* [在庫フィードを使用した広告管理の自動化について](inventory-feeds-about.md)
>* [在庫フィードを使用したキャンペーンデータ管理のワークフロー](inventory-feeds-workflow.md)
