---
title: 買い物製品グループについて
description: ショッピングキャンペーンでのショッピング製品グループの詳細。
exl-id: c91e6fb5-3be1-4d21-b508-09f974058fc7
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '739'
ht-degree: 0%

---

# 買い物製品グループについて

*[!DNL Google Ads]および [!DNL Microsoft Advertising] 買い物キャンペーンのみ*

ショッピングキャンペーンでは、商品グループ（キーワードではなく）が、ショッピング広告が表示されるマーチャントセンターアカウント内の商品を決定します。 各製品グループは、1 つの製品属性（カテゴリ、製品タイプ、ブランド、条件、製品 ID、カスタムラベルなど）に基づき、一致するすべての製品に対して同じ入札を使用します。 各グループの製品の入札を含めたり除外したりできます。

広告グループレベルで製品グループを設定して、広告グループのショッピング広告に表示されるマーチャントセンターアカウントの製品を決定します。 広告グループに広告エンティティが含まれていなくても、広告ネットワークには製品の広告が表示されます。

同じ製品が複数のキャンペーンに含まれる場合、広告ネットワークはまずキャンペーンの優先順位を使用して、広告オークションに適格なキャンペーン（および関連する入札）を決定します。 すべてのキャンペーンが同じ優先順位の場合、最も入札額の高いキャンペーンが適格になります。

詳しくは、 [!DNL Google] 買い物キャンペーンと広告：[実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)「と [Google Ads ドキュメント](https://support.google.com/google-ads/answer/3455481?visit_id=638205553638977410-2592024034&amp;rd=1). Microsoftのショッピングキャンペーンについて詳しくは、[実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)「と [Microsoft Advertising ドキュメント](https://help.bingads.microsoft.com/#apex/3/en/50903/1-500).

>[!NOTE]
>
>ではサポートを利用できません [!DNL Google Ads] スマートショッピングキャンペーンに代わる、パフォーマンス最大キャンペーンにグループをリストする。 リストグループのデータを管理および表示するには、 [!DNL Google Ads] 編集者です。

## 製品グループの階層

広告グループの特定の属性を持つ製品グループを作成する前に、「[!UICONTROL All Products].&quot; この親製品グループから、製品のサブセット用の子製品グループを作成し、子製品グループから孫を作成できます。 広告グループの最初の子製品グループを作成したら、「[!UICONTROL Everything Else]「 」は、デフォルトの広告グループ入札を使用して自動的に作成されます。 製品グループを追加すると、「[!UICONTROL Everything Else]「グループは、別の製品グループに属さないすべての製品を構成するように、適宜調整されます。

広告グループ内では、最大 7 レベルの製品グループを作成できます (「[!UICONTROL All Products]&quot;) 各レベルで 1 つ以上の製品グループが同じ属性 ( 例： [!UICONTROL Brand]=1 つの製品グループの Acme および [!UICONTROL Brand]=AcmePlus（同じレベルの別のの）。 親プロダクトグループはサブディビジョンと呼ばれ、最も低いレベルのサブディビジョンは単位と呼ばれます。 単位レベルで、入札およびトラッキングテンプレートを設定したり、入札を完全に除外したりできます。 広告グループのアクティブな製品グループのセット全体が階層的に適用され、対象となる製品が決定されます。 例えば、 [!UICONTROL All Products] into [!UICONTROL Brand]=AcmeBasic および [!UICONTROL Brand]=AcmePlus の場合は、各製品グループをさらに細分化して、 [!UICONTROL Condition]=新規入札と入札の設定では、AcmeBasic と AcmePlus のブランドを持つ新しい製品のみ広告を作成したり、広告から除外したりできます。

![製品グループセットの例](/help/search-social-commerce/assets/product-group-list.png "製品グループセットの例")

![製品グループ階層の例](/help/search-social-commerce/assets/product-group-tree.png "製品グループ階層の例")

## The [!UICONTROL Product Groups] 表示

で、製品グループを作成および編集したり、製品グループとその子製品グループを削除したりできます。 [!UICONTROL Search] > [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 表示。

## 買い物製品グループのトラッキングとパフォーマンスデータ

(「[!UICONTROL EF Redirect]&quot;追跡オプション ) 検索、ソーシャル、コマースで製品グループのコンバージョンを追跡できるようにするには、 [トラッキング URL ツールを使用して製品グループのトラッキング URL を生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md)をクリックし、次のいずれかの操作を行います。

* ( 必須 [!DNL Google Ads]；ベストプラクティス [!DNL Microsoft Advertising]) トラッキング URL を [!DNL Tracking Template] フィールド（アカウント、キャンペーンまたは製品グループ設定）に含まれています。 メンテナンスを容易にするには、できる限り高いレベルで追加します。 アカウントまたはキャンペーンに指定された追加パラメーターは含まれません。

  >[!CAUTION]
  >
  >([!DNL Microsoft Advertising]) このオプションは、製品フィード内のカスタム列に検索、ソーシャル、コマースの追跡 URL を含めない場合にのみ使用します。 両方を実行した場合、URL には 2 つのリダイレクトが含まれ、リンクが壊れます。

* ([!DNL Microsoft Advertising] （オンライン）トラッキング URL を [!DNL Microsoft Merchant Center] アカウント。 これをおこなうには、トラッキング URL を `link` または `mobile_link` 必要に応じて、という名前のカスタム列の [`bingads_redirect`](https://help.ads.microsoft.com/#apex/3/en/51084/0) 製品フィード内で使用できます。 このメソッドを使用して生成された URL には、検索、ソーシャル、コマース内のアカウント設定やキャンペーン設定で指定されたトラッキングパラメーターは含まれません。

製品グループに関するデータは、 [の [!UICONTROL Product Group Report]](/help/search-social-commerce/reports/management/basic-advanced/product-group-report.md).

>[!MORELIKETHIS]
>
>* [買い物製品グループの管理](product-group-manage.md)
>* [[!DNL Google Ads] 製品グループの設定](product-group-settings-google.md)
>* [実装方法 [!DNL Google Ads] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/google-shopping-campaigns.md)
>* [[!DNL Microsoft Advertising] 製品グループの設定](product-group-settings-microsoft.md)
>* [実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md)
