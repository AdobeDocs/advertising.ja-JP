---
title: '[!UICONTROL Deal ID Inbox]で取引を承認'
description: 契約ID インボックスを使用して、 [!DNL FreeWheel], [!DNL Google Authorized Buyers]  （旧称 [!DNL AdX]), and [!DNL Magnite DV+]  （旧称 [!DNL Rubicon]）の発行者と既に交渉した非公開契約を承認する方法について説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 7c681ab7-3051-451d-ab83-fc75bdd6eaad
TQID: https://experienceleague.adobe.com/8ORfCWhZbjGVKi3YvY0g-yp-Gys6dyabLSMvpXOszHc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 308
ht-degree: 0%

---

# [!UICONTROL Deal ID Inbox]で取引を承認

*SSP アカウントのみにマッピングされているDSP アカウントのユーザー*

[!UICONTROL Deal ID Inbox]を使用して、[!DNL FreeWheel]、[!DNL Google Authorized Buyers] （旧称[!DNL AdX]）、[!DNL Magnite DV+] （旧称[!DNL Rubicon]）にパブリッシャーと既に交渉した非公開取引をすばやく承認します。

>[!NOTE]
>
>[!DNL FreeWheel]でパブリッシャーとのプログラム的な保証取引を設定するには、追加の権限と手順が必要です。 詳しくは、「[FreeWheelでのプログラマティック保証取引の設定の概要](freewheel-overview.md)」を参照してください。

1. メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**&#x200B;をクリックします

1. [!UICONTROL Deals]のリストの上で、青いバーをクリックして[!UICONTROL Deal ID Inbox]を開きます。

1. （オプション）取引の詳細を更新するには、**[!UICONTROL Refresh]**&#x200B;をクリックします。

   DSPでは、東部標準時の午前4:30時に、すべての取引詳細が毎日自動的に更新されます。 また、すべての[!DNL FreeWheel]件の取引が更新され、1時間ごとに[!DNL Google]と[!DNL Magnite DV+]から既存の取引が更新されます。

1. （以前に契約を無視した場合）「**[!UICONTROL Ignored Deals]**」タブをクリックします。

1. 発行者や日付などの取引詳細を確認するには、取引行にカーソルを置き、![&#x200B; レビュー](/help/dsp/assets/review.png)をクリックします。

1. 次のいずれかの操作を行います。

   * 取引の詳細で、**[!UICONTROL Accept]**&#x200B;をクリックします。

   * [!UICONTROL Deal ID Inbox]で、取引の行にカーソルを置き、![承諾](/help/dsp/assets/accept.png)をクリックします。

1. 契約の詳細：
   1. 必要な情報（**[!UICONTROL Publisher]**、**[!UICONTROL Media Type]**、および&#x200B;**[!UICONTROL Deal Access]**）（契約へのアクセス権を持つ広告主）を入力します。
   1. （オプション）取引を共有するか、取引レコードにラベルを添付する追加アカウントを指定します。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （プログラマティック保証取引のみ）プロンプトに従って、取引の広告（またはパブリッシャーが管理する広告の1x1 トラッキングピクセル）を選択し、取引をターゲットとするプログラマティック保証されたデフォルトのプレースメントを作成します。

取引を承認すると、その取引は[!UICONTROL Deal ID Inbox]から[!UICONTROL Inventory] > [!UICONTROL Deals] ビューに移動され、各配置の[!UICONTROL Inventory Targeting] セクションでプライベート在庫ソースとして利用できるようになります。

>[!MORELIKETHIS]
>
>* [について[!UICONTROL Deal ID Inbox]](deal-id-inbox-about.md)
>* [&#x200B; プログラム的な保証契約の設定](programmatic-guaranteed-set-up.md)
>* [様とのプログラムで保証された契約の広告を送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [&#x200B; プログラマティック保証取引について](programmatic-guaranteed-about.md)
>* [在庫機能の概要](inventory-overview.md)
