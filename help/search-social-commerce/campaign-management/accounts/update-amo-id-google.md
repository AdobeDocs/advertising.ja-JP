---
title: の AMO ID(s_kwcid) トラッキングコードを更新します。 [!DNL Google Ads] アカウント
description: の最新の AMO ID トラッキングコードに切り替える方法を説明します。 [!DNL Google Ads] アカウント。
exl-id: 4dfd9ea6-f639-4b9a-aaa5-13f574e3961b
feature: Search Campaign Management
source-git-commit: 515c049a45d795fd973b5fcead5f96e71dbf844a
workflow-type: tm+mt
source-wordcount: '462'
ht-degree: 0%

---

# の AMO ID(s_kwcid) トラッキングコードを更新します。 [!DNL Google Ads] アカウント

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

*[!DNL Google Ads]アカウントのみ*

のレガシー（2019 年 10 月以前）形式 [AMO ID トラッキングコード](/help/integrations/analytics/ids.md#amo-id-formats) ( 既存の [!DNL Google Ads] アカウントは、Analytics の一部の機能（例えば、次のキャンペーンレベルや広告グループレベルでのレポート）をサポートしていません。 [!DNL Google Ads] パフォーマンス最大キャンペーン、ドラフト&amp;実験キャンペーン、および同じ ad+keyword+match タイプの組み合わせが複数のキャンペーンに存在するその他の使用例。

現在の形式には、キャンペーン ID と広告グループ ID のパラメーターが含まれます。

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

既存のアカウントの一部またはすべてに対して、個別に現在の形式に変更できます。 最大パフォーマンスのキャンペーンまたはドラフト&amp;エクスペリメントキャンペーンがない場合、新しい形式への移行は任意です。

すべて新規 [!DNL Google Ads] アカウントは、現在の AMO ID 形式を自動的に使用します。

>[!NOTE]
>
>アカウントを移行すると、変更後、すべてのクリック、コスト、インプレッションのデータが正しくレポートされますが、移行前に発生したクリックスルーは、古い AMO ID 形式に基づくコンバージョンデータに関連付けられます。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.

1. アカウント名の上にカーソルを置き、 ![矢印ドロップダウンアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png)を選択し、 **[!UICONTROL Edit]**.

1. クリック **[!UICONTROL Set Account Tracking]**.

1. 移行を開始します。

   1. 次の隣 **[!UICONTROL S_KWCID FORMAT]** をクリックし、 **[!UICONTROL LEGACY S_KWCID FORMAT]**.

   1. クリック **[!UICONTROL Migrate to new s_kwcid format]**.

   1. 確認メッセージで、チェックボックスを選択し、 **[!UICONTROL Continue]**.

   1. アカウントの設定で、 **[!UICONTROL Post]**.

   キャンペーンのメタデータはで更新されました。 [!DNL Analytics] 数日以内に トラッキングは中断されずに続行されるので、データは失われませんが、レポートには新しいトラッキングコードが反映される可能性があります。 [!DNL Analytics] はすべてのメタデータを受け取ります。

   >[!NOTE]
   >
   >移行前に発生したすべてのクリックスルーでも、古い形式に基づいてコンバージョンデータがレポートされます。

1. 移行を開始したら、必要に応じて、ランディングページサフィックス設定（一部の広告ネットワークでは「最終 URL サフィックス」と呼ばれる）を更新します。

   * 次の場合に [!UICONTROL Auto Upload]「 」機能がトラッキング設定で有効になっている場合、検索、ソーシャル、コマースは、このアカウントとそのキャンペーンのランディングページサフィックスに含まれるトラッキングコードを自動的に更新します。 あなたは何もする必要はありません。

   * 次の場合に [!UICONTROL Auto Upload]」機能が有効になっていないので、 [サーバー側 AMO ID 機能](/help/integrations/analytics/ids.md#amo-id-formats)の場合は、「ランディングページサフィックス」設定の AMO ID パラメーターを手動で更新する必要があります。 アカウントレベルとキャンペーンレベルのサフィックスは、アカウントとキャンペーンの設定で手動で変更するか、バルクシートに変更をアップロードすることで変更できます。 広告グループレベル以下でサフィックスを設定するには、 [!DNL Google Ads] 編集者です。

   * 任意のキャンペーンコンポーネントのベース URL 設定に AMO ID を含める場合は、該当する「ランディングページサフィックス」設定に移動します。

1. （推奨）でこのアカウントのデータを検証します。 [!DNL Analytics] 追加のアカウントを移行する前に

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
>* [Adobe AdvertisingID 使用者 [!DNL Analytics]](/help/integrations/analytics/ids.md)
>* [の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
