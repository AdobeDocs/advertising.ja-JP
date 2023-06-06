---
title: の設定の前提条件 [!DNL Google Analytics] データソース
description: を設定する前に完了する必要がある手順について説明します。 [!DNL Google Analytics] データソース。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '417'
ht-degree: 0%

---

# の設定の前提条件 [!DNL Google Analytics] データソース

事前に [!DNL Google Analytics] データソースを使用する場合は、データを渡す主キーとして、Search、Social および&amp; Commerce クエリー文字列パラメーター&quot;ef_id&quot;を設定する必要があります。 [!DNL Google Analytics] 検索、ソーシャル、コマースに追加します。 それぞれにプライマリキーを設定 [!DNL Google Analytics] 同期するデータのアカウントとプロパティの組み合わせ。 組織内の他のユーザーがこれらのタスクを完了する必要が生じる場合があります。詳しくは、以下を参照してください。

広告やキーワードのランディングページ URL に検索、ソーシャル、コマースのリダイレクトが含まれていない場合は、最初に追加します。

## 前提条件 1:すべての適用可能な広告アカウント用のランディングページ URL に検索、ソーシャル、コマーストークン（「ef_id」クエリー文字列パラメーター）を実装する

各有料検索で、関連するキャンペーンをクリックすると、 `ef_id` は、生成され、次のようなクエリ文字列としてランディングページ URL に追加される必要があります。 `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s`で、 `&ef_id=abcde:123456789:s` は追加記号で、 `ef_id` キーと `ef_id` の値です。 ef_id を含めるには、関連する広告ネットワークアカウントおよびキャンペーンに [!UICONTROL Tracking Type] &quot;[!UICONTROL EF Redirect]「と [!UICONTROL Redirect Type] &quot;[!UICONTROL Token].&quot;

既存のアカウントおよびキャンペーンの場合、ef_id は既に実装されている可能性があります。

ef_id が含まれていない場合は、担当のAdobeアカウントチームに質問してください。

すべての前提条件が完了したら、 `ef_id` は、からデータを渡すためのプライマリキーとして使用されます [!DNL Google Analytics] 検索、ソーシャル、コマースに追加します。

## 前提条件 2:各関連するカスタムディメンションに検索、ソーシャル、コマースのトークン（「ef_id」クエリー文字列パラメーター）を取り込む [!DNL Google Analytics] プロパティ

それぞれに対して、次のタスクを繰り返します [!DNL Google Analytics] データを同期するアカウントとプロパティの組み合わせ。 詳しくは、 [[!DNL Google Analytics] カスタムディメンションの作成と実装に関するドキュメント](https://support.google.com/analytics/answer/2709829?hl=en#zippy=%2Cin-this-article) を参照してください。

1. In [!DNL Google Analytics]、「`ef_id`&quot;. ディメンションの範囲をに設定します。 [!DNL User]をクリックし、次元をアクティブに設定します。

   >[!NOTE]
   >
   >この前提条件では、関連するプロパティの編集権限が必要です。

1. の更新 [!DNL Google Analytics] トラッキングコードを使用して、ef_id クエリー文字列パラメーターの値をランディングページの URL に存在する場合にその値を取り込み、ef_id カスタムディメンションに保存します。

   >[!NOTE]
   >
   >ef_id はランディングページの URL にのみ使用してください。

   例えば、ランディングページの URL が `https://www.adobe.com?someParam=123&ef_id=abcde:123456789:s&anotherParam=asdf`の場合は、 [!DNL Google Analytics] が `abcde:123456789:s`.

   >[!NOTE]
   >
   >この前提条件は、適格な開発者が満たす必要があります。

>[!MORELIKETHIS]
>
>* [同期について [!DNL Google Analytics] コンバージョン指標](data-source-about.md)
>* [の設定 [!DNL Google Analytics] データソースとして表示](data-source-configure.md)
>* [の編集 [!DNL Google Analytics] データソース](data-source-edit.md)
>* [データソースの同期を一時停止する](data-source-pause.md)
>* [の再認証 [!DNL Google Analytics] データソース](data-source-reauthenticate.md)
>* [[!DNL Google Analytics] データソース設定](data-source-settings.md)
>* [付録 — 利用可能 [!DNL Google Analytics] 指標](data-source-ga-metrics.md)

