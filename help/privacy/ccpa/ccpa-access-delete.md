---
title: Adobe Advertising support for the California Consumer Privacy Act &#58; Consumer data access and delete support
description: Learn about the supported data request types, required setup and field values, and examples of API access requests using legacy product IDs and returned data fields.
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
TQID: https://experienceleague.adobe.com/g7Klc5k3qEPYDKIbTmsQcnklUPVvbN6qqhXaHCHvn3A
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
source-wordcount: 1111
ht-degree: 0%

---

# Adobe Advertising support for the California Consumer Privacy Act: Consumer data access and delete support

*For [!DNL Adobe Advertising Search, Social, & Commerce]; Adobe Advertising DSP; Adobe Advertising Creative; and Adobe Advertising DCO*

>[!IMPORTANT]
>
>本文書の内容は、法律上の助言ではなく、法律上の助言に代わるものではありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士にご相談ください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020年1月1日に施行される、カリフォルニア州の新しいプライバシー法です。 CCPAは、カリフォルニア在住の方の個人情報に関する新たな権利を提供し、カリフォルニア州で事業を行う特定の企業に対してデータ保護の責任を課します。 CCPA provides consumers with the right to access and delete their personal information as well as the right to opt out of certain activities that qualify as “selling” personal information to a third party.

企業は、Adobe CX Enterpriseが処理および保存する個人データを自身の代わりに決定します。

As your service provider, Adobe Advertising provides support for your business to fulfill its obligations under CCPA that are applicable to the use of Adobe Advertising products and services, including managing requests to access and delete personal information and managing requests to opt out of the sale of personal information.

This document describes how [!DNL Advertising Search, Social, & Commerce]; Advertising Creative; Advertising DSP (Demand Side Platform); and [!DNL Advertising DCO] — as service providers — support consumers&#39; rights to access and delete personal information using the Adobe [!DNL Experience Platform Privacy Service API] and [!DNL Privacy Service UI].

For information about how Advertising DSP supports the consumer right to opt-out of the sale of personal information, see [Adobe Advertising support for the California Consumer Privacy Act: Consumer opt-out of sale support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

CCPA向けAdobe Privacy Servicesについて詳しくは、[Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## Supported data request types for Adobe Advertising

Adobe Experience Platform provides the ability for businesses to complete the following tasks:

* Access a consumer&#39;s cookie-level data or device ID-level data (for ads in mobile apps) within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO].
* Delete cookie-level data stored within [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP], or [!DNL DCO] for consumers using a browser; or delete ID-level data stored within [!DNL DSP] for consumers using apps on mobile devices.
* Check the status of one or all existing requests.

## Adobe Advertisingのリクエストを送信するための必須セットアップ

Adobe Advertisingから消費者の個人情報にアクセスして削除するリクエストを行うには、次の手順を実行する必要があります。

1. JavaScript ライブラリをデプロイして、お客様のCookieを取得および削除します。 同じライブラリ `AdobePrivacy.js`が、すべてのAdobe CX Enterprise ソリューションに使用されます。

   >[!IMPORTANT]
   >
   >一部のCX Enterprise ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   顧客がアクセス要求や削除要求（企業のプライバシーポータルなど）を送信できるweb ページにライブラリをデプロイする必要があります。 ライブラリは、Adobe Cookie （名前空間ID: `gsurferID`）を取得するのに役立ちます。これにより、[!DNL Adobe Experience Platform Privacy Service API]を介したアクセス要求と削除要求の一部として、これらのIDを送信できます。

   お客様から個人データの削除を求められた場合、ライブラリは、お客様のCookieも顧客のブラウザから削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを使用してエンドユーザーをターゲティングするオプトアウトとは異なります。 ただし、消費者が[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]から個人データを削除するように求めると、ライブラリはAdobe Advertisingにもリクエストを送信して、セグメントターゲティングからお客様をオプトアウトします。 [!DNL Search, Social, & Commerce]を持つ広告主の場合は、オーディエンスセグメントターゲティングをオプトアウトする方法を説明した[https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)へのリンクを顧客に提供することをお勧めします。

1. CX Enterprise組織IDを特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   CX Enterprise organization IDは、「@AdobeOrg」が付いた24文字の英数字の文字列です。 ほとんどのCX Enterpriseのお客様には、組織IDが割り当てられています。 マーケティング部門または社内の[!DNL Adobe] システム管理者が組織IDを把握していない場合、または組織IDがプロビジョニングされているかどうかわからない場合は、Adobe アカウントチームにお問い合わせください。 `imsOrgID`名前空間を使用してPrivacy APIにリクエストを送信するには、組織IDが必要です。

   >[!IMPORTANT]
   >
   >お客様の組織のすべてのAdobe Advertising アカウント（アカウント [!DNL DSP]または広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative]または[!DNL DCO] アカウントを含む）がCX Enterpriseの組織IDにリンクされていることを確認するには、会社のAdobe Advertising担当者にお問い合わせください。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）を使用して、消費者に代わってAdobe Advertisingに個人情報にアクセスおよび削除するリクエストを送信し、既存のリクエストのステータスを確認します。

   モバイルアプリを使用して顧客とやり取りし、[!DNL DSP]を使用してキャンペーンを開始する広告主の場合は、CX Enterprise用のプライバシー対応モバイル SDKをダウンロードする必要があります。 Mobile SDKを使用すると、オプトアウトステータスフラグを設定し、消費者のデバイス ID （名前空間ID: `deviceID`）を取得し、Privacy Service APIにリクエストを送信できます。 モバイルアプリには、SDK バージョン 4.15.0以降が必要です。

   コンシューマアクセスリクエストを送信すると、Privacy Service APIは、指定されたCookieまたはデバイス IDに基づいてコンシューマーの情報を返します。その後、コンシューマーに戻る必要があります。

   消費者の削除リクエストを送信すると、cookie IDまたはデバイス IDと、cookieに関連付けられたすべてのコスト、クリック、収益データがサーバーから削除されます。

   >[!NOTE]
   >
   >ビジネスに複数のCX Enterprise組織IDがある場合は、それぞれに個別のAPI リクエストを送信する必要があります。 ただし、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、および[!DNL DCO]）に1つのAPI リクエストを、サブソリューションごとに1つのアカウントで行うことができます。

Adobe Advertisingからサポートを受けるには、すべての手順が必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクと関連タスク、および必要な項目の検索場所について詳しくは、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)を参照してください。

## Adobe Advertising JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*CX Enterprise組織ID*>

「ユーザー」:

* `"key":` &lt;*通常、お客様の名前*>

* `"action":` （`**access**`または`**delete**`）

* `"user IDs":`

   * `"namespace": **411**` （[[!DNL AdCloud] cookie スペース &#x200B;](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix)を示します）

   * `"value":` &lt;*実際の顧客のcookie ID値（`AdobePrivacy.js`*>から取得）

* `"include": **adCloud**` （リクエストに適用される[[!DNL Adobe] 製品](https://experienceleague.adobe.com/en/docs/experience-platform/privacy/api/appendix)です）

* `"regulation": **ccpa**` （リクエストに適用されるプライバシー規制です）

## AdobePrivacy.jsから取得したAdobe Advertising ユーザーIDを使用して、消費者が送信したリクエストの例

```
{
"companyContexts":[
    {
        "namespace":"imsOrgID",
        "value":"5AB13068374019BC@AdobeOrg"
      }
   ],
   "users": [
{
 "key": "John Doe",
 "action":["access"],
 "userIDs":[
      { 
        "namespace":"411",
        "value":"Wqersioejr-wdg",
        "type":"namespaceId",
        "deletedClientSide":false
      }
   ]
}
],
"include":[
      "adCloud"
   ],
    "regulation":"ccpa"
}
```

## アクセス要求に対して返されるデータフィールド

Adobe Advertisingに対する個人情報アクセス対応の例を次に示します。

```
{
    "jobId":"12345AD43E",
    "action":"access",
    "product":"adCloud",
    "status":"complete",
    "results":{
        "userIDs":[
            {
                "namespace":"411",
                "userID":" Wqersioejr-wdg "
            }
        ],
        "receiptData":{
            "impressionCount":"100",
            "clickCount":5,
            "geo":[
                "United States of America",
                "San Francisco CA"
            ],
            "profile":[
                {
                    "pixelid":"111",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                },
                {
                    "pixelid":"123",
                    "ut1":"abc",
                    "ut2":"def",
                    "ut3":"ghi",
                    "ut4":"jkl",
                    "ut5":"mno"
                }
            ],
            "matchingSegments":[
                {
                    "segmentName":"AP4 - Art/Culture - In-Market",
                    "segmentID":"kV1mPa2aqPNWKSNtf325",
                    "serviceProvider":"Adobe"
                },
                {
                    "segmentName":"eXelate Australia Demographic - Jobs & Education - Job Seekers",
                    "segmentID":"2213789",
                    "serviceProvider":"exelate"
                }
            ]
        }
    }
}
```
