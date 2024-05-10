---
title: ショッピング製品グループについて
description: 買い物キャンペーンでの買い物かご商品グループについて説明します。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 0%

---

# ショッピング製品グループについて

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] ショッピングキャンペーンのみ*

買い物キャンペーンでは、（キーワードではなく）商品グループによって、買い物かご広告を表示するマーチャントセンターアカウントの商品が決まります。 各製品グループは、単一の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID、カスタムラベルなど）に基づいており、一致するすべての製品に同じ入札を使用します。 各グループの商品に入札を含めたり、除外したりできます。

広告グループレベルで商品グループを設定して、マーチャントセンターアカウントのどの商品が広告グループのショッピング広告に表示されるかを決定します。 広告グループに広告エンティティが含まれていない場合でも、広告ネットワークには製品の広告が表示されます。

同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークでは最初にキャンペーンの優先度を使用して、広告オークションに適格なキャンペーン（および関連入札）を決定します。 すべてのキャンペーンの優先度が同じ場合は、入札額が最も高いキャンペーンが実施要件を満たします。

詳しくは、 [!DNL Google] ショッピングキャンペーンおよび広告。「」を参照してください[実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)」と入力し、 [Google Ads ドキュメント](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). 詳しくは、 [!DNL Microsoft®] ショッピングキャンペーン、「」を参照してください[実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)」と入力し、 [[!DNL Microsoft® Advertising] 詳細を見る](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>ではサポートを利用できません [!DNL Google Ads] スマートショッピングキャンペーンに取って代わる performance max キャンペーンのグループを一覧表示します。 リストグループのデータを管理および表示するには、 [!DNL Google Ads] 編集者。

## 製品グループ階層

広告グループに特定の属性を持つ製品グループを作成する前に、まず「」という包括的な製品グループを作成する必要があります[!UICONTROL All Products].」と入力します。 この親製品グループから、製品のサブセットに対して子製品グループを作成し、子製品グループから孫を作成できます。 広告グループの最初の子製品グループを作成したら、別の製品グループは「」になります。[!UICONTROL Everything Else]」は、デフォルトの広告グループ入札を使用して自動的に作成されます。 製品グループをさらに追加すると、「[!UICONTROL Everything Else]「グループは、他の製品グループに属さないすべての製品を構成するように適宜調整されています。

広告グループ内には、最大 7 つのレベルの製品グループ（「[!UICONTROL All Products]&quot;）を選択して、各レベルで同じ属性をターゲットにする 1 つ以上の製品グループの入札を含めるか除外します（例： [!UICONTROL Brand]=1 つの製品グループに対してアクティブで、 [!UICONTROL Brand]=同じレベルの別の関数の場合は AcmePlus）。 親製品グループはサブディビジョンと呼ばれ、サブディビジョンの最下位レベルはユニットと呼ばれます。 入札とトラッキングテンプレートを設定するか、または入札を完全に除外するかを単位レベルで指定できます。 広告グループのアクティブな製品グループのセット全体が階層的に適用され、適格な製品が決定されます。 例えば、を細分化した場合は次のようになります [!UICONTROL All Products] 対象 [!UICONTROL Brand]=AcmeBasic および [!UICONTROL Brand]=AcmePlus を使用すると、それらの各製品グループをさらに [!UICONTROL Condition]=新規およびセット入札を行うと、AcmeBasic および AcmePlus ブランドの新製品のみが広告または広告から除外されます。

![製品グループセットの例](/help/search-social-commerce/assets/product-group-list.png "製品グループセットの例")

![製品グループ階層の例](/help/search-social-commerce/assets/product-group-tree.png "製品グループ階層の例")

## この [!UICONTROL Product Groups] 表示

では、製品グループを作成および編集したり、製品グループとその子製品グループを削除したりできます [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 表示。

## ショッピング商品グループのトラッキングデータおよびパフォーマンスデータ

（「」を持つアカウント/キャンペーン[!UICONTROL EF Redirect]&quot; トラッキングオプション）を使用して、検索、ソーシャル、Commerceで商品グループのコンバージョンをトラッキングできます。 [トラッキング URL ツールを使用した製品グループのトラッキング URL の生成](/help/search-social-commerce/tools/click-tracking-url-generate.md)次に、以下のいずれかの操作を行います。

* （次の場合に必須： [!DNL Google Ads]; ベストプラクティス [!DNL Microsoft® Advertising]） トラッキング URL をに追加します [!DNL Tracking Template] アカウント、キャンペーンまたは製品グループ設定のフィールド。 メンテナンスを容易にするには、可能な限り最高のレベルで追加します。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。

  >[!CAUTION]
  >
  >（[!DNL Microsoft® Advertising]）このオプションは、製品フィード内のカスタム列に検索、ソーシャル、Commerceのトラッキング URL を含めない場合にのみ使用します。 両方を実行すると、URL に 2 つのリダイレクトが含まれ、リンクが壊れます。

* （[!DNL Microsoft® Advertising] のみ）トラッキング URL を内の製品データに追加します [!DNL Microsoft® Merchant Center] アカウント。 これをおこなうには、トラッキング URL を値と共にに含めます。 `link` または `mobile_link` というカスタム列のフィールド（必要に応じて） [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) 製品フィード内。 この方法で生成される URL には、検索、ソーシャル、Commerce内のアカウントまたはキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

製品グループに関するデータは、で表示できます [この [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [ショッピング商品グループの管理](product-group-manage.md)
>* [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)
>* [実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft® Advertising] 製品グループ設定](product-group-settings-microsoft.md)
>* [実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
