---
title: プレースメントのサイト、広告、頻度、インベントリの詳細を表示します
description: プレースメントのターゲットサイト、広告、頻度、在庫データを表示する方法について説明します。
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
TQID: https://experienceleague.adobe.com/QpJqRuDiM59WDwshIyp-OQ2ge81zVyvC1vftLd2sGbQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: a4886037-b6d8-40e1-aeab-edeb7649d7d3
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 660
ht-degree: 0%

---

# プレースメントのサイト、広告、頻度、インベントリの詳細を表示します

プレースメントごとに、[&#x200B; プレースメント内のすべてのターゲットサイト、広告、取引を一覧表示する（詳細ビュー[!UICONTROL Inspector]） &#x200B;](placement-details-view.md)を開くことができます。 また、配置の頻度データも含まれます。 オプションで、任意のタブからデータを書き出すことができます。

![&#x200B; プレースメントインスペクター](/help/dsp/assets/placement-inspector.png)

## プレースメント [!UICONTROL Inspector]の情報 {#placement-inspector}

* **[!UICONTROL Sites]:** プレースメントがインプレッションを持つすべてのサイト。

  [!UICONTROL Sites] タブには、検索とフィルター機能、メインページで使用できる同じ標準およびカスタム列ビューオプション、各行の[!UICONTROL Exclude] ボタンが含まれているため、サイトをプレースメントからすばやく除外できます。

* **[!UICONTROL Ads]:** プレースメント内のすべての広告。

  「[!UICONTROL Ads]」タブには、検索とフィルター機能、メインページで使用できる同じ標準およびカスタム列ビューオプション、および[!UICONTROL View Ad Approvals]などの各行のクイックアクションボタンが含まれています。

* プレースメントの各広告頻度レベルの&#x200B;**[!UICONTROL Frequency]:** データ （以下を含む）:
   * 広告の頻度レベル （ユーザーが1回広告を見たすべてのインスタンスの「1」など）
   * 指定された頻度レベルでインプレッションを受け取ったデバイス/ブラウザーまたはユーザー（キャンペーンに指定された[!UICONTROL Cross Device Level]に応じて）の推定一意の数
   * 指定された周波数レベルでのインプレッションの推定数
   * 指定された周波数レベルの推定平均周波数。 この値は、（推定インプレッション数）/（推定ユニーク数）に等しくなります。

* **[!UICONTROL Inventory]:** プレースメントの対象となるすべての取引に関する情報。

  「[!UICONTROL Inventory]」タブでは、[!UICONTROL Auctions]、[!UICONTROL Bids]、[!UICONTROL Win Rate]などのパフォーマンス統計を表示して、迅速なトラブルシューティングを実行できます。 このタブには、検索とフィルター機能、メインページで使用できる同じ標準とカスタム列の表示オプション、さらにトラブルシューティング用の[!UICONTROL Edit]、[!UICONTROL View Report]、[[!UICONTROL Auction Insights]など、各行のクイックアクションボタンが含まれています](/help/dsp/inventory/private-deal-auction-insights.md)。

## 配置[!UICONTROL Inspector]を開きます {#inspector-open}

1. 親キャンペーンまたはパッケージのプレースメントビューを開きます。

   * 親キャンペーン内のすべてのプレースメントを表示します。

      1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

      1. キャンペーンの名前をクリックします。

      1. 「**[!UICONTROL Placements]**」タブをクリックします。

   * 親パッケージ内のすべてのプレースメントを表示します。

      1. メインメニューで、**[!UICONTROL Campaigns]**&#x200B;をクリックします。

      1. キャンペーンの名前をクリックします。

      1. 「**[!UICONTROL Packages]**」タブをクリックします。

      1. 親パッケージの名前をクリックします。

1. プレースメント行の上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Analyze]** > **[!UICONTROL Inspector]**&#x200B;をクリックします。

1. （オプション） [必要に応じて列ビュー](campaign-data-views-manage.md#column-view-change)を変更して、必要な指標を表示します。

1. （オプション）任意のタブのデータを書き出すには、右上の![詳細](/help/search-social-commerce/assets/more.png "詳細")をクリックし、**[!UICONTROL Export]**&#x200B;をクリックします。

   データは、XLSM形式のレポートとして、ブラウザーのデフォルトのダウンロードフォルダーに保存されます。

## プレースメントから[!UICONTROL Inspector]から広告を削除する {#remove-ads-placement-inspector}

1. [&#x200B; プレースメント [!UICONTROL Inspector]](#inspector-open)を開きます。

1. 「**[!UICONTROL Ads]**」タブをクリックします。

1. 広告名の横にある「**[!UICONTROL ...]** > **[!UICONTROL Detach]**」をクリックします。

## インベントリのトラブルシューティング

| イシュー | 考えられる原因 | 取るべきアクション |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 発行者が入札リクエストの送信を開始していません。 | 取引をアクティブ化するには、発行者に連絡してください。 |
| | 間違った外部取引IDを入力するなど、取引が正しく設定されていない。 | 取引の詳細を確認し、取引を編集します。 |
| [!UICONTROL Auctions but no Bids] | プレースメントのターゲットが、取引の入札リクエストと一致しません。 <br><br>例えば、プレースメントは、契約の対象ではない地域をターゲットにしている場合があります。 | ターゲティングのミスマッチを避けるために、必要に応じてプレースメントターゲットを編集します。 |
| | プレースメントには、取引に必要なメディアタイプを含むアクティブな広告がありません。 | 適切なメディアタイプを使用して広告を作成し、プレースメントに添付します。 |
| | 配置に十分な予算がありません。 | プレースメント予算を増やして、着信リクエストに入札できるようにします。 |
| | プレースメントのフライト日が、契約のインプレッションの配信日と重ならない。 | 必要に応じて、プレースメントのフライト日を編集します。 |
| [!UICONTROL Low Win Rate] | プレースメントの最大入札額（フロアまたは固定）は、契約で必要な最小額を下回っています。 | 必要に応じて、プレースメントの[!UICONTROL Max Bid]を増やします。 |
| | プレースメントでは、入札を制限する入札前フィルターを使用します。 | 入札前のフィルターのしきい値を下げて、より多くの入札を許可します。 |
| | プレースメントのオーディエンスのターゲティングに制限がある。 | 指定したオーディエンスターゲットに十分なアクティブユーザーが含まれているかどうかを確認し、可能であればオーディエンスを拡張します。 |

>[!MORELIKETHIS]
>
>* [&#x200B; キャンペーン管理ビューのパフォーマンスレポートの種類](campaign-reports-about.md)
>* [&#x200B; キャンペーンデータビューの管理](campaign-data-views-manage.md)
