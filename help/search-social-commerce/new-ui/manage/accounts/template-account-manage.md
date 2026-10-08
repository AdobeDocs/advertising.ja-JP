---
title: （新しいUI）トラッキング専用の[!DNL Naver] アカウントの管理
description: '[!DNL Naver] アカウントの新しいUIでアカウントの詳細を設定および管理する方法について説明します。'
feature: Search Campaign Management
exl-id: bc4be409-9935-448b-bfba-f93eb30bd5ca
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
source-git-commit: 6d95caf72d11c404d866e8d091e1ffa89814ae73
workflow-type: tm+mt
source-wordcount: '491'
ht-degree: 1%
---
# （新しいUI）トラッキング専用の[!DNL Naver] アカウントの管理

*Beta機能*

以下は、広告ネットワークから直接購入した広告のパフォーマンスを追跡、報告、可視化するために[[!DNL Naver]  アカウント ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)を管理する手順です。 Search, Social, &amp; Commerceでは、データと広告ネットワークの同期が取れず、自動入札も提供されず、あらゆる種類の最適化やシミュレーションも提供されません。

使用可能な機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## 広告ネットワークアカウントの詳細の作成 {#create-account}

アカウントの追跡を有効にするには、アカウントのアクセス資格情報とステータス *が有効*&#x200B;の対応するアカウントレコードを作成する必要があります。

>[!NOTE]
>
>広告ネットワークで実際のアカウントを作成するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL Create Account]**&#x200B;をクリックします。

1. 広告ネットワークの名前をクリックし、**[!UICONTROL Next]**&#x200B;をクリックします。

1. [ アカウント設定](#account-settings-naver)を指定します。

   1. 「**[!UICONTROL Enter Account Details]**」タブで、一般的なアカウント設定を指定します。

   1. （[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、追跡およびレポートのキャンペーンアクティビティに使用するすべての[!DNL Analytics] レポートスイートを選択します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 広告ネットワークアカウントの詳細を編集 {#edit-account}

アカウント名を変更したり、アカウントステータスを変更したり、トラッキングやレポートに使用する[!DNL Analytics] レポートスイートを変更したりするには、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークのweb サイトに移動します。

1. メインメニューで、**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [ アカウント設定](#account-settings-api)を編集します。

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （オプション、[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、[!DNL Analytics] レポートスイートを編集して、キャンペーンアクティビティの追跡とレポートに使用します。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. **[!UICONTROL Save]**&#x200B;をクリックします。

<!--
 What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**.

1. Do either of the following:

   * (From the [!UICONTROL Accounts] view):

     * (To enable the account) Select the check box next to the account name, and then click **[!UICONTROL Activate]** in the bulk actions toolbar.

     * (To disable the account) Select the check box next to the account name, and then click **[!UICONTROL Pause]** in the bulk actions toolbar.

   * (From the account settings):
   
     1. Select the account in either of the following ways:
     
        * Hold the cursor over the account name, click **...**, and then click **[!UICONTROL Edit]**.
        
        * Select the check box next to the account name, and then click **[!UICONTROL Edit]** in the bulk actions toolbar.
        
     1. On the **[!UICONTROL Account Details]** tab, turn off **[!UICONTROL Account enabled]**.

     1. Click **[!UICONTROL Save]**.

-->

## 広告ネットワークアカウント設定 {#account-settings-api}

### [!UICONTROL Account Details] タブ

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:**&#x200B;検索、ソーシャル、およびCommerce内のアカウントに表示される名前。

>[!NOTE]
>
>Search、Social、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobe アカウントチームにマッピングを更新するように依頼します。

**[!UICONTROL Network Account ID]:**&#x200B;広告ネットワークによって割り当てられたアカウント ID。

**[!UICONTROL Currency]:** アカウントに使用される通貨の略語。

**[!UICONTROL Time Zone]:**&#x200B;広告主のタイムゾーン。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** Search, Social, &amp; Commerceは、キャンペーンデータをアカウントと（サポートされている場合）同期し、ポートフォリオ内のキャンペーンの自動入札やキャンペーン予算をプッシュします。

## [!UICONTROL Setup Analytics] タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （統合[[!DNL Adobe Analytics for Advertising] を持つ広告主](/help/integrations/analytics/overview.md); オプション） Search, Social, &amp; Commerceが広告ネットワーク用にアップロードしたデータを送信する1つ以上のAnalytics レポートスイート （エンティティの分類やアカウントのクリックデータを含む）。

レポートスイートにデータを表示するには、（a）アカウントにサーバーサイド AMO ID機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、広告主の[!DNL Analytics] アカウントは、Search、Social、およびCommerceからデータを受信するように設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ トラッキング専用アカウントを実装 [!DNL Naver] します](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [広告ネットワークアカウントについて](/help/search-social-commerce/new-ui/manage/accounts/ad-network-account-about.md)
