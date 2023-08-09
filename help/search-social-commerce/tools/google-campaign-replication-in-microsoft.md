---
title: 複製 [!DNL Google Ads] キャンペーン [!DNL Microsoft® Advertising]
description: 同期したキャンペーンを [!DNL Google Ads] 直接同期されたにアカウント [!DNL Microsoft® Advertising] アカウント。
exl-id: 1bb0d915-bf33-4c50-88a5-268d4de5ccff
feature: Search Tools
source-git-commit: f857da54ff75ba7b8065b8c08d6d28eb54445b48
workflow-type: tm+mt
source-wordcount: '958'
ht-degree: 0%

---

# 複製 [!DNL Google Ads] キャンペーン [!DNL Microsoft® Advertising]

同期したキャンペーンを [!DNL Google Ads] 直接同期されたにアカウント [!DNL Microsoft® Advertising] アカウントを拡張 CPC(eCPC) キャンペーンとして使用します。 既存の入札とキャンペーンの予算がスケーリングされます。 既存の検索、ソーシャル、コマースの追跡はインポートされません。

次のタイプのキャンペーンとそのキャンペーン構造をレプリケートできます。

* [!DNL Google Ads] キャンペーンを次の場所で検索/表示 [!DNL Microsoft® Advertising] キャンペーンの検索と表示を行います。

* [!DNL Google Display Network] 広告画像を含むキャンペーンを [!DNL Microsoft® Advertising] Microsoft® Audience Network でのオーディエンスキャンペーンに関する情報です。

  買い物フィードベースのディスプレイキャンペーンをレプリケートする場合は、まず [!DNL Google Merchant Center] に対する製品オファー [!DNL Microsoft® Merchant Center]. キャンペーンをレプリケートする場合は、 [!DNL Microsoft® Merchant Center] を保存して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

* [!DNL Google Ads] パフォーマンス最大キャンペーン（ローカルの在庫広告を含む）を [!DNL Microsoft® Advertising] スマートショッピングキャンペーン。

キャンペーンを 1 回、毎日、毎週、毎月、または [!DNL Microsoft® Advertising]推奨スケジュールです。 オプションで、インポートジョブが実行されたときや、エラーや変更が発生したときに、毎回通知を設定することができます。 キャンペーンをにインポートしたら、 [!DNL Microsoft® Advertising]を使用すると、インポートジョブのステータスの確認、エラーログの確認、インポートジョブの手動実行、インポートスケジュールの編集、一時停止、有効化、削除をおこなうことができます。

一部のキャンペーン情報がレプリケートされていないので、 [!DNL Microsoft® Advertising] キャンペーン。 読み込まれるデータの詳細については、「 [!DNL Microsoft® Advertising] ヘルプ」[読み込み元 [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).&quot; 検索、ソーシャル、コマースのトラッキングはインポートされないので、 [アカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [広告グループ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)または [広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## 複製 [!DNL Google Ads] campaigns

>[!NOTE]
>
>買い物フィードベースのディスプレイキャンペーンを複製する場合は、まず [をレプリケート [!DNL Google Merchant Center] の製品オファー [!DNL Microsoft® Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). キャンペーンをレプリケートする場合は、 [!DNL Microsoft® Merchant Center] をインポートオプションに保存して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

詳しくは、 [何がインポートされたか [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 検索、ソーシャル、コマースのメインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. クリック **[!UICONTROL +Import]**.

1. 次を指定します。 [読み込み設定](#campaign-import-settings):

   1. Adobe Analytics の **[!UICONTROL Select accounts]** セクション：

      1. ソースおよび宛先アカウントを選択します。

      1. クリック **[!UICONTROL Get Credential Id from MSA]**.

      1. 宛先にログイン [!DNL Microsoft Advertising] アカウントを作成し、表示された秘密鍵証明書 ID をコピーして、 **[!UICONTROL Credential ID]** フィールドに入力します。

   1. Adobe Analytics の **[!UICONTROL Select campaigns & ad groups]** 「 」セクションで、インポートするキャンペーンおよび広告グループを指定します。

   1. Adobe Analytics の **[!UICONTROL Customize your import]** 「 」セクションで、読み込む項目のタイプを指定します。

   1. Adobe Analytics の **[!UICONTROL Set schedule]** 「 」セクションで、インポートジョブを実行するタイミングを指定します。

1. クリック **[!UICONTROL Post]**.

1. （オプション）検索、ソーシャルおよびコマースの追跡機能を [アカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [広告グループ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)または [広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## キャンペーンインポートジョブのスケジュール設定の編集

詳しくは、 [何がインポートされたか [!DNL Google Ads] campaigns](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. インポートジョブの横のチェックボックスを選択し、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. Adobe Analytics の **[!UICONTROL Set schedule]** セクションで、 [スケジュール設定](#campaign-import-settings).

1. クリック **[!UICONTROL Post]**.

## キャンペーンインポートジョブを表示

ソースを含むすべてのインポートジョブをリストできます [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft® Advertising] アカウント、インポート時間またはスケジュール、およびジョブを作成したユーザー。 定期的にスケジュールされたインポート中を含め、インポートジョブを複数回実行すると、各オカレンスが個別のジョブとして表示されます。

* 次のいずれかの操作を行います。

   * メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     デフォルトでは、ビューは [!UICONTROL List of Import Jobs] タブをクリックします。

   * 次から： [[!UICONTROL Import Logs] タブ](#campaign-import-log)をクリックし、 **[!UICONTROL List of Import Jobs]** タブをクリックします。

## キャンペーンインポートジョブの実行

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. インポートジョブの横にあるチェックボックスを選択します。

1. クリック ![今すぐ実行](/help/search-social-commerce/assets/run.png "今すぐ実行").

## キャンペーンインポートジョブのログを表示します {#campaign-import-log}

開始時刻やソースを含め、完了または失敗したすべてのインポートジョブをリストできます [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft® Advertising] アカウント、ジョブを作成したユーザー、成功した操作と失敗した操作の数、および各ジョブの通知を受け取った電子メールアドレス。 ターゲットに対する変更の詳細を表示できます [!DNL Microsoft® Advertising] 各ジョブで発生したアカウント ( 追加、同期、削除の項目数、およびアカウント内の各エンティティレベル（キャンペーンやキーワードなど）でエラーが発生した項目数を含む )。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 次をクリック： **[!UICONTROL Import Logs]** タブをクリックします。

1. （オプション）インポートジョブの詳細を表示するには、 [!UICONTROL Summary] 列。

## キャンペーンインポートジョブ設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** 同期済み [!DNL Google Ads] キャンペーンデータのエクスポート元のアカウント。

**[!UICONTROL Credential ID]:** 次の ID [!DNL Microsoft® Advertising] は、 [!DNL Google Ads] 認証情報。

の自動生成 [!DNL Microsoft® Advertising] 次の理由により、インポートの資格情報を使用できません： [!DNL Microsoft® Advertising] 制限事項。 担当のAdobeアカウントチームに問い合わせると、資格情報が生成され、ID が提供されます。

**[!UICONTROL Target Microsoft® Ads account]:** 同期済み [!DNL Microsoft® Advertising] アカウントを使用してキャンペーンデータをインポートします。

### [!UICONTROL Select campaigns & ad groups]

**\[ インポートするデータ\]:** インポートするデータを指定します。

* *[!UICONTROL Import all new and existing campaigns]:* 既に存在するすべてのキャンペーンと存在しないキャンペーンのデータをインポートするには [!DNL Microsoft® Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* 特定のキャンペーンおよび広告グループを選択するには：

   * キャンペーンをその子広告グループに展開するには、 **[!UICONTROL >]** キャンペーン名の後に配置します。

   * キャンペーンまたは広告グループを選択するには、項目を選択してチェックマークを付けます。

   * キャンペーンまたは広告グループを削除するには：

      * Adobe Analytics の [!UICONTROL Campaigns] または [!UICONTROL Adgroups] 」列で、キャンペーンまたは広告グループの選択を解除して、チェックマークが消えるようにします。

      * Adobe Analytics の [!UICONTROL Selected] 列、クリック ![削除](/help/search-social-commerce/assets/delete.png "削除").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** インポートする項目、入札と予算、その他のオプションを指定できます。

**[!UICONTROL What to import]:** 読み込む項目を定義します。 項目カテゴリを読み込むためのオプションは、デフォルトで選択され、すべての項目タイプが選択されます。 特定の項目タイプのみを含めるには、 **[!UICONTROL Show advanced options]** をクリックし、含める項目タイプを変更します。

**[!UICONTROL Bids and budgets]:** 読み込む、更新する、およびカスタマイズする入札と予算の設定を定義します。

**[!UICONTROL Other options]:** インポートされたランディングページの URL、トラッキングテンプレート、およびその他のキャンペーン、広告、ターゲティングオプションの処理方法を定義します。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** 読み込みジョブの名前。

**[!UICONTROL When]:** 指定したキャンペーンをインポートするタイミング： *自動* ( [!DNL Microsoft® Advertising] キャンペーンを最適化するためのスケジュールを設定する )、 *[!UICONTROL Now]* （ジョブ設定を投稿する際にジョブを実行する場合） *[!UICONTROL Once]* 指定された時間に *[!UICONTROL Daily]* 指定された時間に *[!UICONTROL Weekly]* 指定した時刻に、または *[!UICONTROL Monthly]* 指定した時刻に。

**[!UICONTROL Receive email notifications]:** インポートジョブに関する電子メール通知を送信する場合とタイミングは、「レポート送信先」フィールドの電子メールアドレスに設定します。

**[!UICONTROL Send reports to]:** インポートジョブに関する通知を受け取る電子メールアドレス。 複数のアドレスを指定する場合はコンマ (`,`) をクリックします。
