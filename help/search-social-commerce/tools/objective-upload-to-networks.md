---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標を次にアップロードする方法を説明します。 [!DNL Google Ads] および [!DNL Microsoft® Advertising].
exl-id: 75a1a804-ad6a-4dbc-9cde-30fe54476162
feature: Search Tools
source-git-commit: 5141c332fc00e9eae62ef507d215dd435e86e8ba
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*次を持つ広告主 [!DNL Google Ads] および [!DNL Microsoft® Advertising] アカウントのみ*

*広告主はハイブリッド最適化のみに対して有効です*

広告主アカウントがハイブリッド最適化を使用するように設定されている場合、Adobe Advertisingは、オプションでアカウントのポートフォリオの目標を次にアップロードできます。 [!DNL Google Ads] および [!DNL Microsoft® Advertising] コンバージョンとして機能し、ハイブリッド最適化に使用できます。

このオプションを有効にすると、スマート入札戦略を持つキャンペーンを含むポートフォリオ用に、自動的にトリガーおよびアップロードが行われます。 検索、ソーシャル、コマースは、広告ネットワーク上で、該当するポートフォリオと目標の組み合わせごとにコンバージョンを作成します。 各コンバージョンには `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`です。 `<portfolio_id>` は数値のポートフォリオ ID で、 `<se_acctid/conversion_manager_se_acctid>` は、広告ネットワークアカウントまたは広告マネージャーアカウントの数値 ID です。 コンバージョンは、目標のすべての重み付けされたコンバージョン指標を表します。

アップロード先 [!DNL Google Ads] は、広告主のタイムゾーンの毎日 06:00 に発生します。 アップロード先 [!DNL Microsoft® Advertising] は、広告主のタイムゾーンの毎日 09:00 に発生します。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横のチェックボックスをオンにします。 **[!UICONTROL Enable Objective Upload]**.

   このオプションは、広告主アカウントがハイブリッド最適化を使用するように設定されている場合にのみ使用できます。 ハイブリッド最適化を有効にするには、Adobeアカウントチームにお問い合わせください。

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者のアカウントレベルで追跡される場合） [管理者アカウントの資格情報を追加します](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [コンバージョン指標のアップロード先 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
