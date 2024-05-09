---
title: レポート宛先設定
description: 宛先タイプ別に、レポート宛先に必要な詳細を確認します。
feature: DSP Custom Reports
exl-id: 1437ceea-111a-4c2e-a439-037b3a35865c
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 0%

---

# レポート宛先設定

メール以外のレポート宛先に必要な詳細は、宛先タイプによって異なります。

>[!NOTE]
>
> また、保存されたレポートの宛先を必要としないカスタムレポートを、メール受信者に配信することもできます。 レポート設定内では、保存した宛先の代わりに、メール受信者を指定できます。

## [!UICONTROL S3]

**[!UICONTROL Name]:** 宛先を識別するのに役立つ名前。

**[!UICONTROL S3 Bucket URL]:** 上のフォルダーのフルパス [!DNL Amazon Simple Storage Service] （S3）レポートのアップロード先のバケット。 例： `s3://dsp_account/reports`

**[!UICONTROL Access Key ID]:** へのアクセスキー ID （[!DNL Amazon S3]） バケット（提供者 [!DNL Amazon]）に設定します。

**[!UICONTROL Secret Access Key]:** の秘密アクセスキー（[!DNL Amazon S3]） バケット（提供者 [!DNL Amazon]）に設定します。

## [!UICONTROL FTP]

**[!UICONTROL Name]:** 宛先を識別するのに役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトはです *[!UICONTROL 21]*.

**[!UICONTROL Username]:** サーバーにログインするためのユーザー名。

**[!UICONTROL Password]:** サーバーにログインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

## [!UICONTROL SFTP]

**[!UICONTROL Name]:** 宛先を識別するのに役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトはです *[!UICONTROL 21]*.

**[!UICONTROL Username]:** サーバーにログインするためのユーザー名。

**[!UICONTROL Password]:** サーバーにログインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

## [!UICONTROL FTP SSL]

**[!UICONTROL Name]:** 宛先を識別するのに役立つ名前。

**[!UICONTROL Server]:** サーバーのホスト名。

**[!UICONTROL Port]:** サーバーで使用するポート番号。 デフォルトはです *[!UICONTROL 21]*.

**[!UICONTROL Username]:** サーバーにログインするためのユーザー名。

**[!UICONTROL Password]:** サーバーにログインするためのパスワード。

**[!UICONTROL Path (Optional)]:** ファイルのアップロード先のサーバーパス。

>[!MORELIKETHIS]
>
>* [について [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
>* [を作成 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-create.md)
>* [を編集 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-edit.md)
>* [を削除 [!UICONTROL Report Destination]](/help/dsp/reports/report-destinations/report-destination-delete.md)
