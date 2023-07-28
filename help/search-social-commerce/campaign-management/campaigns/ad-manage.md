---
title: 広告の管理
description: 広告の作成および管理方法について説明します。
exl-id: 9108bbfd-61e7-49fa-90ba-4eb276eb0897
feature: Search Campaign Management
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '745'
ht-degree: 0%

---

# 広告の管理

*[!DNL Baidu], [!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads]、および [!DNL Yandex] アカウントのみ*

広告のステータスは、 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] 表示。

## 広告の作成

>[!NOTE]
>
>買い物キャンペーン用の製品広告を作成する必要はありません。広告ネットワークによって自動的に作成されます。 の場合 [!DNL Microsoft Advertising] ただし、オプションで広告に含めるプロモーションラインを定義できます。

>[!TIP]
>
>一度に多数の広告を作成するには、 [コピーおよび貼り付け機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成").

1. 広告ネットワーク、アカウント、キャンペーン、広告グループおよび広告タイプを選択し、「 **[!UICONTROL Continue]**.

   様々な広告タイプについて詳しくは、[広告について](ad-about.md).&quot;

1. 次を入力します。 [[!DNL Baidu] テキスト広告](ad-settings-baidu-text.md), [[!DNL Google Ads] 呼び出し専用広告](ad-settings-google-call.md), [[!DNL Google Ads] 拡張された動的検索広告](ad-settings-google-dsa.md) (Google Ads では、現在は「動的検索広告」と呼ばれています )。 [[!DNL Google Ads] レスポンシブ検索広告](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] 拡張された動的検索広告](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] マルチメディア広告](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] 製品広告](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] レスポンシブ（オーディエンス）広告](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] レスポンシブ検索広告](ad-settings-microsoft-rsa.md)または [[!DNL Yandex] テキスト広告](ad-settings-yandex-text.md) 設定。

   >[!NOTE]
   >
   >(Adobe Advertisingコンバージョントラッキングを使用するキャンペーン ) アカウントまたはキャンペーン設定でキーワードレベルでのみトラッキングを指定した場合、検索、ソーシャル、コマースでは広告のトラッキングは生成されません。

1. クリック **[!UICONTROL Post]**.

1. (Adobe Advertisingコンバージョントラッキングを含むキャンペーンのショッピング広告。オプション ) 広告のクリックを追跡するには、 [トラッキング URL ツールを使用してトラッキング URL を生成します](/help/search-social-commerce/tools/click-tracking-url-generate.md)をクリックし、アカウント、キャンペーンまたは製品グループの設定に手動で追加します。

## 広告設定の編集

>[!NOTE]
>
>* 以下の広告タイプがあります *可変*：つまり、広告コピーまたは画像を変更して、同じ広告 ID を保持できます。すべて [!DNL Google Ads] 動的検索広告を除く広告のタイプ [!DNL Microsoft Advertising] 拡張テキスト広告。
>* その他のサポートされる広告は、 *不変*&#x200B;つまり、広告のコピーまたは画像を変更すると、既存の広告が削除され、新しい広告が作成されます。 新しい広告のパフォーマンスは、数週間の間、不安定な場合があります。一方、Search、Social、および Commerce は、入札を最適化するのに十分なデータを収集します。
>* 製品広告のコンテンツは、次のプロモーションラインを除いて編集できません： [!DNL Microsoft Advertising] 製品広告。 ただし、広告を一時停止または削除することはできます。

>[!TIP]
>
>大量のデータを一度に編集するには、 [コピーおよび貼り付け機能](/help/search-social-commerce/campaign-management/campaigns/copy-paste.md) または [キャンペーンバルクシート](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-about.md).

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. 次のいずれかの操作を行います。

   * （単一の広告の設定を編集するには）広告プレビューの上にカーソルを置き、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

   * （1 つ以上の広告の設定を編集するには）次の操作を行います。

      1. 各行の横にあるチェックボックスをオンにします。

         複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

      1. データテーブルの上にあるツールバーで、 ![編集](/help/search-social-commerce/assets/edit.png "編集").

1. を編集します。 [[!DNL Baidu] テキスト広告](ad-settings-baidu-text.md), [[!DNL Google Ads] 呼び出し専用広告](ad-settings-google-call.md), [[!DNL Google Ads] 拡張された動的検索広告](ad-settings-google-dsa.md) (Google Ads では、現在は「動的検索広告」と呼ばれています )。 [[!DNL Google Ads] レスポンシブ検索広告](ad-settings-google-rsa.md), [[!DNL Microsoft Advertising] 拡張された動的検索広告](ad-settings-microsoft-dsa.md), [[!DNL Microsoft Advertising] マルチメディア広告](ad-settings-microsoft-multimedia.md), [[!DNL Microsoft Advertising] 製品広告](ad-settings-microsoft-product.md), [[!DNL Microsoft Advertising] レスポンシブ（オーディエンス）広告](ad-settings-microsoft-responsive.md), [[!DNL Microsoft Advertising] レスポンシブ検索広告](ad-settings-microsoft-rsa.md)または [[!DNL Yandex] テキスト広告](ad-settings-yandex-text.md) 設定。

   複数の広告の場合、選択したすべての広告に共通するフィールドのみを編集でき、変更は選択したすべての広告に適用されます。 一部の英数字フィールドでは、既存の値を指定した値に変更したり、既存の文字列を指定した文字列に置き換えたり、各値の先頭に指定したプレフィックスを追加したり、各値の末尾にサフィックスを追加したりできます。 一部の金額フィールドでは、既存の値を指定した値に変更するか、制限を持つ指定した割合または金額で金額を増減させることができます。

1. データを保存します。

   * （単一の広告）クリック **[!UICONTROL Post]**.

   * （複数の広告）クリック **[!UICONTROL Post Now]**.

## 広告のステータスの変更

アクティブな広告を一時停止して、その広告に対する入札を無効にすることができます。 ステータスを「アクティブ」に戻すと、後で入札を再開できます。

また、アクティブな検索広告や一時停止した検索広告も削除できます。 削除された広告は広告ネットワークから削除されます。 まだ見えますが、変更はできません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]>[!UICONTROL Ads]**.

1. （オプション）リストをフィルタリングして、特定の広告を含めます。

1. ステータスを変更する各広告の横にあるチェックボックスをオンにします。

   複数行を選択する際のヒントについては、[複数行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md).&quot;

1. ツールバーで、ステータスボタンをクリックします。

   * 行をアクティブにするには、 ![有効化](/help/search-social-commerce/assets/activate.png "有効化").

   * 行を一時停止するには、 ![一時停止](/help/search-social-commerce/assets/pause.png "一時停止").

   * 行を削除するには、 ![その他](/help/search-social-commerce/assets/more.png "その他") を選択し、 **[!UICONTROL Delete]**. 確認メッセージで、 **[!UICONTROL Delete]**.

>[!MORELIKETHIS]
>
>* [広告について](ad-about.md)
>* [[!DNL Baidu] テキスト広告設定](ad-settings-baidu-text.md)
>* [[!DNL Google Ads] 呼び出しのみの広告設定](ad-settings-google-call.md)
>* [[!DNL Google Ads] 拡張された動的検索広告設定](ad-settings-google-dsa.md)
>* [[!DNL Google Ads] レスポンシブ検索広告設定](ad-settings-google-rsa.md)
>* [[!DNL Microsoft Advertising] 拡張された動的検索広告設定](ad-settings-microsoft-dsa.md)
>* [[!DNL Microsoft Advertising] マルチメディア広告設定](ad-settings-microsoft-multimedia.md)
>* [[!DNL Microsoft Advertising] 製品広告設定](ad-settings-microsoft-product.md)
>* [[!DNL Microsoft Advertising] レスポンシブ（オーディエンス）広告設定](ad-settings-microsoft-responsive.md)
>* [[!DNL Microsoft Advertising] レスポンシブ検索広告設定](ad-settings-microsoft-rsa.md)
>* [[!DNL Yandex] テキスト広告設定](ad-settings-yandex-text.md)
