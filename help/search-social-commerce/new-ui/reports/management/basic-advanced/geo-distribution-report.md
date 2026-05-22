---
title: '[!UICONTROL Geo Distribution Report]'
description: '[!UICONTROL Geo Distribution Report]について説明します。'
feature: Search Reports, Search Advanced Reports
source-git-commit: bfca434eacf52ec7236804c54b7740442aa12961
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 0%

---

# [!UICONTROL Geo Distribution Report]

[!UICONTROL Geo Distribution Report]には、指定されたポートフォリオ （該当する場合）または広告アカウント内のキャンペーンについて、検索ユーザーのIP アドレスから決定される、地域ごとの推定クリック数[^1]が含まれます。 オプションで、コンバージョン指標を含めることができます。 デフォルトでは、データには、クリック数が生成された各地域の広告グループ/キャンペーン/ポートフォリオの組み合わせごとに推定クリック数が含まれ、行は推定クリック数で降順になります。

推定インプレッション数と推定コストは、ディスプレイ トラッキングのみのキャンペーンでのみ使用できます。

過去2か月と現在の月のデータを表示できます。

>[!NOTE]
>
>* データは、検索および表示キャンペーンでのみ使用できます。
>* このレポートの合計は、地理的な場所を決定する際に異なるベンダーと方法が原因で、[!DNL Google Ads Geo Report] （コンパイルする[!DNL Google Ads]件）の同じキャンペーンの合計と異なる場合があります。

>[!TIP]
>
>その結果を地理的トレンドの活用に利用します。 例えば、カリフォルニア州のユーザーが、特定のキャンペーンの他の地域よりもコンバージョン率が大幅に高い場合は、そのキャンペーンのカリフォルニア州のユーザーを、他の地域のユーザーを除いてターゲットにすることができます。 ただし、急激な市場動向は、他の分野のユーザー行動に影響を与え、これらの分野も潜在的に収益性を高める可能性があることに注意してください。 最適な結果を得るには、地理的キーワードと広告を組み合わせた地理的ターゲティングを利用します。

[^1]：検索、ソーシャル、およびCommerceでは、有効なクリック数を検出するために様々な広告ネットワークとは異なるアルゴリズムを使用する場合があり、検索、ソーシャル、およびCommerceでは前週にクリック数が記録されなかったキーワードをカウントしないため、これらのレポートのクリック（またはクリックスルー）データは、実際のデータではなく見積もりとして表示されます。 また、Search、Social、Commerceが同期しない広告ネットワークアカウントのデータが含まれる場合もあります。

## デフォルトの列

すべてのデフォルト列とカスタム列について詳しくは、「[基本レポートと詳細レポートのレポート列](basic-advanced-report-columns.md)」を参照してください。

* [!UICONTROL Country]
* [!UICONTROL State]
* [!UICONTROL Region]
* [!UICONTROL Portfolio]
* [!UICONTROL Search Engine]
* [!UICONTROL Campaign]
* [!UICONTROL Ad Group]
* [!UICONTROL Est. Clicks]

>[!MORELIKETHIS]
>
>* [基本レポートと詳細レポートについて](basic-advanced-report-about.md)
>* [ スケジュール済みレポートの管理](/help/search-social-commerce/new-ui/reports/management/report-manage.md)
>* [基本および詳細レポート設定](basic-advanced-report-settings.md)
