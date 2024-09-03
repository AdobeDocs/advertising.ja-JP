---
title: オフラインのコンバージョンデータをアップロードしてコンバージョンを強化
description: ファーストパーティのオフラインコンバージョンデータをアップロードして、リードの強化コンバージョンにマッピングする方法  [!DNL Google Ads]  説明します。
feature: Conversions
source-git-commit: c3cb1549adeb7b621c1b426c53da9bb09eddcbdc
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# オフラインのコンバージョンデータをアップロードしてコンバージョンを強化

*[!DNL Google Ads]アカウントのみ*

<!-- Tweak metadata title/description and heading -->

ハッシュ化されたメールアドレスと電話番号を含むファーストパーティのオフラインコンバージョンデータをアップロードして、既存の [[!DNL Google Ads]  リードの拡張コンバージョン ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md) にマッピングできます。 アップロードされたすべてのデータは、リアルタイムで [!DNL Google Ads] に同期されます。

## リードのコンバージョン [!DNL Google Ads] 強化するためにデータをアップロード

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Admin]/[!UICONTROL Conversions]** をクリックし、「**[!UICONTROL Upload]**」タブをクリックします。

1. 広告ネットワークを選択し、次にアカウントを選択します。

1. （オプション）すべての [ 必須データフィールド ](#enhanced-conversions-leads-data) を含むテンプレートを [!DNL Microsoft Excel] の形式でダウンロードするには、「**[!UICONTROL View Template]**」をクリックし、ブラウザーの通常の手順に従ってファイルをダウンロードします。

   ファイルを編集してデータを含め、変更を保存し、次の手順でファイルをアップロードできます。

1. 「**[!UICONTROL Choose File]**」をクリックし、デバイスまたはネットワークからアップロードするファイルを選択します。

## アップロードしたファイルに必要なデータ {#enhanced-conversions-leads-data}

### テーブルの上のデータ

`Parameters:TimeZone=insert_timezone`

この場所、または各行の「[!UICONTROL Conversion Time]」列に、アカウントのタイムゾーンを入力します。 a） [ サポートされているタイムゾーン ID 形式 ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) または b） GMT オフセット（+または – で示される）と 4 桁の時間差（ニューヨークの場合は–0500 など）を使用します。

### テーブルの列と値

| 列 | 説明 |
| ------ | ----------- |
| 電子メール | ユーザーのメールアドレス。SHA-256 アルゴリズムを使用してハッシュ化する必要があります。 各行には、電子メール値または電話番号値を含める必要があります。 |
| 電話番号 | ユーザーの電話番号（SHA-256 アルゴリズムを使用してハッシュ化する必要があります）。 国コードを含める必要があり、ダッシュやその他の記号を含めることができます。 各行には、電子メール値または電話番号値を含める必要があります。 |
| コンバージョン名 | （必須）変換アクションの名前。 |
| コンバージョン時間 | （必須）コンバージョンイベントが発生した時刻 [ サポートされている時間形式 ](https://support.google.com/google-ads/answer/7014069#prepare_data)。 アカウントのタイムゾーン ID をデータテーブルの上の `Parameters:TimeZone=insert_timezone` 行に含めない場合、a）（サポートされているタイムゾーン ID 形式 ](https://developers.google.com/google-ads/api/data/codes-formats#timezone_ids) または b） [+または – で示される GMT オフセット、および 4 桁の時間差（ニューヨークの場合は–0500 など）を使用して各行のタイムゾーンを含めます。 |
| コンバージョン値 | （必須）数値のコンバージョン値。 |
| 換算通貨 | コンバージョンイベントの通貨コード。 |
| 広告ユーザーデータ | （欧州経済地域（EEA）または英国（UK）のユーザーに関連するデータに適用）広告パーソナライゼーション目的で [!DNL Google] ーザーにユーザーデータを送信する際にユーザーの同意が得られたかどうかを示します。 値には、`Granted`、`Denied` または\[null\] （`Unspecified` として [!DNL Google Ads] に送信）を含めることができます。 **メモ：** [!DNL Google Ads] では、現在、リードのエンハンスドコンバージョンに対する同意を実施していませんが、今後、実施する可能性があります。 |
| 広告Personalization | （欧州経済地域（EEA）または英国（UK）のユーザーに関連するデータに適用）広告目的で [!DNL Google] ーザーにユーザーデータを送信する際にユーザーの同意が得られたかどうかを示します。 値には、`Granted`、`Denied` または\[null\] （`Unspecified` として [!DNL Google Ads] に送信）を含めることができます。 **メモ：** [!DNL Google Ads] では、現在、リードのエンハンスドコンバージョンに対する同意を実施していませんが、今後、実施する可能性があります。 |

>[!MORELIKETHIS]
>
>* [ リードの拡張コンバージョン用  [!DNL Google Ads]  コンバージョンアクションの作成 ](/help/search-social-commerce/admin/conversion-metrics/conversion-action-google.md)
>* [ リードのコ  [!DNL Google Ads]  バージョンの実装と強化 ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
>* [ 検索、ソーシャル、Commerceで追跡されるコンバージョン指標のへのアップロード  [!DNL Google Ads]](/help/search-social-commerce/tools/conversion-metrics-upload-to-google.md)
