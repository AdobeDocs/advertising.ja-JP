---
title: ネガティブキーワードの作成
description: 検索キャンペーンと広告グループにネガティブキーワードを作成する方法を説明します。
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# ネガティブキーワードの作成

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] および既存の [!DNL Baidu] アカウントのみ*

検索またはディスプレイ/ネイティブネットワークをターゲットとする検索広告グループまたはキャンペーンに、ネガティブキーワードを作成できます。 負のキーワードは広告をトリガーしません。

>[!NOTE]
>また、[ 広告グループ設定 ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) および [ キャンペーン設定 ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md) でネガティブキーワードを作成および編集することもできます。

>[!TIP]
>一度に多くのネガティブキーワードを作成するには、[campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックし、[**[!UICONTROL Campaign]**] をクリックしてキャンペーン レベルの負のキーワードを作成するか、[**[!UICONTROL Ad Group]**] をクリックして広告グループ レベルの負のキーワードを作成します。

1. 広告ネットワーク、アカウント、キャンペーン、（該当する場合は）広告グループを選択し、「**[!UICONTROL Continue]**」をクリックします。

1. 負のキーワードを入力します。 マイナス記号（`-`）を使用せずに、次の構文を使用します。

   * 負の部分一致：`keyword` （[!DNL Microsoft Advertising] ではサポートされていません）

   * 負の語句の一致：`"keyword"`

   * 完全一致が負の数：`[keyword]`

   複数の値をコンマで区切るか、別々の行に入力します。 1 回の操作で最大 2000 個の負のキーワードを入力または貼り付けることができます。 次の要件と制限事項も参照してください。

   * 最大文字数：[!DNL Baidu]:30 個の 1 バイトまたは 15 個の 2 バイト。[!DNL Microsoft Advertising]:100 個の 1 バイトまたは 50 個の 2 バイト。[!DNL Google Ads] および [!DNL Yahoo! Japan Ads]:80 個の 1 バイトまたは 40 個の 2 バイト。

   * [!DNL Baidu] では、広告グループごとにキーワードごとに 1 つの一致タイプのみを使用できます。 例えば、広告グループ 1 に `"keyword"` と `[keyword]` の両方を含めることはできません。

   * [!DNL Google Ads]：各キーワードは 10 語以内で構成でき、文字、数字、および次の特殊文字のみを含めることができます。スペース `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]：各キーワードには、ストップワードを除いて最大 7 語を含めることができます。 各 [!DNL Yandex ad group] には、最大 200 個のキーワードを含めることができます。

1. 「**[!UICONTROL Post]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ キーワードについて ](keyword-about.md)
>* [ 入札可能キーワードの管理 ](keyword-manage.md)
>* [ キーワードとネガティブキーワードのステータスの変更 ](keyword-status-edit.md)
