---
title: データのアップロード用に広告ネットワークアカウントを設定する
description: 広告ネットワークアカウントのアカウント詳細を設定および管理する方法について説明します。
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: f6dcfa6d3dc0255d002d90f91e700cf285fa593b
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 0%
---
# データのアップロード用の広告ネットワークアカウントの管理

<!-- Edit all, including title and metadata -->

以下は、アカウントデータをアップロードするアドネットワークアカウントのアカウントの詳細を管理する手順です。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

>[!NOTE]
>
>Search, Social, &amp; CommerceがアドネットワークのAPIを使用して同期するアドネットワークアカウントのアカウント詳細を管理する方法については、代わりに「[API接続を介したアドネットワークアカウントの管理](../api-accounts/api-account-manage.md)」を参照してください。

## アカウント詳細を作成 {#create-account}

1. メインメニューで、**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. **[!UICONTROL Create Account]**&#x200B;をクリックします。

1. 広告ネットワークの名前をクリックし、**[!UICONTROL Next]**&#x200B;をクリックします。

1. [ アカウント設定](#account-settings)を指定します。

   1. 「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、追跡およびレポートのキャンペーンアクティビティに使用する[!DNL Analytics] レポートスイートを編集します。

   1. （オプション）「**[!UICONTROL Upload File]**」タブで、アカウントのデータファイルをアップロードします。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## アカウントの詳細を編集 {#edit-account}

1. メインメニューで、**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [ アカウント設定](#account-settings-upload)を編集します。

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （オプション、[[!DNL Adobe Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)を持つ広告主）「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、[!DNL Analytics] レポートスイートを編集して、キャンペーンアクティビティの追跡とレポートに使用します。

   1. （オプション）「**[!UICONTROL Upload File]**」タブで、アカウントのデータファイルをアップロードします。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

1. メインメニューで、**[!UICONTROL Manage]** \> **[!UICONTROL Accounts]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （[!UICONTROL Accounts] ビューから）:

     * （アカウントを有効にするには） アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Activate]**」をクリックします。

     * （アカウントを無効にするには） アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Pause]**」をクリックします。

   * （アカウント設定から）:

     1. 次のいずれかの方法でアカウントを選択します。

        * アカウント名の上にカーソルを置き、**...**&#x200B;をクリックしてから、**[!UICONTROL Edit]**&#x200B;をクリックします。

        * アカウント名の横にあるチェックボックスを選択し、一括操作ツールバーの「**[!UICONTROL Edit]**」をクリックします。

     1. 「**[!UICONTROL Account Details]**」タブで「**[!UICONTROL Account enabled]**」をオフにします。

     1. **[!UICONTROL Save]**&#x200B;をクリックします。

## アカウント設定 {#account-settings-upload}

### [!UICONTROL Account Details] タブ

**[!UICONTROL Account Name]:**&#x200B;検索、ソーシャル、およびCommerce内のアカウントに表示される名前。

>[!NOTE]
>
>Search、Social、およびCommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、マッピングを更新できるようにAdobe アカウントチームに通知します。

**[!UICONTROL Network Account ID]:**&#x200B;広告ネットワークによって割り当てられたアカウント ID。 このIDは、レポートにのみ使用されます。 Search, Social, &amp; Commerceは、広告ネットワークアカウントに直接接続されません。

**[!UICONTROL Currency]:** （既存アカウントの読み取り専用）アカウントに使用される通貨の略語。

**[!UICONTROL Time Zone]:** （既存アカウントの読み取り専用）広告主のタイムゾーン。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:**&#x200B;検索、ソーシャル、およびCommerceを使用すると、指定したS3 バケットの自動データ取得が可能になります。

### [!UICONTROL Setup Analytics] タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （統合[[!DNL Adobe Analytics for Advertising] を持つ広告主](/help/integrations/analytics/overview.md); オプション） Search, Social, &amp; Commerceが広告ネットワーク用にアップロードしたデータを送信する1つ以上のAnalytics レポートスイート （エンティティの分類やアカウントのクリックデータを含む）。

レポートスイートにデータを表示するには、（a）アカウントにサーバーサイド AMO ID機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、広告主の[!DNL Analytics] アカウントは、Search、Social、およびCommerceからデータを受信するように設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

### [!UICONTROL Upload File] タブ

（オプション）アカウントのデータファイルをアップロードします。<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
