---
title: '[!UICONTROL Simple Ad Serving] しい取引の作成'
description: '[!UICONTROL Simple Ad Serving] しい取引のトラッキングピクセルを作成する方法を説明します。'
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 443f8907644bf3e480626e14713e8abb9bfca284
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving] しい取引の作成

1. メインメニューで、**[!UICONTROL Inventory]**/**[!UICONTROL Deals].** をクリックします。

1. データ テーブルの上の [**[!UICONTROL Create]**] をクリックし、[**[!UICONTROL Simple Ad Serving]**] を選択します。

1. [&#x200B; 取引設定 &#x200B;](simple-deal-settings.md) を入力します。

   1. [[!UICONTROL Select Ad Source]] セクションで、発行元、広告主、およびキャンペーンに関する情報、広告の種類を指定し、[**[!UICONTROL Next]**] をクリックします。

   1. [!UICONTROL Select Ad(s)] セクションで、DSPでプロキシとして使用する広告を指定します。

      1. 次のいずれかの操作をおこないます。

         * 既存の広告の場合は、使用する広告を選択します。

         * 新しい広告の場合は、プロキシ [&#x200B; サードパーティ広告 &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md) を作成します。

      >[!NOTE]
      > DSPは指定した広告を配信しません。 出版社が広告を出す。

      1. 「**[!UICONTROL Next]**」をクリックします。

   1. [ フィードの詳細 ] で、フィードの詳細を編集し、[**[!UICONTROL Next]**] をクリックします。

      DSPは、「SAS Placement - &lt;*deal name*>」という名前のプレースメントを広告に対して自動生成します。 プレースメントでは、契約は自動的に「[!UICONTROL Inventory Targets]」セクションでターゲットになります。 その他のターゲティングオプションはすべて適用されません。

1. 次のいずれかの方法で、実装のためにイベントトラッキングピクセルをパブリッシャーに送信します。

   * （任意） [!UICONTROL Activate Tag with Publisher] 画面から、取引タグをパブリッシャーに送信します。

     前の手順を完了すると、DSPによってメールメッセージが送信され、パブリッシャーに送信できます。 メッセージには、取引の詳細、取引タグの取得元のリンク、リンクの認証コードが含まれています。

      1. 取引の詳細を確認し、次のいずれかの操作を行います。

         * デバイス上のメールアプリケーションのメールメッセージに情報を貼り付けるには、「**[!UICONTROL Email & Done]**」をクリックしてメールアプリケーションを選択します。 「[!UICONTROL CC:]」フィールドには、[!DNL Adobe] のサポートアドレスが事前入力されます。 その後、メッセージを発行者の適切な連絡先に送信できます。

         * クリップボードに情報をコピーするには、[**[!UICONTROL Copy Email]] をクリックします。** その後、コンテンツをメールメッセージに手動で貼り付け、発行者の適切な連絡先に送信できます。 `publisher-support-global@adobe.com` にコピー（CC:）を含める必要があります。 メッセージのコピーが終了したら、[**[!UICONTROL Email & Done]**] をクリックします。

      1. （必要に応じて）公開者にフォローアップして、タグに適切なマクロが含まれているかどうかを確認し、タグが公開者の広告サーバーで機能するようにします。

   * （オプション）イベントトラッキングピクセルをパブリッシャーに手動で送信します。

      1. [!UICONTROL Deals] ビュー内の取引行で、![&#x200B; オプションメニュー &#x200B;](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]** をクリックします。

         イベントピクセルは、[!UICONTROL Clickthrough] 画素および [!UICONTROL Impression] 画素を含む。 ビデオおよびオーディオ広告には、四分位数によるイベントピクセルも含まれます（[!UICONTROL 25% Complete] から [!UICONTROL 100% Complete]）。

      1. イベントトラッキングのピクセルをコピーして、公開者に提供します。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Simple Ad Serving]](simple-deal-about.md) について
>* [[!UICONTROL Simple Ad Serving] Settings](simple-deal-settings.md)
>* [&#x200B; 取引の詳細レポートの表示 &#x200B;](/help/dsp/inventory/deal-view-report.md)

<!-- add back when reimplemented:
>* [View Event-Tracking Pixels for a [!UICONTROL Simple Ad Serving] Deal](simple-deal-show-pixels.md)
-->
