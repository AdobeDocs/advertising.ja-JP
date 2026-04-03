---
title: オフライン コンバージョン用に [!DNL Microsoft Advertising] 拡張コンバージョンを実装します
description: オフライン コンバージョン用に [!DNL Microsoft Advertising] 拡張コンバージョンを設定するワークフローについて説明します。
feature: Search Campaign Management, Conversions
exl-id: 44937db7-9e80-4a5d-85c7-5bd5febc3b96
TQID: https://experienceleague.adobe.com/GLFczqDqV8HE5hUZt8ORAlQMNy4OqQTtMdaHoYoN10U
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 0%

---

# オフライン コンバージョン用に[!DNL Microsoft Advertising]の拡張コンバージョンを実装します

*[!DNL Microsoft Advertising]アカウントのみ*

[[!DNL Microsoft Advertising] 拡張コンバージョン ](https://help.ads.microsoft.com/#apex/ads/en/60178)を使用すると、1st パーティのコンバージョンデータを使用して、ユーザーをオフラインコンバージョンにマッピングできます。 クリック IDが使用できない環境で拡張コンバージョンを使用して、web サイトのリードに起因する電話やメール販売を追跡します。

Search, Social, &amp; Commerceでは、次のことができます。

* 既存の拡張コンバージョンを表示して、オフラインコンバージョンを実現。

  Search, Social, &amp; Commerceは、広告主のタイムゾーンの05:00に、既存の強化コンバージョンを毎日同期します。

* 1st パーティのオフラインのコンバージョンデータをアップロードして、既存の強化されたコンバージョン目標にマッピングできます。

* 強化したコンバージョンをレポート内の指標として、また最適化のための目標の中に重み付け指標として含めます。

この機能を使用するには、次の手順を実行します。

1. 「[!DNL Microsoft Advertising]拡張コンバージョン [」に関する](https://help.ads.microsoft.com/#apex/ads/en/60178) ヘルプのすべての前提条件に従ってください。

1. [ [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178)内で強化コンバージョン目標を設定します。

1. 必要に応じて、ハッシュ化されたメールアドレスや電話番号などのファーストパーティデータをアップロードし、指定したアカウントのコンバージョンに関連付けます。 この手順は、[検索、ソーシャル、Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)または[!DNL Microsoft Advertising]内から実行できます。

   * Search, Social, &amp; Commerce内で、[!DNL Microsoft Excel]形式のテンプレートをダウンロードし、コンバージョンデータを入力してファイルをローカルに保存し、編集したファイルをアップロードできます。

     アップロードされたすべてのデータは、リアルタイムで[!DNL Microsoft Advertising]に同期されます。

   * [!DNL Microsoft Advertising]内のデータのアップロードについて詳しくは、「[!DNL Microsoft Advertising]拡張コンバージョン [」の](https://help.ads.microsoft.com/#apex/ads/en/60178) ヘルプの「オフラインコンバージョン用の拡張コンバージョンの設定」の節を参照してください。

>[!MORELIKETHIS]
>
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
