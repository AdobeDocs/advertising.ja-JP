---
title: 在庫フィードの広告テンプレートの管理
description: アカウント構造を管理し、動的広告を配信するためにインベントリデータを処理できる広告テンプレートの管理について説明します。
exl-id: b0e540cf-8735-4812-9df5-58f488a25ba5
feature: Search Inventory Feeds
source-git-commit: 67fe8581832dc0762d62908d01672e53cc95b847
workflow-type: tm+mt
source-wordcount: '1423'
ht-degree: 0%

---

# 在庫フィードの広告テンプレートの管理

*[!DNL Google Ads], [!DNL Microsoft Advertising], [!DNL Yahoo! Japan Ads] （削除アクションのみ）、 [!DNL Yandex] アカウントのみ*

データをアップロードする前または後に、データを処理できる検索エンジン固有の広告テンプレートを作成できます。 テキスト広告や拡張テキスト広告のテンプレートを作成できます。 [!DNL Google Ads] および [!DNL Microsoft Advertising] レスポンシブ検索広告と [!DNL Google Ads] および [!DNL Microsoft Advertising] ショッピング広告。

各テンプレートを 1 つのフィードファイル、 [!DNL Google Merchant Center] account、または [!DNL Microsoft Merchant Center] 複数のテンプレートを同じフィードファイルまたはアカウントに関連付けることができます。 広告テンプレートには、アップロードされたファイルまたはアカウントの実際のデータ列で置き換えられた変数を含めることができます。 ほとんどの場合、変数には次の値も含まれます [修飾子グループ](/help/search-social-commerce/campaign-management/inventory-feeds/modifiers-manage.md) 検索、ソーシャル、Commerceでを設定して、データファイル内の該当する行ごとに複数の広告、キーワード、キャンペーンまたは広告グループを作成します。 テンプレートオプションを使用すると、広告の新しいアカウント構造（キャンペーン、広告グループ、キーワード）を作成したり、広告を既存のアカウント構造にマッピングしたりできます。

新しいテンプレートをゼロから作成する以外にも、既存のテンプレートを複製して新しいテンプレートを作成したり、既存のテンプレートを編集したりできます。

テンプレートを作成してデータフィードファイルまたはマーチャントセンターアカウントに関連付けると、テンプレートを通じてファイルにデータを伝播し、キャンペーンデータとアカウント構造を作成できます。必要に応じて、レビュー用または広告ネットワークへの即時投稿用のバルクシートファイルを作成できます。

任意のテンプレートをアクティブ化、一時停止、削除できます。 フィードデータは、アクティブなテンプレートを介してのみ自動的に伝播できます。 ただし、一時停止されたテンプレートを使用して手動でデータを伝えることはできます。

## フィードテンプレートの作成、クローンまたは編集

テキスト広告と拡張/テキスト広告、レスポンシブ検索広告に対して個別のテンプレートを作成します。 [!DNL Google Ads] ショッピング広告 [!DNL Microsoft Advertising] ショッピング広告。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

1. 次のいずれかの操作を行います。

   * テンプレートをゼロから作成するには、 **[!UICONTROL Create/Clone]** データテーブルの上にあるツールバーで、該当する広告ネットワークを選択します。

   * 既存のテンプレートを複製するには：

      1. コピーするテンプレートの横にあるチェックボックスをオンにします。

      1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Create/Clone]**&#x200B;を選択してから、該当する広告ネットワークを選択します。

   * （既存のテンプレートを編集するには）テンプレート名の横にある ![設定の表示/編集](/help/search-social-commerce/assets/settings.png "設定の表示/編集").

1. の設定を指定します [テキスト広告テンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-text-rsa.md), [[!DNL Google Ads] ショッピング広告テンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-google-shopping.md)、または [[!DNL Microsoft Advertising] ショッピング広告テンプレート](/help/search-social-commerce/campaign-management/inventory-feeds/ad-templates/template-microsoft-shopping.md):

   1. テンプレート設定ウィンドウの上部で、テンプレート名と該当するアカウントを指定します。

      既存のテンプレートを複製する場合は、新しいテンプレートから作成された広告がソーステンプレートから作成された広告に関連付けられないように、新しいテンプレートの名前を変更します。

   1. （オプション）左の列で、テンプレートを通じてデータが伝播される商品フィードファイルまたはマーチャントセンターアカウントを指定します。

      * （製品フィードファイルの場合）以前にアップロードしたファイルを選択するには、をクリックします ![下矢印キー](/help/search-social-commerce/assets/arrow-down-dropdown.png "下矢印キー") 使用可能なフィードファイルのリストからファイルを選択します。 新しいファイルをアップロードするには、フルパスとファイル名を入力するか、をクリックして、ファイルを指定します **[!UICONTROL Browse]** をクリックして、デバイスまたはネットワーク上のファイルを検索し、 **[!UICONTROL Upload]**.

      * （同期されたマーチャントセンターアカウントの場合）アカウント名を選択します。

      選択したファイルまたはアカウントの列が表示されます。

   1. 日 **[!UICONTROL Account Structure]** タブで、アカウント構造設定を指定します。

   1. （テキスト広告のみ）をクリックします **[!UICONTROL Keywords]** タブをクリックし、キーワード設定を指定します。

   1. （テキストおよびレスポンシブ検索広告のみ）をクリックします **[!UICONTROL Ads]** タブをクリックし、次のいずれかの操作を行います。

      >[!NOTE]
      >
      >* 標準テキスト広告テンプレートあたり最大 4 つの広告バリエーションテンプレート、拡張/拡張テキスト広告テンプレートあたり 5 つの広告バリエーションテンプレート、レスポンシブ検索広告テンプレートあたり 3 つの広告バリエーションテンプレートを含めることができます。
      >* 各広告グループには、最大 3 つの有効なレスポンシブ検索広告を含めることができます。
      >* 既存の標準テキスト広告のバリエーションを編集することはできず、既存のテンプレートは標準テキスト広告を生成しなくなりました。
      >* 広告バリエーションテンプレートを変更すると、テンプレートを使用してデータを伝播する際に、既存の広告が削除され、新しい広告が作成される場合があります。 [広告の種類と広告ネットワークに応じて](/help/search-social-commerce/campaign-management/inventory-feeds/when-are-components-created-deleted.md).

      * 広告バリエーションを追加するには、次の手順を実行します。

         1. クリック **[!UICONTROL Add Ad Variation]** テキスト広告を作成するには、 **[!UICONTROL Add ETA Variation]** 拡張/拡張テキスト広告を作成する **[!UICONTROL Add RSA Variation]** レスポンシブテキスト広告を作成する。

            広告タイプを指定すると、テンプレートでその広告タイプのみを作成できます。

         1. 広告設定を指定します。

            レスポンシブ検索広告の場合は、3 ～ 15 のヘッドラインと 2 ～ 4 の説明を含めることができます。

         1. （オプション）すべての代替広告コピーフィールドに元の広告コピーフィールドからのテキストを事前入力するには、の横にあるチェックボックスをオンにします **[!UICONTROL Prefill]**.

         1. （オプション）広告に別の広告コピー・セットを追加するには、伝播中に動的パラメータをデータに置換した後、元の広告コピーのいずれかの行が最大長を超える場合に使用できます。 **[!UICONTROL Add Alternate]**&#x200B;を選択してから、別の値を追加します。

            >[!NOTE]
            >
            >* 次の場合 [!UICONTROL Prefill] オプションを選択すると、代替フィールドに元のフィールドが事前入力され、必要に応じて編集できます。
            >* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
            >* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。
            >* 各広告コピーフィールドに最大 4 つの代替を指定できます。

         * 広告バリエーションを編集するには、次の手順を実行します。

            1. 広告設定を編集します。

               レスポンシブ検索広告の場合は、3 ～ 15 のヘッドラインと 2 ～ 4 の説明を含めることができます。

            1. （オプション）すべての代替広告コピーフィールドに元の広告コピーフィールドからのテキストを事前入力するには、の横にあるチェックボックスをオンにします **[!UICONTROL Prefill]**.

            1. （オプション）広告に別の広告コピー・セットを追加するには、伝播中に動的パラメータをデータに置換した後、元の広告コピーのいずれかの行が最大長を超える場合に使用できます。 **[!UICONTROL Add Alternate]**&#x200B;を選択してから、別の値を追加します。

               >[!NOTE]
               >
               >* 次の場合 [!UICONTROL Prefill] オプションを選択すると、代替フィールドに元のフィールドが事前入力され、必要に応じて編集できます。
               >* 最大長を超える広告コピーフィールドのみが代替値に置き換えられます。 例えば、元のヘッドラインまたはタイトルのみが長すぎる場合、生成された広告バリエーションでは、代替ヘッドラインまたはタイトルと元の説明が使用されます。 したがって、元の広告コピーと組み合わせる際には、代替の広告コピーが理にかなっていることを確認してください。
               >* 元の広告コピーが検索エンジンの長さの要件を満たしている場合、代替広告コピーは破棄されます。
               >* 各広告コピーフィールドに最大 4 つの代替を指定できます。

         * 広告バリエーションを削除するには、をクリックします **[!UICONTROL Remove ETA Variation]** （拡張/拡張テキスト広告の場合）または **[!UICONTROL Remove RSA Variation]** （レスポンシブ検索広告の場合）必要に応じて広告バリエーションの横に表示されます。

   1. （ショッピングテンプレートのみ）をクリックします **[!UICONTROL Product Groups]** タブをクリックし、ターゲットにする製品グループに関する情報を指定します。

   1. （任意） **[!UICONTROL Feed Filters]** タブをクリックし、フィードファイル内のどの行を伝播するかを指定します。

   1. （任意） **[!UICONTROL Label Classifications tab]**&#x200B;次に、作成する様々なキャンペーンコンポーネントに割り当てるラベル分類の値を指定します。

      1. の横にあるチェックボックスをクリックします。 **[!DNL \[Component\] Label Classifications]**.

      1. コンポーネントに割り当てるラベル分類ごとに、次の操作を行います。

         1. クリック **[!UICONTROL Add Label Classification]**.

         1. ラベル分類を選択し、既存の値を選択するか、新しい値を入力します。

1. テンプレートを保存します。

   * テンプレートを保存するには、をクリックします。 **[!UICONTROL Save]**&#x200B;を選択し、 **[!UICONTROL Save]** また。

   * テンプレートを保存し、指定したデータ・ファイルをテンプレートに反映するには、 **[!UICONTROL Save]**&#x200B;を選択し、 **[!UICONTROL Save & Propagate]**.

## フィードテンプレートのステータスの変更

一時停止されているデータフィードテンプレートをアクティブ化するか、アクティブなデータフィードテンプレートを一時停止できます。

>[!NOTE]
>
>一時停止したテンプレートを使用して手動でデータを伝播することはできますが、データは自動的には伝播されません。

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

1. ステータスを変更する各テンプレートの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Change Status]**&#x200B;を選択し、 **[!UICONTROL Activate]** または **[!UICONTROL Pause]**.

## フィードテンプレートの削除

1. メインメニューで、 **[!UICONTROL Search]> [!UICONTROL Campaigns] >[!UICONTROL Advanced (ACM)]**&#x200B;が開き、が表示されます。 [!UICONTROL Templates] タブ。

1. 削除する各テンプレートの横にあるチェックボックスをオンにします。

1. データ テーブルの上にあるツールバーで、 **[!UICONTROL Delete]**.

1. 確認メッセージで、 **[!UICONTROL Yes]**.

>[!MORELIKETHIS]
>
>* [在庫フィードを使用した広告管理の自動化について](../inventory-feeds-about.md)
>* [テキスト広告とレスポンシブ検索広告テンプレートの設定](template-text-rsa.md)
>* [[!DNL Google Ads] 買い物とテンプレートの設定](template-google-shopping.md)
>* [[!DNL Microsoft Advertising] 買い物とテンプレートの設定](template-microsoft-shopping.md)
>* [テンプレートを使用したフィードデータの伝播](../feed-data-propagate.md)
