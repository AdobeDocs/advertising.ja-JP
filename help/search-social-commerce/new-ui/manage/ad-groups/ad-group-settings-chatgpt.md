---
title: '[!DNL ChatGPT]広告グループの設定'
description: '[!DNL ChatGPT]広告グループの設定を参照してください。'
feature: Search Campaign Management
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: aed5e38a-3e62-42fa-8d16-cd080729b2a0
    internal-label: Search, Social, & Commerce
subfeature_v2:
  - id: f3d33161-c519-436e-bbbd-730ba428736b
    internal-label: Campaign management
source-git-commit: 52c1132246ea0cc48b6102e6d6f15be1ded32f09
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 0%
---
# [!DNL ChatGPT]広告グループの設定

[!DNL ChatGPT]の&#x200B;*広告は、[!DNL OpenAI]*&#x200B;による試験的な機能です

## [!UICONTROL Basic Settings] タブ

*新しい広告グループのみ*

**[!UICONTROL Network]:**&#x200B;広告ネットワーク。

**[!UICONTROL Account]:**&#x200B;広告ネットワークアカウント。

**[!UICONTROL Campaign]:** キャンペーン。 広告グループの作成後にキャンペーンを変更することはできません。

## [!UICONTROL Ad Group Details] タブ

**[!UICONTROL Ad Group name]:** キャンペーン内で一意で、少なくとも3文字を含む広告グループ名。

**[!UICONTROL Status]:**&#x200B;広告グループの表示ステータス：*[!UICONTROL Active]*&#x200B;または&#x200B;*[!UICONTROL Paused]*。 新規広告グループのデフォルトは&#x200B;*[!UICONTROL Active]*&#x200B;です。

**[!UICONTROL Bid strategy]:** （目的が[!UICONTROL Clicks]または[!UICONTROL Conversions]のキャンペーン）広告グループで広告を入札する方法：

* *[!UICONTROL Autobid]:* （新しい広告グループのデフォルト） [!DNL OpenAI]は、キャンペーンの目的に応じて、予算から最も多くのクリック数またはコンバージョン数を得るために、自動的に入札額を調整します。 入札額を入力しないでください。 このオプションは、日次キャンペーンとライフタイムキャンペーンの両方で利用できます。

* *[!UICONTROL Target CPC]:* （目標が[!UICONTROL Clicks]のキャンペーン）は、平均クリック単価の目標に向けて入札します。 目標を[!UICONTROL Target CPC] フィールドに入力します。

* *[!UICONTROL Target CPA]:* （目標が[!UICONTROL Conversions]のキャンペーン）は、コンバージョン単価の平均目標に向けて入札します。 目標を[!UICONTROL Target CPA] フィールドに入力します。

* *[!UICONTROL Manual: Max bid]:* （既存の手動入札広告グループのみ）既存の最大入札額を読み取り専用の金額として保持します。 この戦略を維持するか、キャンペーン目標のターゲット戦略を[!UICONTROL Autobid]に切り替えることができます。 このオプションは、新しい広告グループや、既に自動入札またはターゲット入札を使用している広告グループを編集する場合は使用できません。

既存の手動入札の広告グループは、自動的に別の戦略に変更されません。 ターゲット金額または無関係な設定のみを編集しても、既存のターゲット入札戦略は変更されません。

**[!UICONTROL Target CPC]:** （入札戦略[!UICONTROL Target CPC]を持つ広告グループ。必須） アカウントの通貨で達成するクリックあたりの平均コスト。 正の金額を入力してください。 これは平均的なコスト目標であり、最大入札ではありません。

**[!UICONTROL Target CPA]:** （入札戦略[!UICONTROL Target CPA]を持つ広告グループ。必須） アカウントの通貨で、達成するコンバージョンあたりの平均コストです。 正の金額を入力してください。 これは平均的なコスト目標であり、最大入札ではありません。

**[!UICONTROL Maximum CPC bid]:** （目的が[!UICONTROL Clicks]のキャンペーン、既存の手動入札広告グループのみ、読み取り専用） クリックごとに支払う既存の最大金額。

**[!UICONTROL Conversion-optimized bid cap]:** （目的が[!UICONTROL Conversions]のキャンペーン、既存の手動入札広告グループのみ、読み取り専用）コンバージョンに入札する既存の最大金額。 [!DNL OpenAI]は、予測コンバージョン率を使用して、この値をインプレッションごとのオークション入札に変換します。

**[!UICONTROL Maximum CPM bid]:** （目標を持つキャンペーン [!UICONTROL Reach]） アカウントの通貨で、1,000回のインプレッションに対して支払う最大金額。 0.01 ～ 5000の値を入力します。 リーチキャンペーンには[!UICONTROL Bid strategy]個のオプションがありません。

**[!UICONTROL Context hints (optional)]:**&#x200B;製品またはサービスに関連する可能性のある会話、トピック、またはキーワードの説明。 コンマまたは改行でヒントを分離します。 ヒントは、マッチングのガイドに使用される場合がありますが、完全一致のターゲティングルールではありません。 効果的なコンテキストヒントの作成方法については、[[!DNL ChatGPT Ads]  ヘルプを参照してください](https://help.openai.com/en/articles/20001211-create-ad-groups-for-chatgpt#writing-effective-context-hints)。

**[!UICONTROL Landing Page Suffix]:** （オプション）情報を追跡するためにランディングページ URLの末尾に追加するパラメーター。 例：`param1=value1&param2=value2`。

>[!MORELIKETHIS]
>
>* [広告グループの管理](ad-group-manage.md)
