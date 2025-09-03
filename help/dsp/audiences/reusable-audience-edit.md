---
title: 再利用可能なオーディエンスを編集
description: 再利用可能なオーディエンスを編集する方法を説明します。
feature: DSP Audiences
exl-id: 4de6b9a4-2907-474d-92bf-83686a1f0b31
source-git-commit: 0afe1d9985c1451c28943aaa17c7d6f8a73a95ef
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# 再利用可能なオーディエンスを編集

任意のプレースメントや他の再利用可能なオーディエンスで使用されているオーディエンスを編集すると、それらのプレースメントやオーディエンスに変更が直ちに適用されます。<!-- verify -->

>[!NOTE]
>
>（DSPがハッシュ化されたメール ID を LiveRamp RampID セグメントに変換する広告主）アクティブ、スケジュール済み、一時停止のプレースメントに関連付けられていないファーストパーティの RampID セグメントは一時停止されます。 セグメントは、セグメントリストに「自動一時停止」と表示されます。

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL All audiences]** をクリックします。

1. オーディエンスの行の上にカーソルを置き、**[!UICONTROL Edit]** をクリックします。

1. 次のいずれかの方法で、オーディエンス設定を編集します。

   >[!NOTE]
   >
   >オーディエンスセグメントロジックを編集すると、右側のパネルで詳細な [ オーディエンスサイズデータ ](audience-about.md) が更新されます。

   * （任意）オーディエンスを編集するには、オーディ **[!UICONTROL Audience Name]** ンス名の横にある ![ 編集 ](/help/dsp/assets/edit.png) をクリックし、一意のオーディエンス名を入力して、「**[!UICONTROL Apply]**」をクリックします。

   * （オプション）「[[!UICONTROL Third Party Segments]」、「[!UICONTROL First Party Segments]」、「[!UICONTROL Adobe Segments]」、「[!UICONTROL Custom Segments]」および「[!UICONTROL Saved Audiences]」タブで使用可能なセグメントを使用してセグメントロジックを手動で編集するには ](audience-settings.md) 次の手順を実行します。

      * 既存のセグメントグループにセグメントを追加するには：

      1. 右側のパネルでセグメントグループをクリックします。

      1. （オプション）必要に応じて、グループロジックを *[!UICONTROL Include Any]*、*[!UICONTROL Include All]* または *[!UICONTROL Exclude All]* に変更します。

         最初のセグメントグループには *[!UICONTROL Exclude All]* は使用できません。 除外のみを含むオーディエンスの場合、このオーディエンスを *[!UICONTROL Include Any]* のように作成し、プレースメント内で除外オーディエンス メニューからオーディエンスを選択します。

      1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

         セグメントグループは、新しいセグメントで自動的に更新されます。

   * 新しいセグメントグループを追加するには：

      1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

      1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを *[!UICONTROL And]* または *[!UICONTROL Or]* に変更します。

      1. 左側のパネルで新しいグループのセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

      1. （オプション）必要に応じて、グループロジックを *[!UICONTROL Include Any]*、*[!UICONTROL Include All]* または *[!UICONTROL Exclude All]* に変更します。

   * 既存のオーディエンスからセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * すべてのオーディエンス ビューで、オーディエンス行の上にカーソルを置き、**[!UICONTROL More]**/**[!UICONTROL Copy to Clipboard]** をクリックします。

         * 既存オーディエンスの設定のセグメント論理パネルの上部で、**[!UICONTROL More]**/**[!UICONTROL Copy to Clipboard]** をクリックします。

         * テキストエディターで、英数字のセグメント ID と [ ブール構文 ](audience-segment-logic-syntax.md) を使用してセグメントロジックを手動で作成し、クリップボードにコピーします。

      1. 「**[!UICONTROL paste in an audience rule to begin building]**」をクリックし、既存のセグメントロジックを入力フィールドに貼り付けて、「**[!UICONTROL Apply]**」をクリックします。

         >[!NOTE]
         >
         >オーディエンスに既にセグメントロジックが含まれている場合、新しいセグメントロジックを貼り付けると、既存のロジックが上書きされます。

1. 「**[!UICONTROL Save]**」をクリックします。

1. 確認メッセージで、「**[!UICONTROL Continue]**」をクリックします。

>[!MORELIKETHIS]
>
>* [Audience Management について ](audience-about.md)
>* [ 再利用可能なオーディエンスを作成 ](reusable-audience-create.md)
>* [ 再利用可能なオーディエンスを複製 ](reusable-audience-duplicate.md)
>* [ 再利用可能なオーディエンスに関する詳細の表示 ](reusable-audience-view-details.md)
>* [ 再利用可能なオーディエンスの共有 ](reusable-audience-share.md)
>* [ 再利用可能なオーディエンスの書き出し ](reusable-audience-export.md)
>* [ 再利用可能なオーディエンスのセグメントキーをクリップボードにコピー ](reusable-audience-clipboard.md)
>* [ 再利用可能なオーディエンスを削除 ](reusable-audience-delete.md)
>* [ オーディエンス設定 ](audience-settings.md)
>* [ オーディエンスセグメントロジックの構文 ](audience-segment-logic-syntax.md)
>* [ 利用可能なサードパーティデータプロバイダー ](third-party-data-providers.md)
