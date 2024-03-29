---
title: デフォルトビューとカスタムビューの管理
description: デフォルトのビューとカスタムビューをカスタマイズする方法を説明します。
exl-id: b28f58f6-c80a-45f8-8c5f-b821a76dab6d
feature: Search Common Tasks, Search Custom Data Views
source-git-commit: f21283731d7a1830af585cec43805c54c81c72ff
workflow-type: tm+mt
source-wordcount: '2833'
ht-degree: 0%

---

# デフォルトビューとカスタムビューの管理

デフォルトのビューとカスタムビューを使用すると、検索キャンペーンのデータビュー内に表示されるパフォーマンスデータをカスタマイズできます。 表示設定には、含める列、フィルター、日付範囲、コンバージョン属性設定、その他の詳細設定が含まれ、設定を一時的に適用するか、保存することができます。 （例外：デフォルトビューのフィルターは保存できません。） 各デフォルトおよび通常のカスタムビューは、特定のエンティティビュー ( [!UICONTROL Campaigns]) および特定の広告主アカウントのみを表示できます。 各ユニバーサルカスタムビューは、特定の広告主のエンティティビュー間で適用できるので、エンティティのタイプによって異なるプロパティ列（エンティティ名やステータスなど）を含めることはできません。

デフォルトのビューは、ログインするたびにデフォルトで表示されます。 追加のカスタムビューを作成して、いつでも適用できます。 オプションで、作成した任意のカスタムビューを、広告主のデータを表示できる他のすべてのユーザーと共有できます。 ビューリストでは、別のユーザーが共有している各ビューは、「*最も効果の高いキャンペーン*.&quot; カスタムビューを作成したユーザーのみが削除できます。

各ビューは、 [!UICONTROL Custom Views] 」セクションに表示されます。

## デフォルトまたはカスタムビューの適用

* （デフォルトの表示）メインメニューで、 **[!UICONTROL Search]** \> **[!UICONTROL Campaigns]** \> **[!UICONTROL Campaigns]**. サブメニューで、 **[!UICONTROL Live]** \> **\[ エンティティタイプ\]**.

* （カスタムビュー）左側のナビゲーションパネルから、次の操作を実行します。

   1. 左側のパネルで、 **[!UICONTROL Custom Views]** メニューを使用して展開します。

      ビューは、適用可能なエンティティで並べ替えられます。

   1. 使用可能なメニューを展開します。

      &quot;[!UICONTROL Universal Views]「 」には、すべてのエンティティビューで使用できるカスタムビューが含まれます。 その他のすべてのカスタムビューは、エンティティタイプ別にグループ化されます。

   1. ビュー名をクリックします。

      ビューがユニバーサルであるか、現在のエンティティに適用される場合は、ビューの設定に従ってデータテーブルが再表示されます。 ビューが異なるエンティティに適用される場合は、該当するエンティティのデータがビュー設定に従って表示されます。

## カスタムビューの作成 {#create-custom-view}

カスタムビューは、キャンペーン管理ビューにのみ適用できます。

>[!NOTE]
>
>カスタム表示に対して指定した表示設定に加えて、現在の列の並べ替え順も保存されます。

1. データテーブルの上のツールバーの右側で、現在のビューの名前 (「[!UICONTROL Default]」) をクリックします。

1. 次を指定します。 [カスタムビュー設定](#view-settings):

   1. （オプション）すべてのエンティティ表示でデータ設定を使用できるようにする ( [!UICONTROL Campaigns], [!UICONTROL Ads]など )、「 」を選択します。 **[!UICONTROL Universal View]**.

      このオプションを有効または無効にした後は、既存のビューに対する変更を保存することはできませんが、変更を含む新しいビューを作成することはできます。

   1. （オプション）広告主のデータを表示できる他のすべてのユーザーがこのビューを利用できるようにするには、 **[!UICONTROL Shared]** スライダーで設定 *[!UICONTROL Yes]*.

   1. （オプション） **[!UICONTROL Columns]** 」タブで、タブで使用できる列、列の順序、行の並べ替え方法を変更します。

   1. （オプション） **[!UICONTROL Filters]** 」タブをクリックし、適用するフィルタを指定します。

      フィルターを適用すると、指標がレポートの列として含まれているかどうかに関わらず、指標の値が指定された条件を満たす場合にのみ行が返されます。

   1. （オプション） **[!UICONTROL Date]** 」タブをクリックし、デフォルトの日付設定を変更します。

   1. （オプション） **[!UICONTROL Additional Settings]** 」タブをクリックし、設定を変更します。

1. クリック **[!UICONTROL Save as New]**.

1. 新しいビューの名前を入力し、 **[!UICONTROL Save]**.

   >[!TIP]
   >
   >タブおよび適用先の情報を識別するのに役立つ名前（「一時停止したキャンペーン」や「上位 50 件の広告」など）を使用します。

### デフォルトビューまたはカスタムビューの編集

1. 表示設定を開きます。

   * （既にビューを適用している場合）データテーブルの上のツールバーの右側で、現在のビューの名前 ([!UICONTROL Default]」) をクリックします。

   * （適用されていないカスタムビュー）左側のパネルで、 ![カスタムビュー](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "カスタムビュー") 拡大する [!UICONTROL Custom Views] メニュー。 カスタムビュー名をクリックします。

1. を編集します。 [設定を表示](#view-settings):

   1. （オプション）すべての検索エンティティ表示でデータ設定を有効または無効にするには ( [!UICONTROL Campaigns], [!UICONTROL Ad Groups]、など )、選択または選択解除 **[!UICONTROL Universal View]**.

      既存のビューに対する変更は保存できませんが、変更を含む新しいビューを作成できます。

   1. （オプション、作成したカスタムビューのみ）ビューがまだ公開されていない場合、 **[!UICONTROL Shared]** スライダーで設定 *[!UICONTROL Yes]*.

   1. （オプション） **[!UICONTROL Columns]** 」タブで、タブで使用できる列、列の順序、行の並べ替え方法を変更します。

   1. （オプション） **[!UICONTROL Filters]** 」タブをクリックし、適用するフィルターを編集します。

      フィルターを適用すると、指標がレポートの列として含まれているかどうかに関わらず、指標の値が指定された条件を満たす場合にのみ行が返されます。

      >[!NOTE]
      >
      >フィルターに対する変更を適用することはできますが、デフォルトの表示設定には保存することはできません。

   1. （オプション） **[!UICONTROL Date]** 」タブに移動して、デフォルトの日付設定を変更します。

   1. （オプション） **[!UICONTROL Additional Settings]** 」タブに移動して設定を変更します。

1. 設定を適用または保存します。

   * 設定をビューに保存せずに一時的に適用するには、 **[!UICONTROL Apply]**.

     設定は、最上位の管理ビューから移動するまで、または（該当する場合）タブに適用されます。 [別の広告主のデータを表示](/help/search-social-commerce/common-tasks/change-advertiser.md).

   * （作成した既定のビューとカスタムビューの場合）設定を現在のビューに保存するには、 **[!UICONTROL Save]**.

   * 設定を新しいカスタムビューに保存するには、 **[!UICONTROL Save As]**. Adobe Analytics の [!UICONTROL Enter New Custom View Name] ウィンドウで、新しいビューの名前を入力し、 **[!UICONTROL Save]**.

## 既定の表示をシステムの既定の設定にリセットする

既定の表示設定を復元すると、保存した設定がすべて削除され、システムの既定の設定が再適用されます。

システムのデフォルト設定は、タブによって異なります。 ほとんどのタブでは、有効なアカウントの項目とアクティブな項目（アクティブなキャンペーンのアクティブな広告グループのみなど）の前日のデータがコストで並べ替えられ、トランザクション日に基づくコンバージョンデータと共に表示されます。

1. 左側のパネルで、 ![カスタムビュー](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "カスタムビュー") 拡大する [!UICONTROL Custom Views] メニュー。

   ビューは、適用可能なエンティティで並べ替えられます。

1. ビュー名の横にある ![デフォルト設定に戻す](/help/search-social-commerce/assets/revert.png "デフォルト設定に戻す").

## カスタムビューの削除

自分で作成した任意のカスタムビューを削除できます。

現在のタブに適用されているカスタムビューを削除しても、ビューセットの外側に移動するまで ( 例えば、 [!UICONTROL Search] メニューから [!UICONTROL Reports] （メニュー）または（該当する場合） [別の広告主のデータを表示](/help/search-social-commerce/common-tasks/change-advertiser.md).

1. 左側のパネルで、 ![カスタムビュー](/help/search-social-commerce/assets/custom-views-left-rail_icon.png "カスタムビュー") 拡大する [!UICONTROL Custom Views] メニュー。

1. カスタムビュー名の上にカーソルを置き、 ![削除](/help/search-social-commerce/assets/delete.png "削除").

1. 確認メッセージで、 **[!UICONTROL Continue]**.

## デフォルトおよびカスタム表示の設定 {#view-settings}

| **タブ** | **フィールド** | **説明** |
| --- | --- | --- |
| [すべてのタブの上] | 名前 | ビューの一意の名前。 既定のビューの名前は編集できません。 <p><b>ヒント：</b> タブおよび適用先の情報を識別するのに役立つ名前（「一時停止したキャンペーン」や「上位 50 件の広告」など）を使用します。 |
|   | ユニバーサルビュー | すべてのエンティティ表示（キャンペーン、広告など）でデータ設定を使用できるようにします。 ユニバーサルビューには、指標とラベルの分類列を含めることができますが、エンティティのタイプによって異なるので、プロパティの列（エンティティ名やステータスなど）や、その他すべてのビュー属性は含めることができません。 フィルター条件は、該当する場合はエンティティビューに適用され、それ以外の場合は無視されます。 すべての指標フィルターがローカルで評価されます（例えば、クリック数が 1000 回を超える場合、キャンペーンビューには 1000 回を超えるクリック数のキャンペーンが表示され、広告グループビューには 1000 回を超えるクリック数の広告グループが表示されます）。<p>ユニバーサルビューのプロパティ列がエンティティのデフォルトビューから取得されます。 既定の表示設定で、特定のエンティティの既定のプロパティ列を変更できます。<p>このオプションを有効または無効にした後は、既存のビューに対する変更を保存することはできませんが、変更を含む新しいビューを作成することはできます。 |
|   | 共有 | （カスタムビューのみ、オプション）広告主のデータを表示できる他のすべてのユーザーがビューを使用できるようにします。 他のユーザーはビューを編集または削除できませんが、設定から新しいビューを作成できます。ビューリストでは、別のユーザーが共有している各ビューが斜体で表示されます。例：_最も効果の高いキャンペーン_.&quot; |
| 列 | 選択した列と順序 | 表示されるデータの列と順序：<ul><li> （列を追加する場合）「使用可能な列」リストで列名をクリックし、「選択した列と順序」リストにドラッグするか、 ![右矢印](/help/search-social-commerce/assets/chevron-right.png) そこに移動する</li><li>（列の水平方向の位置を変更するには）「選択した列と順序」リストで、列名をクリックし、目的の位置までドラッグするか、 ![上向き矢印](/help/search-social-commerce/assets/chevron-up.png) または ![下向き矢印](/help/search-social-commerce/assets/chevron-down.png) そこに移動する 上の列の名前が左の列に表示されます。</li><li>（列を削除する場合）「選択した列と順序」リストで、列名をクリックし、「使用可能な列」リストにドラッグするか、 ![左矢印](/help/search-social-commerce/assets/chevron-left.png) そこに移動する</li></ul><b>データをフィルター</b><p>特定のタイプのデータのみをリストするには、リストの横にあるアイコンのいずれかをクリックします。<ul><li>![プロパティアイコン](/help/search-social-commerce/assets/properties-icon.png) 検索コンポーネントのプロパティ名と ID（ステータスなど）の場合</li><li>![トラフィックアイコン](/help/search-social-commerce/assets/traffic-metrics-icon.png) 標準のトラフィック指標（インプレッション数およびクリック数など）</li><li>![売上高アイコン](/help/search-social-commerce/assets/revenue-metrics-icon.png) （広告主に対してトラッキングされるコンバージョン指標の場合。Analytics から同期されたコンバージョン指標とサイトエンゲージメント指標が含まれます）</li><li>![カスタムアイコン](/help/search-social-commerce/assets/custom-metrics-icon.png) （広告主が作成したカスタム派生指標の場合）</li><li>![分類アイコン](/help/search-social-commerce/assets/classifications-icon.png) （ラベル分類の場合）。</li></ul> <b>追加情報：</b><ul><li>新しい指標を追加、作成または編集するには、「カスタム指標の作成」、「カスタム指標の編集」および「カスタム指標の削除」を参照してください。</li><li>異なる通貨のアカウントのデータがレポートに含まれる場合、金額ベースの列（コストや CPC など）には合計は含まれません。</li><li>以下が可能です。 [列見出しメニューから列セットを一時的に編集する](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-column-heading.md)、および [列セットを編集し、 [!UICONTROL Columns] アイコン](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-set-edit-sort-icon.md). (![列アイコン](/help/search-social-commerce/assets/custom-columns.png "列アイコン")) をクリックします。</li></ul> |
|   | 並べ替え基準 | データの並べ替えに使用する列。 デフォルト値は、レポートタイプごとに異なります。 |
|   | 並べ替え順 | でデータを並べ替えるかどうか **昇順** または **降順** 注文。 スライダーを動かしてオプションを選択します。 |
| フィルター | [フィルターの定義] | （オプション）データに適用するフィルターです。 フィルターを適用すると、列の値が指定した条件を満たす場合にのみ行が返されます。<p>適用する各フィルターについて、次の操作を行います。<ol><li>フィルターを追加メニューで、列名を選択します。 このリストには、使用可能なすべての列が含まれ、列タイプ別に並べ替えられ、プロパティ列が先に表示されます。</li><li>列に対するフィルターの定義</li></ol>（入力フィールドを含むフィルター）2 番目のメニューから演算子を選択し、適切な値を入力します。 値では大文字と小文字が区別されません。 クリック ![チェックアイコン](/help/search-social-commerce/assets/select.png) 終わったら。<p>例えば、「クリック数」列を選択し、100 回を超えるクリック数の行のみを返す場合は、 _\>_ と入力します。 `100` を入力フィールドに入力します。<p>データタイプに応じて、使用可能な演算子は次のとおりです。 <i>次よりも大きい</i>, <i>より小さい</i>, <i>次と等しい</i>, <i>次を含む</i>, <i>次を含まない</i>, <i>次で始まる</i>, <i>次の語句で終わる</i>,<i>値なし</i>または <i>値を含む</i> <i>前</i>, <i>次より後</i>または <i>日付なし</i>.<p>（入力フィールドを含まないフィルター）クリック ![矢印を下に](/help/search-social-commerce/assets/arrow-down-expand.png) [ リスト項目の選択 ] メニューの横にあるチェックボックスをオンにし、含める各値の横にあるチェックボックスをオンにします。 クリック ![チェックアイコン](/help/search-social-commerce/assets/select.png) 終わったら。<p><b>メモ：</b><ul><li>フィルターに対する変更を適用することはできますが、デフォルトの表示設定には保存することはできません。</li><li>また、 [適用可能なフィルターを一時的に変更する](/help/search-social-commerce/common-tasks/data-views/ad-hoc-settings/column-filter-apply-from-toolbar.md) を選択します。</li></ul> |
|   | パフォーマンスデータのみを含む行を含める | （広告グループ、キーワード、製品グループ、プレースメント、自動ターゲットの各ビューのみ） <p>指定した日付のパフォーマンスデータを持つ行のみが含まれます。 デフォルトでは、このオプションはページの読み込み時間を短縮するために選択されています。 <p><b>警告</b>:「 」オプションの選択を解除し、パフォーマンスデータを持たない多くのエンティティがビューに含まれている場合、データの表示に時間がかかります。<p> <b>注意</b>：フィルターに対する変更をデフォルトの表示設定に適用することはできますが、保存はできません。 デフォルトのビューには、常にパフォーマンスデータを持つエンティティのみが表示されます。 |
| 日付 | 日付範囲 | （「日付範囲を含む」が選択されている場合）<p>データを生成する日付範囲。 次の 1 つのオプションを選択します。<ul><li><i>[プリセット範囲]</i>：一般的な時間増分のリスト ( <i>今日</i> から <i>過去 180 日間</i>. リストから 1 つ選択します。デフォルトはです。 <i>昨日</i>. 注意： <i>先月</i>, <i>過去 3 か月間</i>、および <i>過去 6 か月間</i> 前の暦月のデータを表示します。</li><li><i>カスタム日付範囲：</i> 開始日と終了日を指定します。 MM/DD/YYYY または M/D/YYYY の形式で日付を入力するか、 ![カレンダーアイコン](/help/search-social-commerce/assets/calendar.png) をクリックし、日付を選択します。</li></ul> |
|   | 比較 | 指定した日付範囲のデータと 2 番目の日付範囲のデータを比較します。 このオプションを選択すると、通常のデータ列ごとに 2 つの列が追加されます。 例えば、「インプレッション数」に 1 つの列だけを含める代わりに、「インプレッション数の範囲 1」、「インプレッション数の範囲 2」および「インプレッション数の差異」の列がレポートに含まれます。<p><b>メモ：</b><ul><li>派生指標の場合、差異列は表示されません。</li><li>大きな日付範囲を比較するレポートの生成には、時間がかかる場合があります。</li></ul> |
|   | 比較形式 | 「[_データフィールド_] 差異」列 次の 1 つのオプションを選択します。<ul><li><i>平方偏差</i> （デフォルト）：差異を数値として表示します。</li><li><i>%の変更</i>：差異を割合で表示します。</li></ul> |
| その他の設定 | デフォルトを使用 | 広告主レベルのコンバージョン属性設定で指定された属性設定を適用します。 |
|   | 属性ルール | (Adobe Advertisingのピクセルベースのコンバージョントラッキングサービスのみを使用する広告主 )「 」タブで、コンバージョンにつながる一連のイベントで、（複数の広告チャネルやポートフォリオにまたがる可能性がある）コンバージョンデータを属性設定する方法を説明します。 デフォルトでは、広告主レベルのコンバージョン属性設定で指定されたルールが選択されています。<ul><li> <i>最初のイベント</i>：広告主のクリックルックバックウィンドウ内のシリーズ内の最初の有料クリックに変換するか、有料クリックが発生しなかった場合は広告主のインプレッションルックバックウィンドウ内の最後のインプレッションに変換する属性です。</li><li><i>最初のイベントの重み付けの詳細</i>：広告主のクリックのルックバックウィンドウとインプレッションのルックバックウィンドウ内で発生したシリーズ内のすべてのイベントに変換を属性付けします。ただし、最初のイベントに対する重み付けは最も大きく、以降のイベントに対する重み付けは小さくなります。 コンバージョンの前に有料クリック数とインプレッション数の両方がある場合、指定したインプレッションの上書きの重み付けがさらにインプレッションに適用されます。 コンバージョンの前にインプレッションのみが付く場合、インプレッションの上書きの重みではなく、広告主のビュースルーの重みに従ってインプレッションが重み付けされます。</li><li><i>均等配分</i>：コンバージョンを、広告主のクリックルックバックウィンドウとインプレッションのルックバックウィンドウ内で発生したシリーズ内の各イベントに等しく属性付けします。 コンバージョンの前に有料クリック数とインプレッション数の両方がある場合、指定したインプレッションの上書きの重み付けがさらにインプレッションに適用されます。 コンバージョンの前にインプレッションのみが付く場合、インプレッションの上書きの重みではなく、広告主のビュースルーの重みに従ってインプレッションが重み付けされます。</li><li><i>最後のイベントの重み付けの詳細</i>：広告主のクリックのルックバックウィンドウとインプレッションのルックバックウィンドウ内で発生したシリーズ内のすべてのイベントに変換を属性付けします。ただし、最後のイベントに対する重み付けは最も大きく、先行イベントに対する重み付けは少なくなります。 コンバージョンの前に有料クリック数とインプレッション数の両方がある場合、指定したインプレッションの上書きの重み付けがさらにインプレッションに適用されます。 コンバージョンの前にインプレッションのみが付く場合、インプレッションの上書きの重みではなく、広告主のビュースルーの重みに従ってインプレッションが重み付けされます。</li><li><i>最後のイベント</i> （デフォルト）：広告主のクリックルックバックウィンドウ内のシリーズ内の最後の有料クリックに、または有料クリックが発生しなかった場合は広告主のインプレッションルックバックウィンドウ内の最後のインプレッションに、変換を属性付けします。</li><li><i>U 字形</i>：広告主のクリックルックバックウィンドウとインプレッションルックバックウィンドウ内で発生したシリーズ内のすべてのイベントに変換を属性付けます。最初のイベントと最後のイベントに最も重み付けが適用され、コンバージョンパスの途中にあるイベントに対する重み付けが小さくなります。 コンバージョンの前に有料クリック数とインプレッション数の両方がある場合、指定したインプレッションの上書きの重み付けがさらにインプレッションに適用されます。 コンバージョンの前にインプレッションのみが付く場合、インプレッションの上書きの重みではなく、広告主のビュースルーの重みに従ってインプレッションが重み付けされます。</li></ul><p><b>メモ：</b><ul><li>最後のイベント以外のすべてのアトリビューションルールは、Adobe Advertisingクリックトラッキングを持つ広告主、および（Analytics 統合を使用した）Adobe AdvertisingまたはAdobe Analyticsのコンバージョントラッキングでのみ使用できます。</li><li>アトリビューションルールは、任意のチャネルの有料広告のクリック数に適用されます。 有料検索広告のインプレッション数には適用されません。イベントレベルでは追跡できません。</li><li>「最後のイベント」ルールの 1 つを除く任意のアトリビューションルールを使用してコンバージョンデータをレポートする場合、複数のポートフォリオをまたいで、コンバージョンにつながるイベントが発生する可能性があります。 その場合、ポートフォリオ内の広告やキーワードがビューに含まれている場合にのみ、ビューにコンバージョンのデータが含まれます。</li><li>デフォルト表示の場合は、デフォルトのアトリビューションルールをそのまま使用することをお勧めします。デフォルトのアトリビューションルールは、 [目標値](/help/search-social-commerce/glossary.md#o-p) （以前は「重み付け売上高」と呼ばれていました）入札の最適化中に各入札単位に対して</li></ul> |
|   | 次に基づくコンバージョン： | コンバージョンデータのレポート方法：<ul><li><i>トランザクション日</i> （デフォルト）：指定した期間にトランザクション日が発生したトランザクションを表示します。 指定した期間内に獲得した売上高を示します。</li><li><i>クリック日</i>：指定した期間に発生したクリックに起因するトランザクションを表示します。 ポートフォリオでクリック数とトランザクション数の間に大きな遅延が生じる場合、このオプションは、ポートフォリオのクリックあたりの過去の売上高を計算するのに役立ちます。これは、期間の経過と共に予想される売上高行動を示します。 |
