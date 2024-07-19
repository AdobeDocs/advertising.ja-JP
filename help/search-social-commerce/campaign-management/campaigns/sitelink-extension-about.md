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

*[!DNL Google Ads]と [!DNL Microsoft Advertising] のみ*

サイトリンクは、テキスト広告リスト内の追加のテキストリンクです。 サイトリンクを使用して、サイトの特定のページにユーザーを直接移動します。 広告ネットワークは、広告に対するサイトリンクの関連性に基づいて、広告と共に表示するサイトリンクを決定する。 オプションで、各サイトリンクの説明テキストを広告に含めることができます。 広告コピーがサイトリンクと関連性が高い場合、広告ネットワークは、サイトリンクを含むアカウント内の既存の広告からの広告コピーを自動的に表示する場合があります。 デスクトップ広告 [!DNL Google Ads] は 2～6 個のサイトリンクが表示され、モバイル広告では最大 4 個のサイトリンクが表示される場合があります。 説明を含む 2、4、6 個のサイトリンクが表示される [!DNL Microsoft Advertising]、説明を含まない 4～6 個のサイトリンクが表示される場合があります。

サイトリンクのテキストと設定（広告にサイトリンクを表示できる日付を含む）を、アカウントレベルで共有します。

## [!UICONTROL Sitelinks] ビューと [!UICONTROL Associations] ビュー

[!UICONTROL Campaigns]/[!UICONTROL Campaigns] の [!UICONTROL Extensions]/[!UICONTROL Sitelinks] ライブラリに、アカウントレベルのサイトリンクがすべて一覧表示され、そこで共有サイトリンクを作成および管理できます。 [[!DNL Google Ads]  アカウント ](https://help.ads.microsoft.com/#apex/3/en/52001) および [[!DNL Microsoft Advertising]  アカウント ](https://support.google.com/google-ads/answer/6372658) ごとの最大広告拡張機能の数については、広告ネットワークのヘルプを参照してください。 ライブラリ内のサイトリンクは、アカウントエンティティに割り当てるまで、広告で使用されません。

[!UICONTROL Extensions]/[!UICONTROL Associations] ビューでは、アカウントレベル（[!DNL Google Ads] のみ）、キャンペーンレベル、広告グループレベル（[!DNL Google Ads] のみ）のすべての広告に、可能な拡張機能として任意のサイトリンクを割り当てることができます。

## サイトリンクのパフォーマンスデータ

検索、ソーシャル、Commerceは、広告拡張機能のクリック数と、拡張機能が含まれている広告に関連付けられたキーワードへのコンバージョン結果をマップします。 検索、ソーシャル、Commerceでは、拡張機能レベルでのコストデータやクリックデータを利用できません。 ただし [[!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md) では、「リンクタイプ」列の値が `sl:<Sitelink text>` として表示された場合（sl:See Current Offers など）、トランザクションが（広告自体ではなく）サイトリンクから発生したかどうかを確認できます。

[!DNL Google Ads] と [!DNL Microsoft Advertising] では、[[!DNL Ad Extensions]] タブでコストとクリック データを表示できます。

>[!MORELIKETHIS]
>
>* [ 共有サイトリンク拡張機能の管理 ](sitelink-extension-manage.md)
>* [ 共有サイトリンク拡張機能のキャンペーンまたは広告グループへの関連付け ](sitelink-extension-associate.md)
