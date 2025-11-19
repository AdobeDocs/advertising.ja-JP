---
title: 広告ネットワークへの目標のアップロードを有効にする
description: ' [!DNL Google Ads] and [!DNL Microsoft Advertising] にハイブリッドポートフォリオの目標をアップロードする方法を説明します。'
exl-id: 09ab0b7a-b6ea-45ad-a82c-2c40d518d2e7
feature: Search Tools
source-git-commit: 8b741fd9e5a2cb950bc7d8ba4f3307dab23e72fe
workflow-type: tm+mt
source-wordcount: '680'
ht-degree: 0%

---

# 広告ネットワークへの目標のアップロードを有効にする

*[!DNL Google Ads] と [!DNL Microsoft Advertising] のアカウントのみを持つ広告主*

*ハイブリッド最適化のみを有効にした広告主*

検索、ソーシャルおよびCommerceでは、広告主アカウントのポートフォリオの目標を [!DNL Google Ads] および [!DNL Microsoft Advertising] にアップロードして、ハイブリッド最適化に使用できます。 アップロードした目標は、アカウントレベルとキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート入札戦略を使用したキャンペーンを含んだポートフォリオ内の目標のアップロードが自動的にトリガー付けされます。 検索、ソーシャル、Commerceを行うと、該当する目的ごとに広告ネットワーク上にコンバージョンが作成されます。 コンバージョンは、目標内の EF ID （クリック ID）レベルの重み付けされたコンバージョン指標をすべて表します。 [!DNL Google Ads] クリックの場合、EF ID は [!DNL Google Ads] `gclid` です。[!DNL Microsoft Advertising] クリックの場合、EF ID は [!DNL Microsoft Advertising] `msclkid` です。 このクリック ID により、コンバージョンデータを特定のキーワードとクリック時間にマッピングできます。

アップロードされた各コンバージョンには、以下の名前が付けられます。

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

ここで、`<network_ID>` は、Search、Social、およびCommerceが広告ネットワークに使用する数値 ID、`<objective_id>` は数値の目的 ID、`<network_account_ID>` は広告ネットワークアカウントまたはマネージャーアカウントの数値 ID です。

[!DNL Google Ads] および [!DNL Microsoft Advertising] へのアップロードは、1 日を通じて（通常は 1 時間ごと）行われます。 大規模なアカウントまたはカスタム設定を持つ広告主の場合、アップロードは 1 日に少なくとも 3 回発生します。

>[!IMPORTANT]
>
>Google Ads およびMicrosoft Advertising ユニバーサルイベントトラッキング（UET）タグで追跡されたコンバージョンは、広告ネットワークに再アップロードされません。 目標内に含める場合は、広告ネットワークのエディター内のキャンペーンの目標に追加する必要があります。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Tools]/[!UICONTROL Conversion Upload Setup]** をクリックします。

1. 「**[!UICONTROL Enable Objective Upload]**」の横にあるチェックボックスをオンにします。

1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う [!DNL Google Ads] アカウントを持つ広告主。オプション） EEA および英国のユーザーから、広告目的でデータをアップロードすることに対する同意を収集した場合は、**[!UICONTROL If you are doing business in EEA and/or UK, check this box to send consent status as GRANTED for the user data sent to [!DNL Google Ads] for advertising purposes. If left unchecked, we will send consent status as UNSPECIFIED for the user data sent to [!DNL Google Ads] for advertising purposes.]** の横にあるチェックボックスを選択します

1. 「**[!UICONTROL Save]**」をクリックします。

1. （コンバージョンが管理者アカウントレベルで追跡されている場合） [ 管理者アカウントの資格情報を追加 ](/help/search-social-commerce/admin/manager-accounts.md)**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Admin]/[!UICONTROL Manager Accounts]** で行います。

1. `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` という名前の各目標が、2 日以内に広告ネットワークに表示されることを確認します。

   [!DNL Google Ads] エディターで、[ コンバージョンアクション ](https://support.google.com/google-ads/answer/11461796) を検索します。 [!DNL Microsoft Advertising] エディターで、[ コンバージョンの目標 ](https://help.ads.microsoft.com/#apex/ads/en/56709) を検索します。

   必要に応じて、アップロード日を含めるように日付範囲を更新します。

## 加重目標の計算方法

広告ネットワークに渡される重み付け目標は、[!DNL Google Ads] または [!DNL Microsoft Advertising] Universal Event Tracking （UET）タグによって追跡されたコンバージョンを除き、収集されたすべての指標値の合計です。 値は、広告主の検索、ソーシャル、Commerce アカウントに設定されたアトリビューションメソッドを使用して計算されます。

例えば、目標の目標指標が買い物かごへの追加（重み付け 25）で、アシスト指標には、GGL_Lead と売上高（重み付け 1）およびダウンロード（重み付け 0.5）が含まれているとします。

![ 加重目標の例 ](/help/search-social-commerce/assets/objective-example.png " 加重目標の例 ")

キーワードの結果、ポートフォリオの次のアクションが発生したとします。

* 買い物かごへの 10 件の追加
* 500 ドルの収益
* 50 ダウンロード
* 5 GGL_Lead

Google Ads で追跡される指標なので、GGL_Lead は計算/アップロードに含まれません。 したがって、加重目標値は（（10 x 25） + （500 x 1） + （50 x 0.5））=775 として算出されます。

>[!TIP]
>
>広告ネットワークのレポート内で、Adobe Advertisingの加重売上高のデータを表示できます。 ベストプラクティスとして、重み付けされた売上高を [!DNL Google Ads] の「すべての conv」と比較します。 （conv. 時間）」指標または [!DNL Microsoft Advertising] 指標「すべての変換」 売上高は、O_ACS_OBJ*指標にセグメント化されています。<!--clarify -->

## 目標が見つからない場合のトラブルシューティング

ポートフォリオの目的（`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>` という名前）が広告ネットワークに表示されない場合は、次の点を確認してください。

* （[!DNL Google Ads]） コンバージョンをアカウントレベルまたはマネージャーレベルにアップロードする必要があるかどうかを確認します。 マネージャーレベルでアップロードする場合：

   * [!DNL Google Ads] manager アカウントの資格情報が **[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]** で提供されているかどうかを確認します。 必要に応じて、[ マネージャーアカウントの資格情報を追加 ](/help/search-social-commerce/admin/manager-accounts.md) します。

   * 広告ネットワークアカウントに同じ指標名が既に含まれているかどうかを確認します。 含まれる場合は、適切なマネージャーレベルのプロパティを作成できるように、指標の名前を変更します。

* ポートフォリオの「ハイブリッド」オプションが選択され、目標に有効な売上高があることを確認します。

>[!MORELIKETHIS]
>
>* [ 広告主のコンバージョン指標の管理について ](/help/search-social-commerce/admin/conversion-metrics/conversion-metric-about.md)
>* [ 検索、ソーシャル、Commerceで追跡されるコンバージョン指標のへのアップロード  [!DNL Google Ads]](conversion-metrics-upload-to-google.md)
