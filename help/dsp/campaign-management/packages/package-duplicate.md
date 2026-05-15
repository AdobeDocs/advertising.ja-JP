---
title: パッケージの複製
description: パッケージを複製する方法を説明します。
feature: DSP Packages
exl-id: 75842776-a024-43c9-aaf8-1126c0b9d717
TQID: https://experienceleague.adobe.com/fbOXyvipyiJ7rOlCroMLHvSqCqXPIEL9FTHmqm7CQu8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fddd8d8f-3ba1-4a22-b714-69d0e4655be8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: fdc899fcc763a963e5878b2fcf313174b8f5a74b
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 0%

---

# パッケージの複製

パッケージを複製して、同様の設定を持つパッケージを作成します。 次の操作を実行できます。

* パッケージを元の広告主とキャンペーン内、または別の広告主内で複製します

* オプションで、パッケージ内のプレースメントを複製します

* （元のキャンペーン内の重複したパッケージの場合）オプションで、元の広告とプレースメントレベルのイベントピクセルを複製します

* 新しいパッケージのフライト日を変更する

重複しないプレースメント設定のリストについては、「[重複していないもの](#package-not-duplicated)」を参照してください。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. キャンペーンの名前をクリックして、[!UICONTROL Packages] ビューを開きます。

1. パッケージ名の横にある「**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**」をクリックします。

1. 新しいパッケージ設定を指定します。

   1. 新しいパッケージ名を入力します。

   1. （オプション）デフォルト設定を変更します。

      デフォルトでは：

      * 新しいパッケージは、元の広告主とキャンペーンに割り当てられます。

      * 新しいパッケージは現在の日付にアクティブになります。<!-- and the flight continues for NN  days. -->

      * 元のパッケージ内のプレースメントは、新しいパッケージにコピーされます。

      * 広告とプレースメントレベルのイベントピクセルは、新しいパッケージにコピーされません。

1. **[!UICONTROL Submit]**&#x200B;をクリックします。

## 重複していないもの {#package-not-duplicated}

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
   * プレースメントレベル [!DNL DoubleVerify Authentic Brand Suitability] セグメント （広告主レベルのセグメントを上書きする）

## 新しいパッケージを設定するためのベストプラクティス

>[!TIP]
>
>* バルクシートを使用すると、一度に[複数のキャンペーンコンポーネントに変更を加えることができます](/help/dsp/campaign-management/campaign-components-review-edit.md)。
>* 広告タグシートを使用して[複数のサードパーティ広告をアップロード ](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

* 新しいパッケージをアクティブ化する準備ができるまで一時停止します。

* 次の点を考慮し、必要に応じて新しいパッケージを編集します。

   * 新しいパッケージの予算に対応するのに十分な資金をアカウントに確保していますか？

   * 新しいパッケージには、以前のパッケージとは異なる予算が必要ですか？

   * どのプレースメントにも最低予算は必要ですか？

   * 必要なカスタム広告の重み付けやスケジュールなどを含むクリエイティブをアップロードし、プレースメントに添付します。

   * 必要に応じて、イベントピクセルをプレースメントと広告に添付します。

   * プレースメントに必要に応じて、地理的ターゲットとプレースメントレベルの[!DNL DoubleVerify Authentic Brand Suitability] セグメントを含めます。

   * プログラマティックな保証取引の場合は、新しい取引IDを使用して、デフォルトのプレースメントを作成します。

   * 必要に応じて、[!UICONTROL Simple Ad Serving]件の取引用に新しいプレースメントを作成します。

* カスタム最適化目標を使用するパッケージの場合、各パッケージに[[!UICONTROL Linked Package for Optimization Learnings Carryover]設定](/help/dsp/campaign-management/packages/package-settings.md)を使用して、パッケージを最適化するための入力として前のキャンペーンの履歴データを使用します。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのパッケージ管理について](package-about.md)
>* [ パッケージを作成](package-create.md)
>* [ パッケージの編集](package-edit.md)
>* [ パッケージの変更ログを表示](package-change-log.md)
>* [ パッケージ設定](package-settings.md)
