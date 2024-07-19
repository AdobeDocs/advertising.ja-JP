---
title: 取引 ID の詳細の手動作成
description: 取引 ID の詳細を手動で入力する方法を説明します。
feature: DSP Private Inventory, DSP Deal IDs
exl-id: 20a57919-c68f-4c9d-a8e1-f49484f74655
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '427'
ht-degree: 0%

---

# 取引 ID の詳細の手動作成

1. メインメニューで、**[!UICONTROL Inventory]**/**[!UICONTROL Deals].** をクリックします。

1. データ テーブルの上の [**[!UICONTROL Create]**] をクリックし、[**[!UICONTROL Deal ID]**] を選択します。

1. [ 取引設定 ](deal-id-settings.md) を入力します。

   1. [!UICONTROL Deal ID basics] のセクションでは、取引の詳細と、取引にアクセスできる広告主を指定します。 保証された取引の場合は、トラッキング目的でのみ、予定フライト日と推定インプレッション数も指定する必要があります。

      在庫/取引ビューの「PG インプレッションペーシング」支出列を含めることで、保証された取引のペーシングを追跡できます。

   1. （管理者ユーザーのみ。オプション）「[!UICONTROL Technical]」セクションで、必要に応じてデフォルト設定を編集します。

   1. 「**[!UICONTROL Save]**」をクリックします。

1. （保証された取引のみ）取引に使用する広告（またはパブリッシャーが管理する広告の 1x1 ピクセル）を選択し、デフォルトのプログラム保証（PG）プレースメントを作成します。

   デフォルトの PG 配置では、取引が常に各入札要求の入札を返すようにします。 デフォルトの PG プレースメントを作成しない場合、取引をターゲットとするプレースメントは、正しく設定されていない限り入札を行いません。 常にデフォルトの PG プレースメントを作成する必要があります。 [!UICONTROL Placements] ビューでは、デフォルトの PG 配置の [!UICONTROL Sub-type] 列値は「[!UICONTROL PG Default]」です。

   オプションで、追加のプレースメントで取引を在庫ターゲットとして使用できますが、入札を行うには正しく設定する必要があります。

   1. [!UICONTROL Ad & Campaign Selection] の設定で、取引に使用する広告を選択します。

      1. 広告主、キャンペーンおよび広告タイプを選択します。 必要に応じて、広告をフィルタリングするための広告ステータスを選択します。

      1. 使用可能な広告のリストから、取引に使用する各広告の横にあるチェックボックスを選択します。

         パブリッシャーが管理する各広告に対して、広告主およびキャンペーンが選択された後、1x1 のトラッキングピクセルが自動的に適用されます。

      1. 「**[!UICONTROL Apply]**」をクリックします。

   1. プレースメント設定画面で、次の操作を行います。

      1. 配置名を入力します。

      1. （オプション）デフォルトの入札を上書きする [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md) の編集（契約の CPM 値が自動的に入力される）、日付範囲を変更する、広告を追加するなど）。

      取引は「在庫ターゲット」セクションで自動的にターゲットされます。 その他のターゲティングオプションはすべて適用されません。

      1. 「**[!UICONTROL Create placement]**」をクリックします。

取引を作成した後、その取引を複数のプレースメントの在庫ターゲットとして使用できます。

>[!NOTE]
>
> 検証のために契約タグをパブリッシャーに送信する必要はありません。

>[!TIP]
>
>* [!UICONTROL Inventory]/[!UICONTROL Deals] 表示の [!UICONTROL Pacing & Budget] の列には、指定されたフライト日とインプレッション目標に対して契約がどのようにペーシングされているかが表示されます。
>
>* 配信のペースがアンダーペーシングまたはオーバーペーシングの場合は、パブリッシャーに連絡して、契約を通じて送信される量を調整してください。

>[!MORELIKETHIS]
>
>* [ 手動の取引 ID 設定 ](deal-id-settings.md)
>* [ プログラムで保証された取引の設定 ](programmatic-guaranteed-set-up.md)
>* [ プログラムで保証された取引の広告を送信  [!DNL FreeWheel]](freewheel-submit.md)
>* [ プログラムで保証された取引について ](programmatic-guaranteed-about.md)
<!-- >* [Specify Placements and Ads for a Private Deal](deal-id-attach-placements.md)-->
