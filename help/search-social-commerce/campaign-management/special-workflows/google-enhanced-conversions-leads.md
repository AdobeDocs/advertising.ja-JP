---
title: リードの強化されたコンバージョンを [!DNL Google Ads] 実装する
description: リードの拡張コンバージョンを設定する [!DNL Google Ads]  ワークフローについて説明します。
feature: Search Campaign Management, Conversions
exl-id: b708c9f2-2962-45d9-8780-4e96ef2ae8f7
TQID: https://experienceleague.adobe.com/yFJJ662wcsm2KLzCIpxXo6F8nPsklVItHMTBk1h6wHg
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 388
ht-degree: 0%

---

# リードの[!DNL Google Ads]強化コンバージョンを実装します

*[!DNL Google Ads]アカウントのみ*

[[!DNL Google Ads]  リード向け拡張コンバージョン ](https://support.google.com/google-ads/answer/9888656)を使用すると、ファーストパーティのコンバージョンデータを使用して、ユーザーをオフラインコンバージョンにマッピングできます。 クリック IDが使用できない環境（web サイトのリードに起因する電話やメール販売のトラッキングなど）では、リードに対して拡張コンバージョンを使用します。

Search, Social, &amp; Commerceでは、次のことができます。

* リードの既存の拡張コンバージョンを表示します。

  Search, Social, &amp; Commerceは、広告主のタイムゾーンの05:00に毎日、リード用に既存の拡張コンバージョンを同期します。

* リードのコンバージョンを向上。

* 1st パーティのオフラインのコンバージョンデータをアップロードして、リードのコンバージョンを強化するマップを作成します。

* 強化したコンバージョンは、レポート内の指標として、また最適化のための目標内の重み付け指標として含めることができます。

この機能を使用するには、次の手順を実行します。 コンバージョン追跡タグを作成し、コンバージョンアクションを作成する手順は、オプションで元に戻すことができます。

1. [!DNL Google Ads]内で、リードの拡張コンバージョンをオプトインします。

   1. アカウントのコンバージョン設定を開きます。

   1. リードの拡張コンバージョンのオプションを選択し、利用規約に同意します。

   1. コンバージョンタグの作成に[!DNL Google] タグを使用するか、[!DNL Google Tag Manager]を使用するかを選択します。

1. コンバージョンアクションを追跡するためのタグを設定して実装します。

   手順については、[!DNL Google Ads] ヘルプを参照して、a[ タグ  [!DNL Google] を使用するリード ](https://support.google.com/google-ads/answer/11021502)または[を使用するリード  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292)の強化コンバージョン用のタグを作成します。

1. [Search, Social, &amp; Google](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)または[Commerce Ads](https://support.google.com/google-ads/answer/12216226)内のリードに対して、強化されたコンバージョンのコンバージョンアクションを作成します。

   Search, Social, &amp; Commerce内でコンバージョンアクションを作成する場合は、**コンバージョンの種類**&#x200B;を&#x200B;*コンバージョンのインポート*&#x200B;または&#x200B;*インポート*&#x200B;として指定します。

1. 必要に応じて、ハッシュ化されたメールアドレスや電話番号などのファーストパーティデータをアップロードし、指定したアカウントのコンバージョンに関連付けます。 この手順は、[検索、ソーシャル、Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)内または[!DNL Google Data Manager]を使用して実行できます。

   * Search, Social, &amp; Commerce内で、[!DNL Microsoft Excel]形式のテンプレートをダウンロードし、コンバージョンデータを入力してファイルをローカルに保存し、編集したファイルをアップロードできます。 このテンプレートには、広告目的および広告パーソナライゼーション目的で[!DNL Google]にデータをアップロードするためにユーザーの同意が与えられたかどうかを示す列が含まれています。

     アップロードされたすべてのデータは、リアルタイムで[!DNL Google Ads]に同期されます。

   * [!DNL Google Data Manager]を使用したデータのアップロードについて詳しくは、「[Data Manager](https://support.google.com/google-ads/answer/14639041)について」を参照してください。

>[!MORELIKETHIS]
>
>* [ リードの強化されたコンバージョン  [!DNL Google Ads] のコンバージョンアクションを作成](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
