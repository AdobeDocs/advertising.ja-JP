---
title: ショッピング商品グループについて
description: ショッピング施策のショッピング商品グループについて説明します。
exl-id: ae270935-1464-4393-8b8c-745fee077522
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/P3QrbE-JI1XMVzAqA4Pb8jO1t9bRNN-x1q0ehpBvaPw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 721
ht-degree: 0%

---

# ショッピング商品グループについて

*[!DNL Google Ads]および[!DNL Microsoft Advertising]個のショッピング キャンペーンのみ*

ショッピング施策では、キーワードではなく商品グループが、ショッピング広告が表示されるマーチャントセンターのアカウント内の商品を決定します。 各製品グループは、単一の製品属性（カテゴリ、製品タイプ、ブランド、条件、製品ID、カスタムラベルなど）に基づいており、一致するすべての製品に同じ入札を使用します。 各グループの商品に入札を含めることも、除外することもできます。

広告グループレベルで商品グループを設定し、マーチャントセンターのアカウントのどの商品が広告グループのショッピング広告に表示されるかを決定します。 広告グループに広告エンティティが含まれていない場合でも、広告ネットワークには製品の広告が表示されます。

同じ製品が複数のキャンペーンに含まれている場合、広告ネットワークはまずキャンペーンの優先順位を使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを決定します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。

[!DNL Google]個のショッピング キャンペーンと広告について詳しくは、「[実装 [!DNL Google Ads]  ショッピング キャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)」および[Google広告のドキュメント &#x200B;](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&rd=1)を参照してください。 [!DNL Microsoft]個のショッピング キャンペーンについて詳しくは、「[実装 [!DNL Microsoft Advertising]  ショッピング キャンペーン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)」および[[!DNL Microsoft Advertising]  ドキュメント &#x200B;](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500)を参照してください。

>[!NOTE]
>
>スマートショッピングキャンペーンに代わるperformance max キャンペーンの[!DNL Google Ads] リストグループでは、サポートを利用できません。 リスト グループのデータを管理および表示するには、[!DNL Google Ads] エディターを使用します。

## 製品グループの階層

広告グループに特定の属性を持つ製品グループを作成する前に、まず「[!UICONTROL All Products]」という包括的な製品グループを作成する必要があります。 この親製品グループから、製品のサブセットの子製品グループを作成したり、子製品グループから孫を作成したりできます。 広告グループの最初の子製品グループを作成すると、デフォルトの広告グループ入札を使用して、「[!UICONTROL Everything Else]」という別の製品グループが自動的に作成されます。 製品グループを追加すると、「[!UICONTROL Everything Else]」グループが調整され、別の製品グループに含まれないすべての製品を構成するようになります。

広告グループ内で、入札を含めたり除外したりするために最大7つのレベルの製品グループ（「[!UICONTROL All Products]」を含まない）を作成できます。各レベルで同じ属性をターゲットとする1つ以上の製品グループを作成できます（例：[!UICONTROL Brand]=1つの製品グループにはAcme、同じレベルで別の製品グループには[!UICONTROL Brand]=AcmePlus）。 親製品グループはサブディビジョンと呼ばれ、サブディビジョンの最下位レベルはユニットと呼ばれます。 単体レベルで、入札額やトラッキングテンプレートを設定したり、入札を完全に除外したりできます。 広告グループのアクティブな製品グループ全体が階層的に適用され、対象製品が決定されます。 例えば、[!UICONTROL All Products]を[!UICONTROL Brand]=AcmeBasicと[!UICONTROL Brand]=AcmePlusに分割し、それぞれの製品グループを[!UICONTROL Condition]=Newとset Bidに分割すると、AcmeBasic ブランドとAcmePlus ブランドを持つ新しい製品のみが広告または広告から除外されます。

![製品グループセットの例](/help/search-social-commerce/assets/product-group-list.png "製品グループセットの例")

![製品グループ階層の例](/help/search-social-commerce/assets/product-group-tree.png "製品グループ階層の例")

## [!UICONTROL Product Groups] ビュー

製品グループを作成および編集し、製品グループとその子製品グループを[!UICONTROL Search, Social, & Commerce] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] ビューで削除できます。

## ショッピング商品グループのトラッキングとパフォーマンスデータ

（「[!UICONTROL EF Redirect]」トラッキングオプションを使用したアカウント/キャンペーン） Search、Social、およびCommerceで商品グループのコンバージョンをトラッキングできるようにするには、[&#x200B; トラッキング URL ツールを使用して商品グループのトラッキング URLを生成し](/help/search-social-commerce/tools/click-tracking-url-generate.md)、次のいずれかの操作を行います。

* （必須：[!DNL Google Ads]、ベストプラクティス：[!DNL Microsoft Advertising]） アカウント、キャンペーン、または製品グループの設定の[!DNL Tracking Template] フィールドにトラッキング URLを追加します。 メンテナンスを容易にするために、できるだけ高いレベルで追加してください。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。

  >[!CAUTION]
  >
  >（[!DNL Microsoft Advertising]）このオプションは、商品フィード内のカスタム列に検索、ソーシャル、Commerce トラッキング URLを含まない場合にのみ使用します。 両方を行うと、URLには2つのリダイレクトが含まれ、リンクが壊れる原因になります。

* （[!DNL Microsoft Advertising]のみ） [!DNL Microsoft Merchant Center] アカウント内の製品データにトラッキング URLを追加します。 これを行うには、トラッキング URLを、必要に応じて`link`または`mobile_link` フィールドの値と共に、製品フィード内の[`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0)というカスタム列に含めます。 この方法で生成されたURLには、Search, Social, &amp; Commerce内のアカウントまたはキャンペーン設定で指定されたトラッキングパラメーターが含まれていません。

製品グループに関するデータは、[の[!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md)で表示できます。

>[!MORELIKETHIS]
>
>* [&#x200B; ショッピング商品グループの管理](product-group-manage.md)
>* [[!DNL Google Ads] 製品グループ設定](product-group-settings-google.md)
>* [&#x200B; ショッピング キャンペーン  [!DNL Google Ads] を実装](/help/search-social-commerce/campaign-management/special-workflows/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 製品グループ設定](product-group-settings-microsoft.md)
>* [&#x200B; ショッピング キャンペーン  [!DNL Microsoft Advertising] を実装](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)
