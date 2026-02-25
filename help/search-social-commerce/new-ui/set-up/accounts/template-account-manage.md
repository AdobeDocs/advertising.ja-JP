---
title: （新しい UI）トラッキングのみの管理  [!DNL Naver]  アカウント
description: アカウントの新しい UI でアカウントの詳細を設定および管理する方法について説明  [!DNL Naver]  ます。
feature: Search Campaign Management
source-git-commit: 0de2a01905727314ca6c0792c5efaf6450548293
workflow-type: tm+mt
source-wordcount: '481'
ht-degree: 0%

---

# （新しい UI）トラッキング専用で [!DNL Naver] アカウントを管理

*Beta機能*

以下は、広告ネットワークから直接購入した広告のパフォーマンスを追跡、レポート、視覚化する [[!DNL Naver]  アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md) の管理の手順です。 検索、ソーシャル、Commerceでは、データを広告ネットワークと同期したり、自動入札を行ったり、あらゆる種類の最適化やシミュレーションを行ったりしません。

使用可能な機能について詳しくは、「[&#x200B; サポート対象インベントリ &#x200B;](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## 広告ネットワークアカウントの詳細を作成 {#create-account}

アカウントのトラッキングを有効にするには、対応するアカウントレコードを作成する必要があります。そのレコードには、アカウントアクセス資格情報と、ステータスが *有効* です。

>[!NOTE]
>
>広告ネットワーク上に実際のアカウントを作成するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 「**[!UICONTROL Create Account]**」をクリックします。

1. 広告ネットワークの名前をクリックし、[**[!UICONTROL Next]**] をクリックします。

1. [&#x200B; アカウント設定 &#x200B;](#account-settings-naver) を指定します。

   1. 「**[!UICONTROL Enter Account Details]**」タブで、一般的なアカウント設定を指定します。

   1. （[[!DNL Adobe Analytics for Advertising]  統合 &#x200B;](/help/integrations/analytics/overview.md)）を使用する広告主 **[!UICONTROL Set up Adobe Analytics]** タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用するすべての [!DNL Analytics] レポートスイートを選択します。

1. 「**[!UICONTROL Save]**」をクリックします。

## 広告ネットワークアカウントの詳細の編集 {#edit-account}

アカウント名を変更したり、アカウントステータスを変更したり、トラッキングとレポートに使用する [!DNL Analytics] レポートスイートを変更したりするには、アカウントの詳細を編集します。

>[!NOTE]
>
>広告ネットワーク上の実際のアカウントを編集するには、広告ネットワークの web サイトにアクセスします。

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

1. [&#x200B; アカウント設定 &#x200B;](#account-settings-api) の編集：

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （任意。[[!DNL Adobe Analytics for Advertising]  統合 &#x200B;](/help/integrations/analytics/overview.md)）を使用する広告主。「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用する [!DNL Analytics] レポートスイートを編集します。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 「**[!UICONTROL Save]**」をクリックします。

<!-- What does this do?

## Enable or disable ad network accounts {#enable-disable-account}

When you enable an ad network account, Search, Social, & Commerce synchronizes campaign data with the account (when supported) and pushes automated bids and/or campaign budgets for campaigns in portfolios. When you disable an ad network account, Search, Social, & Commerce stops all activity on the account. Data collected while the account was active is still stored, but the campaign management views and reports don't include data for the time period in which the account is disabled. You can later re-enable the account to resume activity with the account.

1. In the main menu, click **[!UICONTROL Setup]** \> **[!UICONTROL Accounts]**.

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

## ネットワーク アカウント設定の追加 {#account-settings-api}

### 「[!UICONTROL Account Details]」タブ

#### [!UICONTROL Enter Account Details]/[!UICONTROL Account Details]

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

>[!NOTE]
>
>検索、ソーシャル、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更している場合は、Adobe アカウントチームに連絡してマッピングを更新してください。

**[!UICONTROL Network Account ID]:** 広告ネットワークによって割り当てられたアカウント ID。

**[!UICONTROL Currency]:** 勘定に使用する通貨の省略形。

**[!UICONTROL Time Zone]:** 広告主のタイムゾーン。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** 検索、ソーシャル、Commerceは、キャンペーンデータをアカウントと同期し（サポートされている場合）、ポートフォリオのキャンペーンの自動入札やキャンペーン予算をプッシュします。

## 「[!UICONTROL Setup Analytics]」タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （[[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md);（任意）を使用する広告主。検索、ソーシャルおよびCommerceが、広告ネットワークにアップロードする 1 つ以上の Analytics レポートスイート。アカウントのエンティティ分類やクリックデータも含まれます。

レポートスイートにデータを表示するには、（a） アカウントに対してサーバーサイド AMO ID 機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、検索、ソーシャル、Commerceからデータを受信するように広告主の [!DNL Analytics] アカウントを設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [&#x200B; 実装  [!DNL Naver]  トラッキング専用アカウント &#x200B;](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)
>* [&#x200B; 広告ネットワークアカウントについて &#x200B;](/help/search-social-commerce/new-ui/set-up/accounts/ad-network-account-about.md)
