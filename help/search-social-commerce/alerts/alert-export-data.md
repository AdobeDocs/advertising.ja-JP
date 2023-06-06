---
title: カスタムアラート用のデータのエクスポート
description: トリガーされたアラートのデータをファイルにエクスポートする方法を説明します。
source-git-commit: cd461f73f4a70a5647844a6075ba1c65d64a9b04
workflow-type: tm+mt
source-wordcount: '267'
ht-degree: 0%

---

# カスタムアラート用のデータのエクスポート

トリガーされたアラートのデータや、アラートテンプレートの最近トリガーされたアラートのデータを、 [!DNL Microsoft® Excel] ワークブック ([XLS](/help/search-social-commerce/glossary.md#w-x) ファイル )、タブ区切り値 ([TSV](/help/search-social-commerce/glossary.md#s-t)) ファイルまたはコンマ区切り値 ([CSV](/help/search-social-commerce/glossary.md#c-d)) ファイルです。 ダウンロード可能なレポートは、アラートがトリガーされてから 10 日間使用でき、自動的に削除されます。

1. 次のいずれかの操作を行います。

   * （アラートテンプレートに対して最近トリガーされたアラートのデータをエクスポートするには）メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Custom Alerts]**:[Alert Templates] ビューが開きます。

   * （特定のトリガー済みアラートのデータをエクスポートするには）メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Insights & Reports] >[!UICONTROL Custom Alerts]**. サブメニューで、 **[!UICONTROL Triggered Alerts]**.

1. 内 [!UICONTROL Export] テンプレート名またはレポート名の横の列で、形式の名前をクリックし、ブラウザの通常の手順に従ってファイルを開くか保存します。

   * **[!UICONTROL XLS]** — [!DNL Excel] ワークブックに単一のワークシート (XLS) が含まれる レポートの上部にパラメーターのラベルが付いた 1 つのワークシートが含まれ、コンポーネントのデータが使用可能な場合は、含まれる各コンポーネントに対して 1 行ずつ表示されます。 データのない行は省略されます。 基本レポートには、各数値列の合計が含まれます。

   * **[!UICONTROL TSV]** — TSV ファイル用。 レポートには、含まれるコンポーネントごとに、パラメーターと 1 行が含まれます。

   * **[!UICONTROL CSV]** — CSV ファイル用。 レポートには、含まれるコンポーネントごとに、パラメーターと 1 行が含まれます。

>[!MORELIKETHIS]
>
>* [Custom Alerts について](alert-about.md)
>* [カスタムアラートテンプレートの作成](alert-template-create.md)
>* [カスタムアラートテンプレートの編集](alert-template-edit.md)
>* [カスタムアラートテンプレートの一時停止](alert-template-pause.md)
>* [カスタムアラートテンプレートのアクティブ化](alert-template-activate.md)
>* [カスタムアラートテンプレートの削除](alert-template-delete.md)
>* [カスタムアラートテンプレート設定](alert-template-settings.md)
>* [カスタムアラートの表示](alert-view.md)

