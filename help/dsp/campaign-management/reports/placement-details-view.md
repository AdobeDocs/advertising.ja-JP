---
title: プレースメントのサイト、広告、頻度および在庫の詳細を表示します
description: 配置のターゲットサイト、広告、頻度および在庫データを表示する方法を説明します。
feature: DSP Placements
exl-id: b58b442c-2fb8-4a78-9be9-d85aa83136e2
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '685'
ht-degree: 0%

---

# プレースメントのサイト、広告、頻度および在庫の詳細を表示します

各配置に対して、次の操作を実行できます。 [（詳細ビューを開く） [!UICONTROL Inspector])](placement-details-view.md)：すべてのターゲットサイト、広告およびプレースメントの取引をリストします。 また、配置の頻度データも含まれます。 任意のタブからデータを書き出すこともできます。

![配置インスペクター](/help/dsp/assets/placement-inspector.png)

## 配置内の情報 [!UICONTROL Inspector] {#placement-inspector}

* **[!UICONTROL Sites]:** 配置にインプレッションがあるすべてのサイト。

  The [!UICONTROL Sites] 「 」タブには、検索およびフィルター機能、メインページで使用できる標準およびカスタムの列表示オプション、および [!UICONTROL Exclude] ボタンを使用して、配置からサイトをすばやく除外できます。

* **[!UICONTROL Ads]:** 配置内のすべての広告。

  The [!UICONTROL Ads] タブには、検索およびフィルタ機能、メインページで使用可能な標準およびカスタムの列表示オプション、各行のクイックアクションボタン ( [!UICONTROL Pause] （広告をすばやく一時停止できます）。

* **[!UICONTROL Frequency]:** 配置の広告頻度レベルごとのデータ。以下を含みます。
   * 広告頻度レベル（ユーザーが 1 回広告を表示したすべてのインスタンスの「1」など）
   * デバイス/ブラウザーまたはユーザーの推定ユニーク数（指定した数に応じて異なる） [!UICONTROL Cross Device Level] （キャンペーンの）指定された頻度レベルでインプレッションを受け取った人
   * 指定された頻度レベルでの推定インプレッション数
   * 指定した頻度レベルの推定平均頻度。 この値は、 (Estimated Impressions)/(Estimated Uniques) と等しくなります。

* **[!UICONTROL Inventory]:** プレースメントのターゲットとなるすべての契約に関する情報。

  The [!UICONTROL Inventory] 「 」タブには、パフォーマンス統計を表示することで、すばやくトラブルシューティングできます。 [!UICONTROL Auctions], [!UICONTROL Bids]、および [!UICONTROL Win Rate]. このタブには、検索およびフィルタ機能、メインページで使用可能な標準およびカスタムの列表示オプション、および各行のクイックアクションボタン ( [!UICONTROL Edit], [!UICONTROL View Report]、および [[!UICONTROL Auction Insights] その他のトラブルシューティング](/help/dsp/inventory/private-deal-auction-insights.md).

## を開きます。 [!UICONTROL Placement Inspector]

1. 親キャンペーンまたはパッケージの配置ビューを開きます。

   * 親キャンペーン内のすべての配置を表示：

      1. メインメニューで、 **[!UICONTROL Campaigns]**.

      1. キャンペーンの名前をクリックします。

      1. 次をクリック： **[!UICONTROL Placements]** タブをクリックします。

   * 親パッケージ内のすべての配置を表示します。

      1. メインメニューで、 **[!UICONTROL Campaigns]**.

      1. キャンペーンの名前をクリックします。

      1. 次をクリック： **[!UICONTROL Packages]** タブをクリックします。

      1. 親パッケージの名前をクリックします。

1. 配置行の上にカーソルを置いて、 **[!UICONTROL More]**&#x200B;をクリックし、次のオプションをクリックします。

   * 配置のターゲットとなるすべてのサイトを表示するには、 **[!UICONTROL Sites]**.

   * プレースメント内のすべての広告を表示するには、 **[!UICONTROL Ads]**.

   * 配置の頻度データを表示するには、 **[!UICONTROL Frequency]**.

   * プレースメントのターゲットとなるすべての契約を表示するには、 **[!UICONTROL Inventory]**.

1. （オプション） [列表示の変更](campaign-data-views-manage.md#column-view-change) 必要に応じて、必要な指標を表示します。

1. （オプション）任意のタブでデータをエクスポートするには、 ![その他](/help/search-social-commerce/assets/more.png "その他") 右上にあるをクリックし、 **[!UICONTROL Export]**.

   データは、XLSM 形式のレポートとしてブラウザーのデフォルトのダウンロードフォルダーに保存されます。

## 在庫のトラブルシューティング

| 問題 | 考えられる原因 | 実行すべきアクション |
| -----------| ---------- | ---------- |
| [!UICONTROL Zero Auctions] | 発行者が入札リクエストの送信を開始していません。 | 契約を有効化するには、発行者に問い合わせてください。 |
| | 取引が正しく設定されていない（不正な外部取引 ID の入力など）。 | 契約の詳細を確認し、契約を編集します。 |
| [!UICONTROL Auctions but no Bids] | 配置のターゲティングが、契約の受信入札リクエストと一致しません。 <br><br> 例えば、プレースメントは、契約に対する資格のない地域をターゲットとしている場合があります。 | ターゲティングの不一致を避けるために、必要に応じて配置ターゲットを編集します。 |
| | 配置には、契約に必要なメディアタイプを持つアクティブな広告がありません。 | 正しいメディアタイプの広告を作成し、配置に添付します。 |
| | 配置に十分な予算がありません。 | 受信リクエストでの入札を許可するように配置予算を増やします。 |
| | 配置のフライト日は、契約のインプレッションの配信日と重複しません。 | 必要に応じて、プレースメントのフライト日を編集します。 |
| [!UICONTROL Low Win Rate] | プレースメントの最大入札額（下限または固定）は、契約で必要とされる最小入札額を下回っています。 | プレースメントの [!UICONTROL Max Bid] 必要に応じて。 |
| | 配置では、入札を制限する入札前フィルターを使用します。 | 入札前フィルターのしきい値を下げて、より多くの入札を許可します。 |
| | プレースメントのオーディエンスのターゲティングが制限されすぎます。 | 指定したオーディエンスターゲットに十分なアクティブユーザーがあるかどうかを確認し、可能であればオーディエンスを拡張します。 |

>[!MORELIKETHIS]
>
>* [Campaign Managementビューでのパフォーマンスレポートのタイプ](campaign-reports-about.md)
>* [キャンペーンデータビューの管理](campaign-data-views-manage.md)
