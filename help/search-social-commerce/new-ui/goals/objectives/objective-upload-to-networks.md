---
title: （新しいUI）広告ネットワークへの目的のアップロードを有効にする
description: ハイブリッドポートフォリオの目標をGoogle AdsとMicrosoft Advertisingにアップロードする方法について説明します。
feature: Search Objectives, Search Optimization
hide: true
source-git-commit: b9388f691c8e804cece8d9f1eeb1bdc4f352dd11
workflow-type: tm+mt
source-wordcount: '722'
ht-degree: 0%

---

# （新しいUI）広告ネットワークへの目的のアップロードを有効にする

*Beta機能*

[!DNL Google Ads] アカウントと[!DNL Microsoft Advertising] アカウントのみを持つ&#x200B;*広告主*

*ハイブリッド最適化のみ有効な広告主*

Search, Social, &amp; Commerceでは、広告主アカウントのポートフォリオの目標を[!DNL Google Ads]および[!DNL Microsoft Advertising]にアップロードできるため、ハイブリッド最適化に使用できます。 アップロードされた目標は、アカウントレベルおよびキャンペーンレベルのカスタムコンバージョン目標のコンバージョンアクションとして使用できます。

このオプションを有効にすると、スマート入札戦略を含むキャンペーンを含むポートフォリオ内の目標のアップロードが自動的にトリガーされます。 Search, Social, &amp; Commerceは、該当する各目的に対して、広告ネットワーク上でコンバージョンを生み出します。 コンバージョンは、EF ID （クリック ID）レベルで、目的のすべての重み付けされたコンバージョン指標を表します。 [!DNL Google Ads] クリックの場合、EF IDは[!DNL Google Ads] `gclid`です。[!DNL Microsoft Advertising] クリックの場合、EF IDは[!DNL Microsoft Advertising] `msclkid`です。 このクリック IDにより、コンバージョンデータを特定のキーワードとクリック時間にマッピングできます。

アップロードされた各コンバージョンの名前は次のとおりです。

`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`

`<network_ID>`はSearch, Social, &amp; Commerceがアドネットワークに使用する数値ID、`<objective_ID>`は数値目標ID、`<network_account_ID>`はアドネットワークアカウントまたはマネージャーアカウントの数値IDです。

[!DNL Google Ads]および[!DNL Microsoft Advertising]へのアップロードは、通常、1日に1時間ごとに実行されます。 大規模なアカウントやカスタム設定を持つ広告主の場合、1日に少なくとも3回はアップロードが発生します。

>[!IMPORTANT]
>
>[!DNL Google Ads]および[!DNL Microsoft Advertising] ユニバーサル イベント トラッキング （UET） タグによってトラッキングされたコンバージョンは、広告ネットワークに再アップロードされません。 目標に含める場合は、広告ネットワークのエディター内のキャンペーン目標にそれらを追加する必要があります。

1. メインメニューで、**[!UICONTROL Goals]** > **[!UICONTROL Objectives]**&#x200B;をクリックします。

1. ツールバーで、**[!UICONTROL Upload Objective]**&#x200B;をクリックします。

1. [!UICONTROL Objective Upload Setup] ダイアログで、**[!UICONTROL Enable Objective Upload]** トグルを&#x200B;**[!UICONTROL On]**&#x200B;に設定します。

1. （欧州経済地域（EEA）または英国（UK）でビジネスを行う[!DNL Google Ads]人のアカウントを持つ広告主。オプション）広告目的でデータをアップロードするためにEEAおよび英国のユーザーから同意を得た場合は、チェックボックスを選択して、EEA/英国のユーザーの同意が収集されたことを確認します。 これにより、同意ステータスが&#x200B;**[!UICONTROL GRANTED]**&#x200B;として[!DNL Google Ads]および[!DNL Microsoft Advertising]に送信されます。 チェックを外した場合、同意ステータスは&#x200B;**[!UICONTROL UNSPECIFIED]**&#x200B;として送信されます。

1. （コンバージョンがマネージャーのアカウントレベルで追跡されている場合） [保存する前にマネージャーのアカウントの資格情報](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)を追加します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. `O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`という名前の各目的が2日以内に広告ネットワークに表示されることを確認します。

   [!DNL Google Ads] エディターで、[&#x200B; コンバージョンアクション &#x200B;](https://support.google.com/google-ads/answer/11461796){target="_blank"}を検索します。 [!DNL Microsoft Advertising] エディターで、[&#x200B; コンバージョン目標](https://help.ads.microsoft.com/#apex/ads/en/56709){target="_blank"}を検索します。

   必要に応じて、アップロード日を含めるように日付範囲を更新します。

## 重み付けされた目標の計算方法

広告ネットワークに渡される重み付けされた目標は、[!DNL Google Ads]または[!DNL Microsoft Advertising] ユニバーサルイベントトラッキング（UET）タグによって追跡されたコンバージョンを除いて、収集されたすべての指標値の合計です。 この値は、広告主のSearch, Social, &amp; Commerce アカウントに設定されたアトリビューション方式を使用して計算されます。

たとえば、目的の目標指標が25の重みの付いたカート追加数であり、アシスト指標には重みが1のGGL_LeadとRevenue、重みが0.5のDownloadsが含まれているとします。

![重み付けされた目標の例](/help/search-social-commerce/assets/objective-example.png "重み付けされた目標の例")

キーワードがポートフォリオに対して次のアクションを生み出したとします。

* 買い物かごに10個追加
* 500 ドルの収益
* 50 ダウンロード
* 5 GGL_Lead

GGL_LeadはGoogle Adsで追跡される指標であるため、計算/アップロードには含まれません。 したがって、重み付けされた目標値は（（10 x 25） + （500 x 1） + （50 x 0.5）） = 775として計算されます。

>[!TIP]
>
>広告ネットワークのレポート内で、Adobe Advertisingの加重売上に関するデータを表示できます。 ベストプラクティスとして、重み付けされた収益を[!DNL Google Ads] 「すべての変換」と比較します。 （convによる。 time）&quot;指標または[!DNL Microsoft Advertising] メトリック &quot;All conv. 「収益」は、O_ACS_OBJ*指標にセグメント化されています。

## 目標がない場合のトラブルシューティング

いずれかのポートフォリオの目標（`O_ACS_OBJ_<network_ID>_<objective_ID>_<network_account_ID>`）が広告ネットワークに表示されない場合は、次の点を確認してください。

* （[!DNL Google Ads]） コンバージョンをアカウントレベルまたはマネージャーレベルにアップロードする必要があるかどうかを確認します。 マネージャーレベルでアップロードする必要がある場合：

   * [!DNL Google Ads] マネージャーアカウントの資格情報が提供されているかどうかを確認します。 必要に応じて、マネージャーアカウントの資格情報を[追加します](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)。

   * 広告ネットワークアカウントに同じメトリック名が既に含まれているかどうかを確認します。 有効な場合は、指標の名前を変更して、適切なマネージャーレベルのプロパティを作成できるようにします。

* ポートフォリオの「ハイブリッド」オプションが選択されており、目的に有効な収益があることを確認します。

>[!MORELIKETHIS]
>
>* [目標について](objective-about.md)
>* [広告主のコンバージョン指標を管理](/help/search-social-commerce/new-ui/goals/conversions/conversion-metrics-manage.md)
>* [&#x200B; マネージャーアカウント &#x200B;](/help/search-social-commerce/new-ui/set-up/accounts/api-accounts/manager-account-manage.md)の資格情報の管理 [!DNL Google Ads] 

<!--
I don't see this yet in new UI:
>* [Upload Search, Social, & Commerce-tracked conversion metrics to [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
-->
