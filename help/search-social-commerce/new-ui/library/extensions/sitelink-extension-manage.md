---
title: 共有サイトリンク拡張機能を管理
description: 共有サイトリンク拡張機能の作成、編集および削除方法について説明します。
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
source-wordcount: '1127'
ht-degree: 0%
---
# 共有サイトリンク拡張機能を管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

サイトリンクは、テキスト広告リスト内の追加テキストリンクです。 サイトリンクを使用すると、サイト上の特定のページにオーディエンスを直接誘導できます。 広告ネットワークは、広告との関連性に基づいて、表示するサイトリンクを決定します。

オプションで、各サイトリンクに説明テキストを含めることができます。 また、広告ネットワークは、サイトリンクに関連性が高い場合、アカウント内の既存の広告のコピーを表示することもできます。 [!DNL Google Ads]は、デスクトップ広告では2 ～ 6個、モバイル広告では4個までサイトリンクを表示できます。 [!DNL Microsoft Advertising]には、説明のあるサイトリンクが2つ、4つ、6つ、または説明なしのサイトリンクが表示される場合があります。

[同期広告ネットワークアカウント &#x200B;](/help/search-social-commerce/new-ui/manage/accounts/api-accounts/api-account-manage.md)のアカウントレベルで、共有サイトリンクのテキストと設定を作成します。 ライブラリ内のサイトリンクは、アカウントエンティティに関連付けるまで広告と共に使用されません。

## [!UICONTROL Sitelinks]および[!UICONTROL Associations] ビューについて {#sitelink-view-about}

**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;では、**[!UICONTROL Sitelinks]** タブにアカウントレベルの共有サイトリンクが一覧表示されます。 「**[!UICONTROL Associations]**」タブには、拡張機能とアカウントエンティティの関連付けが一覧表示されます。

これらのタブを表示するには[!UICONTROL View Extensions]権限が必要です。 サイトリンクの作成、編集、削除、関連の作成または削除には、[!UICONTROL Edit Extensions]権限が必要です。

[Microsoft Ads アカウント &#x200B;](https://support.google.com/google-ads/answer/6372658)および[Google Ads アカウント &#x200B;](https://help.ads.microsoft.com/#apex/3/en/52001)あたりの最大拡張機能の数については、広告ネットワークのヘルプを参照してください。

### 使用可能なアクション

* [共有サイトリンクの作成](#sitelink-create)

* [共有サイトリンク設定の編集](#sitelink-edit)

* [共有サイトリンクを削除](#sitelink-delete)

* [共有サイトリンクをアカウント、キャンペーン、広告グループに関連付ける](ad-extension-association-manage.md#sitelink-associate)

* [拡張機能の関連付けを削除](ad-extension-association-manage.md#association-delete)

* [選択した行のすべてのデータをクリップボードにコピー](#copy-to-clipboard)

## 共有サイトリンクの作成 {#sitelink-create}

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Sitelinks]** タブをクリックします。

1. **[!UICONTROL Create Sitelink]**&#x200B;をクリックします。

1. **[!UICONTROL Basic Settings]**&#x200B;で、広告ネットワークとアカウントを選択します。

1. [共有サイトリンク設定](#shared-sitelink-settings)を入力します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 設定を確認します。 設定を変更するには、該当するセクションの&#x200B;**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

サイトリンクを作成したら、[&#x200B; アカウント、キャンペーン、または広告グループに関連付けます](ad-extension-association-manage.md#sitelink-associate)。

## 共有サイトリンク設定の編集 {#sitelink-edit}

共有サイトリンクは一度に1つずつ編集できます。 作成後に開始日を変更することはできません。

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Sitelinks]** タブをクリックします。

1. 1つのサイトリンクの横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [共有サイトリンク設定](#shared-sitelink-settings)を編集します。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認し、**[!UICONTROL Update]**&#x200B;をクリックします。

サイトリンクの値をクリックして、データテーブル内でサイトリンクの&#x200B;**[!UICONTROL Base URL]**&#x200B;または&#x200B;**[!UICONTROL Tracking Template]**&#x200B;を直接編集することもできます。

## 共有サイトリンクを削除 {#sitelink-delete}

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Sitelinks]** タブをクリックします。

1. 削除する各共有サイトリンクの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

ライブラリから共有サイトリンクを削除せずに関連付けを削除するには、代わりに[関連付けを削除](ad-extension-association-manage.md#association-delete)してください。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

## 共有サイトリンク設定 {#shared-sitelink-settings}

サイトリンクの非承認に関するその他のポリシーと理由については、[Google Ads サイトリンクの要件](https://support.google.com/adspolicy/answer/1054210)および[Microsoft Advertising サイトリンクの要件](https://help.ads.microsoft.com/#apex/ads/en/ext60206)を参照してください。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** リンクに表示されるテキスト。 これには、最大25個のシングルバイト文字または12個のダブルバイト文字を含めることができます。 リンクテキストは、アカウントまたはキャンペーン内で一意である必要があります。

>[!NOTE]
>
>（[!DNL Google Ads]） 35文字の既存のテキストは、デスクトップやタブレットでは広告に表示されますが、モバイルデバイスでは表示されません。

**[!UICONTROL Status]:**&#x200B;既存のサイトリンクのサイトリンクの表示ステータス：**[!UICONTROL Active]**&#x200B;または&#x200B;**[!UICONTROL Deleted]**。 新しいサイトリンクはデフォルトでアクティブになっています。

**[!UICONTROL Description Line 1]、[!UICONTROL Description Line 2]:**&#x200B;広告ネットワークがリンクテキストの下に表示できる追加テキスト。 説明を含めるには、両方のフィールドを入力します。 それぞれ、最大35個の1 バイト文字または17個の2 バイト文字を含めることができます。

**[!UICONTROL Start Date]:** （オプション、作成のみ） サイトリンクを表示できる最初の日付。 デフォルトは現在の日付です。 今後の日付を指定するには、MM/DD/YYYY形式で入力するか、日付選択ツールを使用します。 開始日は、既存のサイトリンクに対して読み取り専用です。

**[!UICONTROL End Date]:** （オプション）サイトリンクを表示できる最後の日付。 デフォルトでは、サイトリンクは無期限に表示される場合があります。 終了日を指定するには、MM/DD/YYYY形式で入力するか、日付選択ツールを使用します。

**[!UICONTROL Mobile Preference]:** （オプション）デスクトップ ユーザーやタブレットユーザーではなく、モバイルデバイス ユーザーに拡張機能を表示しようとすることをネットワークに許可します。 デフォルトでは、このオプションは有効になっておらず、拡張機能は任意のデバイスタイプに表示されます。 ネットワークは、好みのデバイスタイプに拡張機能が表示されることを保証するものではありません。

### [!UICONTROL URL Options]

{{$include /help/_includes/base-url-keyword-ad-sitelink.md}}

**[!UICONTROL Tracking Template]:** （オプション）最後のランディングページ URLをパラメーターに埋め込んだ、オフランディングドメインのリダイレクトとトラッキングパラメーターを含むトラッキング URL。 例：`https://www.trackingservice.example.com/?url={lpurl}&source={network}&id=5`。

このビューでは、[!UICONTROL Base URL]と[!UICONTROL Tracking Template]に入力された値は`http://`または`https://`で始まる必要があり、スペースを含めることはできません。

* キャンペーン設定に&#x200B;**[!UICONTROL EF Redirect]**&#x200B;と&#x200B;**[!UICONTROL Auto Upload]**&#x200B;が含まれている場合、レコードを保存すると、Search、Social、およびCommerceが自動的に独自のリダイレクトコードとトラッキングコードのプレフィックスを付けます。

* 最終的なURLを埋め込むパラメーターについては、[Microsoft Advertising ドキュメント &#x200B;](https://help.ads.microsoft.com/#apex/3/en/56799)または[Google Ads ValueTrack ドキュメント &#x200B;](https://support.google.com/google-ads/answer/6305348)の「トラッキングテンプレートのみ」パラメーターを参照してください。

* URL パラメーターとキャンペーンレベルのカスタムパラメーターを、アンパサンド（`&`）で区切って含めることができ、サードパーティのリダイレクトとトラッキングを含めることができます。

* 最も詳細なレベルのトラッキングテンプレートでは、より高いレベルのテンプレートが上書きされます。

>[!NOTE]
>
>* 最終URLを持つアカウントの場合、ベース URLには、ランディングページドメインまたはサブドメイン内のリダイレクトが含まれますが、ランディングページドメイン外のリダイレクトは含まれません。 広告ネットワークは、表示URLを作成するためにドメインを抽出します。
>* （[!DNL Google Ads]） キャンペーンまたは広告グループ内の各サイトリンクには、約80%の一意のコンテンツを含む一意のランディングページが必要です。 同じページの複数のアンカーへのリンクを、個別のサイトリンクランディングページとして使用しないでください。
>* （[!DNL Google Ads]） サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 アカウント、キャンペーン、または広告グループレベルで更新しても、広告は再送信されません。
>* （[!DNL Microsoft Advertising]）承認のために広告を再送信せずに、任意のレベルでトラッキングテンプレートを更新できます。
>* （[!DNL Google Ads]）並列トラッキングを有効にするソースからのクリックに代わらないマクロを避けます。 マクロが必要な場合は、Adobe アカウントチームがカスタマーサポートまたは実装チームと協力してマクロを追加します。

## サイトリンクのパフォーマンスデータ {#sitelink-performance}

Search, Social, &amp; Commerceは、広告の拡張機能をクリックし、その拡張機能が表示される広告に関連付けられたキーワードにコンバージョンをマッピングします。 Search, Social, &amp; Commerceでは、拡張機能レベルのコストとクリックデータは利用できません。

[!UICONTROL Transaction Report]では、`sl:See Current Offers`などの[!UICONTROL Link Type]の値`sl:<Sitelink text>`は、広告自体ではなくサイトリンクからのトランザクションを識別します。 「[&#x200B; トランザクションレポート &#x200B;](/help/search-social-commerce/new-ui/reports/management/basic-advanced/transaction-report.md)」を参照してください。

広告ネットワークのインターフェイスで拡張機能レベルのコストを表示し、データをクリックすることができます。

>[!MORELIKETHIS]
>
>* [Google Ads共有コールアウト拡張機能の管理](callout-extension-manage.md)
>* [広告拡張機能の関連付けを管理](ad-extension-association-manage.md)
