---
title: バルクシートエラー
description: 各バルクシートエラーの潜在的な理由を参照してください。
source-git-commit: a59b477a6f8a616851d85bf89b58434d4d56cd83
workflow-type: tm+mt
source-wordcount: '1141'
ht-degree: 0%

---

# バルクシートエラー

Search、Social、および Commerce は、バルクシート操作中に 2 種類のエラーファイルを生成します。

* **SE エラー：** ファイルが投稿されたが、広告ネットワークがすべてのデータを受け付けない場合、と呼ばれるエラーファイル `<uploaded file name>_se_errors.<extension used for the bulksheet>` が作成されました。 一部の行が受け入れられた場合、エラー・ファイルには、投稿されなかった行と各エラーの説明が表示され、修正できます。 エラーは、[!UICONTROL SE Error Message]」列に表示されます。

>[!NOTE]
>
>投稿した場合 [!DNL Google Ads] 広告ネットワークの広告ポリシーに違反しているが、適用対象となる可能性がある広告。その場合、その広告は自動的に除外リクエストと共にリポジトリされます。 除外リクエストが失敗した場合は、違反に関する情報がエラーファイルに含まれます。

* **EF エラー：** bulksheet 操作でファイルまたはファイル内の個々の行をアップロードまたは処理できない場合、 `<uploaded file name>_ef_errors.<extension used for the bulksheet>`. 問題が個々の行にある場合は、それらの行が含まれ、各エラーの説明と共に修正できます。 エラーは、[!UICONTROL EF Error Message]」列に表示されます。

## [!UICONTROL SE Error] メッセージ

エラー [!UICONTROL SE Error] 列は広告ネットワークから直接取得されます。

## [!UICONTROL EF Error] メッセージ

次のエラーが [!UICONTROL EF Error] 列 [!UICONTROL EF Errors] ファイル。

### エラーのダウンロード/作成

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 未分類または未処理のエラーが発生したため、操作が完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームに連絡して原因を調べてください。 |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social, &amp; Commerce は、バルクシートを作成する前に広告ネットワークと同期できなかったので、バルクシートは作成されませんでした。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |

### アップロードエラー

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 操作が完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Invalid Fields.] \[ 無効なフィールドとエラー\] | 指定したデータがないか、無効です。 |
|  | [!UICONTROL Invalid Reference Given] | 広告ネットワーク上のエンティティの ID または親エンティティの ID（アカウント ID など）は、Search、Social、および Commerce のエンティティに対応していません。 これは、バルクシートの ID を編集したときに発生する可能性があります。 |
|  | [!UICONTROL <Entity> is deleted or expired] | エンティティは期限切れか、削除されたので、プロパティを変更できません。 エンティティは、誰かがステータスを手動で編集すると削除される場合があります。 |
|  | [!UICONTROL <Entity> status should be Active or Paused] | （新規エンティティ）新しいエンティティは、「アクティブ」または「一時停止」のみです。 |
|  | [!UICONTROL Duplicate Entries are present] | 同じエンティティに対して複数の行が含まれ、各行に異なる属性が設定されます。 変更を 1 行に統合します。 |
|  | [!UICONTROL Invalid AMO ID given] | 行の AMO ID が存在しません。 これは、バルクシートで ID を編集した場合に発生する可能性があります。 |
|  | [!UICONTROL Invalid row given] | この行には、エンティティタイプを判断するのに十分な情報が含まれていません。 行を編集して、エンティティタイプのすべての必須フィールドを含めます。 |
| アカウント | [!UICONTROL Provide Valid Account Details] | （複数のアカウント用の一括送信シート）アカウント識別子がすべての行に含まれているわけではありません。 各行の次の列の組み合わせのいずれかに値を入力します。a) &quot;[!UICONTROL AMO ID]&quot;または b) &quot;[!UICONTROL Account Name]&quot;および&quot;[!UICONTROL Platform].&quot; |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search、Social、および Commerce は、広告ネットワークアカウントにアクセスできないので、キャンペーンデータを作成または編集できません。 検索アカウントの資格情報が正しく、アカウントが有効になっていることを確認します。 |
| Campaign | [!UICONTROL Invalid Shopping Country specified] | （買い物キャンペーン）「[!UICONTROL Sales Country]「 」フィールドが無効です。 有効な国のリストを表示 [対象 [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) および [対象 [!DNL Microsoft® Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083). |
| すべてのキャンペーンコンポーネント | [!UICONTROL Campaign creation failed] | 親キャンペーンが作成されなかったので、このエンティティは作成されませんでした。 すべての親エンティティに、すべての必須フィールドが含まれていることを確認します。 |
| 広告グループ | [!UICONTROL Campaign Row missing] | 指定された親キャンペーンが存在しないので、広告グループは作成されませんでした。 新しい行に親キャンペーンを作成します。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 広告グループには、キーワードとプレースメントのどちらか一方を含めることができますが、両方を含めることはできません。 キーワードとプレースメントに対して別々の広告グループを作成します。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | ([!DNL Yandex]) キーワードが 1 つも含まれていないので、広告グループは作成されませんでした。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | ([!DNL Yandex])1 つ以上の広告が含まれていないので、広告グループは作成されませんでした。 |
|  | [!UICONTROL Creative Row Missing] | ([!DNL Yandex])1 つ以上の広告が含まれていないので、広告グループは作成されませんでした。 |
| すべての広告グループコンポーネント | [!UICONTROL Adgroup creation failed] | 親広告グループが作成されなかったので、このエンティティを作成できませんでした。 これは、広告グループフィールドのエラーまたは親キャンペーンが失敗したためです。 すべての親エンティティに、すべての必須フィールドが含まれていることを確認します。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定された親広告グループが存在しないので、エンティティを作成できませんでした。 新しい行に親広告グループを作成します。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | 「[!UICONTROL Tracking Template]「 」フィールドは、最終/詳細 URL を使用するアカウントのみに使用します。 最終/詳細 URL を使用するアカウントを移行するまで、値を削除します。 |
| 広告 | [!UICONTROL Cannot modify attributes other than status code and url for <ad type>] | （テキスト、拡張テキスト、製品、アプリインストール、動的検索以外の広告タイプ）この広告タイプのステータスと URL のみを編集できます。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 各広告グループには最大 50 個の広告を含めることができ、このバルクシートには 50 を超える広告を含めます。 広告の数を減らします。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 広告は、期限切れまたは削除された親エンティティに含まれているので、編集できません。 |
| キーワード | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除されたか、期限切れになっているので、エンティティを変更することはできません。 |
| プレースメント | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除されたか、期限切れになっているので、エンティティを変更することはできません。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | (Google Ads) 検索ネットワーク上のキャンペーンでのみプレースメントの入札が可能です。また、検索ネットワークとコンテンツネットワークの両方をターゲットとするキャンペーンでは入札ができません。 |
| 買い物製品グループ | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 製品グループの各レベルには、「[!UICONTROL Everything Else]&quot;グループ。 手動で「[!UICONTROL Everything Else]&quot;グループ；同じレベルで他のすべての製品グループを削除すると、自動的に削除されます。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除されたか、期限切れになっているので、エンティティを変更することはできません。 |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | ([!DNL Yandex] ただし、メッセージが不正確である場合は、各キャンペーンには、最大 4 つ（10 ではなく）のサイトリンクを含めることができ、このバルクシートには 4 つ以上のサイトリンクが含まれます。 一部のサイトリンクを削除します。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 親キャンペーンは期限切れまたは削除されているので、サイトリンクを編集できません。 |
|  | [!UICONTROL Creative creation failed] | ([!DNL Yandex]) 広告が作成されなかったので、サイトリンクを作成できませんでした。 |
| 場所のターゲット | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 親キャンペーンまたは広告グループは削除されたか、期限が切れているので、ロケーションターゲットを編集できません。 |
| 除外 | [!UICONTROL Other than status is modified] | 除外のステータス (「[!UICONTROL Active]&quot;または&quot;[!UICONTROL Deleted]&quot;) です。 |
| Googleリマーケティングリストのターゲット/オーディエンス | [!UICONTROL Invalid Audience given] | ([!DNL Google Ads] campaigns のみ )RLSA ターゲットは、既存の RLSA（オーディエンス）に対応していません。 「[!UICONTROL Audience]&quot;および&quot;[!UICONTROL RLSA Target]&quot;列。 |

### エラーを投稿

次のエラーが [!UICONTROL EF Errors] ファイルのみ。 ほとんどの投稿エラーは広告ネットワークから発生し、SE Errors ファイルに含まれます。

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 操作が完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Entity] は広告ネットワークに投稿されています | このエンティティは広告ネットワークに投稿されましたが、同時に Search、Social、および Commerce に同期されなかったので、エンティティデータは Search、Social、および Commerce ですぐに使用できません。 同期プロセスが自動的にトリガーされます。<br><br>大量のデータを同期した場合、数時間以上、そのデータが検索、ソーシャル、コマースで使用できない可能性があります。 |
| | [!UICONTROL Skipping <ENTITY> creation since <PARENT ENTITY> creation failed.] | 親エンティティを作成できなかったので、この子エンティティは作成されませんでした。 |

>[!MORELIKETHIS]
>
>* [バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [バルクシートファイルのダウンロード/作成](bulksheet-download.md)
>* [バルクシートファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [バルクシートファイルまたは修正済みエラーファイルのアップロード](bulksheet-upload.md)
>* [バルクシートの投稿または修正されたエラーファイル](bulksheet-post.md)
