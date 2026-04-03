---
title: リターゲティングピクセルの管理
description: 広告エクスペリエンスのターゲットとして使用するリターゲティングピクセルを作成して実装する方法について説明します。
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
TQID: https://experienceleague.adobe.com/Io8N6tbyhPOEWHPIYe2Zu2b4xTYXqgwp04geaBKTchg
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 936
ht-degree: 0%

---

# リターゲティングピクセルの管理

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

リターゲティングピクセルを作成し、ユーザーCookieやユニバーサル IDを使用して、広告主のランディングページやコンバージョンページへの訪問者を識別することができます。 ピクセルは、訪問者がページで実行した最新のイベントを追跡し、ページがその訪問者に対して追跡している特定の属性をキャプチャします。 ピクセルを作成したら、関連するweb ページに挿入するピクセルタグを生成して、訪問者のトラッキングを開始します。<!-- Note to self: surfer id=cookie or universal ID -->

その後、ピクセルを広告エクスペリエンス内の任意のクリエイティブのターゲットとして使用して、ピクセルに関連付けられたweb ページを以前に訪問したことがある特定の属性を持つユーザーにのみ広告を表示できます。 例えば、web ページでこれらの属性値が追跡されている場合、サイズが10の赤い靴を見た訪問者をターゲットにすることができます。<!-- better example? Make sure they match attribute examples below --> エクスペリエンスレベルのターゲットは、DSPのターゲティングオプションと組み合わせて適用されます。階層的なターゲティング動作は、DSPによって異なる場合があります。

リターゲティングプロファイルは180日間保存されます。

ピクセル例：

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative]は、Advertising DSPのユニバーサル IDのみをサポートしています。
>* また、Adobe Audience ManagerとAdobe Analyticsの1st パーティオーディエンスを、エクスペリエンスの[&#x200B; クリエイティブ目標](/help/creative/experiences/experience-settings-targeting.md)として使用することもできます。
>* Advertising DSP プレースメント内の広告としてエクスペリエンスを使用する場合、DSPで使用可能なすべてのオーディエンスにプレースメントをターゲティングできます。 また、[&#x200B; カスタムオーディエンスセグメントタグ &#x200B;](/help/dsp/audiences/custom-segment-create.md)を作成して、特定のランディングページに対するすべての訪問者を追跡し、それらのセグメントをプレースメントのクリエイティブターゲットとして使用することもできます。 Advertising DSPでは、プレースメントレベルのターゲティングの上に（代わりに）広告レベルのターゲティングを適用します。
>* 広告ターゲティングのトラッキングをオプトアウトしたweb サイト訪問者は、オーディエンスセグメントやリターゲティングプロファイルにもとづいてパーソナライズされたクリエイティブコンテンツを含む広告を受け取ることはできません。

## リターゲティングピクセルの作成

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**&#x200B;をクリックします。

1. データテーブルの上で「**[!UICONTROL Creative]**」をクリックし、> **[!UICONTROL Retargeting Pixel]**」を選択します。

1. [&#x200B; リターゲティングピクセル設定](#retargeting-pixel-settings)を指定します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. [広告主またはweb サイトの連絡先に提供するピクセルタグ &#x200B;](#retargeting-pixel-generate)を生成します。

   リターゲティングピクセルタグは、ページの最後のアクションである必要があります。<!-- verify here and below -->

   広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。

## リターゲティングピクセルの編集

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**&#x200B;をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Edit]**&#x200B;をクリックします。

1. [&#x200B; リターゲティングピクセル設定](#retargeting-pixel-settings)を編集します。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. [&#x200B; ピクセルタグ &#x200B;](#retargeting-pixel-generate)を生成して、広告主またはweb サイトの連絡先に提供し、元のタグを置き換えることができるようにします。

   リターゲティングピクセルタグは、ランディングページの最後のアクションである必要があります。

   広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。

## リターゲティングピクセルのタグを生成 {#retargeting-pixel-generate}

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**&#x200B;をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Generate Tag]**&#x200B;をクリックします。

1. **[!UICONTROL Copy to Clipboard]**&#x200B;をクリックして、タグをコンピューターのクリップボードにコピーし、そこからテキストをファイルに貼り付けて保存します。

1. ピクセルタグで、各「`<img src>`」を値に置き換えて、`<script src>`および`Insert <attribute>` セクションの各属性の値を指定します。 タグがユニバーサル IDをキャプチャする場合は、ID5 パートナーIDを指定します。

   属性を手動で追加する場合は、URL エンコーディングを含めます。

   例えば、「カテゴリ」、「カラー」および「サイズ」の属性を含め、ID5のユニバーサル IDをキャプチャする場合、ピクセルタグには次のパラメーターが含まれます：`&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--`と`&id5pid=--Insert ID5_PARTNER_ID--`。 サイズ 10の赤いサンダルを選択するユーザーをターゲットにするには、画像タグとスクリプトタグの両方のパラメーターを`&ut1=sandals&ut2=red&ut3=10`に変更し、スクリプトタグ（`&id5pid=0123456789`など）にID5 パートナーIDも入力します。

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. 完成したピクセルタグを、広告主またはweb サイトの連絡先に提供し、関連するランディングページのリストと共に挿入します。

   リターゲティングピクセルタグは、ランディングページの最後のアクションである必要があります。

   広告主のIT部門やその他のグループは、タグのデプロイメントをスケジュールする、または情報を得る必要がある場合があります。

## リターゲティングピクセルの削除

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Pixels]**&#x200B;をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

## ピクセル設定のリターゲティング {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** ピクセルの名前。 **注意：** ピクセルタグには、ピクセル名ではなくピクセル ID （`pxId=<ID>`）が含まれます。

**[!UICONTROL Advertiser]:** （既存のピクセルの読み取り専用） ピクセルが追跡される広告主。

**[!UICONTROL Attribute 1]:** ピクセルタグに含める属性（「SKU」、「カテゴリ」、「サイズ」、ページまたはページに表示される製品のその他の属性など）。 関連するweb ページに属性を挿入する前に、ピクセルタグで属性の値を指定します。

ピクセルに露出しているユーザーに広告エクスペリエンスをターゲティングする場合、ターゲティング設定は、クリエイターを表示するために存在する必要がある属性値を指定します。

**[!UICONTROL Attribute 2]**、**[!UICONTROL Attribute 3]**、**[!UICONTROL Attribute 4]**、**[!UICONTROL Attribute 5]:** （オプション）ピクセルタグに含める追加属性。 関連するweb ページに挿入する前に、ピクセルタグ内の各追加属性の値を指定します。

ピクセルに露出しているユーザーに広告エクスペリエンスをターゲティングする場合、ターゲティング設定は、クリエイターを表示するために存在する必要がある属性値を指定します。

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** （新しいピクセルのみ。オプション）追跡するピクセルタグのユニバーサル IDの種類：

* *[!UICONTROL ID5]:* ピクセルタグは[!DNL ID5] IDを追跡します。 ユニバーサル IDに配信されたインプレッションに対して、料金は発生しません。

* *[!UICONTROL Ramp ID]:* ピクセルタグは[!DNL Ramp IDs]を追跡します。 ユニバーサル IDに配信されたインプレッションに対して、料金は発生しません。

この機能を使用するには、新しいID タイプにユニバーサル IDを使用する前に、DSP アカウント内の他のユーザーがユニバーサル IDを使用するための利用条件に同意する必要があります。 マネージドサービス契約を締結しているお客様には、Adobeアカウントチームが同意を得て、組織の代わりに条件に同意します。 条件を読むには、**[!UICONTROL Terms of Service]**&#x200B;をクリックします。 条件に同意するには、条件の一番下までスクロールして「**[!UICONTROL Accept]**」をクリックします。

>[!MORELIKETHIS]
>
>* [&#x200B; ターゲット広告エクスペリエンス設定](/help/creative/experiences/experience-settings-targeting.md)
>* [広告体験について](/help/creative/experiences/experience-about.md)
