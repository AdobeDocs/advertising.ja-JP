---
title: （新しいUI）リードの [!DNL Google Ads] 拡張コンバージョンのコンバージョンアクションを作成する
description: リードのコンバージョンを強化するための [!DNL Google Ads]  コンバージョンアクションの作成方法について説明します。
feature: Conversions
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0id: e6916c1b-e939-4e0b-99f5-768e83e1e99f
subfeature_v2: id: d068b149-b9d1-421c-9033-a51495366ddc
source-git-commit: 0bfee2b52410b5cab8e9b3dfba35effc36fc40e1
workflow-type: tm+mt
source-wordcount: 510
ht-degree: 0%

---

# （新しいUI）リードの[!DNL Google Ads]強化コンバージョンのコンバージョンアクションを作成

*Beta機能*

*[!DNL Google Ads]アカウントのみ*

マネージャーのアカウントレベルで追跡されるコンバージョンではなく、個々の[!DNL Google Ads] アカウントで追跡されるリードの強化コンバージョンの[!DNL Google Ads]個のコンバージョンアクションを作成できます。

コンバージョンアクションを作成し、コンバージョントラッキングタグを実装すると、組織がキャプチャしたオフラインのコンバージョンデータを[ アップロードして](conversions-upload-offline-enhanced-conversions.md) コンバージョンアクションに関連付けることができます。

[!DNL Microsoft Advertising] アカウントではサポートを利用できません。

## コンバージョンアクションの作成

1. メインメニューで、**[!UICONTROL Goals]>[!UICONTROL Conversions]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Set up Conversion]**&#x200B;をクリックします。

1. [ コンバージョンアクション設定](#conversion-action-settings-google)を指定します。

   1. [!UICONTROL Setup Method] *[!UICONTROL Create Conversion]*&#x200B;を選択します。

   1. アカウントを選択し、変換タイプを選択します：*[!UICONTROL Import conversion]*。

   1. **[!UICONTROL Next]**&#x200B;をクリックします。

   1. コンバージョンアクションのオプションを指定します。

   1. **[!UICONTROL Review and Save]**&#x200B;をクリックして設定を確認します。

   1. **[!UICONTROL Generate]**&#x200B;をクリックします。

1. リードの強化コンバージョンのトラッキングタグを作成する方法に関する情報を読み、**[!UICONTROL Next]**&#x200B;をクリックします。

   コンバージョン指標を追跡するweb サイトで、コンバージョンタグを作成し、必要に応じて実装する必要があります。 また、リードのコンバージョンを強化し、顧客データの利用条件に同意する必要があります。 手順については、「[ リードのコンバージョンを強化するために [!DNL Google]  タグを設定](https://support.google.com/google-ads/answer/11021502)するための[!DNL Google Ads]手順」を参照してください。

   トランザクション固有のコンバージョン値を追跡する場合は、[ イベントスニペットをカスタマイズ ](https://support.google.com/google-ads/answer/6095947)します。

1. **[!UICONTROL Close].**&#x200B;をクリックします

## コンバージョンアクションの設定 {#conversion-action-settings-google}

### パスセクションの設定

**[!UICONTROL Setup Method]:** アクションの種類：*[!UICONTROL Create Conversion]*

**[!UICONTROL Platform]:**&#x200B;広告ネットワーク：*[!UICONTROL Google]*。

### 「コンバージョンの詳細」セクション

**[!UICONTROL Select Account]:**&#x200B;該当する[!DNL Google Ads] アカウント。

**[!UICONTROL Type of conversions]:**&#x200B;追跡するコンバージョンの種類：*[!UICONTROL Import conversion]*&#x200B;を選択します。 他のすべてのタイプは、他のタイプのコンバージョンのコンバージョントラッキングタグ（コンバージョンアクションではなく）を作成するために使用されます。

### 「コンバージョン設定」セクション

**[!UICONTROL Conversion Name]:**&#x200B;変換アクションの一意の名前。

**[!UICONTROL Goal Category]:** コンバージョンカテゴリ（*適格リード*&#x200B;または&#x200B;*サインアップ*&#x200B;など）。

**[!UICONTROL Preferred Action optimization]:**&#x200B;目標が&#x200B;*[!UICONTROL Primary action used for bidding optimization]*&#x200B;か&#x200B;*[!UICONTROL Secondary action not used for bidding optimization]*&#x200B;か。

**[!UICONTROL Conversion Value]:**&#x200B;各コンバージョンの[値を測定する方法](https://support.google.com/google-ads/answer/13064207):

* 通貨を選択し、各変換の値を入力する必要がある&#x200B;*[!UICONTROL Use the same value for each conversion],*。

* 通貨を選択し、各変換の既定値を入力する必要がある&#x200B;*[!UICONTROL Use different values for each conversion],*。 特定のweb ページにタグを実装する場合、タグのデフォルト値をトランザクション固有の値に変更できます。

* *[!UICONTROL Don't use a value for this conversion action (Not recommended)]*

**[!UICONTROL Count]:** [ クリックまたはインタラクションごとにカウントするコンバージョン数](https://support.google.com/google-ads/answer/3438531): *[!UICONTROL Every (Recommended for every purchases because every purchase is valuable)]*&#x200B;または&#x200B;*[!UICONTROL One (Recommended for leads, sign-ups and other conversions for which only the first interaction is valuable)]*。

**[!UICONTROL Click-Through Conversion Window]:** コンバージョンを記録する広告インタラクションの後最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL View-Through Conversion Window]:** ビュースルーコンバージョンが記録される、ユーザーが広告を表示してから経過した最大日数。 検索キャンペーン、ディスプレイキャンペーン、ショッピングキャンペーンの場合、ウィンドウは1～90日です。 数値を選択するか、**[!UICONTROL Custom]**&#x200B;を選択して数値を入力します。

**[!UICONTROL Attribution Model]:** [各広告インタラクションのクレジットを決定するアトリビューションモデル ](https://support.google.com/google-ads/answer/6259715?sjid=8211249329930775138): *[!UICONTROL Data driven]*&#x200B;または&#x200B;*[!UICONTROL Last click]*。

>[!MORELIKETHIS]
>
>* [ （新しいUI） オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [ オフラインのコンバージョンデータをアップロードしてコンバージョンを強化](/help/search-social-commerce/admin/conversion-metrics/upload-data-offline-conversions.md)
>* [実装 [!DNL Google Ads]  リードの拡張コンバージョン ](/help/search-social-commerce/campaign-management/special-workflows/google-enhanced-conversions-leads.md)
