---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ハイブリッドポートフォリオの目標をにアップロードする方法を説明します [!DNL Google Ads] および [!DNL Microsoft Advertising].
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 39936c6834012432447d3216d8463937996b0017
workflow-type: tm+mt
source-wordcount: '711'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*を使用した広告主 [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントのみ*

*ハイブリッド最適化のみ有効な広告主*

検索、ソーシャルおよびCommerceでは、広告主アカウントのポートフォリオの目標をにアップロードできます [!DNL Google Ads] および [!DNL Microsoft Advertising] そのため、ハイブリッド最適化に使用できます。 アップロードした目標は、アカウントレベルとキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート入札戦略を使用したキャンペーンを含んだポートフォリオ内の目標のアップロードが自動的にトリガー付けされます。 検索、ソーシャル、Commerceを行うと、該当する目的ごとに広告ネットワーク上にコンバージョンが作成されます。 コンバージョンは、目標内の EF ID （クリック ID）レベルの重み付けされたコンバージョン指標をすべて表します。 の場合 [!DNL Google Ads] クリックすると、EF ID はになります [!DNL Google Ads] `gclid`; [!DNL Microsoft Advertising] クリックすると、EF ID はになります [!DNL Microsoft Advertising] `msclkid`. このクリック ID により、コンバージョンデータを特定のキーワードとクリック時間にマッピングできます。

アップロードされた各コンバージョンには、以下のいずれかの名前が付けられます。

* `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

  ここで、 `<network_ID>` は、検索、ソーシャル、Commerceが広告ネットワークに使用する数値 ID です。 `<objective_id>` は数値目標 ID で、 `<network_account_ID>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

* （今後非推奨となる古い形式） `ACS_OBJ_SID_<portfolio_id>_<se_acctid/conversion_manager_se_acctid>`

  ここで、 `<portfolio_id>` は数値ポートフォリオ ID で、 `<se_acctid/conversion_manager_se_acctid>` は、広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

  Adobeアカウントチームは、古いフォーマットが廃止される前に、アドネットワーク内の既存のコンバージョンアクション名を移行するためにお客様と協力します。 移行期間中は、古い形式と新しい形式の両方のアップロードが並行して実行されます。 新しいコンバージョンアクションは最初に「セカンダリ」（最適化されていない）ステータスで、90 日間のバックフィルデータで表示されるので、モデリングと最適化は影響を受けません。

へのアップロード [!DNL Google Ads] 毎日 06:00 に広告主のタイムゾーンで発生します。 へのアップロード [!DNL Microsoft Advertising] 広告主のタイムゾーンで毎日 09:00 に発生します。

>[!IMPORTANT]
>
>Google Ads およびMicrosoft Advertising ユニバーサルイベントトラッキング（UET）タグで追跡されたコンバージョンは、広告ネットワークに再アップロードされません。 目標内に含める場合は、広告ネットワークのエディター内のキャンペーンの目標に追加する必要があります。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横にあるチェックボックスをオンにします。 **[!UICONTROL Enable Objective Upload]**.

1. （広告主 [!DNL Google Ads] 欧州経済地域（EEA）または英国（UK）でビジネスを行うアカウント。任意） EEA および英国のユーザーから、広告目的でデータをアップロードすることに対する同意を収集した場合は、の横にあるチェックボックスを選択します **[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]**

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者アカウントレベルで追跡されている場合） [マネージャーアカウントの資格情報の追加](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

1. 各目的が、次の名前であることを確認します。 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` — 2 日以内に広告ネットワークに表示されます。

   が含まれる [!DNL Google Ads] エディター、検索する [コンバージョンアクション](https://support.google.com/google-ads/answer/11461796). が含まれる [!DNL Microsoft Advertising] エディター、検索する [コンバージョン目標](https://help.ads.microsoft.com/#apex/ads/en/56709).

   必要に応じて、アップロード日を含めるように日付範囲を更新します。

## 加重目標の計算方法

広告ネットワークに渡される重み付け目標は、で追跡されたコンバージョンを除く、収集されたすべての指標値の合計です [!DNL Google Ads] または [!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET）タグ。

例えば、目標の目標指標が買い物かごへの追加（重み付け 25）で、アシスト指標には、GGL_Lead と売上高（重み付け 1）およびダウンロード（重み付け 0.5）が含まれているとします。

![加重目標の例](/help/search-social-commerce/assets/objective-example.png "加重目標の例")

キーワードの結果、ポートフォリオの次のアクションが発生したとします。

* 買い物かごへの 10 件の追加
* 500 ドルの収益
* 50 ダウンロード
* 5 GGL_Lead

Google Ads で追跡される指標なので、GGL_Lead は計算/アップロードに含まれません。 したがって、加重目標値は（（10 x 25） + （500 x 1） + （50 x 0.5））=775 として算出されます。

## 目標が見つからない場合のトラブルシューティング

目的の場合 – という名前 `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`  – いずれかのポートフォリオが広告ネットワークに表示されない場合は、次の点を確認してください。

* （[!DNL Google Ads]）コンバージョンをアカウントレベルまたはマネージャーレベルにアップロードする必要があるかどうかを確認します。 マネージャーレベルでアップロードする場合：

   * の資格情報を確認する [!DNL Google Ads] manager account provided at **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**. 必要に応じて、 [マネージャーアカウントの資格情報を追加](/help/search-social-commerce/admin/manager-accounts.md).

   * 広告ネットワークアカウントに同じ指標名が既に含まれているかどうかを確認します。 含まれる場合は、適切なマネージャーレベルのプロパティを作成できるように、指標の名前を変更します。

* ポートフォリオの「ハイブリッド」オプションが選択され、目標に有効な売上高があることを確認します。

>[!MORELIKETHIS]
>
>* [広告主のコンバージョン指標の管理について](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [へのコンバージョン指標のアップロード [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
