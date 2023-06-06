---
title: '"[!DNL Google Ads] 呼び出しのみの広告設定»'
description: 次の設定を参照してください： [!DNL Google Ads] 呼び出しのみの広告。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 0%

---

# [!DNL Google Ads] 呼び出しのみの広告設定

検索ネットワークを使用するキャンペーンに対して、呼び出しのみのテキスト広告を作成できます。

検索、ソーシャル、コマースは、アカウントレベルのランディングページのサフィックスとトラッキングテンプレートを使用して、呼び出しのみの広告を追跡しますが、オプションで、 [!DNL Google Ads] 管理者。

詳しくは、 [!DNL Google Ads] のヘルプ [アカウントごとの広告制限](https://support.google.com/google-ads/answer/6372658?hl=en).

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** ビジネスの名前。 最大長は 25 文字または 2 バイト文字 12 文字です。

**[!UICONTROL Country]:** （オプション）事業所の国。

**[!UICONTROL Phone Number]:** ビジネスの電話番号。 例：(124) 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1], [!UICONTROL Description 2]:** 広告の本文の最初の行と 2 番目の行。 各行の最大長は 35 文字または 17 文字の全角文字です。

キーワード置換構文は最大長にカウントされません。 例：`{Description1: Free Account Analysis!}`&quot;は 22 文字として扱われます（&quot;無料アカウント分析\!&quot;の部分のみ）。

>[!NOTE]
>
>説明フィールドに電話番号を含めることはできません。

**[!UICONTROL Display URL]:** 広告に表示される URL。 ディスプレイ URL は、お客様のビジネスに関連付けられたドメインと一致する必要がありますが、広告は、ランディングページにユーザーを送信しません。

最大の長さは、1 バイト文字で 35 文字または 2 バイト文字で 17 文字です。 キーワード置換構文は最大長にカウントされません。 例：`{DisplayURL: example.com}`&quot;は 11 文字として扱われます（&quot;example.com&quot;部分のみ）。

**[!UICONTROL Verification URL]:** （オプション）広告の電話番号をテキストとして表示し、 [!DNL Google Ads] は、電話番号が有効であることを確認できます。 広告の表示 URL と同じドメインを持つ必要があります。

**[!UICONTROL Is Tracked]:** コールトラッキングおよびコールのみのコンバージョンを有効にします。

**[!UICONTROL Count calls as phone call conversions]:** (「[!UICONTROL Is Tracked]」が選択されている場合、（オプション）広告によって生成されるすべての呼び出しを、特定のタイプの電話コンバージョンに属性付けします（指定されている場合）。 それ以外の場合は、 [!DNL Google Ads] は、「[!UICONTROL Calls from ads]」は、転送番号からのコンバージョンを少なくとも 1 回記録した後、を呼び出す属性を設定します。

**[!UICONTROL Count Action]:** (「[!UICONTROL Count calls as phone call conversions]」が選択されている場合、（オプション）呼び出しの属性を持つ既存のコンバージョンアクション。

コンバージョンアクションは、 [!DNL Google Ads].

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [広告について](ad-about.md)
>* [広告の管理](ad-manage.md)
>* [[!DNL Google Ads] 拡張された動的検索広告設定](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] レスポンシブ検索広告設定](ad-settings-google-rsa.md)

