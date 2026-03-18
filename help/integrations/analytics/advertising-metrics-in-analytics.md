---
title: Analysis WorkspaceのAdobe Advertising指標
description: Analysis WorkspaceのAdobe Advertising指標
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: 94a5b5591aef0aa5ae5d3459d547f52d939d559c
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 0%

---

# Analysis WorkspaceのAdobe Advertising指標

*Adobe AdvertisingとAdobe Analyticsの統合のみを利用する広告主*

>[!NOTE]
>
>* Adobe Advertisingは、トラフィック指標とディメンションを毎日 [!DNL Analytics] に渡します。
>* Adobe Advertising[!DNL Analytics] クリックスルーおよびビュースルーをリアルタイムでキャプチャします。
>* [!DNL Search, Social, & Commerce]：この機能は、ほとんどの広告ネットワークとキャンペーンタイプでサポートされています。 詳しくは、[ Guide の「](/help/search-social-commerce/introduction/supported-inventory.md) サポート対象インベントリ [!DNL Search, Social, & Commerce]」を参照してください。

## Adobe Advertisingからのトラフィック指標

[!DNL Analytics] のAdobe Advertising トラフィック指標は、「[!UICONTROL AMO ID Instances]」を除き、通常は「Adobe Advertising」で始まります。 ただし、長期的に見て、（予約済みイベントではなく）カスタムイベントを使用して、元々クリック数、コスト、インプレッション数の指標を作成していた顧客の場合、その指標は引き続き「AMO」で始まります。

| トラフィック指標 | 説明 |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] または（一部の従来のお客様） [!UICONTROL AMO Clicks] | Adobe Advertisingがクリックされた合計数。 |
| [!UICONTROL Adobe Advertising Cost] または（一部の従来のお客様） [!UICONTROL AMO Cost] | Adobe Advertising支出（レポートスイートの通貨で表示）。 |
| [!UICONTROL Adobe Advertising Impressions] または（一部の従来のお客様） [!UICONTROL AMO Impressions] | Adobe Advertising インプレッション数。 |
| [!UICONTROL Adobe Advertising Measurable Impressions] | ビューアビリティ インストルメンテーションが正常に初期化されたインプレッションの数です。 この値は、（計測インプレッション数 – 測定できないインプレッション数）として計算されます。 |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Adobe Advertising ビデオが表示された時間（分）。 |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | 表示可能でないと判断されたインプレッションの数。 この値は（[!UICONTROL Adobe Advertising Measurable Impressions] ～ [!UICONTROL Adobe Advertising Viewable]）として計算されます。 |
| [!UICONTROL Adobe Advertising Viewable Impressions] | プレースメント設定に従って表示可能と測定されたインプレッションの数。 |
| [!UICONTROL Adobe Advertising Views] | 広告の表示数。 ビューは、ビューアがAdobe Advertising ビデオを開始するとカウントされます。 |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Adobe Advertising ビデオの少なくとも 25% が視聴されたビューの数。 |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Adobe Advertising ビデオの少なくとも 50% が視聴されたビューの数。 |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Adobe Advertising ビデオの少なくとも 75% が視聴されたビューの数。 |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Adobe Advertising ビデオの 100% が視聴されたビューの数。 |
| [!UICONTROL AMO ID Instances] | [!UICONTROL AMO ID] が設定された回数。 |

## Adobe Advertising ディメンション

>[!NOTE]
>
>[!DNL Analytics] 内のすべてのAdobe Advertising ディメンションの後には、「[!DNL (AMO ID)]」が続きます。

| ディメンション | 適用可能なAdobe Advertising データ | 説明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | Advertising DSPまたは検索エンジン名 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | アカウント名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | RTB （[!DNL DSP]）または広告ネットワーク名（[!DNL Search, Social, & Commerce]） |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | キャンペーン名。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | パッケージ（[!DNL DSP]）またはポートフォリオ（[!DNL Search, Social, & Commerce]）の名前。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] データ | プレースメント名。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告グループ名。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワード。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 検索一致タイプ。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワードと一致のタイプ。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告タイプ （`text`、`video`、`display`、`native` など）。 |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告タイプ（[!DNL DSP]）または広告タイトル（[!DNL Search, Social, & Commerce]）。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告の説明（[!DNL DSP]）または広告本文（[!DNL Search, Social, & Commerce]）。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告に表示される URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告の宛先 URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | ランディングページのエントリがビュースルーかクリックスルーか。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 商品リスト広告の商品ターゲット。 |

## Adobe Advertisingに役立つカスタム計算指標

Adobe Advertising データについて、次の指標を作成することを検討します。

* ランディングページインスタンスへのクリック数（[!UICONTROL AMO ID Instances]/[!UICONTROL Adobe Advertising Clicks]）：広告をクリックしてランディングページに移動したユーザーの割合（%）。
* 測定可能な速度（[!UICONTROL Adobe Advertising Viewable Impressions]/[!UICONTROL Adobe Advertising Impressions] * 100）
* 表示可能インプレッション率（[!UICONTROL Adobe Advertising Viewable Impressions]/[!UICONTROL Adobe Advertising Measureable Impressions] * 100）
* ビューあたりのコスト （[!UICONTROL Adobe Advertising Cost]/[!UICONTROL Adobe Advertising Views]）
* クリックあたりのコスト （[!UICONTROL Adobe Advertising Cost]/[!UICONTROL Adobe Advertising Clicks]）

>[!MORELIKETHIS]
>
>* [ 概要  [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] Adobe Advertisingのデータ ](/help/integrations/analytics/analytics-data-in-advertising.md)
