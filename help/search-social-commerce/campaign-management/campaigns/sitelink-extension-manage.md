---
title: 共有サイトリンクの管理
description: 共有サイトリンク拡張機能を作成および管理する方法について説明します。
exl-id: e510f53b-f48c-4129-887c-351a840b8398
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '928'
ht-degree: 0%

---

# 共有サイトリンクの管理

*[!DNL Google Ads]と [!DNL Microsoft Advertising] のみ*

同期された [!DNL Google Ads] ーザーまたは [!DNL Microsoft Advertising] アカウントに対して、アカウントレベルの共有サイトリンクを [!UICONTROL Extensions]/[!UICONTROL Sitelinks] ライブラリで作成および管理します。

## 共有サイトリンクの作成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワークとアカウント名を選択し、「**[!UICONTROL Continue]**」をクリックします。

1. [ 共有サイトリンクの設定 ](#shared-sitelink-settings) を入力します。

1. 「**[!UICONTROL Post]**」をクリックします。

サイトリンクを作成したら、[ アカウント、キャンペーン、広告グループに割り当てる ](sitelink-extension-associate.md) ことができます。

## 共有サイトリンク設定の編集

共有サイトリンクは一度に 1 つずつ編集できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** をクリックします。

1. 編集するサイトリンクの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. [ 共有サイトリンクの設定 ](#shared-sitelink-settings) を編集します。

1. 「**[!UICONTROL Post]**」をクリックします。

## 共有サイトリンクの削除

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Sitelinks]** をクリックします。

1. 削除する各共有サイトリンクの横にあるチェックボックスをオンにします。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. ツールバーの ![ その他 ") をクリックし ](/help/search-social-commerce/assets/more.png " 選択 **[!UICONTROL Delete]** ます。

1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

## 共有サイトリンクの設定 {#shared-sitelink-settings}

サイトリンクが承認されないその他のポリシーと理由については、[[!DNL Google Ads]](https://support.google.com/adspolicy/answer/1054210) および [[!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/ext60206) のサイトリンク拡張機能の要件を参照してください。

### [!UICONTROL Sitelink]

**[!UICONTROL Link Name]:** リンクに表示するテキスト。 最大 25 個のシングルバイト文字または 12 個のダブルバイト文字を含めることができます。 リンクテキストは、アカウントまたはキャンペーン内で一意である必要があります。

>[!NOTE]
>
>（[!DNL Google Ads]）デスクトップおよびタブレットの広告には、35 文字の既存のテキストが表示されますが、モバイルデバイスには表示されません。

**[!UICONTROL Status]:** サイトリンクの表示ステータス：*[!UICONTROL Active]* または *[!UICONTROL Deleted]* （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは *[!UICONTROL Active]* です。

**[!UICONTROL Description Line 1]、[!UICONTROL Description Line 2]:** 検索エンジンがリンクテキストの下に表示する可能性のある追加テキスト。 説明を含めるには、両方の説明フィールドに値を入力します。 各説明フィールドには、最大 35 個のシングルバイト文字または 17 個のダブルバイト文字を含めることができます。

**[!UICONTROL Start Date]:** （既存の従来のサイトリンクがある、またはサイトリンクがないキャンペーンのみ。オプション）キャンペーンの広告でサイトリンクを表示できる最初の日付。 新しいサイトリンクのデフォルトは現在の日付です。 将来の開始日を指定するには、MM/DD/YYYY または M/D/YYYY の形式で日付を入力するか、   日付を選択します。

**[!UICONTROL End Date]:** （任意）キャンペーンで広告にサイトリンクを表示できる最終日。 デフォルトでは、サイトリンクは無期限に表示される場合があります。 終了日を指定するには、MM/DD/YYYY または M/D/YYYY の形式で日付を入力するか、   日付を選択します。

**[!UICONTROL Mobile Preference]:** （オプション）デスクトップまたはタブレットユーザーではなく、モバイルデバイスユーザーに対してネットワークが広告拡張機能を表示することを許可します。 デフォルトでは、このオプションは有効ではなく、広告拡張機能はどのデバイスタイプにも表示されます。

>[!NOTE]
>
>ネットワークでは、優先デバイスタイプに広告拡張機能が表示されるとは保証されません。

### [!UICONTROL Tracking URLs]

**[!UICONTROL Base URL]** 検索エンジンユーザーが広告をクリックした際に取得されるランディングページの URL。 ページのコンテンツを決定するパラメーターを含めます。 値を入力すると、広告のベース URL が上書きされます。

レコードを保存すると、ベース URL には、キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

>[!NOTE]
>
>* （最終的な URL を持つアカウント）ベース URL には、ランディングページのドメインまたはサブドメイン内のリダイレクトを含めることができますが、ランディングページのドメイン外のリダイレクトを含めることはできません。 広告ネットワークは、この URL からドメインを抽出し、広告の任意の表示パスを追加して、広告の表示 URL を作成します。
>* （[!DNL Google Ads]）キャンペーンまたは広告グループの各サイトリンクには、一意のランディングページが必要で、各サイトリンクランディングページのコンテンツには、約 80% の一意のコンテンツが必要です。 例えば、同じページ内に複数のアンカーへのリンクを含むサイトリンクを持つことはできません。
>* （[!DNL Google Ads]） マクロを使用しないでください。このマクロは、並列トラッキングを有効にするソースからのクリックに代わるものではありません。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームはカスタマーサポートまたは実装チームと協力して、マクロを追加する必要があります。

**[!UICONTROL Tracking Template]:** （任意） トラッキングテンプレートまたはトラッキング URL。すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終/ランディングページの URL をパラメーターに埋め込みます。 例：リダイレクトを含めるには、`{lpurl}?source={network}&id=5` または `http://www.trackingservice.example.com/?url={lpurl}?source={network}&id=5` を指定します。

* キャンペーン設定に「[!UICONTROL EF Redirect]」および「自動アップロード」が含まれる場合に適用されるAdobe Advertising コンバージョントラッキングの場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のクリック追跡コードが自動的にプレフィックス付けされます。

* 最終的な URL を埋め込むためのサポート対象パラメーターについては、（[!DNL Microsoft Advertising] のみ） [[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/56799) または（[!DNL Google Ads] のみ） [[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/6305348) の「利用可能なテンプレートのパラメーター」の節の「トラッキ [!DNL ValueTrack] グテンプレートのみ」パラメーターを参照してください。

* オプションで、URL パラメーターと、キャンペーンに定義されたカスタムパラメーターをアンパサンド（&amp;）で区切ったもの（`{lpurl}?matchtype={matchtype}&device={device}` など）を含めることができます。

* オプションで、サードパーティのリダイレクトとトラッキングを追加できます。

>[!NOTE]
>
>* キャンペーン設定に「[!UICONTROL EF Redirect]」および「[!UICONTROL Auto Upload]」が含まれている場合、検索、ソーシャルおよびCommerceでは、レコードを保存すると、独自のリダイレクトおよびトラッキングコードが自動的にプレフィックス付けされます。
>* 最も詳細なレベルの追跡テンプレートは、それより上のすべてのレベルの値を上書きします。 例えば、アカウント設定とキーワード設定の両方に値が含まれている場合、キーワード値が適用されます。
>* （[!DNL Google Ads]） サイトリンクまたはキーワードレベルでトラッキングテンプレートを更新すると、関連する広告がレビュー用に再送信されます。 広告を承認用に再送信しなくても、アカウント、キャンペーン、広告グループのレベルでトラッキングテンプレートを更新できます。
>* （[!DNL Microsoft Advertising]）広告を承認用に再送信しなくても、任意のレベルでトラッキングテンプレートを更新できます。
>* [!DNL Google Ads] えば、並列トラッキングを有効にするソースからのクリックに置き換わらないマクロを使用しないでください。 広告主がマクロを使用する必要がある場合、Adobe アカウントチームはカスタマーサポートまたは実装チームと協力して、マクロを追加する必要があります。

>[!MORELIKETHIS]
>
>* [ サイトリンク拡張機能について ](sitelink-extension-about.md)
>* [ 共有サイトリンクのアカウント、キャンペーンおよび広告グループへの関連付け ](sitelink-extension-associate.md)
