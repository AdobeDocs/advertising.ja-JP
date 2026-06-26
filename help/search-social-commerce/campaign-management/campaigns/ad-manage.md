---
title: 広告を管理
description: 広告の作成と管理方法を説明します。
exl-id: 5ec410cd-9dff-41e6-9ecc-d6ceee84755e
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/qH3BE5BwU8614rZdk-tKqvtw9cqY1uK0Z3zOUh0QRv8
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 743
ht-degree: 0%

---

# 広告を管理

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]および既存の[!DNL Baidu] アカウントのみ*

広告のステータスは、[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] ビューから作成、編集、変更できます。

## 広告の作成

>[!NOTE]
>
>ショッピング施策で商品広告を作成する必要はありません。広告ネットワークが自動的に作成します。 ただし、[!DNL Microsoft Advertising]件のショッピングキャンペーンの場合は、オプションで広告に含めるプロモーション行を定義できます。

>[!TIP]
>
>一度に多くの広告を作成するには、[&#x200B; コピー&amp;ペースト機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md)または[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. 広告ネットワーク、アカウント、キャンペーン、広告グループ、広告タイプを選択し、**[!UICONTROL Continue]**&#x200B;をクリックします。

   様々な広告タイプについて詳しくは、「[広告について](ad-about.md)」を参照してください。

1. [[!DNL Baidu] text ad](ad-settings-baidu-text.md)、[[!DNL Google Ads] 通話専用ad](ad-settings-google-call.md)、[[!DNL Google Ads] 拡張dynamic search ad](ad-settings-google-dsa.md) （現在はGoogle Adsで「dynamic search ad」と呼ばれています）、[[!DNL Google Ads] responsive search ad](ad-settings-google-rsa.md)、[[!DNL Microsoft Advertising] 拡張dynamic search ad](ad-settings-microsoft-dsa.md)、[[!DNL Microsoft Advertising] multimedia ad](ad-settings-microsoft-multimedia.md)、[[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md)、[[!DNL Microsoft Advertising] responsive （audience） ad](ad-settings-microsoft-responsive.md)、[[!DNL Microsoft Advertising] responsive search ad](ad-settings-microsoft-rsa.md)、または[[!DNL Yandex] text ad](ad-settings-yandex-text.md)設定を入力します。

   >[!NOTE]
   >
   >（Adobe Advertising コンバージョントラッキングを使用したキャンペーン）アカウントまたはキャンペーンの設定がキーワードレベルでのみトラッキングを指定する場合、Search, Social, &amp; Commerceでは広告のトラッキングが生成されません。

1. **[!UICONTROL Post]**&#x200B;をクリックします。

1. （Adobe Advertising コンバージョントラッキングを使用したキャンペーンでのショッピング広告。オプション）広告のクリックをトラッキングするには、[&#x200B; トラッキング URL ツールを使用してトラッキング URLを生成し](/help/search-social-commerce/tools/click-tracking-url-generate.md)、アカウント、キャンペーン、または商品グループの設定に手動で追加します。

## 広告設定の編集

>[!NOTE]
>
>* 次の広告タイプは&#x200B;*可変*&#x200B;です。つまり、広告のコピーまたは画像を変更し、同じ広告IDを保持できます。動的検索広告を除くすべての[!DNL Google Ads]広告タイプ、および[!DNL Microsoft Advertising]拡張テキスト広告です。
>* サポートされているその他の広告はすべて&#x200B;*変更不可*&#x200B;です。つまり、広告コピーまたは画像を変更すると、既存の広告が削除され、新しい広告が作成されます。 Search, Social, &amp; Commerceで最適化に十分なデータを収集しながら、新しい広告のパフォーマンスは数週間にわたって不安定になる可能性があります。
>* 製品広告のコンテンツは、[!DNL Microsoft Advertising]個の製品広告のプロモーションラインを除き、編集できません。 ただし、広告を一時停止または削除することはできます。

>[!TIP]
>
>大量のデータを一度に編集するには、[&#x200B; コピー&amp;ペースト機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md)または[&#x200B; キャンペーンのバルクシート &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md)を使用します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * （1つの広告の設定を編集するには）広告プレビューの上にカーソルを置き、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

   * （1つ以上の広告の設定を編集するには）次の操作を行います。

      1. 各行の横にあるチェックボックスをオンにします。

         複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

      1. データテーブルの上にあるツールバーで、![編集](/help/search-social-commerce/assets/edit.png "編集")をクリックします。

1. [[!DNL Baidu] text ad](ad-settings-baidu-text.md)、[[!DNL Google Ads] 通話専用ad](ad-settings-google-call.md)、[[!DNL Google Ads] 拡張dynamic search ad](ad-settings-google-dsa.md) （現在はGoogle Adsで「dynamic search ad」と呼ばれています）、[[!DNL Google Ads] responsive search ad](ad-settings-google-rsa.md)、[[!DNL Microsoft Advertising] 拡張dynamic search ad](ad-settings-microsoft-dsa.md)、[[!DNL Microsoft Advertising] multimedia ad](ad-settings-microsoft-multimedia.md)、[[!DNL Microsoft Advertising] product ad](ad-settings-microsoft-product.md)、[[!DNL Microsoft Advertising] responsive （audience） ad](ad-settings-microsoft-responsive.md)、[[!DNL Microsoft Advertising] responsive search ad](ad-settings-microsoft-rsa.md)、または[[!DNL Yandex] text ad](ad-settings-yandex-text.md)設定を編集します。

   複数の広告の場合、選択したすべての広告に共通するフィールドのみを編集でき、変更は選択したすべての広告に適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、指定した接頭辞を各値の先頭に追加したり、各値の末尾に接尾辞を追加したりできます。 一部の金銭的なフィールドでは、既存の値を指定した値に変更したり、指定した割合または金額を増減したり、制限を設けることができます。

1. データを保存します。

   * （シングル広告）「**[!UICONTROL Post]**」をクリックします。

   * （複数の広告）「**[!UICONTROL Post Now]**」をクリックします。

## 広告のステータスの変更

アクティブな広告を一時停止して、入札を無効にすることができます。 後でステータスをアクティブに戻すことで、入札を再開できます。

アクティブまたは一時停止した検索広告を削除することもできます。 削除された広告は、広告ネットワークから削除されます。 これらは引き続き表示されますが、変更することはできません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**&#x200B;をクリックします。 サブメニューで、**[!UICONTROL Live]>[!UICONTROL Ads]**&#x200B;をクリックします。

1. （オプション）リストをフィルタリングして、特定の広告を含めます。

1. ステータスを変更する各広告の横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. ツールバーで、ステータスボタンをクリックします。

   * 行をアクティブ化するには、![&#x200B; アクティブ化](/help/search-social-commerce/assets/activate.png " アクティブ化")をクリックします。

   * 行を一時停止するには、![一時停止](/help/search-social-commerce/assets/pause.png "一時停止")をクリックします。

   * 行を削除するには、![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Delete]**&#x200B;を選択します。 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [広告について](ad-about.md)
>* [[!DNL Baidu]  テキスト広告設定](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] 呼び出し専用の広告設定](ad-settings-google-call.md)
>* [[!DNL Google Ads] 動的検索広告設定を拡張](ad-settings-google-dsa.md)
>* [[!DNL Google Ads]  レスポンシブ検索の広告設定](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] 動的検索広告設定を拡張](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising]  マルチメディア広告設定](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 製品広告設定](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ （オーディエンス）広告の設定](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising]  レスポンシブ検索の広告設定](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex]  テキスト広告設定](ad-settings-yandex-text.md)
