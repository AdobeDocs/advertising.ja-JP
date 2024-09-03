---
title: リードのコ  [!DNL Google Ads]  バージョンの実装と強化
description: リードの拡張コンバージョンを設定するためのワークフロー  [!DNL Google Ads]  ついて説明します。
feature: Search Campaign Management, Conversions
source-git-commit: 60a67c8668df13afc08e14b0a495a37ded24bc0c
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 0%

---

# リードの [!DNL Google Ads] Enhanced コンバージョンの実装

*[!DNL Google Ads]アカウントのみ*

[[!DNL Google Ads]  リードのコンバージョンの強化 ](https://support.google.com/google-ads/answer/9888656) ファーストパーティコンバージョンデータを使用して、ユーザーをオフラインコンバージョンにマッピングできます。 Web サイトのリードから生じた電話やメールによる販売を追跡するなど、クリック ID を使用できない環境のリードに対して拡張コンバージョンを使用します。

検索、ソーシャルおよびCommerce内で、リードの拡張コンバージョンをレポート内の指標として、また最適化の目標内の重み付け指標として含めることができます。 検索、ソーシャル、Commerceでは、広告主のタイムゾーンの 05:00 に、リードの既存の強化されたコンバージョンを毎日同期します。

この機能を使用するには、次の手順を実行します。 コンバージョントラッキングタグを作成する手順とコンバージョンアクションを作成する手順は、オプションで元に戻すことができます。

1. [!DNL Google Ads] 内で、リードのコンバージョンを強化するオプトインを行います。

   1. アカウントのコンバージョン設定を開きます。

   1. リードのエンハンスドコンバージョンのオプションを選択し、利用規約に同意します。

   1. 変換タグの作成に [!DNL Google] タグを使用するか、[!DNL Google Tag Manager] を使用するかを選択します。


1. コンバージョンアクションの [!DNL Google] タグを設定して実装します。

   手順については、リードの拡張コンバージョン用のタグを作成するための [!DNL Google Ads] ヘルプ [using a [!DNL Google] tag](https://support.google.com/google-ads/answer/11021502) または [using [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11347292) を参照してください。

1. [ 検索、ソーシャル、Commerce](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) または [Google広告 ](https://support.google.com/google-ads/answer/12216226) 内で、リードの拡張コンバージョンのコンバージョンアクションを作成します。

   **コンバージョンのタイプ** で、*コンバージョンをインポート* または *インポート* を選択します。

1. 必要に応じて、ハッシュ化されたメールアドレスや電話番号などのファーストパーティデータを、指定したアカウントのコンバージョンに関連付けるためにアップロードします。 この手順は、[ 検索、ソーシャル、Commerce](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) 内または [!DNL Google Data Manager] を使用して実行できます。

   * 検索、ソーシャル、Commerce内で、[!DNL Microsoft Excel] 形式のテンプレートをダウンロードし、コンバージョンデータを入力して、ファイルをローカルに保存し、編集したファイルをアップロードできます。 テンプレートには、広告目的および広告パーソナライゼーション目的で [!DNL Google] へのデータのアップロードにユーザーの同意が得られたかどうかを示す列が含まれます。

     アップロードされたすべてのデータは、リアルタイムで [!DNL Google Ads] に同期されます。

   * [!DNL Google Data Manager] を使用したデータのアップロードの詳細は、「[Data Manager について ](https://support.google.com/google-ads/answer/14639041) を参照してください。

>[!MORELIKETHIS]
>
>* [ リードの拡張コンバージョン用  [!DNL Google Ads]  コンバージョンアクションの作成 ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化 ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
