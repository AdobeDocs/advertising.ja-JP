---
title: データのアップロード用に広告ネットワークアカウントを設定
description: 広告ネットワークアカウントのアカウント詳細を設定および管理する方法について説明します。
feature: Search Campaign Management
exl-id: 7e8fb475-21f9-446b-a112-e0f27a4c4172
source-git-commit: 00565a6c9e784472fab9c9d223c83b0c7cbb91b1
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 0%

---

# データのアップロードに使用する広告ネットワークアカウントの管理

<!-- Edit all, including title and metadata -->

以下は、アカウントデータをアップロードする広告ネットワークアカウントのアカウント詳細の管理手順です。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

>[!NOTE]
>
>広告ネットワークの API を使用して検索、ソーシャル、Commerceが同期する広告ネットワークアカウントのアカウント詳細を管理する手順については、代わりに「[API 接続を使用した広告ネットワークアカウントの管理 ](../api-accounts/api-account-manage.md)」を参照してください。

## アカウントの詳細を作成 {#create-account}

1. 「**[!UICONTROL Create Account]**」をクリックします。

1. 広告ネットワークの名前をクリックし、[**[!UICONTROL Next]**] をクリックします。

1. [ アカウント設定 ](#account-settings) を指定します。

   1. 「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （[[!DNL Adobe Analytics for Advertising]  統合 ](/help/integrations/analytics/overview.md)）を使用する広告主 **[!UICONTROL Set up Adobe Analytics]** タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用する [!DNL Analytics] レポートスイートを編集します。

   1. （オプション）「**[!UICONTROL Upload File]**」タブで、アカウントのデータファイルをアップロードします。

1. 「**[!UICONTROL Save]**」をクリックします。

## アカウントの詳細を編集 {#edit-account}

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの方法でアカウントを選択します。

   * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

   * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

1. [ アカウント設定 ](#account-settings-upload) の編集：

   1. （オプション）「**[!UICONTROL Account Details]**」タブで、アカウントの詳細を編集します。

   1. （任意。[[!DNL Adobe Analytics for Advertising]  統合 ](/help/integrations/analytics/overview.md)）を使用する広告主。「**[!UICONTROL Set up Adobe Analytics]**」タブをクリックし、キャンペーンアクティビティのトラッキングとレポートに使用する [!DNL Analytics] レポートスイートを編集します。

   1. （オプション）「**[!UICONTROL Upload File]**」タブで、アカウントのデータファイルをアップロードします。

   <!-- What are the repercussions of changing the suites? Timing of updated data? -->

1. 「**[!UICONTROL Save]**」をクリックします。

## 広告ネットワークアカウントを有効または無効にする {#enable-disable-account}

1. メインメニューで、\> **[!UICONTROL Setup]** ード **[!UICONTROL Accounts]** クリックします。

1. 次のいずれかの操作をおこないます。

   * （[!UICONTROL Accounts] ビューから）:

      * （アカウントを有効にするには）アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Activate]**」をクリックします。

      * （アカウントを無効にするには）アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Pause]**」をクリックします。

   * （アカウント設定から）

      1. 次のいずれかの方法でアカウントを選択します。

         * アカウント名の上にカーソルを置き、[**...**] をクリックし、[**[!UICONTROL Edit]**] をクリックします。

         * アカウント名の横にあるチェックボックスをオンにし、一括アクションツールバーの「**[!UICONTROL Edit]**」をクリックします。

      1. [**[!UICONTROL Account Details]**] タブで、[**[!UICONTROL Account enabled]**] をオフにします。

      1. 「**[!UICONTROL Save]**」をクリックします。

## アカウント設定 {#account-settings-upload}

### 「[!UICONTROL Account Details]」タブ

**[!UICONTROL Account Name]:** 検索、ソーシャル、Commerce内でアカウントに対して表示される名前。

>[!NOTE]
>
>検索、ソーシャル、CommerceとAdobe Analyticsの統合があり、検索アカウントの名前を変更した場合は、Adobe アカウントチームに通知して、マッピングを更新できるようにします。

**[!UICONTROL Network Account ID]:** 広告ネットワークによって割り当てられたアカウント ID。 この ID はレポートにのみ使用されます。 検索、ソーシャル、Commerceは、広告ネットワークアカウントに直接接続されません。

**[!UICONTROL Currency]:** （既存のアカウントの場合は読み取り専用）アカウントに使用される通貨の略語。

**[!UICONTROL Time Zone]:** （既存のアカウントの場合は読み取り専用）広告主のタイムゾーン。

**[!UICONTROL Account Synchronization and Management]> [!UICONTROL Account Enabled]:** 検索、ソーシャル、Commerceを使用すると、指定した S3 バケットに対して自動データ取得が可能です。

## 「[!UICONTROL Setup Analytics]」タブ

**[!UICONTROL Adobe Analytics Report Suite]:** （[[!DNL Adobe Analytics for Advertising] integration](/help/integrations/analytics/overview.md);（任意）を使用する広告主。検索、ソーシャルおよびCommerceが、広告ネットワークにアップロードする 1 つ以上の Analytics レポートスイート。アカウントのエンティティ分類やクリックデータも含まれます。

レポートスイートにデータを表示するには、（a） アカウントに対してサーバーサイド AMO ID 機能を設定するか、（b）広告主レベルの「[!UICONTROL Enable Advertising reporting in Analytics]」設定を有効にする必要があります。 さらに、検索、ソーシャル、Commerceからデータを受信するように広告主の [!DNL Analytics] アカウントを設定する必要があります。 詳しくは、Adobe アカウントチームにお問い合わせください。

### 「[!UICONTROL Upload File]」タブ

（任意）アカウントのデータファイルをアップロードします。<!-- For instructions, see "[Upload offline account data for reporting and simulations](upload-account-data.md)." -->
