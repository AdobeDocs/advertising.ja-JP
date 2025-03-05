---
title: リターゲティングピクセルの管理
description: 広告エクスペリエンスのターゲットとして使用するリターゲティングピクセルを作成および実装する方法について説明します。
feature: Creative Pixels
exl-id: dcd13c5a-315d-4380-99f9-6dbab3e1e1be
source-git-commit: e966058f5fe3fe9eb039f74bda8ea950f717e123
workflow-type: tm+mt
source-wordcount: '926'
ht-degree: 0%

---

# リターゲティングピクセルの管理

*クローズドベータ版*

<!-- Note to self: These aren't segments -- we don't create a pool of users. -->

リターゲティングピクセルを作成し、ユーザー Cookie またはユニバーサル ID を使用して広告主のランディングページまたはコンバージョンページへの訪問者を識別し、ページが訪問者に対して追跡している特定の属性を取得できます。 ピクセルは、訪問者がページで実行した最新のイベントを追跡します。 ピクセルを作成したら、関連する web ページに挿入するピクセルタグを生成して、訪問者のトラッキングを開始できます。<!-- Note to self: surfer id=cookie or universal ID -->

その後、ピクセルを広告エクスペリエンス内のすべてのクリエイティブのターゲットとして使用し、ピクセルに関連付けられた web ページに以前にアクセスした指定の属性を持つユーザーにのみ広告を表示できます。 例えば、web ページでこれらの属性値を追跡している場合、サイズ 10 の赤い靴を見ている訪問者をターゲットに設定できます。<!-- better example? Make sure they match attribute examples below -->

リターゲティングプロファイルは 180 日間保存されます。

ピクセルの例：

```
<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--Insert ID5_PARTNER_ID--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--Insert Color--&ut2=--Insert Size--"></script>
```

>[!NOTE]
>
> * [!DNL Creative] は現在、Advertising DSPのユニバーサル ID のみをサポートしています。 今後のリリースでは、サードパーティ DSP 用のユニバーサル ID がサポートされる予定です。<!-- Clarify this and reword as needed  -->
>* また、Adobe Audience ManagerとAdobe Analyticsのファーストパーティオーディエンスを [ エクスペリエンスのクリエイティブターゲット ](/help/creative/experiences/experience-settings-targeting.md) として使用することもできます。
>* Advertising DSP プレースメント内で広告としてエクスペリエンスを使用する場合、DSPで使用可能なすべてのオーディエンスをターゲットに配置できます。 また、[ カスタムオーディエンスセグメントタグを作成 ](/help/dsp/audiences/custom-segment-create.md) して、特定のランディングページへのすべての訪問者をトラッキングし、それらのセグメントをプレースメントのクリエイティブターゲットとして使用することもできます。
>* 広告ターゲティングのトラッキングをオプトアウトした web サイト訪問者は、オーディエンスセグメントまたはリターゲティングプロファイルに基づいてパーソナライズされたクリエイティブコンテンツを含む広告を受信しません。

## リターゲティングピクセルの作成

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Pixels]** をクリックします。

1. データ テーブルの上の [**[!UICONTROL Creative]**] をクリックし、[> **[!UICONTROL Retargeting Pixel]**] を選択します。

1. [ リターゲティングピクセル設定 ](#retargeting-pixel-settings) を指定します。

1. 「**[!UICONTROL Save]**」をクリックします。

1. [ ピクセルタグを生成 ](#retargeting-pixel-generate) して、広告主または web サイトの担当者に提供します。

   リターゲティングピクセルタグは、ページの最後のアクションである必要があります。<!-- verify here and below -->

   広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

## リターゲティングピクセルの編集

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Pixels]** をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Edit]** をクリックします。

1. [ リターゲティングピクセル設定 ](#retargeting-pixel-settings) を編集します。

1. 「**[!UICONTROL Save]**」をクリックします。

1. [ ピクセルタグを生成 ](#retargeting-pixel-generate) して、元のタグを置き換えられるように、広告主や web サイトの担当者に提供します。

   リターゲティングピクセルタグは、ランディングページの最後のアクションである必要があります。

   広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

## リターゲティングピクセルのタグの生成 {#retargeting-pixel-generate}

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Pixels]** をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Generate Tag]** をクリックします。

1. **[!UICONTROL Copy to Clipboard]** をクリックして、タグをコンピューターのクリップボードにコピーします。このクリップボードから、テキストをファイルに貼り付けて保存できます。

1. pixel タグで、各「`Insert <attribute>`」を値に置き換えて、「`<img src>`」セクションと「`<script src>`」セクションの両方で各アトリビュートの値を指定します。 タグがユニバーサル ID をキャプチャする場合は、ID5 パートナー ID を指定します。

   属性を手動で追加する場合は、URL エンコーディングを含める必要があります。

   例えば、属性「category」、「color」および「size」を含み、ID5 のユニバーサル ID を取り込んだ場合、ピクセルタグには次のパラメーターが含まれます。`&ut1=--Insert category--&ut2=--Insert color--&ut3=--Insert size--` および `&id5pid=--Insert ID5_PARTNER_ID--`。 例えば、サイズ 10 の赤いサンダルを選択するユーザーをターゲットにするには、画像タグとスクリプトタグの両方のパラメーターを `&ut1=sandals&ut2=red&ut3=10` に変更し、スクリプトタグに ID5 のパートナー ID （`&id5pid=0123456789` など）を入力します。

   `<img src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--" />  <script src="https://creative-assets-uat.efrontier.com/creative/scripts/rt.js?advId=141731&cro=F&id5Consent=T&id5pid=--0123456789--&lrConsent=T&pxId=oGwrDCSZRWu5ZQKSEy8Y&ut1=--sandals--&ut2=--red--&ut3=--10--"></script>`

1. 完成したピクセルタグを、関連するランディングページのリストと共に、広告主または web サイトの連絡先に提供します。

   リターゲティングピクセルタグは、ランディングページの最後のアクションである必要があります。

   広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

## リターゲティングピクセルの削除

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Creative Pixels]** をクリックします。

1. ピクセル名の上にカーソルを置き、**[!UICONTROL Delete]** をクリックします。

1. 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

## リターゲティングピクセル設定 {#retargeting-pixel-settings}

**[!UICONTROL Pixel Name]:** ピクセルの名前。 **注意：** ピクセルタグには、ピクセル名ではなくピクセル ID （`pxId=<ID>`）が含まれます。

**[!UICONTROL Advertiser]:** （既存のピクセルの場合は読み取り専用）ピクセルがトラッキングされる広告主。

**[!UICONTROL Attribute 1]:** 「SKU」、「カテゴリ」、「サイズ」など、ページまたはページに表示される製品のピクセルタグに含める属性。 関連する web ページに挿入する前に、ピクセルタグで属性の値を指定します。

ピクセルに公開されたユーザーに対して広告エクスペリエンスをターゲット設定する場合、クリエイティブを表示するために存在する必要がある属性値をターゲット設定で指定します。

**[!UICONTROL Attribute 2]**、**[!UICONTROL Attribute 3]**、**[!UICONTROL Attribute 4]**、**[!UICONTROL Attribute 5]:** （任意） pixel タグに含める追加の属性。 関連する web ページに挿入する前に、ピクセルタグ内の各追加属性の値を指定します。

ピクセルに公開されたユーザーに対して広告エクスペリエンスをターゲット設定する場合、クリエイティブを表示するために存在する必要がある属性値をターゲット設定で指定します。

**[!UICONTROL Advanced]** > **[!UICONTROL Universal IDs]:** （Beta機能、新しいピクセルのみ、オプション）トラッキングするピクセルタグのユニバーサル ID のタイプ：

* *[!UICONTROL ID5]:* ピクセルタグは [!DNL ID5] ID を追跡します。 ユニバーサル ID に配信されるインプレッションには料金は発生しません。

* *[!UICONTROL Ramp ID]:* ピクセルタグは [!DNL Ramp IDs] を追跡します。 ユニバーサル ID に配信されるインプレッションには料金は発生しません。

この機能を使用するには、ユニバーサル ID を新しい ID タイプに使用する前に、DSP アカウントの別のユーザーがユニバーサル ID 使用に関するサービス利用規約に 1 回同意する必要があります。 マネージドサービス契約を締結しているお客様の場合、Adobeアカウントチームがお客様の同意を得て、組織に代わって条項に同意します。 用語を読むには、[**[!UICONTROL Terms of Service]**] をクリックします。 条件に同意するには、条件の下部までスクロールし、「**[!UICONTROL Accept]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ ターゲット広告エクスペリエンス設定 ](/help/creative/experiences/experience-settings-targeting.md)
>* [ 広告エクスペリエンスについて ](/help/creative/experiences/experience-about.md)
