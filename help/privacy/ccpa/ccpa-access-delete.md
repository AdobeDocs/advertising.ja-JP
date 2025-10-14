---
title: California Consumer Privacy Act &#58; Consumer Data Access and Delete のサポートに対するAdobe Advertisingのサポート
description: サポートされるデータリクエストタイプ、必須の設定およびフィールド値、従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: a3e39ca4fa89f84ddc2669662c34bccb4425a2bb
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# カリフォルニア州消費者プライバシー法のAdobe Advertising サポート：消費者データのアクセスと削除のサポート

*[!DNL Adobe Advertising Search, Social, & Commerce]:Adobe Advertising DSP、Adobe Advertising CreativeおよびAdobe Advertising DCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、法務担当者にお問い合わせください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の居住者に個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスを行う特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、自身の個人情報にアクセスする権利および自身の個人情報を削除する権利、ならびに第三者への個人情報の「販売」に該当する特定の活動をオプトアウトする権利を提供します。

お客様は会社として、Adobe Experience Cloudが処理および保存するお客様の代わりになる個人情報を決定します。

Adobe Advertisingは、お客様のサービスプロバイダーとして、お客様の事業が、Adobe Advertisingの製品およびサービスの使用に適用される CCPA の義務を履行するためのサポートを提供します。これには、個人情報へのアクセスおよび削除要求の管理や、個人情報の販売に対するオプトアウト要求の管理が含まれます。

このドキュメントでは、[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP（Demand Side Platform）、[!DNL Advertising DCO] （サービスプロバイダー）が、Adobe [!DNL Experience Platform Privacy Service API] および [!DNL Privacy Service UI] を使用して、個人情報にアクセスする消費者の権利および個人情報を削除する権利をサポートする方法について説明します。

Advertising DSPが個人情報の販売のオプトアウトに対するコンシューマーの権利をサポートする方法について詳しくは、[Adobe Advertising Consumer Privacy Act: Consumer Opt-out Support](/help/privacy/ccpa/ccpa-opt-out-of-sale.md) を参照してください。

CCPA のAdobe プライバシーサービスについて詳しくは、[Adobe プライバシーセンター &#x200B;](https://www.adobe.com/privacy/ccpa.html) を参照してください。

## Adobe Advertisingでサポートされるデータリクエストタイプ

Adobe Experience Platformには、企業が次のタスクを実行する機能が用意されています。

* [!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP] または [!DNL DCO] 内で、消費者の cookie レベルのデータまたはデバイス ID レベルのデータ（モバイルアプリの広告の場合）にアクセスします。
* ブラウザーを使用しているコンシューマー向けに、[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP] または [!DNL DCO] に保存された cookie レベルのデータを削除します。または、モバイルデバイス上のアプリを使用しているコンシューマー向けに、[!DNL DSP] に保存された ID レベルのデータを削除します。
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe Advertisingのリクエストを送信するために必要な設定

Adobe Advertisingから消費者の個人情報へのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、顧客の Cookie を取得および削除します。 同じライブラリ `AdobePrivacy.js` は、すべてのAdobe Experience Cloud ソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloud ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   会社のプライバシーポータルなど、顧客がアクセスリクエストや削除リクエストを送信できる web ページにライブラリをデプロイする必要があります。 ライブラリは、Adobe Cookie （名前空間 ID:`gsurferID`）を取得するのに役立ち、[!DNL Adobe Experience Platform Privacy Service API] 経由でアクセスリクエストと削除リクエストの一部としてこれらの ID を送信できます。

   お客様から個人データの削除を求められると、ライブラリはお客様のブラウザーからお客様の Cookie も削除します。

   >[!NOTE]
   >
   >個人データの削除は、オプトアウトとは異なります。オプトアウトすると、オーディエンスセグメントを使用したエンドユーザーのターゲティングが停止します。 ただし、消費者が [!DNL Creative]、[!DNL DSP]、[!DNL DCO] から個人データを削除するように要求すると、ライブラリはAdobe Advertisingに対しても、セグメントターゲティングからお客様をオプトアウトするように要求を送信します。 [!DNL Search, Social, & Commerce] を使用している広告主の場合は、オーディエンスセグメントターゲティングをオプトアウトする方法を説明したリンク [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse) を顧客に提供することをお勧めします。

1. Experience Cloud組織 ID を特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列の後に「@AdobeOrg」が付いたものです。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは社内の [!DNL Adobe] システム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかわからない場合は、Adobe アカウントチームにお問い合わせください。 `imsOrgID` 名前空間を使用して Privacy API にリクエストを送信するには、組織 ID が必要です。

   >[!IMPORTANT]
   >
   >会社のAdobe Advertising担当者に問い合わせて、組織のすべてのAdobe Advertising アカウント（[!DNL DSP] アカウントまたは広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative] アカウントまたは [!DNL DCO] アカウントを含む）がExperience Cloudの組織 ID にリンクされていることを確認します。

1. [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html?lang=ja) （自動リクエストの場合）または [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）を使用して、コンシューマーの代わりにAdobe Advertisingに個人情報へのアクセスおよび削除リクエストを送信したり、既存のリクエストのステータスを確認したりします。

   モバイルアプリを使用して顧客とやり取りし、[!DNL DSP] でキャンペーンを開始する広告主の場合は、Experience Cloud用のプライバシー対応の Mobile SDK をダウンロードする必要があります。 Mobile SDK を使用すると、企業は、オプトアウトステータスフラグの設定、消費者のデバイス ID （名前空間 ID:`deviceID`）の取得、Privacy Service API へのリクエストの送信を行うことができます。 モバイルアプリには、SDK バージョン 4.15.0 以降が必要です。

   コンシューマーアクセスリクエストを送信すると、Privacy Service API は、指定された cookie またはデバイス ID に基づいてコンシューマーに関する情報を返します。この情報は、コンシューマーに返す必要があります。

   消費者データ削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリックおよび売上高のデータがサーバーから削除されます。

   >[!NOTE]
   >
   >ビジネスに複数のExperience Cloud組織 ID がある場合は、それぞれに個別の API リクエストを送信する必要があります。 ただし、サブソリューションごとに 1 つのアカウントを使用して、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO]）に対して 1 つの API リクエストを行うことができます。

Adobe Advertisingからサポートを受けるにはすべての手順が必要です。 Adobe Experience Platform Privacy Serviceを使用して行う必要のあるこれらのタスクやその他の関連タスクの詳細、および必要な項目の場所については、[https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html?lang=ja) を参照してください。

## Adobe Advertising JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織 ID*>

「ユーザー」:

* `"key":`&lt;*通常、顧客の名前*>

* `**access**` または `**delete**` のいずれかを `"action":` します

* `"user IDs":`

   * `"namespace": **411**` （[[!DNL AdCloud] cookie 領域 &#x200B;](https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/api/appendix) を示します）

   * `"value":` &lt;*`AdobePrivacy.js`* から取得した実際の顧客の Cookie ID 値 >

* `"include": **adCloud**` （リクエストに適用される [[!DNL Adobe] product](https://experienceleague.adobe.com/ja/docs/experience-platform/privacy/api/appendix) です）

* `"regulation": **ccpa**` （リクエストに適用されるプライバシー規制）

## AdobePrivacy.js から取得したAdobe Advertising ユーザー ID を使用して消費者によって送信されたリクエストの例

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

## アクセスリクエストに対して返されるデータフィールド

以下は、Adobe Advertisingに対する個人情報アクセス応答の例です。

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
