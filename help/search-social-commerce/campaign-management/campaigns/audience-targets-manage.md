---
title: キャンペーンおよび広告グループのオーディエンスターゲットの管理
description: のオーディエンスターゲットを設定および管理する方法について説明します [!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンと広告グループの両方に割り当てられます。
exl-id: 0016a69c-7642-4060-8125-947ffef6fb03
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '761'
ht-degree: 0%

---

# お客様のオーディエンスターゲットを管理 [!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンと広告グループ

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] のみ*

[!DNL Google Ads] キャンペーンと広告グループ [!DNL Microsoft® Advertising] 広告グループは、同じ広告ネットワークからの特定のオーディエンスをターゲットにすることができます。 広告ネットワークは、オーディエンスがターゲティング可能である必要があるサイズを決定します。

>[!NOTE]
>
>除外は、常に含める/ターゲットを上書きします。

オーディエンスターゲットの設定、オーディエンスターゲットの入札修飾子の編集、オーディエンスターゲットのステータスの変更をおこなうことができます。

## オーディエンスターゲットの設定

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. 特定のキャンペーンおよび広告グループのオーディエンスターゲットを設定します。

   1. 指定した広告ネットワークに適したオーディエンスを選択します。

      オプションで、3 文字以上の特定のテキスト文字列を含むオーディエンスを検索できます。 一致するオーディエンスの場合、 **[!UICONTROL Include]** をクリックして選択します。

      [!DNL Google Ads] 顧客一致オーディエンスは、検索キャンペーンと買い物キャンペーンでのみ使用できます。

   1. ターゲットを指定します。

      1. （オプション）キャンペーンの子広告グループを展開するには、キャンペーン名をクリックします。

      1. （オプション）名前に含まれるテキスト文字列でキャンペーンリストまたは広告グループリストをフィルタリングするには、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター") をクリックし、テキスト文字列を入力フィールドに入力または貼り付けて、 **[!UICONTROL Enter]** キー。

      1. 指定した広告ネットワークの各キャンペーンおよび広告グループのターゲットを指定するには、その横にある空の円をクリックして、青いチェックマーク (![選択](/help/search-social-commerce/assets/include.png "選択")) が表示されます。

      親キャンペーンと子広告グループ（ターゲットを自動的に使用）の両方にターゲットを設定することはできません。

1. クリック **[!UICONTROL Post]**.

1. （オプション）次のいずれかの方法で、ターゲットの入札調整を [!UICONTROL Targets] 表示：

   * をクリックします。 **[!UICONTROL Bid Adjustment]** 」列に値を入力します。

   * ターゲット行の横にあるチェックボックスをオンにします。 ツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集")、入札修飾子を入力して、 **[!UICONTROL Post]**.

   次の値が含まれます。

   * *0%:* このオーディエンスの広告の入札を調整しない。

   * /[*その他の値は —90% ～ 900%です*/]：このオーディエンスの広告の入札額を増減させる場合。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスのターゲットの入札調整が 50%の場合、そのオーディエンスの入札額は 1.50 USD に増加します。

## オーディエンスターゲットの入札修飾子を編集

市場内オーディエンスを除くすべてのオーディエンスタイプに対して、オーディエンスターゲットの入札修飾子とステータスを変更できます。

>[!NOTE]
>
>検索、ソーシャル、コマースは、親キャンペーンが CPC 入札戦略を使用し、オーディエンスターゲットの入札調整値を自動最適化するように設定されたポートフォリオにある場合、入札修飾子を自動的に最適化します。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. 次のいずれかの操作を行います。

   * 1 つのターゲットの入札修飾子を編集するには、 **[!UICONTROL Bid Adjustment]** 列を編集し、入札の調整を編集します。

   * 1 つ以上のターゲットの入札修飾子を編集するには、次の手順を実行します。

      1. 編集する各ターゲットの横にあるチェックボックスを選択します。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

      1. を編集します。 **[!UICONTROL Bid Modifier]** および/または **[!UICONTROL Status]** フィールド。

         の [!UICONTROL Bid Modifier] フィールドに、既存の値を指定した値に変更するか、指定した割合または金額で金額を上限に従って増減するかを選択できます。

         設定値の場合、値には次の値を含めることができます。

         * *0%:* このオーディエンスの広告の入札を調整しない。

         * /[*その他の値は —90% ～ 900%です*/]：このオーディエンスの広告の入札額を増減させる場合。 例えば、キーワードレベルの入札が 1 USD で、特定のオーディエンスのターゲットの入札調整が 50%の場合、そのオーディエンスの入札額は 1.50 USD に増加します。

         複数のターゲットの場合、変更は選択したすべてのターゲットに適用されます。

      1. （オプション）「 **[!UICONTROL Additional Details]** 必要に応じて、プロジェクト名と説明を入力します。

      1. クリック **[!UICONTROL Post]**.

## オーディエンスターゲットのステータスの変更

アクティブなオーディエンスターゲットを一時停止して、そのターゲットに対する入札を無効にできます。 ステータスを「アクティブ」に戻すと、後で入札を再開できます。

また、アクティブな検索オーディエンスターゲットや一時停止した検索オーディエンスターゲットを削除することもできます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Audiences] >[!UICONTROL Targets]**.

1. （オプション）特定のオーディエンスターゲットを含めるようリストをフィルタリングします。

1. ステータスを変更する各オーディエンスターゲットの横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. ツールバーで、ステータスボタンをクリックします。

   * 行をアクティブにするには、 ![有効化](/help/search-social-commerce/assets/activate.png "有効化").

   * 行を一時停止するには、 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、 ![その他のアクション](/help/search-social-commerce/assets/more.png "その他のアクション") を選択し、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [オーディエンスについて](audience-about.md)
>* [キャンペーンおよび広告グループのオーディエンスの除外の管理](/help/search-social-commerce/campaign-management/campaigns/audience-exclusions-manage.md)
