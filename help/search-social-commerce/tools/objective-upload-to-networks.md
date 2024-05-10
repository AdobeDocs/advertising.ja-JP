---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標をにアップロードする方法を説明します [!DNL Google Ads] および [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '405'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*を使用した広告主 [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ*

*ハイブリッド最適化のみ有効な広告主*

検索、ソーシャルおよびCommerceでは、広告主アカウントのポートフォリオの目標をにアップロードできます [!DNL Google Ads] および [!DNL Microsoft Advertising] そのため、ハイブリッド最適化に使用できます。 アップロードした目標は、アカウントレベルとキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート入札戦略を使用したキャンペーンを含んだポートフォリオ内の目標のアップロードが自動的にトリガー付けされます。 検索、ソーシャル、Commerceを行うと、該当する目的ごとに広告ネットワーク上にコンバージョンが作成されます。 コンバージョンは、目標内のすべての重み付けされたコンバージョン指標を表します。 各コンバージョンには、次のいずれかの名前が付けられます。

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  ここで、 `<network_ID>` は、検索、ソーシャル、Commerceが広告ネットワークに使用する数値 ID です。 `<objective_id>` は数値目標 ID で、 `<network_account_ID>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

* （今後非推奨となる古い形式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  ここで、 `<portfolio_id>` は数値ポートフォリオ ID で、 `<se_acctid/conversion_manager_se_acctid>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

  Adobeアカウントチームは、古いフォーマットが廃止される前に、アドネットワーク内の既存のコンバージョンアクション名を移行するためにお客様と協力します。 移行期間中は、古い形式と新しい形式の両方のアップロードが並行して実行されます。 新しいコンバージョンアクションは最初に「セカンダリ」（最適化されていない）ステータスで、90 日間のバックフィルデータで表示されるので、モデリングと最適化は影響を受けません。

へのアップロード [!DNL Google Ads] 毎日 06:00 に広告主のタイムゾーンで発生します。 へのアップロード [!DNL Microsoft Advertising] 広告主のタイムゾーンで毎日 09:00 に発生します。

>[!IMPORTANT]
>
>Google Ads およびMicrosoft Advertising Universal Event Tracking （UET）タグで追跡されたコンバージョンは、広告ネットワークには再アップロードされません。 目標内に含める場合は、広告ネットワークのエディター内のキャンペーンの目標に追加します。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横にあるチェックボックスをオンにします。 **[!UICONTROL Enable Objective Upload]**.

1. （広告主 [!DNL Google Ads] 欧州経済地域（EEA）または英国（UK）でビジネスを行うアカウント。任意） EEA および英国のユーザーから、広告目的でデータをアップロードすることに対する同意を収集した場合は、の横にあるチェックボックスを選択します **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者アカウントレベルで追跡されている場合） [マネージャーアカウントの資格情報の追加](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

毎日のアップロードが完了したら、変換アクションが広告ネットワークに表示されることを確認できます。

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [へのコンバージョン指標のアップロード [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
