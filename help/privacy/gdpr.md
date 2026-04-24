---
title: EU一般データ保護規則に対するAdobe Advertisingのサポート
description: サポートされているデータ要求タイプ、必要な設定およびフィールド値、およびレガシー製品IDと返されたデータフィールドを使用したAPI アクセス要求の例について説明します
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
TQID: https://experienceleague.adobe.com/qR5H-xgBKdtWcMYfrdGdk1y5s9PEA0-hNGZADbR6TuM
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
source-wordcount: 1046
ht-degree: 0%

---

# EU一般データ保護規則に対するAdobe Advertisingのサポート

*[!DNL Adobe Advertising Search, Social, & Commerce]様、Adobe Advertising DSP、Adobe Advertising CreativeおよびAdobe Advertising DCO*&#x200B;様

>[!IMPORTANT]
>
>本文書の内容は、法律上の助言ではなく、法律上の助言に代わるものではありません。 一般データ保護規則に関するアドバイスについては、法務担当者にお問い合わせください。

一般データ保護規則（GDPR）は、2018年5月25日に施行される法律で、欧州連合（EU）の範囲内のすべての個人（データ主体）に個人データを管理させ、国際的なビジネスの規制環境を簡素化します。 この法律は、データ管理者の事業拠点に関係なく、個人データが処理される時点で、EUの国境内の個人に対して商品またはサービスを提供する、個人データの行動を監視または収集するすべての企業（データ管理者）に適用されます。

Adobe CX Enterpriseは、顧客のために収集、保存する個人データのデータ処理者として機能します。 データ管理者は、Adobe CX Enterpriseがユーザーの代わりに処理および保存する個人データを決定します。

このドキュメントでは、Adobe Experience Platform Privacy Service APIとPrivacy Service UIを使用して、[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP （Demand Side Platform）、[!DNL Advertising DCO]がデータ主体のGDPR データへのアクセス権と削除権をどのようにサポートしているかを説明します。

ビジネスにおけるGDPRの意味について詳しくは、[GDPRとビジネス &#x200B;](https://www.adobe.com/privacy/general-data-protection-regulation.html)を参照してください。

## Adobe Advertisingでサポートされているデータリクエストタイプ

Adobe Experience Platformでは、次のタスクを実行できます。

* [!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]または[!DNL DCO]内のデータ主体のcookie レベルのデータまたはデバイス ID レベルのデータ （モバイルアプリの広告用）にアクセスします。
* ブラウザーを使用してデータ主体の[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]内に保存されているcookie レベルのデータを削除するか、モバイルデバイスでアプリを使用しているデータ主体の[!DNL DSP]内に保存されているID レベルのデータを削除します。
* 1つまたは全ての既存のリクエストのステータスを確認します。

## Adobe Advertisingのリクエストを送信するための必須セットアップ

Adobe Advertisingのデータへのアクセスと削除をリクエストするには、次の操作を行う必要があります。

1. JavaScript ライブラリをデプロイして、データ主体のCookieを取得および削除します。 同じライブラリ `AdobePrivacy.js`が、すべてのAdobe CX Enterprise ソリューションに使用されます。

   >[!IMPORTANT]
   >
   >一部のCX Enterprise ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   企業のプライバシーポータルなどのアクセス要求や削除要求をデータ主体が送信できるweb ページにライブラリをデプロイする必要があります。 ライブラリは、[!DNL Adobe] Cookie （名前空間ID: `gsurferID`）を取得するのに役立ちます。これにより、Adobe Experience Platform Privacy Service APIを介したアクセス要求と削除要求の一部として、これらのIDを送信できます。

   データ主体が個人データの削除を要求すると、ライブラリはデータ主体のブラウザーからデータ主体のCookieも削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントによるエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、データ主体が[!DNL Creative]、[!DNL DSP]、または[!DNL DCO]から個人データを削除するように求められると、ライブラリはAdobe Advertisingにもリクエストを送信して、セグメントターゲティングからデータ主体をオプトアウトします。 [!DNL Search, Social, & Commerce]を持つ広告主の場合は、データ主体に[https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)へのリンクを提供することをお勧めします。これにより、オーディエンスセグメントターゲティングをオプトアウトする方法を説明できます。

1. CX Enterprise組織IDを特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   CX Enterprise organization IDは、「@AdobeOrg」が付いた24文字の英数字の文字列です。 ほとんどのCX Enterpriseのお客様には、組織IDが割り当てられています。 マーケティング部門または社内の[!DNL Adobe] システム管理者が組織IDを把握していない場合、または組織IDがプロビジョニングされているかどうかわからない場合は、Adobe カスタマーケア（gdprsupport@adobe.com）にお問い合わせください。 `imsOrgID`名前空間を使用してPrivacy APIにリクエストを送信するには、組織IDが必要です。

   >[!IMPORTANT]
   >
   >お客様の組織のすべてのAdobe Advertising アカウント（アカウント [!DNL DSP]または広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative]または[!DNL DCO] アカウントを含む）がCX Enterpriseの組織IDにリンクされていることを確認するには、会社のAdobe Advertising担当者にお問い合わせください。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=ja) （自動リクエストの場合）または[Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）を使用して、データ主体に代わってAdobe Advertisingにアクセス要求と削除要求を送信し、既存の要求のステータスを確認します。

   モバイルアプリを使用してデータ主体と対話し、CX Enterpriseでキャンペーンを開始する広告主の場合は、DSP用のプライバシー対応モバイル SDKをダウンロードする必要があります。 Mobile SDKを使用すると、データ管理者はオプトアウトステータスフラグを設定し、データ主体のデバイス ID （名前空間ID: `deviceID`）を取得して、Privacy Service APIにリクエストを送信できます。 モバイルアプリには、SDK バージョン 4.15.0以降が必要です。

   データ主体のアクセスリクエストを送信すると、Privacy Service APIは、指定されたcookieまたはデバイス IDに基づいてデータ主体の情報を返します。その後、データ主体に戻る必要があります。

   データ主体の削除要求を送信すると、cookie IDまたはデバイス IDと、cookieに関連付けられたすべてのコスト、クリック、収益データがサーバーから削除されます。

   >[!NOTE]
   >
   >会社が複数のCX Enterprise組織IDを持っている場合は、それぞれに個別のAPI リクエストを送信する必要があります。 ただし、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、および[!DNL DCO]）に1つのAPI リクエストを、サブソリューションごとに1つのアカウントで行うことができます。

すべての手順はAdobe Advertisingに必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクと関連タスク、および必要な項目の検索場所について詳しくは、「[Privacy Serviceの概要](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja)」を参照してください。

## Adobe Advertising JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*CX Enterprise組織ID*>

`"users":`

* `"key":` &lt;*通常はデータ主体の名前*>

* `"action":` （`**access**`または`**delete**`）

* `"user IDs":`

   * `"namespace": **411**` （[!DNL adcloud] Cookie スペースを示します）

   * `"value":` &lt;*実際のデータ主体のcookie ID値（`AdobePrivacy.js`*>から取得）

* `"include": **adCloud**` （リクエストに適用される[!DNL Adobe]製品）

* `"regulation": **gdpr**` （リクエストに適用されるプライバシー規制です）

## `AdobePrivacy.js`から取得したAdobe Advertising ユーザーIDを使用して、データ主体によって送信されたリクエストの例

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
    "regulation":"gdpr"
}
```

## アクセス要求に対して返されるデータフィールド

次に、Adobe Advertisingのアクセス応答の例を示します。

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

<!-- Changed example from BlueKai (no longer supported) to Exelate -->
