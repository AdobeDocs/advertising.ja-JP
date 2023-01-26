---
title: の作成 [!UICONTROL Simple Ad Serving] 契約
description: のトラッキングピクセルを作成する方法を説明します。 [!UICONTROL Simple Ad Serving] 契約
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 1a98b3ba7c37a768825e9e48db7d847f12daa9a0
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# の作成 [!UICONTROL Simple Ad Serving] 契約

1. メインメニューで、 **[!UICONTROL Inventory]** > **[!UICONTROL Deals].**

1. データテーブルの上にある **[!UICONTROL Create]**&#x200B;を選択し、 **[!UICONTROL Simple Ad Serving]**.

1. 次を入力します。 [取引設定](simple-deal-settings.md):

   1. 内 [!UICONTROL Select Ad Source] セクションで、パブリッシャー、広告主、キャンペーン、広告の種類に関する情報を指定し、 **[!UICONTROL Next]**.

   1. 内 [!UICONTROL Select Ad(s)] セクションで、DSPでプロキシとして使用する広告を指定します。

      1. 次のいずれかの操作を行います。

         * 既存の広告の場合、使用する広告を選択します。

         * 新しい広告の場合は、プロキシを作成します [サードパーティ広告](/help/dsp/campaign-management/ads/ad-create-multiple.md).
      >[!NOTE]
      > DSPは、指定した広告を提供しません。 パブリッシャーが広告を提供します。

      1. クリック **[!UICONTROL Next]**.
   1. 「 Feed Details 」で、フィードの詳細を編集し、 **[!UICONTROL Next]**.

      DSPは、「SAS Placement - &lt;」という名前の配置を自動的に生成します。*契約名*>、&quot;（広告の） 配置では、契約は [!UICONTROL Inventory Targets] 」セクションに入力します。 その他のすべてのターゲット設定オプションは適用できません。



1. 次のいずれかの方法で、実装用にイベントトラッキングピクセルをパブリッシャーに送信します。

   * （オプション） [!UICONTROL Activate Tag with Publisher] 画面に表示され、投稿者に契約タグを送信します。

      上記の手順を完了すると、DSPは、投稿者に送信できる電子メールメッセージを生成します。 このメッセージには、契約の詳細、契約タグの取得元となるリンク、およびリンクの認証コードが含まれます。

      1. 契約の詳細を確認し、次のいずれかを実行します。

         * デバイス上の電子メールアプリケーションの電子メールメッセージに情報を貼り付けるには、 **[!UICONTROL Email & Done]** 電子メールアプリケーションを選択します。 この [!UICONTROL CC:] フィールドに [!DNL Adobe] サポートアドレス。 その後、投稿者に適した連絡先にメッセージを送信できます。

         * 情報をクリップボードにコピーするには、 **[!UICONTROL Copy Email].** その後、電子メールメッセージにコンテンツを手動で貼り付け、投稿者に適した連絡先に送信できます。 コピー (CC:) をに含める必要があります `publisher-support-global@adobe.com`. メッセージのコピーが完了したら、 **[!UICONTROL Email & Done]**.
      1. （必要に応じて）投稿者に対してフォローアップを実行し、タグに適切なマクロが含まれているかどうかを確認します。これにより、タグが投稿者の広告サーバーで機能するようになります。
   * （オプション）パブリッシャーにイベント追跡ピクセルを手動で送信します。

      1. 内の契約行 [!UICONTROL Deals] 表示、クリック ![オプションメニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**.

         イベントピクセルには、 [!UICONTROL Clickthrough] ピクセルと [!UICONTROL Impression] ピクセル。 ビデオおよびオーディオ広告には、四分位数ごとに ( [!UICONTROL 25% Complete] から [!UICONTROL 100% Complete]) をクリックします。

      1. イベント追跡ピクセルをコピーし、投稿者に提供します。



>[!MORELIKETHIS]
>
>* [について [!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving] 設定](simple-deal-settings.md)
>* [契約の詳細レポートの表示](/help/dsp/inventory/deal-view-report.md)


<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
