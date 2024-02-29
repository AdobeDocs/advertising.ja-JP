---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標を次にアップロードする方法を説明します。 [!DNL Google Ads] および [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 0fb03410e67be28d24496c948b52399c8465e041
workflow-type: tm+mt
source-wordcount: '260'
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

1. ( [!DNL Google Ads] 欧州経済圏 (EEA) または英国 (UK) でビジネスを行うアカウント（オプション）EEA および UK ユーザーから広告用にデータをアップロードする同意を得ている場合は、の横のチェックボックスをオンにします。 **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者のアカウントレベルで追跡される場合） [管理者アカウントの資格情報を追加します](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [コンバージョン指標のアップロード先 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
