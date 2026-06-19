---
title: フィードから生成されたデータのステータス
description: 在庫データフィードから生成されたデータのステータスについて説明します。
exl-id: 45c93fb2-0ed2-4336-9883-e150c292a7a5
feature: Search Inventory Feeds
TQID: https://experienceleague.adobe.com/3QPUheA0wIhk8aVqCcqeTGbgz9FdMUHstnpm5V8AXgE
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 260
ht-degree: 0%

---

# フィードから生成されたデータのステータス

*[!DNL Google Ads]、[!DNL LY Ads] （削除操作のみ）、[!DNL Microsoft Advertising]、および[!DNL Yandex] アカウントのみ*

各コンポーネントには、次のいずれかのステータスを設定できます。

* *[!UICONTROL New]:* コンポーネントは広告ネットワークに存在せず、広告ネットワークに投稿されませんでした。必要に応じて、コンポーネント名をクリックして設定を編集できます。 データを投稿する準備ができたら、**[!UICONTROL Post to SE]**&#x200B;をクリックし、送信するデータを指定します。

* *[!UICONTROL Posted]:* （キャンペーンと広告グループのみ）キャンペーンまたは広告グループが一部を広告ネットワークに投稿されましたが、エラーのため一部のコンポーネントが投稿されませんでした。 各キーワードと広告の検証ステータスは、修正が必要な情報を示します。 必要に応じて、コンポーネント名をクリックして、コンポーネントの設定を編集できます。

* *[!UICONTROL Active]:* コンポーネントは既に広告ネットワーク上でアクティブであり、ここで設定を編集することはできません。 アクティブなコンポーネントには、[!UICONTROL New]のサブコンポーネントが含まれる場合があります。これは、データが有効な場合に投稿できます。

* *[!UICONTROL Paused]:* コンポーネントは既に広告ネットワークで一時停止されており、ここで設定を編集することはできません。 一時停止したコンポーネントには、[!UICONTROL New]のサブコンポーネントが含まれている可能性があります。このサブコンポーネントは、データが有効な場合に投稿できます。

* *[!UICONTROL Deleted]:* コンポーネントは既に広告ネットワーク上で削除されており、ここで設定を編集することはできません。 削除されたコンポーネントには、[!UICONTROL New]のサブコンポーネントが含まれている可能性があります。このサブコンポーネントは、データが有効な場合に投稿できます。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [ フィードから生成されたデータを表示](propagated-data-view.md)
>* [ フィードから生成されたデータを編集](propagated-data-edit.md)
>* [ フィードから生成されたキャンペーンデータを広告ネットワークに投稿](propagated-data-post.md)
>* [在庫フィード データの投稿ジョブを停止](stop-job.md)
