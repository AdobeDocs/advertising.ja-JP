---
title: Analysis WorkspaceのAdobe Advertising指標
description: Analysis WorkspaceのAdobe Advertising指標
feature: Integration with Adobe Analytics
exl-id: da5e5704-4504-4fc5-93d2-db7d28f0c349
source-git-commit: da69280679a4e0c5ce04f55ee94ce984745395ff
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Analysis WorkspaceのAdobe Advertising指標

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

>[!NOTE]
>
>* Adobe Advertisingがトラフィック指標およびディメンションを [!DNL Analytics] 毎日。
>* [!DNL Analytics] は、Adobe Advertisingのクリックスルー数とビュースルー数をリアルタイムで取り込みます。
>* の場合 [!DNL Search, Social, & Commerce]の場合、この機能は、ほとんどの広告ネットワークとキャンペーンタイプでサポートされます。 参照：[サポートされている在庫](/help/search-social-commerce/introduction/supported-inventory.md)」が [!DNL Search, Social, & Commerce] ガイドを参照してください。

## Adobe Advertisingからのトラフィック指標

Adobe Advertisingトラフィック指標 ( [!DNL Analytics] 通常は「Adobe Advertising」で始まる (「[!UICONTROL AMO ID Instances].&quot; ただし、（予約済みのイベントではなく）カスタムイベントを使用してクリック数、コストおよびインプレッション数の指標を最初に作成した長期的なお客様の場合、これらの指標は引き続き「AMO」で始まります。

| トラフィック指標 | 説明 |
| -------------- | ----------- |
| [!UICONTROL Adobe Advertising Clicks] または（一部のレガシー顧客） [!UICONTROL AMO Clicks] | 合計Adobe Advertisingクリック数。 |
| [!UICONTROL Adobe Advertising Cost] または（一部のレガシー顧客） [!UICONTROL AMO Cost] | Adobe Advertising費用はレポートスイートの通貨です。 |
| [!UICONTROL Adobe Advertising Impressions] または（一部のレガシー顧客） [!UICONTROL AMO Impressions] | Adobe Advertisingインプレッション数。 |
| [!UICONTROL Adobe Advertising Measurable Impressions] | 視認性計測が正常に初期化された、提供されたインプレッション数。 この値は、 （計測されたインプレッション数 — 測定できないインプレッション数）として計算されます。 |
| [!UICONTROL Adobe Advertising Minutes Viewed] | Adobe Advertisingビデオが視聴された時間（分）。 |
| [!UICONTROL Adobe Advertising Not Viewable Impressions] | 表示不可と判断されたインプレッションの数。 この値は ([!UICONTROL Adobe Advertising Measurable Impressions] - [!UICONTROL Adobe Advertising Viewable]) をクリックします。 |
| [!UICONTROL Adobe Advertising Viewable Impressions] | 配置設定に従って表示可能と測定されたインプレッション数。 |
| [!UICONTROL Adobe Advertising Views] | 広告の視聴回数。 ビューアがAdobe Advertisingビデオを開始すると、ビューがカウントされます。 |
| [!UICONTROL Adobe Advertising Views 25% Complete] | Adobe Advertisingビデオの少なくとも 25%が視聴された視聴回数。 |
| [!UICONTROL Adobe Advertising Views 50% Complete] | Adobe Advertisingビデオの 50%以上が視聴された視聴回数。 |
| [!UICONTROL Adobe Advertising Views 75% Complete] | Adobe Advertisingビデオの少なくとも 75%が視聴された視聴回数。 |
| [!UICONTROL Adobe Advertising Views 100% Complete] | Adobe Advertisingビデオの 100%が視聴された視聴回数。 |
| [!UICONTROL AMO ID Instances] | 次の回数： [!UICONTROL AMO ID] が設定されている。 |

## Adobe AdvertisingDimension

>[!NOTE]
>
>のすべてのAdobe Advertisingディメンション [!DNL Analytics] の後に「[!DNL (AMO ID)].&quot;

| Dimension | 適用可能なAdobe Advertisingデータ | 説明 |
| ----------- | ---------- | ---------- |
| [!UICONTROL Ad Platform (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | Advertising DSPまたは検索エンジン名 |
| [!UICONTROL Account (AMO ID] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | アカウント名。 |
| [!UICONTROL Network (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | RTB ([!DNL DSP]) または広告ネットワーク名 ([!DNL Search, Social, & Commerce]) |
| [!UICONTROL Campaign (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | キャンペーン名。 |
| [!UICONTROL Optimization (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | パッケージ ([!DNL DSP]) またはポートフォリオ ([!DNL Search, Social, & Commerce]) 名を入力します。 |
| [!UICONTROL Placement (AMO ID)] | [!DNL DSP] データ | 配置の名前。 |
| [!UICONTROL Ad Group (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告グループ名。 |
| [!UICONTROL Keyword (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワード。 |
| [!UICONTROL Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 検索一致タイプ。 |
| [!UICONTROL Keyword Match Type (AMO ID)] | [!DNL Search, Social, & Commerce] データ | キーワードと一致のタイプ。 |
| [!UICONTROL Ad Type (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告のタイプ（例： ） `text`, `video`, `display`または `native`. |
| [!UICONTROL Ad Title (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告タイプ ([!DNL DSP]) または広告タイトル ([!DNL Search, Social, & Commerce]) をクリックします。 |
| [!UICONTROL Ad Description (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | 広告の説明 ([!DNL DSP]) または広告本文 ([!DNL Search, Social, & Commerce]) をクリックします。 |
| [!UICONTROL Ad Display URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告に表示される URL。 |
| [!UICONTROL Ad Destination URL (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 広告のリンク先 URL。 |
| [!UICONTROL Landing Type (AMO ID)] | [!DNL DSP] および [!DNL Search, Social, & Commerce] データ | ランディングページのエントリがビュースルーかクリックスルーか。 |
| [!UICONTROL Product Target (AMO ID)] | [!DNL Search, Social, & Commerce] データ | 製品リスト広告の製品ターゲット。 |

## Adobe Advertisingに役立つカスタム計算指標

使用する指標データに対して、次の指標を作成することをAdobe Advertisingしてください。

* ランディングページインスタンスに対するクリック数 ([!UICONTROL AMO ID Instances] / [!UICONTROL Adobe Advertising Clicks])：これは、広告をクリックしてランディングページに表示したユーザーの割合です。
* 測定可能な率 ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Impressions] * 100)
* 表示可能なインプレッション率 ([!UICONTROL Adobe Advertising Viewable Impressions] / [!UICONTROL Adobe Advertising Measureable Impressions] * 100)
* ビュー単価 ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Views])
* クリック単価 ([!UICONTROL Adobe Advertising Cost] / [!UICONTROL Adobe Advertising Clicks])

>[!MORELIKETHIS]
>
>* [の概要 [!DNL Analytics for Advertising]](overview.md)
>* [[!DNL Analytics] データのAdobe Advertising](/help/integrations/analytics/analytics-data-in-advertising.md)
