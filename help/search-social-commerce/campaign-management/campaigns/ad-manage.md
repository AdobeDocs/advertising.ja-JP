---
title: 広告の管理
description: 広告を作成および管理する方法について説明します。
exl-id: 5ec410cd-9dff-41e6-9ecc-d6ceee84755e
feature: Search Campaign Management
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 広告の管理

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads]、[!DNL Yandex] および既存の [!DNL Baidu] アカウントのみ*

広告のステータスは、[!UICONTROL Campaigns] / [!UICONTROL Campaigns] / [!UICONTROL Ads] ビューで作成、編集および変更できます。

## 広告の作成

>[!NOTE]
>
>買い物キャンペーン用に製品広告を作成する必要はありません。広告ネットワークによって自動的に作成されます。 ただし、[!DNL Microsoft Advertising] のショッピングキャンペーンの場合は、オプションで、広告に含めるプロモーションラインを定義できます。

>[!TIP]
>
>一度に多くの広告を作成するには、[ コピー&amp;ペースト機能 ](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]** をクリックします。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループ、広告タイプを選択し、「**[!UICONTROL Continue]**」をクリックします。

   様々な広告タイプについて詳しくは、「[ 広告について ](ad-about.md) を参照してください。

1. [[!DNL Baidu]  テキスト広告 ](ad-settings-baidu-text.md)、[[!DNL Google Ads]  呼び出し専用広告 ](ad-settings-google-call.md)、[[!DNL Google Ads]  拡張動的検索広告 ](ad-settings-google-dsa.md) （Google Ads では現在「動的検索広告」と呼ばれています）、[[!DNL Google Ads]  レスポンシブ検索広告 ](ad-settings-google-rsa.md)、[[!DNL Microsoft Advertising]  拡張動的検索広告 ](ad-settings-microsoft-dsa.md)、[[!DNL Microsoft Advertising]  マルチメディア広告 ](ad-settings-microsoft-multimedia.md)、[[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md)、[[!DNL Microsoft Advertising]  レスポンシブ（オーディエンス）広告 ](ad-settings-microsoft-responsive.md)、[[!DNL Microsoft Advertising]  レスポンシブ検索広告 ](ad-settings-microsoft-rsa.md) または [[!DNL Yandex]  テキスト広告 ](ad-settings-yandex-text.md) を入力します。

   >[!NOTE]
   >
   >（Adobe Advertising コンバージョントラッキングを使用したキャンペーン）アカウントまたはキャンペーンの設定でキーワードレベルでのみトラッキングが指定されている場合、検索、ソーシャル、Commerceでは広告のトラッキングが生成されません。

1. 「**[!UICONTROL Post]**」をクリックします。

1. （Adobe Advertising コンバージョントラッキングを使用したキャンペーンのショッピング広告。オプション）広告のクリックを追跡するには、[ トラッキング URL ツールを使用したトラッキング URL の生成 ](/help/search-social-commerce/tools/click-tracking-url-generate.md) を行い、アカウント、キャンペーン、商品グループの設定に手動で追加します。

## 広告設定の編集

>[!NOTE]
>
>* 次の広告タイプは *可変* です。つまり、広告コピーまたは画像を変更して、同じ広告 ID を保持できます。動的検索広告を除くすべての [!DNL Google Ads] 広告タイプと、拡張テキスト広告 [!DNL Microsoft Advertising] あります。
>* サポートされているその他の広告はすべて *不変* です。つまり、広告コピーまたは画像を変更すると、既存の広告が削除され、新しい広告が作成されます。 検索、ソーシャル、Commerceで最適化に必要なデータが十分に収集されるなか、新規広告のパフォーマンスが数週間と不安定になる可能性があります。
>* [!DNL Microsoft Advertising] の製品広告のプロモーションラインを除き、製品広告のコンテンツを編集することはできません。 ただし、広告を一時停止または削除することはできます。

>[!TIP]
>
>一度に大量のデータを編集するには、[ コピーと貼り付け機能 ](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [campaign バルクシート ](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md) を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]** をクリックします。

1. 次のいずれかの操作をおこないます。

   * （1 つの広告の設定を編集するには）広告のプレビューにカーソルを置き、![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ") をクリックします。

   * （1 つ以上の広告の設定を編集するには）次の手順を実行します。

      1. 各行の横にあるチェックボックスをオンにします。

         複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

      1. データ テーブルの上にあるツールバーで、[![ 編集 ](/help/search-social-commerce/assets/edit.png " 編集 ")] をクリックします。

1. [[!DNL Baidu]  テキスト広告 ](ad-settings-baidu-text.md)、[[!DNL Google Ads]  呼び出し専用広告 ](ad-settings-google-call.md)、[[!DNL Google Ads]  拡張動的検索広告 ](ad-settings-google-dsa.md) （Google Ads では現在「動的検索広告」と呼ばれています）、[[!DNL Google Ads]  レスポンシブ検索広告 ](ad-settings-google-rsa.md)、[[!DNL Microsoft Advertising]  拡張動的検索広告 ](ad-settings-microsoft-dsa.md)、[[!DNL Microsoft Advertising]  マルチメディア広告 ](ad-settings-microsoft-multimedia.md)、[[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md)、[[!DNL Microsoft Advertising]  レスポンシブ（オーディエンス）広告 ](ad-settings-microsoft-responsive.md)、[[!DNL Microsoft Advertising]  レスポンシブ検索広告 ](ad-settings-microsoft-rsa.md) または [[!DNL Yandex]  テキスト広告 ](ad-settings-yandex-text.md) の設定を変更します。

   複数の広告の場合、選択したすべての広告に共通するフィールドのみを編集でき、変更は選択したすべての広告に適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の通貨フィールドでは、既存の値を指定の値に変更したり、制限を設けて、指定の割合または金額で金額を増減させることができます。

1. データを保存します。

   * （単一の広告） **[!UICONTROL Post]** をクリックします。

   * （複数の広告） **[!UICONTROL Post Now]** をクリックします。

## 広告のステータスの変更

アクティブな広告を一時停止して、その広告への入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

また、アクティブな検索広告や一時停止した検索広告を削除することもできます。 削除された広告は広告ネットワークから削除されます。 これらは表示されたままですが、変更できません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]/[!UICONTROL Campaigns]/[!UICONTROL Campaigns]** をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]** をクリックします。

1. （任意）特定の広告を含めるようにリストをフィルタリングします。

1. ステータスを変更する各広告の横にあるチェックボックスを選択します。

   複数行の選択に関するヒントについては、「[ 複数行を選択 ](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md) を参照してください。

1. ツールバーの「ステータス」ボタンをクリックします。

   * 行をアクティブにするには、「![ アクティブ化 ](/help/search-social-commerce/assets/activate.png " アクティブ化 ")」をクリックします。

   * 行を一時停止するには、「![ 一時停止 ](/help/search-social-commerce/assets/pause.png " 一時停止 ")」をクリックします。

   * 行を削除するには、「![ その他 ")」をクリックし ](/help/search-social-commerce/assets/more.png " 「**[!UICONTROL Delete]**」を選択します。 確認メッセージで、「**[!UICONTROL Delete]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 広告について ](ad-about.md)
>* [[!DNL Baidu]  テキスト広告設定 ](ad-settings-baidu-text.md)
>* [[!DNL Google Ads]  呼び出し専用広告設定 ](ad-settings-google-call.md)
>* [[!DNL Google Ads]  拡張された動的検索広告設定 ](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  レスポンシブ検索広告設定 ](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising]  拡張された動的検索広告設定 ](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising]  マルチメディア広告設定 ](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising]  製品広告設定 ](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ（オーディエンス）広告設定 ](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ検索広告設定 ](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex]  テキスト広告設定 ](ad-settings-yandex-text.md)
