---
title: 共有サイトリンクの管理
description: 共有サイトリンク拡張機能の作成と管理方法について説明します。
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/bnKg6ySgpFF30MuE19xdHWimvAQVwvIqv1NRg-S2jTI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 928
ht-degree: 0%

---

# 共有サイトリンクの管理

*[!DNL Google Ads]と[!DNL Microsoft Advertising]のみ*

[!DNL Google Ads] > [!DNL Microsoft Advertising] ライブラリから、同期された[!UICONTROL Extensions]または[!UICONTROL Sitelinks] アカウントのアカウントレベルの共有サイトリンクを作成および管理します。

## 共有サイトリンクの作成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワークとアカウント名を選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

1. [共有サイトリンク設定](#shared-sitelink-settings)を入力します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

サイトリンクを作成したら、[&#x200B; アカウント、キャンペーン、または広告グループに割り当てることができます](sitelink-extension-associate.md)。

## 共有サイトリンク設定の編集

共有サイトリンクは一度に1つずつ編集できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**&#x200B;をクリックします。

1. 編集するサイトリンクの横にあるチェックボックスをオンにします。

1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. [共有サイトリンク設定](#shared-sitelink-settings)を編集します。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

## 共有サイトリンクを削除

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**&#x200B;をクリックします。

1. 削除する各共有サイトリンクの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. ツールバーで、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## 共有サイトリンク設定 {#shared-sitelink-settings}

サイトリンクの非承認に関する追加のポリシーと理由については、[[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210)および[[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) サイトリンク拡張機能の要件を参照してください。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** リンクに表示されるテキスト。 これには、最大25個のシングルバイト文字または12個のダブルバイト文字を含めることができます。 リンクテキストは、アカウントまたはキャンペーン内で一意である必要があります。

>[!NOTE]
>
>（[!DNL Google Ads]） 35文字の既存のテキストは、デスクトップやタブレットでは広告に表示されますが、モバイルデバイスでは表示されません。

**[!UICONTROL Status]:** サイトリンクの表示ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Deleted]* （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは&#x200B;*[!UICONTROL Active]*&#x200B;です。

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:**&#x200B;検索エンジンがリンクテキストの下に表示できる追加テキスト。 説明を含めるには、両方の説明フィールドに値を入力します。 各説明フィールドには、最大35個の1 バイト文字または17個の2 バイト文字を含めることができます。

**[!UICONTROL Start Date]:** （既存のサイトリンクがあるキャンペーンまたはサイトリンクがないキャンペーンのみ。オプション） サイトリンクがキャンペーン内の広告と共に表示される最初の日付。 新しいサイトリンクのデフォルトは現在の日付です。 今後の開始日を指定するには、MM/DD/YYYYまたはM/D/YYYY形式で日付を入力するか、クリックします   日付を選択します。

**[!UICONTROL End Date]:** （オプション） サイトリンクがキャンペーン内の広告と共に表示される最後の日付。 デフォルトでは、サイトリンクは無期限に表示される場合があります。 終了日を指定するには、MM/DD/YYYYまたはM/D/YYYY形式で日付を入力するか、クリックします   日付を選択します。

**[!UICONTROL Mobile Preference]:** （オプション） ネットワークが、デスクトップ ユーザーやタブレット ユーザーではなく、モバイル デバイス ユーザーに広告拡張機能を表示しようとすることを許可します。 デフォルトでは、このオプションは有効になっておらず、広告拡張機能は任意のデバイスタイプに表示されます。

>[!NOTE]
>
>ネットワークは、好みのデバイスタイプに広告拡張機能が表示されることを保証するものではありません。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]**&#x200B;検索エンジンユーザーが広告をクリックしたときに取得されるランディングページ URL。 ページの内容を決定するパラメーターを含めます。 値を入力すると、広告のベース URLが上書きされます。

レコードを保存すると、ベース URLには、キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

>[!NOTE]
>
>* （最終URLを持つアカウント）ベース URLには、ランディングページドメインまたはサブドメイン内のリダイレクトが含まれていても、ランディングページドメイン外のリダイレクトは含まれていない場合があります。 広告ネットワークは、このURLからドメインを抽出し、広告の任意の表示パスを追加して、広告の表示URLを作成します。
>* （[!DNL Google Ads]） キャンペーンまたは広告グループ内の各サイトリンクには一意のランディングページが必要で、各サイトリンク ランディングページのコンテンツには約80%の一意のコンテンツが必要です。 例えば、同じページ内に複数のアンカーへのリンクを含むサイトリンクを設定することはできません。
>* （[!DNL Google Ads]）並列トラッキングを有効にするソースからのクリックに代わらないマクロの使用を避けます。 広告主がマクロを使用する必要がある場合は、Adobe アカウントチームがカスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページのURLをパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 例：リダイレクトを含める`{lpurl}?source={network}&id=5`または`http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5`。

* キャンペーン設定に「[!UICONTROL EF Redirect]」と「自動アップロード」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceは自動的に独自のクリックトラッキングコードの先頭に付きます。

* サポートされているパラメーターで最終的なURLを埋め込むには、[!DNL Microsoft Advertising] ドキュメント [[!DNL Microsoft Advertising] の「使用可能な](https://help.ads.microsoft.com/#apex/3/en/56799) パラメーター」の節の「[!DNL Google Ads]のみ） [!DNL ValueTrack] ドキュメント [[!DNL Google Ads] または（](https://support.google.com/google-ads/answer/6305348)のみ）トラッキングテンプレートのみ」パラメーターを参照してください。

* 必要に応じて、URL パラメーターと、キャンペーン用に定義された任意のカスタムパラメーターを、アンパサンド（&amp;）で区切って含めることができます（`{lpurl}?matchtype={matchtype}&device={device}`）。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合、レコードを保存すると、Search、Social、およびCommerceに独自のリダイレクトコードとトラッキングコードが自動的にプレフィックスされます。
>* 最も詳細なレベルのトラッキングテンプレートは、より高いレベルのすべての値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* （[!DNL Google Ads]）サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 承認のために広告を再送信することなく、アカウントレベル、キャンペーンレベル、広告グループレベルでトラッキングテンプレートを更新できます。
>* （[!DNL Microsoft Advertising]）承認のために広告を再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。
>* [!DNL Google Ads]の場合、並列追跡を有効にするソースからのクリックに代わらないマクロの使用を避けてください。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームは、カスタマーサポートまたは実装チームと協力してマクロを追加する必要があります。

>[!MORELIKETHIS]
>
>* [&#x200B; サイトリンク拡張機能について](sitelink-extension-about.md)
>* [共有サイトリンクをアカウント、キャンペーン、広告グループに関連付ける](sitelink-extension-associate.md)
