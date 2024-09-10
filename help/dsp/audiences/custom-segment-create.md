---
title: カスタムセグメントの作成と実装
description: カスタムセグメントを作成および実装して、広告にさらされたユーザーまたは web ページを訪問したユーザーを追跡する方法について説明します。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
source-git-commit: 3774da55139fd9f70162c931dd7708e8e258ad83
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 0%

---

# カスタムセグメントの作成と実装

カスタム DSP セグメントを作成して実装することで、独自のファーストパーティオーディエンスデータを収集できます。 セグメントを使用して、a） デスクトップやモバイルデバイスから広告にさらされたユーザー、および b）特定の web ページを訪問したユーザーを追跡できます。 後で、追加の広告を使用してセグメント内のユーザーを再ターゲットしたり、セグメント内のユーザーが追加の広告を受け取らないようにしたりできます。

>[!NOTE]
>
>Web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡するには、カリフォルニア州消費者プライバシー法（CCPA）に従って、[CCPA の販売オプトアウトセグメント ](ccpa-opt-out-segment-create.md) を作成します。

## セグメントで ID5 ID を追跡するための前提条件

*Beta機能*

* ID5 ID に関連付けられたユーザーを追跡するセグメントを生成する前に、[!DNL ID5] との契約書に署名し、組織のパートナー ID を取得します。 手順については、Adobeアカウントチームにお問い合わせください。

* Adobe Analyticsでの測定の場合、次の操作を行う必要があります。

   1. すべての [ 実装の前提条件  [!DNL Analytics for Advertising]](/help/integrations/analytics/prerequisites.md) を満たし、[AMO ID と EF ID](/help/integrations/analytics/ids.md) がトラッキング URL に入力されていることを確認します。

   1. 次のパラメーターを、[ に必要なJavaScript コードの前または中  [!DNL Analytics for Advertising]](/help/integrations/analytics/javascript.md)、最後のイベントサービスが初期化される前の任意の場所で、Web ページに追加します。

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

      完全なタグフォーマットについては、「[JavaScript コンバージョントラッキングタグバージョン 3 のフォーマット ](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)」および「[JavaScript コンバージョントラッキングタグバージョン 2 のフォーマット ](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)」を参照してください。

   1. 任意のブラウザーデバッグツールを使用して、各呼び出しがドメイン `lasteventf-tm.everesttech.net` に対して開始され、暗号化された ID5 ID を値として持つパラメーター `_les_id5` が含まれていることを確認します。

## カスタムセグメントの作成と実装

1. セグメントを作成します。

   1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL Segments]** をクリックします。

   1. データ テーブルの上にある [**[!UICONTROL Create]**] をクリックします。

   1. 一意の **[!UICONTROL Segment Name]** を入力します。

   1. **[!UICONTROL Segment Type]** に「*[!UICONTROL Custom]*」を選択します。

   1. ユーザーの cookie がセグメントに残る日数である「**[!UICONTROL Lookback Window]**」を入力します。

      デフォルトウィンドウは 45 日です。 1 から 365 までの値を入力します。

   1. 「**[!UICONTROL Advanced]**」をクリックして詳細設定を展開し、セグメントタグが追跡するユーザー識別子のタイプを選択します。

      * *[!UICONTROL Cookies]:* （デフォルト）セグメントタグは Cookie を追跡します。

      * [!UICONTROL Universal IDs (Beta)]:

         * *[!UICONTROL ID5]:* セグメントタグは [!DNL ID5] ID を追跡します。 ユニバーサル ID に配信されるインプレッションには料金は発生しません。

        **[!UICONTROL Terms of Service]:** ユニバーサル ID を使用するためのサービス利用契約。 ユニバーサル ID を新しい ID タイプに使用するには、DSP アカウントの別のユーザーが条件に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、「**>**」をクリックします。 条件に同意するには、条件の下部までスクロールし、「**[!UICONTROL Accept]**」をクリックします。

   1. 「**[!UICONTROL Save]**」をクリックします。

1. 必要に応じて、タグをコピーして実装し、セグメントを追跡します。

   1. **[!UICONTROL Audiences]**/**[!UICONTROL Segments]** に戻ります。

   1. セグメント行の上にカーソルを置き、**[!UICONTROL Get Pixel]** をクリックします。

      * Web ページへのデスクトップおよびモバイル訪問者を追跡するには：

         1. 「[!UICONTROL Desktop or mobile websites]」というラベルの付いたページビュートラッキングタグをコピーします。

         1. （[!DNL ID5] ID を追跡するセグメントのタグ）コピーしたタグ内で、`ID5_PARTNER_ID` を組織に割り当てられ [!DNL ID5] パートナー ID に置き換えます。

            例えば、ID5 のパートナー ID が `abcde` で、生成されたセグメントタグがである場合

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            次に、`ID5_PARTNER_ID` をタグ内の `abcde` に置き換えて、次の情報を取得します。

            ```<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />```

            組織が [!DNL ID5] との契約に署名したときに、パートナー ID を受け取りました。 パートナー ID がわからない場合は、Adobeアカウントチームにお問い合わせください。

            この手順は、デスクトップまたはモバイルデバイスで広告ユニットに公開されたユーザーの [!DNL ID5] ID をタグで追跡する場合には必要ありません。

         1. デプロイメント用に、タグを広告主または web サイトの連絡先に提供します。

            広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

      * デスクトップまたはモバイルデバイスで広告ユニットに公開されたユーザーを追跡するには：

         1. 「[!UICONTROL Desktop or mobile ads]」というラベルの付いたインプレッショントラッキングタグをコピーします。

         1. タグを、関連する各広告の「[!UICONTROL Pixel]」タブ、または関連する各プレースメントの [[!UICONTROL Tracking] 設定の「[!UICONTROL Event Pixels]」セクションに追加 ](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking) ます。

トラッキングタグが実装されると、任意のプレースメントに対してオーディエンスターゲットまたは除外のセグメントを使用できます。

>[!TIP]
>
>ユーザーが追跡されるたびに、セグメントサイズを追跡します。

>[!MORELIKETHIS]
>
>* [Audience Management について ](audience-about.md)
>* [ セグメント情報の編集 ](segment-edit.md)
>* [ セグメントの削除 ](segment-delete.md)
>* [ セグメントのトラッキングピクセルの表示 ](segment-view-pixels.md)
>* [ セグメントの共有または共有の停止 ](segment-share.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントの作成と実装 ](ccpa-opt-out-segment-create.md)
>* [ 再利用可能なオーディエンスを作成 ](reusable-audience-create.md)
>* [ 利用可能なサードパーティデータプロバイダー ](third-party-data-providers.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
