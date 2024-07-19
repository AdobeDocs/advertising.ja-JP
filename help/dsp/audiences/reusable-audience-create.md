---
title: 再利用可能なオーディエンスを作成
description: オーディエンスセグメントとその他の保存済みオーディエンスで構成される、再利用可能なオーディエンスを作成する方法について説明します。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '485'
ht-degree: 0%

---

# 再利用可能なオーディエンスを作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

再利用可能なオーディエンス（オーディエンスセグメントのグループや、複数のプレースメントのターゲットまたは除外として使用できる他の保存済みオーディエンスでさえグループ）を保存および管理できます。

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL All Audiences]** をクリックします。

1. データ テーブルの上にある [**[!UICONTROL Create]**] をクリックします。

1. 一意の **[!UICONTROL Audience Name]** を入力します。

1. （オプション） **[!UICONTROL Share with all advertisers in my account]** すオプションの選択を解除します。

   オーディエンスを共有すると、アカウント内のすべての広告主に対するターゲットまたは除外として、オーディエンスを使用できるようになります。 ただし、オーディエンスの個々のセグメントは、そのセグメントが共有されているユーザーのみが使用できます。 例えば、同じ [!DNL Analytics] アカウントにマッピングされていない広告主とAdobe Analytics セグメントを含むオーディエンスを共有した場合、その広告主に対してそのオーディエンスでセグメントがプレビューされません。 その広告主が使用できるセグメントのみがオーディエンスでプレビューされます。

1. 「**[!UICONTROL Save]**」をクリックします。

1. オーディエンスを作成します。

   >[!NOTE]
   >
   >オーディエンスを作成すると、右側のパネルで詳細な [ オーディエンスサイズデータ ](audience-about.md) が更新されます

   * 「[[!UICONTROL Third Party Segments]」、「[!UICONTROL First Party Segments]」、「[!UICONTROL Adobe Segments]」、「[!UICONTROL Custom Segments]」および「[!UICONTROL Saved Audiences]」タブで使用可能なセグメントを使用してセグメントロジックを手動で作成するには ](audience-settings.md) 次の手順を実行します。

      * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

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

1. 「**[!UICONTROL Create]**」をクリックします。

>[!MORELIKETHIS]
>
>* [Audience Management について ](audience-about.md)
>* [ オーディエンス設定 ](audience-settings.md)
>* [ オーディエンスセグメントロジックの構文 ](audience-segment-logic-syntax.md)
>* [ 利用可能なサードパーティデータプロバイダー ](third-party-data-providers.md)
>* [ カスタムセグメントの作成と実装 ](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントの作成と実装 ](ccpa-opt-out-segment-create.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
