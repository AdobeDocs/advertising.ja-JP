---
title: ユーザー管理
description: 詳細については、を参照してください。
feature: Search Introduction
source-git-commit: ab6acc0ac777edb625b91a29464ca00a4407dcf1
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# （新しい UI）検索、ソーシャル、コマース用のユーザー管理

一部のユーザーは、Adobe Admin Consoleを使用して新しい検索、ソーシャル、Commerceのユーザーインターフェイスへのアクセスを管理できます。この場所では、Adobeのすべての使用権限とユーザー管理を一元的に管理できます。 ユーザーは、エンドユーザーまたは管理者のいずれかに分類されます。 管理者の場合は、Adobe アカウントチームから通知されます。 管理者の場合は、次の節を参照して、ユーザーを管理するための権限とワークフローを特定してください。<!-- How can you see what your user role is, or will your Adobe Account Team tell you? -->

## 関連するタイプの管理者

Admin Consoleには複数のタイプの管理者が用意されていますが、検索、ソーシャル、Commerceに関連するのは、次の管理者のタイプと権限のみです。

**システム管理者：** 組織のスーパーユーザー。 システム管理者は、組織のAdmin Consoleですべての管理タスクを実行でき、他のユーザー（製品管理者）に管理機能を委任できます。&lt;! – 製品プロファイル管理者、ユーザーグループ管理者。   – 製品の管理者だけだと思いますか？  確認します。—>

**製品管理者：** 特定の [!DNL Adobe] 製品（検索、ソーシャル、Commerceなど）へのアクセスと、その製品に対するユーザーの使用権限を管理します。 製品管理者は、製品の製品プロファイルの作成、ユーザーとユーザーグループの作成（削除は不可）、製品プロファイルへのユーザーとユーザーグループの追加または削除、製品への他の製品管理者の追加または削除を行うことができます。

<!--
**Product profile admin:** Manages assigned product profiles for individual products. A product profile admin can add (but not remove) users and user groups to the organization; add or remove users and user groups from product profiles; and assign or revoke permissions from product profiles. [I don't think this is applicable: and manage the product roles for product profiles.]

**User group admin:** Manages assigned user groups and their access rights. A user group admin can add or remove users from groups and add or remove user group admins from groups.
-->

## デフォルトの製品プロファイル

役割と類似した製品プロファイルは、ユーザーに対して、特定の製品の特定のサービスを提供する権利を付与します。

検索、ソーシャル、コマース用の新しいユーザーインターフェイスには、次のデフォルト製品プロファイルがあり、様々な機能やサービスのサブセットを提供します。 デフォルトの製品プロファイルは、編集または削除できません。 ただし、システム管理者は、必要に応じて、権限のサブセットが異なる追加の製品プロファイルを作成および管理できます。

* **基本的な最適化：** このプロファイルは次の機能を提供します。

   * 目標：フルアクセス

   * シミュレーション：フルアクセス

   * Portfolio グループ：フルアクセス

   * ポートフォリオ：目標、キャンペーン、支出管理のポートフォリオ設定へのアクセスを作成/編集します。残りのポートフォリオ設定への読み取り専用アクセスも可能です。

   * キャンペーン：キャンペーン設定への読み取り専用アクセス（作成、編集、削除の各機能は利用できません）。制約の割り当てとポートフォリオの割り当てへのフルアクセス <!-- Is that the correct wording? -->

   * 広告グループ：広告グループ設定への読み取り専用アクセス（作成、編集、削除の各機能は利用できません）。制約の割り当てとポートフォリオの割り当てへのフルアクセス <!-- Is that the correct wording? -->

  このアクセスレベルは、検索、ソーシャル、Commerceの使用を習得中のユーザーに推奨されます。

* **エキスパートの最適化：** このプロファイルは次の機能を提供します。

   * 目標：フルアクセス

   * シミュレーション：フルアクセス

   * Portfolio グループ：フルアクセス

   * ポートフォリオ：フルアクセス

   * キャンペーン：キャンペーンリストへの読み取り専用アクセス（キャンペーンの作成、編集、削除の機能はまだ使用できません）。制約とポートフォリオの割り当てへのフルアクセス <!-- Is that the correct wording? -->

   * 広告グループ：広告グループリストへの読み取り専用アクセス（キャンペーンの作成、編集または削除の機能はまだ使用できません）。制約とポートフォリオの割り当てへのフルアクセス <!-- Is that the correct wording? -->

  検索、ソーシャル、Commerceのエキスパートユーザーには、このアクセスレベルをお勧めします。

* **読み取り専用：** このプロファイルは次の機能を提供します。

   * 目標：読み取り専用アクセス

   * シミュレーション：読み取り専用アクセス

   * Portfolio グループ：読み取り専用アクセス

   * ポートフォリオ：読み取り専用アクセス

   * キャンペーン：読み取り専用アクセス

   * 広告グループ：読み取り専用アクセス

* **管理者：** このプロファイルは、使用可能なすべての機能に対するフルアクセス権を付与し、ユーザーが新しいクライアントインスタンスを作成できるようにします。 適切なビジネス上の理由がない限り、この権限を誰にも割り当てないでください。

<!-- Do I need to include this? If so, adjust wording as needed

## Product-specific instances

 -->

## 管理者向けのタスク

### Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceで開きます

>[!PREREQUISITES]
>
>管理者アクセス権が必要です &lt;! – どんな種類ですか。 製品管理者、システム管理者ですが、検索、ソーシャル、Commerceの各ページでは、製品プロファイル管理者またはユーザーグループ管理者（内部グループの場合もあります – チェック）も確認できます。

1. https://adminconsole.adobe.com/enterprise/に移動します。

1. （Experience Cloudにログインしていない場合） Experience Cloudにログインします。

   1. [!DNL Adobe] ID を入力し、「**[!UICONTROL Continue]**」をクリックします。

   1. **[!UICONTROL Personal Account]&quot;または &#x200B;** [!UICONTROL Company or School Account]**.<!-- Will it necessarily be "Company or School Account?" --> を選択します。

   1. 該当するExperience Cloud組織を選択します。

   1. 製品とサービスで、「[!UICONTROL Adobe Advertising, Search, Social, & Commerce — Org Name]」をクリックします。

   デフォルトでは、検索、ソーシャル、Commerceの「[!UICONTROL Product profiles]」タブに商品ページが開きます。 その他のタブには、「[!UICONTROL Users]」および「[!UICONTROL Product Admins]」があります。

### システム管理者向けのワークフロー

1. [Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceに開きます ](#open-admin-console)。

1. [ 製品管理者の追加 ](https://helpx.adobe.com/jp/enterprise/using/admin-roles.html#enterprise) による製品およびユーザー管理の委任。

<!-- what else? -->

### 製品管理者向けのワークフロー

1. [Adobe Admin Consoleにログインし、検索、ソーシャル、Commerceに開きます ](#open-admin-console)。

1. 必要に応じて、エンドユーザーを [ 個別に ](https://helpx.adobe.com/jp/enterprise/using/manage-users-individually.html) または [ 一括で ](https://helpx.adobe.com/jp/enterprise/using/bulk-upload-users.html) 作成します。

1. （オプション）各製品インスタンスに [ ユーザーグループ ](https://helpx.adobe.com/jp/enterprise/using/user-groups.html) を作成し、各ユーザーグループにユーザーを割り当てます。

   インスタンスに多数のユーザーが存在する場合は、ユーザーグループを作成し、ユーザーが専門知識のレベルに基づいて適切なプロファイルに割り当てられるようにします。 （製品プロファイルにユーザーグループを割り当てるには、手順 4 を参照してください）。 業種、ユーザーアクセスのニーズ、ユーザーの入社日、またはその他の条件に基づいてユーザーグループを作成できます。

   >[!IMPORTANT]
   >
   >ユーザーグループ名は、ユーザーのグループに割り当てる権限を明確に伝える必要があります。 例えば、「読み取り専用」の権限を持つユーザーグループを作成する場合、「Acme_Uk_ReadOnly」や「Acme_ReadOnly」のように、ユーザーグループ名に「読み取り専用」を含めます。

1. （オプション） [ カスタム製品プロファイルの作成 ](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html) 定義済みの権限セットを使用します。

   既に利用可能な 4 つのデフォルトの製品プロファイルに加えて、カスタムプロファイルも使用できます。

   組織の各製品プロファイルには、一意の名前が必要です。 検索、ソーシャル、Commerceの複数のインスタンス（Acme_US や Acme_JP など）を使用している場合、1 つの製品プロファイル名を複数のインスタンスで重複することはできません。 **ベストプラクティス：** 命名規則を使用します&quot;&lt;Name>_&lt;Instance>,」など。

1. [ 各ユーザーまたはユーザーグループを、関連する製品プロファイルに ](https://helpx.adobe.com/jp/enterprise/using/manage-product-profiles.html) 手動でまたは一括で割り当てます。

## 完全なユーザー管理ガイドおよびその他のリンク

* Adobe Admin Consoleを使用したユーザー管理について詳しくは、[Adobeの概要を含む「](https://helpx.adobe.com/jp/enterprise/admin-guide.html)Admin Console Enterprise &amp; Teams 管理ガイド [」を参照してください ](https://helpx.adobe.com/jp/enterprise/using/admin-console.html)

* Admin Console: [https://adminconsole.adobe.com](https://adminconsole.adobe.com)
