---
title: レポートへのFTP アクセス
description: 読み取り専用FTPの場所でレポートを受信する方法を説明します。
exl-id: eca9f033-5b1b-4afa-926b-b4c31e2dede3
feature: Search Reports
TQID: https://experienceleague.adobe.com/Dd72ha3yuVBLu-vCuBUFlc6lYeinKcIAu5agIco4zVY
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 435
ht-degree: 0%

---

# レポートへのFTP アクセス

必要に応じて、読み取り専用のFTPの場所でレポートを受信できます。この場所からファイルを取得して、追加の自動化プロセスを実行できます（例えば、別のプログラムでデータを解析する）。 [!UICONTROL Search Engine Account Report]およびすべての詳細レポートを除くすべての基本レポートは、ZIP ファイル拡張子を持つZIP TSV ファイル（デフォルト）またはCSV ファイルとしてFTPの場所に配信できます。 TSVまたはCSV ファイルヘッダーは含まれており、抑制できません。

レポートへのFTP アクセスには、指定したFTP アカウントへのアクセスが必要です。また、特定の命名規則とスケジュールを使用してレポートテンプレートを設定する必要があります。

## レポートにアクセスするためのFTP アカウントの設定

* レポートにアクセスするためのFTP アカウントを設定するには、Adobe アカウントチームにお問い合わせください。

  チームは、ユーザー名とパスワードを提供します。

## FTP配信用のレポートテンプレートの設定

指定したFTP ディレクトリでレポートを生成するには、次の命名規則とスケジュールを使用して[&#x200B; レポートテンプレート &#x200B;](templates/template-create.md)を作成します。

>[!NOTE]
>
>[!UICONTROL Search Engine Account Report]を除くすべての詳細レポートと基本レポートは、FTPの場所に配信できます。

1. レポートテンプレートで、テンプレート名の任意の場所に次の情報を含めます。

   * `FTP` （大文字）。

   * （オプション） 3つのシステムの日付のうち、括弧を含む大文字と小文字を区別する次の構文を使用する日付。

      * `[TODAY]` — レポートを実行した日付、時間、分を含めます。 これには正確な時間が含まれるため、同じテンプレートを1日に複数回実行できます。以前のレポートは上書きされません。

      * `[SDATE]` — レポート日付範囲の開始日を含めるには。

      * `[EDATE]` — レポート日付範囲の終了日を含めるには。

   * （オプション）デフォルトのTSV形式ではなくCSV形式でファイルを作成するには、`[CSV]` （大文字で囲み、角括弧で囲む）を使用します。

   例：`[TODAY]-Portfolio-FTP-[SDATE]-[EDATE]-[CSV]`は、202305051656-Portfolio-FTP-20230428-20110504.csvのようなファイルを作成します。

1. レポートを特定の時間に実行するようにスケジュール設定します。

   レポートは、完了後1時間以内にFTP アカウントに配信されます。

>[!NOTE]
>
>* 完成したレポートを電子メールで送信するには、レポートまたはテンプレートを生成するときに、すべての電子メール受信者のアドレスを入力するだけです。
>* レポートは、指定したスケジュールに従って実行され、完了してから1時間以内にFTP アカウントに配信されます。

## FTP リポジトリ内のレポートへのアクセス

レポートにアクセスするには、FTP アカウントのログイン（`amo<userID>rpt`、amo1234rptなど）を使用して、次のいずれかのFTP ホストに接続し、パスワードまたは秘密接続キーを設定します。

* 海外のお客様：`ftp3.adobe.net`
* 米国のお客様：`ftp5.adobe.net`

>[!NOTE]
>
>レポートリポジトリは読み取り専用で、15日ごとにパージされます。


>[!MORELIKETHIS]
>
>* [&#x200B; レポートテンプレートを作成](/help/search-social-commerce/reports/automation/templates/template-create.md)
