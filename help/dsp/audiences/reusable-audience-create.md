---
title: 再利用可能なオーディエンスの作成
description: オーディエンスセグメントやその他の保存されたオーディエンスで構成される再利用可能なオーディエンスを作成する方法を説明します。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 3e2164230726fe96d4e43ebba26e84640bd806f1
workflow-type: tm+mt
source-wordcount: 560
ht-degree: 0%

---

# 再利用可能なオーディエンスの作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

再利用可能なオーディエンスを保存および管理できます。このオーディエンスは、オーディエンスセグメントのグループであり、その他の保存されたオーディエンスも含みます。このオーディエンスは、複数のプレースメントのターゲットまたは除外として使用できます。<!-- Create audiences manually or use the AI-assisted audience agent to generate new reusable audiences using all first-party and third-party segments that are available to you, according to your stated requirements. -->

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>（DSPがハッシュ化されたメール IDをLiveRamp RampID セグメントに変換する広告主）アクティブなプレースメント、スケジュール済みプレースメント、または一時停止されたプレースメントにアタッチされていないファーストパーティのRampID セグメントは一時停止されます。 セグメントは、「自動一時停止」としてセグメントリストに表示されます。


<!-- ## Manually create a reusable audience -->

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

1. 一意の&#x200B;**[!UICONTROL Audience Name]**&#x200B;を入力してください。

1. （オプション）オプションの選択を&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;に解除します。

   オーディエンスを共有すると、そのオーディエンスは、アカウント内のすべての広告主に対してターゲットまたは除外として使用できるようになります。 ただし、オーディエンス内の個々のセグメントは、セグメントを共有するユーザーのみが使用できます。 例えば、Adobe Analytics セグメントを含むオーディエンスを、同じ[!DNL Analytics] アカウントにマッピングされていない広告主と共有する場合、そのセグメントはその広告主のそのオーディエンスでプレビューされません。 その広告主が利用できるセグメントのみが、オーディエンスでプレビューされます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. オーディエンスの構築：

   >[!NOTE]
   >
   >オーディエンスを作成すると、右側のパネルに詳細な[&#x200B; オーディエンスサイズデータ &#x200B;](audience-about.md)が更新されます

   * [[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]、および[!UICONTROL Saved Audiences] タブ &#x200B;](audience-settings.md)で使用可能なセグメントを使用して、セグメントロジックを手動で作成するには、次の操作を行います。

      * （オプション）セグメント名、説明、またはパスを検索します。

        検索結果には、使用した用語にもとづいたセグメントが表示されます。 複数の用語を入力すると、1つのセグメントに対するすべての用語が見つかる必要があります。

      * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

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

         * テキストエディターで、英数字のセグメント IDと[&#x200B; ブール構文](audience-segment-logic-syntax.md)を使用してセグメントロジックを手動で作成し、クリップボードにコピーします。

      1. **[!UICONTROL paste in an audience rule to begin building]**&#x200B;をクリックし、既存のセグメントロジックを入力フィールドに貼り付け、**[!UICONTROL Apply]**&#x200B;をクリックします。

         >[!NOTE]
         >
         >オーディエンスにセグメントロジックが既に含まれている場合、新しいセグメントロジックにペーストすると、既存のロジックが上書きされます。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンス管理について](audience-about.md)
>* [&#x200B; オーディエンス設定](audience-settings.md)
>* [&#x200B; オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
>* [&#x200B; カスタムセグメントを作成して実装](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
