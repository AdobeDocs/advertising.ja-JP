---
title: 広告ネットワークとオブジェクトでクリックトラッキング URLを生成するタイミングと方法
description: クリックトラッキング URLが自動的に追加されるタイミングと、様々なキャンペーンコンポーネントに対してURLを手動で追加する方法について説明します。
exl-id: 896de0c1-75ed-450c-b995-893f1a63e5ce
feature: Search Tracking
TQID: https://experienceleague.adobe.com/coG6SeshFIDQwfuv5RNK3Q9dhLdj4uXzl0bZs4syil8
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a65752f7baeae4193fe55d2f8b9f7a78b126ef06
workflow-type: tm+mt
source-wordcount: 905
ht-degree: 0%

---

# 広告ネットワークとオブジェクトでクリックトラッキング URLを生成するタイミングと方法

次の表に、様々なキャンペーンコンポーネントのクリックトラッキング URLを生成する方法を示します。

| 広告ネットワーク | コンポーネント | クリックトラッキング URLの生成方法 |
| ---- | ---- | ---- |
| [!DNL Baidu]、[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]および[!DNL Yandex] | <ul><li>テキスト広告</li><li>キーワード</li><li>（[!DNL Google Ads]件のコンテンツキャンペーン）プレースメント</li><li>（[!DNL Google Advertising]と[!DNL Advertising]） サイトリンク</li></ul> | アクティブなキャンペーンのトラッキング設定にオプション「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」（キャンペーンレベルで設定するか、アカウント設定から継承）が含まれている場合、広告グループコンポーネントのトラッキング URLを生成する必要はありません。 Search, Social, &amp; Commerceは、次の種類のトラッキング URLを自動的に作成し、アドネットワークと同期するたびにアドネットワークにアップロードします。a） （最終URLを持つアカウント） トラッキングテンプレート用のSearch, Social, &amp; Commerce トラッキングパラメーターと、最終URLに追加された同じパラメーター、b） （宛先URLを持つアカウント）新しい宛先URLにSearch, Social, &amp; Commerce トラッキングコードと埋め込まれたc） （[!DNL Google Ads] アカウントと[!DNL Microsoft Advertising] アカウント） ランディングページ サフィックス （最終URL サフィックス） パラメーター）。<br><br> [!UICONTROL Auto Upload] オプションが無効になっている場合は、次のいずれかの方法でコンポーネントのトラッキング URLを生成できます。<ul><li>（[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Ads]および[!DNL Yandex]）フィード ファイルから広告を投稿する場合は、[!UICONTROL Generate Tracking URLs] オプションを選択します。 必要に応じて、広告ネットワークに投稿する前に、任意のバルクシートファイルのトラッキングテンプレートフィールドを検証できます。</li><li>コンポーネントを含むバルクシート ファイルをダウンロード、アップロード、または投稿する場合は、[!UICONTROL Generate Tracking URLs] オプションを選択します。 宛先URLを持つアカウントの場合は、オプションで、ファイルを広告ネットワークに投稿する前に基本URL/最終URL フィールドを検証できます</li><li>[[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、適切な[!UICONTROL Tracking Template]または[!UICONTROL Base URL] フィールドに手動で追加します。 <b>注意：</b>生成するトラッキングテンプレートには、アカウントまたはキャンペーンの設定で指定された追加のトラッキングパラメーターは含まれていません。<ul><li>Google アカウント） [[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)に移動し、適切な[!UICONTROL Tracking Template] フィールドに画面上の値をコピーして、トラッキング文字列全体をコンポーネント設定に手動で追加します。 `&url=` パラメーター（`{lpurl}`など）の後の最終的なURLには、[!DNL Google Ads] [!DNL ValueTrack] パラメーターを追加する必要があります。 トラッキングテンプレートの最終的なURLを示す[!DNL ValueTrack] パラメーターのリストについては、[[!DNL Google Ads] ドキュメント ]9https://support.google.com/google-ads/answer/2375447の「使用可能な[!DNL ValueTrack] パラメーター」の節の「トラッキングテンプレートのみ」パラメーターを参照してください。</li><li>（最終的なURLを持つ他のアカウント） [[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、トラッキング文字列全体をコンポーネント設定に手動で追加します。 `&url=` パラメーター（`{lpurl}`など）の後に、最終的なURLのパラメーターを追加する必要があります。 [!DNL LY Ads] アカウントの場合は、パラメーター`{lpurl}`を使用します。 トラッキングテンプレートの最終的なURLを示す[!DNL Microsoft Advertising] パラメーターのリストについては、[[!DNL Microsoft Advertising]  ドキュメント ](https://help.bingads.microsoft.com/#apex/3/en/56799)を参照してください。</li><li>（宛先URLを持つアカウント） [[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、適切な[!UICONTROL Base URL] フィールドにトラッキング URLを手動で追加します。</li></ul></li></ul><b> メモ：</b><br><br><ul><li>（最終URLを持つアカウント）最も詳細なレベルでトラッキングテンプレートが使用されます（例えば、キーワードレベルのトラッキングテンプレートはアカウント、キャンペーン、広告のグループレベルのテンプレートを上書きし、キーワードとプレースメントのトラッキングテンプレートは関連する広告のテンプレートを上書きします）。</li><li>Adobe Advertisingは、サイトリンクのクリック数と売上を、サイトリンクが含まれている広告に関連付けられているキーワードにマッピングします。サイトリンクの売上は個別にマッピングされません。 「[ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)」を参照してください。</li></ul><b> ヒント：</b> （最終URLを持つアカウント）追跡は、必要な最高レベルでのみ追跡テンプレートを作成する場合（例：アカウントレベルまたはキャンペーンレベルの追跡テンプレートを作成して、アカウントまたはキャンペーン内のすべてのエンティティに同じ追跡を適用する場合など）に最も簡単に管理できます。 |
| [!DNL Google Ads] | 電話の拡張機能 | なし |
| [!DNL Google Ads], [!DNL Microsoft Advertising] | 製品広告 | <ul><li>[!DNL Microsoft Merchant Center] アカウント：ショッピング広告](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)の[ トラッキングテンプレート形式を使用して、[!DNL Microsoft Merchant Center] アカウント内の各製品のトラッキング URLを手動で作成し、アカウント、キャンペーン、または製品グループの設定の[!UICONTROL Tracking Template] フィールドに手動で追加します。<br><br>または、[!DNL Microsoft Merchant Center account]内の製品データにトラッキング URLを追加できます。 これを行うには、トラッキング URLと、必要に応じて、製品フィード ](https://help.ads.microsoft.com/#apex/3/en/51084)内の[ カスタム列「[!DNL bingads_redirect]」に「[!DNL link]」または「[!DNL mobile_link]」フィールドの値を含めます。 「[!DNL bingads_redirect]」フィールドの値は、「[!DNL link]」および「[!DNL mobile_link]」フィールドの値に置き換わります。 この方法で生成されたURLには、アカウント設定で指定されたトラッキングパラメーターが含まれていません。<br><br><b>注：</b>同期中にトラッキングを自動的にアップロードするアカウントレベルおよびキャンペーンレベルの機能では、新しい[!DNL Microsoft Advertising]製品グループのトラッキングは生成されません。 回避策は、バルクシートをアップロードまたは投稿するときにトラッキングを生成することです。</li><li>[!DNL Google Merchant Center] アカウント：[[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、アカウント、キャンペーン、または製品グループの設定の[!UICONTROL Tracking Template] フィールドに手動で追加します。</li></ul> |
| [!DNL Naver] | キーワード | [ バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用して、すべての広告のクリック追跡を設定できます。 または、広告のトラッキング URLを手動で生成し、広告ネットワークのエディターを使用して広告設定に手動で追加することもできます。 「[実装 [!DNL Naver]  トラッキング専用アカウント ](/help/search-social-commerce/campaign-management/naver-tracking-only-account-implement.md)」を参照してください。 |
| [!DNL Yahoo DSP] | テキスト広告とディスプレイ広告 | アクティブなキャンペーンのトラッキング設定にオプション「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」（キャンペーンレベルで設定するか、アカウント設定から継承）が含まれている場合、広告のトラッキング URLを生成する必要はありません。 Search, Social, &amp; Commerceは、トラッキングコードが埋め込まれた新しいリンク先URLを自動的に作成し、広告ネットワークに同期するたびにアップロードします。<br><br> [!UICONTROL Auto Upload] オプションが無効になっている場合、[[!UICONTROL Tracking URLs] ツール ](/help/search-social-commerce/tools/click-tracking-url-generate.md)を使用してトラッキング URLを生成し、広告ネットワークのエディターを使用して広告設定に手動で追加できます。 |

>[!MORELIKETHIS]
>
>* [ トラッキング URL ツールを使用して、検索、ソーシャル、Commerceのクリック トラッキング URLを生成](/help/search-social-commerce/tools/click-tracking-url-generate.md)
>* [ バルクシートを使用したキャンペーンデータの管理について](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)
>* [ サポートされているインベントリ ](/help/search-social-commerce/introduction/supported-inventory.md)
>* [Cookie ベースのクリックの追跡を設定](/help/search-social-commerce/tracking/click-tracking-set-up.md)
