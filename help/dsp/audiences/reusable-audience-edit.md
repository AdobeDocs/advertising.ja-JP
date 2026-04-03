---
title: 再利用可能なオーディエンスの編集
description: 再利用可能なオーディエンスを編集する方法を説明します。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
TQID: https://experienceleague.adobe.com/NkmnBZ5GKhOxmOJZhIS8-V99cV7x2-DTl-tp1cij8W4
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 459
ht-degree: 0%

---

# 再利用可能なオーディエンスの編集

任意のプレースメントまたはその他の再利用可能なオーディエンスで使用されるオーディエンスを編集すると、変更は直ちにそれらのプレースメントとオーディエンスに適用されます。<!-- verify -->

>[!NOTE]
>
>（DSPがハッシュ化されたメール IDをLiveRamp RampID セグメントに変換する広告主）アクティブなプレースメント、スケジュール済みプレースメント、または一時停止されたプレースメントにアタッチされていないファーストパーティのRampID セグメントは一時停止されます。 セグメントは、「自動一時停止」としてセグメントリストに表示されます。

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL All audiences]**&#x200B;をクリックします。

1. オーディエンス行の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. オーディエンス設定を次のいずれかの方法で編集します。

   >[!NOTE]
   >
   >オーディエンスセグメントロジックを編集すると、右側のパネルで詳細な[ オーディエンスサイズデータ ](audience-about.md)が更新されます。

   * （オプション）オーディエンス名の横にある&#x200B;**[!UICONTROL Audience Name]**&#x200B;編集![をクリックして](/help/dsp/assets/edit.png)を編集するには、一意のオーディエンス名を入力し、**[!UICONTROL Apply]**&#x200B;をクリックします。

   * （オプション） [[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]、および[!UICONTROL Saved Audiences] タブ ](audience-settings.md)で使用可能なセグメントを使用して、セグメントロジックを手動で編集するには、次の操作を行います。

      * 既存のセグメントグループにセグメントを追加するには：

      1. 右側のパネルでセグメントグループをクリックします。

      1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

         *[!UICONTROL Exclude All]*&#x200B;は、最初のセグメント グループでは使用できません。 除外のみを含むオーディエンスの場合は、このオーディエンスを&#x200B;*[!UICONTROL Include Any]*&#x200B;として作成し、プレースメント内の除外オーディエンス メニューからそのオーディエンスを選択します。

      1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

         セグメントグループは、新しいセグメントで自動的に更新されます。

   * 新しいセグメントグループを追加するには：

      1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

      1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;*[!UICONTROL And]*&#x200B;または&#x200B;*[!UICONTROL Or]*&#x200B;に変更します。

      1. 左側のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスを選択します。

      1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

   * 既存のオーディエンスからセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * すべてのオーディエンス ビューで、オーディエンス行の上にカーソルを置き、**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**&#x200B;をクリックします。

         * 既存のオーディエンスの設定で、セグメントロジックパネルの上部にある「**[!UICONTROL More]**」 > 「**[!UICONTROL Copy to Clipboard]**」をクリックします。

         * テキストエディターで、英数字のセグメント IDと[ ブール構文](audience-segment-logic-syntax.md)を使用してセグメントロジックを手動で作成し、クリップボードにコピーします。

      1. **[!UICONTROL paste in an audience rule to begin building]**&#x200B;をクリックし、既存のセグメントロジックを入力フィールドに貼り付け、**[!UICONTROL Apply]**&#x200B;をクリックします。

         >[!NOTE]
         >
         >オーディエンスにセグメントロジックが既に含まれている場合、新しいセグメントロジックにペーストすると、既存のロジックが上書きされます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Continue]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ オーディエンス管理について](audience-about.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [再利用可能なオーディエンスを複製](reusable-audience-duplicate.md)
>* [再利用可能なオーディエンスに関する詳細を表示](reusable-audience-view-details.md)
>* [再利用可能なオーディエンスを共有](reusable-audience-share.md)
>* [再利用可能なオーディエンスの書き出し](reusable-audience-export.md)
>* [再利用可能なオーディエンスのセグメントキーをクリップボードにコピー](reusable-audience-clipboard.md)
>* [再利用可能なオーディエンスを削除](reusable-audience-delete.md)
>* [ オーディエンス設定](audience-settings.md)
>* [ オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
