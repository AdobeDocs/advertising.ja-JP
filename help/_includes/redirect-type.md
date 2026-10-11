---
source-git-commit: 029e406fbfb4217ce78364c2d1f1a6dae24ff588
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%
---
# アカウントおよびキャンペーン設定の「リダイレクトタイプ」フィールド

**[!UICONTROL Redirect Type]:** （[!UICONTROL EF Redirect]のみ）エンドユーザーを最終URLまたは宛先URLにリダイレクトする方法。 選択したオプションは、アカウントまたはキャンペーン内のすべての広告、キーワード、およびプレースメントに適用されます。 デフォルトのアカウントレベル設定は広告主のトラッキング設定から継承され、デフォルトのキャンペーンレベル設定はアカウント設定から継承されます。

* *[!UICONTROL Standard]:* エンドユーザーを指定されたURLにリダイレクトするだけです。

* *[!UICONTROL Token]:* エンドユーザーをURLにリダイレクトし、クリック用の検索、ソーシャル、およびCommerce ID （`ef_id`）をクエリ文字列パラメーターとして記録します。このパラメーターはトークンとして使用されます。 オフラインのトランザクションをレポートする場合、Search、Social、およびCommerceでAdobe Analyticsとデータを交換する場合、または[!DNL Apple Safari] ブラウザー内で発生するすべてのコンバージョンをトラッキングする場合は、このオプションを選択します。

**メモ：**

* [!UICONTROL Standard]から[!UICONTROL Token]に切り替える場合、またはその逆の場合は、アカウントのトラッキング URLを再生成する必要があります。
* アカウントレベルの設定は、キャンペーンレベルで上書きできます。
