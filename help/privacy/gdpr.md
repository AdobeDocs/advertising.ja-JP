---
title: EU 一般データ保護規則のAdobe Advertisingサポート
description: サポートされるデータリクエストの種類、必須セットアップとフィールド値、および従来の製品 ID と返されたデータフィールドを使用した API アクセスリクエストの例について説明します
feature: GDPR
role: User, Developer
exl-id: abf0dc51-e23b-4c9a-95aa-14e0844939bb
source-git-commit: df19f47971e97727c85bce99ce80b677fbdb1a49
workflow-type: tm+mt
source-wordcount: '1032'
ht-degree: 0%

---

# EU 一般データ保護規則のAdobe Advertisingサポート

*の場合 [!DNL Adobe Advertising Search, Social, & Commerce];Adobe Advertising DSP;Adobe Advertising Creative;およびAdobe AdvertisingDCO*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 EU 一般データ保護規則に関するアドバイスについては、弁護士に相談してください。

2018 年 5 月 25 日施行の法律である GDPR（EU 一般データ保護規則）は、EU 圏内にあるすべての個人（データ主体）に対して個人データを制御し、国際ビジネスの規制環境を簡素化します。 この法律は、データ管理者の事業所に関係なく、個人データの処理時に EU 圏内の個人に対して商品やサービスを提供し、行動を監視し、個人データを収集するすべての企業（データ管理者）に適用されます。

Adobe Experience Cloudは、顧客に代わって受信および保存する個人データのデータ処理者としての役割を果たします。 データ管理者であるお客様は、Adobe Experience Cloudに処理および保管を委任する個人データを決めます。

このドキュメントでは、 [!DNL Advertising Search, Social, & Commerce];Advertising Creative;Advertising DSP (Demand Side Platform)および [!DNL Advertising DCO] は、Adobe Experience Platform Privacy Service API とPrivacy ServiceUI を使用して、データ主体の GDPR データアクセスおよび削除権をサポートします。

GDPR がお客様のビジネスに与える影響について詳しくは、 [GDPR とビジネス](https://www.adobe.com/privacy/general-data-protection-regulation.html).

## Adobe Advertisingでサポートされているデータリクエストタイプ

Adobe Experience Platformは、企業が次のタスクを実行する機能を提供します。

* 内で、データ主体の cookie レベルのデータまたはデバイス ID レベルのデータにアクセスする（モバイルアプリの広告の場合） [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]または [!DNL DCO].
* に保存されている Cookie レベルのデータの削除 [!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]または [!DNL DCO] ブラウザーを使用するデータ主体の場合または、に保存されている ID レベルのデータを削除します。 [!DNL DSP] モバイルデバイスでアプリを使用するデータ主体向け
* 1 つまたはすべての既存のリクエストのステータスを確認します。

## Adobe Advertisingのリクエストを送信するために必要な設定

Adobe Advertising用にデータへのアクセスおよび削除をリクエストするには、次の操作が必要です。

1. JavaScript ライブラリをデプロイして、データ主体の Cookie を取得および削除します。 同じライブラリ `AdobePrivacy.js`は、すべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience Cloudソリューションへのリクエストには JavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   Web ページにライブラリをデプロイして、会社のプライバシーポータルなど、データ主体がアクセス要求や削除要求を送信できるようにする必要があります。 ライブラリを使用すると、AdobeCookie( 名前空間 ID: `gsurferID`) を使用して、Adobe Experience Platform Privacy Service API を介してこれらの id をアクセスリクエストや削除リクエストの一部として送信できるようにします。

   データ主体が個人データの削除を要求すると、ライブラリはデータ主体のブラウザーからデータ主体の Cookie も削除します。

   >[!NOTE]
   >
   >個人データの削除は、オーディエンスセグメントを持つエンドユーザーのターゲティングを停止するオプトアウトとは異なります。 ただし、データ主体が次の場所から個人データの削除を要求した場合は、 [!DNL Creative], [!DNL DSP]または [!DNL DCO]また、ライブラリは、セグメントのターゲティングからデータ主体をオプトアウトするためのリクエストをAdobe Advertisingに送信します。 を持つ広告主の場合 [!DNL Search, Social, & Commerce]を使用する場合は、データ主体にリンクを設定することをお勧めします。 [https://www.adobe.com/privacy/opt-out.html](https://www.adobe.com/privacy/opt-out.html)：オーディエンスセグメントターゲティングをオプトアウトする方法を説明します。

1. Experience Cloud組織 ID を特定し、組織アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列で、末尾に「@AdobeOrg」が付きます。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア (gdprsupport@adobe.com) にお問い合わせください。 プライバシー API に要求を送信するには、組織 ID が、 `imsOrgID` 名前空間。

   >[!IMPORTANT]
   >
   >貴社のAdobe Advertising担当者に問い合わせて、組織のAdobe Advertisingアカウント ( [!DNL DSP] アカウントまたは広告主 [!DNL Search, Social, & Commerce] アカウントおよび [!DNL Creative] または [!DNL DCO] アカウント — がExperience Cloud組織 ID にリンクされている。

1. 次のいずれかを使用します。 [Adobe Experience Platform Privacy Service API](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/privacy-jobs.html) （自動リクエストの場合）または [Privacy ServiceUI](https://experienceleague.adobe.com/docs/experience-platform/privacy/ui/user-guide.html?lang=ja) （アドホックリクエストの場合）データ主体に代わってAdobe Advertisingにアクセス要求および削除要求を送信し、既存の要求のステータスを確認することができます。

   モバイルアプリを持つ広告主がデータ主体とやり取りし、DSPとキャンペーンを開始する場合、Experience Cloud用にプライバシー対応の Mobile SDK をダウンロードする必要があります。 Mobile SDK を使用すると、データ管理者はオプトアウトステータスフラグの設定、データ主体のデバイス ID( 名前空間 ID:deviceID) を使用し、要求をPrivacy ServiceAPI に送信します。 モバイルアプリには、SDK バージョン4.15.0以降が必要です。

   データ主体のアクセスリクエストを送信すると、Privacy ServiceAPI は指定された Cookie またはデバイス ID に基づいてデータ主体の情報を返します。その後、データ主体に戻る必要があります。

   データ主体の削除リクエストを送信すると、cookie ID またはデバイス ID と、その cookie に関連するすべてのコスト、クリック数、売上高のデータがサーバーから削除されます。

   >[!NOTE]
   >
   会社に複数のExperience Cloud組織 ID がある場合は、それぞれに対して個別の API リクエストを送信する必要があります。 ただし、複数のAdobe Advertisingサブソリューション ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、および [!DNL DCO]) の代わりに、サブソリューションごとに 1 つのアカウントを使用します。

これらの手順はすべて、Adobe Advertisingに必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、 [プライバシーと GDPR](https://developer.adobe.com/client-sdks/documentation/privacy-and-gdpr/).

## Adobe AdvertisingJSON リクエストの必須フィールド値

&quot;&quot;会社コンテキスト&quot;:

* `"namespace": **imsOrgID**`
* `"value":` &lt;*お使いの IMS Org ID 値*>

`"users":`

* `"key":` &lt;*通常、データ主体の名前*>

* `"action":` どちらか `**access**` または `**delete**`

* `"user IDs":`

   * `"namespace": **411**` ( これは、 [!DNL adcloud] cookie スペース )

   * `"value":` &lt;*から取得された実際のデータ主体の Cookie ID 値`AdobePrivacy.js`*>

* `"include": **adCloud**` ( リクエストに適用されるAdobe製品 )

* `"regulation": **gdpr**` （リクエストに適用されるプライバシー規則）

## から取得したユーザー ID を使用してデータ主体から送信されたAdobe Advertisingのリクエストの例 `AdobePrivacy.js`

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
                    "segmentName":"EMEA - UK - Health Food Buyers",
                    "segmentID":"eP2oJ2UPsfsDVDhvlGewx",
                    "serviceProvider":"BlueKai"
                }
            ]
        }
    }
}
```
