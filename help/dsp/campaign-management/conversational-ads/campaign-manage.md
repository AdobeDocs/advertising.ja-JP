---
title: '[!DNL ChatGPT Ads]件の会話型広告キャンペーンを管理'
description: '[!DNL ChatGPT Ads]件のキャンペーン、広告グループ、チャットカード広告を作成および管理する方法について説明します。AI アシスタントの会話内に広告を配置するベータ機能です。'
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
    internal-label: Demand Side Platform
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: cb25ab04e8fef5d00935e5325a897b1de97e2674
workflow-type: tm+mt
source-wordcount: '1188'
ht-degree: 0%
---
# [!DNL ChatGPT Ads]件の会話型広告キャンペーン、広告グループ、広告を管理

*Beta機能*

[会話型広告アカウント &#x200B;](account-manage.md)内の[!DNL ChatGPT Ads]件のキャンペーン、広告グループ、チャットカード広告を管理します。

月末に、他の請求書とともに[!DNL ChatGPT Ads]の使用状況に対する請求が行われます。 お支払いに関するご質問は、Adobeのアカウントチームにお問い合わせください。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] ビュー {#campaign-views-about}

[!UICONTROL Conversational Ads Beta] > [!UICONTROL Campaigns] ビューには、[!UICONTROL Campaigns]、[!UICONTROL Ad Groups]、[!UICONTROL Ads]の3つのタブがあります。 各タブには、選択したアカウントのキャンペーン、広告グループ、広告と、選択した日付範囲のパフォーマンスデータが一覧表示されます。 キャンペーン、広告グループおよび広告レベルのパフォーマンスデータには、[!UICONTROL Impressions]、[!UICONTROL Clicks]、[!UICONTROL Spend]、[!UICONTROL CTR]、[!UICONTROL Avg CPC]、および[!UICONTROL Avg CPM]が含まれます。

>[!NOTE]
>
>* レポートビューで税額を表示するように設定されている組織は、[!DNL ChatGPT Ads]の税額を表示しません。 税額を手動で計算します。

### 使用可能なアクション

<!-- * [Refresh information about your campaigns](#refresh) -- Add topic below. -->

* キャンペーンを[作成](#campaign-create)または[編集](#campaign-edit)

* 既存のキャンペーンの広告グループを[作成](#ad-group-create)または[編集](#ad-group-edit)する

* 既存の広告グループの広告を[作成](#ad-create)または[編集](#ad-edit)する

* [キャンペーン、広告グループ、広告のアクティベートまたは一時停止](#pause-activate)

* [キャンペーン、広告グループ、広告のアーカイブ](#archive)

* [キャンペーンを広告グループや広告にドリルダウンする](#drill-down)

* [キャンペーン、広告グループ、広告リストを更新する](#refresh)

## キャンペーン

### [!DNL ChatGPT Ads]の会話型広告キャンペーンの作成 {#campaign-create}

キャンペーンを作成する際は、オプションで最初の広告グループと広告を作成できます。 各ステップでは、**[!UICONTROL Next]**&#x200B;をクリックするとすぐにエンティティが作成されるので、前のステップに戻すことはできません。後で変更する必要がある場合は、ウィザードを閉じたら編集します。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. サブメニューで、「**[!UICONTROL Campaigns]**」タブをクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. 右上で、**[!UICONTROL Create]>[!UICONTROL Campaign]**&#x200B;をクリックします。

1. [&#x200B; キャンペーン設定](#campaign-settings)を指定します。

1. **[!UICONTROL Next]**&#x200B;をクリックして、キャンペーン設定を保存します。

1. 次のいずれかの操作を行います。

   * キャンペーンの広告グループを作成しない場合は、**[!UICONTROL Close]**&#x200B;をクリックします。

     >[!TIP]
     >
     >広告グループ以降を作成するには、「[広告グループを作成](#ad-group-create)」または「[広告を作成](#ad-create)」を参照してください。

   * （オプション）広告グループを作成します。

     1. [広告グループ設定](#ad-group-settings)を指定します。

     1. 「**[!UICONTROL Next]**」をクリックして、広告グループの設定を保存します。

     1. （オプション）キャンペーンの広告を作成しない場合は、**[!UICONTROL Close]**&#x200B;をクリックします。

   * （広告グループを作成した後はオプション）広告を作成します。

     1. [広告設定](#ad-settings)を指定します。

     1. **[!UICONTROL Create ad]**&#x200B;をクリックします。

### [!DNL ChatGPT Ads]件の対話型広告キャンペーン設定の編集 {#campaign-edit}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 左側のサブメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. （必要に応じて）データテーブルの上で、「**[!UICONTROL Campaigns]**」タブをクリックします。

1. 行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。

1. [&#x200B; キャンペーン設定](#campaign-settings)、[広告グループ設定](#ad-group-settings)、[広告設定](#ad-settings)のいずれかを編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### [!DNL ChatGPT Ads]個の対話型広告キャンペーン設定 {#campaign-settings}

**[!UICONTROL Campaign name]:** キャンペーンの一意の名前。 名前には少なくとも3文字を含める必要があります。

**[!UICONTROL Campaign type]:** （読み取り専用） *標準*&#x200B;は使用可能なタイプだけです。

**[!UICONTROL Objective]:** キャンペーンをフォーカスする指標：*リーチ*&#x200B;または&#x200B;*クリック*。 目的は、キャンペーンの広告グループの入札タイプを決定します。

**[!UICONTROL Locations]:** （オプション）ターゲットにする1つ以上の特定の場所。 すべての場所をターゲットにするには、この設定を空のままにします。 特定の場所を指定するには、名前の任意の場所に表示される2つ以上の文字を入力し、検索結果内の名前をクリックします。

**[!UICONTROL Budget type]:** *日別予算*&#x200B;または&#x200B;*生涯予算*。

**[!UICONTROL Budget]:**&#x200B;指定した予算タイプの予算。 値は0より大きくなければなりません。

**[!UICONTROL Start date]:** アカウントのタイムゾーンで、キャンペーンが開始された日付。

**[!UICONTROL Set an end date]:** （オプション）キャンペーンの終了日を指定できます。 このオプションを選択する場合は、**[!UICONTROL End date]**&#x200B;を指定します。

## 広告グループ

### 既存のキャンペーン用に[!DNL ChatGPT Ads]広告グループを作成 {#ad-group-create}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. サブメニューで、「**[!UICONTROL Campaigns]**」タブをクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. 右上で、**[!UICONTROL Create]>[!UICONTROL Ad Group]**&#x200B;をクリックします。

1. 親キャンペーンを含め、[広告グループ設定](#ad-group-settings)を指定します。

1. **[!UICONTROL Create ad group]**&#x200B;をクリックします。

## [!DNL ChatGPT Ads]広告グループの編集 {#ad-group-edit}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 左側のサブメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. データテーブルの上にある「**[!UICONTROL Ad Groups]**」タブをクリックします。

1. 行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。

1. [広告グループ &#x200B;](#ad-group-settings)の設定を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### [!DNL ChatGPT Ads]広告グループの設定 {#ad-group-settings}

**[!UICONTROL Parent campaign]:** （既存のキャンペーンの広告グループのみ）広告グループが属するキャンペーン。

**[!UICONTROL Ad group name]:**&#x200B;広告グループの一意の名前。 名前には少なくとも3文字を含める必要があります。

**[!UICONTROL Maximum CPC bid]**&#x200B;または&#x200B;**[!UICONTROL Maximum CPM bid]:** クリックごと、または1,000回のインプレッションに対して支払う最大金額。 値は0より大きくなければなりません。 キャンペーンの目的によって入札フィールドが決まります：*クリック数* キャンペーンが&#x200B;**[!UICONTROL Maximum CPC bid]**&#x200B;件を示し、*リーチ* キャンペーンが&#x200B;**[!UICONTROL Maximum CPM bid]**&#x200B;件を示します。

>[!TIP]
>
>より高い入札はより多くのオークションを獲得する可能性があります。

**[!UICONTROL Context hints]:** （オプション）製品またはサービスが関連する会話、トピック、またはキーワードの説明。 これらのヒントはマッチングを導きますが、完全一致のターゲティングルールではありません。

## 広告

### 既存の広告グループの[!DNL ChatGPT Ads] チャットカード広告を作成する {#ad-create}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. サブメニューで、「**[!UICONTROL Campaigns]**」タブをクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. 右上で、**[!UICONTROL Create]>[!UICONTROL Ad]**&#x200B;をクリックします。

1. 親キャンペーンと広告グループを含む[広告設定](#ad-settings)を指定します。

1. **[!UICONTROL Create ad]**&#x200B;をクリックします。

## [!DNL ChatGPT Ads] チャットカード広告の編集 {#ad-edit}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 左側のサブメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. データテーブルの上にある「**[!UICONTROL Ads]**」タブをクリックします。

1. 行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit]**&#x200B;をクリックします。

1. [ad](#ad-settings)設定を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

### [!DNL ChatGPT Ads]件のチャットカード広告の設定 {#ad-settings}

**[!UICONTROL Parent campaign]**&#x200B;と&#x200B;**[!UICONTROL Parent ad group]:** （既存の広告グループの広告のみ）広告が属するキャンペーンと広告グループ。

**[!UICONTROL Ad name]:**&#x200B;広告の一意の名前。 名前には少なくとも3文字を含める必要があります。

**[!UICONTROL Ad URL (Link)]:** ランディングページのURL （`http://`または`https://`で始まる）。

**[!UICONTROL Title (headline)]:**&#x200B;広告の見出し タイトルは3～50文字の範囲で指定してください。 **注意：**&#x200B;一部のプレースメントタイプでは、タイトルが切り捨てられる場合があります。

**[!UICONTROL Description]:**&#x200B;広告の本文。 説明は3 ～ 100文字の範囲で指定してください。

**[!UICONTROL Ad image]:**&#x200B;広告に含めるJPGまたはPNG画像。 画像をアップロードするには、（新しい広告） **[!UICONTROL Upload image (PNG/JPG)]**&#x200B;または&#x200B;**[!UICONTROL Change image]**&#x200B;をクリックし、デバイスまたはネットワーク上のファイルを見つけて選択します。

**[!UICONTROL Preview]:**&#x200B;広告設定に基づく広告のプレビュー。

## [!DNL ChatGPT Ads] キャンペーン、広告グループ、または広告をアクティブ化または一時停止する {#pause-activate}

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 左側のサブメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. 「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」または「**[!UICONTROL Ads]**」タブで、行を検索します。

1. **[!UICONTROL Active]**&#x200B;列で、次のいずれかの操作を行います。

   * 一時停止した項目をアクティブにするには、切り替えスイッチ（右側）をオンにします。

   * アクティブな項目を一時停止するには、切り替えスイッチをオフにします（左）。

## [!DNL ChatGPT Ads] キャンペーン、広告グループ、または広告をアーカイブ {#archive}

アーカイブすると、キャンペーン、広告グループ、または広告が[!UICONTROL Conversational Ads] ビューから完全に削除されます。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 左側のサブメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

1. 右上で、広告主と[!DNL ChatGPT Ads] アカウントを選択します。

1. 「**[!UICONTROL Campaigns]**」、「**[!UICONTROL Ad Groups]**」または「**[!UICONTROL Ads]**」タブで、行の上にカーソルを置き、「**[!UICONTROL ...]」 > 「[!UICONTROL Archive]**」をクリックします。

## [!DNL ChatGPT Ads]件のキャンペーンから広告グループおよび広告にドリルダウンします {#drill-down}

* キャンペーン行をクリックして&#x200B;**[!UICONTROL Ad Groups]** タブでその広告グループのみを表示するか、広告グループ行をクリックして&#x200B;**[!UICONTROL Ads]** タブでその広告のみを表示します。

フィルターを削除してビュー内のすべての行を表示するには、データテーブルの上にあるフィルターの&#x200B;**X**&#x200B;をクリックします。

## キャンペーン、広告グループ、広告リストを更新する {#refresh}

他のユーザーが変更または追加した可能性がある場合に、キャンペーン、広告グループ、または広告のリストを再表示します。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. **[!UICONTROL Campaigns]**、**[!UICONTROL Ad Groups]**、または&#x200B;**[!UICONTROL Ads]** ビューで、データテーブルの上の&#x200B;**[!UICONTROL Refresh]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [会話型広告アカウントの管理](account-manage.md)
