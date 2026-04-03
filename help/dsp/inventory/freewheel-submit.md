---
title: ' [!DNL FreeWheel]へのPG契約の広告の送信'
description: ' [!DNL FreeWheel]のパブリッシャーとのプログラマティック保証取引の広告の承認をリクエストする方法を説明します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 237
ht-degree: 0%

---

# プログラムで保証された契約の広告を[!DNL FreeWheel]に送信します

*のプログラムで保証された権限を持つ[!DNL FreeWheel] アカウントのみ*

広告の選択や、取引に使用するプログラマティック保証のデフォルトプレースメントの作成など、FreeWheel[上のパブリッシャーとのプログラマティック保証取引を](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)承認したら、広告を[!DNL FreeWheel]に送信して承認を得る必要があります。

>[!PREREQUISITES]
>
>Adobe アカウントチームと協力して、[!DNL DSP] アカウントに[!DNL FreeWheel] プログラマティック保証ワークフローを使用する権限があることを確認します。

1. [!DNL FreeWheel]件の案件で使用されている広告の広告キーをコピーします：

   1. キャンペーンの名前をクリックします。

   1. サブメニューで、**[!UICONTROL Ads]**&#x200B;をクリックします。

   1. 広告名の横にある&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックします。

   1. 広告設定を開いたら、ブラウザーのアドレスバーに表示されるURLに英数字の広告キーをコピーします。

      例えば、次のURLでは、広告キーは`3NtNC5ZbaGZtqbei8jD3`です

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. 広告を[!DNL FreeWheel]に送信：

   1. 次のいずれかの操作を行います。

      * 広告名の横にある「**[!UICONTROL ...]** > **[!UICONTROL submit to FreeWheel]**」をクリックします。

      * メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals]**&#x200B;をクリックします。 取引行で、![ オプション メニュー](/help/dsp/assets/options-menu.png)/**[!UICONTROL submit to FreeWheel]**&#x200B;をクリックします。

   1. 取引IDを確認し、手順1でコピーした&#x200B;**[!UICONTROL Ad Key]**&#x200B;を入力し、**[!UICONTROL Submit]**&#x200B;をクリックします。

   広告は、実行前に送信して承認する必要があります。

1. [広告送信ステータスを確認](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [でのプログラムによる保証取引の設定の概要 [!DNL FreeWheel]](freewheel-overview.md)
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [PG取引 [!DNL FreeWheel] の広告のステータスを確認する](freewheel-check-status.md)
>* [広告の送信 [!DNL FreeWheel] のエラーコード](freewheel-error-codes.md)
