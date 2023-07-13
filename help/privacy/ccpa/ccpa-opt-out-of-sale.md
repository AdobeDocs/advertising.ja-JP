---
title: カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者のオプトアウトオブセールのサポート
description: 消費者のオプトアウトオブセールのリクエストをキャプチャするためのサポートについて説明します。
feature: CCPA
role: User, Developer
exl-id: df2b8679-8a1c-4cd7-b867-cd2f53c76c8f
source-git-commit: df19f47971e97727c85bce99ce80b677fbdb1a49
workflow-type: tm+mt
source-wordcount: '1003'
ht-degree: 0%

---

# カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者のオプトアウト（販売のサポート）

*Adobe AdvertisingDemand Side Platform(DSP)*

>[!IMPORTANT]
>
>このドキュメントの内容は法的な助言ではなく、その代用になるものでもありません。 カリフォルニア州消費者プライバシー法に関するアドバイスについては、弁護士に相談してください。

カリフォルニア州消費者プライバシー法 (CCPA) は、2020 年 1 月 1 日に施行されるカリフォルニア州の新しいプライバシー法です。 CCPA は、カリフォルニア州の住民に対して個人情報に関する新しい権利を提供し、カリフォルニア州でビジネスをおこなう特定の事業者に対してデータ保護の責任を課します。 CCPA は、消費者に対し、データにアクセスし削除する権利と、個人情報を第三者に「販売」すると見なされる特定の活動をオプトアウトする権利を提供します。

お客様は、ビジネスとして、Adobe Experience Cloudに処理および保管を委任する個人データを決定します。

Adobe Advertisingは、サービスプロバイダーとして、個人情報に対する消費者のアクセスおよび削除要求の管理や、個人情報の販売をオプトアウトするための消費者要求の管理など、Adobe Advertising製品およびサービスの使用に適用される CCPA に基づく義務を果たすためのサポートを提供します。

このドキュメントでは、Adobe AdvertisingDemand Side Platform(DSP) が、CCPA で定義される「個人情報の販売」の「オプトアウト」を消費者がサポートする方法について説明します。 Adobe Advertisingに販売オプトアウトリクエストを伝える方法や、組織の販売オプトアウトリクエストのレポートを取得する方法に関する情報が含まれています。

詳しくは、 [!DNL Advertising Search, Social, & Commerce];Advertising Creative;および [!DNL Advertising DCO] 消費者の個人情報のアクセスおよび削除権をサポートします。詳しくは、 [カリフォルニア州消費者プライバシー法に対するAdobe広告のサポート：消費者データのアクセスと削除のサポート](/help/privacy/ccpa/ccpa-access-delete.md).

CCPA のAdobeプライバシーサービスについて詳しくは、 [Adobeプライバシーセンター](https://www.adobe.com/privacy/ccpa.html).

## 消費者のオプトアウトオブセールのリクエストについてAdobe Advertisingに伝える

次のいずれかを使用して、消費者のオプトアウトオブセールのリクエストを伝えることができます。

* Advertising DSPで作成された CCPA オプトアウトオブセールセグメント
* Adobe Experience Platform Privacy Service API

### メソッド 1:を使用した CCPA オプトアウトオブセールの通知 [!UICONTROL CCPA Opt-Out-of-Sale] Advertising DSPのセグメント

>[!NOTE]
>
>ユーザーは、無期限に CCPA オプトアウトオブセールセグメントに残ります。

1. Advertising DSP( ) で広告主のアカウントにログインします。 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [CCPA オプトアウトオブセールセグメントを作成し、セグメントピクセルを実装してオプトアウトリクエストを取得する](/help/dsp/audiences/ccpa-opt-out-segment-create.md).

### 方法 2:Adobe Experience Platform Privacy Service API を使用した CCPA オプトアウトオブセールの通信

*広告主がAdobe Experience Cloud組織 ID のみを割り当てた*

1. JavaScript ライブラリをデプロイして、顧客の Cookie を取得します。 同じライブラリ `AdobePrivacy.js`は、すべてのAdobe Experience Cloudソリューションで使用されます。

   >[!IMPORTANT]
   >
   >一部のAdobe Experience Cloudソリューションへのリクエストには JavaScript ライブラリは必要ありませんが、Adobe Advertisingへのリクエストには必要です。

   ライブラリは、会社のプライバシーポータルなど、顧客が販売のオプトアウトリクエストを送信できる Web ページにデプロイする必要があります。 ライブラリを使用すると、AdobeCookie( 名前空間 ID: `gsurferID`) を使用して、Adobe Experience Platform Privacy Service API を介して販売のオプトアウトリクエストの一部としてこれらの id を送信できます。

1. Experience Cloud組織 ID を特定し、組織アカウントにリンクされていることを確認します。

   Experience Cloud組織 ID は、24 文字の英数字から成る文字列で、末尾に「@AdobeOrg」が付きます。 ほとんどのExperience Cloudのお客様には、組織 ID が割り当てられています。 マーケティングチームまたは内部Adobeシステム管理者が組織 ID を把握していない場合や、組織 ID がプロビジョニングされているかどうかが不明な場合は、Adobeカスタマーケア (gdprsupport@adobe.com) にお問い合わせください。 プライバシー API に要求を送信するには、組織 ID が、 `imsOrgID` 名前空間。

   >[!IMPORTANT]
   >
   >貴社のAdobe Advertising担当者に問い合わせて、組織のAdobe Advertisingアカウント ( [!DNL DSP] アカウントまたは広告主 [!DNL Search, Social, & Commerce] アカウントおよび [!DNL Creative] または [!DNL DCO] アカウント — がExperience Cloud組織 ID にリンクされている。

1. Adobe Experience Platform Privacy Service API を使用して、 [販売オプトアウトリクエストの送信](https://experienceleague.adobe.com/docs/experience-platform/privacy/api/consent.html) を使用して、消費者に代わってAdobe Advertisingを設定し、既存のリクエストのステータスを確認できます。

   販売オプトアウトリクエストの例については、以下の付録を参照してください。

   >[!NOTE]
   >
   ビジネスに複数のExperience Cloud組織 ID がある場合は、それぞれに対して個別の API リクエストを送信する必要があります。 ただし、複数のAdobe Advertisingサブソリューション ([!DNL Search, Social, & Commerce], [!DNL Creative], [!DNL DSP]、および [!DNL DCO]) の代わりに、サブソリューションごとに 1 つのアカウントを使用します。

これらの手順はすべて、Adobe Advertisingからサポートを受けるために必要です。 Adobe Experience Platform Privacy Serviceを使用して実行する必要があるこれらのタスクやその他の関連タスクの詳細、および必要な項目の見つけ方については、 [https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html](https://experienceleague.adobe.com/docs/experience-platform/privacy/home.html).

## 販売オプトアウトリクエストを送信した消費者のレポートの取得

Adobe Advertisingは、顧客がアカウントのオプトアウトオブセールのリクエストのために送信した ID の月別レポートを生成します。 各レポートは、GZIP 形式に圧縮されたタブ区切りテキストファイルとして使用できます。 このデータは、Advertising DSPで作成された CCPA オプトアウトオブセールセグメントと、Privacy ServiceAPI を介しておこなわれた送信を使用してキャプチャされたリクエストを統合します。 CCPA オプトアウトオブセールセグメントでキャプチャされたユーザー ID は、セグメントおよび広告主によって識別されます。 レポートは、前月の各月の最初に生成されます。 例えば、6 月の月別ユーザーリストは 7 月 1 日に公開されます。

過去 3 か月間に作成された月別レポートへのリンクは、Advertising DSP内から、または Advertising DSPを使用して取得できます [!DNL Trafficking API]. 各リンクは 7 日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

### メソッド 1:Advertising DSP内での消費者のオプトアウトオブセールレポートの取得

1. Advertising DSP( ) で広告主のアカウントにログインします。 [https://advertising.adobe.com/](https://advertising.adobe.com/).
1. [レポートの取得](/help/dsp/audiences/ccpa-opt-out-segment-report-retrieve.md).

### 方法 2:Advertising DSPを使用した消費者のオプトアウトオブセールレポートの取得 [!DNL Trafficking API]

この機能は、 [!DNL Trafficking API]. 詳しくは、 [!DNL Trafficking API] を参照してください。

組織が [!DNL Trafficking API] が詳細を知りたい場合は、Adobeアカウントチームにお問い合わせください。

## 付録：例 [!UICONTROL CCPA Opt-Out-of-Sale] Privacy ServiceAPI ユーザーのリクエスト

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
    "include": ["AdCloud"],
    "regulation": "ccpa"
}'
```

場所：

* `"namespace": "AdCloud"` は、 `AdCloud` Cookie 領域に含まれ、対応する値は、 `AdobePrivacy.js`
* `"include": ["AdCloud"]` リクエストがAdobe Advertisingに適用されることを示します
