---
title: カスタムセグメントの作成と実装
description: カスタムセグメントを作成および実装して、広告にさらされたユーザーまたは web ページを訪問したユーザーを追跡する方法について説明します。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 2fe54fbcd9711e714246f074ede086910b538b80
workflow-type: tm+mt
source-wordcount: '671'
ht-degree: 0%

---

# カスタムセグメントの作成と実装

カスタム DSP セグメントを作成して実装することで、独自のファーストパーティオーディエンスデータを収集できます。 セグメントを使用して、a） デスクトップやモバイルデバイスから広告にさらされたユーザー、および b）特定の web ページを訪問したユーザーを追跡できます。 後で、追加の広告を使用してセグメント内のユーザーを再ターゲットしたり、セグメント内のユーザーが追加の広告を受け取らないようにしたりできます。

>[!NOTE]
>
>Web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡するには、カリフォルニア州消費者プライバシー法（CCPA）に従って、 [CCPA の販売オプトアウトセグメント](ccpa-opt-out-segment-create.md).

## セグメントで ID5 ID を追跡するための前提条件

*ベータ版機能*

* ID5 ID に関連付けられたユーザーを追跡するセグメントを生成する前に、と契約書に署名します。 [!DNL ID5] 組織のパートナー ID を取得します。 手順については、Adobeアカウントチームにお問い合わせください。

* Adobe Analyticsでの測定の場合、次の操作を行う必要があります。

   1. すべて完了 [実装の前提条件 [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md)を実行し、必ずを [AMO ID と EF ID](/help/integrations/analytics/ids.md) はトラッキング URL に入力されています。

   1. Web ページの前または内に、次のパラメーターを追加します [に必要な JavaScript コード [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)  – 最後のイベント サービスが初期化される前の任意の場所。

      ```window.id5PartnerId=Your_ID5_PartnerID;```

      例：

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=Your_ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

   1. 任意のブラウザーデバッグツールを使用して、各呼び出しがドメインに対して開始されていることを確認します `lasteventf-tm.everesttech.net` およびは、パラメーターを含みます `_les_id5` 値として暗号化された ID5 ID を使用します。

## カスタムセグメントの作成と実装

1. セグメントを作成します。

   1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. データ テーブルの上で、 **[!UICONTROL Create]**.

   1. 一意のを入力 **[!UICONTROL Segment Name]**.

   1. の場合 **[!UICONTROL Segment Type]**&#x200B;を選択 *[!UICONTROL Custom]*.

   1. を入力 **[!UICONTROL Lookback Window]**：ユーザーの cookie がセグメントに残る日数です。

      デフォルトウィンドウは 45 日です。 1 から 365 までの値を入力します。

   1. クリック **[!UICONTROL Advanced]** 詳細設定を展開して、セグメントタグが追跡するユーザー識別子のタイプを選択するには、次の手順を実行します。

      * *[!UICONTROL Cookies]:* （デフォルト）セグメントタグは cookie を追跡します。

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* セグメントタグが追跡する [!DNL ID5] ID。 ユニバーサル ID に配信されるインプレッションには料金は発生しません。

        **[!UICONTROL Terms of Service]:** ユニバーサル ID を使用するためのサービス利用規約。 ユニバーサル ID を新しい ID タイプに使用するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、 **>**. 条件に同意するには、条件の下部までスクロールし、をクリックします **[!UICONTROL Accept]**.

   1. クリック **[!UICONTROL Save]**.

1. 必要に応じて、タグをコピーして実装し、セグメントを追跡します。

   1. に戻る **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**.

   1. セグメント行の上にカーソルを置き、クリックします **[!UICONTROL Get Pixel]**.

      * Web ページへのデスクトップおよびモバイル訪問者を追跡するには：

         1. 「」というラベルの付いたページビュートラッキングタグをコピーします[!UICONTROL Desktop or mobile websites].」と入力します。

         1. （追跡するセグメントのタグ） [!DNL ID5] ID）コピーしたタグで、 `ID5_PARTNER_ID` パートナー ID が [!DNL ID5] を組織に割り当てました。

            例えば、ID5 のパートナー ID がの場合 `abcde` 生成されるセグメントタグはです。

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            その後、を置換 `ID5_PARTNER_ID` （を使用） `abcde` タグ内で次の情報を取得できます。

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            組織がと契約を締結したときに、パートナー ID を受け取りました [!DNL ID5]. パートナー ID がわからない場合は、Adobeアカウントチームにお問い合わせください。

            この手順は、タグでトラッキングする必要はありません [!DNL ID5] デスクトップまたはモバイルデバイスで広告ユニットに公開されるユーザーの ID。

         1. デプロイメント用に、タグを広告主または web サイトの連絡先に提供します。

            広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

      * デスクトップまたはモバイルデバイスで広告ユニットに公開されたユーザーを追跡するには：

         1. 「」というラベルの付いたインプレッショントラッキングタグをコピーします[!UICONTROL Desktop or mobile ads].」と入力します。

         1. タグをのどちらかに追加します。 [!UICONTROL Pixel] 関連する各広告またはに対するタブ [!UICONTROL Event Pixels] の節 [[!UICONTROL Tracking] 関連するプレースメントごとの設定](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking).

トラッキングタグが実装されると、任意のプレースメントに対してオーディエンスターゲットまたは除外のセグメントを使用できます。

>[!TIP]
>
>ユーザーが追跡されるたびに、セグメントサイズを追跡します。

>[!MORELIKETHIS]
>
>* [Audience Management について](audience-about.md)
>* [セグメント情報の編集](segment-edit.md)
>* [セグメントの削除](segment-delete.md)
>* [セグメントのトラッキングピクセルの表示](segment-view-pixels.md)
>* [セグメントの共有または共有の停止](segment-share.md)
>* [の作成と実装 [!UICONTROL CCPA Opt-Out-of-Sale] セグメント](ccpa-opt-out-segment-create.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [利用可能なサードパーティデータプロバイダー](third-party-data-providers.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
