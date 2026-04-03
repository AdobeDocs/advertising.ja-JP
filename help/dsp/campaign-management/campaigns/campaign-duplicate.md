---
title: キャンペーンの複製
description: キャンペーンを複製する方法を説明します。
feature: DSP Campaigns
exl-id: 4e42bd5b-e8a9-45be-af5c-367c48d0b131
TQID: https://experienceleague.adobe.com/Oq-1l3Ls2uEul-OQFVfiMoed8NewiX0X-EZzBPlSCHU
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 380
ht-degree: 0%

---

# キャンペーンの複製

<!-- Some placements don't have this option. Clarify which placement types aren't eligible -- is it PG placements, or all placements using private inventory? And anything else? -->

キャンペーンを複製して、同様の設定を持つ新しいキャンペーンを作成します。 次の操作を実行できます。

* 元の広告主または別の広告主のキャンペーンを複製します

* オプションで、元のパッケージとプレースメントを複製します

* 新しいキャンペーンのフライト日を変更する

重複しないプレースメント設定のリストについては、「[重複していないもの](#campaign-not-duplicated)」を参照してください。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーン名の横にある「**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**」をクリックします。

1. 新しいキャンペーン設定を指定します。

   1. 新しいキャンペーン名と終了投入日を入力します。

   1. （オプション）デフォルト設定を変更します。

      デフォルトでは、新しいキャンペーンは元の広告主に割り当てられ、現在の日に開始するフライトスケジュールがあり、元のパッケージとプレースメントが含まれます。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

## 重複していないもの {#campaign-not-duplicated}

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

## 新しいキャンペーンを設定するためのベストプラクティス

>[!TIP]
>
>* バルクシートを使用すると、一度に[複数のキャンペーンコンポーネントに変更を加えることができます](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 広告タグシートを使用して[複数のサードパーティ広告をアップロード &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 新しいキャンペーンをアクティブ化する準備が整うまで一時停止します。

* 次の点を考慮し、必要に応じて新しいキャンペーンを編集します。

   * 新しいキャンペーン予算に対応するのに十分な資金をアカウントに確保していますか？

   * 新しいキャンペーンには、以前のキャンペーンとは異なる予算が必要ですか？

   * どのプレースメントにも最低予算は必要ですか？

   * 必要なカスタム広告の重み付けやスケジュールなどを含むクリエイティブをアップロードし、プレースメントに添付します。

   * 必要に応じて、イベントピクセルをプレースメントと広告に添付します。

   * プレースメントに必要に応じて、地理的ターゲットとプレースメントレベルの[!DNL DoubleVerify Authentic Brand Safety] セグメントを含めます。

   * プログラマティックな保証取引の場合は、新しい取引IDを使用して、デフォルトのプレースメントを作成します。

   * 必要に応じて、[!UICONTROL Simple Ad Serving]件の取引用に新しいプレースメントを作成します。

* パフォーマンスキャンペーン（カスタム最適化目標を使用するパッケージを含むキャンペーン）の場合、各パッケージに[[!UICONTROL Linked Package for Optimization Learnings Carryover]設定](/help/dsp/campaign-management/packages/package-settings.md)を使用して、パッケージを最適化するための入力として前のキャンペーンの履歴データを使用します。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのキャンペーン管理について](campaign-about.md)
>* [&#x200B; キャンペーンを作成](campaign-create.md)
>* [&#x200B; キャンペーンを編集](campaign-edit.md)
>* [&#x200B; キャンペーンの変更ログを表示](campaign-change-log.md)
>* [&#x200B; キャンペーン設定](campaign-settings.md)
