---
title: キャンペーンの複製
description: キャンペーンの複製方法について説明します。
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
source-git-commit: 4085c1b21c0fe84653978e449321868921841367
workflow-type: tm+mt
source-wordcount: '207'
ht-degree: 0%

---

# キャンペーンの複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

キャンペーンを複製して、類似の設定で新しいキャンペーンを作成します。 次の操作を実行できます。

* 元の広告主または別の広告主のキャンペーンを複製
* オプションで、元のパッケージとプレースメントを複製します
* 新しいキャンペーンの実施日を変更

重複しないプレースメント設定のリストについては [&#128279;](#campaign-not-duplicated) 重複していないもの  を参照してください。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーン名の横で、**[!UICONTROL ...]**/**[!UICONTROL Duplicate]** をクリックします。

1. 新しいキャンペーン設定を指定します。

   1. 新しいキャンペーン名とキャンペーンの終了日を入力します。

   1. （任意）デフォルト設定を変更します。

      デフォルトでは、新しいキャンペーンは元の広告主に割り当てられ、現在の日付に始まるフライトスケジュールがあり、元のパッケージとプレースメントが含まれています。

1. 「**[!UICONTROL Submit]**」をクリックします。

## 重複していない点 {#campaign-not-duplicated}

次の場合を除き、元のプレースメントのすべての設定が複製されます。

* 実験設定
* （フライトの日付を変更する場合）カスタム広告スケジュール
* （広告を添付しない場合）カスタム広告の重み付けとスケジュール
* プログラム保証（PG）取引のデフォルトのプレースメントと [!UICONTROL Simple Ad Serving] の取引のプレースメント
* （プレースメントを別のキャンペーンにコピーする場合）:
   * ジオターゲット
   * イベントピクセル
   * 広告
   * プレースメントレベルの [!DNL DoubleVerify Authentic Brand Safety] セグメント（広告主レベルのセグメントを上書きします）

>[!MORELIKETHIS]
>
>* [Campaign Managementについて ](campaign-about.md)
>* [ キャンペーンの作成 ](campaign-create.md)
>* [ キャンペーンの編集 ](campaign-edit.md)
>* [ キャンペーンの変更ログを表示 ](campaign-change-log.md)
>* [ キャンペーン設定 ](campaign-settings.md)
