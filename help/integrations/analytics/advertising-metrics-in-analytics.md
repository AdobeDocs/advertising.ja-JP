---
title: Analysis WorkspaceのAdobe Advertising指標
description: Analysis WorkspaceのAdobe Advertising指標
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
TQID: https://experienceleague.adobe.com/CLPeE8g0Mix4Scq90qCd-s-tCUuBmkTBrkBWT1aPEhw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 495
ht-degree: 0%

---

# Analysis WorkspaceのAdobe Advertising指標

*Adobe AdvertisingとAdobe Analyticsの統合のみを使用する広告主*

>[!NOTE]
>
>* Adobe Advertisingは、毎日[!DNL Analytics]にトラフィック指標とディメンションを渡します。
>* [!DNL Analytics]は、Adobe Advertisingのクリックスルーとビュースルーをリアルタイムでキャプチャします。
>* [!DNL Search, Social, & Commerce]の場合、この機能はほとんどの広告ネットワークとキャンペーンの種類でサポートされています。 詳しくは、[ ガイドの「](/help/search-social-commerce/introduction/supported-inventory.md) サポートされているインベントリ [!DNL Search, Social, & Commerce]」を参照してください。

## Adobe Advertisingのトラフィック指標

[!DNL Analytics]のAdobe Advertising トラフィック指標は、通常、「[!UICONTROL AMO ID Instances]」以外は「Adobe Advertising」で始まります。 ただし、当初クリック数、コスト、インプレッション数の指標を作成するために（予約イベントではなく）カスタムイベントを使用した長期的な顧客の場合、これらの指標はまだ「AMO」で始まります。

| トラフィック指標 | 説明 |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks]または（一部のレガシー顧客） [!UICONTROL AMO Clicks] | Adobe Advertisingの合計クリック数。 |
| [!UICONTROL Adobe Advertising Cost]または（一部のレガシー顧客） [!UICONTROL AMO Cost] | Adobe Advertisingの支出は、レポートスイートの通貨で行われます。 |
| [!UICONTROL Adobe Advertising Impressions]または（一部のレガシー顧客） [!UICONTROL AMO Impressions] | Adobe Advertising インプレッションの数。 |
| [!UICONTROL Adobe Advertising Measurable Impressions] | ビューアビリティ計測が正常に初期化されたインプレッションの数です。 この値は、（インストルメントされたインプレッション – 測定不可能なインプレッションの数）として計算されます。 |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Adobe Advertising ビデオが表示された分数。 |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | 表示できないと判断されたインプレッションの数。 この値は（[!UICONTROL Adobe Advertising Measurable Impressions] ～ [!UICONTROL Adobe Advertising Viewable]）として計算されます。 |
| [!UICONTROL Adobe Advertising Viewable Impressions] | 配置設定に従って表示可能に測定されたインプレッションの数。 |
| [!UICONTROL Adobe Advertising Views] | 広告の閲覧数。 ビューアがAdobe Advertising ビデオを開始すると、ビューがカウントされます。 |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Adobe Advertising動画の少なくとも25%が視聴された再生回数。 |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Adobe Advertising ビデオの少なくとも50%が視聴された再生回数。 |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Adobe Advertising動画の少なくとも75%が視聴された再生回数。 |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Adobe Advertising ビデオの100%が視聴された再生回数。 |
| [!UICONTROL AMO ID Instances] | [!UICONTROL AMO ID]が設定された回数。 |

## Adobe Advertisingのディメンション

>[!NOTE]
>
>[!DNL Analytics]のすべてのAdobe Advertising ディメンションの後には、「[!DNL (AMO ID)]」が続きます。

| ディメンション | 適用可能なAdobe Advertising データ | 説明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | Advertising DSPまたは検索エンジン名 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | アカウント名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | RTB （[!DNL DSP]）または広告ネットワーク名（[!DNL Search, Social, & Commerce]） |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | キャンペーン名。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | パッケージ （[!DNL DSP]）またはポートフォリオ （[!DNL Search, Social, & Commerce]）の名前。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] データ | プレースメント名。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告グループ名。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワード。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 検索の一致タイプ。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワードと一致タイプ。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | 広告タイプ（`text`、`video`、`display`、`native`など）。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | 広告タイプ （[!DNL DSP]）または広告タイトル （[!DNL Search, Social, & Commerce]）。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | 広告説明（[!DNL DSP]）または広告本文（[!DNL Search, Social, & Commerce]）。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告に表示されるURL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告の宛先URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP]および[!DNL Search, Social, & Commerce] データ | ランディングページのエントリがビュースルーまたはクリックスルーのどちらであったか。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 製品リスト広告の製品ターゲット。 |

## Adobe Advertisingの便利なカスタム計算指標

Adobe Advertisingデータについて、次の指標の作成を検討してください。

* ランディングページインスタンスへのクリック数（[!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks]）：これは、広告をクリックしてランディングページに到達したユーザーの割合です。
* 測定可能なレート （[!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100）
* 表示可能なインプレッション率（[!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100）
* 表示単価（[!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views]）
* クリック単価（[!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks]）

>[!MORELIKETHIS]
>
>* [概要： [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe Advertisingのデータ ](/help/integrations/analytics/analytics-data-in-advertising.md)
