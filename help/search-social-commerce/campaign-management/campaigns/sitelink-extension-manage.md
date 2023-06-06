---
title: 共有サイトリンクを管理
description: 共有サイトリンク拡張機能を作成および管理する方法について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '939'
ht-degree: 0%

---

# 共有サイトリンクを管理

*[!DNL Google Ads]および [!DNL Microsoft Advertising] のみ*

同期されたすべてのアカウントレベルの共有サイトリンクを作成および管理 [!DNL Google Ads] または [!DNL Microsoft Advertising] アカウント [!UICONTROL Extensions] > [!UICONTROL Sitelinks] ライブラリ。

## 共有サイトリンクを作成

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. 次を入力します。 [共有サイトリンク設定](#shared-sitelink-settings).

1. クリック **[!UICONTROL Post]**.

サイトリンクを作成すると、 [アカウント、キャンペーンまたは広告グループに割り当てる](sitelink-extension-associate.md).

## 共有サイトリンク設定を編集

一度に 1 つの共有サイトリンクを編集できます。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 編集するサイトリンクの横にあるチェックボックスを選択します。

1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [共有サイトリンク設定](#shared-sitelink-settings).

1. クリック **[!UICONTROL Post]**.

## 共有サイトリンクを削除

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]**.

1. 削除する各共有サイトリンクの横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. ツールバーで、 ![詳細](/help/search-social-commerce/assets/more.png "詳細") を選択し、 **[!UICONTROL Delete]**.

1. 確認メッセージで、 **[!UICONTROL Delete]**.

## 共有サイトリンク設定 {#shared-sitelink-settings}

サイトリンクの不承認の追加のポリシーと理由については、 [[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) および [[!DNL Microsoft Advertising]](https://about.ads.microsoft.com/en-us/resources/policies/ad-extensions-policies) sitelink 拡張の要件。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** リンクに表示するテキスト。 1 バイト文字または 2 バイト文字を 25 文字まで含めることができます。 リンクテキストは、アカウントまたはキャンペーン内で一意である必要があります。

>[!NOTE]
>
>([!DNL Google Ads]) デスクトップおよびタブレットでは、広告に 35 文字の既存のテキストが表示されますが、モバイルデバイスでは表示されません。

**[!UICONTROL Status]:** サイトリンクの表示ステータス：  *[!UICONTROL Active]* または *[!UICONTROL Deleted]* （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトはです。 *[!UICONTROL Active]*.

**[!UICONTROL Description Line 1], [!UICONTROL Description Line 2]:** リンクテキストの下に検索エンジンで表示される可能性のある追加のテキスト。 説明を含めるには、両方の説明フィールドに値を入力します。 各説明フィールドには、最大 35 文字の 1 バイト文字または 17 文字の 2 バイト文字を含めることができます。

**[!UICONTROL Start Date]:** ( 既存の従来のサイトリンクを持つキャンペーン、またはサイトリンクのみを持たないキャンペーン。（オプション）キャンペーンで広告と共にサイトリンクを表示できる最初の日付。 新しいサイトリンクのデフォルトは現在の日です。 将来の開始日を指定するには、MM/DD/YYYY または M/D/YYYY の形式で日付を入力するか、「 」をクリックして日付を選択します。

**[!UICONTROL End Date]:** （オプション）キャンペーンで広告と共にサイトリンクを表示できる最後の日付。 デフォルトでは、サイトリンクは無期限に表示される場合があります。 終了日を指定するには、MM/DD/YYYY または M/D/YYYY の形式で日付を入力するか、をクリックして日付を選択します。

**[!UICONTROL Mobile Preference]:** （オプション）デスクトップユーザーやタブレットユーザーではなく、モバイルデバイスユーザーに対して広告拡張機能を表示しようとすることを許可します。 デフォルトでは、このオプションは有効になっておらず、広告拡張はどのデバイスタイプにも表示されます。

>[!NOTE]
>
>ネットワークでは、広告の拡張が優先デバイスタイプで表示されるとは保証されません。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** 広告のクリック時に検索エンジンユーザーが取得するランディングページの URL。 ページの内容を決定するパラメーターを含めます。 値を入力すると、広告のベース URL よりも優先されます。

レコードを保存すると、ベース URL にはキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

>[!NOTE]
>
>* （最終 URL を持つアカウント）ベース URL は、ランディングページドメインまたはサブドメイン内でのリダイレクトを含むことができますが、ランディングページドメイン外でのリダイレクトは含まれません。 広告ネットワークは、この URL からドメインを抽出し、広告のオプションの表示パスを追加して、広告の表示 URL を作成します。
>* ([!DNL Google Ads]) キャンペーンまたは広告グループ内の各サイトリンクには一意のランディングページが必要で、各サイトリンクランディングページのコンテンツには約 80%の一意のコンテンツが必要です。 例えば、同じページ内に複数のアンカーへのリンクを含むサイトリンクを含めることはできません。
>* ([!DNL Google Ads]) 並列追跡を有効にするソースからのクリック数に代わられないマクロの使用は避けてください。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。


**[!UICONTROL Tracking Template]:** （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込むトラッキングテンプレートまたはトラッキング URL。 例： `{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` リダイレクトを含める。

* Adobe広告コンバージョントラッキングの場合は、キャンペーン設定に「EF Redirect」と「Auto Upload」が含まれる場合に適用され、レコードを保存する際に、検索、Social、および Commerce によって、独自のクリック追跡コードが自動的に先頭に追加されます。

* 最終的な URL を埋め込むためにサポートされているパラメーターについては、 ([!DNL Microsoft Advertising] のみ ) [[!DNL Microsoft Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/3/en/56799) または ([!DNL Google Ads] （専用） [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/6305348).

* オプションとして、URL パラメーターと、キャンペーンに定義されているカスタムパラメーターを、アンパサンド (&amp;) で区切って含めることができます。例えば、 `{lpurl}?matchtype={matchtype}&device={device}`.

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* キャンペーン設定で[!UICONTROL EF Redirect]&quot;および&quot;[!UICONTROL Auto Upload]、「 Search, Social, &amp; Commerce では、レコードを保存する際に、自動的に独自のリダイレクトおよびトラッキングコードがプレフィックスとして付加されます。
>* 最も精度の高いレベルのトラッキングテンプレートは、より高いレベルの値よりも優先されます。 例えば、アカウント設定とキーワード設定の両方に値が含まれる場合、そのキーワード値が適用されます。
>* ([!DNL Google Ads]) サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告が再送信されてレビューされます。 広告を承認用に再送信しなくても、アカウント、キャンペーンまたは広告グループレベルでトラッキングテンプレートを更新できます。
>* ([!DNL Microsoft Advertising]) 広告を承認用に再送信することなく、任意のレベルでトラッキングテンプレートを更新できます。
>* の場合 [!DNL Google Ads]を使用する場合は、並列追跡を有効にするソースからのクリック数に代わられないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合は、Adobeアカウントチームがカスタマーサポートまたは実装チームと連携してマクロを追加する必要があります。


>[!MORELIKETHIS]
>
>* [sitelink の拡張について](sitelink-extension-about.md)
>* [共有サイトリンクをアカウント、キャンペーンおよび広告グループに関連付ける](sitelink-extension-associate.md)

