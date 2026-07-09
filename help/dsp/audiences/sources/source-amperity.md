---
title: ユーザーIDを [!DNL Amperity] からユニバーサル IDに変換
description: DSPで [!DNL Amperity]  ファーストパーティセグメントの取り込みを有効にする方法について説明します。
feature: DSP Audiences
exl-id: c751709a-5ad2-43fa-ba3a-fc7a9683da3f
TQID: https://experienceleague.adobe.com/LOl3N6NB0alkOXiTNe7Xzj9mcVVfYxog3x-iIuVa82M
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 50af5a8fc6e5e82268489259073e27911ca5a45c
workflow-type: tm+mt
source-wordcount: 708
ht-degree: 0%

---

# ユーザーIDを[!DNL Amperity]からユニバーサル IDに変換

[!DNL Amperity] Customer Data PlatformとのDSP統合を使用して、組織の1st パーティハッシュ化されたメールアドレスを、ターゲット広告のユニバーサル IDに変換します。

1. （電子メールアドレスを[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->に変換するには、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を持つ広告主） [&#x200B; トラッキングを設定して [!DNL Analytics] 測定](#analytics-tracking)を有効にします。

1. [DSPでオーディエンスソースを作成](#source-create)。

1. [&#x200B; セグメントマッピングデータの準備と共有](#map-data)。

1. [DSP](#push-data)への [!DNL Amperity] からのデータプッシュをリクエストします。

1. [&#x200B; ユニバーサル IDの数とハッシュ化された電子メールアドレスの数を比較](#compare-id-count)。

## 手順1: [!DNL Analytics]測定用トラッキングの設定 {#analytics-tracking}

*広告主と[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）*

メールアドレスを[!DNL RampIDs]または[!DNL ID5]のIDに変換するには、次の操作を行う必要があります。

1. （まだ実行していない場合）実装の[&#128279;](/help/integrations/analytics/prerequisites.md)前提条件をすべて完了し、[AMO IDとEF ID](/help/integrations/analytics/ids.md)がトラッキング URLに入力されていることを確認します。 [!DNL Analytics for Advertising]

1. ユニバーサル ID パートナーに登録し、web ページにユニバーサル ID固有のコードをデプロイして、デスクトップおよびモバイルのweb ブラウザー（モバイルアプリは除く）のIDからビュースルーのコンバージョンを一致させます。

   * **[!DNL RampIDs]の場合：** デスクトップおよびモバイル web ブラウザー（モバイルアプリではない）のIDからビュースルーに一致させるには、web ページにJavaScript タグを追加してデプロイする必要があります。 [!DNL LiveRamp]認証トラフィックソリューション（ats.js）から[!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順については、Adobe アカウントチームにお問い合わせください。 登録は無料ですが、契約書に署名する必要があります。 登録が完了すると、Adobeアカウントチームが独自のタグを生成し、web ページへの導入に使用します。

## 手順2:DSPでオーディエンスソースを作成する {#source-create}

1. [&#x200B; オーディエンスソースを作成](source-manage.md)して、DSP アカウントまたは広告主アカウントにオーディエンスを読み込みます。 ユーザーIDを[使用可能なユニバーサル ID形式](source-about.md)のいずれかに変換することを選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用します。

1. オーディエンスソースを作成したら、ソースコードのキーを[!DNL Amperity] ユーザーと共有します。

## 手順3：セグメントマッピングデータの準備と共有 {#map-data}

広告主は、セグメントマッピングデータを準備して共有する必要があります。

1. [!DNL Amperity]内で、SHA-256 アルゴリズムを使用してオーディエンスのメール IDをハッシュ化します。

1. 広告主は、DSPでセグメントを作成するために、Adobe アカウントチームにセグメントマッピングデータを提供する必要があります。 コンマ区切りの値ファイルでは、次の列名と値を使用します。

   * **外部セグメントキー：** セグメントに関連付けられた[!DNL Amperity] セグメントキー。

   * **セグメント名：** セグメント名。

   * **セグメントの説明：** セグメントの目的またはルール、またはその両方。

   * **親ID:**&#x200B;空白のままにする

   * **ビデオ CPM:** 0

   * **CPMの表示：** 0

   * **セグメントウィンドウ：** セグメントの有効期間。

## 手順4: [!DNL Amperity]からDSPへのデータプッシュをリクエストする {#push-data}

1. DSP内でセグメントがマッピングされた後、広告主は[!DNL Amperity]担当者と協力してセグメントデータをDSPに配信する必要があります。

1. その後、広告主はAdobe アカウントチームに対して、セグメントデータが受信されたことを確認する必要があります。

これらのセグメントは、24時間以内にDSPで利用できるようになります。 オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用できる）で、セグメントが使用可能であり、入力されていることを確認します。

セグメントは、[!DNL Amperity]以内に広告主向けに設定されたとおりに更新されます。 セグメントが更新される頻度に関係なく、セグメントに含める有効期限は、デフォルトで30日後、または顧客が指定した有効期限の後に切れます。 有効期限が切れる前に[!DNL Amperity]からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobe アカウントチームにお問い合わせください。

## 手順5：ユニバーサル IDの数とハッシュ化された電子メールアドレスの数を比較する {#compare-id-count}

DSPがセグメントデータを受け取った後、オーディエンスサイズは9時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用可能）で、ユニバーサル IDの数とハッシュ化された元のメールアドレスの数を比較します。 使用可能なIDの翻訳率と、セグメント数が異なる理由については、「[&#x200B; メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

## トラブルシューティング

翻訳率とユーザー数の問題をトラブルシューティングするには、「[&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)」を参照してください。

変換手順に関する問題をトラブルシューティングするには、Adobe アカウントチームまたは`adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; オーディエンス管理について](/help/dsp/audiences/audience-about.md)
