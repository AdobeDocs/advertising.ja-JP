---
title: ' [!DNL Google Ads]のコンバージョンタグを作成'
description: ' [!DNL Google Ads]  コンバージョンタグの作成方法について説明します。'
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
TQID: https://experienceleague.adobe.com/pskBpQ12sQXj9RyLd3IQAG0MktlOvV2JvZBl5rGtQT0
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: b2ff290c2cee19c8acdc8001433189ea9bdbf83f
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# [!DNL Google Ads]のコンバージョンタグを作成

マネージャーのアカウントレベルで追跡するのではなく、個々の[!DNL Google Ads] アカウントで追跡する新しいコンバージョンのコンバージョンタグを作成できます。

既存のコンバージョンのコンバージョンタグを生成するには、広告ネットワークのエディターを使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックすると、**[!UICONTROL Summary]** タブが開きます。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. [&#x200B; コンバージョンタグ設定](#conversion-tag-settings-google)を指定します。

   1. アカウントを選択し、コンバージョンタイプを選択します。

   1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. 変換オプションを指定します。

   1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. コンバージョンタグをコピーし、コンバージョン指標を追跡するweb サイトに実装します。

   「[!DNL Google]2」の[!DNL Google Ads] ヘルプの「[&#x200B; タグのインストール」を参照してください。 Google タグ &#x200B;](https://support.google.com/google-ads/answer/12215519)を設定します。」

1. **[!UICONTROL Done].**&#x200B;をクリックします

タグをweb サイトに追加して実行を開始すると、[!DNL Google Ads]はweb サイトにコンバージョンを記録します。 Search, Social, &amp; Commerceは、コンバージョンを毎日同期します。 同期されるデータについて詳しくは、「[[!DNL Google Ads] Search, Social, &amp; Commerceのコンバージョンデータ &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)」を参照してください。

## コンバージョンタグ設定 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:**&#x200B;該当する[!DNL Google Ads] アカウント。

**[!UICONTROL Type of Conversion]:**&#x200B;追跡するコンバージョンの種類：*[!UICONTROL Click on a webpage element]*、*[!UICONTROL Calls to a phone number on your website]*、または&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*。 **注：** *[!UICONTROL Import conversion]*&#x200B;は別の目的に使用されています。「[&#x200B; リードのコンバージョンを強化 [!DNL Google Ads] するためのコンバージョンアクションの作成](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)」を参照してください。

**[!UICONTROL Conversion Name]:** コンバージョン指標の一意の名前。

**\[ コンバージョンカテゴリ\]:** コンバージョンカテゴリ。 利用できるカテゴリは、コンバージョンの種類によって異なります。 *[!UICONTROL Calls to a phone number on your website]*&#x200B;および&#x200B;*[!UICONTROL Clicks to your number on your mobile website]*&#x200B;では、「[!UICONTROL Phone Call Lead]」がデフォルトで選択されています。

**\[Action Type\]:**&#x200B;目標が&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;か&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*&#x200B;かです。

**[!UICONTROL Value]:**&#x200B;各コンバージョンの[値を測定する方法](https://support.google.com/google-ads/answer/3419241):

* 通貨を選択し、各変換の値を入力する必要がある&#x200B;*[!UICONTROL Use the same value for each conversion],*。

* 通貨を選択し、各変換の既定値を入力する必要がある&#x200B;*[!UICONTROL Use a different value for each conversion],*。 特定のweb ページにタグを実装する場合、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [&#x200B; クリックまたはインタラクションごとにカウントするコンバージョン数](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;または&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]:** コンバージョンを記録する広告インタラクションの後最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL View Through Conversion Window]:** ビュースルーコンバージョンが記録される、ユーザーが広告を表示してから経過した最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [各広告インタラクションに対するクレジット額](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*&#x200B;または&#x200B;*[!UICONTROL Last click]*。 **メモ：**&#x200B;以前はサポートされていなかった&#x200B;*[!UICONTROL First click]*、*[!UICONTROL Linear]*、*[!UICONTROL Time decay]*、または&#x200B;*[!UICONTROL Position based]* モデルを使用していたコンバージョンアクションで、*[!UICONTROL Data driven]* モデルが使用されるようになりました。

>[!MORELIKETHIS]
>
>* [&#x200B; オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* Search, Social, &amp; Commerceの[[!DNL Google Ads]  コンバージョンデータ &#x200B;](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
