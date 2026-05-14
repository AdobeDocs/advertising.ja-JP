---
title: オフラインのコンバージョンデータをアップロードしてコンバージョンを向上
description: 1st パーティのオフラインのコンバージョンデータをアップロードして、リードのコンバージョンを [!DNL Google Ads] 強化し、コンバージョンを [!DNL Microsoft Advertising] 強化する方法を説明します。
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
TQID: https://experienceleague.adobe.com/Hfmc5VCw9682cYmOQIcoy1Yy6InkoSmE18qqILbD2oI
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ab69d6b27b86f6e4d9da6be3cd0245d6116469d3
workflow-type: tm+mt
source-wordcount: 792
ht-degree: 0%

---

# オフラインのコンバージョンデータをアップロードしてコンバージョンを向上

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

ハッシュ化された電子メールアドレスや電話番号を含むファーストパーティのオフラインのコンバージョンデータをアップロードして、既存の[[!DNL Google Ads] 強化コンバージョンのリード &#x200B;](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)および[[!DNL Microsoft Advertising] 強化コンバージョン &#x200B;](https://help.ads.microsoft.com/#apex/ads/en/60178)にマッピングできます。 アップロードされたすべてのデータは、広告ネットワークにリアルタイムで同期されます。

## データをアップロードしてコンバージョンを高める

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックし、**[!UICONTROL Upload]** タブをクリックします。

1. 広告ネットワークを選択し、アカウントを選択します。

1. （オプション）すべての[必須データフィールド &#x200B;](#enhanced-conversions-leads-data)を[!DNL Microsoft Excel]形式で含むテンプレートをダウンロードするには、**[!UICONTROL View Template]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

   ファイルを編集してデータを含め、変更を保存し、次の手順でファイルをアップロードできます。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワークからアップロードするファイルを選択します。

## アップロードされたファイルに必要なデータ {#enhanced-conversions-leads-data}

### テーブルの上のデータ

`Parameters:TimeZone=insert_timezone`

アカウントのタイムゾーンをこの場所または各行の「[!UICONTROL Conversion Time]」列に入力します。 「+」または「 – 」で示される[&#x200B; サポートされているタイムゾーン ID形式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)またはb\）と4桁の時間差（ニューヨークの場合は–0500、ベルリンの場合は+0100、グリニッジ標準時の場合は+0000など）のa\）（[!DNL [!DNL Google Ads]のみ]）をGMT オフセットとして使用します。

### [!DNL Google Ads]のテーブル列と値

| 列 | 説明 |
| ------ | ----------- |
| メール | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 各行には、電子メールの値または電話番号の値を含める必要があります。 |
| 電話番号 | ユーザーの電話番号。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 各行には、電子メールの値または電話番号の値を含める必要があります。 |
| コンバージョン名 | （必須）変換アクションの名前。 |
| コンバージョン時間 | （必須）コンバージョンイベントが[&#x200B; サポートされている時間形式](https://support.google.com/google-ads/answer/7014069#prepare_data)で発生した時間。 データテーブルの上の`Parameters:TimeZone=insert_timezone`行にアカウントのタイムゾーン IDを含めない場合は、「+」または「 – 」で示されるGMT オフセットを「[&#x200B; サポートされているタイムゾーン ID形式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)」または「 – 」を使用して各行のタイムゾーンを含め、4桁の時間差（ニューヨークでは–0500、ベルリンでは+0100、グリニッジ平均時間では+000など）を指定します。 |
| コンバージョン値 | （必須）数値の変換値。 |
| コンバージョン通貨 | コンバージョンイベントの通貨コード。 |
| 広告ユーザーデータ | （欧州経済地域（EEA）または英国（UK）のユーザーに関するデータに適用）広告パーソナライゼーション目的で[!DNL Google]にユーザーデータを送信するためにユーザーの同意が与えられたかどうかを示します。 値には、`Granted`、`Denied`または\[null\]が含まれます（これは[!DNL Google Ads]に`Unspecified`として送信されます）。 **注：** [!DNL Google Ads]は、現在、リードのコンバージョンを強化するための同意を適用していませんが、今後は適用される可能性があります。 |
| Ad Personalization | （欧州経済地域（EEA）または英国（UK）のユーザーに関するデータに適用）広告目的で[!DNL Google]にユーザーデータを送信することにユーザーの同意が与えられたかどうかを示します。 値には、`Granted`、`Denied`または\[null\]が含まれます（これは[!DNL Google Ads]に`Unspecified`として送信されます）。 **注：** [!DNL Google Ads]は、現在、リードのコンバージョンを強化するための同意を適用していませんが、今後は適用される可能性があります。 |

### [!DNL Microsoft Advertising]のテーブル列と値

データのフォーマットとハッシュ化について詳しくは、[拡張コンバージョン &#x200B;](https://help.ads.microsoft.com/#apex/ads/60178)に関する[!DNL Microsoft Ads] ドキュメントを参照してください。

| 列 | 説明 |
| ------ | ----------- |
| [!UICONTROL Email] | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 各行には、[!UICONTROL Email]値または[!UICONTROL Phone Number]値を含める必要があります。 |
| [!UICONTROL Phone Number] | ユーザーの電話番号。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 拡張オフライン コンバージョンの場合、各行には[!UICONTROL Email]値または[!UICONTROL Phone Number]値を含める必要があります。 |
| [!UICONTROL Conversion Name] | （必須）変換アクションの名前。 |
| [!UICONTROL Conversion Time] | （必須）コンバージョンイベントが発生した時間。 データテーブルの上の`Parameters:TimeZone=insert_timezone`行にアカウントのタイムゾーン IDを含めない場合は、+または – で示されるGMT オフセットを使用して各行のタイムゾーンと4桁の時間差を含めます（例えば、ニューヨークでは–0500、ベルリンでは+0100、グリニッジ標準時では+000）。 様々な都市のタイムゾーンのリストについては、[https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones)を参照してください。ただし、タイムゾーンリストの形式ではなく、ここで指定した形式を使用してください。 |
| [!UICONTROL Conversion Value] | （必須）数値の変換値。 |
| [!UICONTROL Conversion Currency] | コンバージョンイベントの通貨コード。 |

>[!MORELIKETHIS]
>
>* [実装 [!DNL Google Ads]  リードの拡張コンバージョン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [実装 [!DNL Microsoft Advertising]  オフライン コンバージョンの強化](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [&#x200B; リードの強化されたコンバージョン  [!DNL Google Ads] のコンバージョンアクションを作成](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [検索、ソーシャル、Commerceで追跡したコンバージョン指標を [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)にアップロード
