---
title: ユーザーIDを [!DNL Optimizely] からユニバーサル IDに変換
description: DSPで [!DNL Optimizely]  ファーストパーティセグメントの取り込みを有効にする方法について説明します。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
TQID: https://experienceleague.adobe.com/lT5w6rvO5OmO5l-6rnSsVn6liPnbZxTFrvU4umR4aHQ
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 612
ht-degree: 0%

---

# ユーザーIDを[!DNL Optimizely]からユニバーサル IDに変換

*Beta機能*

[!DNL Optimizely] Customer Data PlatformとのDSP統合を使用して、組織の1st パーティハッシュ化されたメールアドレスを、ターゲット広告のユニバーサル IDに変換します。

1. （電子メールアドレスを[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->に変換するには、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を持つ広告主） [ トラッキングを設定して [!DNL Analytics] 測定](#analytics-tracking)を有効にします。

1. [DSPでオーディエンスソースを作成](#source-create)。

1. [ セグメントデータを準備してプッシュ ](#push-data)。

1. [ ユニバーサル IDの数とハッシュ化された電子メールアドレスの数を比較](#compare-id-count)。

## 手順1: [!DNL Analytics]測定用トラッキングの設定 {#analytics-tracking}

*広告主と[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスを[!DNL RampIDs]または[!DNL ID5]のIDに変換するには、次の操作を行う必要があります。

1. （まだ実行していない場合）実装の[前提条件をすべて完了し、 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)AMO IDとEF ID[がトラッキング URLに入力されていることを確認します。](/help/integrations/analytics/ids.md)

1. ユニバーサル ID パートナーに登録し、web ページにユニバーサル ID固有のコードをデプロイして、デスクトップおよびモバイルのweb ブラウザー（モバイルアプリは除く）のIDからビュースルーのコンバージョンを一致させます。

   * **[!DNL RampIDs]の場合：** デスクトップおよびモバイル web ブラウザー（モバイルアプリではない）のIDからビュースルーに一致させるには、web ページにJavaScript タグを追加してデプロイする必要があります。 Adobe アカウントチームにお問い合わせください。担当チームは、[!DNL LiveRamp]認証トラフィックソリューションから[!DNL LaunchPad] [!DNL LiveRamp] タグを登録する手順を説明します。 登録は無料ですが、契約書に署名する必要があります。 登録が完了すると、Adobeアカウントチームが独自のタグを生成し、web ページへの導入に使用します。

## 手順2:DSPでオーディエンスソースを作成する {#source-create}

1. [ オーディエンスソースを作成](source-manage.md)して、DSP アカウントまたは広告主アカウントにオーディエンスを読み込みます。 ユーザーIDを[使用可能なユニバーサル ID形式](source-about.md)のいずれかに変換することを選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用します。

1. オーディエンスソースを作成したら、ソースコードのキーを[!DNL Optimizely] ユーザーと共有します。

## 手順3：セグメントデータの準備とプッシュ {#push-data}

広告主は、[!DNL Optimizely Data Platform]を使用してデータを準備およびプッシュする必要があります。 このプロセスに関するご質問は、[!DNL Optimizely]担当者にお問い合わせください。

1. [!DNL Optimizely Data Platform]内で、SHA-256 アルゴリズムを使用してオーディエンスのメール IDをハッシュ化します。

1. セグメントをDSP[[!DNL Optimizely's] にプッシュするには、次の](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)の手順に従います。 統合を有効にするには、次の情報を含めます。

   * **Source キー：**&#x200B;これは、[手順2](#source-create)で作成したソース キーです。

   * **アカウントコード：**&#x200B;これは英数字のDSP アカウントコードです。DSP内の[!UICONTROL Settings] > [!UICONTROL Account]で確認できます。

セグメントは、広告主用に設定されたとおりに更新されます。 セグメントが更新される頻度に関係なく、セグメントに含める有効期限は、デフォルトで30日後、または顧客が指定した有効期限の後に切れます。 有効期限が切れる前に[!DNL Optimizely]からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobe アカウントチームにお問い合わせください。

## 手順4：ユニバーサル IDの数とハッシュ化されたメールアドレスの数を比較する {#compare-id-count}

これらのセグメントは、24時間以内にDSPで利用できるようになります。 DSPがセグメントデータを受け取った後、オーディエンスサイズは9時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用できる）で、セグメントが使用可能で入力されていることを確認し、ユニバーサル IDの数と元のハッシュ化されたメールアドレスの数を比較します。 使用可能なIDの翻訳率と、セグメント数が異なる理由については、「[ メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

## トラブルシューティング

翻訳率とユーザー数の問題をトラブルシューティングするには、「[ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

変換手順に関する問題をトラブルシューティングするには、Adobe アカウントチームまたは`adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [ オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
