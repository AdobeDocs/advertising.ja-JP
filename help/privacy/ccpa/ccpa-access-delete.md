---
title: カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者データのアクセスと削除のサポート
description: サポートされるデータリクエストタイプ、必須の設定およびフィールド値、従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します。
feature: CCPA
role: User, Developer
exl-id: e7808411-7dc3-499c-bda1-1f5882f651b2
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 0%

---

# カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者データのアクセスと削除のサポート

*の場合 [!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative、Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、法務担当者にお問い合わせください。

カリフォルニア州消費者プライバシー法（CCPA）は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の居住者に個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスを行う特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、自身の個人情報にアクセスする権利および自身の個人情報を削除する権利、ならびに第三者への個人情報の「販売」に該当する特定の活動をオプトアウトする権利を提供します。

お客様は会社として、Adobe Experience Cloudが処理および保存するお客様の代わりになる個人情報を決定します。

Adobe Advertisingは、お客様のサービスプロバイダーとして、個人情報へのアクセスおよび削除要求の管理、個人情報のAdobe Advertisingのオプトアウト要求の管理など、お客様のビジネスが CCPA に基づく個人情報およびサービスの使用に適用される義務を履行するためのサポートを提供します。

このドキュメントでは、その方法を説明します [!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP（Demand Side Platform）、および [!DNL Advertising DCO]  – サービスプロバイダーとして – Adobeを使用して、個人情報へのアクセスおよび削除に関する消費者の権利をサポートします [!DNL Experience Platform Privacy Service API] および [!DNL Privacy Service UI].

Advertising DSPが個人情報の販売をオプトアウトする消費者の権利をサポートする方法について詳しくは、以下を参照してください。 [カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者オプトアウトサポート](/help/privacy/ccpa/ccpa-opt-out-of-sale.md).

CCPA のAdobe プライバシーサービスの詳細については、次を参照してください。 [Adobe プライバシーセンター](https://www.adobe.com/privacy/ccpa.html).

## Adobe Advertisingでサポートされるデータリクエストタイプ

Adobe Experience Platformには、企業が次のタスクを実行する機能が用意されています。

* 内で消費者の cookie レベルのデータまたはデバイス ID レベルのデータ（モバイルアプリの広告用）にアクセスします [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、または [!DNL DCO].
* 内に保存された cookie レベルのデータの削除 [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、または [!DNL DCO] ブラウザーを使用しているコンシューマーの場合、または内に保存されている ID レベルのデータを削除する場合 [!DNL DSP] モバイルデバイスでアプリを使用する消費者の場合。
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe Advertisingリクエストを送信するために必要な設定

Adobe Advertisingから消費者の個人情報へのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、顧客の Cookie を取得および削除します。 同じライブラリ、 `AdobePrivacy.js`は、すべてのAdobe Experience Cloud ソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloudソリューションへのリクエストには JavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   会社のプライバシーポータルなど、顧客がアクセスリクエストや削除リクエストを送信できる web ページにライブラリをデプロイする必要があります。 ライブラリを使用すると、Adobe Cookie （名前空間 ID: `gsurferID`を使用して、これらの ID をアクセスリクエストおよび削除リクエストの一部として送信できるように [!DNL Adobe Experience Platform Privacy Service API].

   お客様から個人データの削除を求められると、ライブラリはお客様のブラウザーからお客様の Cookie も削除します。

   >[!NOTE]
   >
   >個人データの削除は、オプトアウトとは異なります。オプトアウトすると、オーディエンスセグメントを使用したエンドユーザーのターゲティングが停止します。 ただし、消費者がから個人データを削除するように求めた場合は、 [!DNL Creative], [!DNL DSP]、または [!DNL DCO]また、ライブラリは、セグメントターゲティングからAdobe Advertisingをオプトアウトするリクエストを顧客に送信します。 を使用する広告主向け [!DNL Search, Social, & Commerce]の場合は、次へのリンクを顧客に提供することをお勧めします [https://www.adobe.com/privacy/opt-out.html#customeruse](https://www.adobe.com/privacy/opt-out.html#customeruse)オーディエンスセグメントのターゲティングをオプトアウトする方法を説明します。

1. Experience Cloud組織 ID を特定し、その ID がAdobe Advertisingアカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列の後に「@AdobeOrg」を付けたものです。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは社内の場合 [!DNL Adobe] システム管理者が組織 ID を把握していないか、プロビジョニングされているかどうかわからない場合は、Adobeアカウントチームにお問い合わせください。 を使用してプライバシー API にリクエストを送信するには、組織 ID が必要です。 `imsOrgID` 名前空間。

   >[!IMPORTANT]
   >
   >以下を含む組織のすべてのAdobe Advertisingアカウントを確認するには、Adobe Advertising担当者にお問い合わせください [!DNL DSP] アカウントまたは広告主、 [!DNL Search, Social, & Commerce] アカウント、 [!DNL Creative] または [!DNL DCO] アカウント — Experience Cloud組織 ID にリンクされています。

1. 次のいずれかを使用します [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）消費者の代わりにAdobe Advertisingに対して個人情報へのアクセスおよび削除要求を送信し、既存の要求のステータスを確認します。

   モバイルアプリを使用して顧客とやり取りし、でキャンペーンを開始する広告主の場合 [!DNL DSP]の場合、Experience Cloud用にプライバシー対応の Mobile SDK をダウンロードする必要があります。 Mobile SDK を使用すると、企業は、オプトアウトステータスフラグを設定し、消費者のデバイス ID （名前空間 ID: `deviceID`）、Privacy ServiceAPI にリクエストを送信します。 モバイルアプリには、SDK バージョン 4.15.0 以降が必要です。

   コンシューマーアクセスリクエストを送信すると、Privacy ServiceAPI は、指定された cookie またはデバイス ID に基づいてコンシューマーに関する情報を返します。この情報は、コンシューマーに返す必要があります。

   消費者データ削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリックおよび売上高のデータがサーバーから削除されます。

   >[!NOTE]
   >
   >ビジネスに複数のExperience Cloud組織 ID がある場合は、それぞれに個別の API リクエストを送信する必要があります。 ただし、複数のAdobe Advertisingサブソリューション（[!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、および [!DNL DCO]）、サブソリューションごとに 1 つのアカウントを使用します。

Adobe Advertisingのサポートを受けるには、これらすべての手順が必要です。 Adobe Experience Platform Privacy Serviceを使用して行う必要のあるこれらのタスクやその他の関連タスクの詳細、および必要な情報については、を参照してください。 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## Adobe Advertisingの JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織 ID*>

「ユーザー」:

* `"key":` &lt;*通常、顧客の名前*>

* `"action":` 次のいずれか `**access**` または `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （これは、 [!DNL adCloud] cookie 領域）

   * `"value":` &lt;*から取得された、実際の顧客の Cookie ID 値`AdobePrivacy.js`*>

* `"include": **adCloud**` （これはです [!DNL Adobe] （該当する商品）

* `"regulation": **ccpa**` （リクエストに適用されるプライバシー規制です）

## AdobePrivacy.js から取得したAdobe Advertisingユーザー ID を使用して消費者によって送信されたリクエストの例

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

次に、Adobe Advertisingに対する個人情報アクセス応答の例を示します。

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
