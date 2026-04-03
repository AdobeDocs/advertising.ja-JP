---
title: リードの [!DNL Google Ads] 強化コンバージョンのコンバージョンアクションを作成します
description: リードのコンバージョンを強化するための [!DNL Google Ads]  コンバージョンアクションの作成方法について説明します。
feature: Conversions
exl-id: faf4a6de-e82f-4afd-bda5-2602fb45aee5
TQID: https://experienceleague.adobe.com/KqFHgxjc-4snyo3nf-3-ry6nsyapMPcwKEWvgi-pxGc
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 459
ht-degree: 0%

---

# リードの[!DNL Google Ads]強化コンバージョンのコンバージョンアクションを作成します

*[!DNL Google Ads]アカウントのみ*

マネージャーのアカウントレベルで追跡されるコンバージョンではなく、個々の[!DNL Google Ads] アカウントで追跡されるリードの強化コンバージョンの[!DNL Google Ads]個のコンバージョンアクションを作成できます。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックすると、**[!UICONTROL Summary]** タブが開きます。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. [&#x200B; コンバージョンアクション設定](#conversion-action-settings-google)を指定します。

   1. アカウントを選択し、変換タイプを選択します：*[!UICONTROL Import conversion]*。

   1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. コンバージョンアクションのオプションを指定します。

   1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. リードの強化コンバージョンのトラッキングタグを作成する方法に関する情報を読み、**[!UICONTROL Next]**&#x200B;をクリックします。

   コンバージョン指標を追跡するweb サイトで、コンバージョンタグを作成し、必要に応じて実装します。 手順については、次を参照してください。

   * [!DNL Google] タグを使用するには、「[!DNL Google Ads] タグを使用したリードの拡張コンバージョンの設定[!DNL Google] タグ [」の「 [!DNL Google]  タグ設定の設定」に関する](https://support.google.com/google-ads/answer/11347292)の手順を参照してください。

   * [!DNL Google Tag Manager]を使用するには、「[!DNL Google Ads]&#x200B;[!DNL Google]」の「[&#x200B; リードの拡張コンバージョンの設定」の「 [!DNL Google Tag Manager] タグ設定の設定」と「設定を確認してコンテナを公開する」の](https://support.google.com/google-ads/answer/11021502?#configure)の手順を参照してください。

1. **[!UICONTROL Done].**&#x200B;をクリックします

コンバージョンアクションを作成し、コンバージョントラッキングタグを実装したら、組織がキャプチャしたオフラインのコンバージョンデータをアップロードし、コンバージョンアクションに関連付けることができます。 「[&#x200B; オフラインのコンバージョンデータをアップロードしてコンバージョンを強化する](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)」を参照してください。

## コンバージョンアクションの設定 {#conversion-action-settings-google}

**[!UICONTROL Select an Account]:**&#x200B;該当するGoogle Ads アカウント。

**[!UICONTROL Type of Conversion]:**&#x200B;追跡するコンバージョンの種類：*[!UICONTROL Import conversion]*&#x200B;を選択します。 他のすべてのタイプは、他のタイプのコンバージョンのコンバージョントラッキングタグ（コンバージョンアクションではなく）を作成するために使用されます。

**[!UICONTROL Conversion Name]:**&#x200B;変換アクションの一意の名前。

**\[ コンバージョンカテゴリ\]:** *適格リード*&#x200B;または&#x200B;*サインアップ*&#x200B;などのコンバージョンカテゴリ。

**\[Action Type\]:**&#x200B;目標が&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;か&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*&#x200B;かです。

**[!UICONTROL Value]:**&#x200B;各コンバージョンの[値を測定する方法](https://support.google.com/google-ads/answer/13064207):

* 通貨を選択し、各変換の値を入力する必要がある&#x200B;*[!UICONTROL Use the same value for each conversion],*。

* 通貨を選択し、各変換の既定値を入力する必要がある&#x200B;*[!UICONTROL Use a different value for each conversion],*。 特定のweb ページにタグを実装する場合、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [&#x200B; クリックまたはインタラクションごとにカウントするコンバージョン数](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;または&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions because only the first interaction is valuable)]*。

**[!UICONTROL Click Through Conversion Window]:** コンバージョンを記録する広告インタラクションの後最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL View Through Conversion Window]:** ビュースルーコンバージョンが記録される、ユーザーが広告を表示してから経過した最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [各広告インタラクションに対するクレジット額](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*&#x200B;または&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [&#x200B; オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [実装 [!DNL Google Ads]  リードの拡張コンバージョン &#x200B;](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
