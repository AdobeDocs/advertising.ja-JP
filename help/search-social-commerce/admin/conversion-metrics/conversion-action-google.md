---
title: リードの拡張コンバージョン用  [!DNL Google Ads]  コンバージョンアクションの作成
description: リードのコンバージョンを強化するため  [!DNL Google Ads]  コンバージョンアクションを作成する方法を説明します。
feature: Conversions
source-git-commit: 5eb6ed5b42e74f424fc8499f6df0dbe3f2430ab2
workflow-type: tm+mt
source-wordcount: '459'
ht-degree: 0%

---

# リードのコンバージョンを [!DNL Google Ads] しく強化するためのコンバージョンアクションの作成

*[!DNL Google Ads]アカウントのみ*

管理者アカウントレベルで追跡され [!DNL Google Ads] コンバージョンではなく、個々の [!DNL Google Ads] アカウントで追跡されるリードの拡張コンバージョンに対して、コンバージョンアクションを作成できます。

1. メインメニューで、**[!UICONTROL Search]> [!UICONTROL Admin] >[!UICONTROL Conversions]** をクリックすると、「**[!UICONTROL Summary]**」タブが開きます。

1. データ テーブルの上にあるツールバーで、[![ 作成 ](/help/search-social-commerce/assets/add.png " 作成 ")] をクリックします。

1. [ 変換アクションの設定 ](#conversion-action-settings-google) を指定します。

   1. アカウントを選択してから、コンバージョンの種類を選択します：*[!UICONTROL Import conversion]*。

   1. 「**[!UICONTROL Next]**」をクリックします。

   1. 変換アクションオプションを指定します。

   1. 「**[!UICONTROL Generate]**」をクリックします。

1. リードのコンバージョン強化用のトラッキングタグを作成する方法についての情報を読み、「**[!UICONTROL Next]**」をクリックします。

   コンバージョンタグを作成し、必要に応じてコンバージョン指標を追跡する Web サイトに実装します。 手順については、次を参照してください。

   * [!DNL Google] タグを使用するには、「[ タグを使用したリードの拡張コンバージョンの設定 ](https://support.google.com/google-ads/answer/11347292)」の「[!DNL Google] タグの設定を構成する」に関する [!DNL Google Ads] の手順を参照し  [!DNL Google]  ください。

   * [!DNL Google Tag Manager] を使用するには、「[ リードの拡張コンバージョンの設定  [!DNL Google Tag Manager]](https://support.google.com/google-ads/answer/11021502?#configure)」の「[!DNL Google] タグ設定の指定」および「設定を確認してコンテナを公開」の [!DNL Google Ads] の手順を参照してください。

1. 「**[!UICONTROL Done].**」をクリックします。

コンバージョンアクションを作成し、コンバージョントラッキングタグを実装したら、組織が取得したオフラインコンバージョンデータをアップロードして、そのデータをコンバージョンアクションに関連付けることができます。 [ 拡張コンバージョン用のオフラインコンバージョンデータのアップロード ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md) を参照してください。

## 変換アクションの設定 {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:** 該当するGoogle広告アカウント。

**[!UICONTROL Type of Conversion]:** 追跡するコンバージョンのタイプ：*[!UICONTROL Import conversion]* を選択します。 その他のすべてのタイプは、他のタイプのコンバージョンの（コンバージョンアクションではなく）コンバージョントラッキングタグの作成に使用されます。

**[!UICONTROL Conversion Name]:** コンバージョンアクションの一意の名前。

**\[ コンバージョンカテゴリ\]:** コンバージョンカテゴリ（*適格リード*、*サインアップ* など）。

**\[ アクションの種類\]:** 目標が *[!UICONTROL Primary action used for bidding optimization]* と *[!UICONTROL Secondary action not used for bidding optimization]* のどちらであるか。

**[!UICONTROL Value]:** [ 各コンバージョンの値 ](https://support.google.com/google-ads/answer/13064207) の測定方法：

* *[!UICONTROL Use the same value for each conversion],* 通貨を選択し、各換算の値を入力する必要があります。

* *[!UICONTROL Use a different value for each conversion]、* 通貨を選択し、各換算にデフォルト値を入力する必要があります。 特定の web ページでタグを実装する際に、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:**&#x200B;[ クリックまたはインタラクションごとにカウントするコンバージョン数 ](https://support.google.com/google-ads/answer/3438531):*[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]* または *[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]:** コンバージョンが記録される広告インタラクション後の最大日数。 検索、ディスプレイ、ショッピングキャンペーンの場合、ウィンドウは 1～90 日です。 数値を選択するか、**[!UICONTROL Custom]** を選択して数値を入力します。

**[!UICONTROL View Through Conversion Window]:** ユーザーが広告を表示してから、ビュースルーコンバージョンが記録されるまでの最大日数。 検索、ディスプレイ、ショッピングキャンペーンの場合、ウィンドウは 1～90 日です。 数値を選択するか、**[!UICONTROL Custom]** を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [ 各広告インタラクションのクレジットの取得額 ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138):*[!UICONTROL Data driven]* または *[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化 ](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [ リードのコ  [!DNL Google Ads]  バージョンの実装と強化 ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
