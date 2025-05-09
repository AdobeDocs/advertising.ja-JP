---
title: Adobe Advertisingによる California Consumer Privacy Act &#58; Consumer Opt-Out-of-Sale サポートのサポート
description: 消費者の販売オプトアウトリクエストをキャプチャするためのサポートについて説明します。
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: 26a4451fb09f2a42ac60ba123ddf0cf38323312d
workflow-type: tm+mt
source-wordcount: '996'
ht-degree: 0%

---

# カリフォルニア州消費者プライバシー法のAdobe Advertising サポート：消費者の販売オプトアウトサポート

*Adobe Advertising Demand Side Platform（DSP）の場合*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、法務担当者にお問い合わせください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の居住者に個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスを行う特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、データにアクセスする権利およびデータを削除する権利、ならびに個人情報を第三者に「販売」する特定の活動をオプトアウトする権利を提供します。

お客様は会社として、Adobe Experience Cloudが処理および保存するお客様の代わりになる個人情報を決定します。

Adobe Advertisingは、お客様のサービスプロバイダーとして、お客様のAdobe Advertisingの製品およびサービスの使用に適用される、CCPA におけるお客様の義務を履行するためのサポートを提供します。これには、お客様の個人情報へのアクセスおよび消去のリクエストや、個人情報の販売をオプトアウトするためのリクエストの管理が含まれます。

このドキュメントでは、Adobe Advertising Demand Side Platform（DSP）が、サービスプロバイダーとして、CCPA によって定義される各用語において、「個人情報」の「販売」のオプトアウトに対する消費者の権利をどのようにサポートするかについて説明します。 Adobe Advertisingに販売のオプトアウトリクエストを通知する方法と、組織の販売のオプトアウトリクエストに関するレポートを取得する方法について説明します。

[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、および [!DNL Advertising DCO] が消費者の個人情報へのアクセスおよび削除権をどのようにサポートするかについて詳しくは、[Adobe Advertising消費者プライバシー法のカリフォルニア州サポート（消費者のデータへのアクセスおよび削除のサポート ](/help/privacy/ccpa/ccpa-access-delete.md) を参照してください。

CCPA のAdobe プライバシーサービスについて詳しくは、[Adobe プライバシーセンター ](https://www.adobe.com/privacy/ccpa.html) を参照してください。

## Adobe Advertisingへの消費者の販売オプトアウトリクエストの送信

次のいずれかを使用して、消費者の販売のオプトアウトリクエストを伝えることができます。

* Advertising DSPで作成された CCPA の販売オプトアウトセグメント
* ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API

### 方法 1:Advertising DSPの [!UICONTROL CCPA Opt-Out-of-Sale] セグメントを使用して、CCPA の販売オプトアウトリクエストを伝える

>[!NOTE]
>
>ユーザーは、CCPA の販売のオプトアウトセグメントに無期限に残ります。

1. Advertising DSP （[https://advertising.adobe.com/](https://advertising.adobe.com/)）の広告主のアカウントにサインインします。

1. [CCPA の販売オプトアウトセグメントを作成し、セグメントピクセルを実装してオプトアウトリクエストをキャプチャします ](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法 2:Adobe Experience Platform Privacy Service API を使用して CCPA の販売のオプトアウトリクエストを伝える

*Adobe Experience Cloud組織 ID のみを割り当てられた広告主*

1. JavaScript ライブラリをデプロイして、顧客の cookie を取得します。 同じライブラリ `AdobePrivacy.js` は、すべてのAdobe Experience Cloud ソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience Cloud ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   ライブラリは、会社のプライバシーポータルなど、顧客が販売のオプトアウトリクエストを送信できる Web ページにデプロイする必要があります。 ライブラリは、Adobe Cookie （名前空間 ID:`gsurferID`）を取得するのに役立ち、Adobe Experience Platform Privacy Service API 経由での販売のオプトアウトリクエストの一部としてこれらの ID を送信できます。

1. Experience Cloud組織 ID を特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列の後に「@AdobeOrg」が付いたものです。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは社内のAdobe システム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかわからない場合は、Adobe アカウントチームにお問い合わせください。 `imsOrgID` 名前空間を使用して Privacy API にリクエストを送信するには、組織 ID が必要です。

   >[!IMPORTANT]
   >
   >会社のAdobe Advertising担当者に問い合わせて、組織のすべてのAdobe Advertising アカウント（[!DNL DSP] アカウントまたは広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative] アカウントまたは [!DNL DCO] アカウントを含む）がExperience Cloudの組織 ID にリンクされていることを確認します。

1. Adobe Experience Platform Privacy Service API を使用して、コンシューマーに代わってAdobe Advertisingに [ 販売のオプトアウトリクエストを送信 ](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) したり、既存のリクエストのステータスを確認したりできます。

   販売のオプトアウトリクエストの例については、以下の付録を参照してください。

   >[!NOTE]
   >
   >ビジネスに複数のExperience Cloud組織 ID がある場合は、それぞれに個別の API リクエストを送信する必要があります。 ただし、サブソリューションごとに 1 つのアカウントを使用して、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO]）に対して 1 つの API リクエストを行うことができます。

これらの手順はすべて、Adobe Advertisingからのサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して行う必要のあるこれらのタスクやその他の関連タスクの詳細、および必要な項目の場所については、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html) を参照してください。

## 販売のオプトアウトリクエストを送信した消費者のレポートを取得します

Adobe Advertisingは、アカウントの販売オプトアウトリクエスト用に顧客が送信した ID の月間レポートを生成します。 各レポートは、タブ区切りのテキストファイルとして、GZIP 形式に圧縮して利用できます。 データは、Advertising DSPで作成された CCPA の販売のオプトアウトセグメントと、Privacy Service API を介して行われた送信を使用してキャプチャされたリクエストを統合します。 CCPA の販売オプトアウトセグメントで取得されたユーザー ID は、セグメント別および広告主別に識別されます。 レポートは、前月の各月の最初に生成されます。 例えば、6 月の月次ユーザーリストは 7 月 1 日に利用できます。

過去 3 か月間に作成された月次レポートへのリンクを、Advertising DSP内から、またはAdvertising DSP [!DNL Trafficking API] を使用して取得できます。 各リンクは 7 日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

### 方法 1:Advertising DSP内の消費者の販売オプトアウトレポートの取得

1. Advertising DSP （[https://advertising.adobe.com/](https://advertising.adobe.com/)）の広告主のアカウントにサインインします。

1. [ レポートの取得 ](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法 2:Advertising DSP [!DNL Trafficking API] を使用した消費者の販売オプトアウトレポートの取得

この機能は、[!DNL Trafficking API] を使用する組織が使用できます。 詳しくは、[!DNL Trafficking API] のドキュメントを参照してください。<!-- Add link to API doc once it's published. -->

組織が [!DNL Trafficking API] を使用していないが、詳細について知りたい場合は、Adobe アカウントチームにお問い合わせください。

## 付録：Privacy Service API ユーザー [!UICONTROL CCPA Opt-Out-of-Sale] リクエストの例

```
curl -X POST \
  https://platform.adobe.io/data/privacy/gdpr/ \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'Content-Type: application/json' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -d '{
    "companyContexts": [
      {
        "namespace": "imsOrgID",
        "value": "{IMS_ORG}"
      }
    ],
    "users": [
      {
        "key": "DavidSmith",
        "action": ["opt-out-of-sale"],
        "userIDs": [
          {
            "namespace": "email",
            "value": "dsmith@acme.com",
            "type": "standard"
          },
          {
            "namespace": "AdCloud",
            "type": "standard",
            "value":  "Wqersioejr-wdg",
          }
    ],
    "include": ["adCloud"],
    "regulation": "ccpa"
}'
```

ここで、[Privacy Service API 仕様に従って ](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix):

* `"namespace": "AdCloud"` は `AdCloud` cookie 領域を示し、対応する値は `AdobePrivacy.js` から取得された顧客の cookie ID です
* `"include": ["adCloud"]` は、リクエストが商品Adobe Advertisingに適用されることを示します
