---
title: ' [!DNL Google Ads] での [!DNL Microsoft Advertising] キャンペーンのレプリケート'
description: 同期されたキャンペーンを [!DNL Google Ads]  アカウントで同期された [!DNL Microsoft Advertising]  アカウントに直接書き出す方法について説明します。
exl-id: e7714d3d-4a8e-44ef-a3a7-e5198c091660
feature: Search Tools
TQID: https://experienceleague.adobe.com/l0yaZq0hmQSXXeJon22Fm8HOWJ6JDOaZuGqwxVfdw-c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 942
ht-degree: 0%

---

# [!DNL Google Ads]での[!DNL Microsoft Advertising] キャンペーンのレプリケート

同期したキャンペーンを[!DNL Google Ads] アカウントで直接、同期した[!DNL Microsoft Advertising] アカウントに拡張CPC （eCPC） キャンペーンとして書き出すことができます。 既存の入札額とキャンペーン予算が拡張されます。 既存の検索、ソーシャル、Commerce トラッキングは読み込まれません。

次の種類のキャンペーンとそのキャンペーン構造をレプリケートできます。

* [!DNL Google Ads]件の検索および表示キャンペーンを[!DNL Microsoft Advertising]件の検索および表示キャンペーンに追加しました。

* Microsoft Audience Networkの[!DNL Google Display Network]個のオーディエンスキャンペーンに、広告画像を含む[!DNL Microsoft Advertising]個のキャンペーンを追加しました。

  ショッピング フィード ベースの表示キャンペーンをレプリケートする場合は、まず[!DNL Google Merchant Center]製品オファーを[!DNL Microsoft Merchant Center]にレプリケートします。 キャンペーンをレプリケートする場合は、読み込みオプションで[!DNL Microsoft Merchant Center] ストアを選択して、ストアをフィードベースのオーディエンスキャンペーンにリンクします。

* ローカル広告在庫を含む[!DNL Google Ads]個のパフォーマンスの最大キャンペーンを[!DNL Microsoft Advertising]個のパフォーマンスの最大キャンペーンに追加します。

キャンペーンは、1回、毎週毎週または毎月更新するか、[!DNL Microsoft Advertising]の推奨スケジュールに従って更新することができます。 インポートジョブが実行されるたびに、またはエラーや変更が発生するたびに、オプションで通知を設定できます。 キャンペーンを[!DNL Microsoft Advertising]に読み込むと、読み込みジョブのステータスを確認したり、エラーログを確認したり、読み込みジョブを手動で実行したり、読み込みスケジュールを編集、一時停止、有効、削除したりできます。

すべてのキャンペーン情報がレプリケートされるわけではなく、[!DNL Microsoft Advertising] キャンペーンに一部の情報を追加する必要がある場合があります。 どのデータが読み込まれるかについて詳しくは、「[!DNL Microsoft Advertising]何が[ [!DNL Google Ads]から読み込まれるか」の](https://help.ads.microsoft.com/#apex/ads/en/50851) ヘルプを参照してください。 検索、ソーシャル、およびCommerce トラッキングは読み込まれないので、[account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、[ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)の設定でもトラッキングを追加する必要があります。

## [!DNL Google Ads]件のキャンペーンを複製

>[!NOTE]
>
>ショッピング フィード ベースの表示キャンペーンを複製する場合は、まず[で [!DNL Google Merchant Center] 製品オファーを [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870)に複製します。 キャンペーンをレプリケートする場合は、インポートオプションで[!DNL Microsoft Merchant Center] ストアを選択して、ストアをフィードベースのオーディエンスキャンペーンにリンクします。

[ キャンペーン  [!DNL Google Ads] からインポートされたものを](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500)確認してください。

1. Search, Social, &amp; Commerce メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. **[!UICONTROL +Import]**&#x200B;をクリックします。

1. [読み込み設定](#campaign-import-settings)を指定します。

   1. **[!UICONTROL Select accounts]** セクション：

      1. ソースアカウントと宛先アカウントを選択します。

      1. **[!UICONTROL Get Credential Id from MSA]**&#x200B;をクリックします。

      1. 宛先[!DNL Microsoft Advertising] アカウントにログインし、表示されている資格情報IDをコピーして、**[!UICONTROL Credential ID]** フィールドに値を貼り付けます。

   1. **[!UICONTROL Select campaigns & ad groups]** セクションで、読み込むキャンペーンと広告グループを指定します。

   1. 「**[!UICONTROL Customize your import]**」セクションで、読み込む項目タイプを指定します。

   1. **[!UICONTROL Set schedule]** セクションで、インポート ジョブを実行するタイミングを指定します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

1. （オプション）検索、ソーシャル、およびCommerce トラッキングを[account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、または[ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)の設定内に追加します。

## キャンペーン読み込みジョブのスケジュール設定の編集

[ キャンペーン  [!DNL Google Ads] からインポートされたものを](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500)確認してください。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. インポートジョブの横にあるチェックボックスを選択し、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. **[!UICONTROL Set schedule]** セクションで、[ スケジュール設定](#campaign-import-settings)を指定します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## キャンペーン読み込みジョブの表示

ソース [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、インポート時間またはスケジュール、ジョブを作成したユーザーなど、すべてのインポート ジョブを一覧表示できます。 定期的にスケジュールされたインポート中を含め、インポートジョブを複数回実行すると、各オカレンスは個別のジョブとしてリストされます。

* 次のいずれかの操作を行います。

   * メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

     デフォルトでは、ビューは[!UICONTROL List of Import Jobs] タブに開きます。

   * [[!UICONTROL Import Logs] タブ ](#campaign-import-log)から、「**[!UICONTROL List of Import Jobs]**」タブをクリックします。

## キャンペーン読み込みジョブの実行

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. 読み込みジョブの横にあるチェックボックスをオンにします。

1. 「![今すぐ実行](/help/search-social-commerce/assets/run.png "今すぐ実行")」をクリックします。

## キャンペーン読み込みジョブのログの表示 {#campaign-import-log}

開始時間、ソース [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、ジョブを作成したユーザー、成功および失敗した操作の数、各ジョブの通知を受信した電子メールアドレスなど、完了または失敗したすべてのインポートジョブを一覧表示できます。 アカウント内の各エンティティレベル（キャンペーンやキーワードなど）で追加、同期、削除されたアイテムの数、生成されたエラーなど、各ジョブで発生したターゲット [!DNL Microsoft Advertising] アカウントへの変更に関する詳細を表示できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Tools] >[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. 「**[!UICONTROL Import Logs]**」タブをクリックします。

1. （オプション）任意のインポート ジョブの詳細を表示するには、[!UICONTROL Summary]列の値をクリックします。

## Campaign インポートジョブ設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Source Google Ads account]:** キャンペーンデータの書き出し元となる同期済み[!DNL Google Ads] アカウント。

**[!UICONTROL Credential ID]:** [!DNL Microsoft Advertising]が[!DNL Google Ads]資格情報を表すために使用するID。

[!DNL Microsoft Advertising]個の制限があるため、インポート用の[!DNL Microsoft Advertising]資格情報の自動生成は使用できません。 Adobeのアカウントチームに連絡すると、チームが資格情報を生成し、IDを提供します。

**[!UICONTROL Target Microsoft Ads account]:** キャンペーンデータが読み込まれる同期[!DNL Microsoft Advertising] アカウント。

### [!UICONTROL Select campaigns & ad groups]

**\[読み込むデータ\]:**&#x200B;読み込むデータを指定：

* *[!UICONTROL Import all new and existing campaigns]:*&#x200B;既存のすべてのキャンペーンと[!DNL Microsoft Advertising]に存在しないキャンペーンのデータを読み込むには。

* *[!UICONTROL Import specific campaigns and adgroups]:*&#x200B;特定のキャンペーンと広告グループを選択します。

   * キャンペーンを子の広告グループに展開するには、キャンペーン名の後の&#x200B;**[!UICONTROL >]**&#x200B;をクリックします。

   * キャンペーンまたは広告グループを選択するには、チェックマークが表示されるようにアイテムを選択します。

   * キャンペーンまたは広告グループを削除するには：

      * [!UICONTROL Campaigns]または[!UICONTROL Adgroups]列で、チェックマークが消えるように、キャンペーンまたは広告グループの選択を解除します。

      * [!UICONTROL Selected]列で、![削除](/help/search-social-commerce/assets/delete.png "削除")をクリックします。

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:**&#x200B;読み込む内容、入札と予算、その他のオプションを指定できます。

**[!UICONTROL What to import]:**&#x200B;読み込む項目を定義します。 アイテムカテゴリを読み込むオプションは、デフォルトで選択されており、すべてのアイテムタイプが選択されています。 特定の項目タイプのみを含めるには、**[!UICONTROL Show advanced options]**&#x200B;をクリックし、含めるように項目タイプを変更します。

**[!UICONTROL Bids and budgets]:**&#x200B;読み込み、更新、カスタマイズする入札設定と予算設定を定義します。

**[!UICONTROL Other options]:**&#x200B;読み込まれたランディングページ URL、トラッキングテンプレート、その他のキャンペーン、広告、ターゲティングのオプションの処理方法を定義します。

### [!UICONTROL Set schedule]

**[!UICONTROL Import name]:** インポート ジョブの名前。

**[!UICONTROL When]:**&#x200B;指定したキャンペーンを読み込むタイミング：*自動* （[!DNL Microsoft Advertising]がキャンペーンを最適にスケジュールを設定できるようにする）、*[!UICONTROL Now]* （ジョブ設定を投稿する際にジョブを実行する）、*[!UICONTROL Once]*、指定した時間に&#x200B;*[!UICONTROL Daily]*、指定した時間に&#x200B;*[!UICONTROL Weekly]*、指定した時間に&#x200B;*[!UICONTROL Monthly]*。

**[!UICONTROL Receive email notifications]:** インポートジョブに関する電子メール通知を「レポートを送信」フィールドの電子メールアドレスに送信する場合とタイミング。

**[!UICONTROL Send reports to]:** インポート ジョブに関する通知を受信する電子メールアドレス。 複数のアドレスをコンマ （`,`）で区切ります。
