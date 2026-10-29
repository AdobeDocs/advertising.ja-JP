---
title: '[!DNL ChatGPT Ads]個の会話型広告アカウントを管理'
description: AI アシスタントの会話内に広告を配置するベータ機能である[!DNL ChatGPT Ads]のチャットカード広告のアカウントを作成および管理する方法について説明します。
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
source-wordcount: '898'
ht-degree: 0%
---
# [!DNL ChatGPT Ads]個の会話型広告アカウントを管理

*Beta機能*

Adobe DSPと[!DNL OpenAI Ads]との統合により、[!DNL ChatGPT Ads]件のチャットカード広告を実行することができ、[!DNL ChatGPT]件の会話内に表示されます。 DSPは、この機能のために会話型の広告アカウントを作成し、組織の代わりにメディアを購入します。 ads.openai.comから広告アカウントにアクセスすることはできません。 この機能を使用すると、[!DNL ChatGPT Ads]との直接的な関係を確立せずにAI メディアをテストできます。

キャンペーン、広告グループ、広告を含む[!DNL ChatGPT Ads]個の会話型広告アカウントを、構造化が異なる通常のDSP キャンペーンとは別に管理します。 また、DSP キャンペーンとは別に、 [!DNL ChatGPT Ads]  キャンペーン、広告グループ、広告](campaign-manage.md#campaign-views-about)のパフォーマンスデータを[表示できます。

## 実施要件

次の手順で、この機能の実施要件を決定します。

* **既存の[!DNL Search, Social, & Commerce]のお客様：**&#x200B;広告主が既に[!DNL Search, Social, & Commerce]を使用している場合、[DSPではなく、検索、ソーシャル、Commerce](/help/search-social-commerce/new-ui/manage/campaigns/campaign-manage.md)で [!DNL ChatGPT Ads]  キャンペーンを作成および管理します。

* **制限付き業界：**&#x200B;制限付きカテゴリー（金融や医療など）の広告主は、会話型の広告アカウントやキャンペーンを作成できません。

選択した広告主が対象外の場合、[!UICONTROL Accounts]と[!UICONTROL Campaigns]のタブはその理由を示します。 広告主セレクターを使用して、別の広告主に切り替えることができます。

この機能を使用するには、Adobe アカウントチームに連絡してオンボーディングプロセスを開始してください。

## 課金

DSP アカウントの請求通貨と請求タイムゾーンを使用して、他の請求書と共に月末に[!DNL ChatGPT Ads]の使用量に対して請求されます（ [!DNL ChatGPT Ads]  アカウント ](#account-settings)に使用される[通貨とタイムゾーンに関係なく）。 お支払いに関するご質問は、Adobeのアカウントチームにお問い合わせください。

## [!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts] ビュー {#accounts-view}

「[!UICONTROL Conversational Ads Beta] > [!UICONTROL Accounts]」タブには、選択した広告主の[!DNL OpenAI] アカウントが一覧表示されます。 各アカウントの情報には、次のものが含まれます。

**[!UICONTROL Status]:** アカウントが現在広告を配信しているかどうか：*アクティブ*&#x200B;または&#x200B;*一時停止*。 アカウントのステータスを変更することはできません。アカウントを一時停止または再アクティブ化する場合は、Adobe アカウントチームにお問い合わせください。

**[!UICONTROL Review status]:** [!DNL OpenAI]のレビュー状態：*レビュー中*、*承認済み*、または&#x200B;*未承認*。 理由のステータスにカーソルを合わせます（使用可能な場合）。

**[!UICONTROL Active campaigns]:** アカウント内で現在アクティブなキャンペーンの数。

**[!UICONTROL Cost]:** アカウントの総支出。

### 使用可能なアクション

* [アカウント制限の表示](#account-limits)

<!-- * [Refresh information about your accounts](#refresh) -- Add topic below. -->

* [アカウントの作成](#account-create)

* [アカウントの編集](#account-edit)

* [アカウントリストを更新する](#account-refresh)

* [DSPのメインメニューに戻る](#return-to-menu)

## アカウントの管理

### アカウント制限の表示 {#account-limits}

アカウント制限は、特定の日付範囲におけるアカウントの総支出に上限を設定します。 アカウントの制限は表示できますが、制限を作成、編集、または削除できるのはAdobe アカウントチームのみです。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. **[!UICONTROL Accounts]** ビューで、アカウント行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL View account limit]**&#x200B;をクリックします。

[!UICONTROL Account limits] ページには、アカウントの各制限が一覧表示されます。

**[!UICONTROL Name]:**&#x200B;制限の名前。

**[!UICONTROL Amount]:**&#x200B;制限期間の合計支出上限です。

**[!UICONTROL Period]:**&#x200B;制限が適用される日付範囲。

**[!UICONTROL Status]:** *アクティブ*、*予定*、または&#x200B;*完了*。

**[!UICONTROL Spent]:**&#x200B;制限期間内にこれまで費やした金額。

>[!NOTE]
>
>完了した制限を編集または削除することはできず、同じアカウントの制限期間を重ねることはできません。

### [!DNL ChatGPT Ads]の会話型広告アカウントを作成 {#account-create}

広告主向けに2つ以上の[!DNL ChatGPT Ads] アカウントを作成するには、Adobe アカウント チームにお問い合わせください。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （最初のアカウントのみ）ようこそ画面で「**[!UICONTROL Create an Account]**」をクリックします。

   * **[!UICONTROL Accounts]** ビューで、広告主を選択し、**[!UICONTROL Create Account]**&#x200B;をクリックします。

1. [ アカウント設定](#account-settings)を指定します。

1. 「**[!UICONTROL I agree to the Terms and Conditions]**」チェックボックスを選択します。

1. **[!UICONTROL Create account]**&#x200B;をクリックします。

[!DNL OpenAI]さんがアカウントをレビューしている間、新しいアカウントは一時停止された状態で作成されます。 DSPは、承認されるとアカウントをアクティベートします。

### [!DNL ChatGPT Ads]の会話型広告アカウントを編集 {#account-edit}

アカウントの法人名とweb サイトは、作成後に編集できます。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. **[!UICONTROL Accounts]** ビューで、アカウント行の上にカーソルを置き、**[!UICONTROL ...]>[!UICONTROL Edit account]**&#x200B;をクリックします。

1. **[!UICONTROL Legal Business Name]**&#x200B;または&#x200B;**[!UICONTROL Advertiser Website]**&#x200B;を編集します。 フィールドについて詳しくは、「[ アカウント設定](#account-settings)」を参照してください。

1. **[!UICONTROL Save changes]**&#x200B;をクリックします。

>[!IMPORTANT]
>
>変更を保存すると、アカウントの[!DNL OpenAI]さんのレビューが再開されます。 アカウントが再度承認されるまで、アカウントは広告を配信しません。

### アカウントリストを更新する {#account-refresh}

他のユーザーが変更または追加を行った可能性がある場合に、アカウントのリストを再表示します。

1. メインメニューで、**[!UICONTROL Conversational Ads Beta]**&#x200B;をクリックします。

1. **[!UICONTROL Accounts]** ビューで、アカウントリストの上の&#x200B;**[!UICONTROL Refresh]**&#x200B;をクリックします。

### DSPのメインメニューに戻る {#return-to-menu}

* メインメニューの上にある「**[!UICONTROL Back to DSP]**」をクリックします。

### [!DNL ChatGPT Ads]個の対話型広告アカウント設定 {#account-settings}

**[!UICONTROL Legal Business Name]:**&#x200B;組織の登録済みビジネス名。

**[!UICONTROL Advertiser Website]:**&#x200B;広告主のweb サイトのURL （`http://`または`https://`から始まる）。

**[!UICONTROL Country]:**&#x200B;組織が法的に登録されている国（広告を掲載する国ではありません）。 DSP契約に使用する国と同じである必要があります。 アカウントを保存した後にこの値を変更することはできません。

**[!UICONTROL Currency]:** （読み取り専用） Adobe アカウントチームが[!DNL ChatGPT Ads] アカウントに設定する通貨。 これは、DSP内の他の場所に表示されるDSP アカウントの通貨とは異なる場合があります。 **注：**&#x200B;この値にかかわらず、すべての使用料金は、DSP アカウントに使用される&#x200B;*請求通貨*&#x200B;になります。

**[!UICONTROL Timezone]:** （読み取り専用） Adobe アカウントチームが[!DNL ChatGPT Ads] アカウントに設定したタイムゾーン。 これは、DSP内の他の場所に表示されるDSP アカウントに使用されるタイムゾーンとは異なる場合があります。 **注：**&#x200B;この値にかかわらず、すべての使用料金は、DSP アカウントに使用される&#x200B;*請求タイムゾーン*&#x200B;を表します。

**[!UICONTROL Favicon]:** アカウントのweb サイトのファビコンとして使用する画像ファイル。<!-- How is this used within this context? --> ブラウザーは、アドレスバー、タブ、ブックマークなど、さまざまな場所にファビコンを表示します。 ファイルは、JPG、PNGまたはWEBP形式で、256 x 256 ピクセル以上である必要があります。

アイコンをアップロードするには、**[!UICONTROL Upload favicon]**&#x200B;をクリックし、デバイスまたはネットワーク上のファイルを見つけて選択します。

**[!UICONTROL I agree to the Terms and Conditions]:**&#x200B;すべての法的条件に同意することを示すチェックボックス。 チェックボックスを選択して、アカウントを作成するか、アカウント設定を更新します。

>[!MORELIKETHIS]
>
>* [会話型広告キャンペーンの管理](campaign-manage.md)
