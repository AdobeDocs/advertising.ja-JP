---
title: オフラインのコンバージョンデータをアップロードしてコンバージョンを強化
description: ファーストパーティのオフラインコンバージョンデータをアップロードして、リードの強化コンバージョンおよび強化コンバージョンの  [!DNL Google Ads]  強化コンバージョンにマッピングする方法  [!DNL Microsoft Advertising]  説明します。
feature: Conversions
exl-id: 5c5dfbb8-3b17-4973-8012-fc7f0e97e33b
source-git-commit: eb7320fdddce4895a689c32ec6fb1e44cb8f2705
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# オフラインのコンバージョンデータをアップロードしてコンバージョンを強化

*[!DNL Google Ads]および [!DNL Microsoft Advertising] アカウントのみ*

ファーストパーティのオフラインコンバージョンデータ（ハッシュ化されたメールアドレスと電話番号を含む）をアップロードして、既存の [[!DNL Google Ads]  リードの拡張コンバージョン ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) および [[!DNL Microsoft Advertising]  拡張コンバージョン ](https://help.ads.microsoft.com/#apex/ads/en/60178) にマッピングできます。 アップロードされたすべてのデータは、リアルタイムで広告ネットワークに同期されます。

## 拡張コンバージョン用のデータをアップロード

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Conversions]** をクリックし、「**[!UICONTROL Upload]**」タブをクリックします。

1. 広告ネットワークを選択し、次にアカウントを選択します。

1. （オプション）すべての [ 必須データフィールド ](#enhanced-conversions-leads-data) を含むテンプレートを [!DNL Microsoft Excel] の形式でダウンロードするには、「**[!UICONTROL View Template]**」をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

   ファイルを編集してデータを含め、変更を保存し、次の手順でファイルをアップロードできます。

1. 「**[!UICONTROL Choose File]**」をクリックし、デバイスまたはネットワークからアップロードするファイルを選択します。

## アップロードしたファイルに必要なデータ {#enhanced-conversions-leads-data}

### テーブルの上のデータ

`Parameters:TimeZone=insert_timezone`

この場所、または各行の「[!UICONTROL Conversion Time]」列に、アカウントのタイムゾーンを入力します。 a\） （[!DNL Google Ads only]） [ サポートされているタイムゾーン ID 形式 ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) または b\）で、+または – で示される GMT オフセットと、4 桁の時間差（ニューヨークの場合は–0500、ベルリンの場合は+0100、グリニッジ標準時の場合は+0000 など）を使用します。

### [!DNL Google Ads] のテーブル列と値

| 列 | 説明 |
| ------ | ----------- |
| 電子メール | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 各行には、電子メール値または電話番号値を含める必要があります。 |
| 電話番号 | ユーザーの電話番号（SHA-256 アルゴリズムを使用してハッシュ化する必要があります）。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 各行には、電子メール値または電話番号値を含める必要があります。 |
| コンバージョン名 | （必須）変換アクションの名前。 |
| コンバージョン時間 | （必須）コンバージョンイベントが発生した時刻 [ サポートされている時間形式 ](https://support.google.com/google-ads/answer/7014069#prepare_data)。 アカウントのタイムゾーン ID をデータテーブルの上の `Parameters:TimeZone=insert_timezone`[ 行に含めない場合、a\）（サポートされているタイムゾーン ID 形式 ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) または b\）の GMT オフセット（+または – で示される）と 4 桁の時間差（ニューヨークの場合は–0500、ベルリンの場合は+0100、グリニッジ標準時の場合は+0000 など）を使用して各行のタイムゾーンを含めます。 |
| コンバージョン値 | （必須）数値のコンバージョン値。 |
| 換算通貨 | コンバージョンイベントの通貨コード。 |
| 広告ユーザーデータ | （欧州経済地域（EEA）または英国（UK）のユーザーに関連するデータに適用）広告パーソナライゼーション目的で [!DNL Google] ーザーにユーザーデータを送信する際にユーザーの同意が得られたかどうかを示します。 値には、`Granted`、`Denied` または\[null\] （`Unspecified` として [!DNL Google Ads] に送信）を含めることができます。 **メモ：** [!DNL Google Ads] では、現在、リードのエンハンスドコンバージョンに対する同意を実施していませんが、今後、実施する可能性があります。 |
| 広告Personalization | （欧州経済地域（EEA）または英国（UK）のユーザーに関連するデータに適用）広告目的で [!DNL Google] ーザーにユーザーデータを送信する際にユーザーの同意が得られたかどうかを示します。 値には、`Granted`、`Denied` または\[null\] （`Unspecified` として [!DNL Google Ads] に送信）を含めることができます。 **メモ：** [!DNL Google Ads] では、現在、リードのエンハンスドコンバージョンに対する同意を実施していませんが、今後、実施する可能性があります。 |

### [!DNL Microsoft Advertising] のテーブル列と値

テンプレートの使用方法の詳細については、[https://help.ads.microsoft.com/#apex/3/56852](https://help.ads.microsoft.com/#apex/3/56852) を参照してください。

| 列 | 説明 |
| ------ | ----------- |
| コンバージョン名 | （必須） コンバージョン目標の名前。 |
| コンバージョン時間 | （必須）コンバージョンイベントが発生した時刻。 アカウントのタイムゾーン ID をデータ表の上の `Parameters:TimeZone=insert_timezone` 行に含めない場合は、+または – で示される GMT オフセットと 4 桁の時間差（ニューヨークの場合は–0500、ベルリンの場合は+0100、グリニッジ標準時の場合は+0000 など）を使用して各行のタイムゾーンを含めます。 様々な都市のタイムゾーンのリストについては、[https://learn.microsoft.com/en-us/advertising/guides/time-zones](https://learn.microsoft.com/en-us/advertising/guides/time-zones) を参照してください。ただし、タイムゾーンリストの形式ではなく、ここで指定した形式を使用していることを確認してください。 |
| コンバージョン値 | （必須）数値のコンバージョン値。 |
| 換算通貨 | コンバージョンイベントの通貨コード。 |
| Microsoft クリック ID | 関連付けられた一意の [!DNL Microsoft] クリック識別子（MSCLKID）。 拡張オフラインコンバージョンの場合、このフィールドは空にできます。 |
| ハッシュ化されたメールアドレス | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 拡張オフラインコンバージョンでは、各行にハッシュ化されたメールアドレス値またはハッシュ化された電話番号値を含める必要があります。 |
| ハッシュ化された電話番号 | ユーザーの電話番号（SHA-256 アルゴリズムを使用してハッシュ化する必要があります）。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 拡張オフラインコンバージョンでは、各行にハッシュ化されたメールアドレス値またはハッシュ化された電話番号値を含める必要があります。 |

>[!MORELIKETHIS]
>
>* [ リードのコ  [!DNL Google Ads]  バージョンの実装と強化 ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [ 拡張オフラインコンバージョン  [!DNL Microsoft Advertising]  実装 ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-enhanced-conversions.md)
>* （[!DNL Google Ads only]） [ リードの拡張コンバージョン用のコ  [!DNL Google Ads]  バージョンアクションの作成 ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ 検索、ソーシャル、Commerceで追跡されるコンバージョン指標のへのアップロード  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
