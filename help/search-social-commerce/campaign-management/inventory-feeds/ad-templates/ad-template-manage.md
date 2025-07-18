---
title: 在庫フィードの広告テンプレートの管理
description: アカウント構造を管理し、動的広告を配信するためにインベントリデータを処理できる広告テンプレートの管理について説明します。
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: d0f1c413134a0868ddec79ded7672af316267edd
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# 在庫フィードの広告テンプレートの管理

*[!DNL Google Ads]、[!DNL Microsoft Advertising]、[!DNL Yahoo! Japan Ads] （削除アクションのみ）および [!DNL Yandex] アカウントのみ*

データをアップロードする前または後に、データを処理できる検索エンジン固有の広告テンプレートを作成できます。 テキスト広告や拡張/拡張テキスト広告、[!DNL Google Ads] および [!DNL Microsoft Advertising] レスポンシブ検索広告、[!DNL Google Ads] および [!DNL Microsoft Advertising] のショッピング広告用のテンプレートを作成できます。

各テンプレートを 1 つのフィードファイル、[!DNL Google Merchant Center] のアカウントまたは [!DNL Microsoft Merchant Center] のアカウントに関連付けることができます。また、複数のテンプレートを同じフィードファイルまたはアカウントに関連付けることもできます。 広告テンプレートには、アップロードされたファイルまたはアカウントの実際のデータ列で置き換えられた変数を含めることができます。 ほとんどの場合、変数には [ モディファイアグループ ](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) も含めることができます。検索、ソーシャル、Commerceで設定して、データファイルの該当する行ごとに複数の広告、キーワード、キャンペーンまたは広告グループを作成します。 テンプレートオプションを使用すると、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成したり、広告を既存のアカウント構造にマッピングしたりできます。

新しいテンプレートをゼロから作成する以外にも、既存のテンプレートを複製して新しいテンプレートを作成したり、既存のテンプレートを編集したりできます。

テンプレートを作成してデータフィードファイルまたはマーチャントセンターアカウントに関連付けると、テンプレートを通じてファイルにデータを伝播し、キャンペーンデータとアカウント構造を作成できます。必要に応じて、レビュー用または広告ネットワークへの即時投稿用のバルクシートファイルを作成できます。

任意のテンプレートをアクティブ化、一時停止、削除できます。 フィードデータは、アクティブなテンプレートを介してのみ自動的に伝播できます。 ただし、一時停止されたテンプレートを使用して手動でデータを伝えることはできます。

## フィードテンプレートの作成、クローンまたは編集

テキスト広告、拡張/拡張テキスト広告、レスポンシブ検索広告、[!DNL Google Ads] のショッピング広告および [!DNL Microsoft Advertising] のショッピング広告に対して、個別のテンプレートを作成します。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

1. 次のいずれかの操作を行います。

   * テンプレートをゼロから作成するには、データテーブルの上にあるツールバーの **[!UICONTROL Create/Clone]** をクリックし、該当する広告ネットワークを選択します。

   * 既存のテンプレートを複製するには：

      1. コピーするテンプレートの横にあるチェックボックスをオンにします。

      1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Create/Clone]**] をクリックし、該当する広告ネットワークを選択します。

   * （既存のテンプレートを編集する場合）テンプレート名の横にある ![ 設定を表示/編集 ](/help/search-social-commerce/assets/settings.png " 設定を表示/編集 ") をクリックします。

1. [ テキスト広告テンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md)、[[!DNL Google Ads]  ショッピング広告テンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md) または [[!DNL Microsoft Advertising]  ショッピング広告テンプレート ](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md) の設定を指定します。

   1. テンプレート設定ウィンドウの上部で、テンプレート名と該当するアカウントを指定します。

      既存のテンプレートを複製する場合は、新しいテンプレートから作成された広告がソーステンプレートから作成された広告に関連付けられないように、新しいテンプレートの名前を変更します。

   1. （オプション）左の列で、テンプレートを通じてデータが伝播される商品フィードファイルまたはマーチャントセンターアカウントを指定します。

      * （製品フィードファイルの場合）以前にアップロードしたファイルを選択するには、![ 下向き矢印 ](/help/search-social-commerce/assets/arrow-down-dropdown.png " 下向き矢印 ") をクリックし、使用可能なフィードファイルのリストからファイルを選択します。 新しいファイルをアップロードするには、フル パスとファイル名を入力するか、[**[!UICONTROL Browse]**] をクリックしてデバイスまたはネットワーク上のファイルを探し、[**[!UICONTROL Upload]**] をクリックして、ファイルを指定します。

      * （同期されたマーチャントセンターアカウントの場合）アカウント名を選択します。

      選択したファイルまたはアカウントの列が表示されます。

   1. 「**[!UICONTROL Account Structure]**」タブで、勘定科目構造の設定を指定します。

   1. （テキスト広告のみ）「**[!UICONTROL Keywords]**」タブをクリックし、キーワード設定を指定します。

   1. （テキストおよびレスポンシブ検索広告のみ）「**[!UICONTROL Ads]**」タブをクリックし、次のいずれかの操作をおこないます。

      >[!NOTE]
      >
      >* 標準テキスト広告テンプレートあたり最大 4 つの広告バリエーションテンプレート、拡張/拡張テキスト広告テンプレートあたり 5 つの広告バリエーションテンプレート、レスポンシブ検索広告テンプレートあたり 3 つの広告バリエーションテンプレートを含めることができます。
      >* 各広告グループには、最大 3 つの有効なレスポンシブ検索広告を含めることができます。
      >* 既存の標準テキスト広告のバリエーションを編集することはできず、既存のテンプレートは標準テキスト広告を生成しなくなりました。
      >* 広告バリエーションテンプレートを変更すると、（広告タイプと広告ネットワークに応じて [ テンプレートを介してデータを伝播する際に、既存の広告が削除され、新しい広告が作成される場合があ ](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md) ます。

      * 広告バリエーションを追加するには、次の手順を実行します。

         1. 「**[!UICONTROL Add Ad Variation]**」をクリックしてテキスト広告を作成する場合 **[!UICONTROL Add ETA Variation]**、展開/拡張テキスト広告を作成する場合、または「**[!UICONTROL Add RSA Variation]**」をクリックしてレスポンシブテキスト広告を作成する場合があります。

            広告タイプを指定すると、テンプレートでその広告タイプのみを作成できます。

         1. 広告設定を指定します。

            レスポンシブ検索広告の場合は、3 ～ 15 のヘッドラインと 2 ～ 4 の説明を含めることができます。

         1. （オプション）すべての代替広告コピーフィールドに元の広告コピーフィールドからのテキストを事前入力するには、**[!UICONTROL Prefill]** の横にあるチェックボックスを選択します。

         1. （オプション）広告に別の広告コピーのセットを追加するには、伝播中に動的パラメーターをデータに置き換えた後に、元の広告コピー内のいずれかの行が最大長を超える場合に使用できます。その場合は、「**[!UICONTROL Add Alternate]**」をクリックし、代替値を追加します。

            >[!NOTE]
            >
            >* 「[!UICONTROL Prefill]」オプションを選択した場合、代替フィールドには元のフィールドが事前入力され、必要に応じて編集できます。
            >* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
            >* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。
            >* 各広告コピーフィールドに最大 4 つの代替を指定できます。

         * 広告バリエーションを編集するには、次の手順を実行します。

            1. 広告設定を編集します。

               レスポンシブ検索広告の場合は、3 ～ 15 のヘッドラインと 2 ～ 4 の説明を含めることができます。

            1. （オプション）すべての代替広告コピーフィールドに元の広告コピーフィールドからのテキストを事前入力するには、**[!UICONTROL Prefill]** の横にあるチェックボックスを選択します。

            1. （オプション）広告に別の広告コピーのセットを追加するには、伝播中に動的パラメーターをデータに置き換えた後に、元の広告コピー内のいずれかの行が最大長を超える場合に使用できます。その場合は、「**[!UICONTROL Add Alternate]**」をクリックし、代替値を追加します。

               >[!NOTE]
               >
               >* 「[!UICONTROL Prefill]」オプションを選択した場合、代替フィールドには元のフィールドが事前入力され、必要に応じて編集できます。
               >* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
               >* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。
               >* 各広告コピーフィールドに最大 4 つの代替を指定できます。

         * 広告バリエーションを削除するには、必要に応じて、広告バリエーションの横にある **[!UICONTROL Remove ETA Variation]** （展開/拡張テキスト広告の場合）または **[!UICONTROL Remove RSA Variation]** （レスポンシブ検索広告の場合）をクリックします。

   1. （買い物テンプレートのみ）「**[!UICONTROL Product Groups]**」タブをクリックし、ターゲットにする製品グループに関する情報を指定します。

   1. （オプション）「**[!UICONTROL Feed Filters]**」タブをクリックして、フィードファイル内の伝達する行を指定します。

   1. （オプション） **[!UICONTROL Label Classifications tab]** をクリックし、作成した様々なキャンペーンコンポーネントに割り当てるラベル分類値を指定します。

      1. 「**[!DNL \[Component\] Label Classifications]**」の横にあるチェックボックスをクリックします。

      1. コンポーネントに割り当てるラベル分類ごとに、次の操作を行います。

         1. 「**[!UICONTROL Add Label Classification]**」をクリックします。

         1. ラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

1. テンプレートを保存します。

   * テンプレートを保存するには、[**[!UICONTROL Save]**] をクリックし、もう一度 [**[!UICONTROL Save]**] をクリックします。

   * テンプレートを保存し、指定したデータ ファイルをそのテンプレートに反映するには、[**[!UICONTROL Save]**] をクリックし、[**[!UICONTROL Save & Propagate]**] をクリックします。

## フィードテンプレートのステータスの変更

一時停止されているデータフィードテンプレートをアクティブ化するか、アクティブなデータフィードテンプレートを一時停止できます。

>[!NOTE]
>
>一時停止したテンプレートを使用して手動でデータを伝播することはできますが、データは自動的には伝播されません。

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

1. ステータスを変更する各テンプレートの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Change Status]**] をクリックし、[**[!UICONTROL Activate]**] または [**[!UICONTROL Pause]**] をクリックします。

## フィードテンプレートの削除

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]** をクリックすると、「[!UICONTROL Templates]」タブが開きます。

1. 削除する各テンプレートの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、[**[!UICONTROL Delete]**] をクリックします。

1. 確認メッセージで、「**[!UICONTROL Yes]**」をクリックします。

>[!MORELIKETHIS]
>
>* [ 在庫フィードを使用した広告管理の自動化について ](../inventory-feeds-about.md)
>* [ テキスト広告とレスポンシブ検索広告のテンプレート設定 ](template-text-rsa.md)
>* [[!DNL Google Ads]  ショッピング広告テンプレートの設定 ](template-google-shopping.md)
>* [[!DNL Microsoft Advertising]  ショッピング広告テンプレートの設定 ](template-microsoft-shopping.md)
>* [ テンプレートを使用したフィードデータの伝播 ](../feed-data-propagate.md)
