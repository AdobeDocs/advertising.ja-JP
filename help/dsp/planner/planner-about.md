---
title: DSP [!UICONTROL Planner] ツールについて
description: プランナーツールについて学び、指定された予算とターゲティング基準に従って、コネクテッド TV （CTV）の配置のユニークリーチを予測します。
feature: DSP Planner
exl-id: b25d4ac5-e85f-4a38-8765-6c5261987668
TQID: https://experienceleague.adobe.com/dvO9ZtGs76Tm-AxE8ljLsnBXqUcX-q2J0HueG1-HASA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: e8b92199-d82f-4b20-9fc3-ffe694f93ce5
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 543
ht-degree: 0%

---

# DSP [!UICONTROL Planner] ツールについて

<!-- rename all titles/descriptions from "CTV reach planner" to "campaign reach planner" -->

*Beta機能*

プランナーツールは、在庫を開始する前に、指定された予算とターゲティング基準に従って、コネクテッド TV （CTV）の配置の世帯レベルのユニークリーチを予測するのに役立ちます。 複数のリーチプランを評価したら、パッケージとプレースメントの望ましい成果に最も適したプランを実装できます。

プランナーツールは、過去90日間の過去の入札、インプレッション、リーチデータを使用して、プラン設定のユニークリーチ、平均CPM、平均頻度、インプレッションを推定します。

## プランナー予測

各予測は、リーチと予算の予測曲線で構成され、計画設定で達成可能なリーチの量を示します。 ビジュアライゼーションの上にカーソルを置くと、より高い予算でリーチの機会が増えます。

![&#x200B; プランナー予測](/help/dsp/assets/planner-forecast.png " プランナー予測")

予測出力には、[!UICONTROL Inventory Breakdown] セクションも含まれており、異なるパブリッシャーがどのようにユニークリーチに貢献しているかを示し、貴重な発見の機会を提供します。

>[!NOTE]
>
>* [!UICONTROL Inventory Breakdown] セクションには、プライベートおよび[!UICONTROL On Demand] インベントリのデータのみが表示されます。
>* 2つの媒体企業で表示される推定のユニークリーチは、重複する可能性があります。

## プランナービュー

[!UICONTROL Planner] ビューでは、既存のCTV リーチプランを表示したり、新しいCTV リーチプランを作成したりできます。

また、任意のプランの予測を編集、複製、書き出し、アーカイブまたは再生成することもできます。

## FAQ

+++プランナーツールは、どのような種類の在庫をサポートしていますか？

プランナーツールは、プログラマティック保証（PG）、プライベートマーケットプレイス（PMP）、[!UICONTROL On Demand]、パブリックなど、あらゆるタイプの在庫をサポートしています。 正確な予測をおこなうために、過去7日間に少なくとも5万件のインプレッションを獲得した契約を含めます。

+++

+++「[!UICONTROL Unable to generate forecast]」が表示されるのはなぜですか？

このエラーの最も一般的な理由の1つは、予算が不十分か、入札額が最大であるためです。 最良の結果を得るには、5000米ドルの最小予算を使用してください。 [!UICONTROL Connected TV] メディアタイプが選択されている場合は、少なくとも10 USDの最大入札額を入力します。

また、含まれているパブリッシャーまたは取引先情報がアクティブであり、インプレッションのアクティビティが最近あることを確認します。

+++

+++予測にもとづいてプレースメントを構築しましたが、リーチ予測で示されるユニークリーチの量には達しませんでした。 なぜでしょうか？ 

リーチ予測は推定値に過ぎず、実際の結果は、季節性、入札競争力、需要など、頻繁に変化する複数の要因によって異なることが予想されます。 完全に正確であるとは期待されていませんが、最適な結果を導き出す可能性のあるキャンペーン戦略を指向するインサイトに最も有用です。

+++

+++プランナーは、同じ入力設定で異なる予測結果を生成できますか？

プランナーは最新の観測データに基づいて予測を生成するので、計画設定が同じでも予測出力は異なるタイミングで異なる場合があります。 同じ計画に対して複数の予測を生成し、それぞれの結果を書き出すことを検討してください。

+++

+++プランナ予測出力を保存できますか？

はい。右上の[!DNL Microsoft Excel] > **[!UICONTROL ...]**&#x200B;をクリックすると、予測を&#x200B;**[!UICONTROL Export]** スプレッドシートに書き出すことができます。 スプレッドシートは、2つのデータ列[!UICONTROL Budget]と[!UICONTROL Reach]を使用して、リーチ予算曲線に表示される情報をキャプチャします。

+++

>[!MORELIKETHIS]
>
>* [DSP [!UICONTROL Planner] ツールについて](planner-about.md)
>* [&#x200B; コネクテッド TV リーチ プランの作成](planner-create.md)
>* [&#x200B; コネクテッド TV リーチ プランを複製](planner-duplicate.md)
>* [&#x200B; コネクテッド TV リーチ プランの編集](planner-edit.md)
>* [&#x200B; コネクテッド TV リーチ プランの書き出し](planner-export.md)
>* [&#x200B; コネクテッド TV リーチ プランの予測を再生成](planner-forecast.md)
>* [&#x200B; コネクテッド TV リーチ プランのアーカイブ &#x200B;](planner-archive.md)
>* [&#x200B; コネクテッド TV リーチ プランの設定](planner-settings.md)
