---
title: データソースを設定するため  [!DNL Google Analytics]  前提条件
description: データソースを設定する前に完了する必要がある手順  [!DNL Google Analytics]  ついて説明します。
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '402'
ht-degree: 0%

---

# [!DNL Google Analytics] データソースを設定するための前提条件

[!DNL Google Analytics] データソースを設定する前に、Search、Social、Commerceの各クエリ文字列パラメーター「ef_id」をプライマリキーとして設定し、[!DNL Google Analytics] から Search、Social、Commerceにデータを渡す必要があります。 同期データが必要な [!DNL Google Analytics] アカウントとプロパティの組み合わせごとにプライマリキーを設定します。 組織内の他のユーザーが、これらのタスクを完了する必要がある場合があります。詳しくは、以下を参照してください。

広告またはキーワードのランディングページ URL に、検索、ソーシャル、Commerceのリダイレクトがまだ含まれていない場合は、それらを最初に追加します。

## 前提条件 1：該当するすべての広告アカウントのランディングページ URL に検索、ソーシャル、Commerceトークン（「ef_id」クエリ文字列パラメーター）を実装する

関連するキャンペーンの各有料検索クリック時に、一意の `ef_id` を生成し、`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s` などのクエリ文字列としてランディングページ URL に追加する必要があります。ここで、`&ef_id=abcde:123456789:s` は追加記号、`ef_id` キー、`ef_id` 値です。 ef_id を含めるには、関連する広告ネットワークアカウントおよびキャンペーンに [!UICONTROL Tracking Type] 「[!UICONTROL EF Redirect]」と [!UICONTROL Redirect Type] 「[!UICONTROL Token]」が必要です。

既存のアカウントおよびキャンペーンの場合、ef_id はおそらく既に実装されています。

ef_id が含まれていない場合は、Adobeアカウントチームにお問い合わせください。

すべての前提条件が満たされた場合、`ef_id` は、[!DNL Google Analytics] から検索、ソーシャルおよびCommerceにデータを渡すためのプライマリキーとして使用されます。

## 前提条件 2：関連する各 [!DNL Google Analytics] プロパティのカスタムディメンションで検索、ソーシャル、Commerceのトークン（「ef_id」クエリ文字列パラメーター）を取得する

データを同期する [!DNL Google Analytics] アカウントとプロパティの組み合わせごとに、次のタスクを繰り返します。 これらのタスクに関するヘルプについては、[[!DNL Google Analytics]  カスタムディメンションの作成と実装に関するドキュメント &#x200B;](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) を参照してください。

1. [!DNL Google Analytics] で、「`ef_id`」という名前のカスタムディメンションを作成します。 ディメンションの範囲を [!DNL User] に設定し、ディメンションをアクティブに設定します。

   >[!NOTE]
   >
   >この前提条件では、関連するプロパティに対する編集権限が必要です。

1. [!DNL Google Analytics] トラッキングコードを更新し、ef_id クエリ文字列パラメーターがランディングページの URL に存在する場合はその値を取得し、ef_id カスタムディメンションに保存します。

   >[!NOTE]
   >
   >ef_id は、ランディングページの URL 内にのみ設定してください。

   例えば、ランディングページの URL が `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf` の場合、[!DNL Google Analytics] の ef_id ディメンションの値は `abcde:123456789:s` になります。

   >[!NOTE]
   >
   >この前提条件は、資格のある開発者が完了する必要があります。

>[!MORELIKETHIS]
>
>* [&#x200B; 同期  [!DNL Google Analytics]  コンバージョン指標について &#x200B;](data-source-about.md)
>* [&#x200B; データソースとして  [!DNL Google Analytics]  ビューを設定する &#x200B;](data-source-configure.md)
>* [&#x200B; データソース  [!DNL Google Analytics]  編集 &#x200B;](data-source-edit.md)
>* [&#x200B; データソースの同期の一時停止 &#x200B;](data-source-pause.md)
>* [&#x200B; データソース  [!DNL Google Analytics]  再認証 &#x200B;](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定 &#x200B;](data-source-settings.md)
>* [&#x200B; 付録 – 利用可能  [!DNL Google Analytics]  指標 &#x200B;](data-source-ga-metrics.md)
