---
title: ' [!DNL Google Analytics]  データソースを設定するための前提条件'
description: ' [!DNL Google Analytics]  データソースを設定する前に完了する必要がある手順について説明します。'
role: User, Admin
exl-id: 97b0c149-5f82-4a1e-a5d9-aeab43cbd88f
feature: Search Admin, Search Data Sources
TQID: https://experienceleague.adobe.com/viBRqiwqJm2BabtLP7b3h1TMTjkeITeSVA1vMMmbrPY
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: e55292b5-d4a1-4c98-9c20-2a2c5bea07fb
subfeature_v2: id: e778848d-90fa-4520-b80f-e8dd7dfdcffc
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 402
ht-degree: 0%

---

# [!DNL Google Analytics] データソースを設定するための前提条件

[!DNL Google Analytics] データソースを設定する前に、[!DNL Google Analytics]からSearch, Social, &amp; Commerceにデータを渡すプライマリキーとして、Search, Social, &amp; Commerce クエリ文字列パラメーター「ef_id」を設定する必要があります。 データを同期する[!DNL Google Analytics] アカウントとプロパティの組み合わせごとにプライマリキーを設定します。 組織内の他のユーザーがこれらのタスクを完了する必要がある場合があります。詳しくは、以下を参照してください。

広告またはキーワードのランディングページ URLに、検索、ソーシャル、Commerceのリダイレクトがまだ含まれていない場合は、最初に追加します。

## 前提条件1：該当するすべての広告アカウントのランディングページ URLにSearch, Social, &amp; Commerce トークン（「ef_id」クエリ文字列パラメーター）を実装する

関連するキャンペーンの有料検索クリックごとに、一意の`ef_id`を生成し、クエリ文字列（`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`など）としてランディングページ URLに追加する必要があります。ここで、`&ef_id=abcde:123456789:s`は追加記号、`ef_id` キー、`ef_id`値です。 ef_idを含めるには、関連する広告ネットワークアカウントとキャンペーンに[!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]&quot;と[!UICONTROL Redirect Type] &quot;[!UICONTROL Token]&quot;が必要です。

既存のアカウントとキャンペーンの場合、ef_idはおそらく既に実装されています。

ef_idが含まれていない場合は、Adobe アカウントチームにお問い合わせください。

すべての前提条件が完了すると、プライマリキーとして`ef_id`が使用され、[!DNL Google Analytics]からSearch, Social, &amp; Commerceにデータが渡されます。

## 前提条件2：関連する各[!DNL Google Analytics] プロパティのカスタムディメンションで、Search、Social、およびCommerce トークン（「ef_id」クエリ文字列パラメーター）をキャプチャする

データを同期する[!DNL Google Analytics] アカウントとプロパティの組み合わせごとに、次のタスクを繰り返します。 これらのタスクのヘルプについては、[[!DNL Google Analytics]  カスタムディメンションの作成と実装に関するドキュメント ](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article)を参照してください。

1. [!DNL Google Analytics]で、「`ef_id`」という名前のカスタムディメンションを作成します。 ディメンションの範囲を[!DNL User]に設定し、ディメンションをアクティブに設定します。

   >[!NOTE]
   >
   >この前提条件には、関連するプロパティの編集権限が必要です。

1. ランディングページ URLにef_id クエリ文字列パラメーターが存在する場合は、その値を取得し、ef_id カスタムディメンションに保存するように、[!DNL Google Analytics] トラッキングコードを更新します。

   >[!NOTE]
   >
   >ef_idは、ランディングページ URL内でのみ使用する必要があります。

   例えば、ランディングページ URLが`https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`の場合、[!DNL Google Analytics]のef_id ディメンションの値は`abcde:123456789:s`です。

   >[!NOTE]
   >
   >この前提条件は、適格な開発者が完了する必要があります。

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics]  コンバージョン指標](data-source-about.md)
>* [ データソースとして [!DNL Google Analytics]  ビューを設定](data-source-configure.md)
>* [ データソースの編集 [!DNL Google Analytics] ](data-source-edit.md)
>* [ データソースの同期を一時停止](data-source-pause.md)
>* [ データソースを再認証 [!DNL Google Analytics] します](data-source-reauthenticate.md)
>* [[!DNL Google Analytics]  データソース設定](data-source-settings.md)
>* [付録 – 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)
