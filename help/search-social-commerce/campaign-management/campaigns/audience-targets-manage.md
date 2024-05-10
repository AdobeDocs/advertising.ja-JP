---
title: キャンペーンおよび広告グループのオーディエンスターゲットの管理
description: のオーディエンスターゲットを設定および管理する方法について説明します [!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンと広告グループ。
exl-id: 9a496d15-082d-44e1-a0a3-71356e24b932
feature: Search Campaign Management
source-git-commit: 0a858fb9437439d2755f1a9679b0849c614293b7
workflow-type: tm+mt
source-wordcount: '771'
ht-degree: 0%

---

# のオーディエンスターゲットの管理 [!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンと広告グループ

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] のみ*

[!DNL Google Ads] キャンペーンと広告グループ [!DNL Microsoft® Advertising] 広告グループは、同じ広告ネットワークから特定のオーディエンスをターゲットに設定できます。 広告ネットワークは、オーディエンスがターゲティング可能である必要があるサイズを決定します。

>[!NOTE]
>
>除外は、常に包含/ターゲットを上書きします。

オーディエンスターゲットの設定、オーディエンスターゲットの入札修飾子の編集、オーディエンスターゲットのステータスの変更を行うことができます。

## オーディエンスターゲットを設定

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. データ テーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. 特定のキャンペーンおよび広告グループのオーディエンスターゲットを設定します。

   1. 指定した広告ネットワークに適用できるオーディエンスを選択します。

      オプションで、3 文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスを検索するには、 **[!UICONTROL Include]** をクリックして選択します。

      [!DNL Google Ads] 顧客一致オーディエンスは、検索キャンペーンとショッピングキャンペーンでのみ使用できます。

   1. ターゲットを指定します。

      1. （任意）キャンペーンをその子広告グループとして展開するには、キャンペーン名をクリックします。

      1. （オプション）名前に含まれているテキスト文字列でキャンペーンリストまたは広告グループリストをフィルタリングするには、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター") を選択し、テキスト文字列を入力フィールドに入力または貼り付けて、 **[!UICONTROL Enter]** キー。

      1. 青いチェックマーク（![を選択](/help/search-social-commerce/assets/include.png "を選択")）が表示されます。

      （ターゲットを自動的に使用する）親キャンペーンと子広告グループの両方にターゲットを設定することはできません。

1. クリック **[!UICONTROL Post]**.

1. （オプション）から次のいずれかの方法で、ターゲットの入札調整を設定します [!UICONTROL Targets] 表示：

   * 内をクリック **[!UICONTROL Bid Adjustment]** 列に追加して、値を入力します。

   * ターゲット行の横にあるチェックボックスをオンにします。 ツールバーで、をクリックします ![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックし、入札修飾子を入力して、 **[!UICONTROL Post]**.

   値には、次のものが含まれます。

   * *0%:* このオーディエンスの広告の入札を調整しないようにします。

   * /[*-90% ～ 900% のその他の値*/]：このオーディエンスの広告の入札を増減させます。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスターゲットの入札調整が 50% の場合、そのオーディエンスの入札は 1.50 USD に増加します。

## オーディエンスターゲットの入札修飾子の編集

市場内オーディエンスを除くすべてのオーディエンスタイプについて、オーディエンスターゲットの入札修飾子とステータスを変更できます。

>[!NOTE]
>
>親キャンペーンが CPC 入札戦略を使用し、オーディエンスターゲットの入札調整値を自動最適化するように設定されたポートフォリオに含まれる場合、検索、ソーシャル、Commerceによって入札修飾子が自動的に最適化されます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 次のいずれかの操作をおこないます。

   * 1 つのターゲットの入札修飾子を編集するには、 **[!UICONTROL Bid Adjustment]** 入札調整を列および編集します。

   * 1 つ以上のターゲットの入札修飾子を編集するには、次の手順を実行します。

      1. 編集する各ターゲットの横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

      1. データ テーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

      1. を編集する **[!UICONTROL Bid Modifier]** および/または **[!UICONTROL Status]** フィールド。

         の場合 [!UICONTROL Bid Modifier] フィールドには、既存の値を指定の値に変更するオプションと、制限を使用して、指定の割合または金額で金額を増減するオプションがあります。

         設定値の場合、値には次の値を含めることができます。

         * *0%:* このオーディエンスの広告の入札を調整しないようにします。

         * /[*-90% ～ 900% のその他の値*/]：このオーディエンスの広告の入札を増減させます。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスターゲットの入札調整が 50% の場合、そのオーディエンスの入札は 1.50 USD に増加します。

         複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。

      1. （任意）クリック **[!UICONTROL Additional Details]** 必要に応じて、プロジェクト名と説明を入力します。

      1. クリック **[!UICONTROL Post]**.

## オーディエンスターゲットのステータスの変更

アクティブなオーディエンスターゲットを一時停止して、そのターゲットへの入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブな検索オーディエンスターゲットまたは一時停止した検索オーディエンスターゲットを削除することもできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. （任意）特定のオーディエンスターゲットを含めるようにリストをフィルタリングします。

1. ステータスを変更する各オーディエンスターゲットの横にあるチェックボックスを選択します。

   複数の行を選択する際のヒントについては、「」を参照してください[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).」と入力します。

1. ツールバーの「ステータス」ボタンをクリックします。

   * 行をアクティブにするには、をクリックします ![Activate](/help/search-social-commerce/assets/activate.png "Activate").

   * 行を一時停止するには、をクリックします。 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、をクリックします ![その他のアクション](/help/search-social-commerce/assets/more.png "その他のアクション") を選択して、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [キャンペーンおよび広告グループのオーディエンス除外の管理](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
