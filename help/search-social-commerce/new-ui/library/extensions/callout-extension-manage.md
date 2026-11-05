---
title: Google Ads共有コールアウト拡張機能の管理
description: Google Ads共有コールアウト拡張機能を作成、編集、削除する方法について説明します。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%
---
# [!DNL Google Ads]個の共有コールアウト拡張機能を管理

*[!DNL Google Ads]アカウントのみ*

コールアウト拡張機能とは、サイトが提供する製品、サービス、プロモーションに関する情報テキストを、テキスト広告とともに表示することです。 広告ネットワークは、広告を含む2～4のコールアウトを表示する場合があります。

[同期済みのGoogle Ads アカウント &#x200B;](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)のアカウントレベルで、共通のコールアウトテキストと設定を作成します。 ライブラリ内のコールアウトは、検索ネットワークでサポートされているキャンペーンまたは広告グループに関連付けるまで、広告では使用されません。

コールアウト付きの広告を表示する資格を得るには、キャンペーンまたは広告グループごとに少なくとも2つのコールアウトを割り当てます。 広告グループレベルのコールアウトは、キャンペーンレベルのコールアウトを上書きします。

## [!UICONTROL Callouts]および[!UICONTROL Associations] ビューについて {#callout-view-about}

**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;では、**[!UICONTROL Callouts]** タブにアカウントレベルの共有コールアウトが一覧表示されます。 「**[!UICONTROL Associations]**」タブには、拡張機能とアカウントエンティティの関連付けが一覧表示されます。

これらのタブを表示するには[!UICONTROL View Extensions]権限が必要です。 コールアウトの作成、編集、削除、関連の作成または削除には、[!UICONTROL Edit Extensions]権限が必要です。

1 アカウントあたりの最大拡張機能の数については、アカウント制限[&#128279;](https://support.google.com/google-ads/answer/6372658)に関するGoogle広告のドキュメントを参照してください。

### 使用可能なアクション

* [共有コールアウトの作成](#callout-create)

* [共有コールアウト設定の編集](#callout-edit)

* [共有コールアウトの削除](#callout-delete)

* [共有コールアウトをキャンペーンと広告グループに関連付ける](ad-extension-association-manage.md#callout-associate)

* [拡張機能の関連付けを削除](ad-extension-association-manage.md#association-delete)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

## 共有コールアウトの作成 {#callout-create}

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Callouts]** タブをクリックします。

1. **[!UICONTROL Create Callout]**&#x200B;をクリックします。

1. **[!UICONTROL Basic Settings]**&#x200B;で、[!DNL Google Ads]とアカウントを選択します。

1. [共有コールアウト設定](#shared-callout-settings)を入力します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 設定を確認します。 設定を変更するには、該当するセクションの&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

コールアウトを作成したら、[&#x200B; キャンペーンまたは広告グループに関連付けます](ad-extension-association-manage.md#callout-associate)。

## 共有コールアウト設定の編集 {#callout-edit}

1つの共有コールアウトを一度に編集できます。 作成後に開始日を変更することはできません。

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Callouts]** タブをクリックします。

1. 1つの吹き出しの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [共有コールアウト設定](#shared-callout-settings)を編集します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認し、**[!UICONTROL Update]**&#x200B;をクリックします。

## 共有コールアウトの削除 {#callout-delete}

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Callouts]** タブをクリックします。

1. 削除する各共有コールアウトの横にあるチェックボックスをオンにします。

   複数の行の選択について詳しくは、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

ライブラリから共有コールアウトを削除せずに関連付けを削除するには、代わりに[関連付けを削除](ad-extension-association-manage.md#association-delete)します。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## 共有コールアウト設定 {#shared-callout-settings}

コールアウトの承認を取り消す追加のポリシーと理由については、[Google Ads コールアウト要件](https://support.google.com/adspolicy/answer/1054212)を参照してください。

**[!UICONTROL Callout Text]:**&#x200B;表示されるテキスト。 これには、最大25個のシングルバイト文字または12個のダブルバイト文字を含めることができます。 テキストの先頭に感嘆符や句読点を含めることはできません。

**[!UICONTROL Start Date]:** （オプション、作成のみ）引き出しが表示される最初の日付。 デフォルトは現在の日付です。 今後の日付を指定するには、MM/DD/YYYY形式で入力するか、日付選択ツールを使用します。 開始日は、既存のコールアウトに対して読み取り専用です。

**[!UICONTROL End Date]:** （オプション）コールアウトが表示される最後の日付。 デフォルトでは、コールアウトは無期限に表示される場合があります。 終了日を指定するには、MM/DD/YYYY形式で入力するか、日付選択ツールを使用します。

**[!UICONTROL Mobile Preference]:** （オプション） [!DNL Google Ads]が、デスクトップまたはタブレットユーザーではなく、モバイルデバイスユーザーに拡張機能を表示しようとすることを許可します。 それ以外の場合、拡張機能は任意のデバイスタイプに表示されます。 [!DNL Google Ads]は、好みのデバイスタイプで拡張機能が表示されることを保証しません。

## コールアウトのパフォーマンスデータ {#callout-performance}

Search, Social, &amp; Commerceは、広告の拡張機能をクリックし、その拡張機能が表示される広告に関連付けられたキーワードにコンバージョンをマッピングします。 Search, Social, &amp; Commerceでは、拡張機能レベルのコストとクリックデータは利用できません。

拡張機能レベルのコストを表示し、[!DNL Google Ads] インターフェイスでデータをクリックできます。

>[!MORELIKETHIS]
>
>* [共有サイトリンク拡張機能の管理](sitelink-extension-manage.md)
>* [広告拡張機能の関連付けを管理](ad-extension-association-manage.md)
