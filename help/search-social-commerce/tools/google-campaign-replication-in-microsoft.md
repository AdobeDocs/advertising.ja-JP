---
title: Replicate [!DNL Google Ads] のキャンペーン [!DNL Microsoft Advertising]
description: で同期したキャンペーンをエクスポートする方法を説明します [!DNL Google Ads] 同期されたに直接反映 [!DNL Microsoft Advertising] アカウント。
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# Replicate [!DNL Google Ads] のキャンペーン [!DNL Microsoft Advertising]

同期したキャンペーンはにエクスポートできます [!DNL Google Ads] 同期されたに直接反映 [!DNL Microsoft Advertising] 拡張 CPC （eCPC）キャンペーンとしてアカウントします。 既存の入札とキャンペーン予算は拡大・縮小されます。 既存の検索、ソーシャル、Commerceのトラッキングは読み込まれません。

次のタイプのキャンペーンとそのキャンペーン構造をレプリケートできます。

* [!DNL Google Ads] キャンペーンの検索と表示： [!DNL Microsoft Advertising] キャンペーンを検索および表示します。

* [!DNL Google Display Network] キャンペーン（広告画像を含む） [!DNL Microsoft Advertising] Microsoft Audience Network のオーディエンスキャンペーン。

  ショッピングフィードベースのディスプレイキャンペーンをレプリケートする場合は、最初にをレプリケートします [!DNL Google Merchant Center] 製品オファー先 [!DNL Microsoft Merchant Center]. キャンペーンをレプリケートする際に、 [!DNL Microsoft Merchant Center] 読み込みオプションに保存して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

* [!DNL Google Ads] へのローカル在庫広告を含むパフォーマンス最大キャンペーン数 [!DNL Microsoft Advertising] パフォーマンス最大キャンペーン数。

キャンペーンの更新を 1 回、毎日、毎週、毎月、または次のように選択できます [!DNL Microsoft Advertising]の推奨スケジュールです。 オプションで、インポートジョブが実行されるたびに、またはエラーや変更が発生した場合に、通知を設定できます。 キャンペーンをにインポートした後 [!DNL Microsoft Advertising]を使用すると、インポートジョブのステータスの確認、エラーログの確認、インポートジョブの手動実行、インポートスケジュールの編集、一時停止、有効化または削除を行うことができます。

キャンペーン情報の一部はレプリケートされないので、に情報を追加する必要がある場合があります [!DNL Microsoft Advertising] キャンペーン。 インポートされるデータの詳細については、を参照してください。 [!DNL Microsoft Advertising] のヘルプ &quot;[から読み込むもの [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851).」と入力します。 検索、ソーシャル、Commerceのトラッキングはインポートされないので、内にトラッキングを追加する必要もあります [アカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [広告グループ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、または [広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## Replicate [!DNL Google Ads] キャンペーン

>[!NOTE]
>
>ショッピングフィードベースのディスプレイキャンペーンをレプリケートする場合は、最初に [をレプリケート [!DNL Google Merchant Center] での製品オファー [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870). キャンペーンをレプリケートする際に、 [!DNL Microsoft Merchant Center] インポートオプションに保存して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

参照： [からのインポート [!DNL Google Ads] キャンペーン](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. 検索、ソーシャル、Commerceのメインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. クリック **[!UICONTROL +Import]**.

1. を指定 [設定を読み込み](#campaign-import-settings):

   1. が含まれる **[!UICONTROL Select accounts]** セクション：

      1. ソースおよび宛先アカウントを選択します。

      1. クリック **[!UICONTROL Get Credential Id from MSA]**.

      1. 宛先にログインします [!DNL Microsoft Advertising] に入力し、表示された資格情報 ID をコピーし、値を **[!UICONTROL Credential ID]** フィールド。

   1. が含まれる **[!UICONTROL Select campaigns & ad groups]** セクションで、インポートするキャンペーンと広告グループを指定します。

   1. が含まれる **[!UICONTROL Customize your import]** セクションで、インポートするアイテムの種類を指定します。

   1. が含まれる **[!UICONTROL Set schedule]** セクションで、インポート ジョブを実行するタイミングを指定します。

1. クリック **[!UICONTROL Post]**.

1. （オプション）内に検索、ソーシャル、Commerceのトラッキングを追加します [アカウント](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md), [campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md), [広告グループ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、または [広告](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) 設定。

## キャンペーンインポートジョブのスケジュール設定の編集

参照： [からのインポート [!DNL Google Ads] キャンペーン](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. インポート ジョブの横にあるチェック ボックスをオンにし、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. が含まれる **[!UICONTROL Set schedule]** セクションで、 [スケジュール設定](#campaign-import-settings).

1. クリック **[!UICONTROL Post]**.

## キャンペーンインポートジョブの表示

ソースを含むすべてのインポートジョブをリストできます [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、読み込み時間またはスケジュール、ジョブを作成したユーザー。 インポートジョブを（定期的にスケジュールされたインポートの実行中を含めて）複数回実行した場合、各発生が個別のジョブとしてリストされます。

* 次のいずれかの操作をおこないます。

   * メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

     デフォルトでは、ビューは次の項目に開きます [!UICONTROL List of Import Jobs] タブ。

   * から [[!UICONTROL Import Logs] タブ](#campaign-import-log)を選択し、 **[!UICONTROL List of Import Jobs]** タブ。

## キャンペーンインポートジョブの実行

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. インポートジョブの横にあるチェックボックスをオンにします。

1. クリック ![今すぐ実行](/help/search-social-commerce/assets/run.png "今すぐ実行").

## キャンペーンインポートジョブのログを表示 {#campaign-import-log}

開始時間、ソースを含む、完了または失敗したすべてのインポートジョブをリストできます [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、ジョブを作成したユーザー、成功および失敗した操作の数、各ジョブの通知を受信したメールアドレス。 ターゲットに対する変更に関する詳細を表示できます [!DNL Microsoft Advertising] 各ジョブで発生したアカウント（追加、同期、削除された項目の数、アカウントの各エンティティレベル（キャンペーンやキーワードなど）でエラーが発生した数など）。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**.

1. 「」をクリックします **[!UICONTROL Import Logs]** タブ。

1. （任意）任意の読み込みジョブの詳細を表示するには、にある値をクリックします [!UICONTROL Summary] 列。

## Campaign インポートジョブの設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** 同期された [!DNL Google Ads] キャンペーンデータの書き出し元のアカウント。

**[!UICONTROL Credential ID]:** ID: [!DNL Microsoft Advertising] を使用してを表す [!DNL Google Ads] 資格情報。

自動生成 [!DNL Microsoft Advertising] 次の理由により、読み込みの資格情報を使用できません： [!DNL Microsoft Advertising] 制限事項 Adobeアカウントチームに問い合わせると、チームが資格情報を生成し、ID を提供します。

**[!UICONTROL Target Microsoft Ads account]:** 同期された [!DNL Microsoft Advertising] キャンペーンデータのインポート先となるアカウント。

### [!UICONTROL Select campaigns & ad groups]

**\[ インポートするデータ\]:** インポートするデータを指定してください：

* *[!UICONTROL Import all new and existing campaigns]:* 既に存在するすべてのキャンペーンと存在しないキャンペーンのデータをインポートする場合 [!DNL Microsoft Advertising].

* *[!UICONTROL Import specific campaigns and adgroups]:* 特定のキャンペーンおよび広告グループを選択します。

   * キャンペーンをその子広告グループに展開するには、をクリックします **[!UICONTROL >]** キャンペーン名の後に。

   * キャンペーンまたは広告グループを選択するには、項目を選択してチェックマークを表示します。

   * キャンペーンまたは広告グループを削除するには：

      * が含まれる [!UICONTROL Campaigns] または [!UICONTROL Adgroups] 列で、キャンペーンまたは広告グループの選択を解除して、チェックマークが表示されないようにします。

      * が含まれる [!UICONTROL Selected] 列、クリック ![削除](/help/search-social-commerce/assets/delete.png "削除").

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** インポートするもの、入札と予算、その他のオプションを指定できます。

**[!UICONTROL What to import]:** インポートする項目を定義します。 既定では、アイテム カテゴリをインポートするオプションが選択され、すべてのアイテム タイプが選択されます。 特定の項目タイプのみを含めるには、 **[!UICONTROL Show advanced options]** さらに、含める項目の種類を変更します。

**[!UICONTROL Bids and budgets]:** インポート、更新、カスタマイズする入札設定と予算設定を定義します。

**[!UICONTROL Other options]:** 読み込んだランディングページ URL、トラッキングテンプレート、その他のキャンペーン、広告、ターゲティングオプションの処理方法を定義します。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** インポートジョブの名前。

**[!UICONTROL When]:** 指定したキャンペーンをインポートするタイミング： *自動* （許可する [!DNL Microsoft Advertising] キャンペーンを最適に最適化するためのスケジュールを設定）、 *[!UICONTROL Now]* （ジョブ設定をポストするときにジョブを実行するには）、 *[!UICONTROL Once]* 指定した時間、 *[!UICONTROL Daily]* 指定した時間、 *[!UICONTROL Weekly]* 指定した時間、または *[!UICONTROL Monthly]* 指定した時間に。

**[!UICONTROL Receive email notifications]:** インポートジョブに関するメール通知を送信する場合およびタイミングは、「レポートの送信先」フィールドのメールアドレスにします。

**[!UICONTROL Send reports to]:** 読み込みジョブに関する通知を受信するメールアドレス。 複数のアドレスをコンマで区切ります（`,`）に設定します。
