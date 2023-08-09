---
title: のコンバージョンタグを作成します。 [!DNL Google Ads]
description: を作成する方法を学ぶ [!DNL Google Ads] コンバージョンタグです。
feature: Conversions
source-git-commit: af32aea1c50edb6b22b0b15c920cb8c2dcdc37e9
workflow-type: tm+mt
source-wordcount: '379'
ht-degree: 0%

---

# のコンバージョンタグを作成します。 [!DNL Google Ads]

個々のコンバージョンを追跡する新しいコンバージョン用のコンバージョンタグを作成できます。 [!DNL Google Ads] アカウントを管理するアカウントレベルでは追跡されません。

既存のコンバージョンのコンバージョンタグを生成するには、広告ネットワークのエディターを使用します。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 次を指定します。 [コンバージョンタグの設定](#conversion-tag-settings-google).

   1. アカウントを選択し、コンバージョンタイプを選択します。

   1. クリック **[!UICONTROL Next]**.

   1. 変換オプションを指定します。

   1. クリック **[!UICONTROL Generate]**.

1. コンバージョンタグをコピーして、コンバージョン指標を追跡する Web サイトに実装します。

   詳しくは、「 [!DNL Google] タグ」 [!DNL Google Ads] 」をクリックします。[2. Googleタグの設定](https://support.google.com/google-ads/answer/12215519).&quot;

1. クリック **[!UICONTROL Done].**

Web サイトにタグを追加し、実行を開始すると、 [!DNL Google Ads] はコンバージョンを Web サイトに記録します。 検索、ソーシャル、コマースは、コンバージョンを毎日同期します。 同期されたデータの詳細については、「[[!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md).

## コンバージョンタグの設定 {#conversion-tag-settings-google}

**[!UICONTROL Select an Account]:** 該当するGoogle Ads アカウント。

**[!UICONTROL Type of Conversion]:** 追跡するコンバージョンのタイプ。 *[!UICONTROL Click on a webpage element]*, *[!UICONTROL Calls to a phone number on your website]*&#x200B;または *[!UICONTROL Clicks to your number on your mobile website]*.

**[!UICONTROL Conversion Name]:** コンバージョン指標の一意の名前。

**\[ 目標カテゴリ\]:** コンバージョン目標。 使用可能な目標は、コンバージョンのタイプによって異なります。 の場合 *[!UICONTROL Calls to a phone number on your website]* および *[!UICONTROL Clicks to your number on your mobile website]*, &quot;[!UICONTROL Phone Call Lead]」がデフォルトで選択されています。

**\[ アクションタイプ\]:** 目標が *[!UICONTROL Primary action used for bidding optimization]* または *[!UICONTROL Secondary action not used for bidding optimization]*.

**[!UICONTROL Value]:** の測定方法 [各コンバージョンの値](https://support.google.com/google-ads/answer/3419241):

* *[!UICONTROL Use the same value for each conversion],* 通貨を選択し、各コンバージョンの値を入力する必要があります。

* *[!UICONTROL Use a different value for each conversion],* 通貨を選択し、各コンバージョンのデフォルト値を入力する必要があります。 特定の Web ページにタグを実装する際に、タグ内のデフォルト値をトランザクション固有の値で変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [クリックまたはインタラクションごとにカウントするコンバージョン数](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* または *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*.

**[!UICONTROL Click Through Conversion Window]:** コンバージョンが記録される広告インタラクション後の最大日数。 検索、表示および買い物キャンペーンの場合、ウィンドウは 1 ～ 90 日にすることができます。 数値を選択するか、 **[!UICONTROL Custom]** をクリックし、数値を入力します。

**[!UICONTROL View Through Conversion Window]:** ユーザーが広告を表示してから、ビュースルーコンバージョンが記録されるまでの最大日数です。 検索、表示および買い物キャンペーンの場合、ウィンドウは 1 ～ 90 日にすることができます。 数値を選択するか、 **[!UICONTROL Custom]** をクリックし、数値を入力します。

**[!UICONTROL Attribution Model]:** [各広告インタラクションが受け取るクレジットの量](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*, *[!UICONTROL Last click]*, *[!UICONTROL First click]*, *[!UICONTROL Linear]*, *[!UICONTROL Time decay]*&#x200B;または *[!UICONTROL Position based]*.

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads] 検索、ソーシャル、コマースのコンバージョンデータ](/help/search-social-commerce/campaign-management/introduction/google-conversion-data.md)
