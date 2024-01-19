---
title: 除外キーワードの作成
description: 検索キャンペーンおよび広告グループの除外キーワードを作成する方法を説明します。
exl-id: afe786bf-eda8-4590-b471-3fb696c420de
feature: Search Campaign Management
source-git-commit: c2a1ce841a9dc99c57239f817dbd2065b91cdfb9
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 0%

---

# 除外キーワードの作成

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads]、および既存 [!DNL Baidu] アカウントのみ*

検索またはディスプレイ/ネイティブネットワークをターゲットにした検索広告グループまたはキャンペーンに対して、除外キーワードを作成できます。 除外キーワードは広告をトリガーしません。

>[!NOTE]
>また、除外キーワードを [広告グループ設定](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) および [キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md).

>[!TIP]
>一度に多数の除外キーワードを作成するには、 [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Keywords] >[!UICONTROL Negatives]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成")をクリックし、 **[!UICONTROL Campaign]** キャンペーンレベルの除外キーワードまたは **[!UICONTROL Ad Group]** 広告グループレベルの除外キーワードを作成する。

1. 広告ネットワーク、アカウント、キャンペーン、および（関連する場合）広告グループを選択し、「 **[!UICONTROL Continue]**.

1. 除外キーワードを入力します。 次の構文を、マイナス記号 (`-`):

   * 負の部分一致： `keyword` ( ではサポートされていません。 [!DNL Microsoft® Advertising])

   * 否定的なフレーズ一致： `"keyword"`

   * 負の完全一致： `[keyword]`

   複数の値はコンマで区切るか、別々の行に入力します。 1 回の操作で 2,000 個までの除外キーワードを入力または貼り付けることができます。 次の要件および制限も参照してください。

   * 最大文字数： [!DNL Baidu]:30 シングルバイトまたは 15 ダブルバイト。 [!DNL Microsoft® Advertising]:1 バイトまたは 2 バイトを 50 個指定します。 [!DNL Google Ads] および [!DNL Yahoo! Japan Ads]:80 シングルバイトまたは 40 ダブルバイト。

   * [!DNL Baidu] では、広告グループごとに 1 つのキーワードにつき 1 つの一致タイプのみを使用できます。 例えば、広告グループ 1 に `"keyword"` および `[keyword]`.

   * [!DNL Google Ads]：各キーワードは 10 語以下で構成でき、文字、数字、次の特殊文字のみを含めることができます。スペース `# $ & _ - " [ ] ' + . / :`

   * [!DNL Yandex]：各キーワードは、停止語を除く最大 7 語まで指定できます。 各 [!DNL Yandex ad group] には最大 200 個のキーワードを含めることができます。

1. クリック **[!UICONTROL Post]**.

>[!MORELIKETHIS]
>
>* [キーワードについて](keyword-about.md)
>* [入札可能なキーワードの管理](keyword-manage.md)
>* [キーワードと除外キーワードのステータスの変更](keyword-status-edit.md)
