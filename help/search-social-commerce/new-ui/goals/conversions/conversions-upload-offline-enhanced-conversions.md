---
title: （新しいUI）オフラインのコンバージョンデータをアップロードしてコンバージョンを強化
description: 1st パーティのオフラインのコンバージョンデータをアップロードして、リードのコンバージョンを [!DNL Google Ads] 強化し、コンバージョンを [!DNL Microsoft Advertising] 強化する方法を説明します。
feature: Conversions
feature_v2: id: e6916c1b-e939-4e0b-99f5-768e83e1e99fid: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 903
ht-degree: 0%

---

# オフラインのコンバージョンデータをアップロードしてコンバージョンを向上

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

ハッシュ化された電子メールアドレスや電話番号を含むファーストパーティのオフラインのコンバージョンデータをアップロードして、既存の[[!DNL Google Ads] 強化コンバージョンのリード ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)および[[!DNL Microsoft Advertising] 強化コンバージョン ](https://help.ads.microsoft.com/#apex/ads/en/60178)にマッピングできます。 アップロードされたすべてのデータは、広告ネットワークにリアルタイムで同期されます。

## （新しいUI） データをアップロードしてコンバージョンを強化

*Beta機能*

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Set up Conversion]**&#x200B;をクリックします。

1. データアップロード設定を指定します。

   1. 「[!UICONTROL Basic Details]」タブ：

      1. [!UICONTROL Setup Method] *[!UICONTROL Data Upload]*&#x200B;を選択します。

      1. [!UICONTROL Platform]: *[!UICONTROL Google]*&#x200B;または&#x200B;*[!UICONTROL Microsoft]*&#x200B;を選択します。

      1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. 「[!UICONTROL Configure]」タブ：

      1. （オプション）すべての[必須データフィールド ](#enhanced-conversions-leads-data)を[!DNL Microsoft Excel]形式で含むテンプレートをダウンロードするには、**[!UICONTROL Download Template]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

         データを含めるようにファイルを編集し、変更を保存してから、指定した広告ネットワークアカウントにファイルをアップロードできます。

      1. データをアップロードする広告ネットワークアカウントを選択します。

      1. [!UICONTROL Upload Conversion File] ボックスで、次のいずれかの操作を行います。

         * ファイルをボックスにドラッグします。

         * **[!UICONTROL Browse File]**&#x200B;をクリックし、デバイスまたはネットワークからアップロードするファイルを選択します。

   1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認します。

   1. **[!UICONTROL Upload]**&#x200B;をクリックします。

## （従来のUI）データをアップロードしてコンバージョンを強化

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックし、**[!UICONTROL Upload]** タブをクリックします。

1. 広告ネットワークを選択し、アカウントを選択します。

1. （オプション）すべての[必須データフィールド ](#enhanced-conversions-leads-data)を[!DNL Microsoft Excel]形式で含むテンプレートをダウンロードするには、**[!UICONTROL View Template]**&#x200B;をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

   ファイルを編集してデータを含め、変更を保存し、次の手順でファイルをアップロードできます。

1. **[!UICONTROL Choose File]**&#x200B;をクリックし、デバイスまたはネットワークからアップロードするファイルを選択します。

## アップロードされたファイルに必要なデータ {#enhanced-conversions-leads-data}

### テーブルの上のデータ

`Parameters:TimeZone=insert_timezone`

アカウントのタイムゾーンをこの場所または各行の「[!UICONTROL Conversion Time]」列に入力します。 「+」または「 – 」で示される[ サポートされているタイムゾーン ID形式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)またはb\）と4桁の時間差（ニューヨークの場合は–0500、ベルリンの場合は+0100、グリニッジ標準時の場合は+0000など）のa\）（[!DNL [!DNL Google Ads]のみ]）をGMT オフセットとして使用します。

### [!DNL Google Ads]のテーブル列と値

| 列 | 説明 |
| ------ | ----------- |
| [!UICONTROL Email] | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 各行には、[!UICONTROL Email]値または[!UICONTROL Phone Number]値を含める必要があります。 |
| [!UICONTROL Phone Number] | ユーザーの電話番号。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 各行には、[!UICONTROL Email]値または[!UICONTROL Phone Number]値を含める必要があります。 |
| [!UICONTROL Conversion Name] | （必須）変換アクションの名前。 |
| [!UICONTROL Conversion Time] | （必須）コンバージョンイベントが[ サポートされている時間形式](https://support.google.com/google-ads/answer/7014069#prepare_data)で発生した時間。 データテーブルの上の`Parameters:TimeZone=insert_timezone`行にアカウントのタイムゾーン IDを含めない場合は、「+」または「 – 」で示されるGMT オフセットを「[ サポートされているタイムゾーン ID形式](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids)」または「 – 」を使用して各行のタイムゾーンを含め、4桁の時間差（ニューヨークでは–0500、ベルリンでは+0100、グリニッジ平均時間では+000など）を指定します。 |
| [!UICONTROL Conversion Value] | （必須）数値の変換値。 |
| [!UICONTROL Conversion Currency] | コンバージョンイベントの通貨コード。 |
| [!UICONTROL Ad User Data] | （欧州経済地域（EEA）または英国（UK）のユーザーに関するデータに適用）広告パーソナライゼーション目的で[!DNL Google]にユーザーデータを送信するためにユーザーの同意が与えられたかどうかを示します。 値には、`Granted`、`Denied`または\[null\]が含まれます（これは[!DNL Google Ads]に`Unspecified`として送信されます）。 **注：** [!DNL Google Ads]は、現在、リードのコンバージョンを強化するための同意を適用していませんが、今後は適用される可能性があります。 |
| [!UICONTROL Ad Personalization] | （欧州経済地域（EEA）または英国（UK）のユーザーに関するデータに適用）広告目的で[!DNL Google]にユーザーデータを送信することにユーザーの同意が与えられたかどうかを示します。 値には、`Granted`、`Denied`または\[null\]が含まれます（これは[!DNL Google Ads]に`Unspecified`として送信されます）。 **注：** [!DNL Google Ads]は、現在、リードのコンバージョンを強化するための同意を適用していませんが、今後は適用される可能性があります。 |

### [!DNL Microsoft Advertising]のテーブル列と値

データのフォーマットとハッシュ化について詳しくは、[拡張コンバージョン ](https://help.ads.microsoft.com/#apex/ads/60178)に関する[!DNL Microsoft Ads] ドキュメントを参照してください。

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
>* [実装 [!DNL Google Ads]  リードの拡張コンバージョン ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [実装 [!DNL Microsoft Advertising]  オフライン コンバージョンの強化](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* [ リードの強化されたコンバージョン  [!DNL Google Ads] のコンバージョンアクションを作成](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [検索、ソーシャル、Commerceで追跡したコンバージョン指標を [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)にアップロード
