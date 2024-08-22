---
title: ' [!DNL Google Ads] のコンバージョンタグを作成します。'
description: コンバージョンタグの作成方法  [!DNL Google Ads]  説明します。
feature: Conversions
exl-id: 214611f0-bd38-499e-a7de-3a5878995fb5
source-git-commit: 04330e26dbad6efe76dfcbe4662b062511ae14f6
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# [!DNL Google Ads] のコンバージョンタグを作成

新しいコンバージョンのコンバージョンタグを作成して、管理者アカウントレベルでは追跡せず、個々の [!DNL Google Ads] アカウントで追跡できるようにすることができます。

既存のコンバージョンのコンバージョンタグを生成するには、広告ネットワークのエディターを使用します。

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Conversions]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. [ 変換タグ設定 ](#conversion-tag-settings-google) を指定します。

   1. アカウントを選択してから、コンバージョンタイプを選択します。

   1. 「**[!UICONTROL Next]**」をクリックします。

   1. 変換オプションを指定します。

   1. 「**[!UICONTROL Generate]**」をクリックします。

1. コンバージョンタグをコピーし、コンバージョン指標を追跡する Web サイトに実装します。

   [!DNL Google Ads] ヘルプの「[!DNL Google] タグのインストール」を「[2」に参照してください。 Googleのタグを設定 ](https://support.google.com/google-ads/answer/12215519) ます。」というメッセージが表示されます。

1. 「**[!UICONTROL Done].**」をクリックします。

Web サイトにタグを追加し、そのタグが実行を開始すると、[!DNL Google Ads] は web サイト上でコンバージョンを記録します。 検索、ソーシャル、Commerceでは、コンバージョンが毎日同期されます。 同期されるデータについて詳しくは、「[[!DNL Google Ads]  検索、ソーシャル、Commerceのコンバージョンデータ ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md) を参照してください。

## 変換タグの設定 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** 該当するGoogle広告アカウント。

**[!UICONTROL Type of Conversion]:** 追跡するコンバージョンのタイプ。*[!UICONTROL Click on a webpage element]*、*[!UICONTROL Calls to a phone number on your website]* または *[!UICONTROL Clicks to your number on your mobile website]*。

**[!UICONTROL Conversion Name]:** コンバージョン指標の一意の名前。

**\[ コンバージョン カテゴリ\]:** コンバージョン カテゴリ。 使用できるカテゴリは、コンバージョンのタイプによって異なります。 *[!UICONTROL Calls to a phone number on your website]* および *[!UICONTROL Clicks to your number on your mobile website]* の場合、デフォルトで「[!UICONTROL Phone Call Lead]」が選択されています。

**\[ アクションの種類\]:** 目標が *[!UICONTROL Primary action used for bidding optimization]* と *[!UICONTROL Secondary action not used for bidding optimization]* のどちらであるか。

**[!UICONTROL Value]:** [ 各コンバージョンの値 ](https://support.google.com/google-ads/answer/3419241) の測定方法：

* *[!UICONTROL Use the same value for each conversion],* 通貨を選択し、各換算の値を入力する必要があります。

* *[!UICONTROL Use a different value for each conversion]、* 通貨を選択し、各換算にデフォルト値を入力する必要があります。 特定の web ページでタグを実装する際に、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:**[ クリックまたはインタラクションごとにカウントするコンバージョン数 ](https://support.google.com/google-ads/answer/3438531):*[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* または *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]:** コンバージョンが記録される広告インタラクション後の最大日数。 検索、ディスプレイ、ショッピングキャンペーンの場合、ウィンドウは 1～90 日です。 数値を選択するか、**[!UICONTROL Custom]** を選択して数値を入力します。

**[!UICONTROL View Through Conversion Window]:** ユーザーが広告を表示してから、ビュースルーコンバージョンが記録されるまでの最大日数。 検索、ディスプレイ、ショッピングキャンペーンの場合、ウィンドウは 1～90 日です。 数値を選択するか、**[!UICONTROL Custom]** を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [ 各広告インタラクションのクレジットの取得額 ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138):*[!UICONTROL Data driven]* または *[!UICONTROL Last click]*。 **メモ：** 以前、サポートされなくなった *[!UICONTROL First click]*、*[!UICONTROL Linear]*、*[!UICONTROL Time decay]* または *[!UICONTROL Position based]* モデルを使用していたコンバージョンアクションでは、*[!UICONTROL Data driven]* モデルを使用するようになりました。

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads]  検索、ソーシャル、Commerceのコンバージョンデータ ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
