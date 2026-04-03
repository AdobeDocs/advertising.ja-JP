---
title: プレースメントの重複
description: 1つ以上のプレースメントを複製する方法について説明します。
feature: DSP Placements
exl-id: 41021f5b-13d1-419f-af03-c5507f9fed4d
TQID: https://experienceleague.adobe.com/1QHdooPh2tr6pfbnRsPbe-P5o-lZLgX-NQIUNG2ulHM
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 0%

---

# プレースメントの重複

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

1つまたは複数のプレースメントを複製して、同様の設定を持つプレースメントを作成します。 次の操作を実行できます。

* プレースメントの複数の複製を作成
* 元の広告主やキャンペーン内または異なる広告内でプレースメントを複製します
* （元のキャンペーン内の重複したプレースメントの場合） オプションで元の広告を複製します
* 新しいプレースメントのステータスとフライト日を変更する

重複しないプレースメント設定のリストについては、「[重複していないもの](#placement-not-duplicated)」を参照してください。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックします。

1. サブメニューで、**[!UICONTROL Placements]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * 1つの配置を複製するには、パッケージ名の横にある&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**&#x200B;をクリックします。

   * 複数の配置を複製するには：

      1. 複製する各プレースメントの横にあるチェックボックスをオンにします。

      1. 一括操作ツールバーで、**[!UICONTROL Duplicate]**&#x200B;をクリックします。

1. 新しい配置設定を指定します。

   1. （単一のプレースメント）新しいプレースメント名を入力します。

   1. **[!UICONTROL Choose Package (Required)]** メニューで、親パッケージまたは**[!UICONTROL No package]*&#x200B;のいずれかを選択します。

   1. （オプション）デフォルト設定を変更します。

   設定は、選択したすべてのプレースメントに適用されます。

   デフォルトでは、新しいプレースメントは元の広告タイプ用であり、元の広告主とキャンペーンに割り当てられ、現在の日から開始するフライトスケジュールがあり、一時停止され、元の広告は含まれません。

   複数のプレースメントを作成する場合、新しいプレースメント名には番号が順番に追加されます。例えば、「My Placement #2」などの規則&lt;*original_placement_name #N*>を使用します。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

## 重複していないもの {#placement-not-duplicated}

元のプレースメントのすべての設定は、次を除いて複製されます。

* 実験の設定
* 配置レベルの最小予算
* （フライト日を変更した場合） カスタム広告スケジュール
* （広告を添付しない場合） カスタム広告の重み付けとスケジュール設定
* プログラマティック保証（PG）取引のデフォルトのプレースメントと[!UICONTROL Simple Ad Serving]取引のプレースメント
* （プレースメントを別のキャンペーンにコピーした場合）:
   * 地域ターゲット
   * イベントピクセル
   * 広告
   * プレースメントレベル [!DNL DoubleVerify Authentic Brand Safety] セグメント （広告主レベルのセグメントを上書きする）

## 新しいプレースメントを設定するためのベストプラクティス

>[!TIP]
>
>* バルクシートを使用すると、一度に[複数のキャンペーンコンポーネントに変更を加えることができます](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 広告タグシートを使用して[複数のサードパーティ広告をアップロード &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 新しいプレースメントをアクティブ化する準備ができるまで一時停止します。

* 次の点を考慮し、必要に応じて新しいプレースメントを編集します。

   * アカウントには、新しいプレースメント予算に対応するのに十分な資金がありますか？

   * 新しいプレースメントには、以前のプレースメントとは異なる予算が必要ですか？ 最低予算は必要ですか？

   * 必要なカスタム広告の重み付けやスケジュールなどを含むクリエイティブをアップロードし、プレースメントに添付します。

   * 必要に応じて、イベントピクセルをプレースメントと広告に添付します。

   * プレースメントに必要に応じて、地理的ターゲットとプレースメントレベル [!DNL DoubleVerify Authentic Brand Safety]のセグメントを含めます。

   * プログラマティックな保証取引の場合は、新しい取引IDを使用して、デフォルトのプレースメントを作成します。

   * 必要に応じて、[!UICONTROL Simple Ad Serving]件の取引用に新しいプレースメントを作成します。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのプレースメント管理について](placement-about.md)
>* [&#x200B; プレースメントの作成](placement-create.md)
>* [&#x200B; プレースメントを編集](placement-edit.md)
>* [&#x200B; プレースメントの変更ログを表示](placement-change-log.md)
>* [配置の設定](placement-settings.md)
