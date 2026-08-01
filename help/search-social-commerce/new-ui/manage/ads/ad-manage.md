---
title: 広告を管理
description: 利用可能な広告タイプなど、広告の作成および管理方法について説明します。
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 6a479ae0bb30d609b16a343efcec296137b9ab43
workflow-type: tm+mt
source-wordcount: 1733
ht-degree: 0%

---

# 広告を管理

*Beta機能*

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]および既存の[!DNL Baidu] アカウントのみ*

広告は広告グループに属し、広告ネットワークと広告の種類に応じて、見出し、説明、画像、その他のクリエイティブ要素など、ユーザーに表示されるコンテンツを含みます。

[API接続を介して広告ネットワークアカウントにアクセスできるようにし](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/api-account-manage.md)、Search, Social, &amp; Commerceがアカウントデータを広告ネットワークと同期したら、[ サポートされているキャンペーンタイプ ](/help/search-social-commerce/introduction/supported-inventory.md)の広告を作成できます。 また、広告のステータスを編集および変更することもできます。

各広告ネットワークで使用できる機能について詳しくは、「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。

## [!UICONTROL Ads] ビューについて {#ad-view-about}

[!UICONTROL Manage] > [!UICONTROL Ads] ビューには、選択した広告主アカウントのフィルター処理されたビュー内のすべての広告が一覧表示されます。

### 使用可能なアクション

* [広告の作成](#ad-create)

* [行内から広告の名前を変更する](#ad-rename)

* [広告設定の編集](#ad-edit)

* [広告のステータスを変更または削除](#ad-status)

* [[!UICONTROL Ads] ビューからのデータビューレポートの管理](#ad-reports)

## 利用可能な広告タイプ {#ad-types}

同期広告ネットワークアカウント内の広告グループでサポートされている広告タイプを作成および管理できます。

* 検索ネットワークをターゲットとするキャンペーンの広告グループの&#x200B;**テキスト広告または拡張テキスト広告**。 テキスト広告には、広告グループレベルまたはキャンペーンレベルのパラメーターを上書きする、オプションのトラッキングパラメーターを含めることができます。 広告ネットワークによっては、拡張/拡張テキスト広告または標準テキスト広告を作成できる場合があります。

* [!DNL Microsoft Audience Network]の[!DNL Microsoft Advertising]件のキャンペーンに対するクロスデバイスのネイティブ **オーディエンス広告**。 キャンペーン設定に基づいて、オーディエンス広告には2つのオプションがあります。

  * キャンペーンが加盟店センターストアにリンクされている場合、広告ネットワークは、ストアの商品情報を使用して、キャンペーンのフィードベースの広告を自動的に生成します。 キャンペーン用にフィードベースの広告を作成する必要はありませんが、ユーザーターゲティングを使用して広告グループを作成する必要があります。

  * キャンペーンが加盟店センターのアカウントにリンクされていない場合は、複数のテキストや画像アセットを含むレスポンシブ広告フォーマットを使用して、画像ベースのオーディエンス広告を作成します。 広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を組み立て、[!DNL MSN]、[!DNL Outlook.com]、[!DNL Microsoft Edge]などのサイトに表示します。

* 検索ネットワーク上の[!DNL Google Ads]件のキャンペーンに対する&#x200B;**呼び出し専用広告**。 通話のみの広告は、電話番号を含むテキスト広告です。 オプションで、高度な通話レポートに[!DNL Google Ads]割り当てられた転送番号を使用できます。

  >[!NOTE]
  >
  >現在、呼び出し専用の広告を作成または編集することはできません。 既存の呼び出し専用広告の表示、ステータスの変更、または削除を行うことができます。

* **検索キャンペーンの[!DNL Google Ads]および[!DNL Microsoft Advertising]の動的検索広告グループに対して、動的検索広告** （現在は広告ネットワーク上で「動的検索広告」と呼ばれています）を拡張しました。 動的検索広告では、広告を表示するタイミングを決定するために、キーワードではなくweb サイトのコンテンツを使用します。 広告ネットワークは、見出しを動的に生成し、ランディングページのURLと表示URLを選択し、最終的なURLを自動的に生成します。

  動的検索広告について詳しくは、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/2471185)および[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/ads/en/56794)を参照してください。

* [!DNL Microsoft Advertising]件の検索キャンペーンの&#x200B;**マルチメディア広告**。 マルチメディア広告は、メインラインとサイドバーの目立つ位置に表示される大きな画像広告で、ページごとに1つのマルチメディア広告のみが表示されます。 レスポンシブ広告のように、複数のテキストや画像のアセットを含めることができます。また、広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を組み立てます。 マルチメディア広告がテキスト広告の配置を置き換えることはありません。

* ショッピング ネットワーク上の&#x200B;**[!DNL Microsoft Advertising]製品（ショッピング）広告**&#x200B;のプロモーション ライン。 ショッピング広告では、広告の表示方法と場所を決定するために、キーワードの代わりに既存の[!DNL Microsoft Merchant Center]製品フィードで製品を使用します。 広告のコピーとランディングページのURLは、フィード内の製品情報から自動的に生成されますが、オプションで広告グループに含めるプロモーションラインを設定できます。

  商品の広告について詳しくは、[Microsoft Advertising ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/51082)を参照してください。

* 検索ネットワーク上の[!DNL Google Ads]および[!DNL Microsoft Advertising] キャンペーンの&#x200B;**レスポンシブ検索広告**。 広告ネットワークは、一連の広告タイトルと説明からテキストベースのレスポンシブ検索広告を動的に組み合わせ、パフォーマンスが高い組み合わせを好みます。 この広告には、最大3つの見出し、2つの説明、およびベース URLとオプションのpath1およびpath2 フィールドからのカスタマイズ可能なURLが含まれます。 オプションで、特定の位置に広告タイトルと説明をピン留めすることができます。

  >[!NOTE]
  >
  >[!DNL Google Ads]は、ネイティブエディター以外では、広告として表示されたテキストの組み合わせに関するデータを提供しません。 各テキストの組み合わせのレポートについて詳しくは、[Google Ads ドキュメント ](https://support.google.com/google-ads/answer/7684791)を参照してください。

### 広告レベルのパフォーマンスデータ

広告レベルのデータは、ほとんどの広告タイプで利用可能です。

ただし、[!DNL Google Ads]件の動的検索広告（DSA）、パフォーマンスの最大値、スマートショッピング、および[!DNL YouTube]件のキャンペーンでは使用できません。 キャンペーンの広告レベルの合計データとキャンペーンの合計データの間に不一致が生じることを想定しています。

| 広告ネットワーク/キャンペーン/広告タイプ | データの可用性 |
|---|---|
| [!DNL Google Ads]件の動的検索広告（DSA） | キャンペーン、広告グループ |
| パフォーマンスの最大値：[!DNL Google Ads] | キャンペーン |
| [!DNL Google Ads]件のショッピング、スマートショッピング | キャンペーン、広告グループ |
| [!DNL Google Ads] [!DNL YouTube] | キャンペーン、広告グループ |

## 広告の作成 {#ad-create}

<!-- Verify that this note is still applicable -->

>[!NOTE]
>
>* ショッピング施策で商品広告を作成する必要はありません。広告ネットワークが自動的に作成します。 ただし、[!DNL Microsoft Advertising]件のショッピングキャンペーンの場合は、オプションで広告に含めるプロモーション行を定義できます。
>* [!DNL Google Ads]件の呼び出し専用の広告を作成することはできません。

>[!TIP]
>
>一度に多数の広告を作成するには、[ キャンペーンのバルクシート ](/help/search-social-commerce/new-ui/set-up/bulksheets/about.md)を使用します。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. **[!UICONTROL Create Ads]**&#x200B;をクリックします。

1. **[!UICONTROL Basic Settings]** ステップで、ネットワーク、アカウント、キャンペーン、広告グループ、広告タイプを選択します。

   使用可能な広告タイプについて詳しくは、「[使用可能な広告タイプ ](#ad-types)」を参照してください。

1. [Baidu テキスト広告](ad-settings-baidu-text.md)、[Google Ads expanded dynamic search ad](ad-settings-google-dsa.md) （Google Adsでは「動的検索広告」と呼ばれます）、[Google Ads responsive search ad](ad-settings-google-rsa.md)、[Microsoft Advertising expanded dynamic search ad](ad-settings-microsoft-dsa.md)、[Microsoft Advertising multimedia ad](ad-settings-microsoft-multimedia.md)、[Microsoft Advertising product ad](ad-settings-microsoft-product.md)、[Microsoft Advertising responsive （audience） ad](ad-settings-microsoft-responsive.md)、[Microsoft Advertising responsive search ad](ad-settings-microsoft-rsa.md)、または[yandex テキストのの残の残の残りの設定ad](ad-settings-yandex-text.md)設定。

   >[!NOTE]
   >
   >（Adobe Advertising コンバージョントラッキングを使用したキャンペーン）アカウントまたはキャンペーンの設定がキーワードレベルでのみトラッキングを指定する場合、Search, Social, &amp; Commerceでは広告のトラッキングが生成されません。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、広告設定を変更します。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

1. <!-- Add link to where to generate this once available to users-->（Adobe Advertising コンバージョントラッキングを使用したキャンペーンでのショッピング広告。オプション）広告のクリックをトラッキングするには、アカウント、キャンペーン、または商品グループの設定にトラッキング URLを手動で追加します。

## 広告の名前を変更 {#ad-rename}

完全な広告設定を開かずに、広告の名前をすばやく変更できます。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. 広告行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Rename]**&#x200B;をクリックします。

1. 名前を編集し、**[!UICONTROL Apply]**&#x200B;をクリックします。

## 広告設定の編集 {#ad-edit}

>[!NOTE]
>
>* 次の広告タイプは&#x200B;*可変*&#x200B;です。つまり、広告のコピーまたは画像を変更し、同じ広告IDを保持できます。動的検索広告を除くすべての[!DNL Google Ads]広告タイプ、および[!DNL Microsoft Advertising]拡張テキスト広告です。
>* サポートされているその他の広告はすべて&#x200B;*変更不可*&#x200B;です。つまり、広告コピーまたは画像を変更すると、既存の広告が削除され、新しい広告が作成されます。 Search, Social, &amp; Commerceで最適化に十分なデータを収集しながら、新しい広告のパフォーマンスは数週間にわたって不安定になる可能性があります。
>* 製品広告のコンテンツは、[!DNL Microsoft Advertising]個の製品広告のプロモーションラインを除き、編集できません。 ただし、広告を一時停止または削除することはできます。
>* [!DNL Google Ads]件の呼び出し専用の広告を編集することはできません。 ただし、一時停止または削除することはできます。
>* 一度に編集できる広告は1つだけです。

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. 広告の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [Baiduのテキスト広告](ad-settings-baidu-text.md)、[Google Ads expanded dynamic search ad](ad-settings-google-dsa.md) （現在はGoogle Adsで「動的検索広告」と呼ばれています）、[Google Ads responsive search ad](ad-settings-google-rsa.md)、[Microsoft Advertising expanded dynamic search ad](ad-settings-microsoft-dsa.md)、[Microsoft Advertising multimedia ad](ad-settings-microsoft-multimedia.md)、[Microsoft product ad](ad-settings-microsoft-product.md)、[Microsoft Advertising responsive （audience） ad](ad-settings-microsoft-responsive.md)、[Microsoft Advertising responsive search ad](ad-settings-microsoft-rsa.md)、または[Yandex ad](ad-settings-yandex-text.md)設定。

1. **[!UICONTROL Review and Save]**&#x200B;をクリックします。

1. 必要に応じて、![編集](/help/search-social-commerce/assets/edit-new.png "編集") **[!UICONTROL Edit]**&#x200B;をクリックし、広告設定を変更します。

1. **[!UICONTROL Update]**&#x200B;をクリックします。

## 広告のステータスの変更 {#ad-status}

完全な広告設定を開かずに、広告のステータスをすばやく変更できます。

サポートされている広告ネットワーク上のアクティブな広告を一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブな広告または一時停止した広告を削除することもできます。 削除された広告は、広告ネットワークから削除されます。 データフィルターに含めても表示されますが、変更することはできません。

### 広告のアクティベートまたは一時停止

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. 広告行のチェックボックスをオンにします。

1. 一括操作ツールバーで、ステータスを変更します。

   * 一時停止した広告を有効にするには、**[!UICONTROL Activate]**&#x200B;をクリックします。

   * アクティブな広告を一時停止するには、**[!UICONTROL Pause]**&#x200B;をクリックします。

### 広告の削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. 広告行のチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## [!UICONTROL Ads] ビューからのデータビューレポートの管理 {#ad-reports}

[!UICONTROL Ads] ビューの1つ以上の広告のデータ行を含むレポートを生成し、レポートをMicrosoft Excel ワークシート ファイル （XLXS形式）としてダウンロードします。 レポートには、表示されているすべての列がビューに含まれます。

生成されたレポートはすべて削除できます。

「[ （従来のUI） キャンペーン管理ビューからデータをダウンロード ](/help/search-social-commerce/common-tasks/navigation-editing-selection/download.md)」および「[ （従来のUI） [!UICONTROL Downloads] メニュー](/help/search-social-commerce/common-tasks/navigation-editing-selection/download-delete-data.md)からパフォーマンスデータレポートまたはバルクシートファイルを削除」も参照してください。

### フィルタリングされたデータ行を含むレポートを生成する

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. データをダウンロードする広告を指定します。

   * 特定の広告のデータをダウンロードするには、広告の横にあるチェックボックスをオンにします。

   * すべての広告のデータをダウンロードするには、チェックボックスをオンにする必要はありません。 すべての広告はデフォルトで含まれています。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports]設定で、一意のレポート名を入力し、**[!UICONTROL Generate]**&#x200B;をクリックします。

   デフォルトでは、ファイルの名前は「ad_YYYYMMDD_NNNNN」です。ここでは、「NNNN」は順次ジョブ番号（「ad_20250402_1326」など）です。

   ファイルが[!UICONTROL Recently Generated] リストに追加されます。

1. （オプション）完了したファイルをダウンロードするには、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完成したレポートをダウンロード

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![ ダウンロード ](/help/search-social-commerce/assets/download.png " ダウンロード ")をクリックします。

   ファイルは、ブラウザーの通常の手順に従ってダウンロードされます。

### 完了済みレポートの削除

1. メインメニューで、**[!UICONTROL Manage]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![ レポートをダウンロード ](/help/search-social-commerce/assets/download.png " レポートをダウンロード ") **[!UICONTROL Reports]**&#x200B;をクリックします。

1. [!UICONTROL Grid Reports] ダイアログの[!UICONTROL Recently Generated] リストで、ファイル名の横にある![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

>[!MORELIKETHIS]
>
>* [[!DNL Baidu]  テキスト広告設定](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] 動的検索広告設定を拡張](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  レスポンシブ検索の広告設定](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] 動的検索広告設定を拡張](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising]  マルチメディア広告設定](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 製品広告設定](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ （オーディエンス）広告の設定](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ検索の広告設定](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex]  テキスト広告設定](ad-settings-yandex-text.md)
