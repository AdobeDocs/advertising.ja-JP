---
title: ユースケース
description: Advertising DSP メディアデータをAudience Managerと共有するユースケースについて説明します
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
TQID: https://experienceleague.adobe.com/bEvS7Wb-Xk0nHAchL60c3AUNm7K4S2p3tBxJ2aWWevA
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: b01c7841-b9d0-4fd5-8458-a6a6f601ad3d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dcid: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 730
ht-degree: 0%

---

# Adobe Audience Managerでメディア露出データを取得するユースケース

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを使用する広告主*

Audience ManagerでAdvertising DSP メディア露出データ <!-- ad impression data? -->をキャプチャすると、次のようなメリットが得られます。

## 最新性と頻度の管理

Audience Managerでインプレッションデータを取得すると、特定の広告やキャンペーンに接触したオーディエンスのセグメントを作成することで、頻度の管理を強化できます。 これらのセグメントは、頻度を上げる場合は広告ターゲティングに、頻度を制限する場合は広告サプレッションに使用できます。

また、Audience Manager [!DNL Segment Builder]では、実用的なシグナルを含む[ ルールベースの特性](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html)に[最新性と頻度の制御](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html)を適用できます。 これにより、例えば、ユーザーがメディアキャンペーン内で特定のクリエイティブを表示される回数を制限できます。 この方法については、「[即時クロスデバイス抑制](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html)」を参照してください。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## シーケンシャルメッセージ

インプレッションデータを取得することで、キャンペーンや広告に露出したユーザーセグメントを作成し、このセグメントをシーケンシャルメッセージや抑制に使用できます。 例えば、クリエイティブ `123`を見たものの、クリックまたはコンバージョンしなかったユーザーを、クリエイティブ `456`を表示してリターゲティングできます。

この例をAudience Managerで実行するには、次の手順に従います。<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. 特性を作成して、そのクリエイティブを見たユーザーをキャプチャします。

   例えば、特性`Creative Trait 123`に名前を付けるには、次の特性ルールを使用します。

   ```
   d_creative == 123 AND d_event == imp
   ```

1. クリックまたはコンバージョンしたユーザーをキャプチャするための特性を作成します。

   例えば、この特性に`Click and Converter`という名前を付けるには、次の特性ルールを使用します。

   ```
   d_event == click OR d_event=conv
   ```

1. 「`Retarget Users`」という名前のセグメントを作成して、クリエイティブ `123`を見たものの、クリックまたはコンバージョンしなかったユーザーを入力します。 次の特性ルールを使用します。

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. セグメント `Retarget Users`を宛先にマッピングし、クリエイティブ `456`を使用して宛先内のユーザーをターゲットにします。

## [!DNL Adobe Audience Analytics]とキャンペーンの露出データ

Audience Managerでキャンペーンのインプレッション数とクリック数のデータを利用できるようになると、特定のキャンペーンや戦術に接触したり、接触したりしたオーディエンスの特性とセグメントを構築できます。 [[!DNL Audience Analytics] 統合](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html)を使用すると、Audience Manager セグメントを[!DNL Analytics]と同期して、さらに詳しく分析できます。 次のようなユースケースが考えられます。

* **DSPと[!DNL Advertising Search, Social, & Commerce]広告のインタラクション分析：**&#x200B;標準の[[!DNL Analytics for Advertising] 統合](/help/integrations/analytics/overview.md)では、DSPと[!DNL Search, Social, & Commerce]のインタラクションに関するインサイトは提供されません。これは、両方のチャネルでAMO ID アトリビューションルールに従うAMO IDが使用され、検索クリックで表示ビュースルーが上書きされるためです。 Audience ManagerでDSP露出セグメントを作成すると、[!DNL Audience Analytics]を使用して、[!DNL Search, Social, & Commerce]のDSP広告と[!DNL Analytics]広告のインタラクションを分析できます。

* **頻度分析：** ユーザーが特定の広告またはキャンペーンに接触した回数に基づいて、Audience Managerでセグメントを作成できます。 次に、Analyticsで様々な露出セグメントを分析して、DSPの露出の数に応じてユーザーの動作がどのように変化するかを確認できます。

## [!DNL Audience Optimization Reports]

[Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html)を活用して、キャンペーン全体のセグメントの潜在的なパフォーマンスオポチュニティを特定できます。 これらのレポートは、キャンペーンのインプレッション、クリック、コンバージョンのデータをセグメント指標と組み合わせ、セグメント中心の最適化と効果的なチャネルミックスに役立つ情報を提供します。

### Audience Optimization関連レポートの種類

| レポート | 説明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] レポート ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html) | インプレッションとコンバージョン率によって、マッピングされたセグメントとマッピングされていないセグメントを比較します。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] レポート ]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html） | 幅広い広告ディメンションのインプレッション、クリックスルー率、コンバージョンに関するデータを返します。 |
| [[!UICONTROL Optimal Frequency] レポート ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html) | 配信されたインプレッション数とコンバージョン数の最適なバランスを把握するのに役立ちます。 リターンの減少を確認する前に、表示するインプレッション数を調整できます。 |
| [[!UICONTROL Unique User Reach] レポート ](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html) | バブルチャート：選択したディメンションのユニークユーザー数に直接比例して、各バブルのサイズが表示されます。 |

### 検討事項

* [!DNL Audience Optimization Reports]人のユーザーにロールベースのアクセス制御（RBAC）がある場合、[!DNL Adobe Customer Care]は、広告主IDと組織のAudience Manager データソース統合コードとのマッピングを設定する必要があります。 管理者ユーザーは、異なるユーザーにRBAC権限を提供できます。

* [!DNL Audience Optimization Reports]のコンバージョンレポートには、エンドユーザーによる設定が必要です。 ユーザーはメタデータファイルを入力する必要があります。

* [!DNL Audience Optimization Reports]は、キャンペーンのメタデータ （キャンペーン名やプレースメント名など）の変更をサポートしていません。

* 検索広告のクリック数は、インプレッションと関連付けられている場合にのみ[!DNL Audience Optimization Reports]に含まれます。 つまり、検索クリックはインプレッション後のコンバージョンとして扱われます。 その結果、多くの検索クリックが[!DNL Audience Optimization Reports]に含まれない可能性があります。

>[!MORELIKETHIS]
>
>* [Adobe Audience ManagerへのDSP メディア露出データの送信の概要](overview.md)
>* [Advertising DSP キャンペーンからクリックとインプレッションのデータを収集](collect.md)
