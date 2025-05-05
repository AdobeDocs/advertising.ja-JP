---
title: プレースメントの作成
description: プレースメントの作成方法を説明します。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
source-git-commit: 9b3d6893e004b16714bf50f1334424d50fac7c91
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# プレースメントの作成

>[!TIP]
>
>キャンペーンの特定の目標やレポートのニーズに基づいてプレースメントを作成します。

1. メインメニューで、「**[!UICONTROL Campaigns]**」をクリックします。

1. プレースメントを含めるキャンペーンの名前をクリックします。

1. データ テーブルの上にある [**[!UICONTROL Create]**] をクリックします。 メニューの「[!UICONTROL Placement Types]」セクションで、配置タイプをクリックします。

   プレースメントのタイプによって、プレースメントに含めることができる広告タイプが決まります。

1. [ 配置設定 ](placement-settings.md) を入力します。

   1. [!UICONTROL Placement Basics] の設定を指定します。

   1. 「[!UICONTROL Goals]」セクションで、[!UICONTROL Gross Budget] を指定し、オプションで追加の配置目標を指定します。

      一部のフィールドには、上書きできるデフォルト値が設定されています。

      プレースメントが割り当てられたパッケージにパッケージレベルのペーシングがある場合、目標とペーシング設定はパッケージ設定を反映します。

   1. （任意） [!UICONTROL Geo-Targeting] セクションで、含める場所または除外する場所を絞り込みます。

      特定の場所を識別しない場合は、すべての場所がターゲットになります。

      >[!NOTE]
      >
      >Roku プレースメントでは、市区町村と DMA の場所は使用できません。

   1. 「[!UICONTROL Inventory Targeting]」セクションで、含めるか除外する在庫ソースを絞り込みます。

      ほとんどのプレースメント タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 プレースメント [!DNL Roku] 場合、在庫タイプとソースを指定する必要があります。

   1. （オプション） [!UICONTROL Site Targeting] セクションで、ターゲットにするサイトを絞り込み、除外するサイトを指定します。

   1. （オプション） [!UICONTROL Audience Targeting] のセクションで、次の操作を行います。

      1. オーディエンスを絞り込みます。 これには、プレースメント内でターゲットとするオーディエンスセグメントの選択が含まれます。

         [!DNL Roku] プレースメントの場合、[!DNL Roku] （オプトイン）の決定論的データセットと照合できる 1 つ以上のオーディエンスセグメントを含めることで  [!DNL Roku][&#128279;](/help/dsp/inventory/roku-inventory.md)DSPでの一意のオーディエンスマッチングを活用できます。

      1. （人物レベルのクロスデバイスターゲティングを使用するキャンペーンの場合。オプション）プレースメントで 1 つ以上の特定のオーディエンスをターゲットにする場合は、プレースメントの人物ベースのクロスデバイスターゲティングを有効にします。

         人物ベースのクロスデバイスターゲティングは、米国のデータのみを使用する [!DNL LiveRamp] によって提供されます。 このサービスは、[!DNL LiveRamp] デバイスグラフを使用して配信されるインプレッション（つまり、ターゲットのオーディエンスセグメント内に見つからないデバイス）に対して、午後 0.35 CPM ドルですべての広告主が利用できます。

   1. （任意） [!DNL Brand Safety and Media Targeting] のセクションで、プレースメントにブランドセーフティ制限を適用します。

   1. （任意）「[!DNL Tracking]」セクションで、プレースメントの広告についてサードパーティのイベントのピクセルまたはコンバージョンピクセルを入力します。

      >[!NOTE]
      >
      >（[!DNL Roku] のプレースメント） [!DNL Roku] によって承認されたサードパーティのピクセルベンダーには、[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk] および [!DNL Research Now] が含まれます。

1. 「**[!UICONTROL Create Placement]**」をクリックします。

1. （任意）プレースメントに広告を添付します。

   1. 「**[!UICONTROL Attach an ad]**」をクリックします。

   1. 次のいずれかの操作をおこないます。

      * 新しい広告を作成するには：

         1. 「**[!UICONTROL Create a New Ad].**」をクリックします。

         1. [ オーディオ広告 ](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[ 接続テレビ ](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[ ディスプレイ広告 ](/help/dsp/campaign-management/ads/ad-settings-display.md)、[ モバイル広告 ](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[ ネイティブ広告 ](/help/dsp/campaign-management/ads/ad-settings-native.md)、[ プリロール広告 ](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md) または [ ユニバーサルビデオ広告 ](/help/dsp/campaign-management/ads/ad-settings-universal-video.md) の広告設定を指定します。

        >[!NOTE]
        >
        >ユニバーサルビデオプレースメントには、ユニバーサルビデオ広告のみを含めることができます。

         1. 「**[!UICONTROL Save & Submit for Review]**」をクリックします。

         1. （オプション）プレースメントに対して作成する追加広告ごとに「**[!UICONTROL Attach Another Ad]**」をクリックし、手順 1 ～ 3 を繰り返します。

         1. 既存の広告を添付しない場合は、「**[!UICONTROL I'm done for now]**」をクリックします。

      * キャンペーンに既存の広告を添付する手順は次のとおりです。

      1. 「**[!UICONTROL Select an Ad]**」をクリックします。

      1. 次のいずれかの操作をおこないます。

         * 広告を 1 つずつ追加するには：

            1. 広告名の横の「**[!UICONTROL Select].**」をクリックします。

            1. （オプション）添付する追加の広告ごとに [**[!UICONTROL Attach Another Ad]**] をクリックし、同じ操作を繰り返します。

         * 一度に最大 20 件の広告を追加するには：

            1. 広告リストの上のチェックボックスを選択します。

            1. 追加する各広告の横にあるチェックボックスをオンにします。

            1. 「**[!UICONTROL Attach]**」をクリックします。

            1. 広告名の横の「**[!UICONTROL Select]**」をクリックします。

      1. （任意）プレースメント内の特定の広告に対してデフォルトのフライト期間と広告の回転を上書きするには：

         1. 「**[!UICONTROL Custom Schedule Ads]**」をクリックします。

         1. 次のいずれかの操作をおこないます。

            * フライトを追加するには、[**[!UICONTROL Add Flight]**] をクリックし、開始日と終了日を指定します。

            * 既存のフライトを広告に追加するには、フライト列の広告行の **[!UICONTROL +]** をクリックします。

            * 既存のフライトを広告から削除するには、フライト列の広告行の **[!UICONTROL x]** をクリックします。

            * （複数の広告が同じフライトを持つ場合）広告を不均等に回転させるには、フライト情報の **[!UICONTROL Even Rotation]** をクリックし、各広告を回転させる相対的な重みをパーセントで入力します。

              合計重量は 100 にする必要があります。

         1. 右上で、「**[!UICONTROL Continue]**」をクリックします。

         1. フライトの詳細を確認し、[**[!UICONTROL Save & Finish]**] をクリックします。

>[!MORELIKETHIS]
>
>* [ プレースメント管理について ](placement-about.md)
>* [ プレースメントを編集 ](placement-edit.md)
>* [ プレースメントの入札乗数の管理 ](placement-manage-bid-multipliers.md)
>* [ プレースメントの広告スケジュールの編集 ](placement-edit-ad-schedule.md)
>* [ プレースメントの一時停止またはアクティブ化 ](placement-pause-activate.md)
>* [ プレースメントの変更ログを表示 ](placement-change-log.md)
>* [ プレースメント設定 ](placement-settings.md)
>* [ 配置予測レポートの表示 ](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [ ショートカットキー ](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [ パフォーマンスのトラブルシューティング ](/help/dsp/optimization/troubleshooting-performance.md)
>* [ ビデオ：標準の表示配置を作成する方法 ](https://video.tv.adobe.com/v/345001?captions=jpn)
