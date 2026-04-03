---
title: バルクシートエラー
description: 各バルクシートエラーの潜在的な理由を参照します。
exl-id: dc3559b0-05c0-4896-b9e9-67084f56ab80
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/7jGIKXI-Un6mnstJlPDqk0q4yB6k3tEsqHngD1cCyEw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1137
ht-degree: 1%

---

# バルクシートエラー

Search, Social, &amp; Commerceでは、バルクシート処理中に2種類のエラーファイルが生成されます。

* **SE エラー：** ファイルが投稿されたものの、広告ネットワークがすべてのデータを受け入れられない場合、`<uploaded file name>_se_errors.<extension used for the bulksheet>`というエラーファイルが作成されます。 一部の行が受け入れられましたが、すべての行が受け入れられなかった場合、エラーファイルには、投稿されなかった行と各エラーの説明が表示されるので、修正できます。 エラーは「[!UICONTROL SE Error Message]」列に含まれています。

>[!NOTE]
>
>広告ネットワークの広告ポリシーに違反する[!DNL Google Ads]広告を投稿したが、免除対象となる可能性がある場合、その広告は自動的に免除要求とともに再投稿されます。 除外リクエストが失敗した場合、違反に関する情報がエラーファイルに含まれます。

* **EF エラー：** バルクシート操作で、ファイルまたはファイル内の個々の行をアップロードまたは処理できない場合、`<uploaded file name>_ef_errors.<extension used for the bulksheet>`というエラーファイルが作成されます。 問題が個々の行にある場合、その行が含まれ，
修正できるように各エラーの説明を書きます。 エラーは「[!UICONTROL EF Error Message]」列に含まれています。

## [!UICONTROL SE Error]件のメッセージ

[!UICONTROL SE Error]列のエラーは、広告ネットワークから直接発生します。

## [!UICONTROL EF Error]件のメッセージ

次のエラーは、[!UICONTROL EF Error] ファイルの[!UICONTROL EF Errors]列に含まれる可能性があります。

### エラーのダウンロード/作成

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | 未分類または未処理のエラーにより、操作は完全に失敗しました。 問題が解決しない場合は、Adobe アカウントチームに連絡して原因を調べてください。 |
| | [!UICONTROL Pre-Sync Failed. Please Try Creating the bulksheet Again. If Problem Persists Contact Technical Support] | Search, Social, &amp; Commerceでは、バルクシートを作成する前に広告ネットワークと同期できなかったため、バルクシートは作成されませんでした。 問題が解決しない場合は、Adobe アカウントチームにお問い合わせください。 |

### アップロードエラー

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Uploading the bulksheet Again. If Problem Persists Contact Customer Care] | 操作は完全に失敗しました。 問題が解決しない場合は、Adobe アカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Invalid Fields.] \[無効なフィールドとエラー\] | 指定されたデータが見つからないか、無効です。 |
|  | [!UICONTROL Invalid Reference Given] | 広告ネットワーク上のエンティティのID、または親エンティティのID （アカウント IDなど）が、Search, Social, &amp; Commerceのエンティティに対応しません。 これは、バルクシートでIDを編集したときに発生する可能性があります。 |
|  | [!UICONTROL &lt;Entity> is deleted or expired] | エンティティが期限切れになっているか削除されました。プロパティを変更することはできません。 誰かが手動でステータスを編集すると、エンティティが削除される場合があります。 |
|  | [!UICONTROL &lt;Entity> status should be Active or Paused] | （新しいエンティティ）新しいエンティティは「アクティブ」または「一時停止」のみです。 |
|  | [!UICONTROL Duplicate Entries are present] | 同じエンティティに対して、各行に異なる属性を持つ複数の行が含まれます。 変更を1行に統合します。 |
|  | [!UICONTROL Invalid AMO ID given] | 行のAMO IDが存在しません。 これは、バルクシートでIDを編集した場合に発生する可能性があります。 |
|  | [!UICONTROL Invalid row given] | 行には、エンティティタイプを決定するのに十分な情報が含まれていません。 行を編集して、エンティティタイプのすべての必須フィールドを含めます。 |
| アカウント | [!UICONTROL Provide Valid Account Details] | （複数のアカウントのバルクシート） アカウント IDはすべての行に含まれません。 各行の列の次のいずれかの組み合わせの値を入力します：a） &quot;[!UICONTROL AMO ID]&quot;またはb） &quot;[!UICONTROL Account Name]&quot;および&quot;[!UICONTROL Platform]&quot;。 |
|  | [!UICONTROL Account is disabled. Disabled Accounts cannot be processed] | Search, Social, &amp; Commerceでは、広告ネットワークアカウントにアクセスできないため、キャンペーンデータを作成または編集できません。 検索アカウントの資格情報が正しく、アカウントが有効になっていることを確認します。 |
| キャンペーン | [!UICONTROL Invalid Shopping Country specified] | （ショッピングキャンペーン）「[!UICONTROL Sales Country]」フィールドの値が無効です。 [&#x200B; [!DNL Google Ads]の有効な国](https://support.google.com/merchants/answer/160637#countrytable)と[&#x200B; [!DNL Microsoft Advertising]の](https://help.ads.microsoft.com/#apex/3/en/51083)の一覧を参照してください。 |
| すべてのキャンペーンコンポーネント | [!UICONTROL Campaign creation failed] | 親キャンペーンは作成されていないので、このエンティティは作成されませんでした。 すべての親エンティティにすべての必須フィールドが含まれていることを確認します。 |
| 広告グループ | [!UICONTROL Campaign Row missing] | 指定された親キャンペーンは存在しないため、広告グループは作成されませんでした。 新しい行に親キャンペーンを作成します。 |
|  | [!UICONTROL New adgroup has both keywords and placement] | 広告グループには、キーワードとプレースメントのどちらかを含めることができますが、両方を含めることはできません。 キーワードとプレースメント用に個別の広告グループを作成します。 |
|  | [!UICONTROL No corresponding keyword for Adgroup] | （[!DNL Yandex]）広告グループは、少なくとも1つのキーワードが含まれていないため、作成されませんでした。 |
|  | [!UICONTROL No corresponding creative for Adgroup] | （[!DNL Yandex]）広告グループは、少なくとも1つの広告が含まれていないため、作成されませんでした。 |
|  | [!UICONTROL Creative Row Missing] | （[!DNL Yandex]）広告グループは、少なくとも1つの広告が含まれていないため、作成されませんでした。 |
| すべての広告グループコンポーネント | [!UICONTROL Adgroup creation failed] | 親広告グループが作成されていないので、このエンティティを作成できませんでした。 これは、広告グループフィールドのエラー、または親キャンペーンの失敗が原因である可能性があります。 すべての親エンティティにすべての必須フィールドが含まれていることを確認します。 |
|  | [!UICONTROL Adgroup Row Missing] | 指定された親広告グループは存在しないため、エンティティを作成できませんでした。 新しい行に親広告グループを作成します。 |
|  | [!UICONTROL Cannot modify Tracking Template at Keyword / Creative / Site Link level until Account has been migrated to use Upgraded URLs. Please retry after migration] | 「[!UICONTROL Tracking Template]」フィールドは、最終/詳細URLを使用するアカウント専用です。 最終/詳細URLを使用するようにアカウントを移行するまで、この値を削除します。 |
| 広告 | [!UICONTROL Cannot modify attributes other than status code and url for &lt;ad type>] | （テキスト、拡張テキスト、製品、アプリのインストール、動的検索以外の広告タイプ）この広告タイプのステータスとURLのみを編集できます。 |
|  | [!UICONTROL The number of creatives under an AdGroup should not exceed 50] | 各広告グループには最大50の広告を掲載でき、このバルクシートには50を超える広告が掲載されています。 広告の数を減らす。 |
|  | [!UICONTROL Cannot modify an ad which is either deleted/expired or under an deleted/expired campaign] | 広告は期限切れまたは削除された親エンティティにあるため、編集できません。 |
| キーワード | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除または期限切れのため、エンティティを変更できません。 |
| プレースメント | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除または期限切れのため、エンティティを変更できません。 |
|  | [!UICONTROL Cannot specify placement bids for websites under Display Select enabled Campaign with Search and Display Networks] | （Google Ads）プレースメントは、検索ネットワーク上のキャンペーンでのみ、またはコンテンツネットワーク上でのみ入札できますが、検索ネットワークとコンテンツネットワークの両方をターゲットとするキャンペーンでは入札できません。 |
| ショッピング商品グループ | [!UICONTROL Cannot delete Everything Else manually. It will be deleted automatically when all Product Group Conditions under the same parent are removed] | 製品グループの各レベルには、「[!UICONTROL Everything Else]」グループを含める必要があります。 「[!UICONTROL Everything Else]」グループを手動で削除することはできません。同じレベルの他のすべての製品グループを削除すると、自動的に削除されます。 |
|  | [!UICONTROL Cannot modify a keyword/website/product which is under deleted Adgroup or Campaign] | 親キャンペーンまたは広告グループは削除または期限切れのため、エンティティを変更できません。 |
| Sitelink | [!UICONTROL Sitelinks Cannot update more than 10 site links per campaign] | （[!DNL Yandex]のみ）メッセージが不正確です。各キャンペーンには最大4つの（10個ではなく）サイトリンクを含めることができます。また、このバルクシートには4つ以上のサイトリンクが含まれます。 サイトリンクの削除。 |
|  | [!UICONTROL Cannot update sitelinks under deleted/expired campaign] | 親キャンペーンの有効期限が切れているか削除されているため、サイトリンクを編集できません。 |
|  | [!UICONTROL Creative creation failed] | （[!DNL Yandex]）広告が作成されていないため、サイトリンクを作成できませんでした。 |
| 位置情報 | [!UICONTROL Cannot modify locations under deleted campaigns or adgroups] | 親キャンペーンまたは広告グループは削除または期限切れになるので、場所ターゲットを編集できません。 |
| 除外 | [!UICONTROL Other than status is modified] | 編集できるのは、除外（「[!UICONTROL Active]」または「[!UICONTROL Deleted]」）のステータスのみです。 |
| Google リマーケティングリストのターゲット/オーディエンス | [!UICONTROL Invalid Audience given] | （[!DNL Google Ads] キャンペーンのみ） RLSA ターゲットが既存のRLSA （オーディエンス）に対応していません。 「[!UICONTROL Audience]」列と「[!UICONTROL RLSA Target]」列の値を修正します。 |

### Post エラー

次のエラーは[!UICONTROL EF Errors] ファイルでのみ発生します。 ほとんどの投稿エラーは広告ネットワークから発生し、SE エラーファイルに含まれます。

| カテゴリ | メッセージ | 説明 |
|----|----|----|
| 一般 | [!UICONTROL Internal Error: Please Try Posting the bulksheet Again. If Problem Persists Contact Customer Care] | 操作は完全に失敗しました。 問題が解決しない場合は、Adobe アカウントチームにお問い合わせください。 |
| すべてのエンティティ | [!UICONTROL Entity]は広告ネットワークに投稿されています | エンティティは広告ネットワークに投稿されましたが、同時にSearch、Social、およびCommerceに同期されなかったため、エンティティ データはSearch、Social、およびCommerceですぐに利用できません。 同期プロセスが自動的にトリガーされます。<br><br>大量のデータが同期されると、Search、Social、Commerceでデータが数時間以上利用できなくなる場合があります。 |
| | [!UICONTROL Skipping &lt;ENTITY> creation since &lt;PARENT ENTITY> creation failed.] | 親エンティティを作成できなかったため、この子エンティティは作成されませんでした。 |

>[!MORELIKETHIS]
>
>* [&#x200B; バルクシートを使用したキャンペーンデータの管理について](bulksheet-about.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](bulksheet-download.md)
>* [&#x200B; バルクシート ファイル内のランディングページの検証](bulksheet-validate-landing-pages.md)
>* [&#x200B; バルクシート ファイルをアップロードするか、エラーファイルを修正](bulksheet-upload.md)
>* [&#x200B; バルクシートの投稿またはエラーファイルの修正](bulksheet-post.md)
