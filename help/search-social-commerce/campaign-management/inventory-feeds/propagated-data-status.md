---
title: フィードから生成されたデータのステータス
description: 在庫データフィードから生成されたデータのステータスについて説明します。
exl-id: 8e5e7649-a16b-4634-896a-7c216185b367
feature: Search Inventory Feeds
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 0%

---

# フィードから生成されたデータのステータス

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads] （アクションの削除のみ）および [!DNL Yandex] アカウントのみ*

各コンポーネントには、次のいずれかのステータスを設定できます。

* *[!UICONTROL New]:* コンポーネントは、広告ネットワークに存在せず、広告ネットワークにも投稿されませんでした。必要に応じて、コンポーネント名をクリックして設定を編集できます。 データを投稿する準備が整ったら、「 **[!UICONTROL Post to SE]** 送信するデータを指定します。

* *[!UICONTROL Posted]:* （キャンペーンおよび広告グループのみ）キャンペーンまたは広告グループが広告ネットワークに部分的に投稿されましたが、一部のコンポーネントはエラーのため投稿されませんでした。 各キーワードおよび広告の検証ステータスは、修正が必要な情報を示します。 必要に応じて、コンポーネント名をクリックして、コンポーネントの設定を編集できます。

* *[!UICONTROL Active]:* コンポーネントは既に広告ネットワーク上でアクティブになっているので、ここで設定を編集することはできません。 アクティブなコンポーネントには、 [!UICONTROL New]：データが有効な場合に投稿できます。

* *[!UICONTROL Paused]:* コンポーネントは広告ネットワーク上で既に一時停止されています。ここで設定を編集することはできません。 一時停止されたコンポーネントには、 [!UICONTROL New]：データが有効な場合に投稿できます。

* *[!UICONTROL Deleted]:* コンポーネントは既に広告ネットワーク上で削除されているので、ここで設定を編集することはできません。 削除されたコンポーネントには、 [!UICONTROL New]：データが有効な場合に投稿できます。

>[!MORELIKETHIS]
>
>* [在庫フィードについて](inventory-feeds-about.md)
>* [フィードから生成されたデータを表示](propagated-data-view.md)
>* [フィードから生成されたデータを編集](propagated-data-edit.md)
>* [フィードから広告ネットワークに生成されたキャンペーンデータを投稿します](propagated-data-post.md)
>* [在庫フィードデータの転記ジョブを停止します](stop-job.md)
