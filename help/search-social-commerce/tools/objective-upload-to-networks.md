---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標をにアップロードする方法を説明します [!DNL Google Ads] および [!DNL Microsoft® Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 7b857f2f75f05685d0776c710a442088a72f590c
workflow-type: tm+mt
source-wordcount: '236'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*を使用した広告主 [!DNL Google Ads] および [!DNL Microsoft® Advertising] アカウントのみ*

*ハイブリッド最適化のみ有効な広告主*

広告主アカウントがハイブリッド最適化を使用するように設定されている場合、Adobe Advertisingはオプションとして、アカウントのポートフォリオの目標をにアップロードできます [!DNL Google Ads] および [!DNL Microsoft® Advertising] をコンバージョンとして使用することで、ハイブリッド最適化に使用できます。

このオプションを有効にすると、スマート入札戦略を使用したキャンペーンを含んだポートフォリオのアップロードが自動的にトリガー付けされます。 検索、ソーシャル、Commerceを行うと、該当するポートフォリオと目標の組み合わせごとに広告ネットワーク上でコンバージョンが作成されます。 各コンバージョンには名前があります `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`、ここで `<portfolio_id>` は数値ポートフォリオ ID で、 `<se_acctid/conversion_manager_se_acctid>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。 コンバージョンは、目標内のすべての重み付けされたコンバージョン指標を表します。

へのアップロード [!DNL Google Ads] 毎日 06:00 に広告主のタイムゾーンで発生します。 へのアップロード [!DNL Microsoft® Advertising] 広告主のタイムゾーンで毎日 09:00 に発生します。

<!-- Note to self: Conversions tracked by Google Ads and by the Microsoft Advertising universal event tracking (UET) tag aren't re-uploaded to the ad networks. -->

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横にあるチェックボックスをオンにします。 **[!UICONTROL Enable Objective Upload]**.

1. （広告主 [!DNL Google Ads] 欧州経済地域（EEA）または英国（UK）でビジネスを行うアカウント。任意） EEA および英国のユーザーから、広告目的でデータをアップロードすることに対する同意を収集した場合は、の横にあるチェックボックスを選択します **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者アカウントレベルで追跡されている場合） [マネージャーアカウントの資格情報の追加](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [へのコンバージョン指標のアップロード [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
