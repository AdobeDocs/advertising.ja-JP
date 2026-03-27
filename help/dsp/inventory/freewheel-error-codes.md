---
title: ' [!DNL FreeWheel] 広告の送信に関するエラーコード'
description: 広告送信用に返されるエラーコードを [!DNL FreeWheel]に参照します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: e48937c2-ced9-4107-9e1d-65a3bac51fff
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '641'
ht-degree: 3%

---

# [!DNL FreeWheel]件の広告送信のエラーコード

失敗した広告の送信に関するエラーメッセージは、Advertising DSPまたは[!DNL FreeWheel]から送信できます。 [!UICONTROL API Response] ダイアログ [[!UICONTROL FreeWheel Status]の](freewheel-check-status.md)列でエラーメッセージを検索します。

## Advertising DSPの内部エラー

| エラーメッセージ | 説明 | 次のステップ |
|--- |--- |--- |
| [!DNL Awaiting status response from [!DNL FreeWheel]] | [!DNL FreeWheel]は、送信が成功したか失敗したかについてまだ応答していません。 | 10分後にもう一度ステータスを確認します。 |
| [!DNL The submitted ad does not have a clock number assigned.] | [!DNL FreeWheel]は、割り当てられた時計番号を持たないイギリスの広告を受け付けません。 | 広告に時計の番号を割り当てて、広告を再送信します。 |
| [!DNL The ad you are attempting to submit has not yet finished transcoding. Please wait ten minutes then try again.] | 広告を送信しようとしたときに、トランスコーダーが広告のトランスコードを完了しませんでした。 | 10分待ってから、広告を再送信します。 |
| [!DNL The deal id you input is not setup as a guaranteed feed. Please submit guaranteed deals only.] | 提出された契約は、プログラム的に保証された契約として設定されていません。 [!DNL FreeWheel]は保証された取引のみを受け入れます。 | 取引IDをプログラム的な保証取引として設定します。 案件ID ワークフローの最後にプログラムで保証された既定のプレースメントを保存すると、広告は自動的に[!DNL FreeWheel]に送信されます。 |
| [!DNL Invalid external_deal_id:] \&lt;deal_id\> | 送信された案件IDが存在しないか、Adobe エンドでアクティブになっていません。 | 取引がアクティブであることを確認してから、広告を再送信します。 |
| [!DNL \[public_id=]\&lt;deal\>]が存在しません | 送信された案件IDが[!DNL FreeWheel]側に存在しません。 | [!DNL FreeWheel]担当者に連絡して、取引IDを確認してください。 |
| [!DNL Ad with identifier] \&lt;*広告名*\> [!DNL was not found.] | 送信された広告キーが存在しないか、Adobe エンドでアクティブになっていません。 | 正しい広告キーを見つけて、広告を再送信します。 |
| [!DNL Pending Submission] | 提出はまだ保留です。 | ページを更新します。 |

{style="table-layout:auto"}

## [!DNL FreeWheel] API エラー

| コード | 意味 | 説明 | 次のステップ |
|--- |--- |--- |--- |
| 401 | 未承認 | アクセス資格情報が正しくないか、見つからないか、無効です。 | Adobeのアカウントチームにお問い合わせください。 |
| 403 | 禁止 | サーバーはリクエストを理解しましたが、承認を拒否しました。 | Adobeのアカウントチームにお問い合わせください。 |
| 404 | 見つかりません | リクエストされたリソースは利用できません。 PUT操作でCreative IDが見つからない場合は、404が返されます。 | Adobeのアカウントチームにお問い合わせください。 |
| 405 | メソッドは許可されていません | リクエストは、そのリソースでサポートされていないリクエストメソッドを使用するリソースで作成されました（例えば、POSTでデータを送信する必要があるメソッドでGETを使用するか、読み取り専用リソースでPUTを使用するなど）。 | Adobeのアカウントチームにお問い合わせください。 |
| 408 | 要求タイムアウト | この要求の処理中にタイムアウトが発生しました。 タイムアウトは通常、特定のリソースへの排他的なアクセスのリクエストが同時に発生することが原因です。 | このステータスを受け取ったら、リクエストを再送信します。 問題が解決しない場合は、Adobe アカウントチームにお問い合わせください。 |
| 422 | 未処理エンティティ | 無効なリソースです。 このエラーは、リクエスト本文が無効であるか、作成または更新されたリソースが無効な場合（取引IDが見つからない場合など）に発生します。 詳しくは、[FreeWheel API 422 エラー](#freewheel-422-errors)を参照してください。 | Adobeのアカウントチームにお問い合わせください。 |
| 500 | 内部サーバーエラー | API システムエラー。 | Adobeのアカウントチームにお問い合わせください。 |

{style="table-layout:auto"}

## [!DNL FreeWheel] API 422 エラー {#freewheel-422-errors}

| コード | HTTP コード | 説明 |
|--- |--- |--- |
| DATA_UNMARSHALL_FAILURE | 422 | リクエストデータが無効なjson形式です。 詳細については、エラーメッセージを確認してください。 |
| DATA_VALIDATION_FAILURE | 422 | リクエストデータに必須フィールドがないか、無効なデータタイプがあります。 詳細については、エラーメッセージを確認してください。 |
| DATA_DEAL_INVALID | 422 | 契約が正しく設定されていないか、存在しません。 詳細については、エラーメッセージを確認してください。 |
| DATA_DEAL_GET_FAILURE | 422 | 契約が見つからないか、構成に問題があります。 詳細については、エラーメッセージを確認してください。 |
| DATA_CREATIVE_INGEST_FAILURE | 422 | クリエイティブ URLが無効です。 詳細については、エラーメッセージを確認してください。 |
| DATA_CREATIVE_LINK_FAILURE | 422 | クリエイティブが契約の広告ユニットノードにリンクされていませんでした。 詳細については、エラーメッセージを確認してください。 |
| DATA_CREATIVE_UPDATE_FAILURE | 422 | クリエイティブは更新されませんでした。 詳細については、エラーメッセージを確認してください。 |
| DATA_DSP_GET_FAILURE | 422 | DSPはシステム内に存在しません。 |
| DATA_CREATIVE_UNLINK_FAILURE | 422 | クリエイティブと広告ユニットの連携が解除されたわけではありません。 |
| DATA_CREATIVE_DELETE_FAILURE | 422 | クリエイティブは削除されませんでした。 |
| DATA_CREATIVE_DETECTION_FAILURE | 422 | URLが検出されませんでした。 |
| DATA_ENTITY_NOT_FOUND | 422 | クリエイティブは存在しません。 |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [でのプログラムによる保証取引の設定の概要 [!DNL FreeWheel]](/help/dsp/inventory/freewheel-overview.md)
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [ プログラマティック保証取引の広告を [!DNL FreeWheel]](/help/dsp/inventory/freewheel-submit.md)に送信します
>* [PG取引 [!DNL FreeWheel] の広告のステータスを確認する](/help/dsp/inventory/freewheel-check-status.md)
