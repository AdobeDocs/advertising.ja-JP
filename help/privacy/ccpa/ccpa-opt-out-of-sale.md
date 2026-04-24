---
title: Adobe Advertisingによるカリフォルニア州消費者プライバシー法のサポート &#58；消費者による購入拒否のサポート
description: 消費者のオプトアウトの要求をキャプチャするためのサポートについて説明します。
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
TQID: https://experienceleague.adobe.com/16JkyKVsVoBIGKEbhEIH7HWZ-H-XkjBad7yq9-NhY3s
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: 1101
ht-degree: 0%

---

# Adobe Advertisingのカリフォルニア州消費者プライバシー法のサポート：消費者の購入拒否のサポート

*Adobe Advertising Demand Side Platform （DSP）*&#x200B;の場合

>[!IMPORTANT]
>
>本文書の内容は、法律上の助言ではなく、法律上の助言に代わるものではありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士にご相談ください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020年1月1日に施行される、カリフォルニア州の新しいプライバシー法です。 CCPAは、カリフォルニア在住の方の個人情報に関する新たな権利を提供し、カリフォルニア州で事業を行う特定の企業に対してデータ保護の責任を課します。 CCPAは、消費者が自身のデータにアクセスして削除する権利と、個人情報を第三者に「販売」すると認定された特定の活動をオプトアウトする権利を提供します。

企業は、Adobe CX Enterpriseが処理および保存する個人データを自身の代わりに決定します。

お客様のサービスプロバイダーとして、Adobe Advertisingは、個人情報へのアクセスおよび削除に関する消費者のリクエストの管理、個人情報の販売をオプトアウトする消費者のリクエストの管理など、Adobe Advertisingの製品およびサービスの使用に適用されるCCPAに基づく義務を果たすためのビジネスのサポートを提供します。

このドキュメントでは、Adobe Advertising Demand Side Platform（DSP）が、CCPAによって定義される「個人情報」の「販売」をオプトアウトする消費者の権利をサービスプロバイダーとしてサポートする方法について説明します。 このレポートには、販売停止リクエストをAdobe Advertisingに送信する方法と、組織の販売停止リクエストのレポートを取得する方法に関する情報が含まれています。

[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、および[!DNL Advertising DCO]が消費者の個人情報へのアクセスおよび削除権をどのようにサポートしているかについては、[Adobe Advertising消費者プライバシー法のサポート：消費者データへのアクセスおよび削除のサポート &#x200B;](/help/privacy/ccpa/ccpa-access-delete.md)を参照してください。

CCPA向けAdobe Privacy Servicesについて詳しくは、[Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## 消費者のオプトアウトのリクエストをAdobe Advertisingに伝える

次のいずれかを使用して、消費者のオプトアウトオブセールのリクエストを伝えることができます。

* Advertising DSPで作成されたCCPAのオプトアウトオブセールセグメント
* Adobe Experience Platform Privacy Service APIでは

### 方法1: Advertising DSPの[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを使用して、CCPAのオプトアウトのリクエストを伝える

>[!NOTE]
>
>ユーザーはCCPAの販売不可セグメントに無期限で残ります。

1. Advertising DSPの広告主アカウント（[https://advertising.adobe.com/](https://advertising.adobe.com/)）にログインします。

1. [CCPA オプトアウトのセールスセグメントを作成し、セグメントピクセルを実装してオプトアウト要求を取得します](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。

### 方法2:Adobe Experience Platform Privacy Service APIを使用してCCPAのオプトアウトオブセールリクエストを送信する

*広告主がAdobe CX Enterprise組織IDのみを割り当てました*

1. JavaScript ライブラリをデプロイして、顧客のCookieを取得します。 同じライブラリ `AdobePrivacy.js`が、すべてのAdobe CX Enterprise ソリューションに使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe CX Enterprise ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   顧客がオプトアウト要求（プライバシーポータルなど）を送信できるweb ページにライブラリをデプロイする必要があります。 ライブラリは、Adobe Cookie （名前空間ID: `gsurferID`）を取得するのに役立ちます。これにより、Adobe Experience Platform Privacy Service APIを介したオプトアウトオブセールリクエストの一部として、これらのIDを送信できます。

1. CX Enterprise組織IDを特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   CX Enterprise organization IDは、「@AdobeOrg」が付いた24文字の英数字の文字列です。 ほとんどのCX Enterpriseのお客様には、組織IDが割り当てられています。 マーケティング部門または社内のAdobeシステム管理者が組織IDを認識していない場合、または組織IDがプロビジョニングされているかどうかわからない場合は、Adobeアカウントチームにお問い合わせください。 `imsOrgID`名前空間を使用してPrivacy APIにリクエストを送信するには、組織IDが必要です。

   >[!IMPORTANT]
   >
   >お客様の組織のすべてのAdobe Advertising アカウント（アカウント [!DNL DSP]または広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative]または[!DNL DCO] アカウントを含む）がCX Enterpriseの組織IDにリンクされていることを確認するには、会社のAdobe Advertising担当者にお問い合わせください。

1. Adobe Experience Platform Privacy Service APIを使用して、消費者に代わってAdobe Advertisingにオプトアウトリクエスト [&#128279;](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html)を送信し、既存のリクエストのステータスを確認します。

   オプトアウトオブセールリクエストの例については、以下の付録を参照してください。

   >[!NOTE]
   >
   >ビジネスに複数のCX Enterprise組織IDがある場合は、それぞれに個別のAPI リクエストを送信する必要があります。 ただし、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、および[!DNL DCO]）に1つのAPI リクエストを、サブソリューションごとに1つのアカウントで行うことができます。

Adobe Advertisingのサポートを受けるには、これらすべての手順が必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクと関連タスク、および必要な項目の検索場所について詳しくは、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)を参照してください。

## オプトアウト要求を送信した消費者のレポートの取得

Adobe Advertisingは、お客様がアカウントのオプトアウト要求を送信したIDの月次レポートを生成します。 各レポートは、GZIP形式に圧縮されたタブ区切りのテキストファイルとして使用できます。 このデータは、Advertising DSPで作成されたCCPAのオプトアウトオブセールセグメントと、Privacy Service APIを介して送信された送信を使用してキャプチャされたリクエストを統合します。 CCPAのオプトアウトオブセールスセグメントで取得されたユーザーIDは、セグメントおよび広告主によって識別されます。 レポートは、前月の各月の最初に生成されます。 例えば、6月の月間ユーザーリストは7月1日に利用できます。

Advertising DSP内またはAdvertising DSP [!DNL Trafficking API]を使用して、過去3か月間に作成された月次レポートへのリンクを取得できます。 各リンクは7日間有効ですが、顧客が取得するたびに更新されます。

### 方法1:Advertising DSP内で消費者のオプトアウトオブセールレポートを取得する

1. Advertising DSPの広告主アカウント（[https://advertising.adobe.com/](https://advertising.adobe.com/)）にログインします。

1. [&#x200B; レポートを取得](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md)。

### 方法2: Advertising DSP [!DNL Trafficking API]を使用してコンシューマーの販売拒否レポートを取得する

この機能は、[!DNL Trafficking API]を使用する組織で使用できます。 詳しくは、[!DNL Trafficking API]のドキュメントを参照してください。<!-- Add link to API doc once it's published. -->

お客様の組織が[!DNL Trafficking API]を使用していないが、詳細については、Adobe アカウント チームにお問い合わせください。

## 付録：Privacy Service API ユーザーに対する[!UICONTROL CCPA Opt-Out-of-Sale] リクエストの例

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

ここで、[Privacy Service API仕様](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix)に従って、

* `"namespace": "AdCloud"`は`AdCloud` Cookie スペースを示し、対応する値は`AdobePrivacy.js`から取得した顧客のCookie IDです
* `"include": ["adCloud"]`は、リクエストが商品Adobe Advertisingに適用されることを示します
