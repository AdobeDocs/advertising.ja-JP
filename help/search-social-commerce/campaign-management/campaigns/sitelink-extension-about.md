---
title: sitelink の拡張について
description: サイトリンクの拡張について説明します。
exl-id: bf4ef112-7a9f-4e8a-8f04-06ed123c862a
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '347'
ht-degree: 0%

---

# sitelink の拡張について

*[!DNL Google Ads]および [!DNL Microsoft® Advertising] のみ*

サイトリンクは、テキスト広告リスト内の追加のテキストリンクです。 サイトリンクを使用して、ユーザーをサイト内の特定のページに直接移動させます。 広告ネットワークは、広告に対するサイトリンクの関連性に基づいて、広告と共に表示するサイトリンクを決定します。 オプションで、広告に含めることのできる各サイトリンクの説明テキストを含めることができます。 広告コピーがサイトリンクと非常に関連性の高い場合、広告ネットワークは、サイトリンクを含むアカウント内の既存の広告の広告コピーを自動的に表示することができます。 [!DNL Google Ads] は、デスクトップ広告では 2 ～ 6 個のサイトリンクを表示し、モバイル広告では最大 4 個のサイトリンクを表示できます。 [!DNL Microsoft® Advertising] には、2、4、6 個のサイトリンクと説明が表示され、4 ～ 6 個のサイトリンクと説明が表示されない場合があります。

共有サイトリンクのテキストと設定（広告と共にサイトリンクを表示できる日付など）をアカウントレベルで作成します。

## The [!UICONTROL Sitelinks] および [!UICONTROL Associations] ビュー

The [!UICONTROL Extensions] > [!UICONTROL Sitelinks] ライブラリ内 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] は、すべてのアカウントレベルのサイトリンクを一覧表示し、共有サイトリンクをそこで作成および管理できます。 広告ネットワークのヘルプを参照して、それぞれの広告の最大拡張数を確認してください [[!DNL Google Ads] アカウント](https://support.google.com/google-ads/answer/6372658) および [[!DNL Microsoft® Advertising] アカウント](https://help.ads.microsoft.com/#apex/3/en/52001). ライブラリ内のサイトリンクは、アカウントエンティティに割り当てるまで、広告で使用されません。

次から： [!UICONTROL Extensions] > [!UICONTROL Associations] を表示する場合は、任意のサイトリンクを、アカウントレベルですべての広告に可能な限り割り当てることができます ([!DNL Google Ads] （のみ）、キャンペーンレベル、または広告グループレベル ([!DNL Google Ads] のみ )。

## サイトリンクのパフォーマンスデータ

検索、Social、および Commerce は、広告拡張機能のクリック数と結果のコンバージョンを、拡張機能が含まれている広告に関連付けられたキーワードにマッピングします。 検索、ソーシャル、コマースで、拡張機能レベルのコストやクリックデータは使用できません。 ただし、では [の [!UICONTROL Transaction Report]](/help/search-social-commerce/reports/management/basic-advanced/transaction-report.md)の場合、「リンクタイプ」列の値が `sl:<Sitelink text>`sl:See Current Offers など。

In [!DNL Google Ads] および [!DNL Microsoft® Advertising]をクリックすると、 [!DNL Ad Extensions] タブをクリックします。

>[!MORELIKETHIS]
>
>* [共有サイトリンク拡張の管理](sitelink-extension-manage.md)
>* [キャンペーンまたは広告グループへの共有サイトリンク拡張の関連付け](sitelink-extension-associate.md)
