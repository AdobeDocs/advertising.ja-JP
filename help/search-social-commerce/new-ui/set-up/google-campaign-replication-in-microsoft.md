---
title: （新しいUI） Microsoft AdvertisingでのGoogle Ads キャンペーンのレプリケート
description: Google Ads アカウント内の同期済みキャンペーンを、同期済みMicrosoft Advertising アカウントに直接書き出す方法について説明します。
feature: Search Campaign Management
exl-id: d4f8e452-7b3d-4a1f-9c3e-6b8d2e5a4917
source-git-commit: 3f769f18ce006278b12a62f8d837d60affffda65
workflow-type: tm+mt
source-wordcount: '1047'
ht-degree: 0%

---

# （新しいUI） [!DNL Google Ads]件のキャンペーンを[!DNL Microsoft Advertising]にレプリケート

*Beta機能*

同期したキャンペーンを[!DNL Google Ads] アカウントで直接、同期した[!DNL Microsoft Advertising] アカウントに拡張CPC （eCPC） キャンペーンとして書き出すことができます。 既存の入札額とキャンペーン予算が拡張されます。 既存の検索、ソーシャル、Commerce トラッキングは読み込まれません。

次の種類のキャンペーンとそのキャンペーン構造をレプリケートできます。

* [!DNL Google Ads]件の検索および表示キャンペーンを[!DNL Microsoft Advertising]件の検索および表示キャンペーンに追加しました。

* Microsoft Audience Networkの[!DNL Microsoft Advertising]個のオーディエンスキャンペーンに、広告画像を含む[!DNL Google Display Network]個のキャンペーンを追加しました。

  ショッピング フィード ベースの表示キャンペーンをレプリケートする場合は、まず[!DNL Google Merchant Center]製品オファーを[!DNL Microsoft Merchant Center]にレプリケートします。 キャンペーンをレプリケートする場合は、インポートオプションで[!DNL Microsoft Merchant Center] ストアを選択して、ストアをフィードベースのオーディエンスキャンペーンにリンクします。

* ローカル広告在庫を含む[!DNL Google Ads]個のパフォーマンスの最大キャンペーンを[!DNL Microsoft Advertising]個のパフォーマンスの最大キャンペーンに追加します。

キャンペーンを1回、日単位、週単位、月単位で更新するか、[!DNL Microsoft Advertising]の推奨スケジュールに従って更新するかを選択できます。 インポートジョブが実行されるたびに、またはエラーや変更が発生するたびに、オプションで通知を設定できます。 キャンペーンを[!DNL Microsoft Advertising]に読み込むと、読み込みジョブのステータスを確認したり、エラーログを確認したり、読み込みジョブを手動で実行したり、読み込みスケジュールを編集、一時停止、有効、削除したりできます。

すべてのキャンペーン情報がレプリケートされるわけではなく、[!DNL Microsoft Advertising] キャンペーンに一部の情報を追加する必要がある場合があります。 どのデータが読み込まれるかについて詳しくは、「[何が [!DNL Google Ads]](https://help.ads.microsoft.com/#apex/ads/en/50851){target="_blank"}から読み込まれるか」の[!DNL Microsoft Advertising] ヘルプを参照してください。 検索、ソーシャル、およびCommerce トラッキングは読み込まれないので、[account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、[ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)の設定でもトラッキングを追加する必要があります。

## [!DNL Google Ads]件のキャンペーンを複製

>[!NOTE]
>
>ショッピング フィード ベースの表示キャンペーンを複製する場合は、まず[で [!DNL Google Merchant Center] 製品オファーを [!DNL Microsoft Merchant Center]](https://help.ads.microsoft.com/apex/index/3/en/56870){target="_blank"}に複製します。 キャンペーンをレプリケートする場合は、インポートオプションで[!DNL Microsoft Merchant Center] ストアを選択して、ストアをフィードベースのオーディエンスキャンペーンにリンクします。

 [!DNL Google Ads]  キャンペーン [&#128279;](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}からインポートされたものを確認してください。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. [読み込み設定](#campaign-import-settings)を指定します。

   1. **[!UICONTROL Select accounts]** ステップで：

      1. インポート ジョブの名前を&#x200B;**[!UICONTROL Import Name]** フィールドに入力します。

      1. ソース [!DNL Google Ads] アカウントとターゲット [!DNL Microsoft Advertising] アカウントを選択します。

      1. **[!UICONTROL Credential ID]**&#x200B;を入力します。 資格情報IDをお持ちでない場合は、Adobe アカウントチームにお問い合わせください（[!DNL Microsoft Advertising]の制限により、自動生成は利用できません）。

      1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. **[!UICONTROL Select campaigns & ad groups]** ステップで、読み込むキャンペーンと広告グループを指定し、**[!UICONTROL Next]**&#x200B;をクリックします。

   1. **[!UICONTROL Customize your import]** ステップで、必要に応じてアイテムの種類、入札設定および予算設定、およびその他の読み込みオプションを指定し、**[!UICONTROL Next]**&#x200B;をクリックします。

   1. **[!UICONTROL Set schedule]** ステップで、インポートジョブを実行するタイミングと通知の受信方法を指定します。

1. 概要で選択内容を確認し、**[!UICONTROL Start Import]**&#x200B;をクリックします。

1. （オプション）検索、ソーシャル、およびCommerce トラッキングを[account](/help/search-social-commerce/campaign-management/accounts/ad-network-account-manage.md)、[campaign](/help/search-social-commerce/campaign-management/campaigns/campaign-manage.md)、[ad group](/help/search-social-commerce/campaign-management/campaigns/ad-group-manage.md)、または[ad](/help/search-social-commerce/campaign-management/campaigns/ad-manage.md)の設定内に追加します。

## キャンペーン読み込みジョブのスケジュール設定の編集

 [!DNL Google Ads]  キャンペーン [&#128279;](https://help.ads.microsoft.com/#apex/ads/en/50851/0-500){target="_blank"}からインポートされたものを確認してください。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. 「**[!UICONTROL Jobs]**」タブをクリックします。

1. 読み込みジョブの名前をクリックし、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. **[!UICONTROL Set schedule]** ステップで、[&#x200B; スケジュール設定](#campaign-import-settings)を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

## キャンペーン読み込みジョブの表示

ソース [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、インポート時間またはスケジュール、ジョブを作成したユーザーなど、すべてのインポート ジョブを一覧表示できます。 定期的にスケジュールされたインポート中を含め、インポートジョブを複数回実行すると、各オカレンスは個別のジョブとしてリストされます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

   ビューはデフォルトで&#x200B;**[!UICONTROL Jobs]** タブに開きます。

## キャンペーン読み込みジョブの実行

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. 「**[!UICONTROL Jobs]**」タブをクリックします。

1. 読み込みジョブの横にあるチェックボックスを選択し、**[!UICONTROL Run Now]**&#x200B;をクリックします。

## キャンペーン読み込みジョブのログの表示 {#campaign-import-log}

開始時間、ソース [!DNL Google Ads] アカウント、ターゲット [!DNL Microsoft Advertising] アカウント、ジョブを作成したユーザー、成功および失敗した操作の数、各ジョブの通知を受信した電子メールアドレスなど、完了または失敗したすべてのインポートジョブを一覧表示できます。 アカウント内の各エンティティレベル（キャンペーンやキーワードなど）で追加、同期、削除されたアイテムの数、生成されたエラーなど、各ジョブで発生したターゲット [!DNL Microsoft Advertising] アカウントへの変更に関する詳細を表示できます。

1. メインメニューで、**[!UICONTROL Setup]** \> **[!UICONTROL Import Campaigns]**&#x200B;をクリックします。

1. 「**[!UICONTROL Logs]**」タブをクリックします。

1. （オプション）任意のインポート ジョブの詳細を表示するには、[!UICONTROL Summary]列の値をクリックします。

## Campaign インポートジョブ設定 {#campaign-import-settings}

### [!UICONTROL Select accounts]

**[!UICONTROL Import Name]:**&#x200B;読み込みジョブを識別する名前。

**[!UICONTROL Source Google Ads account]:** キャンペーンデータの書き出し元となる同期済み[!DNL Google Ads] アカウント。

**[!UICONTROL Target Microsoft Ads account]:** キャンペーンデータが読み込まれる同期[!DNL Microsoft Advertising] アカウント。

**[!UICONTROL Credential ID]:** [!DNL Microsoft Advertising]が[!DNL Google Ads]資格情報を表すために使用するID。 [!DNL Microsoft Advertising]個の制限があるため、インポート用の[!DNL Microsoft Advertising]資格情報の自動生成は使用できません。 Adobeのアカウントチームに連絡すると、チームが資格情報を生成し、IDを提供します。

### [!UICONTROL Select campaigns & ad groups]

**\[ インポートするデータ\]:** インポートするデータ：

* *[!UICONTROL Import all new and existing campaigns]:*&#x200B;既存のすべてのキャンペーンと[!DNL Microsoft Advertising]に存在しないキャンペーンのデータを読み込むには。

* *[!UICONTROL Import specific campaigns and adgroups]:*&#x200B;特定のキャンペーンと広告グループを選択します。

   * キャンペーンを子の広告グループに展開するには、キャンペーン名の後の&#x200B;**[!UICONTROL >]**&#x200B;をクリックします。

   * キャンペーンまたは広告グループを選択するには、チェックマークが表示されるようにアイテムを選択します。

   * キャンペーンまたは広告グループを削除するには、項目の選択を解除するか、[!UICONTROL Selected]列の削除アイコンをクリックします。

### [!UICONTROL Customize your import]

**[!UICONTROL Choose specific import options]:**&#x200B;読み込む内容、入札と予算、その他のオプションを指定できます。

**[!UICONTROL What to import]:**&#x200B;読み込む項目を定義します。 アイテムカテゴリを読み込むオプションは、デフォルトで選択され、すべてのアイテムタイプが選択されています。 特定の項目タイプのみを含めるには、**[!UICONTROL Show advanced options]**&#x200B;をクリックし、含めるように項目タイプを変更します。 オプションで、UET タグ IDを、以前に[!DNL Microsoft Advertising]に読み込まれていないリマーケティングリストまたはオーディエンスに関連付けることもできます。

**[!UICONTROL Bids and budgets]:**&#x200B;読み込み、更新、カスタマイズする入札設定と予算設定を定義します。これには、[!DNL Microsoft Advertising]に対して指定した割合で入札額と予算を増減するオプションが含まれます。

**[!UICONTROL Other options]:**&#x200B;読み込まれたランディングページ URL、トラッキングテンプレート、その他のキャンペーン、広告、ターゲット設定の処理方法を定義します。これには、テキストを検索して置換したり、サフィックスを挿入したりするオプションが含まれます。

### [!UICONTROL Set schedule]

**[!UICONTROL When]:**&#x200B;指定したキャンペーンを読み込むタイミング：*自動* （[!DNL Microsoft Advertising]がキャンペーンを最適にスケジュールを設定できるようにする）、*[!UICONTROL Now]* （ジョブ設定を投稿する際にジョブを実行する）、*[!UICONTROL Once]*、指定した時間に&#x200B;*[!UICONTROL Daily]*、指定した時間に&#x200B;*[!UICONTROL Weekly]*、指定した時間に&#x200B;*[!UICONTROL Monthly]*。

**[!UICONTROL Receive email notifications]:** インポート ジョブに関するメール通知を[!UICONTROL Send reports to] フィールドのアドレスに送信するかどうか、タイミング：*[!UICONTROL No emails]*、*[!UICONTROL Only if there are changes or errors]* （既定値）、*[!UICONTROL Only if there are errors]*、または&#x200B;*[!UICONTROL Every time this import runs]*。

**[!UICONTROL Send reports to]:** インポート ジョブに関する通知を受信する電子メールアドレス。 複数のアドレスをコンマ （`,`）で区切ります。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)
