---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標を [!DNL Google Ads]  [!DNL Microsoft Advertising]にアップロードする方法について説明します。
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: d703b0d0134dbd16b2672b13d2ea63e4f102e105
workflow-type: tm+mt
source-wordcount: '677'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*[!DNL Google Ads] アカウントと [!DNL Microsoft Advertising] アカウントのみを持つ広告主*

*ハイブリッド最適化のみが有効になっている広告主*

Search、Social、コマースは、広告主 アカウントポートフォリオの目標をアップロードして [!DNL Google Ads] し、 [!DNL Microsoft Advertising] してハイブリッド最適化に使用できます。 アップロードした目標は、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート自動入札戦略を使用するキャンペーンを含むポートフォリオの目的に対してアップロードが自動的にトリガーされます。 Search、Social、およびコマースは、該当する各目的の広告ネットワークにコンバージョンを作成します。 コンバージョンは、目標内のすべての加重コンバージョン指標を EF ID(クリック ID)レベルで表します。 各コンバージョンには、次のいずれかの名前が付けられます。

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  ここで、 `<network_ID>` は、検索、ソーシャル、Commerceが広告ネットワークに使用する数値 ID です。 `<objective_id>` は数値目標 ID で、 `<network_account_ID>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

* （今後非推奨となる古い形式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  ここで、 `<portfolio_id>` は数値ポートフォリオ ID で、 `<se_acctid/conversion_manager_se_acctid>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

  Adobeアカウントチームは、古いフォーマットが廃止される前に、アドネットワーク内の既存のコンバージョンアクション名を移行するためにお客様と協力します。 移行期間中は、古い形式と新しい形式の両方のアップロードが並行して実行されます。 新しいコンバージョンアクションは最初に「セカンダリ」（最適化されていない）ステータスで、90 日間のバックフィルデータで表示されるので、モデリングと最適化は影響を受けません。

へのアップロード [!DNL Google Ads] 毎日 06:00 に広告主のタイムゾーンで発生します。 へのアップロード [!DNL Microsoft Advertising] 広告主のタイムゾーンで毎日 09:00 に発生します。

>[!IMPORTANT]
>
>Google Ads およびMicrosoft Advertising ユニバーサルイベントトラッキング（UET）タグで追跡されたコンバージョンは、広告ネットワークに再アップロードされません。 目標内に含める場合は、広告ネットワークのエディター内のキャンペーンの目標に追加します。

<!--
>[!IMPORTANT]
>
>Objectives for hybrid portfolios may include conversion goals from multiple ad networks and other types of conversion metrics. However, the individual campaigns in the portfolio can't include conversion goals that aren't included in the portfolio's objective; using additional conversion goals may impact portfolio performance.
-->

<!-- Can conversions from events triggered on other ad networks be included in the portfolio (and just be ignored)? -->

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横にあるチェックボックスをオンにします。 **[!UICONTROL Enable Objective Upload]**.

1. (欧州経済領域(EEA)または英国(UK)でビジネスを行う [!DNL Google Ads] アカウントを持つ広告主様、省略可) EEAおよび英国のユーザーから、広告目的でデータアップロードことに同意した場合は、[ **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. [ **[!UICONTROL Save]**] をクリックします。

1. (コンバージョンがマネージャー アカウント レベルでトラッキングされている場合) [マネージャーの資格情報追加 アカウント](/help/search-social-commerce/admin/manager-accounts.md) **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**。

1. `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` という名前の各目標が 2 日以内に広告ネットワークに表示されることを確認します。

   [!DNL Google Ads] 編集者で、[コンバージョンアクションを調べます](https://support.google.com/google-ads/answer/11461796)。が含まれる [!DNL Microsoft Advertising] エディター、検索する [コンバージョン目標](https://help.ads.microsoft.com/#apex/ads/en/56709).

   必要に応じて、アップロード日付が含まれるように日付範囲を更新します。

## 重み付けされた目標の計算方法

広告ネットワークに渡される加重目標は、 [!DNL Google Ads] または [!DNL Microsoft Advertising] ユニバーサルイベント トラッキング(UET)タグによってトラッキングされたコンバージョンを除き、収集されたすべての指標値の合計です。

たとえば、目標の目標指標が重み付け 25 の「買い物かごへの追加」で、アシスト指標に重みが 1 の「GGL_Lead」と「売上高」、重み付けが 0.5 の「ダウンロード」が含まれているとします。

![重み付けされた目標の例](/help/search-social-commerce/assets/objective-example.png "重み付けされた目標の例")

あるキーワードによって、そのポートフォリオに対して次のアクションがおこなわれたとします。

* 買い物かごへの 10 件の追加
* 500 ドルの収益
* 50 ダウンロード
* 5 GGL_Lead

Google Ads で追跡される指標なので、GGL_Lead は計算/アップロードに含まれません。 したがって、加重目標値は（（10 x 25） + （500 x 1） + （50 x 0.5））=775 として算出されます。

## 目標が見つからない場合のトラブルシューティング

目的の場合 – という名前 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`  – いずれかのポートフォリオが広告ネットワークに表示されない場合は、次の点を確認してください。

* （[!DNL Google Ads]）コンバージョンをアカウントレベルまたはマネージャーレベルにアップロードする必要があるかどうかを確認します。 マネージャーレベルでアップロードする場合：

   * の資格情報を確認する [!DNL Google Ads] manager account provided at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. 必要に応じて、 [マネージャーアカウントの資格情報を追加](/help/search-social-commerce/admin/manager-accounts.md).

   * 広告ネットワーク アカウントに既に同じ指標名が含まれているかどうかを確認します。 その場合は、正しいマネージャレベルのプロパティを作成できるように指標名前を変更します。

* ポートフォリオの「ハイブリッド」オプションが選択されていることと、目標に有効な売上高があることを確認します。

>[!MORELIKETHIS]
>
>* [広告主コンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [コンバージョン指標のアップロード先 [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
