---
title: 再利用可能なオーディエンスを作成
description: オーディエンスセグメントとその他の保存済みオーディエンスで構成される、再利用可能なオーディエンスを作成する方法について説明します。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
source-git-commit: eb3ce7d8bcddf52844b50797a95cb3b5aec13684
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 0%

---

# 再利用可能なオーディエンスを作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

再利用可能なオーディエンス（オーディエンスセグメントのグループや、複数のプレースメントのターゲットまたは除外として使用できる他の保存済みオーディエンスでさえグループ）を保存および管理できます。

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**.

1. データ テーブルの上で、 **[!UICONTROL Create]**.

1. 一意のを入力 **[!UICONTROL Audience Name]**.

1. （オプション）次のオプションを選択解除します **[!UICONTROL Share with all advertisers in my account]**.

   オーディエンスを共有すると、アカウント内のすべての広告主に対するターゲットまたは除外として、オーディエンスを使用できるようになります。 ただし、オーディエンスの個々のセグメントは、そのセグメントが共有されているユーザーのみが使用できます。 例えば、Adobe Analytics セグメントを含むオーディエンスを、同じユーザーにマッピングされていない広告主と共有する場合です [!DNL Analytics] アカウントに追加された場合、そのセグメントは、その広告主のそのオーディエンスでプレビューされなくなります。 その広告主が使用できるセグメントのみがオーディエンスでプレビューされます。

1. クリック **[!UICONTROL Save]**.

1. オーディエンスを作成します。

   >[!NOTE]
   >
   >オーディエンスを作成する際の詳細 [オーディエンスサイズデータ](audience-about.md) 右側のパネルで更新済み

   * で使用可能なセグメントを使用して、セグメントロジックを手動で作成するには [[!UICONTROL Third Party Segments], [!UICONTROL First Party Segments], [!UICONTROL Adobe Segments], [!UICONTROL Custom Segments]、および [!UICONTROL Saved Audiences] タブ](audience-settings.md)、次の手順を実行します。

      * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

      * 既存のセグメントグループにセグメントを追加するには：

         1. 右側のパネルでセグメントグループをクリックします。

         1. （オプション）グループロジックをに変更します *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*、または *[!UICONTROL Exclude All]*、必要に応じて。

            *[!UICONTROL Exclude All]* 最初のセグメントグループには使用できません。 除外のみを含むオーディエンスの場合、このオーディエンスをとして作成します *[!UICONTROL Include Any]* 次に、プレースメント内の除外オーディエンス メニューからオーディエンスを選択します。

         1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

            セグメントグループは、新しいセグメントで自動的に更新されます。

      * 新しいセグメントグループを追加するには：

         1. クリック **[!UICONTROL + New Group]** 右側のパネルに表示されます。

         1. （オプション）前のグループと新しいグループの間のロジックをに変更します *[!UICONTROL And]* または *[!UICONTROL Or]*、必要に応じて。

         1. 左側のパネルで新しいグループのセグメントを見つけ、セグメント名の横にあるチェックボックスをオンにします。

         1. （オプション）グループロジックをに変更します *[!UICONTROL Include Any]*, *[!UICONTROL Include All]*、または *[!UICONTROL Exclude All]*、必要に応じて。

   * 既存のオーディエンスからセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * すべてのオーディエンス ビューで、オーディエンス行の上にカーソルを置いてをクリックします **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * 既存オーディエンスの設定のセグメント論理パネルの上部で、をクリックします **[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**.

         * テキストエディターで、英数字のセグメント ID とを使用して、セグメントロジックを手動で作成します。 [ブール構文](audience-segment-logic-syntax.md)を開き、クリップボードにコピーします。

      1. クリック **[!UICONTROL paste in an audience rule to begin building]**&#x200B;をクリックし、既存のセグメントロジックを入力フィールドに貼り付けて、 **[!UICONTROL Apply]**.

         >[!NOTE]
         >
         >オーディエンスに既にセグメントロジックが含まれている場合、新しいセグメントロジックを貼り付けると、既存のロジックが上書きされます。

1. クリック **[!UICONTROL Create]**.

>[!MORELIKETHIS]
>
>* [Audience Management について](audience-about.md)
>* [オーディエンス設定](audience-settings.md)
>* [オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
