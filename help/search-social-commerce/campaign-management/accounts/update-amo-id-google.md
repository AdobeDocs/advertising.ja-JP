---
title: の AMO ID （s_kwcid） トラッキングコードの更新 [!DNL Google Ads] アカウント
description: を最新の AMO ID トラッキングコードに切り替える方法を説明します [!DNL Google Ads] アカウント。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# の AMO ID （s_kwcid） トラッキングコードの更新 [!DNL Google Ads] アカウント

*Adobe AdvertisingとAdobe Analyticsの統合のみを持つ広告主*

*[!DNL Google Ads]アカウントのみ*

のレガシー（2019 年 10 月より前）形式 [AMO ID トラッキングコード](/help/integrations/analytics/ids.md#amo-id-formats) 既存のの場合 [!DNL Google Ads] アカウントは、のキャンペーンレベルや広告グループレベルでのレポートなど、Analytics の一部の機能をサポートしていません [!DNL Google Ads] パフォーマンス最大キャンペーン、ドラフトと実験キャンペーン、および広告+キーワード+一致タイプの同じ組み合わせが複数のキャンペーンに存在するその他のユースケース。

現在の形式には、キャンペーン ID と広告グループ ID のパラメーターが含まれます。

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

既存のアカウントの一部またはすべてについて、現在の形式に個別に変更できます。 Performance MAX キャンペーンまたはドラフトと実験キャンペーンがない場合は、新しい形式への移行はオプションです。

すべての新規 [!DNL Google Ads] アカウントでは、現在の AMO ID 形式が自動的に使用されます。

>[!NOTE]
>
>アカウントの移行後、すべてのクリック、コスト、インプレッションのデータは変更後に正しくレポートされますが、移行前に発生したクリックスルーは引き続き古い AMO ID 形式に基づくコンバージョンデータに関連付けられます。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、クリックします ![矢印ドロップダウンアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png)を選択してから、 **[!UICONTROL Edit]**.

1. クリック **[!UICONTROL Set Account Tracking]**.

1. 移行を開始します。

   1. 次の **[!UICONTROL S_KWCID FORMAT]** を選択し、 **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. クリック **[!UICONTROL Migrate to new s_kwcid format]**.

   1. 確認メッセージで、チェック ボックスをオンにし、 **[!UICONTROL Continue]**.

   1. アカウント設定で、 **[!UICONTROL Post]**.

   キャンペーンのメタデータの更新先： [!DNL Analytics] 数日以内に。 トラッキングは中断されることなく継続されるので、データは失われませんが、レポートは次の場合まで新しいトラッキングコードを反映しない可能性があります [!DNL Analytics] すべてのメタデータを受信します。

   >[!NOTE]
   >
   >移行前に発生したすべてのクリックスルーで、引き続き古い形式に基づいたコンバージョンデータがレポートされます。

1. 移行を開始した後、必要に応じてランディングページのサフィックス設定（一部の広告ネットワークでは「最終的な URL サフィックス」と呼ばれます）を更新します。

   * いつ [!UICONTROL Auto Upload]「トラッキング設定、検索、ソーシャルおよびCommerceで機能が有効になると、このアカウントおよびそのキャンペーンのランディングページサフィックスのトラッキングコードが自動的に更新されます。 何もする必要はありません。

   * いつ [!UICONTROL Auto Upload]「機能が有効になっていません。また、 [サーバーサイド AMO ID 機能](/help/integrations/analytics/ids.md#amo-id-formats)ランディングページのサフィックス設定の AMO ID パラメーターを手動で更新する必要があります。 アカウントレベルとキャンペーンレベルのサフィックスは、アカウント設定とキャンペーン設定で手動で変更することも、バルクシートに変更をアップロードして変更することもできます。 広告グループレベル以下でサフィックスを設定するには、次を使用します [!DNL Google Ads] 編集者。

   * キャンペーンコンポーネントのベース URL 設定に AMO ID を含める場合は、関連するランディングページのサフィックス設定に移動します。

1. （推奨）このアカウントのデータを次で確認します： [!DNL Analytics] 追加のアカウントを移行する前に、

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
>* [が使用するAdobe Advertising ID [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
