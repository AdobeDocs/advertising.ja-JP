---
title: リードの [!DNL Google Ads] 強化コンバージョンのコンバージョンアクションを作成します
description: リードのコンバージョンを強化するための [!DNL Google Ads]  コンバージョンアクションの作成方法について説明します。
feature: Conversions
source-git-commit: 3272a0d3e5766a22c2ff761b84f1774cafe153bd
workflow-type: tm+mt
source-wordcount: '919'
ht-degree: 0%

---

# リードの[!DNL Google Ads]強化コンバージョンのコンバージョンアクションを作成します

<!-- Includes procedure in new UI, which isn't available to all yet -->

*[!DNL Google Ads]アカウントのみ*

マネージャーのアカウントレベルで追跡されるコンバージョンではなく、個々の[!DNL Google Ads] アカウントで追跡されるリードの強化コンバージョンの[!DNL Google Ads]個のコンバージョンアクションを作成できます。<!-- I don't see a list of synced conversion actions here; supposedly we do list them, but I don't see them in the legacy UI either (unless they're just listed as conversions, but not identified differently). Clarify and reword if necessary. -->

## （新しいUI）コンバージョンアクションの作成

*Beta機能*

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Set up Conversion]**&#x200B;をクリックします。

1. [&#x200B; コンバージョンアクション設定](#conversion-action-settings-google)を指定します。

   1. [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*&#x200B;を選択します。

   1. アカウントを選択し、変換タイプを選択します：*[!UICONTROL Import conversion]*。

   1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. コンバージョンアクションのオプションを指定します。

   1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認します。

   1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. リードの強化コンバージョンのトラッキングタグを作成する方法に関する情報を読み、**[!UICONTROL Next]**&#x200B;をクリックします。

   コンバージョン指標を追跡するweb サイトで、コンバージョンタグを作成し、必要に応じて実装する必要があります。 また、リードのコンバージョンを強化し、顧客データの利用条件に同意する必要があります。 手順については、「[&#x200B; リードのコンバージョンを強化するために [!DNL Google]  タグを設定](https://support.google.com/google-ads/answer/11021502)するための[!DNL Google Ads]手順」を参照してください。

   トランザクション固有のコンバージョン値を追跡する場合は、[&#x200B; イベントスニペットをカスタマイズ &#x200B;](https://support.google.com/google-ads/answer/6095947)します。

1. **[!UICONTROL Close].**&#x200B;をクリックします

コンバージョンアクションを作成し、コンバージョントラッキングタグを実装したら、組織がキャプチャしたオフラインのコンバージョンデータをアップロードし、コンバージョンアクションに関連付けることができます。 拡張コンバージョン [&#128279;](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)については、「 オフラインのコンバージョンデータをアップロード」を参照してください。「<!-- Update that reference once I move the file to new-ui/ folder. -->」

### コンバージョンアクションの設定 {#conversion-action-settings-google}

#### パスセクションの設定

**[!UICONTROL Setup Method]:** <!--The method of XX: --> *[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:**&#x200B;広告ネットワーク：*[!UICONTROL Google]*。

#### 「コンバージョンの詳細」セクション

**[!UICONTROL Select Account]:**&#x200B;該当する[!DNL Google Ads] アカウント。

**[!UICONTROL Type of conversions]:**&#x200B;追跡するコンバージョンの種類：*[!UICONTROL Import conversion]*&#x200B;を選択します。 他のすべてのタイプは、他のタイプのコンバージョンのコンバージョントラッキングタグ（コンバージョンアクションではなく）を作成するために使用されます。

#### 「コンバージョン設定」セクション

**[!UICONTROL Conversion Name]:**&#x200B;変換アクションの一意の名前。

**[!UICONTROL Goal Category]:** コンバージョンカテゴリ（*適格リード*&#x200B;または&#x200B;*サインアップ*&#x200B;など）。

**[!UICONTROL Preferred Action optimization]:**&#x200B;目標が&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;か&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*&#x200B;か。

**[!UICONTROL Conversion Value]:**&#x200B;各コンバージョンの[値を測定する方法](https://support.google.com/google-ads/answer/13064207):

* 通貨を選択し、各変換の値を入力する必要がある&#x200B;*[!UICONTROL Use the same value for each conversion],*。

* 通貨を選択し、各変換の既定値を入力する必要がある&#x200B;*[!UICONTROL Use different values for each conversion],*。 特定のweb ページにタグを実装する場合、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [&#x200B; クリックまたはインタラクションごとにカウントするコンバージョン数](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;または&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*。

**[!UICONTROL Click-Through Conversion Window]:** コンバージョンを記録する広告インタラクションの後最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL View-Through Conversion Window]:** ビュースルーコンバージョンが記録される、ユーザーが広告を表示してから経過した最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [各広告インタラクションのクレジットを決定するアトリビューションモデル &#x200B;](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*&#x200B;または&#x200B;*[!UICONTROL Last click]*。

## （レガシーUI）コンバージョンアクションの作成

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Admin] >[!UICONTROL Conversions]**&#x200B;をクリックすると、**[!UICONTROL Summary]** タブが開きます。

1. データテーブルの上にあるツールバーで、![作成](/help/search-social-commerce/assets/add.png "作成")をクリックします。

1. [&#x200B; コンバージョンアクション設定](#conversion-action-settings-google-legacy)を指定します。

   1. アカウントを選択し、変換タイプを選択します：*[!UICONTROL Import conversion]*。

   1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. コンバージョンアクションのオプションを指定します。

   1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. リードの強化コンバージョンのトラッキングタグを作成する方法に関する情報を読み、**[!UICONTROL Next]**&#x200B;をクリックします。

   コンバージョン指標を追跡するweb サイトで、コンバージョンタグを作成し、必要に応じて実装します。 手順については、次を参照してください。

   * [!DNL Google] タグを使用するには、「[&#x200B; タグを使用したリードの拡張コンバージョンの設定 [!DNL Google]  タグ &#x200B;](https://support.google.com/google-ads/answer/11347292)」の「[!DNL Google] タグ設定の設定」に関する[!DNL Google Ads]の手順を参照してください。

   * [!DNL Google Tag Manager]を使用するには、「 [!DNL Google Tag Manager][&#128279;](https://support.google.com/google-ads/answer/11021502?#configure)」の「 リードの拡張コンバージョンの設定」の「[!DNL Google] タグ設定の設定」と「設定を確認してコンテナを公開する」の[!DNL Google Ads]の手順を参照してください。

1. **[!UICONTROL Done].**&#x200B;をクリックします

コンバージョンアクションを作成し、コンバージョントラッキングタグを実装したら、組織がキャプチャしたオフラインのコンバージョンデータをアップロードし、コンバージョンアクションに関連付けることができます。 「[&#x200B; オフラインのコンバージョンデータをアップロードしてコンバージョンを強化する](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)」を参照してください。

### コンバージョンアクションの設定 {#conversion-action-settings-google-legacy}

**[!UICONTROL Select an Account]:**&#x200B;該当する[!DNL Google Ads] アカウント。

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
