---
title: PG 契約の広告を  [!DNL FreeWheel] に送信します。
description: ' [!DNL Freewheel] で、プログラムで保証されたパブリッシャーとの取引に対する広告の承認をリクエストする方法を説明します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 18d91f0c-4a27-4e40-b762-6c5e97e9a21a
source-git-commit: 14f78b89dea8cc680756232c6116975c652feee5
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 0%

---

# プログラムで保証された取引の広告を [!DNL Freewheel] に送信

*[!DNL FreeWheel] プログラムで保証された権限のみを持つアカウント*

広告の選択や取引に使用するプログラムで保証されたデフォルトの配置の作成など、FreeWheel 上のパブリッシャーとのプログラムで保証された取引を [&#x200B; 承認 &#x200B;](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox) したら、その広告を承認を得るために [!DNL Freewheel] に送信する必要があります。

>[!PREREQUISITES]
>
>Adobeアカウントチームと協力して、[!DNL DSP] アカウントに [!DNL FreeWheel] プログラムで保証されたワークフローを使用する権限があることを確認します。

1. [!DNL Freewheel] の取引で使用される広告の広告キーをコピーします。

   1. キャンペーンの名前をクリックします。

   1. サブメニューで、**[!UICONTROL Ads]** をクリックします。

   1. 広告名の横にある **[!UICONTROL ...]**/**[!UICONTROL Edit]** をクリックします。

   1. 広告設定が開いたら、ブラウザーのアドレスバーに表示される URL の英数字とキーをコピーします。

      例えば、次の URL では、広告キーは `3NtNC5ZbaGZtqbei8jD3` です

      ```
      https://advertising.adobe.com/configurator/ad/3NtNC5ZbaGZtqbei8jD3?referrer=/playtime/ads
      ```

1. [!DNL Freewheel] に広告を送信します。

   1. 次のいずれかの操作をおこないます。

      * 広告名の横で、**[!UICONTROL ...]**/**[!UICONTROL submit to FreeWheel]** をクリックします。

      * メインメニューで、**[!UICONTROL Inventory]**/**[!UICONTROL Deals]** をクリックします。 取引行で、![&#x200B; オプションメニュー &#x200B;](/help/dsp/assets/options-menu.png) > **[!UICONTROL submit to FreeWheel]** をクリックします。

   1. 取引 ID を確認し、手順 1 でコピーした **[!UICONTROL Ad Key]** を入力して、「**[!UICONTROL Submit]**」をクリックします。

   広告は、実行する前に送信し承認する必要があります。

1. [&#x200B; 広告送信ステータスを確認します &#x200B;](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [&#x200B; プログラムで保証された取引の設定の概要  [!DNL Freewheel]](freewheel-overview.md)
>* [&#x200B; 取引 ID インボックスでの取引の承認 &#x200B;](deal-id-inbox-accept.md)
>* [&#x200B; プログラムで保証された取引の広告  [!DNL FreeWheel]  ステータスの確認 &#x200B;](freewheel-check-status.md)
>* [&#x200B; 広告送信  [!DNL Freewheel]  エラーコード &#x200B;](freewheel-error-codes.md)
