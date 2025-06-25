---
title: ' [!DNL Microsoft Advertising] でキャンペーン  [!DNL Google Ads]  レプリケート'
description: アカウント内の同期されたキャンペーンを同期された  [!DNL Google Ads]  カウントに直接エクスポートする方法を説明  [!DNL Microsoft Advertising]  ます。
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '942'
ht-degree: 0%

---

# [!DNL Microsoft Advertising] で [!DNL Google Ads] キャンペーンをレプリケート

[!DNL Google Ads] アカウントの同期されたキャンペーンを、拡張 CPC （eCPC）キャンペーンとして、同期された [!DNL Microsoft Advertising] アカウントに直接エクスポートできます。 既存の入札とキャンペーン予算は拡大・縮小されます。 既存の検索、ソーシャル、Commerceのトラッキングは読み込まれません。

次のタイプのキャンペーンとそのキャンペーン構造をレプリケートできます。

* 検索キャンペーンと表示キャンペーンを [!DNL Microsoft Advertising] の検索キャンペーンと表示キャンペーンに [!DNL Google Ads] り込みます。

* キャンペーン（広告画像を含む）をMicrosoft Audience Network 上 [!DNL Microsoft Advertising] オーディエンスキャンペーンに [!DNL Google Display Network] り込みます。

  ショッピングフィードベースのディスプレイキャンペーンをレプリケートする場合は、最初に [!DNL Google Merchant Center] の製品オファーを [!DNL Microsoft Merchant Center] にレプリケートします。 キャンペーンをレプリケートする際に、インポートオプションの [!DNL Microsoft Merchant Center] ストアを選択して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

* パフォーマンス最大キャンペーン（ローカル在庫広告を含む）をパフォーマンス最大キャンペーン [!DNL Microsoft Advertising] 一 [!DNL Google Ads] します。

キャンペーンの更新は、1 回、毎日、毎週、毎月、または [!DNL Microsoft Advertising] の推奨スケジュールに従って選択できます。 オプションで、インポートジョブが実行されるたびに、またはエラーや変更が発生した場合に、通知を設定できます。 キャンペーンを [!DNL Microsoft Advertising] にインポートすると、インポートジョブのステータスの確認、エラーログの確認、インポートジョブの手動実行、インポートスケジュールの編集、一時停止、有効化または削除ができます。

すべてのキャンペーン情報がレプリケートされるわけではなく、[!DNL Microsoft Advertising] キャンペーンに情報を追加する必要が生じる場合があります。 どのデータがインポートされるかについての詳細は、ヘルプ [!DNL Microsoft Advertising] 「[ からインポートされるもの  [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851) を参照してください。 検索、ソーシャル、Commerceのトラッキングは読み込まれないので、[account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md) または [ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md) の設定内にトラッキングを追加する必要もあります。

## キャンペーン [!DNL Google Ads] レプリケート

>[!NOTE]
>
>ショッピングフィードベースのディスプレイキャンペーンをレプリケートする場合は、最初に [ 製品オファーを  [!DNL Google Merchant Center]  レプリケート  [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870) します。 キャンペーンをレプリケートする際に、インポートオプションの [!DNL Microsoft Merchant Center] ストアを選択して、フィードベースのオーディエンスキャンペーンにストアをリンクします。

[campaigns からのインポート内容 ](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) を参照  [!DNL Google Ads]  てください。

1. 検索、ソーシャル、Commerceのメインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Import Campaigns]** をクリックします。

1. 「**[!UICONTROL +Import]**」をクリックします。

1. [ 読み込み設定 ](#campaign-import-settings) を指定します。

   1. **[!UICONTROL Select accounts]** のセクションで以下を実行します。

      1. ソースおよび宛先アカウントを選択します。

      1. 「**[!UICONTROL Get Credential Id from MSA]**」をクリックします。

      1. 宛先 [!DNL Microsoft Advertising] アカウントにログインし、表示された資格情報 ID をコピーして、「**[!UICONTROL Credential ID]**」フィールドに値を貼り付けます。

   1. **[!UICONTROL Select campaigns & ad groups]** セクションで、インポートするキャンペーンと広告グループを指定します。

   1. **[!UICONTROL Customize your import]** セクションで、インポートするアイテムの種類を指定します。

   1. **[!UICONTROL Set schedule]** セクションで、インポート ジョブを実行するタイミングを指定します。

1. 「**[!UICONTROL Post]**」をクリックします。

1. （任意）「[ アカウント ](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)」、「[ キャンペーン ](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)」、「[ 広告グループ ](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)」または「[ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)」設定内に、検索、ソーシャル、Commerceのトラッキングを追加します。

## キャンペーンインポートジョブのスケジュール設定の編集

[campaigns からのインポート内容 ](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500) を参照  [!DNL Google Ads]  てください。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Import Campaigns]** をクリックします。

1. 読み込みジョブの横にあるチェックボックスを選択し、「![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")」をクリックします。

1. **[!UICONTROL Set schedule]** セクションで、[ スケジュール設定 ](#campaign-import-settings) を指定します。

1. 「**[!UICONTROL Post]**」をクリックします。

## キャンペーンインポートジョブの表示

ソースの [!DNL Google Ads] アカウント、ターゲットの [!DNL Microsoft Advertising] アカウント、読み込み時間またはスケジュール、ジョブを作成したユーザーなど、すべての読み込みジョブをリストできます。 インポートジョブを（定期的にスケジュールされたインポートの実行中を含めて）複数回実行した場合、各発生が個別のジョブとしてリストされます。

* 次のいずれかの操作をおこないます。

   * メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Import Campaigns]** をクリックします。

     デフォルトでは、ビューは「[!UICONTROL List of Import Jobs]」タブに開きます。

   * 「[[!UICONTROL Import Logs]」タブで ](#campaign-import-log) 「**[!UICONTROL List of Import Jobs]**」タブをクリックします。

## キャンペーンインポートジョブの実行

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Import Campaigns]** をクリックします。

1. インポートジョブの横にあるチェックボックスをオンにします。

1. ![ 今すぐ実行 ](/help/search-social-commerce/assets/run.png " 今すぐ実行 ") をクリックします。

## キャンペーンインポートジョブのログを表示 {#campaign-import-log}

開始時間、ソース・[!DNL Google Ads] ーザー・アカウント、ターゲット・[!DNL Microsoft Advertising] ーザー・アカウント、ジョブの作成者、操作の成功数と失敗数、各ジョブの通知を受信した電子メール・アドレスなど、完了または失敗したすべてのインポート・ジョブをリストできます。 追加、同期、削除された項目の数、アカウントの各エンティティレベル（キャンペーンやキーワードなど）でエラーが発生した数など、各ジョブで発生したターゲット [!DNL Microsoft Advertising] アカウントへの変更に関する詳細を表示できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Import Campaigns]** をクリックします。

1. 「**[!UICONTROL Import Logs]**」タブをクリックします。

1. （任意）インポートジョブの詳細を表示するには、[!UICONTROL Summary] 列の値をクリックします。

## Campaign インポートジョブの設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** キャンペーンデータのエクスポート元となる同期された [!DNL Google Ads] アカウント。

**[!UICONTROL Credential ID]:** [!DNL Google Ads] 資格情報を表 [!DNL Microsoft Advertising] ために使用する ID。

[!DNL Microsoft Advertising] の制限 [!DNL Microsoft Advertising] より、インポート用の資格情報を自動生成できません。 Adobe アカウントチームに連絡すると、チームは資格情報を生成し、ID を提供します。

**[!UICONTROL Target Microsoft Ads account]:** キャンペーンデータのインポート先となる同期された [!DNL Microsoft Advertising] アカウント。

### [!UICONTROL Select campaigns & ad groups]

**\[ インポートするデータ\]:** インポートするデータを指定してください：

* *[!UICONTROL Import all new and existing campaigns]:* 既に存在するすべてのキャンペーンと [!DNL Microsoft Advertising] に存在しないキャンペーンのデータをインポートします。

* *[!UICONTROL Import specific campaigns and adgroups]:* 特定のキャンペーンおよび広告グループを選択します。

   * キャンペーンをその子広告グループに展開するには、キャンペーン名の後の **[!UICONTROL >]** をクリックします。

   * キャンペーンまたは広告グループを選択するには、項目を選択してチェックマークを表示します。

   * キャンペーンまたは広告グループを削除するには：

      * [!UICONTROL Campaigns] または [!UICONTROL Adgroups] 列で、キャンペーンまたは広告グループの選択を解除して、チェックマークが表示されないようにします。

      * [!UICONTROL Selected] 列で、「![ 削除 ](/help/search-social-commerce/assets/delete.png " 削除 ")」をクリックします。

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:** インポートするもの、入札と予算、その他のオプションを指定できます。

**[!UICONTROL What to import]:** インポートする項目を定義します。 既定では、アイテム カテゴリをインポートするオプションが選択され、すべてのアイテム タイプが選択されます。 特定のアイテム タイプのみを含めるには、[**[!UICONTROL Show advanced options]**] をクリックし、含めるアイテム タイプを変更します。

**[!UICONTROL Bids and budgets]:** インポート、更新、およびカスタマイズする入札設定および予算設定を定義します。

**[!UICONTROL Other options]:** 読み込んだランディングページの URL、トラッキングテンプレート、その他のキャンペーン、広告、ターゲティングオプションの処理方法を定義します。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** インポートジョブの名前。

**[!UICONTROL When]:** 指定したキャンペーンをインポートするタイミング。*自動* （[!DNL Microsoft Advertising] がキャンペーンを最適に最適化するスケジュールを設定する）、*[!UICONTROL Now]* （ジョブ設定を投稿したときにジョブを実行する）、指定した時間に *[!UICONTROL Once]*、指定した時間に *[!UICONTROL Daily]*、*[!UICONTROL Weekly]*、指定した時間に *[!UICONTROL Monthly]*、または指定した時間に実行します。

**[!UICONTROL Receive email notifications]:** 読み込みジョブに関するメール通知を「レポートの送信先」フィールドのメールアドレスに送信するかどうか、およびそのタイミング。

**[!UICONTROL Send reports to]:** 読み込みジョブに関する通知を受信するメールアドレス。 複数のアドレスをコンマで区切ります（`,`）。
