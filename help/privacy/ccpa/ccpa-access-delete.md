---
title: Adobe Advertisingによるカリフォルニア州消費者プライバシー法のサポート &#58；消費者データへのアクセスと削除のサポート
description: サポートされているデータ要求タイプ、必要な設定およびフィールド値、およびレガシー製品IDと返されたデータフィールドを使用したAPI アクセス要求の例について説明します。
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
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1041
ht-degree: 0%

---

# Adobe Advertisingによるカリフォルニア州消費者プライバシー法のサポート：消費者データへのアクセスと削除のサポート

*[!DNL Adobe Advertising Search, Social, & Commerce]様、Adobe Advertising DSP、Adobe Advertising CreativeおよびAdobe Advertising DCO*&#x200B;様

>[!IMPORTANT]
>
>本文書の内容は、法律上の助言ではなく、法律上の助言に代わるものではありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士にご相談ください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020年1月1日に施行される、カリフォルニア州の新しいプライバシー法です。 CCPAは、カリフォルニア在住の方の個人情報に関する新たな権利を提供し、カリフォルニア州で事業を行う特定の企業に対してデータ保護の責任を課します。 CCPAは、消費者が自身の個人情報にアクセスして削除する権利と、個人情報を第三者に「販売」すると認定される特定の活動をオプトアウトする権利を提供します。

企業は、Adobe Experience Cloudが処理および保存する個人データを自身の代わりに決定します。

お客様のサービスプロバイダーとして、Adobe Advertisingは、個人情報へのアクセスおよび削除のリクエストの管理、個人情報の販売をオプトアウトするリクエストの管理など、Adobe Advertisingの製品およびサービスの使用に適用されるCCPAに基づく義務を果たすために、お客様のビジネスをサポートします。

このドキュメントでは、[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP （Demand Side Platform）、および[!DNL Advertising DCO]がサービスプロバイダーとして、Adobe [!DNL Experience Platform Privacy Service API]および[!DNL Privacy Service UI]を使用して個人情報にアクセスおよび削除する消費者の権利をどのようにサポートしているかを説明します。

Advertising DSPが個人情報の販売をオプトアウトする消費者の権利をどのようにサポートしているかについて詳しくは、[Adobe Advertising消費者プライバシー法に関するカリフォルニア州サポート：消費者の販売停止サポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)を参照してください。

CCPA向けAdobe Privacy Servicesについて詳しくは、[Adobe Privacy Center](https://www.adobe.com/privacy/ccpa.html)を参照してください。

## Adobe Advertisingでサポートされているデータリクエストタイプ

Adobe Experience Platformでは、次のタスクを実行できます。

* [!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]または[!DNL DCO]内の消費者のcookie レベルのデータまたはデバイス ID レベルのデータ （モバイルアプリの広告用）にアクセスします。
* ブラウザーを使用しているコンシューマーの場合は[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]内に保存されているcookie レベルのデータを削除します。モバイルデバイスでアプリを使用しているコンシューマーの場合は、[!DNL DSP]内に保存されているID レベルのデータを削除します。
* 1つまたは全ての既存のリクエストのステータスを確認します。

## Adobe Advertisingのリクエストを送信するための必須セットアップ

Adobe Advertisingから消費者の個人情報にアクセスして削除するリクエストを行うには、次の手順を実行する必要があります。

1. JavaScript ライブラリをデプロイして、お客様のCookieを取得および削除します。 同じライブラリ `AdobePrivacy.js`が、すべてのAdobe Experience Cloud ソリューションに使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloud ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   顧客がアクセス要求や削除要求（企業のプライバシーポータルなど）を送信できるweb ページにライブラリをデプロイする必要があります。 ライブラリは、Adobe Cookie （名前空間ID: `gsurferID`）を取得するのに役立ちます。これにより、[!DNL Adobe Experience Platform Privacy Service API]を介したアクセス要求と削除要求の一部として、これらのIDを送信できます。

   お客様から個人データの削除を求められた場合、ライブラリは、お客様のCookieも顧客のブラウザから削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを使用してエンドユーザーをターゲティングするオプトアウトとは異なります。 ただし、消費者が[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]から個人データを削除するように求めると、ライブラリはAdobe Advertisingにもリクエストを送信して、セグメントターゲティングからお客様をオプトアウトします。 [!DNL Search, Social, & Commerce]を持つ広告主の場合は、オーディエンスセグメントターゲティングをオプトアウトする方法を説明した[https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)へのリンクを顧客に提供することをお勧めします。

1. Experience Cloud組織IDを特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   Experience Cloud組織IDは、「@AdobeOrg」が付いた24文字の英数字の文字列です。 ほとんどのExperience Cloudのお客様には、組織IDが割り当てられています。 マーケティング部門または社内の[!DNL Adobe] システム管理者が組織IDを把握していない場合、または組織IDがプロビジョニングされているかどうかわからない場合は、Adobe アカウントチームにお問い合わせください。 `imsOrgID`名前空間を使用してPrivacy APIにリクエストを送信するには、組織IDが必要です。

   >[!IMPORTANT]
   >
   >お客様の組織のすべてのAdobe Advertising アカウント（アカウント [!DNL DSP]または広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative]または[!DNL DCO] アカウントを含む）がExperience Cloudの組織IDにリンクされていることを確認するには、会社のAdobe Advertising担当者にお問い合わせください。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）を使用して、消費者に代わってAdobe Advertisingに個人情報にアクセスおよび削除するリクエストを送信し、既存のリクエストのステータスを確認します。

   モバイルアプリを使用して顧客とやり取りし、[!DNL DSP]を使用してキャンペーンを開始する広告主の場合は、Experience Cloud用のプライバシー対応モバイル SDKをダウンロードする必要があります。 Mobile SDKを使用すると、オプトアウトステータスフラグを設定し、消費者のデバイス ID （名前空間ID: `deviceID`）を取得し、Privacy Service APIにリクエストを送信できます。 モバイルアプリには、SDK バージョン 4.15.0以降が必要です。

   コンシューマアクセスリクエストを送信すると、Privacy Service APIは、指定されたCookieまたはデバイス IDに基づいてコンシューマーの情報を返します。その後、コンシューマーに戻る必要があります。

   消費者の削除リクエストを送信すると、cookie IDまたはデバイス IDと、cookieに関連付けられたすべてのコスト、クリック、収益データがサーバーから削除されます。

   >[!NOTE]
   >
   >ビジネスに複数のExperience Cloud組織IDがある場合は、それぞれに個別のAPI リクエストを送信する必要があります。 ただし、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、および[!DNL DCO]）に1つのAPI リクエストを、サブソリューションごとに1つのアカウントで行うことができます。

Adobe Advertisingからサポートを受けるには、すべての手順が必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクと関連タスク、および必要な項目の検索場所について詳しくは、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja)を参照してください。

## Adobe Advertising JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織ID*>

「ユーザー」:

* `"key":` &lt;*通常、お客様の名前*>

* `"action":` （`**access**`または`**delete**`）

* `"user IDs":`

   * `"namespace": **411**` （[[!DNL AdCloud] cookie スペース &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/api/appendix)を示します）

   * `"value":` &lt;*実際の顧客のcookie ID値（`AdobePrivacy.js`*>から取得）

* `"include": **adCloud**` （リクエストに適用される[[!DNL Adobe] 製品](https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/api/appendix)です）

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
