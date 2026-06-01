---
title: カスタムセグメントの作成と実装
description: カスタムセグメントを作成して実装し、広告に表示されるユーザーやweb ページにアクセスするユーザーを追跡する方法について説明します。
feature: DSP Segments
exl-id: 3190fd78-18d2-4da3-920b-d4171e693c03
TQID: https://experienceleague.adobe.com/Xemx2oExt-bNTgJPVkDaWfillRBAZAfOPQx1eJYxupw
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c2be0313-b3ae-45e0-b454-d20bf54b23f2
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: baec698f16aafc163adf2c4cfa76c92af7e1ad61
workflow-type: tm+mt
source-wordcount: 700
ht-degree: 0%

---

# カスタムセグメントの作成と実装

DSPのカスタムセグメントを作成して実装することで、独自の1st パーティオーディエンスデータを収集できます。 このセグメントを使用して、a） デスクトップおよびモバイルデバイスから広告に表示されたユーザー、およびb）特定のweb ページにアクセスしたユーザーを追跡できます。 後で、追加の広告を使用してセグメント内のユーザーをリターゲティングしたり、セグメント内のユーザーが追加の広告を受信するのを防ぐことができます。

>[!NOTE]
>
>Web サイトの消費者のオプトアウト要求からユーザーIDを追跡するには、カリフォルニア州消費者プライバシー法（CCPA）に従って、[CCPA オプトアウト アウト アウト販売セグメント &#x200B;](ccpa-opt-out-segment-create.md)を作成します。

## セグメントがID5を追跡するための前提条件

* ID5 IDに関連付けられたユーザーを追跡するセグメントを生成する前に、[!DNL ID5]と契約書に署名し、組織のパートナーIDを取得します。 手順については、Adobe アカウントチームにお問い合わせください。

* Adobe Analyticsで測定を行うには、次の操作が必要です。

   1. 実装 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/prerequisites.md)の前提条件をすべて完了し、[AMO IDとEF ID](/help/integrations/analytics/ids.md)がトラッキング URLに入力されていることを確認します。

   1. 次のパラメーターを、 [!DNL Analytics for Advertising][&#128279;](/help/integrations/analytics/javascript.md)に必要なJavaScript コードの前または中（最後のイベントサービスが初期化される前）にweb ページに追加します。

      `window.id5PartnerId=ID5_PartnerID;`

      例：

      ```
      <script src="https://www.everestjs.net/static/le/last-event-tag-latest.min.js">
      <script>
        window.id5PartnerId=ID5_PartnerID;
             if("undefined" != typeof AdCloudEvent)
                 AdCloudEvent('IMS ORG Id','rsid');
      </script>
      ```

      完全なタグ形式については、「[Format of JavaScript conversion tracking tags version 3](/help/search-social-commerce/tracking/format-conversion-tag-jsv3.md)」および「[Format of JavaScript conversion tracking tags version 2](/help/search-social-commerce/tracking/format-conversion-tag-jsv2.md)」を参照してください。

   1. 任意のブラウザーのデバッグツールを使用して、各呼び出しがドメイン `lasteventf-tm.everesttech.net`に対して開始され、暗号化されたID5 IDを値とするパラメーター`_les_id5`が含まれていることを確認します。

## カスタムセグメントの作成と実装

1. セグメントを作成します。

   1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL Segments]**&#x200B;をクリックします。

   1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

   1. 一意の&#x200B;**[!UICONTROL Segment Name]**&#x200B;を入力してください。

   1. **[!UICONTROL Segment Type]**&#x200B;の場合は、*[!UICONTROL Custom]*&#x200B;を選択します。

   1. ユーザーのCookieがセグメントに滞在する日数である&#x200B;**[!UICONTROL Lookback Window]**&#x200B;を入力します。

      デフォルトのウィンドウは45日です。 1から365までの値を入力します。

   1. **[!UICONTROL Advanced]**&#x200B;をクリックして詳細設定を展開し、セグメントタグが追跡するユーザーIDの種類を選択します。

      * [!UICONTROL Legacy]:

         * *[!UICONTROL Cookies]:* （既定値） セグメントタグはCookieを追跡します。

      * [!UICONTROL Universal IDs]:

         * *[!UICONTROL ID5]:* セグメントタグは[!DNL ID5]個のIDを追跡します。 ユニバーサル IDに配信されたインプレッションに対して、料金は発生しません。

        **[!UICONTROL Terms of Service]:** ユニバーサル IDを使用するための利用条件。 新しいID タイプにユニバーサル IDを使用する前に、DSP アカウント内の他のユーザーが条件に同意する必要があります。 マネージドサービス契約を締結しているお客様には、Adobeアカウントチームが同意を得て、組織の代わりに条件に同意します。 条件を読むには、**>**&#x200B;をクリックします。 条件に同意するには、条件の一番下までスクロールして「**[!UICONTROL Accept]**」をクリックします。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. 必要に応じて、タグをコピーして実装し、セグメントを追跡します。

   1. **[!UICONTROL Audiences]** > **[!UICONTROL Segments]**&#x200B;に戻ります。

   1. セグメント行の上にカーソルを置き、**[!UICONTROL Get Pixel]**&#x200B;をクリックします。

      * Web ページへのデスクトップおよびモバイル訪問者を追跡するには：

         1. 「[!UICONTROL Desktop or mobile websites]」というラベルが付いたページビューのトラッキングタグをコピーします。

         1. （[!DNL ID5] IDを追跡するセグメントのタグ）コピーしたタグで、`ID5_PARTNER_ID`を[!DNL ID5]が組織に割り当てたパートナーIDに置き換えます。

            例えば、ID5のパートナーIDが`abcde`で、生成されたセグメントタグが

            `<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=ID5_PARTNER_ID"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />`

            次に、`ID5_PARTNER_ID`をタグ内の`abcde`に置き換えて、次の情報を取得します。

            `<script src="https://playtime.tubemogul.com/ud/prod/universal_ids/segment.js?sid=012345&id5pid=abcde"></script><img src="https://rtd-tm.everesttech.net/upi/?sid=012345&cs=1" />`

            組織が[!DNL ID5]との契約書に署名したときに、パートナーIDを受け取りました。 パートナーIDがわからない場合は、Adobeアカウントチームにお問い合わせください。

            この手順は、デスクトップまたはモバイルデバイスで広告単位に公開されているユーザーの[!DNL ID5] IDをタグが追跡するために必要ではありません。

         1. デプロイメントのために、広告主またはweb サイトの連絡先にタグを提供します。

            広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。

      * デスクトップまたはモバイルデバイスで広告ユニットに公開されたユーザーを追跡するには：

         1. 「[!UICONTROL Desktop or mobile ads]」というラベルが付いたインプレッション追跡タグをコピーします。

         1. 関連する各広告の[!UICONTROL Pixel] タブ、または関連する各配置の[[!UICONTROL Tracking]設定の[!UICONTROL Event Pixels] セクション &#x200B;](/help/dsp/campaign-management/placements/placement-settings.md#placement-tracking)にタグを追加します。

トラッキングタグを実装したら、オーディエンスターゲットまたは除外のセグメントを任意のプレースメントに使用できます。

>[!TIP]
>
>ユーザーが追跡される際に、セグメントサイズを追跡します。

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンス管理について](audience-about.md)
>* [&#x200B; セグメント情報を編集](segment-edit.md)
>* [&#x200B; セグメントを削除](segment-delete.md)
>* [&#x200B; セグメントのトラッキングピクセルを表示](segment-view-pixels.md)
>* [&#x200B; セグメントの共有または共有を停止](segment-share.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
