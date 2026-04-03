---
title: レポート宛先の設定
description: 宛先タイプ別に、レポート宛先に必要な詳細を確認します。
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
TQID: https://experienceleague.adobe.com/VB5UY9vm147LQJMKKyGOlhZdNcq6mVDYTT0Ef4RcwVs
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: cc3b7f3c-58f0-4ba4-b808-391002930fd4id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 267
ht-degree: 0%

---

# レポート宛先の設定

メール以外のレポートの宛先に必要な詳細は、宛先タイプによって異なります。

>[!NOTE]
>
> また、カスタムレポートをメール受信者に配信することもできます。メール受信者は、保存されたレポート宛先を必要としません。 レポート設定内で、保存先の代わりにメール受信者を指定できます。

## [!UICONTROL S3]

**[!UICONTROL Name]:**&#x200B;宛先の特定に役立つ名前。

**[!UICONTROL S3 Bucket URL]:** レポートのアップロード先となる[!DNL Amazon Simple Storage Service] （S3） バケット上のフォルダーへの完全パス。 例：`s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** （[!DNL Amazon S3]） バケットへのアクセス キーID （[!DNL Amazon]から提供）。

**[!UICONTROL Secret Access Key]:** （[!DNL Amazon S3]） バケットへの秘密アクセス キー（[!DNL Amazon]様から提供）。

## [!UICONTROL FTP]

**[!UICONTROL Name]:**&#x200B;宛先の特定に役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトは&#x200B;*[!UICONTROL 21]*&#x200B;です。

**[!UICONTROL Username]:** サーバーにサインインするユーザー名。

**[!UICONTROL Password]:** サーバーにサインインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

## [!UICONTROL SFTP]

**[!UICONTROL Name]:**&#x200B;宛先の特定に役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトは&#x200B;*[!UICONTROL 21]*&#x200B;です。

**[!UICONTROL Username]:** サーバーにサインインするユーザー名。

**[!UICONTROL Password]:** サーバーにサインインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:**&#x200B;宛先の特定に役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトは&#x200B;*[!UICONTROL 21]*&#x200B;です。

**[!UICONTROL Username]:** サーバーにサインインするユーザー名。

**[!UICONTROL Password]:** サーバーにサインインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

>[!MORELIKETHIS]
>
>* [ レポートの宛先について](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [ レポートの宛先を作成](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [[!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)を編集
>* [ レポートの宛先を削除](/help/dsp/reports/report-destinations/report-destination-delete.md)
