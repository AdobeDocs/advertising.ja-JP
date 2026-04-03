---
title: パフォーマンスのトラブルシューティング
description: 一般的なパフォーマンスの問題を参照し、トラブルシューティング方法を確認します。
feature: DSP Optimization
exl-id: b87f8556-1908-40c1-9f98-fbdc6d9b59b1
TQID: https://experienceleague.adobe.com/CLEAjCOYzIKDaAbH4-mZxna7MK5jmpvaCjdhGScwzQs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: af280ddc-b4d0-4416-86be-8f3ea3c6ebe7
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 519
ht-degree: 0%

---

# パフォーマンスのトラブルシューティング

| イシュー | 考えられる原因 | 取るべきアクション |
| --- | --- | --- |
| プレースメントへの支出がありません | プレースメントに広告が含まれていないか、広告がアクティブではありません。 | 想定されるすべての広告がプレースメントに添付され、承認され、アクティブであることを確認します。<br><br>また、プレースメントにカスタム広告スケジュールが含まれているかどうかを確認してください。これにより、各広告のフライト期間が制限される可能性があります。 プレースメント ビューでプレースメントの広告スケジュールを表示するには、プレースメント名の横にある&#x200B;**[!UICONTROL ...]** > **[!UICONTROL Ad schedule]**&#x200B;をクリックします。 |
| | 影響を受ける日付は、設定されたフライト日付内ではありません。 | フライト日がキャンペーン、パッケージ、プレースメントレベルで有効&#x200B;あることを確認します。 |
| | 予算の目標が達成されたか、十分に高くありません。 | キャンペーン、パッケージ、配置レベルの予算設定を確認します。 |
| | 口座は十分な資金を持っていません。 | アカウントが適切に資金調達されているかどうかを確認するには、**[!UICONTROL Settings]** > **[!UICONTROL Account]**&#x200B;に移動し、[!UICONTROL Usable Funds]の金額を確認します。 さらに資金を追加する必要がある場合は、Adobeアカウントチームにお問い合わせください。 |
| | 在庫はありません。 | 指定されたインベントリ ソース （[!UICONTROL Public]、[!UICONTROL Private]または[!UICONTROL On Demand]）が次の場合に確認します。<ul><li>正しく設定する。</li><li>アクティブでオークションを通して送信します。</li><li>該当する広告とプレースメントタイプに対応しています。</li></ul><br>在庫ソースがすべて有効でアクティブな場合は、可能な限り、追加またはすべての在庫ソースをターゲットにします。 |
| | 使用できるユーザーはありません。 | 指定したオーディエンスターゲットに十分なアクティブユーザーが含まれていることを確認します。 機能しない場合は、オーディエンスを追加してターゲットを拡大します。 |
| プレースメントへの支出が少ない | プレースメントの診断レポートの[!UICONTROL Non Bids] セクションには、プレースメントが入札しなかった理由として考えられる理由が表示されます。 | [&#x200B; プレースメントが入札しなかった理由を理解するには、[!UICONTROL Non Bids] レポート &#x200B;](/help/dsp/campaign-management/reports/placement-diagnostics.md)を確認してください。 <!-- add link/edit text when file available: See the [in-depth guide to possible Non-Bid Reasons (NBR)](link) for more information. --> |
| | プレースメントでは、入札を制限する[入札前フィルター](/help/dsp/campaign-management/placements/placement-settings.md)を使用します。 | 入札前のフィルターのしきい値を5%下げて、支出とパフォーマンスのバランスを評価します。 <!-- wording? and are users just supposed to manually monitor whether it makes a difference? --><br><br>入札前のフィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、入札と支出が累積的に制限される場合があることに注意してください。 |
| | プレースメントの勝率は低くなります。 | [!UICONTROL Max Bid]を増やして、勝利率を向上させます。<br><br><b> メモ：</b>在庫価格は、プレースメントのターゲティングによって異なる場合があります。<br><br>10%の勝利率は正常と見なされます。 |
| | 在庫数が少ない。 | 可能な場合は、追加またはすべての在庫ソースをターゲットにする。<br><br>入札前のフィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、入札と支出が累積的に制限される場合があることに注意してください。 |
| | 利用できるユーザーの数が少ない。 | 指定したオーディエンスターゲットに十分なアクティブユーザーが含まれていることを確認します。 機能しない場合は、オーディエンスを追加してターゲットを拡大します。<br><br>入札前のフィルター、地域、在庫、オーディエンスなど、複数の配置ターゲットを使用すると、入札と支出が累積的に制限される場合があることに注意してください。 |
| | パッケージには、多数のアクティブなプレースメントが含まれています。 | パッケージ内のアクティブなプレースメントの数を減らすか、パッケージ全体の予算を増やします。<br><br> パッケージに多くのプレースメントがありますが、十分な予算がない場合、DSPは各プレースメントに十分な予算を割り当てることができない可能性があります。 各プレースメントには、少なくとも2米ドル/日を費やす機会が必要です。 例えば、パッケージの予算が10 USD/日の場合、プレースメントは5つ以下にすることをお勧めします&#x200B; |

{style="table-layout:auto"}

>[!MORELIKETHIS]
>
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
>* [&#x200B; パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [&#x200B; キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
