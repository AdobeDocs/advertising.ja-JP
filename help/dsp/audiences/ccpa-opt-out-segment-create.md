---
title: CCPA販売停止セグメントを作成して実装する
description: 消費者のオプトアウト要求からユーザーIDを追跡するセグメントを作成して実装する方法について説明します。
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
TQID: https://experienceleague.adobe.com/NYXgnUkEw4uSilL8LO8qlRPp5AVAjXeXNS0pVeIZl3Y
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 405
ht-degree: 0%

---

# CCPA販売停止セグメントを作成して実装する

カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイト上の消費者のオプトアウト要求からユーザーIDを追跡するセグメントを作成できます。 ユーザーはCCPAの販売不可セグメントに無期限で残ります。

セグメントピクセルタグが実装されると、Adobe Advertisingは広告主の代わりにID プールの収集を開始します。

>[!NOTE]
>
>* Adobe Experience Platform Privacy Service APIを使用してCCPA オプトアウトオブセールリクエストをAdobe Advertisingに通知する方法について詳しくは、[https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=ja](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html?lang=ja)を参照してください。
>* CCPA オプトアウトオブセールスイベントのトラッキングに関連しない目的でweb ページにアクセスするユーザーと、デスクトップ、モバイル、およびCTV デバイスから広告に露出したユーザーを追跡するには、[&#x200B; カスタムセグメント &#x200B;](/help/dsp/audiences/custom-segment-create.md)を作成します。

1. セグメントを作成します。

   1. メインメニューで、**オーディエンス / セグメント**&#x200B;をクリックします。

   1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

   1. 一意の&#x200B;**[!UICONTROL Segment Name]**&#x200B;を入力してください。

      推奨されるセグメント名：「&lt;*広告主名*> - CCPA オプトアウトの販売」（「Acme - CCPA オプトアウトの販売」など）

   1. [!UICONTROL Segment Type]の場合は、**[!UICONTROL CCPA Opt-out of sale]**&#x200B;を選択します。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. ピクセルタグをコピーして実装し、セグメントを追跡します。

   1. **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**&#x200B;に戻ります。

   1. セグメント行で、新しいセグメントの上にカーソルを置き、**[!UICONTROL Get pixel]**&#x200B;をクリックします。

   1. 画像ピクセル（`<img src="https://rtd-tm.everesttech.net"`で始まる）をコピーして、web ページにアクセスするデスクトップおよびモバイル訪問者のユーザーIDを収集します。

   1. 広告主またはweb サイトの担当者に、CCPAの販売拒否リクエストを追跡するために使用するメカニズム（同意管理プラットフォームの使用など）を使用して、デプロイメント用のタグを提供します。

      広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。

      ピクセルが実装されると、Adobe Advertisingは広告主の代わりにID プールの収集を開始します。

      実装の選択とロジックは広告主次第ですが、広告主がピクセルを起動する方法の例を次に示します。

      1. 消費者が広告主のホームページにアクセスします。
      1. 消費者は、広告主の「CCPAが販売停止をオプトアウト」ボタンを見つけてクリックします。
      1. 消費者には、広告主が機能するサービスプロバイダーのリストが表示されます。
      1. 顧客は、Adobe Advertisingへのデータ販売をオプトアウトするチェックボックスをオンにします。

         このアクションは、指定された「[!UICONTROL CCPA Opt-out of sale]」セグメント内の消費者のCookie IDを取得し、アクティベートするピクセルをトリガーします。

>[!MORELIKETHIS]
>
>* [Adobe Advertisingのカリフォルニア州消費者プライバシー法に対するサポート：消費者の販売拒否サポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [約[!UICONTROL CCPA Opt-out-of-Sale]個のセグメントとレポート &#x200B;](ccpa-opt-out-about.md)
>* [消費者のオプトアウトに関するレポートを取得](ccpa-opt-out-segment-report-retrieve.md)
>* [&#x200B; カスタムセグメントを作成して実装](custom-segment-create.md)
>* [&#x200B; オーディエンス管理について](audience-about.md)
