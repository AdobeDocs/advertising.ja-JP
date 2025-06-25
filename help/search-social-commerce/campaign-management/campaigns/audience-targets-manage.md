---
title: キャンペーンおよび広告グループのオーディエンスターゲットの管理
description: キャンペーンと広告グループのオーディエンスターゲットを設定お  [!DNL Google Ads]  び管理す  [!DNL Microsoft Advertising]  方法について説明します。
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# [!DNL Google Ads] および [!DNL Microsoft Advertising] キャンペーンと広告グループのオーディエンスターゲットを管理します。

*[!DNL Google Ads]と [!DNL Microsoft Advertising] のみ*

キャンペーンと広告グループ、および [!DNL Microsoft Advertising] の広告グループで [!DNL Google Ads]、同じ広告ネットワークから特定のオーディエンスをターゲットに設定できます。 広告ネットワークは、オーディエンスがターゲティング可能である必要があるサイズを決定します。

>[!NOTE]
>
>除外は、常に包含/ターゲットを上書きします。

オーディエンスターゲットの設定、オーディエンスターゲットの入札修飾子の編集、オーディエンスターゲットのステータスの変更を行うことができます。

## オーディエンスターゲットを設定

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワークとアカウント名を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. 特定のキャンペーンおよび広告グループのオーディエンスターゲットを設定します。

   1. 指定した広告ネットワークに適用できるオーディエンスを選択します。

      オプションで、3 文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスがある場合は、「**[!UICONTROL Include]**」をクリックして選択します。

      カスタマーマッチオーディエンス [!DNL Google Ads]、検索キャンペーンとショッピングキャンペーンでのみ使用できます。

   1. ターゲットを指定します。

      1. （任意）キャンペーンをその子広告グループとして展開するには、キャンペーン名をクリックします。

      1. （オプション）名前に含まれているテキスト文字列でキャンペーンリストまたは広告グループリストをフィルタリングするには、![ フィルター ](/help/search-social-commerce/assets/filter.png " フィルター ") をクリックして、テキスト文字列を入力または入力フィールドに貼り付けて、**[!UICONTROL Enter]** キーを押します。

      1. 青いチェックマーク（![ 選択 ](/help/search-social-commerce/assets/include.png " 選択 ")）が表示されるように、隣接する空の円をクリックして、指定した広告ネットワークの各キャンペーンおよび広告グループのターゲットを指定します。

      （ターゲットを自動的に使用する）親キャンペーンと子広告グループの両方にターゲットを設定することはできません。

1. 「**[!UICONTROL Post]**」をクリックします。

1. （オプション） [!UICONTROL Targets] 表示から次のいずれかの方法で、ターゲットの入札調整を設定します。

   * **[!UICONTROL Bid Adjustment]** 列内をクリックし、値を入力します。

   * ターゲット行の横にあるチェックボックスをオンにします。 ツールバーの ![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ") をクリックし、入札修飾子を入力して「**[!UICONTROL Post]**」をクリックします。

   値には、次のものが含まれます。

   * *0%:* このオーディエンスの広告の入札を調整しません。

   * /[*-90% ～ 900% の間のその他の値*/]：このオーディエンスの広告の入札を増減させます。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスターゲットの入札調整が 50% の場合、そのオーディエンスの入札は 1.50 USD に増加します。

## オーディエンスターゲットの入札修飾子の編集

市場内オーディエンスを除くすべてのオーディエンスタイプについて、オーディエンスターゲットの入札修飾子とステータスを変更できます。

>[!NOTE]
>
>親キャンペーンが CPC 入札戦略を使用し、オーディエンスターゲットの入札調整値を自動最適化するように設定されたポートフォリオに含まれる場合、検索、ソーシャル、Commerceによって入札修飾子が自動的に最適化されます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** をクリックします。

1. 次のいずれかの操作をおこないます。

   * 1 つのターゲットの入札モディファイアを編集するには、「**[!UICONTROL Bid Adjustment]**」列をクリックして入札調整を編集します。

   * 1 つ以上のターゲットの入札修飾子を編集するには、次の手順を実行します。

      1. 編集する各ターゲットの横にあるチェックボックスをオンにします。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

      1. 「**[!UICONTROL Bid Modifier]**」フィールドや「**[!UICONTROL Status]**」フィールドを編集します。

         [!UICONTROL Bid Modifier] フィールドには、既存の値を指定の値に変更するオプションと、制限を指定して、指定の割合または金額で金額を増減するオプションがあります。

         設定値の場合、値には次の値を含めることができます。

         * *0%:* このオーディエンスの広告の入札を調整しません。

         * /[*-90% ～ 900% の間のその他の値*/]：このオーディエンスの広告の入札を増減させます。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスターゲットの入札調整が 50% の場合、そのオーディエンスの入札は 1.50 USD に増加します。

         複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。

      1. （任意）「**[!UICONTROL Additional Details]**」をクリックし、オプションでプロジェクト名と説明を入力します。

      1. 「**[!UICONTROL Post]**」をクリックします。

## オーディエンスターゲットのステータスの変更

アクティブなオーディエンスターゲットを一時停止して、そのターゲットへの入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブな検索オーディエンスターゲットまたは一時停止した検索オーディエンスターゲットを削除することもできます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]** をクリックします。

1. （任意）特定のオーディエンスターゲットを含めるようにリストをフィルタリングします。

1. ステータスを変更する各オーディエンスターゲットの横にあるチェックボックスを選択します。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. ツールバーの「ステータス」ボタンをクリックします。

   * 行をアクティブにするには、「![ アクティブ化 ](/help/search-social-commerce/assets/activate.png " アクティブ化 ")」をクリックします。

   * 行を一時停止するには、「![ 一時停止 ](/help/search-social-commerce/assets/pause.png " 一時停止 ")」をクリックします。

   * 行を削除するには、「![ その他のアクション ](/help/search-social-commerce/assets/more.png " その他のアクション ")」をクリックし、**[!UICONTROL Delete]** を選択します。 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ オーディエンスについて ](audience-about.md)
>* [ キャンペーンおよび広告グループのオーディエンス除外の管理 ](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
