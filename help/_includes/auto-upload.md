---
source-git-commit: bef353542ee73d32b8ac53e6abd3265528be154f
workflow-type: tm+mt
source-wordcount: '195'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定の自動アップロードフィールド

**[!UICONTROL Auto Upload]:** （同期されたキャンペーンで [!UICONTROL EF Redirect] のみを使用する場合）次回の検索、ソーシャルおよびCommerceの同期時に、次のものを広告ネットワークに自動的にアップロードします。（a）トラッキングテンプレートの検索、ソーシャルおよびCommerceトラッキングパラメーターと、最終 URL に追加された同じパラメーター、または（b）検索、ソーシャルおよびCommerceのトラッキングコードを埋め込んだ新しい宛先 URL。 [Adobe AdvertisingとAdobe Analyticsの統合 ](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) およびサーバーサイドの AMO ID （s_kwcid）設定を持つ広告主の場合、アップロードには [!DNL Google Ads] アカウントと [!DNL Microsoft Advertising] アカウントの [AMO ID パラメーター ](/help/integrations/analytics/ids.md#amo-id) も含まれます。 デフォルトのアカウントレベルの設定は、広告主のトラッキング設定から継承されます。 アカウントレベルの設定は、キャンペーンレベルで上書きできます。

**メモ：** トラッキング URL は、同期していないエンティティ（追加された新しいエンティティと、プロパティが変更された既存のエンティティ）でのみ毎日更新されます。 したがって、既存の広告主/アカウント/キャンペーンに対してこの設定を無効から有効に変更した場合、既に同期している既存のエンティティのトラッキング URL は更新されません。 既存の同期内エンティティの URL にトラッキングを追加するには、Adobeアカウントチームに連絡して、1 回限りの手動による同期プロセスをリクエストします。 自動アップロードプロセスは、今後の変更に対応します。
