---
title: ' [!DNL Adobe] [!DNL Real-time CDP] の機能を備えたDSP統合の使用'
description: DSPでファーストパーティセグメントを取り込む方法  [!DNL Adobe] [!DNL Real-time CDP] ついて説明します。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 91b08bf54f067666c9c27949ff740639738887d0
workflow-type: tm+mt
source-wordcount: '492'
ht-degree: 0%

---

# ユーザー ID を [!DNL Adobe Real-Time CDP] からユニバーサル ID に変換

*Beta機能*

Adobe Experience Platformの一部である [the [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html) とのDSP統合を使用して、ハッシュ化されたメールアドレスをターゲット広告のユニバーサル ID に変換します。

1. （メールアドレスを [!DNL RampIDs]<!-- or [!DNL ID5] IDs --> に変換するには：[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を使用する広告主） [!DNL Analytics] 測定のトラッキングを設定します。

   1. （まだ行っていない場合）すべての [ 実装の前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) と、トラッキング URL の [AMO ID と EF ID](/help/integrations/analytics/ids.md) を完了します。

   1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

      * **[!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへのコンバージョンに一致するように、web ページに追加のJavaScript タグをデプロイする必要があります（モバイルアプリは除く）。 Adobeアカウントチームに問い合わせてください。このチームには、[!DNL LiveRamp] Authentication Traffic Solutions の [!DNL LiveRamp] [!DNL LaunchPad] タグを登録する手順が記載されています。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

1. [ オーディエンスソースを作成 ](source-manage.md) して、オーディエンスをDSP アカウントまたは広告主アカウントにインポートします。 ユーザー識別子を任意の [ 使用可能なユニバーサル ID 形式 ](source-about.md) に変換するよう選択できます。

   ソース設定には、自動生成されたソースキーが含まれます。これは、次の手順で使用します。

1. Adobe Experience Platformで、DSP ソース設定で生成された [!UICONTROL Source Key] を使用して、Advertising DSP宛先接続を設定します。

   DSP宛先接続のアクティブ化、セグメントの選択および制御権限へのアクセス手順については、「[Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)」を参照してください。

   ソースメールアドレスは、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。

1. オーディエンスライブラリ（[!UICONTROL Audiences]/[!UICONTROL All Audiences] またはプレースメント設定内でオーディエンスを作成または編集する場合に使用できます）でセグメントが入力されていることを確認し、ユニバーサル ID の数を元のハッシュ化されたメールアドレスの数と比較します。

   セグメントは、24 時間以内にDSPで使用可能になります。 DSPがセグメントデータを受信したら、オーディエンス数は 9 時間以内に表示されます。 許容可能な ID 翻訳率と、セグメント数が変化する理由について詳しくは、「[ メール ID とユニバーサル ID の間のデータの相違 ](#universal-ids-data-variances) を参照してください。

セグメントは 24 時間ごとに更新されます。 ただし、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に有効期限が切れます。 有効期限が切れる前にReal-Time CDPからセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

## トラブルシューティング

翻訳率とユーザー数の問題のトラブルシューティングについては、「[ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)」を参照してください。

コンバージョン手順に関する問題のトラブルシューティングについては、Adobeアカウントチームまたは `adcloud-support@adobe.com` に問い合わせてください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](source-manage.md)
>* [Adobe Advertising DSP接続 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform[ 宛先カタログの概要 ](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
