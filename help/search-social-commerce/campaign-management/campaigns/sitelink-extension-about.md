---
title: サイトリンク拡張機能について
description: サイトリンク拡張機能について説明します。
exl-id: c2d96440-62da-4b57-a98e-d7b94882d6c5
feature: Search Campaign Management
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# サイトリンク拡張機能について

*[!DNL Google Ads]および [!DNL Microsoft Advertising] のみ*

サイトリンクは、テキスト広告リスト内の追加のテキストリンクです。 サイトリンクを使用して、サイトの特定のページにユーザーを直接移動します。 広告ネットワークは、広告に対するサイトリンクの関連性に基づいて、広告と共に表示するサイトリンクを決定する。 オプションで、各サイトリンクの説明テキストを広告に含めることができます。 広告コピーがサイトリンクと関連性が高い場合、広告ネットワークは、サイトリンクを含むアカウント内の既存の広告からの広告コピーを自動的に表示する場合があります。 [!DNL Google Ads] の 5 月には、デスクトップ広告に 2～6 個のサイトリンク、モバイル広告に最大 4 個のサイトリンクが表示されます。 [!DNL Microsoft Advertising] は、説明を含む 2、4、6 個のサイトリンク、または説明を含まない 4～6 個のサイトリンクを表示できます。

サイトリンクのテキストと設定（広告にサイトリンクを表示できる日付を含む）を、アカウントレベルで共有します。

## この [!UICONTROL Sitelinks] および [!UICONTROL Associations] 表示

この [!UICONTROL Extensions] > [!UICONTROL Sitelinks] のライブラリ [!UICONTROL Campaigns] > [!UICONTROL Campaigns] アカウントレベルのサイトリンクがすべて一覧表示され、そこで共有サイトリンクを作成および管理できます。 ごとの最大広告拡張機能の数については、広告ネットワークのヘルプを参照してください [[!DNL Google Ads] アカウント](https://support.google.com/google-ads/answer/6372658) および per [[!DNL Microsoft Advertising] アカウント](https://help.ads.microsoft.com/#apex/3/en/52001). ライブラリ内のサイトリンクは、アカウントエンティティに割り当てるまで、広告で使用されません。

から [!UICONTROL Extensions] > [!UICONTROL Associations] 表示し、アカウントレベルですべての広告に、可能な拡張機能として任意のサイトリンクを割り当てることができます（[!DNL Google Ads] のみ）、キャンペーンレベルまたは広告グループレベル（[!DNL Google Ads] のみ）。

## サイトリンクのパフォーマンスデータ

検索、ソーシャル、Commerceは、広告拡張機能のクリック数と、拡張機能が含まれている広告に関連付けられたキーワードへのコンバージョン結果をマップします。 検索、ソーシャル、Commerceでは、拡張機能レベルでのコストデータやクリックデータを利用できません。 ただし、 [この [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)リンクタイプ列の値が次のようにリストされている場合、トランザクションが（広告自体ではなく）サイトリンクから生じたかどうかを確認できます `sl:<Sitelink text>`sl:See Current Offers など。

対象： [!DNL Google Ads] および [!DNL Microsoft Advertising]でコストとクリックデータを確認できます [!DNL Ad Extensions] タブ。

>[!MORELIKETHIS]
>
>* [共有サイトリンク拡張機能の管理](sitelink-extension-manage.md)
>* [共有サイトリンク拡張機能のキャンペーンまたは広告グループへの関連付け](sitelink-extension-associate.md)
