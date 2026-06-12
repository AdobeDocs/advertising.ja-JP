---
title: '[!DNL Google Ads]件の呼び出し専用の広告設定'
description: ' [!DNL Google Ads] 呼び出し専用の広告の設定を参照します。'
exl-id: 10672771-53fd-4ce9-9d67-6b1f8f5a41b8
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/KtnceFJbgZ-jPcNzl1c6XychNzr4tOIs5B9mMbXegxo
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 351
ht-degree: 0%

---

# [!DNL Google Ads]件の呼び出し専用の広告設定

検索ネットワークを使用するキャンペーンでは、呼び出し専用のテキスト広告を作成できます。

Search, Social, &amp; Commerceでは、アカウントレベルのランディングページのサフィックスとトラッキングテンプレートを使用して呼び出し専用の広告をトラッキングしますが、[!DNL Google Ads] Manager内の広告レベルでアカウントレベルのトラッキングをオプションで上書きできます。

アカウントごとの[広告制限](https://support.google.com/google-ads/answer/6372658?hl=en)について、[!DNL Google Ads]のヘルプを参照してください。

<!-- ## Call-only Ad -->

<!-- hiding section header since there's only one section -->

**[!UICONTROL Business Name]:** ビジネスの名前。 最大長は25文字または2 バイト文字12文字です。

**[!UICONTROL Country]:** （オプション）会社が所在する国。

**[!UICONTROL Phone Number]:** ビジネスの電話番号。 例：（124） 123-4567、12345678901、+441234567890。

**[!UICONTROL Description 1], [!UICONTROL Description 2]:**&#x200B;広告の本文の1行目と2行目。 各行の最大長は35文字または2 バイト文字17文字です。

キーワード置換構文は、最大長にカウントされません。 例えば、「`{Description1: Free Account Analysis!}`」は22文字として扱われます（「無料アカウント分析」の部分のみ）。

>[!NOTE]
>
>説明フィールドには電話番号を含めることはできません。

**[!UICONTROL Display URL]:**&#x200B;広告に表示されるURL。 表示URLは、ビジネスに関連付けられているドメインと一致する必要がありますが、広告がランディングページにユーザーを送信することはありません。

最大長は35個の1 バイトまたは17個の2 バイト文字です。 キーワード置換構文は、最大長にカウントされません。 例えば、「`{DisplayURL: example.com}`」は11文字として扱われます（「example.com」部分のみ）。

**[!UICONTROL Verification URL]:** （オプション）広告の電話番号がテキストとして表示されるweb ページです。これにより、[!DNL Google Ads]は電話番号が有効であることを確認できます。 広告の表示URLと同じドメインである必要があります。

**[!UICONTROL Is Tracked]:**&#x200B;呼び出しトラッキングと呼び出し専用コンバージョンを有効にします。

**[!UICONTROL Count calls as phone call conversions]:** （「[!UICONTROL Is Tracked]」が選択されている場合。オプション）広告から発生するすべての通話を、特定の種類の電話変換に属性として指定します。 それ以外の場合、[!DNL Google Ads]は、転送番号から少なくとも1つのコンバージョンを記録し、そのコンバージョンに対する呼び出しを属性として、「[!UICONTROL Calls from ads]」というデフォルトのコンバージョンアクションを作成します。

**[!UICONTROL Count Action]:** （「[!UICONTROL Count calls as phone call conversions]」が選択されている場合。オプション）呼び出しの原因となる既存のコンバージョンアクション。

[!DNL Google Ads]内でコンバージョンアクションを作成および管理できます。

<!-- **[!UICONTROL Status]:** -->

{{$include /help/_includes/status-ad.md}}

>[!MORELIKETHIS]
>
>* [広告について](ad-about.md)
>* [広告の管理](ad-manage.md)
>* [[!DNL Google Ads] 動的検索広告設定を拡張](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  レスポンシブ検索の広告設定](ad-settings-google-rsa.md)
