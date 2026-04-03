---
title: '[!DNL Baidu] キーワード設定'
description: ' [!DNL Baidu]  キーワードの設定を参照してください。'
exl-id: 3b3a578b-06f1-486f-9ade-9104e0a1dd5f
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/uMU0oAkL8rmsOIMXYR8qgp9-upe2qWIK-ev1YtPQUb4
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 230
ht-degree: 0%

---

# [!DNL Baidu] キーワード設定

## [!UICONTROL Keyword Details]

**[!UICONTROL Keywords]:** キーワード。 キーワードごとの最大長は、30個の1 バイトまたは15個の2 バイト文字です

最大2000個のキーワードを入力または貼り付けることができます。 複数のキーワードをコンマで区切るか、別々の行に入力します。 次の構文を使用します。

* `keyword` （部分一致）
* フレーズ一致の`"keyword"`
* 完全一致の`[keyword]`

>[!NOTE]
>
>* [!DNL Baidu]では、広告グループごとにキーワードごとに1つの一致タイプのみが許可されます。 例えば、広告グループ 1に`"keyword"`と`[keyword]`の両方を含めることはできません。
>* 負のキーワードは、[!UICONTROL Keywords] > [!UICONTROL Negatives] ビューと、広告グループおよびキャンペーン設定で作成できます。
>* [!DNL Baidu] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード IDを持つ新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。

**[!UICONTROL Status]:** キーワードの表示ステータス：*アクティブ*&#x200B;または&#x200B;*一時停止*。 新しいキーワードのデフォルトは&#x200B;*Active*&#x200B;です。

## [!UICONTROL Bids]

<!-- **[!UICONTROL Bid]:** -->

{{$include /help/_includes/bid-keyword.md}}

## URL オプション

**[!UICONTROL Base URL]:** （キーワードレベルのトラッキングを含むキャンペーンのみ。オプション）ユーザーが広告をクリックしたときに取得されるランディングページ URL。 次を含めることができます
サードパーティのリダイレクトとトラッキングコード。 値を入力すると、広告のベース URLが上書きされます。

レコードを保存すると、ベース URLには、キャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。

Adobe Advertising コンバージョントラッキングサービスを使用し、キャンペーン設定に[!UICONTROL EF Redirect]を使用してキーワードレベルでトラッキングを追加する場合、Search, Social, &amp; Commerceは自動的に独自のクリックトラッキングコードを追加します。

>[!MORELIKETHIS]
>
>* [&#x200B; キーワードの管理](/help/search-social-commerce/campaign-management/campaigns/keyword-manage.md)
