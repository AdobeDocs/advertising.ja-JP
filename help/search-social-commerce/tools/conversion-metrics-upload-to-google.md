---
title: コンバージョン指標のアップロード先 [!DNL Google Ads]
description: 検索、ソーシャル、コマースで追跡されたコンバージョン指標をにアップロードする方法について説明します。 [!DNL Google Ads].
exl-id: 88db66c2-12db-41cf-b6c4-ed821cb3b8ea
feature: Search Tools
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 0%

---

# コンバージョン指標のアップロード先 [!DNL Google Ads]

*次を持つ広告主 [!DNL Google Ads] アカウントのみ*

検索、ソーシャル、コマース（オプション）は次にアップロードできます： [!DNL Google Ads] 追跡するすべてのコンバージョン指標 [!DNL Google Ads] Adobe Analyticsから同期されたAdobe Advertisingコンバージョントラッキングサービスとコンバージョン指標を使用するキャンペーン。 このオプションを選択した場合、ハイブリッドの最適化ではコンバージョンを利用できません。 ハイブリッドの最適化にAdobeコンバージョンを使用する場合は、[広告ネットワークへの目標のアップロードを有効にする](objective-upload-to-networks.md).&quot;

日別のアップロードでは、追跡される `gclid` 値、広告主レベルのアトリビューションモデルを使用して定義されたコンバージョン値、およびタイムスタンプ。 アトリビューションモデルが更新されると、次回のアップロードで新しいモデルが使用されますが、過去のデータは新しいモデルを使用するように更新されません。

>[!NOTE]
>
>アップロードには、フィードファイルからAdobe Advertisingにアップロードされたコンバージョン指標は含まれません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Tools] >[!UICONTROL Conversion Upload Setup]**.

1. の横のチェックボックスをオンにします。 **[!UICONTROL Upload Conversions to Google Ads]**.

1. クリック **[!UICONTROL Save]**.

1. （コンバージョンが管理者のアカウントレベルで追跡される場合） [管理者アカウントの資格情報を追加します](/help/search-social-commerce/admin/manager-accounts.md) 時刻 **[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Manager Accounts]**.

>[!MORELIKETHIS]
>
>* [広告ネットワークへの目標のアップロードを有効にする](objective-upload-to-networks.md)
