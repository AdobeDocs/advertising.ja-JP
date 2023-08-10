---
title: の AMO ID(s\_kwcid) トラッキングコードを更新します。 [!DNL Google Ads] アカウント
description: の最新の AMO ID トラッキングコードに切り替える方法を説明します。 [!DNL Google Ads] アカウント。
exl-id: 82168ee6-43bb-4b8d-882d-5254a1abcb09
feature: Search Campaign Management
source-git-commit: f80d05aa40fd4114e9585220fe747ca7d36a19bb
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# の s_kwcid トラッキングコードを更新します。 [!DNL Google Ads] アカウント

*Adobe AdvertisingとAdobe Analyticsの統合のみの広告主*

*[!DNL Google Ads]アカウントのみ*

既存の s\_kwcid トラッキングコードの従来の形式 [!DNL Google Ads] アカウントは、Analytics の一部の機能（例えば、次のキャンペーンレベルや広告グループレベルでのレポート）をサポートしていません。 [!DNL Google Ads] パフォーマンス最大キャンペーン、ドラフト&amp;実験キャンペーン、および同じ ad+keyword+match タイプの組み合わせが複数のキャンペーンに存在するその他の使用例。

最新の形式には、キャンペーン ID と広告グループ ID のパラメーターが含まれます。

```
s_kwcid=AL!{userid}!3!{creative}!{matchtype}!{placement}!{network}!{product_partition_id}!{keyword}!{campaignid}!{adgroupid}
```

既存のアカウントの一部またはすべてに対して、新しい形式に個別に変更できます。 最大パフォーマンスのキャンペーンまたはドラフト&amp;エクスペリメントキャンペーンがない場合、新しい形式への移行は任意です。

すべて新規 [!DNL Google Ads] アカウントは、新しい s\_kwcid 形式を自動的に使用します。

>[!NOTE]
>
>アカウントを移行すると、変更後、すべてのクリック、コスト、インプレッションのデータが正しくレポートされますが、移行前に発生したクリックスルーは、古い s\_kwcid 形式に基づくコンバージョンデータに関連付けられます。

1. メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **[!UICONTROL Accounts]**.
1. アカウント名の上にカーソルを置き、 ![矢印ドロップダウンアイコン](/help/search-social-commerce/assets/arrow-dropdown-menu.png)を選択し、 **[!UICONTROL Edit]**.
1. クリック **[!UICONTROL Set Account Tracking]**.
1. 移行を開始します。

   1. 次の隣 **[!UICONTROL S_KWCID FORMAT]** をクリックし、 **[!UICONTROL LEGACY S_KWCID FORMAT]**.
   1. クリック **[!UICONTROL Migrate to new s_kwcid format]**.
   1. 確認メッセージで、チェックボックスを選択し、 **[!UICONTROL Continue]**.
   1. アカウントの設定で、 **[!UICONTROL Post]**.

   キャンペーンのメタデータは、数日以内に Analytics で更新されます。 トラッキングは中断されずに続行されるので、データは失われませんが、Analytics がすべてのメタデータを受信するまで、レポートには新しいトラッキングコードが反映されない場合があります。

   >[!NOTE]
   >
   >移行前に発生したすべてのクリックスルーでも、古い形式に基づいてコンバージョンデータがレポートされます。

1. 移行を開始したら、必要に応じて、ランディングページサフィックス設定（一部の広告ネットワークでは「最終 URL サフィックス」と呼ばれる）を更新します。

   * 次の場合に [!UICONTROL Auto Upload]「 」機能がトラッキング設定で有効になっている場合、検索、ソーシャル、コマースは、このアカウントとそのキャンペーンのランディングページサフィックスに含まれるトラッキングコードを自動的に更新します。 あなたは何もする必要はありません。
   * 次の場合に [!UICONTROL Auto Upload]」機能が有効になっておらず、サーバー側の s-kwcid を使用していない場合は、「ランディングページサフィックス」設定で s\_kwcid パラメーターを手動で更新する必要があります。 アカウントレベルとキャンペーンレベルのサフィックスは、アカウントとキャンペーンの設定で手動で変更するか、バルクシートに変更をアップロードすることで変更できます。 広告グループレベル以下でサフィックスを設定するには、 [!DNL Google Ads] 編集者です。
   * 任意のキャンペーンコンポーネントのベース URL 設定に s\_kwcid を含める場合は、関連する「ランディングページサフィックス」設定に移動します。

1. （推奨）追加のアカウントを移行する前に、Analytics でこのアカウントのデータを確認します。

>[!MORELIKETHIS]
>
>* [広告ネットワークアカウントの管理](ad-network-account-manage.md)
>* [AMO ID トラッキングパラメーター](/help/search-social-commerce/tracking/skwcid-tracking-parameter.md)
>* [の概要 [!DNL Analytics for Advertising]](https://experienceleague.adobe.com/docs/advertising/integrations/home.html){target="_blank"}
