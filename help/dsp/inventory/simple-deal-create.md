---
title: '[!UICONTROL Simple Ad Serving]件の取引を作成'
description: '[!UICONTROL Simple Ad Serving]件のトラッキングピクセルの作成方法を説明します。'
feature: DSP Simple Ad Serving
exl-id: 77d5dabd-1a0d-4dce-8a9a-8d54a637e15d
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '384'
ht-degree: 0%

---

# [!UICONTROL Simple Ad Serving]件の取引を作成

1. メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**&#x200B;をクリックします

1. データテーブルの上で「**[!UICONTROL Create]**」をクリックし、「**[!UICONTROL Simple Ad Serving]**」を選択します。

1. [取引設定](simple-deal-settings.md)を入力します。

   1. [!UICONTROL Select Ad Source] セクションで、パブリッシャー、広告主とキャンペーン、広告タイプに関する情報を指定し、**[!UICONTROL Next]**&#x200B;をクリックします。

   1. 「[!UICONTROL Select Ad(s)]」セクションで、DSPでプロキシとして使用する広告を指定します。

      1. 次のいずれかの操作を行います。

         * 既存の広告の場合は、使用する広告を選択します。

         * 新しい広告の場合は、プロキシ [&#x200B; サードパーティ広告](/help/dsp/campaign-management/ads/ad-create-multiple.md)を作成します。

      >[!NOTE]
      > DSPでは、指定した広告は配信されません。 発行者が広告を配信します。

      1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. フィードの詳細で、フィードの詳細を編集し、**[!UICONTROL Next]**&#x200B;をクリックします。

      DSPは、広告の「SAS Placement - &lt;*契約名*>」という名前のプレースメントを自動的に生成します。 プレースメントでは、契約は[!UICONTROL Inventory Targets] セクションで自動的にターゲット設定されます。 その他のターゲティングオプションは適用できません。

1. イベントトラッキングピクセルをパブリッシャーに送信して、次のいずれかの方法で実装します。

   * （オプション） [!UICONTROL Activate Tag with Publisher]画面から、取引タグをパブリッシャーに送信します。

     前の手順を完了すると、DSPによってパブリッシャーに送信できるメールメッセージが生成されます。 メッセージには、取引の詳細、取引タグを取得するためのリンク、およびリンクの認証コードが含まれます。

      1. 取引の詳細を確認し、次のいずれかの操作を行います。

         * デバイス上の電子メールアプリケーションの電子メールメッセージに情報を貼り付けるには、**[!UICONTROL Email & Done]**&#x200B;をクリックし、電子メールアプリケーションを選択します。 [!UICONTROL CC:] フィールドには、[!DNL Adobe] サポート アドレスが事前入力されています。 その後、パブリッシャーの適切な連絡先にメッセージを送信できます。

         * 情報をクリップボードにコピーするには、**[!UICONTROL Copy Email]をクリックします。**&#x200B;その後、コンテンツを手動で電子メール メッセージに貼り付け、発行者の適切な担当者に送信できます。 `publisher-support-global@adobe.com`へのコピー（CC:）を含めます。 メッセージのコピーが完了したら、**[!UICONTROL Email & Done]**&#x200B;をクリックします。

      1. （必要に応じて）発行者にフォローアップして、タグが発行者の広告サーバーと連携するように、適切なマクロが含まれているかどうかを確認します。

   * （オプション）イベントトラッキングピクセルをパブリッシャーに手動で送信します。

      1. [!UICONTROL Deals] ビュー内の取引行で、![&#x200B; オプション メニュー](/help/dsp/assets/options-menu.png) **>[!UICONTROL show pixel]**&#x200B;をクリックします。

         イベントピクセルは、[!UICONTROL Clickthrough] ピクセルと[!UICONTROL Impression] ピクセルとを含む。 ビデオ広告およびオーディオ広告には、完了した四分位数ごとのイベントピクセルも含まれます（[!UICONTROL 25% Complete]から[!UICONTROL 100% Complete]）。

      1. イベントトラッキングピクセルをコピーし、パブリッシャーに提供します。

>[!MORELIKETHIS]
>
>* [約[!UICONTROL Simple Ad Serving]](simple-deal-about.md)
>* [[!UICONTROL Simple Ad Serving]設定](simple-deal-settings.md)
>* [取引に関する詳細なレポートを表示](/help/dsp/inventory/deal-view-report.md)

<!--
 add back when reimplemented:
>* [View event-tracking pixels for a [!UICONTROL Simple Ad Serving] deal](simple-deal-show-pixels.md)
-->
