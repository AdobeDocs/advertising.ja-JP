---
title: バルクシートエラー
description: 各バルクシートエラーの考えられる理由を参照します。
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1137'
ht-degree: 0%

---

# バルクシートエラー

検索、ソーシャル、Commerceは、バルクシートの操作中に次の 2 種類のエラーファイルを生成します。

* **SE エラー：** ファイルが投稿されても、広告ネットワークがすべてのデータを受け入れない場合、`<uploaded file name>_se_errors.<extension used for the bulksheet>` というエラーファイルが作成されます。 すべての行ではなく一部の行が受け入れられると、エラーファイルに投稿されなかった行と各エラーの説明が表示され、修正できます。 エラーは「[!UICONTROL SE Error Message]」列に含まれます。

>[!NOTE]
>
>広告ネットワークの広告ポリシーに違反する [!DNL Google Ads] 広告を投稿しても、免除対象となる可能性がある場合、それらの広告は自動的に免除要求で再投稿されます。 除外リクエストが失敗した場合、違反に関する情報がエラーファイルに含まれます。

* **EF エラー：** バルクシート操作で、ファイルまたはファイル内の個々の行をアップロードまたは処理できない場合、`<uploaded file name>_ef_errors.<extension used for the bulksheet>` というエラーファイルが作成されます。 問題が個々の行に関するものである場合、それらの行は含まれます。
修正できるように、各エラーの説明を付けます。 エラーは「[!UICONTROL EF Error Message]」列に含まれます。

## [!UICONTROL SE Error] メッセージ

[!UICONTROL SE Error] 列のエラーは、広告ネットワークから直接送信されます。

## [!UICONTROL EF Error] メッセージ

[!UICONTROL EF Errors] ファイルの [!UICONTROL EF Error] 列には、次のエラーが含まれる場合があります。

### ダウンロード/作成エラー

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 未分類または未処理のエラーが原因で、操作が完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームに問い合わせて原因を調査してください。 |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 検索、ソーシャル、Commerceは、バルクシートを作成する前に広告ネットワークと同期できなかったので、バルクシートは作成されませんでした。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |

### アップロードエラー

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 操作は完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Invalid Fields.] \[ 無効なフィールドとエラー\] | 指定されたデータが見つからないか無効です。 |
|  | [!UICONTROL Invalid Reference Given] | 広告ネットワーク上のエンティティの ID、または親エンティティの ID （アカウント ID など）が、検索、ソーシャル、Commerceのエンティティに対応していません。 この問題は、バルクシートで ID を編集した場合に発生する可能性があります。 |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | このエンティティは有効期限が切れているか削除されているため、プロパティを変更できません。 ステータスが手動で編集されたときにエンティティが削除されることがあります。 |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | （新規エンティティ）新規エンティティは「アクティブ」または「一時停止」のみです。 |
|  | [!UICONTROL Duplicate Entries are present] | 同じエンティティに対して複数の行が含まれ、各行に異なる属性が含まれます。 変更を 1 行に統合します。 |
|  | [!UICONTROL Invalid AMO ID given] | 行の AMO ID が存在しません。 この問題は、バルクシート内の ID を編集した場合に発生する可能性があります。 |
|  | [!UICONTROL Invalid row given] | 行に、エンティティの種類を特定するのに十分な情報が含まれていません。 行を編集して、エンティティタイプのすべての必須フィールドを含めます。 |
| アカウント | [!UICONTROL Provide Valid Account Details] | （複数のアカウントのバルクシート）アカウント識別子は、すべての行に含まれるわけではありません。 各行に、a）「[!UICONTROL AMO ID]」または b）「[!UICONTROL Account Name]」および「[!UICONTROL Platform]」の列の組み合わせのいずれかの値を入力します。 |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | 検索、ソーシャル、Commerceは広告ネットワークアカウントにアクセスできないため、キャンペーンデータを作成または編集できません。 検索アカウントの資格情報が正しいこと、およびアカウントが有効になっていることを確認してください。 |
| キャンペーン | [!UICONTROL Invalid Shopping Country specified] | （ショッピングキャンペーン）「[!UICONTROL Sales Country]」フィールドの値が無効です。 有効な国 [for [!DNL Google Ads]](https://support.google.com/merchants/answer/160637#countrytable) および [for [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/3/en/51083) のリストを参照してください。 |
| すべての Campaign コンポーネント | [!UICONTROL Campaign creation failed] | 親キャンペーンが作成されなかったので、このエンティティは作成されませんでした。 すべての親エンティティにすべての必須フィールドが含まれていることを確認します。 |
| 広告グループ | [!UICONTROL Campaign Row missing] | 指定された親キャンペーンは存在しないので、広告グループは作成されませんでした。 新しい行に親キャンペーンを作成します。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 広告グループには、キーワードまたはプレースメントのどちらか一方を含めることができますが、両方を含めることはできません。 キーワードとプレースメントに対して個別の広告グループを作成します。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | （[!DNL Yandex]）少なくとも 1 つのキーワードが含まれていないので、広告グループは作成されませんでした。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | （[!DNL Yandex]）少なくとも 1 つの広告が含まれていないので、広告グループは作成されませんでした。 |
|  | [!UICONTROL Creative Row Missing] | （[!DNL Yandex]）少なくとも 1 つの広告が含まれていないので、広告グループは作成されませんでした。 |
| すべての広告グループコンポーネント | [!UICONTROL Adgroup creation failed] | 親広告グループが作成されなかったので、このエンティティを作成できませんでした。 これは、広告グループのフィールドにエラーが発生したか、親キャンペーンが失敗したことが原因である可能性があります。 すべての親エンティティにすべての必須フィールドが含まれていることを確認します。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定された親広告グループが存在しないので、エンティティを作成できませんでした。 新しい行に親広告グループを作成します。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | 「[!UICONTROL Tracking Template]」フィールドは、最終/詳細 URL を使用するアカウント専用です。 最終/高度な URL を使用するようにアカウントを移行するまでは、値を削除してください。 |
| 広告 | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | （テキスト、展開テキスト、製品、アプリのインストール、動的検索以外の広告タイプ）この広告タイプのステータスと URL のみを編集できます。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 各広告グループには最大 50 件の広告を含めることができ、このバルクシートには 50 件以上の広告を含めることができます。 広告の数を減らします。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 広告は期限切れまたは削除された親エンティティにあるので、編集できません。 |
| キーワード | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループが削除または期限切れになっているので、エンティティを変更できません。 |
| プレースメント | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループが削除または期限切れになっているので、エンティティを変更できません。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | （Google広告）プレースメントに対する入札は、検索ネットワークのみのキャンペーンまたはコンテンツネットワークのみのキャンペーンで行うことができ、検索ネットワークとコンテンツネットワークの両方をターゲットとするキャンペーンでは行えません。 |
| ショッピング製品グループ | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 製品グループの各レベルには、「[!UICONTROL Everything Else]」グループを含める必要があります。 「[!UICONTROL Everything Else]」グループは手動で削除できません。同じレベルで他のすべての製品グループを削除すると、自動的に削除されます。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループが削除または期限切れになっているので、エンティティを変更できません。 |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | （[!DNL Yandex] のみ）メッセージが不正確です。各キャンペーンには最大 4 個（10 個ではなく）のサイトリンクを含めることができ、このバルクシートには 4 個を超えるリンクを含めることができます。 サイト リンクをいくつか削除します。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 親キャンペーンの有効期限が切れているか削除されているため、サイトリンクを編集できません。 |
|  | [!UICONTROL Creative creation failed] | （[!DNL Yandex]）広告が作成されなかったため、サイトリンクを作成できませんでした。 |
| 場所のターゲット | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 親キャンペーンまたは広告グループが削除されているか期限切れなので、場所のターゲットを編集できません。 |
| 除外 | [!UICONTROL Other than status is modified] | 編集できるのは、除外のステータス（「[!UICONTROL Active]」または「[!UICONTROL Deleted]」）のみです。 |
| Google リマーケティングリストのターゲット/オーディエンス | [!UICONTROL Invalid Audience given] | （[!DNL Google Ads] キャンペーンのみ） RLSA ターゲットは既存の RLSA （オーディエンス）に対応しません。 「[!UICONTROL Audience]」列と「[!UICONTROL RLSA Target]」列の値を修正します。 |

### 投稿エラー

次のエラーは [!UICONTROL EF Errors] ファイルでのみ発生します。 ほとんどの投稿エラーは広告ネットワークから発生し、SE エラーファイルに含まれます。

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 操作は完全に失敗しました。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Entity] が広告ネットワークに投稿されました | エンティティは広告ネットワークに投稿されましたが、同時に検索、ソーシャル、Commerceに同期されなかったので、検索、ソーシャル、Commerceでエンティティデータをすぐに使用することはできません。 同期プロセスは自動的にトリガーされるようになりました。<br><br> 大量のデータを同期する場合、数時間以上にわたって検索、ソーシャル、Commerceでデータを使用できないことがあります。 |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | 親エンティティを作成できなかったので、この子エンティティは作成されませんでした。 |

>[!MORELIKETHIS]
>
>* [ バルクシートを使用した Campaign データの管理について ](bulksheet-about.md)
>* [ バルクシートファイルのダウンロード/作成 ](bulksheet-download.md)
>* [ バルクシートファイル内のランディングページの検証 ](bulksheet-validate-landing-pages.md)
>* [ バルクシートファイルまたは修正されたエラーファイルのアップロード ](bulksheet-upload.md)
>* [ ポストバルクシートまたは修正されたエラーファイル ](bulksheet-post.md)
