---
title: （新しいUI） ユーザー管理
description: ユーザーアクセスの管理方法について説明します。
feature: Search Introduction
exl-id: bfc43692-cfb6-468f-90df-a808a21a0c23
TQID: https://experienceleague.adobe.com/b28N5zmqqdZ6Yvg2swGLWv260fWsMUgjK2eW1DDn-uo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1045
ht-degree: 0%

---

# （新しいUI）検索、ソーシャル、コマースのユーザー管理

一部のユーザーは、すべてのAdobeの使用権限とユーザー管理を一元管理する[Adobe Admin Console](https://helpx.adobe.com/enterprise/using/admin-console.html)を使用して、新しいSearch, Social, &amp; Commerce ユーザーインターフェイスへのアクセスを管理できます。 ユーザーは、エンドユーザーまたは管理者に分類されます。 管理者の場合は、Adobe アカウントチームから通知されます。 管理者の場合は、次の節を参照して、ユーザーを管理するための権限とワークフローを特定してください。

## 管理者の種類

Admin Consoleには、複数のタイプの管理者が用意されています。 Search、Social、およびCommerceには、次の管理者タイプと権限が必要です。 ユーザー管理タスクを委任する場合は、追加のタイプを追加できます。

**システム管理者：**&#x200B;組織のすべてのクライアントインスタンスを含む、組織のすべての製品を管理するスーパーユーザー。 （クライアントインスタンスは、従来の広告主アカウントと同じで、組織IDごとに1つ以上のインスタンスがあります）。 システム管理者は、組織のすべての管理タスクをAdmin Consoleで実行でき、組織のすべての製品の管理機能を他のユーザーに委任できます。

**製品管理者：**&#x200B;特定の[!DNL Adobe]製品（検索、ソーシャル、Commerceなど）へのアクセスと、その製品に対するユーザーエンタイトルメントを管理します。 製品管理者は、製品の製品プロファイルの作成、製品のユーザーとユーザーグループの作成（削除はしません）、製品プロファイルからのユーザーとユーザーグループの追加または削除、製品から他の製品管理者の追加または削除を行うことができます。

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## デフォルトの製品プロファイル

製品プロファイル：役割に似たもので、特定の製品に対して特定のサービスを利用者に提供します。

Search, Social &amp; Commerceの新しいユーザーインターフェイスには、次のデフォルトの製品プロファイルがあり、様々な機能やサービスのサブセットを提供します。 デフォルトの製品プロファイルの製品権限を編集したり、デフォルトの製品プロファイルを削除したりすることはできません。 ただし、製品管理者、製品プロファイル管理者、システム管理者は、必要に応じて、利用可能な権限の異なるサブセットを持つ追加の製品プロファイルを作成および管理できます。

* **[!UICONTROL Basic Optimization]:**&#x200B;このプロファイルは次の機能を提供します：

   * [!UICONTROL Objectives]：完全アクセス

   * [!UICONTROL Simulations]：完全アクセス

   * [!UICONTROL Portfolio Groups]：完全アクセス

   * [!UICONTROL Portfolios]: [!UICONTROL Objectives]、[!UICONTROL Campaigns]、および費用[!UICONTROL Management]のポートフォリオ設定へのアクセス権を作成/編集します。残りのポートフォリオ設定への読み取り専用アクセス権があります。

   * [!UICONTROL Campaigns]: キャンペーン設定への読み取り専用アクセス （作成、編集、削除機能は使用できません）。制約およびポートフォリオ割り当てに対する完全アクセス権

   * [!UICONTROL Ad Groups]：広告グループ設定への読み取り専用アクセス（作成、編集、削除機能は使用できません）。制約およびポートフォリオの割り当てに対する完全アクセス権

  このアクセスレベルは、まだSearch、Social、およびCommerceの使用を学んでいるユーザーに適しています。

* **[!UICONTROL Expert Optimization]:**&#x200B;このプロファイルは次の機能を提供します：

   * [!UICONTROL Objectives]：完全アクセス

   * [!UICONTROL Simulations]：完全アクセス

   * [!UICONTROL Portfolio Groups]：完全アクセス

   * [!UICONTROL Portfolios]：完全アクセス

   * [!UICONTROL Campaigns]: キャンペーンリストへの読み取り専用アクセス （キャンペーンの作成、編集、または削除機能はまだ利用できません）。制約とポートフォリオの割り当てに完全にアクセスできます

   * [!UICONTROL Ad Groups]：広告グループリストへの読み取り専用アクセス（キャンペーンの作成、編集、または削除機能はまだ利用できません）。制約とポートフォリオの割り当てに完全にアクセスできます

  このアクセスレベルは、Search、Social、およびCommerceのエキスパートユーザーにお勧めします。

* **[!UICONTROL Read-Only]:**&#x200B;このプロファイルは次の機能を提供します：

   * [!UICONTROL Objectives]：読み取り専用アクセス

   * [!UICONTROL Simulations]：読み取り専用アクセス

   * [!UICONTROL Portfolio Groups]：読み取り専用アクセス

   * [!UICONTROL Portfolios]：読み取り専用アクセス

   * [!UICONTROL Campaigns]：読み取り専用アクセス

   * [!UICONTROL Ad Groups]：読み取り専用アクセス

* **[!UICONTROL Admin]:** This profile grants full access to all functionality available and allows users to create new client instances (the same as legacy advertiser accounts, with one or more instances per organization ID). Don&#39;t assign this right to anyone unless you have a proper business justification.

## Tasks for administrators

### Adobe Admin Consoleにログインし、Search, Social, &amp; Commerceに開きます

>[!PREREQUISITES]
>
>You must have some type of administrator access to Search, Social, &amp; Commerce to sign in to Admin Console.

1. Go to https://adminconsole.adobe.com/enterprise/.

1. (If you&#39;re not signed in to CX Enterprise) Sign in to CX Enterprise:

   1. [!DNL Adobe] IDを入力し、**[!UICONTROL Continue]**&#x200B;をクリックします。

   1. Select either **[!UICONTROL Personal Account]&quot; or &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" -->

   1. 該当するCX Enterprise組織を選択します。

      Admin Consoleが[!UICONTROL Overview] タブに開きます。

   1. Under [!UICONTROL Product & services], click &quot;[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name].&quot;

      The product page opens to the [!UICONTROL Product profiles] tab for Search, Social, &amp; Commerce. その他のタブには[!UICONTROL Users]と[!UICONTROL Product Admins]が含まれます。

### Workflow for system administrators

Follow this workflow for each client instance of Search, Social, &amp; Commerce.

1. [Sign in to Adobe Admin Console and open it to Search, Social, &amp; Commerce](#open-admin-console).

1. (Optional) [Add another system administrator](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) as backup.

1. Delegate product and user management by [adding product administrators](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise).

### Workflow for product administrators

Search, Social, &amp; Commerceの各クライアントインスタンスについて、このワークフローに従います。

1. [Adobe Admin Consoleにログインし、Search, Social, &amp; Commerceに開きます](#open-admin-console)。

1. 必要に応じて、[個別に](https://helpx.adobe.com/enterprise/using/manage-users-individually.html)または[一括で](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) エンドユーザーを作成します。

1. （オプション）インスタンスの[&#x200B; ユーザーグループ &#x200B;](https://helpx.adobe.com/enterprise/using/user-groups.html)を作成し、各ユーザーグループにユーザーを割り当てます。

   インスタンスに多数のユーザーがいる場合は、ユーザーグループを作成して、ユーザーがそのレベルの専門知識に基づいて適切なプロファイルを割り当てられていることを確認します。 （製品プロファイルへのユーザーグループの割り当てについては、手順4を参照してください）。 事業部門、ユーザーアクセスのニーズ、ユーザーの採用日などの基準にもとづいて、ユーザーグループを作成できます。

   >[!IMPORTANT]
   >
   >ユーザーグループ名は、ユーザーグループに割り当てる権限を明確に伝える必要があります。 例えば、「読み取り専用」権限を持つユーザーグループを作成する場合、「Acme_Uk_ReadOnly」や「Acme_ReadOnly」などのユーザーグループ名に「読み取り専用」を含めます。

1. （オプション） [定義された権限セットを持つカスタム製品プロファイル &#x200B;](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)を作成します。

   カスタムプロファイルには、既に使用可能な4つのデフォルト製品プロファイルが含まれています。

   組織の各製品プロファイルには、一意の名前を付ける必要があります。 組織で複数のSearch、Social、Commerce インスタンス（Acme_USやAcme_JPなど）を使用している場合、複数のインスタンスで製品プロファイル名を複製することはできません。 **ベストプラクティス：** 「Simulations_Only_JP」などの命名規則`<Name>_<Instance>,`を使用します。

   **注意：**&#x200B;製品の権限は非常に詳細です。 カスタム製品プロファイルを設定する場合や、含める機能を省略する場合は注意してください。

1. [各ユーザーまたはユーザーグループを、手動または一括で関連する製品プロファイル &#x200B;](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html)に割り当てます。

## 完全なユーザー管理ガイドとその他のリンク

* Adobe Admin Consoleを使用したユーザー管理について詳しくは、「[Adobe Enterprise &amp; Teams Administration Guide](https://helpx.adobe.com/enterprise/admin-guide.html)」を参照してください。これには、[Admin Consoleの概要](https://helpx.adobe.com/enterprise/using/admin-console.html)が含まれます。

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
