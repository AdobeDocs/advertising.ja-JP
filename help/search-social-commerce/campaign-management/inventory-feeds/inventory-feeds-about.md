---
title: 在庫フィードを利用した広告管理の自動化について
description: アカウント構造を自動的に管理し、商品やサービスの在庫に関するデータにもとづいて動的な広告を配信できる、高度なキャンペーン管理について解説します。
exl-id: 46e78f32-96ef-4a23-bbe3-f18b84309463
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/UqICY8g8nUAo4JSdAJ8h09P65nbe36aUYDEfOnBT9Jg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 838
ht-degree: 0%

---

# 在庫フィードを利用した広告管理の自動化について

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除操作のみ）、[!DNL Yandex] アカウントのみ*

高度なキャンペーン管理の[!UICONTROL Campaigns] > [!UICONTROL Advanced (ACM)] ビューを使用すると、製品またはサービスの在庫に関するデータに基づいて、広告ネットワーク アカウント構造を自動的に作成および更新し、動的な広告を配信できます。 製品データを含む新しいファイルを毎日または好きなだけ頻繁にアップロードするか、[!DNL Google]または[!DNL Microsoft]の加盟店センターのアカウントに直接リンクできます。 この機能を使用して、以下を行います。

* 順序付けられたデータソースから新しいキャンペーンを構築します。

* 変更可能なデータ要素（価格や数量など）に動的変数を使用することで、新しいデータが処理されるたびに、テキストおよびレスポンシブ検索広告、[!DNL Google Ads]個のショッピング広告、[!DNL Microsoft Advertising]個のショッピング広告を動的に更新します。 データを変更するたびに、既存の広告が削除され、新しい広告が作成されます。

* 指定された終了日に従って在庫が特定のレベルを下回った場合、またはフィードデータから既存のコンポーネントが除外された場合、広告グループ、キーワード、広告を自動的に一時停止または削除します。

広告を設定するには、変数（プレースホルダー）を含む在庫フィードテンプレートを作成し、アップロードされたファイルまたは[GoogleまたはMicrosoft merchant center アカウントの実際のデータ列で変数を置き換えます（](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)）。 変数には、ファイルまたはファイル内の個々の行に設定した修飾子グループを含めることもできます。これにより、データファイル内の該当する各行に複数の広告、キーワード、キャンペーン、広告グループを作成できます。 例えば、広告の見出しで修飾子グループ変数を使用し、修飾子グループに2つの修飾子が含まれている場合（安い場合、および「割引価格」）、製品ごとに2つの別々の広告が作成されます。各修飾子に1つずつ。 [!DNL Google Ads]および[!DNL Microsoft Advertising]の動的検索広告の場合は、広告カスタマイズの値を含めることもできます。

| テンプレートの[!UICONTROL Ad Variation] セクション | Search, Social, &amp; Commerceの修飾子 | フィード内容 | 成果となる広告 |
|----|----|----|----|
| タイトル：ハイエンドを購入\{<i>製品カテゴリ </i>\} &lt;<i>CheapList</i>><br><br>説明1: \{<i>製品名</i>\}の膨大な在庫。<br><br>説明2: \{<i>割引率</i>}%の割引で利用できます。 | 修飾子グループ「CheapList」の値：<br><br>&quot;for cheap&quot;<br><br>&quot;at a discount&quot; | 製品カテゴリ，製品名，割引率<br>電子機器，iPods,10<br><br> アパレル，シャツ，15<br><br><b>注：</b>値は、コンマまたはタブで区切ることができます。 | <u> ハイエンド電子機器を安く購入する。</u><br> タブレットの膨大な在庫。 10%割引でご利用いただけます。<br><br><u>高級エレクトロニクスを割引価格で購入します。</u><br> タブレットの膨大な在庫。 10%割引でご利用いただけます。<br><br><u>高級アパレルを安く購入する。</u><br> シャツの膨大な在庫。 15%の割引で利用可能。<br><br><u>高級アパレルを割引価格で購入する。</u><br> シャツの膨大な在庫。 15%の割引で利用可能。 |

広告を生成したら、オプションで広告をレビューし、広告ネットワークに投稿できます。

>[!NOTE]
>スプレッドシート ファイルを使用してキャンペーンデータを一括で作成または編集するには、「[&#x200B; バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)」を参照してください。

## 在庫フィードを使用したキャンペーンデータ管理のワークフロー

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除操作のみ）、[!DNL Yandex] アカウントのみ*

最初に、少なくとも1つのフィードファイルまたはアカウントをテストし、プロセスを完全に自動化するか、各ステップで引き続き制御できます。

1. （オプション）Adobe アカウントチームに連絡して、データファイルをデポジットするためのFTP ディレクトリを設定します。

   FTP ディレクトリを使用する場合、フィードサービスは2時間ごとに新しいファイルをチェックします。

   それ以外の場合は、[!UICONTROL Advanced (ACM)] ビューでファイルを手動でアップロードできます。

1. フィード データを処理するための[&#x200B; パラメーター](feed-settings-manage.md#feed-data-settings)を設定します。

   FTPを使用している場合は、最初に広告ネットワークにデータを自動的に投稿しないでください。 最初のファイルの出力を確認し、結果に満足したら、設定を変更できます。

1. FTP ディレクトリにデータファイルをアップロードするか、[手動で](feed-files-manage.md)にデータファイル [!UICONTROL Advanced (ACM) view]をアップロードするか、[GoogleまたはMicrosoft merchant center アカウントへのアクセスを有効にします](/help/search-social-commerce/campaign-management/accounts/merchant-account-manage.md)。

ファイルを手動でアップロードするには、データファイルを使用するテンプレートを作成するまで待ちます。

1. （オプション）フィード データ テンプレートの様々なデータ フィールドで変数として使用する[修飾子](modifiers-manage.md)のグループを作成します。

1. [&#x200B; データ列を使用して、特定の広告ネットワークアカウントのキャンペーン、広告グループ、キーワード、広告コピーを作成する1つ以上のテンプレート &#x200B;](ad-templates/ad-template-manage.md)を作成します。

1. [&#x200B; テンプレート &#x200B;](feed-data-propagate.md)を通じてフィード データを伝達します。テンプレート内の列名をファイルまたはアカウント内のデータで置き換えます。 Search, Social, &amp; Commerceでは、テンプレートオプションに応じて、デフォルト設定を使用して広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成するか、広告を既存のアカウント構造にマッピングします。

1. （オプション） [出力](propagated-data-view.md)を[!UICONTROL Advanced (ACM)] ビューでプレビューし、オプションで[!UICONTROL Propagations] タブのデータ変更の概要を表示します。

1. [関連する広告ネットワーク アカウントにデータ &#x200B;](propagated-data-post.md)を投稿します。

1. （FTPまたはマーチャント センターのアカウントを使用してデータをアップロードする場合。オプション）最初のフィード ファイルからの出力を検証した後、[&#x200B; パラメーター](feed-settings-manage.md#feed-data-settings)を編集して、関連するテンプレートを介して後続のデータを自動的に伝播し、関連する広告ネットワークに投稿します。

1. （新しいデータファイルがある場合）必要に応じて、新しいファイルをアップロードし、テンプレートを通じてデータを伝搬し、関連する広告ネットワークにデータを投稿します。 必要に応じて、データを1つの手順で伝達および投稿できます。

>[!MORELIKETHIS]
>
>* [在庫フィードでアカウントコンポーネントを作成または削除するタイミング？](when-are-components-created-deleted.md)
