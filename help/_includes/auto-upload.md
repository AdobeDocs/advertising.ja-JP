---
source-git-commit: 546e391745b1469efbcc9c2024dfc193224f0ed0
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 0%

---
# アカウントおよびキャンペーン設定の自動アップロードフィールド

**[!UICONTROL Auto Upload]:** （[!UICONTROL EF Redirect]との同期キャンペーンの場合のみ）次の項目が次回Search, Social, &amp; Commerceと同期されるときに、自動的に広告ネットワークにアップロードされます。（a） トラッキングテンプレートと最終URLに追加された同じパラメーター、または（b） Search, Social, &amp; Commerce トラッキングコードに埋め込まれた新しい宛先URL。 [Adobe AdvertisingとAdobe Analyticsの統合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html)およびサーバーサイド AMO ID （s_kwcid）設定を持つ広告主の場合、アップロードには[&#x200B; アカウントと](https://experienceleague.adobe.com/en/docs/analytics/components/dimensions/amo-id) アカウントの[!DNL Google Ads]AMO ID パラメーター[!DNL Microsoft Advertising]も含まれます。 デフォルトのアカウントレベル設定は、広告主のトラッキング設定から継承されます。 アカウントレベルの設定は、キャンペーンレベルで上書きできます。

**注：** トラッキング URLは、同期されていないエンティティ（追加された新しいエンティティとプロパティが変更された既存のエンティティ）に対してのみ、毎日更新されます。 したがって、既存の広告主/アカウント/キャンペーンに対してこの設定を「無効」から「有効」に変更した場合、既に同期している既存のエンティティのトラッキング URLは更新されません。 既存の同期中のエンティティのURLにトラッキングを追加するには、Adobe アカウントチームに連絡し、1回限りの手動同期プロセスをリクエストしてください。 自動アップロードプロセスは、今後の変更を処理します。
