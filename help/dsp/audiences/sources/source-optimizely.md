---
title: ユーザー ID をユニバーサル ID [!DNL Optimizely]  からユニバーサル ID に変換
description: DSPでファーストパーティセグメントを取り込む方法  [!DNL Optimizely]  説明します。
feature: DSP Audiences
exl-id: 2c48a874-132a-4e5c-ba24-0e7ab80ac2d4
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 0%

---

# ユーザー ID を [!DNL Optimizely] からユニバーサル ID に変換

*Beta機能*

DSPと [!DNL Optimizely] customer data platform の統合を使用すると、組織のファーストパーティのハッシュ化されたメールアドレスを、ターゲット広告のためのユニバーサル ID に変換できます。

1. （メールアドレスを [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> に変換するには：[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主） [&#x200B; トラッキングを設定して有効  [!DNL Analytics]  測定 &#x200B;](#analytics-tracking) します。

1. [DSPでオーディエンスソースを作成 &#x200B;](#source-create) します。

1. [&#x200B; セグメントデータの準備とプッシュ &#x200B;](#push-data)。

1. [&#x200B; ユニバーサル ID の数とハッシュ化されたメールアドレスの数を比較 &#x200B;](#compare-id-count)。

## 手順 1:[!DNL Analytics] 測定のトラッキングの設定 {#analytics-tracking}

*[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主）*

メールアドレスを [!DNL RampIDs] ID または [!DNL ID5] ID に変換するには、次の手順を実行する必要があります。

1. （まだ行っていない場合）すべての [&#x200B; 実装の前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) を完了し、[AMO ID と EF ID](/help/integrations/analytics/ids.md) がトラッキング URL に入力されていることを確認します。

1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

   * **[!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへのコンバージョンに一致するように、web ページに追加のJavaScript タグをデプロイする必要があります（モバイルアプリは除く）。 Adobeアカウントチームに問い合わせてください。このチームには、[!DNL LiveRamp] Authentication Traffic Solutions の [!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順が記載されています。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

## 手順 2:DSPでのオーディエンスソースの作成 {#source-create}

1. [&#x200B; オーディエンスソースを作成 &#x200B;](source-manage.md) して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 ユーザー識別子を任意の [&#x200B; 使用可能なユニバーサル ID 形式 &#x200B;](source-about.md) に変換するよう選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、セグメントデータのプッシュに使用されます。

1. オーディエンスソースを作成したら、[!DNL Optimizely] ユーザーとソースコードキーを共有します。

## 手順 3：セグメントデータの準備とプッシュ {#push-data}

広告主は、[!DNL Optimizely Data Platform] を使用してデータを準備し、プッシュする必要があります。 プロセスに関するご質問については、[!DNL Optimizely] 担当者にお問い合わせください。

1. [!DNL Optimizely Data Platform] 内で、SHA-256 アルゴリズムを使用して、オーディエンスのメール ID をハッシュ化します。

1. の [[!DNL Optimizely's]  手順に従って、セグメントをDSPにプッシュします &#x200B;](https://support.optimizely.com/hc/en-us/articles/27974930963981-Integrate-Adobe-Ads)。 統合を有効にするには、以下の情報を含めます。

   * **Source キー：** これは、[&#x200B; 手順 2](#source-create) で作成されたソースキーです。

   * **アカウントコード：** 英数字のDSP アカウントコードで、DSPの [!UICONTROL Settings]/[!UICONTROL Account] にあります。

セグメントは、広告主の設定に従って更新されます。 セグメントの更新頻度に関係なく、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に期限切れになります。 有効期限が切れる前に [!DNL Optimizely] からセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

## 手順 4：ユニバーサル ID の数とハッシュ化されたメールアドレスの数の比較 {#compare-id-count}

セグメントは、24 時間以内にDSPで使用可能になります。 DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。

オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）で、セグメントが使用可能であり、入力されていることを確認し、ユニバーサル ID の数を元のハッシュ化されたメールアドレスの数と比較します。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「[&#x200B; メール ID とユニバーサル ID の間のデータの相違 &#x200B;](#universal-ids-data-variances) を参照してください。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「[&#x200B; ユニバーサル ID のアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)」を参照してください。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com` に問い合わせてください。

>[!MORELIKETHIS]
>
>* [&#x200B; ファーストパーティオーディエンスソースについて &#x200B;](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 &#x200B;](source-manage.md)
>* [&#x200B; ユニバーサル ID のアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について &#x200B;](/help/dsp/audiences/audience-about.md)
