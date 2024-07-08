---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標を [!DNL Google Ads]  [!DNL Microsoft Advertising]にアップロードする方法について説明します。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 803f1ad2ad5be005b7dab467efbeb1c4ceaa7559
workflow-type: tm+mt
source-wordcount: '536'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*[!DNL Google Ads] アカウントと [!DNL Microsoft Advertising] アカウントのみを持つ広告主*

*ハイブリッド最適化のみが有効になっている広告主*

Search、Social、コマースは、広告主 アカウントポートフォリオの目標をアップロードして [!DNL Google Ads] し、 [!DNL Microsoft Advertising] してハイブリッド最適化に使用できます。 アップロードした目標は、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート自動入札戦略を使用するキャンペーンを含むポートフォリオの目的に対してアップロードが自動的にトリガーされます。 Search、Social、およびコマースは、該当する各目的の広告ネットワークにコンバージョンを作成します。 コンバージョンは、目標内のすべての重み付けされたコンバージョン指標を表します。 各コンバージョンには、次のいずれかの名前が付けられます。

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  ここで、 `<network_ID>` はSearch、Social、コマースが広告ネットワークに使用する数値 ID、 `<objective_id>` は数値の目的IDであり、 `<network_account_ID>` は広告ネットワーク アカウントまたはマネージャーアカウントの数値IDです。

* (将来廃止される古い形式) `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  ここで、 `<portfolio_id>` は数値 ポートフォリオ ID、 `<se_acctid/conversion_manager_se_acctid>` は広告ネットワーク アカウントまたはマネージャ アカウントの数値 ID です。

  古い形式が廃止される前に、Adobe Systemsアカウントチームがお客様と協力して、広告ネットワーク内の既存のコンバージョンアクション名を移行します。 移行期間中は、古い形式と新しいの両方のアップロードが並行して実行されます。 モデリングと最適化は、新しいコンバージョンアクションが最初は「セカンダリ」(最適化されていない)ステータスで表示され、90日間のバックフィルデータとともに表示されるため、影響を受けません。

[!DNL Google Ads]へのアップロードは、広告主タイムゾーンの毎日 6:00 に行われます。[!DNL Microsoft Advertising]へのアップロードは、広告主タイムゾーンの毎日09:00に行われます。

>[!IMPORTANT]
>
>Google 広告と Microsoft Advertising ユニバーサル イベント トラッキング (UET) タグによって追跡されたコンバージョンは、広告 ネットワークに再アップロードされません。 目標に含める場合は、広告ネットワーク編集者内のキャンペーン目標に追加します。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. メインメニューで、「 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**」をクリックします。

1. 「 **[!UICONTROL Enable Objective Upload]**」の横にあるチェックボックスを選択します。

1. (欧州経済領域(EEA)または英国(UK)でビジネスを行う [!DNL Google Ads] アカウントを持つ広告主様、省略可) EEAおよび英国のユーザーから、広告目的でデータアップロードことに同意した場合は、[ **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. [ **[!UICONTROL Save]**] をクリックします。

1. (コンバージョンがマネージャー アカウント レベルでトラッキングされている場合) [マネージャーの資格情報追加 アカウント](/help/search-social-commerce/admin/manager-accounts.md) **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` という名前の各目標が 2 日以内に広告ネットワークに表示されることを確認します。

   [!DNL Google Ads] 編集者で、[コンバージョンアクションを調べます](https://support.google.com/google-ads/answer/11461796)。[!DNL Microsoft Advertising] 編集者で、[コンバージョン目標を調べます](https://help.ads.microsoft.com/#apex/ads/en/56709)。

   必要に応じて、アップロード日付が含まれるように日付範囲を更新します。

## 目標が見つからない場合のトラブルシューティング

ポートフォリオの 1 つの目的 ( `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` という名前) が広告ネットワークに表示されない場合は、次の点を確認してください。

* ([!DNL Google Ads]) コンバージョンをアカウント レベルまたはマネージャー レベルにアップロードする必要があるかどうかをチェックします。 マネージャーレベルでアップロードする必要がある場合:

   * [!DNL Google Ads] マネージャー アカウント の資格情報が **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** で指定されているかどうかを確認します。必要に応じて、マネージャー アカウント](/help/search-social-commerce/admin/manager-accounts.md)の資格情報[追加します。

   * 広告ネットワーク アカウントに既に同じ指標名が含まれているかどうかを確認します。 その場合は、正しいマネージャレベルのプロパティを作成できるように指標名前を変更します。

* ポートフォリオの「ハイブリッド」オプションが選択されていることと、目標に有効な売上高があることを確認します。

>[!MORELIKETHIS]
>
>* [広告主コンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [コンバージョン指標のアップロード先 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
