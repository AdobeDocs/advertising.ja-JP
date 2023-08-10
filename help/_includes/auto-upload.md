---
source-git-commit: 6e5d79eb9c04a12813c42e33a2228c69f2adbaae
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---
# アカウント設定とキャンペーン設定の「自動アップロード」フィールド

**[!UICONTROL Auto Upload]:** （と同期したキャンペーンの場合） [!UICONTROL EF Redirect] ) 次回検索で、Social、&amp;Commerce が広告ネットワークに自動的にアップロードします。(a) トラッキングテンプレートと最終 URL に追加された同じパラメーター、(b) 検索、Social、&amp;Commerce トラッキングコードに埋め込まれた新しい宛先 URL 用の検索、Social、およびコマース。 次の条件を満たす広告主の場合： [Adobe AdvertisingとAdobe Analyticsの統合](https://experienceleague.adobe.com/docs/advertising/integrations/analytics/overview.html) およびサーバー側 AMO ID(s_kwcid) 設定の場合、アップロードには [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウント。 デフォルトのアカウントレベルの設定は、広告主のトラッキング設定から継承されます。 キャンペーンレベルでアカウントレベルの設定を上書きできます。

**注意：** トラッキング URL は、同期されていないエンティティ（つまり、追加された新しいエンティティや、プロパティが変更された既存のエンティティ）に対してのみ、毎日更新されます。 したがって、この設定を無効から既存の広告主、アカウント、キャンペーンに対して有効に変更した場合、既に同期している既存のエンティティのトラッキング URL は更新されません。 既存の同期内エンティティの URL にトラッキングを追加するには、担当のAdobeアカウントチームに連絡して、1 回限りの手動同期プロセスをリクエストします。 自動アップロードプロセスでは、今後の変更を処理します。
