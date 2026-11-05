---
title: 広告の拡張機能の関連付けを管理
description: 広告拡張機能の関連付けを削除し、関連データをクリップボードにコピーする方法について説明します。
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
  - id: 76ac9ff6-5d89-5acb-bc0b-875761bb3320
    internal-label: Search Campaign Management
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 10d7adc3b3ced812ee1281139a23a573df2beeef
workflow-type: tm+mt
source-wordcount: '228'
ht-degree: 0%
---
# 広告の拡張機能の関連付けを管理

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

関連付けは、広告拡張機能をアカウントエンティティにリンクして、拡張機能を広告と共に使用できるようにします。 サイトリンク、コールアウト、場所、および広告ネットワークでサポートされている電話機の拡張機能の関連付けなど、既存の関連付けを削除できます。

共有サイトリンクまたはコールアウト関連付けを削除すると、選択したエンティティとの関連付けが削除されます。ライブラリから共有拡張機能が削除されることはありません。 代わりに、共有拡張機能を削除するには、**[!UICONTROL Sitelinks]**&#x200B;または&#x200B;**[!UICONTROL Callouts]** タブを使用します。

関連付けを表示するには、[!UICONTROL View Extensions]権限が必要です。 関連付けを削除するには、[!UICONTROL Edit Extensions]権限が必要です。

## 関連付けを削除 {#association-delete}

1. メインメニューで、**[!UICONTROL Library]>[!UICONTROL Extensions]**&#x200B;をクリックし、**[!UICONTROL Associations]** タブをクリックします。

1. （オプション）特定の拡張機能、キャンペーン、広告グループを含めるようにリストをフィルタリングします。

1. 削除する各関連付けの横にあるチェックボックスをオンにします。

   複数の行を選択する際のヒントについては、「[複数の行を選択](/help/search-social-commerce/common-tasks/navigation-editing-selection/multiple-rows-select.md)」を参照してください。

1. 一括操作ツールバーで、![削除](/help/search-social-commerce/assets/delete-new.png "削除")をクリックします。

1. 確認メッセージで、**[!UICONTROL Confirm]**&#x200B;をクリックします。

## 選択した行のすべてのデータをクリップボードにコピー {#copy-to-clipboard}

ビューに表示されるフィルターと列に従って、選択した行に表示される情報をコピーします。 情報はタブ区切り値（TSV）として保存されます。

1. データをコピーする各行の横にあるチェックボックスをオンにします。

1. 一括操作ツールバーで、**[!UICONTROL Copy]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [共有サイトリンク拡張機能の管理](sitelink-extension-manage.md)
>* [Google Ads共有コールアウト拡張機能の管理](callout-extension-manage.md)
