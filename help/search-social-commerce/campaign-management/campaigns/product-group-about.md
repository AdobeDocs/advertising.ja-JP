---
title: ショッピング製品グループについて
description: 買い物キャンペーンでの買い物かご商品グループについて説明します。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: 7e4d2aa502f26b480a5fd76d68411586c24f68b2
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# ショッピング製品グループについて

*[!DNL Google Ads]および [!DNL Microsoft Advertising] のショッピングキャンペーンのみ*

買い物キャンペーンでは、（キーワードではなく）商品グループによって、買い物かご広告を表示するマーチャントセンターアカウントの商品が決まります。 各製品グループは、単一の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID、カスタムラベルなど）に基づいており、一致するすべての製品に同じ入札を使用します。 各グループの商品に入札を含めたり、除外したりできます。

広告グループレベルで商品グループを設定して、マーチャントセンターアカウントのどの商品が広告グループのショッピング広告に表示されるかを決定します。 広告グループに広告エンティティが含まれていない場合でも、広告ネットワークには製品の広告が表示されます。

同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークでは最初にキャンペーンの優先度を使用して、広告オークションに適格なキャンペーン（および関連入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

[!DNL Google] のショッピングキャンペーンおよび広告について詳しくは、「[ ショッピングキャンペーンの実装  [!DNL Google Ads] ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)」および [Google広告のドキュメント ](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1) を参照してください。 [!DNL Microsoft] 買い物キャンペーンについて詳しくは、「[ 買い物キャンペーンの実装  [!DNL Microsoft Advertising]  ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)」および [[!DNL Microsoft Advertising]  ドキュメント ](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500) を参照してください。

>[!NOTE]
>
>スマートショッピングキャンペーンに代わる performance max キャンペーンの [!DNL Google Ads] リストグループはサポートされていません。 リストグループのデータを管理および表示するには、[!DNL Google Ads] エディターを使用します。

## 製品グループ階層

広告グループの特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」と呼ばれる包括的な製品グループを作成する必要があります。 この親製品グループから、製品のサブセットに対して子製品グループを作成し、子製品グループから孫を作成できます。 広告グループの最初の子製品グループを作成すると、デフォルトの広告グループ入札を使用して、「[!UICONTROL Everything Else]」という別の製品グループが自動的に作成されます。 製品グループを追加すると、「[!UICONTROL Everything Else]」グループは、別の製品グループに含まれないすべての製品を構成するように調整されます。

広告グループ内に、最大 7 つのレベルの製品グループ（「[!UICONTROL All Products]」を含まない）を作成して、各レベルで同じ属性をターゲットにする 1 つ以上の製品グループを使用して、入札に含めたり入札から除外したりできます（例えば、ある製品グループには [!UICONTROL Brand]=Acme、同じレベルの別の製品グループには [!UICONTROL Brand]=AcmePlus）。 親製品グループはサブディビジョンと呼ばれ、サブディビジョンの最下位レベルはユニットと呼ばれます。 入札とトラッキングテンプレートを設定するか、または入札を完全に除外するかを単位レベルで指定できます。 広告グループのアクティブな製品グループのセット全体が階層的に適用され、適格な製品が決定されます。 例えば、[!UICONTROL All Products] を [!UICONTROL Brand]=AcmeBasic および [!UICONTROL Brand]=AcmePlus に再分割し、さらに各製品グループを [!UICONTROL Condition]=New に再分割して入札を設定した場合、AcmeBasic および AcmePlus ブランドを持つ新規製品のみが広告または広告から除外される可能性があります。

![ 製品グループセットの例 ](/help/search-social-commerce/assets/product-group-list.png " 製品グループセットの例 ")

![ 製品グループ階層 ](/help/search-social-commerce/assets/product-group-tree.png " 例 – 製品グループ階層 ")

## [!UICONTROL Product Groups] ビュー

[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]/[!UICONTROL Product Groups] 表示で、製品グループを作成および編集したり、製品グループとその子製品グループを削除したりできます。

## ショッピング商品グループのトラッキングデータおよびパフォーマンスデータ

（「[!UICONTROL EF Redirect]」トラッキングオプションを使用するアカウント/キャンペーン）検索、ソーシャル、Commerceで商品グループのコンバージョンをトラッキングできるようにするには、[ トラッキング URL ツールを使用して商品グループのトラッキング URL を生成 ](/help/search-social-commerce/tools/click-tracking-url-generate.md) し、次のいずれかの操作を行います。

* （[!DNL Google Ads] の場合は必須、[!DNL Microsoft Advertising] の場合はベストプラクティス）アカウント、キャンペーンまたは製品グループ設定の「[!DNL Tracking Template]」フィールドにトラッキング URL を追加します。 メンテナンスを容易にするには、可能な限り最高のレベルで追加します。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。

  >[!CAUTION]
  >
  >（[!DNL Microsoft Advertising]）このオプションは、商品フィード内のカスタム列に検索、ソーシャル、Commerceのトラッキング URL を含めない場合にのみ使用します。 両方を実行すると、URL に 2 つのリダイレクトが含まれ、リンクが壊れます。

* （[!DNL Microsoft Advertising] のみ）トラッキング URL を [!DNL Microsoft Merchant Center] アカウント内の製品データに追加します。 これを行うには、トラッキング URL を、必要に応じて `link` または `mobile_link` フィールドの値と共に、製品フィード内の [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) というカスタム列に含めます。 この方法で生成される URL には、検索、ソーシャル、Commerce内のアカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

製品グループに関するデータは [[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md) で表示できます。

>[!MORELIKETHIS]
>
>* [ ショッピング商品グループの管理 ](product-group-manage.md)
>* [[!DNL Google Ads]  製品グループ設定 ](product-group-settings-google.md)
>* [ 買い物キャンペ  [!DNL Google Ads]  ンの実装 ](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising]  製品グループ設定 ](product-group-settings-microsoft.md)
>* [ 買い物キャンペ  [!DNL Microsoft Advertising]  ンの実装 ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
