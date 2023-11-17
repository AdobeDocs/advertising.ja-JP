---
title: 管理 [!DNL Google Ads] 場所の拡張
description: 作成および管理方法を学ぶ [!DNL Google Ads] 場所の拡張。
exl-id: 8515f77d-c00e-46f5-9711-b68930c3c171
feature: Search Campaign Management
source-git-commit: 61e31f8edea6f6d1ee4a1901125e7f5594c342f1
workflow-type: tm+mt
source-wordcount: '500'
ht-degree: 0%

---

# 管理 [!DNL Google Ads] 場所の拡張

場所の拡張には、会社の住所、クリック可能な電話番号、およびテキスト広告を含むマップマーカーが表示されます。 モバイルデバイスに表示される広告には、ビジネスへの道筋とのリンクが含まれます。 [!DNL Google Ads] 場所の拡張機能は、の情報を使用します。 [リンク [!DNL Google My Business] アカウント](https://support.google.com/google-ads/answer/2404182).

場所の拡張は、キャンペーンレベルと広告グループレベルの両方で作成できます。 キャンペーンまたは広告グループに複数の場所の拡張がある場合、広告ネットワークには、ユーザーに最も近い場所の拡張が表示されます。 オプションで、特定ののすべての場所の拡張を無効にすることができます [!DNL Google Ads] キャンペーンおよび広告グループを場所拡張設定から選択できます。

## 場所の拡張のパフォーマンスデータ

広告ネットワークは、場所の拡張に対するクリックを、拡張が含まれる広告に関連付けられたキーワードにマッピングします。  検索、ソーシャル、コマースで、拡張機能レベルのコストやクリックデータは使用できません。 In [!DNL Google Ads]をクリックすると、 [!DNL Campaigns] タブ/ [!DNL Ad Extensions] タブをクリックします。 場所の拡張機能には追跡する URL がないので、Search、Social、&amp;Commerce ではそのコンバージョンデータをレポートできません。

*[!DNL Google Ads]アカウントのみ*

## キャンペーンおよび広告グループの場所の拡張の作成

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Associations]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成")を選択し、 **[!UICONTROL Location]**.

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. 次を指定します。 [場所拡張の設定](#location-extension-settings):

   * Adobe Analytics の [!UICONTROL Location Settings] 「 」セクションで、場所を指定します。

   * Adobe Analytics の [!UICONTROL Assignment] セクションで、ロケーション設定を適用できるキャンペーンおよび広告グループを選択します。

1. クリック **[!UICONTROL Post]**.

## キャンペーンおよび広告グループの場所の拡張を無効にする

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]> [!UICONTROL Extensions] >[!UICONTROL Associations]**.

1. データテーブルの上にあるツールバーで、 ![作成](/help/search-social-commerce/assets/add.png "作成")を選択し、 **[!UICONTROL Location]**.

1. 広告ネットワークとアカウント名を選択し、 **[!UICONTROL Continue]**.

1. 次を指定します。 [場所拡張の設定](#location-extension-settings):

   * Adobe Analytics の [!UICONTROL Location Settings] セクション、選択 **[!UICONTROL Disable Locations]**.

   * Adobe Analytics の [!UICONTROL Assignment] セクションで、ロケーション設定を適用できるキャンペーンおよび広告グループを選択します。

1. クリック **[!UICONTROL Post]**.

## Google Ads ロケーション拡張機能の設定 {#location-extension-settings}

### [!UICONTROL Location Settings]

のビジネスロケーション [リンクされたGoogle My Business アカウント](https://support.google.com/google-ads/answer/2404182?vid=1-635794239083658097-1242615452#link) は、指定したキャンペーンおよび広告グループの場所の拡張で使用できます。

* *[!UICONTROL All Locations]:* リンクされたアカウント内のすべてのビジネスの場所を使用するには、次の手順に従います。

* *[!UICONTROL Locations matching filter]:* ビジネス名を指定し、必要に応じて最大 3 つのビジネスカテゴリを指定して、リンクされたアカウントのビジネスをフィルターします。

* *[!UICONTROL Locations I pick]:* リンクされたアカウント内のすべてのビジネスのリストから選択します。 ビジネスを選択するには、名前をクリックし、次に「 」をクリックして、ビジネスを右側の列に移動します。

* *[!UICONTROL Disable Locations]:* 指定したキャンペーンまたは広告グループのすべての場所の拡張を無効にします。

### [!UICONTROL Assignment]

**[!UICONTROL Campaigns/Ad Groups]:** ロケーション設定が適用されるキャンペーンおよび広告グループ。

* キャンペーンの子エンティティを表示するには、キャンペーン名をクリックします。

* 名前に含まれるテキスト文字列でキャンペーンリストまたは広告グループリストをフィルタリングするには、 ![フィルター](/help/search-social-commerce/assets/filter.png "フィルター")をクリックし、テキスト文字列を入力フィールドに入力または貼り付けて、 **入力** キー。

* エンティティを選択するには、エンティティの横にある円 (![選択](/help/search-social-commerce/assets/include.png "選択")) をクリックします。
