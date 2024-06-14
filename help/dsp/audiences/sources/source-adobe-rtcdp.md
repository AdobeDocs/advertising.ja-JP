---
title: とのDSP統合の使用 [!DNL Adobe] [!DNL Real-time CDP]
description: DSPでのデータの取り込みを有効にする方法を説明します [!DNL Adobe] [!DNL Real-time CDP] ファーストパーティセグメント。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 7963623d20686553629e2aa7ad76b4fd48403555
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 0%

---

# からのユーザー ID の変換 [!DNL Adobe Real-Time CDP] ユニバーサル ID に

*ベータ版機能*

とのDSP統合の使用 [この [!DNL Adobe Real-Time Customer Data Platform (CDP)]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)はAdobe Experience Platformの一部で、ターゲット広告のために、ハッシュ化されたメールアドレスをユニバーサル ID に変換します。

1. （メールアドレスを変換： [!DNL RampIDs]<!-- or [!DNL ID5] IDs -->、を使用する広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)） トラッキングの設定 [!DNL Analytics] 測定：

   1. （まだ完了していない場合）すべて完了 [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) および [トラッキング URL の AMO ID と EF ID](/help/integrations/analytics/ids.md).

   1. ユニバーサル ID パートナーに登録し、Web ページにユニバーサル ID 固有のコードをデプロイして、デスクトップおよびモバイル Web ブラウザーの ID からビュースルーへのコンバージョンに一致させます（モバイルアプリは除く）。

      * **の場合 [!DNL RampIDs]:** デスクトップおよびモバイル web ブラウザーの ID からビュースルーへの変換に一致するように（モバイルアプリではなく）、web ページに追加の JavaScript タグをデプロイする必要があります。 Adobeアカウントチームにお問い合わせください。チームからは、に登録するための手順が示されます [!DNL LiveRamp] [!DNL LaunchPad] tag from [!DNL LiveRamp] 認証トラフィックソリューション。 登録は無料ですが、契約書に署名する必要があります。 登録後、Adobeアカウントチームは、組織が web ページに実装するための一意のタグを生成し、提供します。

1. [オーディエンスソースの作成](source-manage.md) オーディエンスをDSP アカウントまたは広告主アカウントに読み込みます。 ユーザー識別子を任意のに変換することもできます [使用可能なユニバーサル ID 形式](source-about.md).

   ソース設定には、自動生成されたソースキーが含まれます。これは、次の手順で使用します。

1. Adobe Experience Platformで、を使用して Advertising DSP宛先接続を設定します [!UICONTROL Source Key] これは、DSP ソース設定で生成されました。

   DSP宛先接続のアクティブ化、セグメントの選択および制御権限へのアクセス手順については、「」を参照してください[Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html).」と入力します。

   ソースメールアドレスは、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。

1. すべての手順を完了したら、オーディエンスライブラリ（からオーディエンスを作成または編集する際に使用可能）で検証します。 [!UICONTROL Audiences] > [!UICONTROL All Audiences] またはプレースメント設定内）を選択した場合、24 時間以内にセグメントが入力されます。 ユニバーサル ID の数と、元のハッシュ化されたメールアドレスの数を比較します。

   ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。 例えば、顧客データプラットフォームからハッシュ化されたメールアドレスを 100 個送信する場合は、90 個を超えるユニバーサル ID に翻訳する必要があります。 90% 以下の翻訳率が課題です。 セグメント数の変化について詳しくは、「」を参照してください[メール ID とユニバーサル ID のデータの相違の原因](#universal-ids-data-variances).」と入力します。

   トラブルシューティングのサポートについては、Adobeアカウントチームまたは `adcloud-support@adobe.com`.

セグメントは 24 時間ごとに更新されます。 ただし、セグメントへの追加は、デフォルトで 30 日後、または顧客が指定した有効期限が切れた後に有効期限が切れます。 有効期限が切れる前にReal-Time CDPからセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobeアカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](source-manage.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [宛先カタログの概要](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [ユニバーサル ID の有効化のサポート](/help/dsp/audiences/universal-ids.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
