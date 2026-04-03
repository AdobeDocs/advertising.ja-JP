---
title: プレースメントの作成
description: プレースメントの作成方法を説明します。
feature: DSP Placements
exl-id: 28a328b1-0839-442e-a245-f586a7042f41
TQID: https://experienceleague.adobe.com/QEpUfFvrVq62P64w-7gwFk2ujuCNzkegHKz6UancZDY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 701
ht-degree: 0%

---

# プレースメントの作成

>[!TIP]
>
>特定のキャンペーン目標やレポートニーズにもとづいて、プレースメントを作成できます。

1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. プレースメントを含めるキャンペーンの名前をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。 メニューの[!UICONTROL Placement Types] セクションで、配置タイプをクリックします。

   プレースメントの種類によって、プレースメントに含めることができる広告の種類が決まります。

1. [&#x200B; プレースメント設定](placement-settings.md)を入力します。

   1. [!UICONTROL Placement Basics]設定を指定します。

   1. [!UICONTROL Goals] セクションで、[!UICONTROL Gross Budget]を指定し、オプションでプレースメントの目標を追加します。

      一部のフィールドには、上書きできるデフォルト値があります。

      プレースメントが割り当てられているパッケージにパッケージレベルのペーシングがある場合、目標とペーシング設定にはパッケージ設定が反映されます。

   1. （オプション）「[!UICONTROL Geo-Targeting]」セクションで、含まれる場所または除外される場所を絞り込みます。

      特定の場所を特定しない場合は、すべての場所がターゲットになります。

      >[!NOTE]
      >
      >Roku プレースメントでは、市区町村とDMAの場所は使用できません。

   1. [!UICONTROL Inventory Targeting] セクションで、含めるインベントリ ソースまたは除外するインベントリ ソースを絞り込みます。

      ほとんどの配置タイプでは、すべての在庫タイプと各タイプのすべてのソースがデフォルトで含まれています。 [!DNL Roku]件のプレースメントの場合は、在庫タイプとソースを指定する必要があります。

   1. （オプション）「[!UICONTROL Site or app And Keyword Targeting]」セクションで、ターゲットにして除外するサイトとアプリを絞り込みます。

   1. （オプション） [!UICONTROL Audience Targeting] セクションで：

      1. オーディエンスを絞り込む： これには、プレースメント内でターゲティングするオーディエンスセグメントの選択も含まれます。

         [!DNL Roku]個のプレースメントの場合、[&#x200B; （オプトイン）決定論的データセットと照合できる1つ以上のオーディエンスセグメントを含めることで、 [!DNL Roku]](/help/dsp/inventory/roku-inventory.md)と一致する[!DNL Roku]DSPの一意のオーディエンスを活用できます。

         アクティブなプレースメント、スケジュールされたプレースメント、または一時停止されたプレースメントにアタッチされていないファーストパーティのRampID セグメントは一時停止されます。 セグメントは、「自動一時停止」としてセグメントリストに表示されます。

      1. （ピープルレベルのクロスデバイスターゲティングを使用するキャンペーンの場合。オプション）プレースメントが1つ以上の特定のオーディエンスをターゲットにしている場合は、プレースメントのピープルベースのクロスデバイスターゲティングを有効にします。

         ピープルベースのクロスデバイスターゲティングは、米国のデータのみを使用して[!DNL LiveRamp]によって提供されます。 このサービスは、[!DNL LiveRamp] デバイスグラフを使用して配信されるインプレッション（ターゲットオーディエンスセグメント内に見つからないデバイス）に対して、すべての広告主が0.35 CPMで利用できます。

   1. （オプション）「[!DNL Brand Safety and Media Targeting]」セクションで、プレースメントにブランドセーフティ制限を適用します。

   1. （オプション）「[!DNL Tracking]」セクションで、プレースメント内の広告のサードパーティイベントピクセルまたはコンバージョンピクセルを入力します。

      >[!NOTE]
      >
      >（[!DNL Roku] プレースメント） [!DNL Roku]によって承認されたサードパーティのピクセルベンダーには、[!DNL Acxiom]、[!DNL Comscore]、[!DNL Data Plus Math]、[!DNL Experian]、[!DNL Factual]、[!DNL Kantar]、[!DNL Marketing Evolution]、[!DNL Neustar]、[!DNL Nielsen]、[!DNL Nielsen Catalina Solutions]、[!DNL NinthDecimal]、[!DNL Oracle]、[!DNL Placed]、[!DNL Polk]、および[!DNL Research Now]が含まれます。

1. **[!UICONTROL Create Placement]**&#x200B;をクリックします。

1. （オプション）広告をプレースメントに添付します。

   1. **[!UICONTROL Attach an ad]**&#x200B;をクリックします。

   1. 次のいずれかの操作を行います。

      * 新しい広告を作成するには：

         1. **[!UICONTROL Create a New Ad].**&#x200B;をクリックします

         1. [&#x200B; オーディオ広告](/help/dsp/campaign-management/ads/ad-settings-audio.md)、[&#x200B; コネクテッド TV](/help/dsp/campaign-management/ads/ad-settings-connected-tv.md)、[&#x200B; ディスプレイ広告](/help/dsp/campaign-management/ads/ad-settings-display.md)、[&#x200B; モバイル広告](/help/dsp/campaign-management/ads/ad-settings-mobile.md)、[&#x200B; ネイティブ広告](/help/dsp/campaign-management/ads/ad-settings-native.md)、[&#x200B; プレロール広告](/help/dsp/campaign-management/ads/ad-settings-pre-roll.md)、または[&#x200B; ユニバーサルビデオ広告](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)の広告設定を指定します。

        >[!NOTE]
        >
        >ユニバーサルビデオの配置には、ユニバーサルビデオ広告のみを含めることができます。

         1. **[!UICONTROL Save & Submit for Review]**&#x200B;をクリックします。

         1. （オプション）プレースメント用に作成する追加広告ごとに、**[!UICONTROL Attach Another Ad]**&#x200B;をクリックし、手順1 ～ 3を繰り返します。

         1. 既存の広告を添付しない場合は、**[!UICONTROL I'm done for now]**&#x200B;をクリックします。

      * キャンペーン内の既存の広告を添付するには：

         1. **[!UICONTROL Select an Ad]**&#x200B;をクリックします。

         1. 次のいずれかの操作を行います。

            * 一度に1つの広告を追加するには：

               1. 広告名の横にある「**[!UICONTROL Select]」をクリックします。**

               1. （オプション）添付する各追加広告について、**[!UICONTROL Attach Another Ad]**&#x200B;をクリックし、プロセスを繰り返します。

            * 一度に最大20個の広告を追加するには：

               1. 広告リストの上にあるチェックボックスをオンにします。

               1. 追加する各広告の横にあるチェックボックスをオンにします。

               1. **[!UICONTROL Attach]**&#x200B;をクリックします。

               1. 広告名の横にある「**[!UICONTROL Select]**」をクリックします。

         1. （オプション）プレースメント内の特定の広告のデフォルトのフライト期間と広告ローテーションを上書きするには：

            1. **[!UICONTROL Custom Schedule Ads]**&#x200B;をクリックします。

            1. 次のいずれかの操作を行います。

               * フライトを追加するには、**[!UICONTROL Add Flight]**&#x200B;をクリックし、開始日と終了日を指定します。

               * 既存のフライトを広告に追加するには、フライト列の広告行の&#x200B;**[!UICONTROL +]**&#x200B;をクリックします。

               * 広告から既存のフライトを削除するには、フライト列の広告行の&#x200B;**[!UICONTROL x]**&#x200B;をクリックします。

               * （複数の広告に同じフライトがある場合）広告を不均等に回転させるには、フライト情報の&#x200B;**[!UICONTROL Even Rotation]**&#x200B;をクリックし、各広告を回転させる相対的な重みをパーセント単位で入力します。

                 重みの合計は100に等しくなければなりません。

            1. 右上の「**[!UICONTROL Continue]**」をクリックします。

            1. フライトの詳細を確認し、**[!UICONTROL Save & Finish]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising DSPでのプレースメント管理について](placement-about.md)
>* [&#x200B; プレースメントを編集](placement-edit.md)
>* [&#x200B; プレースメントの入札乗数を管理](placement-manage-bid-multipliers.md)
>* [&#x200B; プレースメントの広告スケジュールを編集](placement-edit-ad-schedule.md)
>* [&#x200B; プレースメントを非アクティブ化またはアクティブ化](placement-pause-activate.md)
>* [&#x200B; プレースメントの変更ログを表示](placement-change-log.md)
>* [配置の設定](placement-settings.md)
>* [&#x200B; プレースメント予測レポートを表示](/help/dsp/campaign-management/reports/placement-forecast.md)
>* [&#x200B; ユニバーサルビデオに関するFAQ](/help/dsp/campaign-management/faq-universal-video.md)
>* [&#x200B; キーボードショートカット &#x200B;](/help/dsp/campaign-management/reports/keyboard-shortcuts.md)
>* [&#x200B; パフォーマンスのトラブルシューティング &#x200B;](/help/dsp/optimization/troubleshooting-performance.md)
>* [&#x200B; ビデオ：標準の表示配置を作成する方法](https://video.tv.adobe.com/v/345001?captions=jpn)
