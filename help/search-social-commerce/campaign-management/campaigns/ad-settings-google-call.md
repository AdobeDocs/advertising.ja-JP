---
title: '[!DNL Google Ads] 呼び出し専用広告設定'
description: 呼び出し専用広告の設定  [!DNL Google Ads]  参照します。
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '333'
ht-degree: 0%

---

# [!DNL Google Ads] 呼び出し専用広告設定

検索ネットワークを使用するキャンペーンに対して、呼び出し専用のテキスト広告を作成できます。

検索、ソーシャル、Commerceでは、アカウントレベルのランディングページ接尾辞とトラッキングテンプレートを使用して、呼び出し専用広告を追跡しますが、[!DNL Google Ads] Manager 内の広告レベルでアカウントレベルのトラッキングを上書きすることもできます（オプション）。

[ アカウントごとの広告制限 ](https://support.google.com/google-ads/answer/6372658?hl=en) については、[!DNL Google Ads] のヘルプを参照してください。

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** ビジネスの名前。 最大長は 25 文字、つまり 12 個の 2 バイト文字です。

**[!UICONTROL Country]:** （オプション）ビジネスが所在する国。

**[!UICONTROL Phone Number]:** ビジネスの電話番号。 例：（124） 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** 広告の本文の最初と 2 番目の行。 各行の最大長は 35 文字または 17 個の 2 バイト文字です。

キーワード置換構文が、最大長にカウントされません。 例えば、「`{Description1: Free Account Analysis!}`」は 22 文字として扱われます（「フリーアカウント分析」の部分のみ）。

>[!NOTE]
>
>説明フィールドに電話番号を含めることはできません。

**[!UICONTROL Display URL]:** 広告に表示される URL。 ディスプレイ URL は、ビジネスに関連付けられているドメインと一致する必要がありますが、広告はユーザーをランディングページに送信しません。

最大長は 35 個の 1 バイト文字または 17 個の 2 バイト文字です。 キーワード置換構文が、最大長にカウントされません。 例えば、「`{DisplayURL: example.com}`」は 11 文字として扱われます（「example.com」の部分のみ）。

**[!UICONTROL Verification URL]:** （オプション）電話番号が有効であることを確認で [!DNL Google Ads] るように、広告の電話番号がテキストとして表示される Web ページ。 広告の表示 URL と同じドメインが必要です。

**[!UICONTROL Is Tracked]:** コールトラッキングとコールのみのコンバージョンを有効にします。

**[!UICONTROL Count calls as phone call conversions]:** （「[!UICONTROL Is Tracked]」を選択した場合。オプション）広告から生じるすべての通話を、特定のタイプの通話コンバージョンに関連付けます（1 つ指定した場合）。 それ以外の場合、[!DNL Google Ads] では、転送番号からの少なくとも 1 つのコンバージョンを記録した後、そのコンバージョンへの呼び出しを属性すると、「[!UICONTROL Calls from ads]」と呼ばれるデフォルトのコンバージョンアクションを作成します。

**[!UICONTROL Count Action]:** （「[!UICONTROL Count calls as phone call conversions]」を選択した場合。オプション）呼び出しの属性となる既存のコンバージョンアクション。

[!DNL Google Ads] 内でコンバージョンアクションを作成および管理できます。

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [ 広告について ](ad-about.md)
>* [ 広告の管理 ](ad-manage.md)
>* [[!DNL Google Ads]  拡張された動的検索広告設定 ](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  レスポンシブ検索広告設定 ](ad-settings-google-rsa.md)
