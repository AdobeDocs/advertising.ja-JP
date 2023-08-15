---
title: カスタム目標の作成
description: カスタム目標の作成
feature: DSP Optimization
exl-id: 81b0acfa-085d-495b-9516-576b952b1307
source-git-commit: 1dbe8da7122b38dd11a242c453d71a832b31eee8
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 0%

---

# カスタム目標の作成

カスタム目標は、 *目標* 範囲 [!DNL Advertising Search, Social, & Commerce].

カスタム目標を作成するには、DSPアカウントを [!DNL Search, Social, & Commerce] 内から同じAdobe Experience Cloud組織 ID を持つアカウント [!DNL Search, Social, & Commerce] クライアント設定。 DSPアカウントが [!DNL Search, Social, & Commerce] アカウントに問い合わせる場合は、Adobeアカウントチームにお問い合わせください。

>[!TIP]
>
>詳しくは、 [カスタム目標の作成に関するベストプラクティス](custom-goal-best-practices.md) カスタム目標の設定方法に関するヒントを参照してください。

1. にログインします。 [!DNL Advertising Search, Social, & Commerce] at （北米のユーザー） [`https://enterprise-na.efrontier.com`](https://enterprise-na.efrontier.com) または（他のすべてのユーザー） [`https://enterprise-intl.efrontier.com`](https://enterprise-intl.efrontier.com).
1. 目標に含める指標が追跡され、製品で利用できること、および表示名が含まれていることを確認します。
   1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.
   1. 指標を見つけ、 **[!UICONTROL Show in UI and Reports]** は指標に対して有効になっています。
   1. 指標の値が **[!UICONTROL Display Name]** 列をクリックし、セル内をクリックして表示名を入力し、 **[!UICONTROL Apply].**
1. カスタム目標を *目的*:
   1. メインメニューで、 **[!UICONTROL Search]** > **[!UICONTROL Optimization]>[!UICONTROL Objectives]**.
   1. ツールバーで、 **[!UICONTROL Create objective].**
   1. 目的の設定を入力します。
      1. Adobe Analytics の **[!UICONTROL Change Objective Name]** 「 」フィールドに、目的の名前を入力します。

         目標名は、 [!UICONTROL Custom Goals] リストをDSPパッケージ設定に表示します。

      1. プロパティを目的に関連付けます。

         >[!NOTE]
         >
         > デフォルトでは、広告主に対してトラッキングされるすべてのコンバージョン指標が [!UICONTROL Available Properties] リスト。

         * コンバージョン指標とその重みを含む CSV ファイルを読み込むには、 **[!UICONTROL Import]** をクリックし、インポートするファイルを探します。

           読み込んだコンバージョン指標は、既に広告主に存在している必要があります。名前では大文字と小文字が区別されません。

           インポートされたコンバージョン指標は、指定された既存のプロパティを置き換えます。

         * 最初のコンバージョン指標をデフォルトの重み付け (1) で手動で指定するには、広告主に対して追跡されるすべてのコンバージョン指標のリストから選択します。

         * デフォルトの重み付け (1) を指定して別のコンバージョン指標を手動で追加するには、 **[!UICONTROL +]** .

           >[!TIP]
           >
           > リスト内の指標を検索するには、指標名の任意の場所から文字列を入力します。

         * 複数のコンバージョン指標を手動で追加するには、 **[!UICONTROL Add Multiple Properties].** 追加する各コンバージョン指標に対して、 [!UICONTROL Available Properties] 列をクリックし、 [!UICONTROL Added Properties] 列。 指標の追加が完了したら、 **[!UICONTROL Add]**.

           >[!TIP]
           >
           >* リスト内の指標を検索するには、入力フィールドに指標名内の任意の場所から文字列を入力します。
           >* リストをフィルタリングしてレポートから除外する指標を除外するには、「 」オプションを選択します **[!UICONTROL Hide properties excluded from reports].**

         * （目標に複数のコンバージョン指標が含まれる場合）目標内の他の指標に対する指標の重みを変更するには、 **[!UICONTROL Weight]** フィールドに値を入力します。

      1. 設定の下部で、 **[!UICONTROL Save]**.

目標を作成したら、最適化目標が「 」で終わる場合に、カスタム目標としてDSPパッケージに割り当てることができます。[!UICONTROL - Custom Goal]&quot; (&quot;[!UICONTROL Highest ROAS - Custom Goal]」) をクリックします。

>[!TIP]
>
>パフォーマンスを最適化するために、カスタム目標（目標）の組み合わせ指標では、1 日に少なくとも 10 のコンバージョンを合計する必要があります。 適用されない場合は、ベストプラクティスとして、製品ページやアプリケーションの開始など、サポートされるコンバージョン指標を目的に追加することが推奨されます。 詳しくは、 [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md) 」を参照してください。

>[!MORELIKETHIS]
>
>* [カスタム目標について](custom-goal-about.md)
>* [カスタム目標を構築するためのベストプラクティス](custom-goal-best-practices.md)
>* [最適化目標とその使用方法](optimization-goals.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
> * [キャンペーンの最適化方法](optimization-how-dsp-optimizes-campaigns.md)
