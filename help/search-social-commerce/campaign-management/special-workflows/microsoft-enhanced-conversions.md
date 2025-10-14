---
title: オフライ  [!DNL Microsoft Advertising]  コンバージョン用の拡張コンバージョンの実装
description: オフラインコンバージョン用の拡張コンバージョンを設定  [!DNL Microsoft Advertising]  る際のワークフローについて説明します。
feature: Search Campaign Management, Conversions
source-git-commit: 8f87e5bdab25aa527e72d7e9c75411267fe63780
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 0%

---

# オフラインコンバージョン用の [!DNL Microsoft Advertising] enhanced コンバージョンの実装

*[!DNL Microsoft Advertising]アカウントのみ*

[[!DNL Microsoft Advertising]  拡張コンバージョン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60178) ファーストパーティのコンバージョンデータを使用して、ユーザーをオフラインコンバージョンにマッピングできます。 Web サイトのリードから生じた電話やメールによる売上高を追跡するなど、クリック ID を使用できない環境では、拡張コンバージョンを使用します。

検索、ソーシャル、Commerce内では、次のことができます。

* オフラインコンバージョン向けに既存の拡張コンバージョンを表示します。

  検索、ソーシャル、Commerceでは、広告主のタイムゾーンの 05:00 に、既存の強化されたコンバージョンを毎日同期します。

* ファーストパーティのオフラインコンバージョンデータをアップロードして、既存の強化されたコンバージョン目標にマッピングします。

* 強化されたコンバージョンを、レポート内の指標として、および最適化の目標内の重み付け指標として含めます。

この機能を使用するには、次の手順を実行します。

1. 「[Enhanced Conversions](https://help.ads.microsoft.com/#apex/ads/en/60178)」の [!DNL Microsoft Advertising] ヘルプで示されているすべての前提条件に従ってください。

1. [&#x200B; 内で拡張コンバージョン目標を設定します  [!DNL Microsoft Advertising]](https://help.ads.microsoft.com/#apex/ads/en/60178)。

1. 必要に応じて、ハッシュ化されたメールアドレスや電話番号などのファーストパーティデータを、指定したアカウントのコンバージョンに関連付けるためにアップロードします。 この手順は、[&#x200B; 検索、ソーシャル、Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) 内または [!DNL Microsoft Advertising] 内から実行できます。

   * 検索、ソーシャル、Commerce内で、[!DNL Microsoft Excel] 形式のテンプレートをダウンロードし、コンバージョンデータを入力して、ファイルをローカルに保存し、編集したファイルをアップロードできます。

     アップロードされたすべてのデータは、リアルタイムで [!DNL Microsoft Advertising] に同期されます。

   * [!DNL Microsoft Advertising] 内でのデータのアップロードについて詳しくは、「拡張コンバージョン [&#128279;](https://help.ads.microsoft.com/#apex/ads/en/60178)」に関する [!DNL Microsoft Advertising] ヘルプの「オフラインコンバージョン用の拡張コンバージョンの設定  を参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; オフラインのコンバージョンデータをアップロードしてコンバージョンを強化 &#x200B;](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
