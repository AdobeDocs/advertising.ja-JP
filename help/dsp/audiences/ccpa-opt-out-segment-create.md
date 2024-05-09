---
title: CCPA の販売オプトアウトセグメントの作成と実装
description: セグメントを作成および実装して、消費者の販売オプトアウトリクエストからユーザー ID を追跡する方法を説明します。
feature: CCPA, DSP Segments
exl-id: 0623c52e-02ea-4e06-bc54-8abb7a87765a
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 0%

---

# CCPA の販売オプトアウトセグメントの作成と実装

カリフォルニア消費者プライバシー法（CCPA）に従って、セグメントを作成し、web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡できます。 ユーザーは、CCPA の販売のオプトアウトセグメントに無期限に残ります。

セグメントピクセルタグが実装されると、Adobe Advertisingは、広告主に代わって ID のプールの収集を開始します。

>[!NOTE]
>
>* Adobe Experience Platform Privacy Service API を使用して CCPA の販売オプトアウトリクエストをAdobe Advertisingに通知する方法について詳しくは、以下を参照してください。 [https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html](https://experienceleague.adobe.com/docs/advertising/privacy/ccpa/ccpa-opt-out-of-sale.html).
>* CCPA の販売オプトアウトイベントのトラッキングに関連しない目的で web ページにアクセスするユーザーや、デスクトップ、モバイルおよび CTV デバイスから広告に公開されるユーザーをトラッキングするには、次を作成します [カスタムセグメント](/help/dsp/audiences/custom-segment-create.md).

1. セグメントを作成します。

   1. メインメニューで、 **オーディエンス / セグメント**.

   1. データ テーブルの上で、 **[!UICONTROL Create]**.

   1. 一意のを入力 **[!UICONTROL Segment Name]**.

      推奨されるセグメント名：「&lt;*広告主名*> - CCPA の販売のオプトアウト」（「Acme - CCPA の販売のオプトアウト」など）

   1. の場合 [!UICONTROL Segment Type]を選択 **[!UICONTROL CCPA Opt-out of sale]**.

   1. クリック **[!UICONTROL Save]**.

1. セグメントを追跡するピクセルタグをコピーして実装します。

   1. に戻る **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. セグメント行で、新しいセグメントの上にカーソルを置いてクリックします **[!UICONTROL Get pixel]**.

   1. 画像ピクセル（で始まる）をコピーします `<img src="https://rtd-tm.everesttech.net"`）を使用して、web ページへのデスクトップおよびモバイル訪問者のユーザー ID を収集します。

   1. 会社が CCPA の販売オプトアウトリクエストを追跡するために使用するメカニズム（同意管理プラットフォームの使用など）を使用して、デプロイメント用にタグを広告主または web サイトの連絡先に提供します。

      広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

      ピクセルが実装されると、Adobe Advertisingは広告主に代わって ID のプールの収集を開始します。

      実装の選択とロジックは広告主によって決まりますが、広告主がピクセルを実行する方法の例を次に示します。

      1. 消費者が広告主のホームページにアクセスします。
      1. 消費者が広告主の「CCPA の販売のオプトアウト」ボタンを見つけてクリックします。
      1. 消費者には、広告主が機能するサービスプロバイダーのリストが表示されます。
      1. 消費者はチェックボックスをオンにして、Adobe Advertisingへのデータの販売をオプトアウトします。

         このアクションにより、トリガーするピクセルと、指定された「」内での消費者の Cookie ID を収集するピクセルがトリガーされます[!UICONTROL CCPA Opt-out of sale]「セグメント。

>[!MORELIKETHIS]
>
>* [カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者オプトアウトサポート](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [について [!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポート](ccpa-opt-out-about.md)
>* [消費者の販売オプトアウトレポートの取得](ccpa-opt-out-segment-report-retrieve.md)
>* [カスタムセグメントの作成と実装](custom-segment-create.md)
>* [Audience Management について](audience-about.md)
