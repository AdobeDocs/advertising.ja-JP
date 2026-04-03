---
title: ' [!DNL FreeWheel]でのPG取引の設定の概要'
description: ' [!DNL FreeWheel]でパブリッシャーとのプログラマティック保証取引の広告を実行するために必要な前提条件と追加の手順について説明します。'
feature: DSP Private Inventory, DSP Deal IDs
exl-id: b9c60248-8104-42ef-8afb-2f9db67b33b0
TQID: https://experienceleague.adobe.com/8ovkE7w5qXW7Csibxy-PyHvUud0wwrhdSTulQP7bIeM
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 222
ht-degree: 0%

---

# [!DNL FreeWheel]でのプログラマティック保証取引の設定の概要

[!DNL FreeWheel]でパブリッシャーとのプログラム的な保証取引を設定するには、追加の権限と手順が必要です。

>[!PREREQUISITES]
>
>Adobe アカウントチームと協力して、[!DNL DSP] アカウントに次の権限があることを確認します。
>
>* プログラマティック保証取引の広告を[!DNL FreeWheel]に送信するために必要な[!DNL FreeWheel] プログラマティック保証付きワークフローを使用する権限。
>
>* （広告ごとに[!DNL Clearcast] クロック番号を必要とする英国のパブリッシャーと連携している場合）広告にクロック番号を含める権限。

## ワークフロー

1. 取引で指定されたメディアタイプを使用して広告を作成します。

   一部の英国のパブリッシャーの場合は、広告に[!DNL Clearcast] クロック番号を含める必要があります。

1. [取引ID インボックスを使用して、既に](#programmatic-guaranteed-set-up.md#pg-setup-deal-id-inbox)の発行者と交渉した取引ID[!DNL FreeWheel]を承認します。

   取引を承認したら、プロンプトに従って、1）取引に使用する広告を選択し、2）広告を配信するためのプログラマティックな保証されたデフォルトのプレースメントを作成します。

1. [広告を [!DNL FreeWheel]に送信](freewheel-submit.md)

   広告は、実行前に送信して承認する必要があります。

1. [広告送信ステータスを確認](freewheel-check-status.md)。

>[!MORELIKETHIS]
>
>* [[!UICONTROL Deal ID Inbox]](deal-id-inbox-accept.md)で取引を承諾
>* [ プログラマティック保証取引の広告を [!DNL FreeWheel]](freewheel-submit.md)に送信します
>* [PG取引 [!DNL FreeWheel] の広告のステータスを確認する](freewheel-check-status.md)
>* [広告の送信 [!DNL FreeWheel] のエラーコード](freewheel-error-codes.md)
