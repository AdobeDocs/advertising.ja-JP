---
title: ユーザー ID のユニバーサル ID  [!DNL Optimizely] ユニバーサル ID への変換
description: DSPがファーストパーティセグメントを取り込む [!DNL Optimizely] を有効にする方法について説明します。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 2c42e8e4b7ca7e0cfaaf7895f067e4ccf7a2a40e
workflow-type: tm+mt
source-wordcount: '625'
ht-degree: 0%

---

# ユーザー ID の [!DNL Optimizely] ID からユニバーサル ID への変換

*ベータ版機能*

Use the DSP integration with the [!DNL Optimizely] customer data platform to convert your organization&#39;s first-party hashed email addresses to universal IDs for targeted advertising.

1. (To convert email addresses to [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->; advertisers with [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） [Set up tracking to enable [!DNL Analytics] measurement](#analytics-tracking).

1. [Create an audience source in DSP](#source-create).

1. [Prepare and push the segment data](#push-data).

1. [Compare the number of universal IDs with the number of hashed email addresses](#compare-id-count).

## Step 1: Set up tracking for [!DNL Analytics] measurement {#analytics-tracking}

*[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md))のある広告主*

電子メールアドレスを変換するして ID を [!DNL RampIDs] または [!DNL ID5] するには、次の手順を実行する必要があります。

1. (まだ行っていない場合) [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) をすべてコンプリートプランし、トラッキング URL に [AMO ID と EF ID](/help/integrations/analytics/ids.md) が設定されていることを確認します。

1. ユニバーサルIDパートナーに登録し、ウェブページにユニバーサルID固有のコードをデプロイして、デスクトップとモバイルウェブブラウザ(モバイルアプリは除く)のIDから表示スルーIDへのコンバージョンを一致させます。

   * **[!DNL RampIDs]の場合:**&#x200B;ウェブページに追加のJavaScript タグデプロイして、デスクトップとモバイルウェブブラウザの ID(モバイルアプリは除く)のコンバージョンを表示スルーに一致させる必要があります。Contact your Adobe Account Team, who will give you instructions to register for a [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] Authentication Traffic Solutions. Registration is free, but you must sign an agreement. Once you register, your Adobe Account Team will generate and provide a unique tag for your organization to implement on your webpages.

## Step 2: Create an audience source in DSP {#source-create}

1. [Create an audience source](source-manage.md) to import audiences to your DSP account or an advertiser account. You can choose to convert your user identifiers to any of the [available universal ID formats](source-about.md).

   The source settings will include an auto-generated source key, which you&#39;ll use to push the segment data.

1. After you create the audience source, share the source code key with the [!DNL Optimizely] user.

## ステップ 3:セグメントデータを準備してプッシュする {#push-data}

広告主は、 [!DNL Optimizely] 担当者の助けを借りてデータを準備し、プッシュする必要があります。

1. [!DNL Optimizely Data Platform] 内で、SHA-256 アルゴリズムを使用して、広告主のオーディエンスの電子メール ID ハッシュします。

1. の [[!DNL Optimizely's] 指示に従って、セグメントをDSP](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)に押します。 統合を有効にするには、次の情報を含めます。

   * **Source Key:** This is the source key created in [Step 2](#source-create).

   * **Account Code:** This is the alphanumeric DSP Account Code, which you can find within DSP at [!UICONTROL Settings] > [!UICONTROL Account].

The segments should be available in DSP within 24 hours and are refreshed as configured for the advertiser. Regardless of how frequently the segment is refreshed, inclusion in a segment expires after 30 days by default or after a customer-specified expiration period. Refresh your segments by re-pushing them from [!DNL Optimizely] prior to the expiration. To request a custom segment expiration, contact your Adobe Account Team.

## Step 4: Compare the number of universal IDs with the number of hashed email addresses {#compare-id-count}

すべての手順を完了したら、オーディエンスライブラリ ( [!UICONTROL Audiences] > [!UICONTROL All Audiences] または 配置設定内でオーディエンスを作成または編集するときに使用可能) で、セグメントが使用可能であり、24 時間以内に入力されていることを確認します。 Compare the number of universal IDs with the number of original hashed email addresses.

ハッシュ化された電子メールアドレスからユニバーサル ID への変換率は 90%以上である必要があります。 たとえば、顧客 データプラットフォームから 100 個のハッシュ化された電子メールアドレスを送信する場合は、90 を超えるユニバーサル ID に変換する必要があります。 翻訳率90%以下が課題です。 セグメント数がどのように異なるかについて詳しくは、「[電子メール ID とユニバーサル ID のデータ相違の原因](#universal-ids-data-variances)」を参照してください。

トラブルシューティングのサポートについては、Adobe Systems アカウントチームまたは `adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
