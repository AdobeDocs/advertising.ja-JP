---
title: メディア企業のレコメンデーションとインサイトのサポート
description: パブリッシャーのレコメンデーションとインサイトの表示と管理のサポートについて説明します。
feature: Search Recommendations
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '1604'
ht-degree: 0%

---

# メディア企業のレコメンデーションとインサイトのサポート

*[!DNL Google Ads]と[!DNL Microsoft Advertising] アカウント*

キャンペーンのパフォーマンスと効率性を向上させるために、広告ネットワークから[!DNL Google Ads]と[!DNL Microsoft Advertising]の推奨事項とインサイトが提案されます。

* アカウントのパフォーマンス履歴、キャンペーン設定、[!DNL Google Ads]の傾向にもとづいて、アセットの追加から予算の増加まで、キャンペーンのさまざまなパフォーマンス側面に関してカスタマイズされた提案を各[!DNL Google Ads] レコメンデーションで提供します。

* 各[!DNL Microsoft Advertising] パフォーマンス insightとレコメンデーションでは、マシンラーニング アルゴリズムとベストプラクティスに基づいて、キャンペーンのパフォーマンスを最適化するための変更が提案されます。

## [!UICONTROL Recommendations] ビュー

（新しいUI） [!UICONTROL Dashboard] > [!UICONTROL Recommendations]および（従来のUI） [!UICONTROL Insights & Reports] > [!UICONTROL Recommendations & Publisher Insights]内で、次の操作を実行できます。

* アカウントで対応していない、サポートされているレコメンデーションを一目で確認できます。 各エントリの情報には、レコメンデーションタイプ、[!DNL Adobe]のレコメンデーション、影響を受ける指標、影響を受けるエンティティ、および詳細へのリンクが含まれます。 指標の予測増加は緑色で強調表示されます。

  ![Recommendations UI](/help/search-social-commerce/assets/recommendations-ui.png "Recommendations UI")

  ビューを開くと、データはリアルタイムで利用できます。 データを更新するには、ページの左下にある「![更新](/help/search-social-commerce/assets/refresh.png "更新")」をクリックします。

* [!DNL Microsoft Advertising]件のアカウントについて、[!DNL Microsoft Advertising]件のアカウントについて、過去30日間に生成された各パフォーマンス insightを一目で確認できます。 インサイトは、レコメンデーションと似た情報を提供しますが、その形式は異なります。 各insightには、日付、問題の説明、影響を受けるエンティティ、根本原因（詳細へのリンクが含まれる場合があります）、特定のinsightに対して操作できる[!DNL Microsoft Advertising] エディターを開くためのリンクを含む提案アクションが含まれます。

* レコメンデーションの詳細を表示し、そのレコメンデーションを直接適用または却下します。

* アカウントに適用された各レコメンデーションのログを表示します。

## [!DNL Google Ads]でサポートされているレコメンデーションタイプ

| レコメンデーションカテゴリー | レコメンデーションタイプ | 説明 |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] （[!DNL Google Ads]では「[!DNL Ads and assets]」と呼ばれるようになりました） | [!UICONTROL Call extension] | キャンペーンへの呼び出し拡張機能の追加 |
| | [!UICONTROL Callout extension] | キャンペーンへのコールアウト拡張機能の追加 |
|  | [!UICONTROL Improve demand gen ad strength] | 需要創出広告の広告強度を向上させるための提案 |
| | [!UICONTROL Optimize ad rotation] | 最適化された広告ローテーションの使用 |
| | [!UICONTROL Responsive search ad] | 新しいレスポンシブ検索広告を追加 |
| | [!UICONTROL Responsive search ad asset] | 広告へのレスポンシブ検索広告アセットの追加 |
| | [!UICONTROL Responsive search improve ad strength] | レスポンシブ検索広告の広告強度を向上させるための提案 |
| | [!UICONTROL Sitelink extension] | サイトリンク拡張機能をキャンペーンに追加 |
| | [!UICONTROL Text ad] | 新しいテキスト広告を追加 |
| [!UICONTROL Automated campaigns] | [!UICONTROL DSA to performance max migration] | 動的検索広告をパフォーマンス最大数キャンペーンに移行する |
| | [!UICONTROL Dynamic image extension opt in] | アカウントの動的画像拡張機能を有効にします。これにより、[!DNL Google Ads] マシンラーニングが、広告のランディングページから最も関連性の高い画像を自動的に広告に追加できます |
| | [!UICONTROL Improve performance max ad strength] | パフォーマンス最大施策のアセットグループの強度を「優れている」評価に改善する |
| | [!UICONTROL Performance max final URL opt in] | パフォーマンス最大キャンペーンの最終的なURL拡張を有効にする |
| | [!UICONTROL Performance max opt in] | パフォーマンス最大数キャンペーンにオプトイン |
| | [!UICONTROL Upgrade local campaign to performance max] | 従来のローカルキャンペーンをパフォーマンス最大キャンペーンにアップグレードする |
| | [!UICONTROL Upgrade smart shopping campaign to performance max] | 従来のスマートショッピングキャンペーンをパフォーマンス最大キャンペーンにアップグレードする |
| [!UICONTROL Bidding and budget] | [!UICONTROL Campaign budget] | 現在、予算によって制限されているキャンペーンのおすすめ予算 |
| | [!UICONTROL Forecasting campaign budget] | 今後、予算の制約が予想されるキャンペーンの推奨予算 |
| | [!UICONTROL Forecasting set Target CPA] | トラフィックを増やすために予測されるシーズンイベントの前に、施策のターゲット CPAを1つも設定しない |
| | [!UICONTROL Forecasting set Target ROAS] | トラフィックの増加が予測されている季節イベントの前に予算を増やし、入札戦略を[!UICONTROL Maximize Conversion Value]から[!UICONTROL Target ROAS]に変更します |
| | [!UICONTROL Marginal ROI campaign budget] | キャンペーン予算を調整してROIを向上 |
| | [!UICONTROL Maximize clicks opt in] | [!UICONTROL Maximize Clicks]入札戦略への変更 |
| | [!UICONTROL Maximize conversion value opt in] | 「コンバージョン価値最大化入札戦略」への変更 |
| | [!UICONTROL Maximize conversions opt in] | [!UICONTROL Maximize Conversions]入札戦略への変更 |
| | [!UICONTROL Move unused budget] | 未使用の予算を制約付き予算に移動 |
| | [!UICONTROL Raise Target CPA bid too low] | コンバージョンが少なすぎたり、少なすぎたりすると、[!UICONTROL Target CPA]を推奨量だけ増やします |
| | [!UICONTROL Set Target CPA] | キャンペーンのターゲット CPAを設定する |
| | [!UICONTROL Set Target ROAS] | 施策の目標ROASを設定する |
| | [!UICONTROL Target CPA opt in] | [!UICONTROL Target CPA]入札戦略への変更 |
| | [!UICONTROL Target CPA raising] | 過去のコンバージョンから計算された[!DNL Google Ads]の予測に基づいて[!UICONTROL Target CPA]を上げます |
| | [!UICONTROL Target ROAS lowering] | 過去のコンバージョンから計算される[!DNL Google Ads]の予測に基づいて[!UICONTROL Target ROAS]を下げます |
| | [!UICONTROL Target ROAS opt in] | [!UICONTROL Target ROAS]入札戦略への変更 |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Display expansion opt in] | ディスプレイの拡張を使用するようにキャンペーンを更新してリーチを拡大する |
| | [!UICONTROL Keyword] | 新しいキーワードを追加 |
|  | [!UICONTROL Refresh customer match list] | 最近の顧客にパーソナライズされた広告を表示するには、顧客マッチリストを更新します |
| | [!UICONTROL Search partners opt in] | [!DNL Google]人の検索パートナーとリーチを拡大 |
| | [!UICONTROL Use broad match keyword] | 完全自動化されたコンバージョンベース入札により、コンバージョンベースのキャンペーンに幅広いマッチを使用できます |

## [!DNL Microsoft Advertising]でサポートされているレコメンデーションタイプ

| レコメンデーションカテゴリー | レコメンデーションタイプ | 説明 |
| --- | --- | --- |
| [!UICONTROL Ads and extensions] | [!UICONTROL Responsive search ad] | 新しいレスポンシブ検索広告を追加 |
| [!UICONTROL Bidding and budgets] | [!UICONTROL Campaign budget] | キャンペーンの修正を予算で制限 |
| [!UICONTROL Keywords and targeting] | [!UICONTROL Keyword] | すべてのソースから新しいキーワードを追加する |

## レコメンデーションとインサイトを確認 {#recommendations-view}

>[!NOTE]
>
>広告ネットワークのレコメンデーションとパフォーマンスインサイトは、キャンペーンのパフォーマンスを向上させるのに役立ちますが、より広範な目標と一致しない場合があります。 そのため、レコメンデーションやinsightを導入する前に、Adobeのアカウントチームと相談することをお勧めします。

### （新しいUI）パブリッシャーのレコメンデーションを表示

1. メインメニューで、**[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

   [!DNL Microsoft Advertising] アカウントの場合、デフォルトで[!UICONTROL Recommendations] タブが開きます。

1. 行の[!UICONTROL Actions]列で、**[!UICONTROL View]**&#x200B;をクリックします。 レコメンデーションにサブレコメンデーションがある場合は、サブレコメンデーションの横にある&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

   オプションで[広告ネットワークの推奨事項を適用または却下](#recommendations-apply-dismiss)できます。

### （レガシーUI）パブリッシャーのレコメンデーションを表示

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**&#x200B;をクリックします。

1. 右上で、広告ネットワークとアカウントを選択します。

   [!DNL Microsoft Advertising] アカウントの場合、アカウントの[!UICONTROL Recommendations]がデフォルトで一覧表示されます。

1. 行の[!UICONTROL Actions]列で、**[!UICONTROL View]**&#x200B;をクリックします。 レコメンデーションにサブレコメンデーションがある場合は、サブレコメンデーションの横にある&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

   オプションで[広告ネットワークの推奨事項を適用または却下](#recommendations-apply-dismiss)できます。

### （新しいUI） [!DNL Microsoft Advertising]のパフォーマンス インサイトを表示する

1. メインメニューで、**[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

1. データテーブルの上にある「**[!UICONTROL Insights]**」タブをクリックします。

1. （オプション）行の[!UICONTROL Actions]列に1つ以上のアクションが含まれている場合：

   * 個々のinsightに対してアクションを実行できる[!DNL Microsoft Advertising] エディターを開くには、アクションの横にある&#x200B;**[!UICONTROL Click here]**&#x200B;をクリックします。

   * （複数のアクションを含むインサイト）insightのすべてのアクションの全文を表示するには、**[!UICONTROL Read More]**&#x200B;をクリックします。 次に、個々のinsightに対してアクションを実行できる[!DNL Microsoft Advertising] エディターを開くには、個々のアクションの横にある&#x200B;**[!UICONTROL Click here]**&#x200B;をクリックします。

   [!DNL Microsoft Advertising] エディターにログインしていない場合は、まずログイン画面に移動します。

### （従来のUI） [!DNL Microsoft Advertising]のパフォーマンス インサイトを表示する

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**&#x200B;をクリックします。

1. 右上で、広告ネットワークとアカウントを選択します。

1. データテーブルの上の&#x200B;**[!UICONTROL Insights]**&#x200B;をクリックします。

1. 行の[!UICONTROL Actions]列にアクションが含まれている場合は、オプションで&#x200B;**[!UICONTROL Click here]**&#x200B;をクリックして[!DNL Microsoft Advertising] エディターを開き、そこからinsightでアクションを実行できます。

   [!DNL Microsoft Advertising] エディターにログインしていない場合は、まずログイン画面に移動します。

## パブリッシャーのレコメンデーションの適用または却下 {#recommendations-apply-dismiss}

ビジネス目標と一致している場合はレコメンデーションを適用し、そうでない場合は除外します。

>[!NOTE]
>
>レコメンデーションは施策のパフォーマンスを向上させるのに役立ちますが、より広範な目標と合致しない場合もあります。 そのため、レコメンデーションを導入する前に、Adobeのアカウントチームと相談することをお勧めします。

### （新しいUI）パブリッシャーのレコメンデーションの適用または却下

1. メインメニューで、**[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

   [!DNL Microsoft Advertising] アカウントの場合、デフォルトで[!UICONTROL Recommendations] タブが開きます。

1. （オプション）カテゴリとタイプ別にレコメンデーションをフィルタリングします。

1. レコメンデーションまたはinsight行の[!UICONTROL Actions]列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. （サブレコメンデーションを含むレコメンデーション） サブレコメンデーションの横にある&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

1. （オプション）次のいずれかの操作を行います。

   * レコメンデーションを適用するには、**[!UICONTROL Apply]**&#x200B;をクリックします。

     レコメンデーションのサイズによっては、レコメンデーションの適用にミリ秒から数秒かかる場合があります。

   * レコメンデーションを却下するには、**[!UICONTROL Dismiss]**&#x200B;をクリックします。

### （レガシーUI）発行者のレコメンデーションの適用または却下

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**&#x200B;をクリックします。

1. 右上で、広告ネットワークとアカウントを選択します。

   [!DNL Microsoft Advertising] アカウントの場合、アカウントの[!UICONTROL Recommendations]がデフォルトで一覧表示されます。

1. （オプション）カテゴリとタイプ別にレコメンデーションをフィルタリングします。

1. レコメンデーションまたはinsight行の[!UICONTROL Actions]列で、**[!UICONTROL View]**&#x200B;をクリックします。

1. （サブレコメンデーションを含むレコメンデーション） サブレコメンデーションの横にある&#x200B;**[!UICONTROL View]**&#x200B;をクリックします。

1. （オプション）次のいずれかの操作を行います。

   * レコメンデーションを適用するには、**[!UICONTROL Apply]**&#x200B;をクリックします。

     レコメンデーションのサイズによっては、レコメンデーションの適用にミリ秒から数秒かかる場合があります。

   * レコメンデーションを却下するには、**[!UICONTROL Dismiss]**&#x200B;をクリックします。

## アカウントの発行者レコメンデーションのログを表示します {#recommendations-log}

適用された各レコメンデーションのログを表示できます。 この情報には、レコメンデーションカテゴリ、レコメンデーションタイプ、影響を受けるエンティティ、レコメンデーションを適用したユーザー、およびタイムスタンプが含まれます。

却下されたレコメンデーションは、広告ネットワークでは利用できません。

### （新しいUI） アカウントの発行者レコメンデーションのログを表示する

1. メインメニューで、**[!UICONTROL Dashboard]>[!UICONTROL Recommendations]**&#x200B;をクリックします。

1. ツールバーで、広告ネットワークとアカウントを選択します。

1. 右上の「![ レコメンデーションログ ](/help/search-social-commerce/assets/recommendations-log-view-new.png " レコメンデーションログ ")」をクリックします。

### （従来のUI） アカウントの発行者レコメンデーションのログを表示する

1. メインメニューで、**[!UICONTROL Search, Social, & Commerce]> [!UICONTROL Insights & Reports] >[!UICONTROL Recommendations & Publisher Insights]**&#x200B;をクリックします。

1. 右上で、広告ネットワークとアカウントを選択します。

1. 右上の「![ レコメンデーションログ ](/help/search-social-commerce/assets/recommendations-log-view.png " レコメンデーションログ ")」をクリックします。

## ポートフォリオでメディア企業のレコメンデーションを使用するためのベストプラクティス

<!--
 Add info for MS once we have it ..." 

*[!DNL Google Ads] and [!DNL Microsoft Advertising] accounts*
 
-->

## [!DNL Google Ads]件の推奨事項

| レコメンデーションタイプ | 説明 | Search、Social、Commerceのポートフォリオでレコメンデーションを自動適用しますか？ | コメント |
|--- |--- |--- |--- |
| [!UICONTROL Ads]と拡張機能（[!DNL Google Ads]では「広告とアセット」と呼ばれるようになりました） | 広告とアセットの追加/編集に関する推奨事項 | 自動的に適用できますが、広告主はレコメンデーションを手動でレビューする必要があります。 | レスポンシブ検索広告が広告主の要件に沿ったものであることを確認するには、レコメンデーションのレビューが必要です。 |
| [!UICONTROL Automated campaigns] | 自動キャンペーン（ローカルキャンペーンとスマートキャンペーン）のレコメンデーション | Search, Social, &amp; Commerceでは利用できません。 | — |
| [!UICONTROL Bidding and budget] | 入札、予算、ターゲットのレコメンデーションによるパフォーマンスの向上 | 最適化されたポートフォリオのキャンペーンには自動的に適用しない。 | 現在のレコメンデーションは、目的に合わせて1次元的なものにすることができます。 例えば、[!DNL Google Ads]は、キャンペーンのクリック数が減少した場合、予算を気にすることなくターゲット CPAの増加を推奨します。 |
| [!UICONTROL Keywords and targeting] | キーワードクリーンアップとオーディエンスレコメンデーション | は自動適用できますが、自動適用は選択的に使用できます。 | キーワードのクリーンアップを利用し、キャンペーン間の重複を削除しますが、それ以上の自動化（動的検索広告の自動作成やオーディエンスの自動拡張など）は避けます。 |
| [!UICONTROL Measurement] | コンバージョンの追跡と認定制度に関する推奨事項 | Search, Social, &amp; Commerceでは利用できません。 | これらの推奨事項は、パフォーマンスに影響を与える可能性があります。 Adobeのアカウントチームと相談し、レコメンデーションを適用する前に、その長所と短所について話し合いましょう。 |
| [!UICONTROL Repairs] | アカウントの問題を改善するためのその他の推奨事項 | Search, Social, &amp; Commerceでは利用できません。 | [!DNL Google Ads]内の修復の推奨事項を定期的に手動で確認します。 このレコメンデーションタイプは、未承認の広告、フィードの問題、トラッキングの問題などを特定するのに適した方法です。 |
| [!UICONTROL Other] | [!DNL Google Ads] モバイルアプリの使用をお勧めします | Search, Social, &amp; Commerceでは利用できません。 | — |

<!--

>[!MORELIKETHIS]
>
>* [View your publisher recommendations and performance insights](recommendation-view.md)
>* [Apply or dismiss a publisher recommendation](recommendation-apply-dismiss.md)
>* [View the publisher recommendations log for an account](recommendation-view-log.md)
>* [Best practices for using publisher recommendations with portfolios](recommendation-best-practices.md)

-->
