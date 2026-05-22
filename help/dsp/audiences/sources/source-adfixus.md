---
title: ' [!DNL AdFixus]から1st パーティセグメントをインポート'
description: ' [!DNL AdFixus]  ユニバーサル IDで構成される [!DNL AdFixus]  ファーストパーティセグメントをDSPに読み込む方法について説明します。'
feature: DSP Audiences
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c1579802-ddd4-4214-8a91-97b2066abe11id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
source-git-commit: 79f0b3872a0d5d3765093ce83cc8f1c284a8255c
workflow-type: tm+mt
source-wordcount: 448
ht-degree: 0%

---

# [!DNL AdFixus]から1st パーティセグメントをインポート

*オーストラリアの広告主にのみ適用*

[!DNL AdFixus]とのAdvertising DSP統合を使用して、ターゲット広告のセグメントマッピング付きの[!DNL AdFixus] ユニバーサル IDをインポートします。[!DNL AdFixus] IDはオーストラリアでのみ利用可能です。 DSPでは、[!DNL AdFixus] IDを他のID タイプに変更したり、他のID タイプを[!DNL AdFixus] IDに変換したりすることはありません。 DSPでは、IDの読み込みに対して料金は発生しません。

[!DNL AdFixus] セグメントをDSPに読み込むと、プレースメントを[!DNL AdFixus] IDに、特定の1st パーティセグメントを[!DNL AdFixus]にターゲティングできます。 [!DNL AdFixus] セグメントを再利用可能なオーディエンスに追加することもできます。 任意のセグメントの詳細には、該当する[!DNL AdFixus] IDの数が含まれます。

カスタムレポートで[!DNL AdFixus] IDを持つユーザーのインプレッション、クリック数、頻度などの指標を表示できます。 [!DNL Analytics for Advertising]を持つ広告主は、Adobe Analyticsの[!DNL AdFixus] IDのビュースルーデータと、DSP内のAdobe Analyticsのデータも表示できます。

1. [!DNL AdFixus]を使用して、組織の1st パーティデータを[!DNL AdFixus]のIDを持つセグメントに変換します。

   これには、[!DNL AdFixus]とアクティブなライセンスキーを持つ別のアカウントが必要です。 また、web サイトのプロパティとドメインに[!DNL AdFixus]固有のコードを実装する必要があります。 [!DNL AdFixus]と直接連携して、IDを持つセグメントを生成します。

1. （広告主、[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)）次の[!DNL Analytics]の測定に対するトラッキングを設定します：

   1. （まだ実行していない場合）トラッキング URL](/help/integrations/analytics/ids.md)で、 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)および[AMO IDとEF IDを実装するための[すべての前提条件を完了してください。

   1. Web ページに[!DNL AdFixus]固有のコードをデプロイして、デスクトップおよびモバイル web ブラウザー（モバイルアプリではなく）の[!DNL AdFixus] IDからビュースルーへのコンバージョンを一致させます。

1. ファーストパーティ [!DNL AdFixus] セグメントをインポートします。

   1. [ オーディエンスソースを作成](source-manage.md) / [!UICONTROL Type] **[!UICONTROL AdFixus ID]**。 利用規約に同意する必要があります。

      ソース設定には、自動生成されたソースキーが含まれます。

   1. ソース キーを[!DNL AdFixus] チームと共有して、必要なセグメントをDSPにストリーミングできるようにします。

1. オーディエンスライブラリの[!UICONTROL First Party Segments] セクションで、セグメントが入力されていることを確認します（[!UICONTROL Audiences] > [!UICONTROL All Audiences]またはプレースメント設定内でオーディエンスを作成または編集する際に使用できます）。 [!DNL AdFixus] IDの数と[!DNL AdFixus]内のユーザーIDの数を比較します。

   セグメントは、作成後すぐにDSPで利用できます。

セグメントは更新され、3時間ごとにターゲティングで利用できますが、DSPに表示されるカウントは24時間ごとに更新されます。 **注：** セグメント内のインクルージョンは、[!DNL AdFixus]で設定した指定された有効期限の後に期限切れになります。 有効期限が切れる前に[!DNL AdFixus]からセグメントを再プッシュして、セグメントを更新します。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [ オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](source-manage.md)
>* [Adobe Advertising DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* Adobe Experience Platform [宛先カタログの概要](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/overview.html)
>* [ ユニバーサル IDのアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
