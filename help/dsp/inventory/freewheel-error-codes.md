---
title: ' [!DNL FreeWheel]  広告送信のエラーコード'
description: ' [!DNL FreeWheel] への広告送信に返されるエラーコードを参照します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '645'
ht-degree: 3%

---

# [!DNL FreeWheel] 広告送信のエラーコード

失敗した広告送信のエラーメッセージは、Advertising DSPまたは [!DNL FreeWheel] のいずれかから取得できます。 エラーメッセージは、[[!UICONTROL Freewheel Status] ダイアログの「[!UICONTROL API Response]」列に表示され &#x200B;](freewheel-check-status.md) す。

## Advertising DSP内部エラー

| エラーメッセージ | 説明 | 次の手順 |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel] は、送信が成功または失敗したことを返信していません。 | 10 分後にもう一度ステータスを確認します。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel] では、時計番号が割り当てられていない UK 広告は受け付けていません。 | 広告に時計番号を割り当ててから、広告を再送信します。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 広告を送信しようとしたときに、トランスコーダーが広告のトランスコードを完了していませんでした。 | 10 分待ってから、広告を再送信してください。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 送信された取引は、プログラムで保証された取引として設定されていません。 [!DNL FreeWheel] は保証された取引のみを受け入れます。 | プログラムで保証された取引として取引 ID を設定します。 取引 ID ワークフローの最後に、プログラムで保証されたデフォルトのプレースメントを保存すると、広告は自動的に [!DNL FreeWheel] に送信されます。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | 送信された取引 ID が存在しないか、Adobe側でアクティブではありません。 | 取引がアクティブであることを確認してから、広告を再送信してください。 |
| [!DNL \[public_id=]\&lt;deal\>] は存在しません | 送信された取引 ID が [!DNL FreeWheel] 側に存在しません。 | 取引 ID を確認するには、[!DNL FreeWheel] 担当者にお問い合わせください。 |
| [!DNL Ad with identifier] \&lt;*ad name*\> [!DNL was not found.] | 送信された広告キーが存在しないか、Adobeエンドでアクティブになっていません。 | 正しい広告キーを見つけて、広告を再送信します。 |
| [!DNL Pending Submission] | 送信はまだ保留中です。 | ページを更新します。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API エラー

| コード | 意味 | 説明 | 次の手順 |
|--- |--- |--- |--- |
| 401 | 未認証 | アクセス認証情報が正しくない、見つからない、または無効です。 | Adobeアカウントチームにお問い合わせください。 |
| 403 | 禁止 | サーバーは要求を理解しましたが、承認を拒否しました。 | Adobeアカウントチームにお問い合わせください。 |
| 404 | 見つかりません | 要求されたリソースは使用できません。 クリエイティブ ID がPUT処理で見つからない場合は、404 が返されます。 | Adobeアカウントチームにお問い合わせください。 |
| 405 | 許可されていないメソッド | そのリソースでサポートされていないリクエストメソッドを使用して、リソースに対してリクエストが行われました（例えば、POSTがGETを送信する必要があるメソッドでデータを使用する、読み取り専用リソースでPUTを使用する）。 | Adobeアカウントチームにお問い合わせください。 |
| 408 | 要求タイムアウト | このリクエストの処理中にタイムアウトが発生しました。 タイムアウトは、通常、特定のリソースへの排他的アクセスの同時リクエストによって発生します。 | このステータスを受け取ったら、リクエストを再送信します。 問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。 |
| 422 | 処理できないエンティティ | 無効なリソースです。 このエラーは、リクエスト本文が無効な場合や、作成または更新したリソースが無効な場合（例えば、取引 ID が見つからなかった場合など）に発生します。 詳しくは、[FreeWheel API 422 エラー &#x200B;](#freewheel-422-errors) を参照してください。 | Adobeアカウントチームにお問い合わせください。 |
| 500 | 内部サーバーエラー | API システムエラー。 | Adobeアカウントチームにお問い合わせください。 |

{style="table-layout:auto"}

## [!DNL Freewheel] API 422 エラー {#freewheel-422-errors}

| コード | HTTP コード | 説明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | リクエストデータは無効な json 形式です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_VALIDATION_FAILURE | 422 | リクエストデータに必須フィールドがないか、無効なデータタイプです。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_INVALID | 422 | 契約が正しく設定されていないか、存在しません。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DEAL_GET_FAILURE | 422 | 契約が見つからなかったか、設定に問題があります。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | クリエイティブ URL が無効です。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | クリエイティブは取引の広告ユニットノードにリンクされていませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | クリエイティブは更新されませんでした。 詳しくは、エラーメッセージを確認してください。 |
| DATA_DSP_GET_FAILURE | 422 | DSPがシステム内に存在しません。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | クリエイティブと広告ユニットのリンクが解除されませんでした。 |
| DATA_CREATIVE_FAILURE_DELETE | 422 | クリエイティブは削除されませんでした。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | URL が検出されませんでした。 |
| DATA_ENTITY_NOT_FOUND | 422 | そのクリエイティブは存在しません。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [&#x200B; プログラムで保証された取引の設定の概要  [!DNL Freewheel]](/help/dsp/inventory/freewheel-overview.md)
>* [&#x200B; 取引 ID インボックスでの取引の承認 &#x200B;](deal-id-inbox-accept.md)
>* [&#x200B; プログラムで保証された取引の広告の送信先  [!DNL Freewheel]](/help/dsp/inventory/freewheel-submit.md)
>* [&#x200B; プログラムで保証された取引の広告  [!DNL FreeWheel]  ステータスの確認 &#x200B;](/help/dsp/inventory/freewheel-check-status.md)
