---
title: ' [!DNL Adobe] [!DNL Real-time CDP]とのDSP統合の使用'
description: DSPで [!DNL Adobe] [!DNL Real-time CDP] ファーストパーティセグメントの取り込みを有効にする方法について説明します。
feature: DSP Audiences
exl-id: cb1da95b-0d19-4450-8770-6c383248ddae
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '540'
ht-degree: 0%

---

# ユーザーIDを[!DNL Adobe Real-Time CDP]からユニバーサル IDに変換

*Beta機能*

Adobe Experience Platformの一部である[the [!DNL Adobe Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/overview.html)とのDSP統合を使用して、ハッシュ化された電子メールアドレス、Cookie、モバイル広告IDなどのユーザーIDを、ターゲット広告のユニバーサル IDに変換します。

1. （ユーザーIDを[!DNL RampIDs]<!-- or [!DNL ID5] IDs -->に変換するには、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)を持つ広告主） [!DNL Analytics]の測定に対するトラッキングを設定します。

   1. （まだ実行していない場合）トラッキング URL[で、 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)および[AMO IDとEF IDを実装するための](/help/integrations/analytics/ids.md)すべての前提条件を完了してください。

   1. ユニバーサル ID パートナーに登録し、web ページにユニバーサル ID固有のコードをデプロイして、デスクトップおよびモバイルのweb ブラウザー（モバイルアプリは除く）のIDからビュースルーのコンバージョンを一致させます。

      * **[!DNL RampIDs]の場合：** デスクトップおよびモバイル web ブラウザー（モバイルアプリではない）のIDからビュースルーに一致させるには、web ページにJavaScript タグを追加してデプロイする必要があります。 Adobe アカウントチームにお問い合わせください。担当チームは、[!DNL LiveRamp]認証トラフィックソリューションから[!DNL LaunchPad] [!DNL LiveRamp] タグを登録する手順を説明します。 登録は無料ですが、契約書に署名する必要があります。 登録が完了すると、Adobeアカウントチームが独自のタグを生成し、web ページへの導入に使用します。

1. [&#x200B; オーディエンスソースを作成](source-manage.md)して、DSP アカウントまたは広告主アカウントにオーディエンスを読み込みます。 ユーザーIDを[使用可能なユニバーサル ID形式](source-about.md)のいずれかに変換することを選択できます。

   ソース設定には、自動生成されたソースキーが含まれ、次の手順で使用します。

1. Adobe Experience Platformで、DSP ソース設定で生成された[!UICONTROL Source Key]を使用して、Advertising DSP宛先接続を設定します。

   メールアドレスは、SHA-256 アルゴリズムを使用してハッシュ化する必要があります。

   DSP宛先接続のアクティブ化、オーディエンスのアクティブ化、データ書き出しの検証の手順については、「[Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)」を参照してください。

   >[!NOTE]
   >
   >ハッシュ化された電子メールアドレスのみをサポートする従来の接続は、「[Legacy Adobe Advertising Cloud DSP connection](https://experienceleague.adobe.com/en/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection-legacy)」と呼ばれるようになりました。 既に従来の接続を使用している場合は、すぐに変更を加える必要はありません。 ただし、従来の接続は最終的に削除されます。

1. オーディエンスライブラリ（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用可能）で、セグメントが入力されていることを確認し、ユニバーサル IDの数と元のユーザーIDの数を比較します。

   これらのセグメントは、24時間以内にDSPで利用できるようになります。 DSPがセグメントデータを受け取った後、オーディエンスサイズは9時間以内に表示されます。 使用可能なIDの翻訳率と、セグメント数が異なる理由については、「[&#x200B; メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

セグメントは24時間ごとに更新されます。 ただし、セグメントに含めるには、デフォルトで30日が経過するか、顧客が指定した有効期限が経過した後に有効期限が切れます。 有効期限が切れる前にReal-Time CDPからセグメントを再プッシュして、セグメントを更新します。 カスタムセグメントの有効期限をリクエストするには、Adobe アカウントチームにお問い合わせください。

## トラブルシューティング

翻訳率とユーザー数の問題をトラブルシューティングするには、「[&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)」を参照してください。

変換手順に関する問題をトラブルシューティングするには、Adobe アカウントチームまたは`adcloud-support@adobe.com`にお問い合わせください。

>[!MORELIKETHIS]
>
>* [&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [宛先カタログの概要](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [&#x200B; オーディエンス管理について](/help/dsp/audiences/audience-about.md)
