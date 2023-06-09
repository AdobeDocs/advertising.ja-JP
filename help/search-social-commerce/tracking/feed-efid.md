---
title: EF ID フィードを使用したコンバージョントラッキング
description: コンバージョントラッキングデータでの EF ID フィードの使用について説明します。
source-git-commit: 46e918418bf2e5c412efa8825dda22bc1953e439
workflow-type: tm+mt
source-wordcount: '354'
ht-degree: 0%

---

# EF ID フィードを使用したコンバージョントラッキング

この方法では、Advertising Cloudは `ef_id` ユーザーがランディングページをクリックして到達するたびに値が返され、広告主が `ef_id` の値を含めてデータフィードに送信する必要があります。

## 実装の概要

*代理店のアカウントマネージャー [!DNL Adobe] アカウントマネージャー、管理者ユーザーロールのみ*

1. アカウントまたはキャンペーントラッキングオプションを使用する」[!UICONTROL EF Redirect]」、「[!UICONTROL Token],&quot;および&quot;[!UICONTROL Auto Upload]」をクリックします。

   >[!NOTE]
   >* このメソッドでは、広告主がAdobe Advertisingのコンバージョントラッキングタグを使用する必要はありません。
   >* 既存のアカウントまたはキャンペーンのリダイレクトタイプをから切り替える場合 [!UICONTROL Standard] から [!UICONTROL Token]またはその逆の場合は、該当するすべてのトラッキング URL を再生成する必要があります。

   ef_id は、エンドユーザーが広告をクリックし、Adobe Advertisingサーバーにリダイレクトされると設定され、ランディングページの URL に追加されます。 ef_id は、広告主の宛先 URL または広告またはキーワードの最終 URL で渡されます。 次に、リダイレクト時に広告主に渡されるリンク先 URL の例を示します。

   `http://pixel.everesttech.net/1180/cq?ev_sid=3&ev_ln={keyword}&ev_crx={creative}&ev_mt={matchtype}&ev_n={network}&ev_ltx=&ev_pl={placement}&url=http%3A//www.example.com&ef_id=D59Nu0u@BD0AAM1q:20110630172936:s`

1. 広告主は、リダイレクトから ef_id を抽出し、フィードファイルに含める関連するコンバージョンデータと共に保存します。 ef_id を変更したり、大文字と小文字を変更したりしないでください。

1. （オプション、推奨）広告主は、フィードファイルに含めるトランザクションごとに一意のトランザクション ID を作成できます。

1. 広告主が、 [必要なコンバージョンデータ](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md) を指定したサーバーの場所に追加します。

1. テクニカルサービスは、アップロードされたファイルのコンバージョンデータを解析し、そのデータをAdobe広告にアップロードします。 Adobe Advertisingは、個々のキーワード、広告およびプレースメントに対してデータを追跡し、それぞれの売上高予測を作成します。

1. テクニカルサービスは、処理されたデータをフィードデータと照合して検証し、 [孤立トランザクション](/help/search-social-commerce/glossary.md#o-p).

>[!MORELIKETHIS]
>
>* [コンバージョンフィードファイルのファイル要件](feed-file-requirements.md)
>* [EF ID を使用したデータフィードのデータ要件](/help/search-social-commerce/tracking/feed-ef-id-data-requirements.md)


