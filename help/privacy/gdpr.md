---
title: EU 一般データ保護規則（GDPR）のAdobe Advertisingサポート
description: サポートされるデータリクエストタイプ、必須の設定およびフィールド値、従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: 724b4ff772fa7d6dc0640d35a968d664707ceae6
workflow-type: tm+mt
source-wordcount: '999'
ht-degree: 0%

---

# EU 一般データ保護規則（GDPR）のAdobe Advertisingサポート

*の場合 [!DNL Adobe Advertising Search, Social, & Commerce]、Adobe Advertising DSP、Adobe Advertising Creative、Adobe AdvertisingDCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 EU 一般データ保護規則（GDPR）に関するアドバイスについては、法務担当者にお問い合わせください。

2018 年 5 月 25 日に施行された法律である一般データ保護規則（GDPR）は、欧州連合（EU）の境界内のすべての個人（データ主体）に個人データの管理を提供し、国際的なビジネスのための規制環境を簡素化します。 この法律は、個人データが処理される時点で、データ管理者の事業拠点に関係なく、EU の境界内の個人に対して商品またはサービスを提供、行動を監視、または個人データを収集するすべての企業（データ管理者）に適用されます。

Adobe Experience Cloudは、お客様に代わって受け取り、保存する個人データのデータ処理者として機能します。 データ管理者は、お客様に代わってAdobe Experience Cloudが処理および保存する個人データを決定します。

このドキュメントでは、その方法を説明します [!DNL Advertising Search, Social, & Commerce]、Advertising Creative、Advertising DSP（Demand Side Platform）、および [!DNL Advertising DCO] Adobe Experience Platform Privacy Service API とPrivacy ServiceUI を使用して、データ主体の GDPR データアクセスおよび削除権をサポートします。

GDPR がお客様のビジネスに与える影響について詳しくは、以下を参照してください。 [GDPR とビジネス](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Adobe Advertisingでサポートされるデータリクエストタイプ

Adobe Experience Platformには、企業が次のタスクを実行する機能が用意されています。

* 内で、データ主体の cookie レベルのデータまたはデバイス ID レベルのデータ（モバイルアプリの広告用）にアクセスします [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、または [!DNL DCO].
* 内に保存された cookie レベルのデータの削除 [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、または [!DNL DCO] ブラウザーを使用してデータ主体の場合、または内に保存された ID レベルのデータを削除します [!DNL DSP] モバイルデバイスでアプリを使用するデータ主体。
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe Advertisingリクエストを送信するために必要な設定

Adobe Advertising用のデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、データ主体の Cookie を取得および削除します。 同じライブラリ、 `AdobePrivacy.js`は、すべてのAdobe Experience Cloud ソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のExperience Cloudソリューションへのリクエストには JavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   ライブラリは、データ主体がアクセス要求および削除要求（会社のプライバシーポータルなど）を送信できる Web ページにデプロイする必要があります。 ライブラリは次の情報を取得するのに役立ちます [!DNL Adobe] cookie （名前空間 ID: `gsurferID`）を設定できるので、Adobe Experience Platform Privacy Service API 経由でのアクセスリクエストおよび削除リクエストの一環として、これらの ID を送信できます。

   データ主体が個人データの削除を要求すると、ライブラリはデータ主体のブラウザーからもデータ主体の Cookie を削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、データ主体がから個人データを削除するように求めた場合は、 [!DNL Creative], [!DNL DSP]、または [!DNL DCO]また、ライブラリは、データ主体をセグメントターゲティングからオプトアウトするリクエストをAdobe Advertisingに送信します。 を使用する広告主向け [!DNL Search, Social, & Commerce]データ主体は、次へのリンクを指定することをお勧めします [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)オーディエンスセグメントのターゲティングをオプトアウトする方法を説明します。

1. Experience Cloud組織 ID を特定し、Adobe Advertisingアカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列の後に「@AdobeOrg」を付けたものです。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは社内の場合 [!DNL Adobe] システム管理者が組織 ID を把握できないか、組織 ID がプロビジョニングされているかどうかわからない場合は、Adobeカスタマーケア（gdprsupport@adobe.com）にお問い合わせください。 を使用してプライバシー API にリクエストを送信するには、組織 ID が必要です。 `imsOrgID` 名前空間。

   >[!IMPORTANT]
   >
   >以下を含む組織のすべてのAdobe Advertisingアカウントを確認するには、Adobe Advertising担当者にお問い合わせください [!DNL DSP] アカウントまたは広告主、 [!DNL Search, Social, & Commerce] アカウント、 [!DNL Creative] または [!DNL DCO] アカウント — Experience Cloud組織 ID にリンクされています。

1. 次のいずれかを使用します [ADOBE EXPERIENCE PLATFORM PRIVACY SERVICE API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または [PRIVACY SERVICEUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）データ主体に代わってAdobe Advertisingにアクセスリクエストと削除リクエストを送信し、既存のリクエストのステータスを確認します。

   モバイルアプリを使用してデータ主体とやり取りし、DSPでキャンペーンを開始する広告主の場合は、プライバシーに対応した Mobile SDK をダウンロードしてExperience Cloudする必要があります。 Mobile SDK を使用すると、データ管理者はオプトアウトステータスフラグを設定し、データ主体のデバイス ID （名前空間 ID）を取得できます。 `deviceID`）、Privacy ServiceAPI にリクエストを送信します。 モバイルアプリには、SDK バージョン 4.15.0 以降が必要です。

   データ主体のアクセスリクエストを送信すると、Privacy ServiceAPI は、指定された cookie またはデバイス ID に基づいてデータ主体の情報を返します。その後、データ主体に戻る必要があります。

   データ主体の削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリック数、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   >
   >会社に複数のExperience Cloud組織 ID がある場合、それぞれに個別の API リクエストを送信する必要があります。 ただし、複数のAdobe Advertisingサブソリューション（[!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、および [!DNL DCO]）、サブソリューションごとに 1 つのアカウントを使用します。

これらすべての手順はAdobe Advertisingに必要です。 Adobe Experience Platform Privacy Serviceを使用して行う必要のあるこれらのタスクやその他の関連タスクの詳細、および必要な項目の場所については、「」を参照してください[Privacy Serviceの概要](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).」と入力します。

## Adobe Advertisingの JSON リクエストの必須フィールド値

`"company context":`

* `"namespace": **imsOrgID**`
* `"value":` &lt;*Experience Cloud組織 ID*>

`"users":`

* `"key":` &lt;*通常、データ主体の名前*>

* `"action":` 次のいずれか `**access**` または `**delete**`

* `"user IDs":`

   * `"namespace": **411**` （これは、 [!DNL adcloud] cookie 領域）

   * `"value":` &lt;*から取得された実際のデータ主体の Cookie ID 値`AdobePrivacy.js`*>

* `"include": **adCloud**` （これはです [!DNL Adobe] （該当する商品）

* `"regulation": **gdpr**` （リクエストに適用されるプライバシー規制です）

## から取得したAdobe Advertisingユーザー ID を使用してデータ主体が送信したリクエストの例 `AdobePrivacy.js`

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
