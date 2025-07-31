---
title: （新しい UI）ユーザー管理
description: ユーザーアクセスを管理する方法を説明します。
feature: Search Introduction
source-git-commit: c198b5ea2f8ef125b1a5d25616158d57950ce3b0
workflow-type: tm+mt
source-wordcount: '975'
ht-degree: 0%

---

# （新しい UI）検索、ソーシャル、コマース用のユーザー管理

一部のユーザーは、[Adobe Admin Console](https://helpx.adobe.com/jp/enterprise/using/admin-console.html) を使用して、新しい検索、ソーシャル、Commerceのユーザーインターフェイスへのアクセスを管理できます。この場所では、Adobeのすべての使用権限と User Management を一元的に管理できます。 ユーザーは、エンドユーザーまたは管理者のいずれかに分類されます。 管理者の場合は、Adobe アカウントチームから通知されます。 管理者の場合は、次の節を参照して、ユーザーを管理するための権限とワークフローを特定してください。

## 管理者のタイプ

Admin Consoleには複数のタイプの管理者が用意されています。 検索、ソーシャル、Commerceには、次の管理者タイプと権限が必要です。 ユーザー管理タスクを委任する場合は、タイプを追加できます。

**システム管理者：** 組織のすべての製品（組織のすべてのクライアントインスタンスを含む）を管理するスーパーユーザー。 （クライアントインスタンスは従来の広告主アカウントと同じで、組織 ID ごとに 1 つ以上のインスタンスがあります）。 システム管理者は、組織のAdmin Consoleですべての管理タスクを実行でき、組織の商品の管理機能を他のユーザーに委任できます。

**製品管理者：** 特定の [!DNL Adobe] 製品（検索、ソーシャル、Commerceなど）へのアクセスとその製品に対するユーザーの使用権限を管理します。 製品管理者は、製品の製品プロファイルの作成、製品のユーザーとユーザーグループの作成（削除は不可）、製品プロファイルへのユーザーとユーザーグループの追加または削除、製品への他の製品管理者の追加または削除を行うことができます。

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## デフォルトの製品プロファイル

役割と類似した製品プロファイルは、ユーザーに対して、特定の製品の特定のサービスを提供する権利を付与します。

検索、ソーシャル、コマース用の新しいユーザーインターフェイスには、次のデフォルト製品プロファイルがあり、様々な機能やサービスのサブセットを提供します。 デフォルト製品プロファイルの製品権限を編集したり、デフォルト製品プロファイルを削除したりすることはできません。 ただし、製品管理者、製品プロファイル管理者およびシステム管理者は、必要に応じて、使用可能な権限の異なるサブセットを持つ追加の製品プロファイルを作成および管理できます。

* **[!UICONTROL Basic Optimization]:** このプロファイルは次の機能を提供します。

   * [!UICONTROL Objectives]: フル アクセス

   * [!UICONTROL Simulations]: フル アクセス

   * [!UICONTROL Portfolio Groups]: フル アクセス

   * [!UICONTROL Portfolios]:[!UICONTROL Objectives]、[!UICONTROL Campaigns]、費用 [!UICONTROL Management] のポートフォリオ設定へのアクセス権を作成/編集します。残りのポートフォリオ設定への読み取り専用アクセス権。

   * [!UICONTROL Campaigns]：キャンペーン設定への読み取り専用アクセス（作成、編集、削除の各機能は利用できない）、制約の割り当ておよびポートフォリオの割り当てへのフルアクセス

   * [!UICONTROL Ad Groups]：広告グループ設定への読み取り専用アクセス（作成、編集、削除の各機能は利用できません）。制約の割り当ておよびポートフォリオの割り当てへのフルアクセス

  このアクセスレベルは、検索、ソーシャル、Commerceの使用を習得中のユーザーに推奨されます。

* **[!UICONTROL Expert Optimization]:** このプロファイルは次の機能を提供します。

   * [!UICONTROL Objectives]: フル アクセス

   * [!UICONTROL Simulations]: フル アクセス

   * [!UICONTROL Portfolio Groups]: フル アクセス

   * [!UICONTROL Portfolios]: フル アクセス

   * [!UICONTROL Campaigns]：キャンペーンリストへの読み取り専用アクセス （キャンペーンの作成、編集または削除の機能はまだ使用できません）。制約とポートフォリオの割り当てへのフルアクセス

   * [!UICONTROL Ad Groups]：広告グループリストへの読み取り専用アクセス（キャンペーンの作成、編集または削除の機能はまだ使用できません）。制約とポートフォリオの割り当てへのフルアクセス

  検索、ソーシャル、Commerceのエキスパートユーザーには、このアクセスレベルをお勧めします。

* **[!UICONTROL Read-Only]:** このプロファイルは次の機能を提供します。

   * [!UICONTROL Objectives]：読み取り専用アクセス

   * [!UICONTROL Simulations]：読み取り専用アクセス

   * [!UICONTROL Portfolio Groups]：読み取り専用アクセス

   * [!UICONTROL Portfolios]：読み取り専用アクセス

   * [!UICONTROL Campaigns]：読み取り専用アクセス

   * [!UICONTROL Ad Groups]：読み取り専用アクセス

* **[!UICONTROL Admin]:** このプロファイルは、使用可能なすべての機能に対するフルアクセス権を付与し、ユーザーが新しいクライアントインスタンスを作成できるようにします（従来の広告主アカウントと同じで、組織 ID ごとに 1 つ以上のインスタンスを持ちます）。 適切なビジネス上の理由がない限り、この権限を誰にも割り当てないでください。

## 管理者向けのタスク

### Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceで開きます

>[!PREREQUISITES]
>
>Admin Consoleにログインするには、検索、ソーシャル、Commerceに対する管理者アクセス権が必要です。

1. https://adminconsole.adobe.com/enterprise/に移動します。

1. （Experience Cloudにログインしていない場合） Experience Cloudにログインします。

   1. [!DNL Adobe] ID を入力し、「**[!UICONTROL Continue]**」をクリックします。

   1. **[!UICONTROL Personal Account]&quot;または &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" --> を選択します。

   1. 該当するExperience Cloud組織を選択します。

      Admin Consoleが開いて、「[!UICONTROL Overview]」タブが表示されます。

   1. [!UICONTROL Product & services] の下の「[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]」をクリックします。

      商品ページが開き、検索、ソーシャル、Commerce用の「[!UICONTROL Product profiles]」タブが表示されます。 その他のタブには、「[!UICONTROL Users]」および「[!UICONTROL Product Admins]」があります。

### システム管理者向けのワークフロー

検索、ソーシャル、Commerceの各クライアントインスタンスに対して、次のワークフローを実行します。

1. [Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceに開きます ](#open-admin-console)。

1. （任意） [ 別のシステム管理者をバックアップとして追加 ](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) ます。

1. [ 製品管理者の追加 ](https://helpx.adobe.com/enterprise/using/admin-roles.html#enterprise) による製品およびユーザー管理の委任。

### 製品管理者向けのワークフロー

検索、ソーシャル、Commerceの各クライアントインスタンスに対して、次のワークフローを実行します。

1. [Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceに開きます ](#open-admin-console)。

1. 必要に応じて、エンドユーザーを [ 個別に ](https://helpx.adobe.com/enterprise/using/manage-users-individually.html) または [ 一括で ](https://helpx.adobe.com/enterprise/using/bulk-upload-users.html) 作成します。

1. （任意）インスタンスの [ ユーザーグループ ](https://helpx.adobe.com/enterprise/using/user-groups.html) を作成し、各ユーザーグループにユーザーを割り当てます。

   インスタンスに多数のユーザーが存在する場合は、ユーザーグループを作成し、ユーザーが専門知識のレベルに基づいて適切なプロファイルに割り当てられるようにします。 （製品プロファイルにユーザーグループを割り当てるには、手順 4 を参照してください）。 業種、ユーザーアクセスのニーズ、ユーザーの入社日、またはその他の条件に基づいてユーザーグループを作成できます。

   >[!IMPORTANT]
   >
   >ユーザーグループ名は、ユーザーのグループに割り当てる権限を明確に伝える必要があります。 例えば、「読み取り専用」の権限を持つユーザーグループを作成する場合、「Acme_Uk_ReadOnly」や「Acme_ReadOnly」のように、ユーザーグループ名に「読み取り専用」を含めます。

1. （オプション） [ カスタム製品プロファイルの作成 ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) 定義済みの権限セットを使用します。

   既に利用可能な 4 つのデフォルトの製品プロファイルに加えて、カスタムプロファイルも使用できます。

   組織の各製品プロファイルには、一意の名前が必要です。 検索、ソーシャル、Commerceの複数のインスタンス（Acme_US や Acme_JP など）を使用している場合、1 つの製品プロファイル名を複数のインスタンスで重複することはできません。 **ベストプラクティス：** 「Simulations_Only_JP」などの命名規則 `<Name>_<Instance>,` を使用します。

   **注意：** 製品の権限は非常に詳細です。 カスタム製品プロファイルを設定する際は注意が必要です。また、含めたい機能が省略される場合もあります。

1. [ 各ユーザーまたはユーザーグループを、関連する製品プロファイルに ](https://helpx.adobe.com/enterprise/using/manage-product-profiles.html) 手動でまたは一括で割り当てます。

## 完全なユーザー管理ガイドおよびその他のリンク

* Adobe Admin Consoleを使用したユーザー管理について詳しくは、[Adobeの概要を含む「&lbrace;0](https://helpx.adobe.com/enterprise/admin-guide.html)Admin Console Enterprise &amp; Teams 管理ガイド [」を参照してください。](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
