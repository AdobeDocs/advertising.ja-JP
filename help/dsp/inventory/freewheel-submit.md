---
title: '[!DNL FreeWheel]へのPG契約の広告を送信'
description: '[!DNL FreeWheel]のパブリッシャーとのプログラマティック保証取引の広告の承認をリクエストする方法について説明します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
TQID: 'https://experienceleague.adobe.com/f6Cu6mG77YOjwshI4xVbkLSkykAhqXonfSMg5ynDK5g'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
  - id: 20c71a28-1f3b-56af-ad52-f3281489a219
    internal-label: DSP Private Inventory
  - id: 85825b7c-c02c-536d-b821-66dc33454fb8
    internal-label: DSP Deal IDs
subfeature_v2:
  - id: ac506c20-96f2-48f6-9096-77706e336bda
    internal-label: Private Inventory
  - id: fae3ff5f-9a75-4de1-a100-c90dd8268528
    internal-label: Deal IDs
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '235'
ht-degree: 0%
---
# プログラムで保証された契約の広告を[!DNL FreeWheel]に送信します

[!DNL FreeWheel]のプログラムで保証された権限を持つ&#x200B;*アカウントのみ*

広告の選択や、取引に使用するプログラマティック保証のデフォルトプレースメントの作成など、FreeWheel[&#128279;](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)上のパブリッシャーとのプログラマティック保証取引を承認したら、広告を[!DNL FreeWheel]に送信して承認を得る必要があります。

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

      * メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals]**&#x200B;をクリックします。 取引行で、![&#x200B; オプション メニュー](/help/dsp/assets/options-menu.png)/**[!UICONTROL submit to FreeWheel]**&#x200B;をクリックします。

   1. 取引IDを確認し、手順1でコピーした&#x200B;**[!UICONTROL Ad Key]**&#x200B;を入力し、**[!UICONTROL Submit]**&#x200B;をクリックします。

   広告は、実行前に送信して承認する必要があります。

1. [広告送信ステータスを確認](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [でのプログラムによる保証取引の設定の概要 [!DNL FreeWheel]](freewheel-overview.md)
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [PG取引 [!DNL FreeWheel] の広告のステータスを確認する](freewheel-check-status.md)
>* [広告の送信](freewheel-error-codes.md)のエラーコード [!DNL FreeWheel] 
