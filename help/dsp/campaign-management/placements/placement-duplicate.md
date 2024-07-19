---
title: プレースメントを複製
description: 1 つ以上のプレースメントを複製する方法を説明します。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
source-git-commit: ae1a58bd0aed430cd2914146dfb2850bc8125025
workflow-type: tm+mt
source-wordcount: '304'
ht-degree: 0%

---

# プレースメントを複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

1 つ以上のプレースメントを複製して、類似の設定を持つプレースメントを作成します。 次の操作を実行できます。

* プレースメントの重複を複数作成
* 元の広告主やキャンペーン内、または異なる広告主内でのプレースメントの複製
* （元のキャンペーン内でプレースメントが重複している場合）オプションで、元の広告を複製します
* 新しいプレースメントのステータスとフライト日を変更する

重複しないプレースメント設定のリストについては ](#placement-not-duplicated) 重複していないもの [ を参照してください。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]** をクリックします。

1. 次のいずれかの操作をおこないます。

   * 1 つのプレースメントを複製するには、パッケージ名の横にある **[!UICONTROL ...]** > **[!UICONTROL Duplicate]** をクリックします。

   * 複数のプレースメントを複製するには：

      1. 複製する各プレースメントの横にあるチェックボックスをオンにします。

      1. 一括アクションツールバーで、「**[!UICONTROL Duplicate]**」をクリックします。

1. 新しい配置設定を指定します。

   1. （単一プレースメント）新しいプレースメント名を入力します。

   1. **[!UICONTROL Choose Package (Required)]** メニューで、親パッケージまたは**[!UICONTROL No package]*を選択します。

   1. （任意）デフォルト設定を変更します。

   設定は、選択したすべてのプレースメントに適用されます。

   デフォルトでは、新しいプレースメントは元の広告タイプ用であり、元の広告主とキャンペーンに割り当てられ、当日に開始するフライトスケジュールがあり、一時停止されており、元の広告は含まれません。

   複数のプレースメントを作成する場合、「My Placement #2」などの規則 &lt;*original_placement_name #N*> に従って、新しいプレースメント名に数字が順番に追加されます。

1. 「**[!UICONTROL Submit]**」をクリックします。

## 重複していない点 {#placement-not-duplicated}

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
>* [ プレースメント管理について ](placement-about.md)
>* [ プレースメントの作成 ](placement-create.md)
>* [ プレースメントを編集 ](placement-edit.md)
>* [ プレースメントの変更ログを表示 ](placement-change-log.md)
>* [ プレースメント設定 ](placement-settings.md)
