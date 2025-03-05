---
title: EU 一般データ保護規則に対するAdobe Advertisingのサポート
description: サポートされるデータリクエストタイプ、必須の設定およびフィールド値、従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 8d88a46e82a17ce5d2debf93ea0652f35a734d7a
workflow-type: tm+mt
source-wordcount: '997'
ht-degree: 0%

---

# EU 一般データ保護規則に対するAdobe Advertisingのサポート

*[!DNL Adobe Advertising Search, Social, & Commerce]:Adobe Advertising DSP、Adobe Advertising CreativeおよびAdobe Advertising DCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 EU 一般データ保護規則（GDPR）に関するアドバイスについては、法務担当者にお問い合わせください。

2018 年 5 月 25 日に施行された法律である一般データ保護規則（GDPR）は、欧州連合（EU）の境界内のすべての個人（データ主体）に個人データの管理を提供し、国際的なビジネスのための規制環境を簡素化します。 この法律は、個人データが処理される時点で、データ管理者の事業拠点に関係なく、EU の境界内の個人に対して商品またはサービスを提供、行動を監視、または個人データを収集するすべての企業（データ管理者）に適用されます。

Adobe Experience Cloudは、お客様に代わって受け取り、保存する個人データのデータ処理者として機能します。 データ管理者は、お客様に代わってAdobe Experience Cloudが処理および保存する個人データを決定します。

このドキュメントでは、[!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP（Demand Side Platform）、および [!DNL Advertising DCO] が、Adobe Experience Platform Privacy Service API とPrivacy Service UI を使用して、データ主体の GDPR データアクセスおよび削除権をサポートする方法について説明します。

GDPR がお客様のビジネスに与える影響について詳しくは、「[GDPR とお客様のビジネス ](https://www.adobe.com/privacy/general-data-protection-regulation.html)」を参照してください。

## Adobe Advertisingでサポートされるデータリクエストタイプ

Adobe Experience Platformには、企業が次のタスクを実行する機能が用意されています。

* [!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO] 内で、データ主体の cookie レベルのデータまたはデバイス ID レベルのデータ（モバイルアプリの広告の場合）にアクセスします。
* ブラウザーを使用してデータ主体の [!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO] に保存された cookie レベルのデータを削除します。または、モバイルデバイス上のアプリを使用して、データ主体の [!DNL DSP] に保存された ID レベルのデータを削除します。
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe Advertisingのリクエストを送信するために必要な設定

Adobe Advertisingのデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、データ主体の cookie を取得および削除します。 同じライブラリ `AdobePrivacy.js` は、すべてのAdobe Experience Cloud ソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloud ソリューションへのリクエストにはJavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   ライブラリは、データ主体がアクセス要求および削除要求（会社のプライバシーポータルなど）を送信できる Web ページにデプロイする必要があります。 ライブラリは、[!DNL Adobe] Cookie （名前空間 ID:`gsurferID`）を取得するのに役立ち、Adobe Experience Platform Privacy Service API を使用してアクセスリクエストや削除リクエストの一部としてこれらの ID を送信できます。

   データ主体が個人データの削除を要求すると、ライブラリはデータ主体のブラウザーからもデータ主体の Cookie を削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、データ主体が [!DNL Creative]、[!DNL DSP] または [!DNL DCO] から個人データを削除するように要求すると、ライブラリはAdobe Advertisingに対しても、セグメントターゲティングからデータ主体をオプトアウトするように要求を送信します。 [!DNL Search, Social, & Commerce] を使用している広告主の場合は、データ主体に、オーディエンスセグメントターゲティングをオプトアウトする方法を説明した [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html) へのリンクを提供することをお勧めします。

1. Experience Cloud組織 ID を特定し、Adobe Advertising アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列の後に「@AdobeOrg」が付いたものです。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは社内の [!DNL Adobe] システム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかわからない場合は、gdprsupport@adobe.comのAdobe カスタマーケアにお問い合わせください。 `imsOrgID` 名前空間を使用して Privacy API にリクエストを送信するには、組織 ID が必要です。

   >[!IMPORTANT]
   >
   >会社のAdobe Advertising担当者に問い合わせて、組織のすべてのAdobe Advertising アカウント（[!DNL DSP] アカウントまたは広告主、[!DNL Search, Social, & Commerce] アカウント、[!DNL Creative] アカウントまたは [!DNL DCO] アカウントを含む）がExperience Cloudの組織 ID にリンクされていることを確認します。

1. データ主体に代わってAdobe Advertisingにアクセスリクエストと削除リクエストを送信し、既存のリクエストのステータスを確認するには、[Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または [Privacy Service UI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）を使用します。

   モバイルアプリを使用してデータ主体とやり取りし、DSPでキャンペーンを開始する広告主の場合は、Experience Cloudのプライバシーに対応した Mobile SDK をダウンロードする必要があります。 Mobile SDK を使用すると、データ管理者はオプトアウトステータスフラグを設定し、データ主体のデバイス ID （名前空間 ID:`deviceID`）を取得して、Privacy Service API にリクエストを送信できます。 モバイルアプリには、SDK バージョン 4.15.0 以降が必要です。

   データ主体のアクセスリクエストを送信すると、Privacy Service API は、指定された cookie またはデバイス ID に基づいてデータ主体の情報を返します。その後、データ主体に戻る必要があります。

   データ主体の削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリック数、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   >
   >会社に複数のExperience Cloud組織 ID がある場合、それぞれに個別の API リクエストを送信する必要があります。 ただし、サブソリューションごとに 1 つのアカウントを使用して、複数のAdobe Advertising サブソリューション（[!DNL Search, Social, & Commerce]、[!DNL Creative]、[!DNL DSP]、[!DNL DCO]）に対して 1 つの API リクエストを行うことができます。

すべての手順はAdobe Advertisingに必要です。 Adobe Experience Platform Privacy Serviceを使用して行う必要のあるこれらのタスクやその他の関連タスクの詳細、および必要な項目をどこで見つけるかについて詳しくは、「[Privacy Serviceの概要 ](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html)」を参照してください。

## Adobe Advertising JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織 ID*>

`"users":`

* `"key":` &lt;*通常はデータ主体の名前*>

* `**access**` または `**delete**` のいずれかを `"action":` します

* `"user IDs":`

   * `"namespace": **411**` （[!DNL adcloud] の cookie 領域を示します）

   * `"value":` &lt;*`AdobePrivacy.js`* から取得した実際のデータ主体の Cookie ID 値 >

* `"include": **adCloud**` （リクエストに適用される [!DNL Adobe] 製品）

* `"regulation": **gdpr**` （リクエストに適用されるプライバシー規制）

## `AdobePrivacy.js` から取得したAdobe Advertising ユーザー ID を使用してデータ主体から送信されたリクエストの例

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

## アクセスリクエストに対して返されるデータフィールド

次に、Adobe Advertisingに対するアクセス応答の例を示します。

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
