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

1. メインメニューで、 **[!UICONTROL Campaigns]**.

1. プレースメントを含めるキャンペーンの名前をクリックします。

1. データ テーブルの上で、 **[!UICONTROL Create]**. が含まれる [!UICONTROL Placement Types] メニューのセクションで、配置タイプをクリックします。

   プレースメントのタイプによって、プレースメントに含めることができる広告タイプが決まります。

1. を入力 [プレースメント設定](placement-settings.md):

   1. を指定 [!UICONTROL Placement Basics] 設定。

   1. が含まれる [!UICONTROL Goals] セクションで、 [!UICONTROL Gross Budget] また、オプションで、追加の配置目標を指定します。

      一部のフィールドには、上書きできるデフォルト値が設定されています。

      プレースメントが割り当てられたパッケージにパッケージレベルのペーシングがある場合、目標とペーシング設定はパッケージ設定を反映します。

   1. （オプション） [!UICONTROL Geo-Targeting] セクションでは、含める場所または除外する場所を絞り込みます。

      特定の場所を識別しない場合は、すべての場所がターゲットになります。

      >[!NOTE]
      >
      >Roku プレースメントでは、市区町村と DMA の場所は使用できません。

   1. が含まれる [!UICONTROL Inventory Targeting] セクションで、含めるか除外する在庫ソースを絞り込みます。

      ほとんどのプレースメント タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれます。 の場合 [!DNL Roku] プレースメントでは、在庫タイプとソースを指定する必要があります。

   1. （オプション） [!UICONTROL Site Targeting] セクションで、ターゲットにするサイトを絞り込み、除外するサイトを指定します。

   1. （オプション） [!UICONTROL Audience Targeting] セクション：

      1. オーディエンスを絞り込みます。 これには、プレースメント内でターゲットとするオーディエンスセグメントの選択が含まれます。

         の場合 [!DNL Roku] プレースメントを利用する [との一意のオーディエンスのマッチングをDSP [!DNL Roku]](/help/dsp/inventory/roku-inventory.md) と照合できる 1 つ以上のオーディエンスセグメントを含めることで答えることができます。 [!DNL Roku] （オプトイン）決定論的データセット。

      1. （人物レベルのクロスデバイスターゲティングを使用するキャンペーンの場合。オプション）プレースメントで 1 つ以上の特定のオーディエンスをターゲットにする場合は、プレースメントの人物ベースのクロスデバイスターゲティングを有効にします。

         人物ベースのクロスデバイスターゲティングは、次のように提供されます [!DNL LiveRamp] 米国のデータのみを使用します。 このサービスは、を使用して配信されるインプレッションに対して、すべての広告主が午後 0.35 ドルで利用できます [!DNL LiveRamp] デバイスグラフ（ターゲットオーディエンスセグメント内に見つからないデバイス用）。

   1. （オプション） [!DNL Brand Safety and Media Targeting] セクションでは、プレースメントにブランドセーフティ制限を適用します。

   1. （オプション） [!DNL Tracking] 「」セクションで、プレースメント内の広告についてサードパーティのイベントピクセルまたはコンバージョンピクセルを入力します。

      >[!NOTE]
      >
      >（[!DNL Roku] プレースメント）が承認したサードパーティピクセルベンダー [!DNL Roku] 次を含める [!DNL Acxiom], [!DNL Comscore], [!DNL Data Plus Math], [!DNL Experian], [!DNL Factual], [!DNL Kantar], [!DNL Marketing Evolution], [!DNL Neustar], [!DNL Nielsen], [!DNL Nielsen Catalina Solutions], [!DNL NinthDecimal], [!DNL Oracle], [!DNL Placed], [!DNL Polk]、および [!DNL Research Now].

1. クリック **[!UICONTROL Create Placement]**.

1. （任意）プレースメントに広告を添付します。

   1. クリック **[!UICONTROL Attach an ad]**.

   1. 次のいずれかの操作をおこないます。

      * 新しい広告を作成するには：

         1. クリック **[!UICONTROL Create a New Ad].**

         1. 広告設定を指定： [オーディオ広告](/help/dsp/campaign-management/ads/ad-settings-audio.md), [接続された TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md), [広告の表示](/help/dsp/campaign-management/ads/ad-settings-display.md), [モバイル広告](/help/dsp/campaign-management/ads/ad-settings-mobile.md), [ネイティブ広告](/help/dsp/campaign-management/ads/ad-settings-native.md), [プリロール広告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)、または [ユニバーサルビデオ広告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md).

        >[!NOTE]
        >
        >ユニバーサルビデオプレースメントには、ユニバーサルビデオ広告のみを含めることができます。

         1. クリック **[!UICONTROL Save & Submit for Review]**.

         1. （オプション）プレースメント用に作成する追加広告ごとに、 **[!UICONTROL Attach Another Ad]**&#x200B;手順 1 ～ 3 を繰り返します。

         1. 既存の広告を添付しない場合は、 **[!UICONTROL I'm done for now]**.

      * キャンペーンに既存の広告を添付する手順は次のとおりです。

      1. クリック **[!UICONTROL Select an Ad]**.

      1. 次のいずれかの操作をおこないます。

         * 広告を 1 つずつ追加するには：

            1. 広告名の横にある「」をクリックします。 **[!UICONTROL Select].**

            1. （オプション）添付する追加広告ごとに、 **[!UICONTROL Attach Another Ad]**&#x200B;を選択し、このプロセスを繰り返します。

         * 一度に最大 20 件の広告を追加するには：

            1. 広告リストの上のチェックボックスを選択します。

            1. 追加する各広告の横にあるチェックボックスをオンにします。

            1. クリック **[!UICONTROL Attach]**.

            1. 広告名の横にある「」をクリックします。 **[!UICONTROL Select]**.

      1. （任意）プレースメント内の特定の広告に対してデフォルトのフライト期間と広告の回転を上書きするには：

         1. クリック **[!UICONTROL Custom Schedule Ads]**.

         1. 次のいずれかの操作をおこないます。

            * フライトを追加するには、をクリックします **[!UICONTROL Add Flight]**&#x200B;を選択し、開始日と終了日を指定します。

            * 広告に既存のフライトを追加するには、をクリックします **[!UICONTROL +]** フライト列の広告行

            * 広告から既存のフライトを削除するには、をクリックします。 **[!UICONTROL x]** フライト列の広告行

            * （複数の広告が同じフライトを持つ場合）広告を不均等に回転するには、をクリックします **[!UICONTROL Even Rotation]** フライト情報で、各広告を回転させる相対的な重みをパーセントで入力します。

              合計重量は 100 にする必要があります。

         1. 右上のをクリック **[!UICONTROL Continue]**.

         1. フライトの詳細を確認し、 **[!UICONTROL Save & Finish]**.

>[!MORELIKETHIS]
>
>* [プレースメント管理について](placement-about.md)
>* [プレースメントを編集](placement-edit.md)
>* [プレースメントの入札乗数の管理](placement-manage-bid-multipliers.md)
>* [プレースメントの広告スケジュールの編集](placement-edit-ad-schedule.md)
>* [プレースメントの一時停止またはアクティブ化](placement-pause-activate.md)
>* [プレースメントの変更ログの表示](placement-change-log.md)
>* [プレースメント設定](placement-settings.md)
>* [配置予測レポートの表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [ユニバーサルビデオに関する FAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [ショートカットキー](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [トラブルシューティングのパフォーマンス](/help/dsp/optimization/troubleshooting-performance.md)
>* [ビデオ：標準の表示配置を作成する方法](https://video.tv.adobe.com/v/340454)
