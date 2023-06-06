---
title: EF ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータでの EF ID フィードの使用について説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 0%

---

# EF ID フィードを使用したコンバージョントラッキング

この方法では、Advertising Cloudは `ef_id` ユーザーがランディングページをクリックして到達するたびに値が返され、広告主が `ef_id` の値を含めてデータフィードに送信する必要があります。

## 実装の概要

*代理店のアカウントマネージャー [!DNL Adobe] アカウントマネージャー、管理者ユーザーロールのみ*

1. アカウントまたはキャンペーントラッキングオプションを使用する」[!UICONTROL EF Redirect]」、「[!UICONTROL Token],&quot;および&quot;[!UICONTROL Auto Upload]「 」：アカウントまたはキャンペーン内の各Adobeのキーワードの広告トークン (ef_id) または広告（広告レベルのトラッキング用）を使用して、宛先 URL または最終 URL を自動的に生成します。

   >[!NOTE]
   >* このメソッドでは、広告主がAdobe広告のコンバージョントラッキングタグを使用する必要はありません。
   >* 既存のアカウントまたはキャンペーンのリダイレクトタイプをから切り替える場合 [!UICONTROL Standard] から [!UICONTROL Token]またはその逆の場合は、該当するすべてのトラッキング URL を再生成する必要があります。


   ef_id は、エンドユーザーが広告をクリックし、Adobe広告サーバーにリダイレクトされると設定され、ランディングページ URL に追加されます。 ef_id は、広告主の宛先 URL または広告またはキーワードの最終 URL で渡されます。 次に、リダイレクト時に広告主に渡されるリンク先 URL の例を示します。

   http://pixel.everesttech.net/1180/cq?ev_sid=3&amp;ev_ln={keyword}&amp;ev_crx={creative}&amp;ev_mt={matchtype}&amp;ev_n={network}&amp;ev_ltx=&amp;ev_pl={placement}&amp;url=http%3A//www.example.com&amp;ef_id=D59Nu0u@BD0AAM1q:20110630172936:s

1. 広告主は、リダイレクトから ef_id を抽出し、フィードファイルに含める関連するコンバージョンデータと共に保存します。 ef_id を変更したり、大文字と小文字を変更したりしないでください。

1. （オプション、推奨）広告主は、フィードファイルに含めるトランザクションごとに一意のトランザクション ID を作成できます。

1. 広告主が、 [必要なコンバージョンデータ](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) を指定したサーバーの場所に追加します。

1. テクニカルサービスは、アップロードされたファイルのコンバージョンデータを解析し、そのデータをAdobe広告にアップロードします。 Adobe広告は、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [コンバージョンフィードファイルのファイル要件](feed-file-requirements.md)
>* [EF ID を使用したデータフィードのデータ要件](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)



