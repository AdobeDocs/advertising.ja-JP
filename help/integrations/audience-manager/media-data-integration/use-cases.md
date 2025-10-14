---
title: ユースケース
description: Advertising DSP メディアデータをAudience Managerと共有するユースケースについて説明します
feature: Integration with Adobe Audience Manager
exl-id: 1d961799-b8be-499a-8db6-b59762d96bf1
source-git-commit: 7f35b3f3b33ed320ac186d219cbd0f826666bb3b
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 0%

---

# Adobe Audience Managerでのメディア露出データのキャプチャのユースケース

*Advertising DSPのみの広告主*

*Adobe AdvertisingとAdobe Audience Managerの統合のみを行う広告主*

以下に、Advertising DSP media の公開データをAudience Managerでキャプチャするメリットを <!-- ad impression data? --> つ方法を示します。

## 最新性と頻度の管理

インプレッションデータをAudience Managerで取得すると、特定の広告やキャンペーンの対象となったユーザーのセグメントを作成することで、頻度管理を強化できます。 これらのセグメントは、頻度を高める場合は広告ターゲティングに、頻度を制限する場合は広告抑制に使用できます。

また、Audience Manager[!DNL Segment Builder] を使用すると、アクションにつながるシグナルを含むすべての [&#x200B; ルールベースの特性 &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/segments/recency-and-frequency.html?lang=ja) に [&#x200B; 最新性と頻度の制御 &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/traits/trait-builder/create-onboarded-rule-based-traits.html?lang=ja) を適用できます。 これにより、例えば、メディアキャンペーン内で特定のクリエイティブをユーザーに表示する回数を制限できます。 この方法については、「[&#x200B; インスタントクロスデバイス抑制 &#x200B;](https://experienceleague.adobe.com/docs/audience-manager/user-guide/features/profile-merge-rules/instant-cross-device-suppression.html?lang=ja)」を参照してください。<!-- The AM pulled this paragraph verbatim from AEM doc; I change only a word or two. -->

## 順次メッセージ

インプレッションデータをキャプチャすることで、キャンペーンや広告の対象となったユーザーのセグメントを作成でき、このセグメントを使用して順次メッセージや抑制を行うことができます。 例えば、クリエイティブリク `123` ストを表示したけれどクリックやコンバージョンをおこなわなかったユーザーを、クリエイティブリター `456` スを表示することでリターゲットできます。

この例をAudience Managerで実行するには、次の手順に従います。<!-- The AM pulled this example/procedure verbatim from AEM doc; I changed only a word or two. -->

1. クリエイティブを閲覧したユーザーを取り込むための特性を作成します。

   例えば、特性に `Creative Trait 123` という名前を付けるには、次の特性ルールを使用します。

   ```
   d_creative == 123 AND d_event == imp
   ```

1. クリックしたユーザーや変換したユーザーをキャプチャするための特性を作成します。

   例えば、この特性に `Click and Converter` という名前を付けるには、次の特性ルールを使用します。

   ```
   d_event == click OR d_event=conv
   ```

1. クリエイティブリク `123` ストを表示したがクリックやコンバージョンを行わなかったユーザーを入力する、`Retarget Users` という名前のセグメントを作成します。 次の特性ルールを使用します。

   ```
   Creative Trait 123 AND NOT Click and Converter
   ```

1. クリエイティブ `456` を使用して、セグメント `Retarget Users` を宛先にマッピングし、宛先のターゲットユーザーをマッピングします。

## [!DNL Adobe Audience Analytics] と Campaign の公開データ

キャンペーンのインプレッションとクリックのデータをAudience Manager内で使用できるようになると、特定のキャンペーンや戦術に晒された、またはこれらとインタラクションを受けたユーザーの特性とセグメントを作成できます。 [[!DNL Audience Analytics] integration](https://experienceleague.adobe.com/docs/analytics/integration/audience-analytics/mc-audiences-aam.html?lang=ja) を使用すると、Audience Managerセグメントを [!DNL Analytics] と同期して、さらに分析できます。 考えられるユースケースを次に示します。

* **DSPと [!DNL Advertising Search, Social, & Commerce] 広告のインタラクション分析：** 標準の [[!DNL Analytics for Advertising] integration](/help/integrations/analytics/overview.md) では、DSPと [!DNL Search, Social, & Commerce] のインタラクションに関するインサイトは提供されません。これは、両方のチャネルで、AMO ID アトリビューションルールに従う AMO ID が使用され、検索クリックが表示ビュースルーを上書きするからです。 Audience ManagerでDSP公開セグメントを作成すると、[!DNL Audience Analytics] を使用してDSPと [!DNL Search, Social, & Commerce] 広告のインタラクションを [!DNL Analytics] で分析できます。

* **頻度分析：** 特定の広告またはキャンペーンにさらされた回数に基づいて、Audience Managerでセグメントを作成できます。 その後、Analytics で様々な露出セグメントを分析し、DSPでの露出数に応じてユーザーの行動がどのように変化するかを確認できます。

## [!DNL Audience Optimization Reports]

[Audience Manager [!DNL Audience Optimization Reports]](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-reports.html?lang=ja) を活用して、キャンペーン全体でセグメントの潜在的なパフォーマンスの機会を特定できます。 これらのレポートでは、キャンペーンのインプレッション、クリック数およびコンバージョンデータをセグメント指標と組み合わせて、セグメント中心の最適化と効果的なチャネルミックスを示します。

### 関連するAudience Optimizationレポートのタイプ

| 報告書 | 説明 |
| ------ | ----------- |
| [[!UICONTROL Segment Performance] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/segment-performance.html?lang=ja) | マッピングされたセグメントとマッピングされていないセグメントをインプレッション数とコンバージョン率で比較します。 |
| [[!UICONTROL Trend Analysis and Volume Analysis] Reports]9https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/trend-analysis-volume-analysis.html） | 様々な広告ディメンションのインプレッション数、クリックスルー率およびコンバージョン数に関するデータを返します。 |
| [[!UICONTROL Optimal Frequency] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/optimal-frequency.html?lang=ja) | 提供されたインプレッション数とコンバージョン数の最適なバランスを見つけるのに役立ちます。 これにより、表示するインプレッション数を調整してから、リターンの減少を確認できます。 |
| [[!UICONTROL Unique User Reach] Report](https://experienceleague.adobe.com/docs/audience-manager/user-guide/reporting/audience-optimization-reports/audience-optimization-advertisers/unique-user-reach.html?lang=ja) | バブルチャート。選択したディメンションの一意のユーザーの数に直接比例して、各バブルのサイズが調整されます。 |

### 検討事項

* [!DNL Audience Optimization Reports] ユーザーがロールベースのアクセス制御（RBAC）を持 [!DNL Adobe Customer Care] 場合、広告主 ID と組織のAudience Managerデータソース統合コードの間のマッピングを設定する必要があります。 その後、管理者ユーザーは、様々なユーザーに RBAC 権限を提供できます。

* [!DNL Audience Optimization Reports] のコンバージョンレポートには、エンドユーザーによる設定が必要です。 ユーザーはメタデータファイルにデータを入力する必要があります。

* [!DNL Audience Optimization Reports] は、キャンペーンメタデータ（キャンペーン名やプレースメント名など）に対する変更をサポートしていません。

* 検索広告のクリック数は、インプレッション数と相関関係がある場合にのみ [!DNL Audience Optimization Reports] に含まれます。 つまり、検索クリックはインプレッション後のコンバージョンとして扱われます。 その結果、多くの検索クリックが [!DNL Audience Optimization Reports] に含まれない場合があります。

>[!MORELIKETHIS]
>
>* [DSP Media のAdobe Audience Managerへの公開データ送信の概要 &#x200B;](overview.md)
>* [Advertising DSP キャンペーンからクリックとインプレッションのデータを収集 &#x200B;](collect.md)
