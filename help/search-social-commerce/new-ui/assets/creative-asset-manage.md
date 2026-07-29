---
title: クリエイティブアセットの表示と作成
description: ' [!DNL Google Ads] および [!DNL Microsoft Advertising]  アカウントレベルのアセットライブラリで再利用可能な画像、ビデオ、テキストアセットを表示および作成する方法について説明します。'
feature: Search Campaign Management
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
subfeature_v2: id: f3d33161-c519-436e-bbbd-730ba428736b
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 47301d06bc2a06c2601107abd988e787114e36bb
workflow-type: tm+mt
source-wordcount: 492
ht-degree: 0%

---


# クリエイティブアセットの表示と作成

*[!DNL Google Ads]および[!DNL Microsoft Advertising] アカウントのみ*

[!UICONTROL Assets] > [!UICONTROL Creatives]では、[!DNL Google Ads]および[!DNL Microsoft Advertising]のアカウントレベルのアセットライブラリで、再利用可能なすべての画像、ビデオ、および（2}の場合のみ）テキストアセットを表示できます。 [!DNL Google Ads]このリストには、[!DNL AI Max]対応キャンペーンの[!DNL Google Ads]広告グループに対してAIが生成したアセットが含まれています。

広告ネットワークアカウントの新しいアセットを手動で作成し、広告ネットワークにアップロードできます。 <!-- Verify if you can use the AI-generated ones --> アップロードしたアセットは、パフォーマンスの最大化キャンペーンに使用できます。

AIが生成したテキストアセットを、関連する広告グループから削除することもできます。

## クリエイティブアセットを表示

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Creatives]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

   デフォルトでは、[!UICONTROL Image] タブが開きます。

1. &lt; （オプション） **[!UICONTROL Video]**&#x200B;と&#x200B;**[!UICONTROL Text]** タブをクリックして、これらの形式のアセットを表示します。

1. （オプション）利用可能な条件で、任意のタブをフィルタリングします。

## アセットの作成とアップロード

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Creatives]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

1. **[!UICONTROL Upload Creatives]**&#x200B;をクリックします。

1. **[!UICONTROL Asset Type]**&#x200B;を選択します。

1. アセットをアップロードまたは入力します。

   * 画像アセット用：

     1. **[!UICONTROL +]**&#x200B;をクリックし、デバイスまたはネットワークから画像を選択します。

        各画像は最大10 MBまで指定できます。 一度に最大200 MBの画像をアップロードできます。

     1. 各画像について：

        1. 縦横比を選択します。

        1. 必要に応じて切り抜きボックスをドラッグして配置し、画像の表示可能部分を選択し、可能な限り画像の表示可能部分のサイズを変更します。

        1. （オプション）追加の縦横比を選択し、オプションで、選択した縦横比ごとに必要に応じて画像の位置とサイズを変更します。

           選択した縦横比ごとに1つのアセットが作成されます。

        1. **[!UICONTROL Proceed]**&#x200B;をクリックします。

   * ビデオアセットの場合は、10秒以上の[!DNL YouTube]動画のURLを入力します。 別のビデオアセットを追加するには、**[!UICONTROL + Add video]**&#x200B;をクリックし、別のURLを入力します。

     一度に最大10個の動画URLを投稿できます。

   * （[!DNL Google Ads] アカウントのみ） テキストアセットの場合は、テキスト文字列を入力します。 別のテキストアセットを追加するには、**[!UICONTROL + Add text]**&#x200B;をクリックし、別のテキスト文字列を入力します。

     各テキストアセットには、最大1000文字を設定できます。 一度に最大10個のテキストアセットをアップロードできます。

     後で、選択した広告要素（見出しや短い説明など）に対して、その広告要素の文字制限を満たす限り、テキストアセットを使用できます。

1. **[!UICONTROL Upload]**&#x200B;をクリックします。

## AI生成クリエイティブアセットの削除<!-- AI-generated ones also, or any? -->

<!-- Possible in bulksheets, too?  What about manual creation? -->

[!DNL AI Max]対応キャンペーン *の広告グループに対して*[!DNL Google Ads]&#x200B;個のアセットが自動的に生成されました

削除されたテキストアセットは再度提供されませんが、パフォーマンスデータはレポートで引き続き利用できます。

1. メインメニューで、**[!UICONTROL Assets]>[!UICONTROL Creatives]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

   デフォルトでは、[!UICONTROL Image] タブが開きます。

1. &lt; （オプション） **[!UICONTROL Video]**&#x200B;と&#x200B;**[!UICONTROL Text]** タブをクリックして、これらの形式のアセットを表示します。

1. &lt;必要に応じてアセットをフィルタリングします。

   [!DNL AI Max]対応キャンペーンの[!DNL Google Ads]広告グループからAIが生成したアセットには、[!UICONTROL Source]の種類「[!UICONTROL Automatically Created]」があります。

1. 各アセットの横にあるチェックボックスを選択して、広告グループから削除します。

1. 一括操作ツールバーで、**[!UICONTROL Remove]**&#x200B;をクリックします。

1. <!-- VERIFY -->確認メッセージで、**[!UICONTROL Remove]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [[!DNL Google Ads]  キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-google.md)
>* [[!DNL Microsoft Advertising]  キャンペーン設定](/help/search-social-commerce/campaign-management/campaigns/campaign-settings-microsoft.md)
