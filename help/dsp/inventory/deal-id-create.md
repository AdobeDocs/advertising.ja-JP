---
title: 取引IDの詳細を手動で作成する
description: 案件IDの詳細を手動で入力する方法について説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
TQID: https://experienceleague.adobe.com/lg8BJhKDVNRKrZNr5WJLhDt7HU2pz7p-zTU6ShU2yCE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: ac506c20-96f2-48f6-9096-77706e336bdaid: fae3ff5f-9a75-4de1-a100-c90dd8268528
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 427
ht-degree: 0%

---

# 取引IDの詳細を手動で作成する

1. メインメニューで、**[!UICONTROL Inventory]** > **[!UICONTROL Deals].**&#x200B;をクリックします

1. データテーブルの上で「**[!UICONTROL Create]**」をクリックし、「**[!UICONTROL Deal ID]**」を選択します。

1. [取引設定](deal-id-settings.md)を入力します。

   1. 「[!UICONTROL Deal ID basics]」セクションで、取引の詳細と、取引にアクセスできる広告主を指定します。 保証された契約の場合は、追跡目的でのみ、計画されたフライト日とインプレッション数を指定する必要があります。

      在庫/取引ビューに「PG インプレッションのペーシング」支出列を含めることで、保証された取引のペーシングを追跡できます。

   1. （管理者ユーザーのみ。オプション）「[!UICONTROL Technical]」セクションで、必要に応じてデフォルト設定を編集します。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. （保証された契約のみ）契約に使用する広告（またはパブリッシャーが管理する広告の1x1 ピクセル）を選択し、デフォルトのプログラマティック保証（PG）プレースメントを作成します。

   デフォルトのPG プレースメントでは、入札リクエストごとに常に入札が返されるようにします。 デフォルトのPG プレースメントを作成しない場合、取引をターゲットとするプレースメントは、正しく設定されていない限り入札を行いません。 常にデフォルトのPG プレースメントを作成する必要があります。 [!UICONTROL Placements] ビューでは、デフォルトのPG プレースメントの列値は[!UICONTROL Sub-type]です。「[!UICONTROL PG Default]」

   オプションで、追加のプレースメントで在庫ターゲットとして取引を使用できますが、入札を行うには正しく設定する必要があります。

   1. [!UICONTROL Ad & Campaign Selection]設定で、取引に使用する広告を選択します。

      1. 広告主、キャンペーン、広告タイプを選択します。 オプションで、広告をフィルタリングする広告ステータスを選択します。

      1. 利用可能な広告のリストから、取引に使用する各広告の横にあるチェックボックスを選択します。

         パブリッシャーが管理する広告ごとに、広告主とキャンペーンが選択された後、1x1のトラッキングピクセルが自動的に適用されます。

      1. **[!UICONTROL Apply]**&#x200B;をクリックします。

   1. プレースメント設定画面で、次の操作を行います。

      1. プレースメント名を入力します。

      1. （オプション） [ プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)を編集します。これには、取引のCPM値が自動的に入力されるデフォルト入札額の上書き、日付範囲の変更、追加の広告の添付などが含まれます。

      取引は、「在庫目標」セクションで自動的にターゲット設定されます。 その他のターゲティングオプションは適用できません。

      1. **[!UICONTROL Create placement]**&#x200B;をクリックします。

取引を作成した後、その取引を複数のプレースメントの在庫ターゲットとして使用できます。

>[!NOTE]
>
> 確認のために契約タグをパブリッシャーに送信する必要はありません。

>[!TIP]
>
>* [!UICONTROL Inventory] > [!UICONTROL Deals] ビューでは、[!UICONTROL Pacing & Budget]列に、指定されたフライト日とインプレッション目標に対する取引のペーシング方法が表示されます。
>
>* 配信の量が不足している場合や、ペースが過剰な場合は、メディア企業に連絡して、成約を通じて送信する配信数を調整してください。

>[!MORELIKETHIS]
>
>* [取引情報IDの手動設定](deal-id-settings.md)
>* [ プログラム的な保証契約の設定](programmatic-guaranteed-set-up.md)
>* [様とのプログラムで保証された契約の広告を送信 [!DNL FreeWheel]](freewheel-submit.md)
>* [ プログラマティック保証取引について](programmatic-guaranteed-about.md)
<!-- >* [Specify placements and ads for a private deal](deal-id-attach-placements.md)-->
