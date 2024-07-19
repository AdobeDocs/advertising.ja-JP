---
title: 基本レポートまたは詳細レポートの生成
description: カスタマイズした基本レポートや詳細レポートを生成する方法について説明します。
exl-id: 529a35f5-517f-4bde-b752-c0afc6346f4b
feature: Search Reports, Search Basic Reports, Search Advanced Reports
source-git-commit: e16bc62127a708de8f4deb1eddfa53a14405cbc2
workflow-type: tm+mt
source-wordcount: '391'
ht-degree: 0%

---

# 基本レポートまたは詳細レポートの生成

1. メインメニューで、**[!UICONTROL Search]/[!UICONTROL Insights & Reports]/[!UICONTROL Reports]** をクリックします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Create Report]**] をクリックし、カーソルを **[!UICONTROL Basic Reports]** または **[!UICONTROL Advanced Reports]** に置いて [ レポートの種類 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md) をクリックします。

1. （オプション） [!UICONTROL Report Settings] ウィンドウで、デフォルト [ レポート設定 ](basic-advanced-report-settings.md) を変更します。

   1. （オプション）レポートおよびテンプレートのカスタム名を入力します（レポートをテンプレートとして保存する場合）。

   1. （オプション）レポート設定をテンプレートとして保存するには、**[!UICONTROL Save as template]** の横にあるチェックボックスを選択します。

   1. （オプション）「**[!UICONTROL Basic Settings]**」タブで、レポートのデフォルトの基本設定を使用または変更する既存のレポートテンプレートを選択します。

   1. （オプション） **[!UICONTROL Columns tab]** をクリックして、レポートのデフォルト列を変更します。

      デフォルトでは、レポート内のすべての通貨データは、米国ドルの形式（1,000.00 など）で表示されます。 値を正しい通貨形式（ただし、CSV および TSV 形式の通貨記号は除く）で表示するには、レポートに「[!UICONTROL Currency]」列を追加します。 異なる通貨を使用する勘定科目のデータがレポートに含まれる場合、通貨に関係なく、「[!UICONTROL Total]」の金額の値は列のすべての数値の合計になります。

   1. （オプション：[!UICONTROL Campaign Report]、[!UICONTROL Ad Group Report]、[!UICONTROL Ad Variation Report]、[!UICONTROL Keyword Report] および [!UICONTROL Label Classification Report] のみ）「**[!UICONTROL Classifications]**」タブをクリックし、特定のラベル分類のみを含めるようにレポート結果を制限します。

   1. （任意）「**[!UICONTROL Advanced Filters]**」タブをクリックして、デフォルトの詳細オプションを変更します。

   1. （任意）「**[!UICONTROL Attribution]**」タブをクリックして、デフォルトのアトリビューションルールを変更します。

   1. （任意）「**[!UICONTROL Scheduling and Delivery]**」タブをクリックして、デフォルトのスケジュールと配信オプションを変更します。

1. （オプションが使用可能な場合）レポートの最初の 50 行をプレビューするには、「**[!UICONTROL Preview]**」をクリックします。 完了したら、「**[!UICONTROL Back]**」をクリックしてレポート設定ページに戻ります。

   >[!NOTE]
   >
   >「プレビュー」ボタンは、[!UICONTROL Campaign Hourly Report]、[!UICONTROL Ad Variation Report]、[!UICONTROL Keyword Report]、[!UICONTROL Domain Referral Report] および [!UICONTROL Transaction Report] を除く、すべての基本レポートと詳細レポートで使用できます。

1. 「**[!UICONTROL Create]**」をクリックします。

レポートスケジュールを指定しなかった場合、レポートはすぐに実行されます。指定しなかった場合は、指定したスケジュールに従ってレポートが実行されます。 レポート名が [[!UICONTROL Latest Reports] ビューに追加され ](/help/search-social-commerce/reports/report-about.md) す。 レポートをテンプレートとして保存した場合は、[[!UICONTROL Templates] ビュー ](/help/search-social-commerce/reports/report-about.md) にも追加されます。 レポートが完成すると、ファイルを開いたり保存したりできます。テンプレートはすぐに使用できます。

通知用のメールアドレスを入力した場合、各受信者は、レポートに対して、ユーザーの [ 設定された通知設定 ](/help/search-social-commerce/notifications/notification-edit.md) に基づいて、レポートジョブが完了または失敗すると、通知を受け取ります。

>[!MORELIKETHIS]
>
>* [ 基本レポートと高度なレポートについて ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-about.md)
>* [ 基本および詳細レポートの設定 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-settings.md)
>* [ 基本レポートおよび高度なレポートのレポート列 ](/help/search-social-commerce/reports/management/basic-advanced/basic-advanced-report-columns.md)
>* [ 報告書の削除 ](/help/search-social-commerce/reports/management/report-delete.md)
