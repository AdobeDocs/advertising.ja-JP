---
title: 否定的なキーワードを作成
description: 検索キャンペーンと広告グループに対して否定的なキーワードを作成する方法を説明します。
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/NjLsCcI2-1kWIAfZOv4-IJytuPKUfQWO0OG7ptEDe9w
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 272
ht-degree: 0%

---

# 否定的なキーワードを作成

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]および既存の[!DNL Baidu] アカウントのみ*

検索やディスプレイ/ネイティブネットワークをターゲットとする検索広告グループまたはキャンペーンに対して、ネガティブキーワードを作成できます。 ネガティブキーワードは広告をトリガーにしない。

>[!NOTE]
>また、[広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)および[ キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)で、否定的なキーワードを作成および編集することもできます。

>[!TIP]
>一度に多くの否定的なキーワードを作成するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックし、**[!UICONTROL Campaign]**&#x200B;をクリックしてキャンペーンレベルのネガティブキーワードを作成するか、**[!UICONTROL Ad Group]**&#x200B;をクリックして広告グループレベルのネガティブキーワードを作成します。

1. 広告ネットワーク、アカウント、キャンペーン、および（関連する場合）広告グループを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. 否定的なキーワードを入力します。 マイナス記号（`-`）なしで次の構文を使用します。

   * 負の部分一致：`keyword` （[!DNL Microsoft Advertising]ではサポートされていません）

   * 否定的な語句の一致：`"keyword"`

   * 負の完全一致：`[keyword]`

   複数の値をコンマで区切るか、別々の行に入力します。 1回の操作で最大2000個のネガティブキーワードを入力またはペーストできます。 次の要件と制限も参照してください。

   * 最大文字長：[!DNL Baidu]: 30 シングルバイトまたは15 ダブルバイト、[!DNL Microsoft Advertising]: 100 シングルバイトまたは50 ダブルバイト、[!DNL Google Ads]および[!DNL Yahoo! Japan Ads]: 80 シングルバイトまたは40 ダブルバイト。

   * [!DNL Baidu]では、広告グループごとにキーワードごとに1つの一致タイプのみが許可されます。 例えば、広告グループ 1に`"keyword"`と`[keyword]`の両方を含めることはできません。

   * [!DNL Google Ads]：各キーワードは10文字以下で構成でき、文字、数字、および次の特殊文字のみを含めることができます：スペース `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]：各キーワードには、ストップワードを除く最大7つの単語を指定できます。 各[!DNL Yandex ad group]には、最大200個のキーワードを含めることができます。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [ キーワードについて](keyword-about.md)
>* [入札可能なキーワードの管理](keyword-manage.md)
>* [ キーワードと否定的なキーワードのステータスを変更](keyword-status-edit.md)
