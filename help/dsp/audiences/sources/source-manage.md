---
title: オーディエンスソースを作成および管理してユニバーサル ID オーディエンスをアクティブ化
description: ソースを作成および管理して、顧客データプラットフォームからオーディエンスを読み込み、ユニバーサル ID を含むセグメントに変換する方法を説明します。
feature: DSP Audiences
exl-id: 728130d7-d19c-4d5d-9bca-695f8c17f89b
source-git-commit: 295cc610a7e5e811fe555db69373a8bf5b4012f7
workflow-type: tm+mt
source-wordcount: '369'
ht-degree: 0%

---

# オーディエンスソースを作成してユニバーサル ID オーディエンスを有効化

*ベータ版機能*

DSPで、顧客データプラットフォーム内のファーストパーティオーディエンスごとに、指定したユニバーサル ID タイプを含むセグメントに変換するソースを作成します。 セグメントは、組織のDSP アカウントまたは広告主アカウントに読み込むことができます。 データ料金は、選択したユニバーサル ID タイプに基づいて適用されます。

各顧客データプラットフォームからオーディエンスを取り込むには、追加の手順が必要です。 手順の最後のメモを参照してください。

## オーディエンスソースの作成

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. クリック **[!UICONTROL Add Source]**.

1. が含まれる [!UICONTROL Select a Type] メニューで、顧客データプラットフォームを選択します。

   * *[!UICONTROL RT-CDP]*: [この [!DNL Adobe Real-Time Customer Data Platform]](source-about.md).

   * *[!UICONTROL ActionIQ]*：です [[!DNL ActionIQ] 顧客データプラットフォーム](source-about.md).

   * *[!UICONTROL Tealium CDP]*: （設定されたユーザーのみ）次の [[!DNL Tealium] 顧客データプラットフォーム](source-about.md).

1. を指定 [!UICONTROL Data Visibility Level]: *[!UICONTROL Advertiser]* または *[!UICONTROL Account]*.

1. 残りを入力 [ソース設定](source-settings.md).

   のコピーを保持 [!UICONTROL Source Key] が生成されます。 値は後で必要になります。

1. クリック **[!UICONTROL Save]**.

>[!NOTE]
>
>顧客データプラットフォームのソースを作成したら、追加の手順を完了する必要があります。 を参照してください。 [オーディエンスをから読み込むワークフロー [!DNL Adobe] [!DNL Real-time CDP]](source-adobe-rtcdp.md)<!-- the [activation workflow for [!DNL ActionIQ]](source-actioniq.md), --> および [オーディエンスをから読み込むワークフロー [!DNL Tealium]](source-tealium.md).

## オーディエンスソースの ID タイプの変更

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. カーソルをソース行の上に置き、クリックします **[!UICONTROL Edit]**.

1. 変更： [ソースに対して選択された ID](source-settings.md).

1. クリック **[!UICONTROL Save]**.

## オーディエンスソースの削除

ソースを削除すると、ソースを通じて翻訳されたセグメントが削除されます。<!-- Will performance data for the segment still be available in any types of reports?  If yes, which? -->

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. カーソルをソース行の上に置き、クリックします **[!UICONTROL Delete]**.

1. 確認メッセージで、 **[!UICONTROL Delete]**.

## オーディエンスソースの変更ログの表示

オーディエンスソースレコードに対する変更の詳細を表示したり、オプションでログにメモを添付したりできます。

1. メインメニューで、 **[!UICONTROL Audiences]** > **[!UICONTROL Sources]**.

1. カーソルをソース行の上に置き、クリックします **[!UICONTROL Change log]**.

1. （オプション）変更ログにメモを添付するには、次の手順に従います。

   1. カーソルをソース行の上に置き、クリックします **[!UICONTROL Add Notes]**.

   1. メモを入力し、 **[!UICONTROL Save]**.

      最大長は 256 文字です。

1. （オプション）ログをより詳細な画面で開くには、ソース行の上にカーソルを置いてクリックします **[!UICONTROL View Details]**.

>[!MORELIKETHIS]
>
>* [オーディエンスソース設定](source-settings.md)
>* [ファーストパーティオーディエンスソースについて](source-about.md)
>* [Adobe Advertising Cloud DSP接続](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/advertising/adobe-advertising-cloud-connection.html)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
