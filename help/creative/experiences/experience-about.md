---
title: Advertising Creativeのエクスペリエンスについて
description: パーソナライズされた広告エクスペリエンスを設定し、パフォーマンスに基づいて広告要素を最適化する方法を説明します。
feature: Creative Experiences
exl-id: 91d4b4e5-c646-4485-8149-89f41dc9c3e6
source-git-commit: 2ddda1e23e3a3413ef93ca0705f0b9688c893f64
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# Advertising Creative 2.0 のエクスペリエンスについて

*クローズドベータ版*

[!DNL Advertising Creative 2.0] は、クリエイティブライブラリの広告に対して、<!-- can use a single library only --> の 2 つの異なる広告エクスペリエンス構造を提供します。

* **意思決定ツリーターゲティングを使用したエクスペリエンス：** [!DNL Creative] では、意思決定ツリーモデルを使用して、カスタマージャーニー全体を通してパーソナライズされた広告エクスペリエンスを設定できます。 ターゲットオーディエンスに基づいて、すべての広告要素（画像、ヘッドライン、オファー、ランディングページ）をカスタマイズできます。

  例えば、シカゴとニューヨーク市のユーザーを対象に同じクリエイティブのバンドルを指定し、シカゴのユーザーをAdobe Analyticsとは異なるランディングページに送信できます。 また、シカゴとニューヨーク市以外に住んでいるセグメント内のユーザーには別のバンドルを指定し、セグメントに属していない他のユーザーには 3 番目のバンドルを指定することもできます。

  ターゲティングオプションは次のとおりです。

   * Adobe Audience Manager、Adobe Analyticsおよび Advertising Cloud DSP からのファーストパーティオーディエンスセグメント

   * 特定の地理的な場所（国、州、米国内の DMA、都市、郵便番号を含む）

   * 特定のキーと値のペア（データパスターゲット）がDSP、パブリッシャー、パートナーから渡されるビューア

   * [!DNL Creative] リターゲティングピクセルと指定された属性値

   * 特定のデバイスタイプ、オペレーティングシステムおよびブラウザー

  デシジョンツリーでターゲットオーディエンスのブランチを作成したら、ブランチにクリエイティブバンドルを割り当てることにより、ターゲットオーディエンスを潜在的なクリエイティブとペアにすることができます。 各エクスペリエンスで、クリエイティブバンドルの最適化とスケジュールをカスタマイズし、各バンドル内の個々のクリエイティブのデフォルトのランディングページとトラッキング URL<!-- later: and any flexible attributes --> を変更できます。

* **デシジョンツリーのターゲット設定を使用しないエクスペリエンス：** [!DNL Creative] は、オーディエンスを絞り込まずに、広告エクスペリエンスの広告要素を最適化します。 エクスペリエンスごとに、開始日と終了日および一部のデフォルト設定を指定しますが、ワークフローの多くは、エクスペリエンス内に直接存在しません。 エクスペリエンスにクリエイティブを直接追加する代わりに、[!UICONTROL Tag Manager] を使用してエクスペリエンスの各広告サイズに広告タグを作成したあと、それにクリエイティブを追加し、クリエイティブの最適化とスケジュールを設定し、ランディングページとトラッキング URL をカスタマイズしま <!-- later: and any flexible attributes -->。

## 広告の最適化

<!-- MORE -->
[!DNL Creative] では、パフォーマンスに基づいて任意のエクスペリエンス用に広告要素を最適化します。 特定のオーディエンスをターゲットにしたエクスペリエンスの場合、ターゲットオーディエンスセットの個々の広告要素のパフォーマンスに基づいて広告を最適化できます。 特定のオーディエンスターゲットのないエクスペリエンスの場合、広告要素は、個々の広告要素のパフォーマンスにのみ基づいて最適化されます。

## エクスペリエンスの実装と管理

ライブエクスペリエンス（必要なすべての広告要素を含む）を作成したら、[ エクスペリエンス全体のJavaScriptまたは iframe タグを生成 ](experience-tag-export.md) できます。 Experience tag を広告としてAdobe Advertising DSPのキャンペーンにアップロードしたり、サードパーティのDSPで広告として実装したりできます。 [!DNL Creative] は、ターゲティング、広告ローテーションのオプションおよび利用可能な広告在庫に基づいて、エクスペリエンスのファーストパーティ広告およびトリガーサードパーティ広告を提供します。

## エクスペリエンスのパフォーマンスデータ

次のパフォーマンスデータを使用できます。

* [!UICONTROL Creative]/[!UICONTROL Experiences] ビューで「[!UICONTROL Metrics]」オプションを有効にすると、各エクスペリエンスカードまたは行は、エクスペリエンスが受け取ったインプレッション数とクリック数を示します。

  ![ 指標オプション ](/help/creative/assets/metrics-option.png " 指標オプション ")

  <!-- insert screen shot of Metrics option?  If not, then add instructions elsewhere -->

  <!-- I don't see this as of 1/9; why only in the table view?   You can also add conversion columns in the table view. -->

* [!UICONTROL Experiences] ビューから [ 任意のエクスペリエンスの詳細なパフォーマンスデータを表示 ](experience-performance-details.md) できます。

* エクスペリエンス全体のパフォーマンスを監視するには、[ カスタムCreativeレポート ](/help/creative/report-custom-creative.md) を作成します。

## エクスペリエンスのステータス {#experience-statuses}

エクスペリエンスのステータスは自動的に設定されます（手動で設定した *削除済み* は除く）。

| ステータス | 説明 |
| ------ | ----------- |
| [!UICONTROL Live] | このエクスペリエンスには必要な要素がすべて含まれているので、エクスペリエンスタグを生成して、DSPの広告として実装できます。 ライブエクスペリエンスは今後開始される予定になっている可能性があります。 |
| [!UICONTROL Draft] | エクスペリエンスのすべてのブランチにクリエイティブが割り当てられないので、エクスペリエンスが不完全で、エクスペリエンスタグを生成できません。 |
| [!UICONTROL Processing] | 以前にライブになっていたエクスペリエンスは編集されましたが、現在は不完全です。 そのためのエクスペリエンスタグは生成できません。 **注意：** エクスペリエンスにエクスペリエンスタグを既に実装している場合、以前にライブになっていたバージョンは引き続き提供できます。 後でエクスペリエンスを完了し、再度ライブにした場合は、既存のタグ実装を使用して新しいバージョンを提供できます。 |
| [!UICONTROL Deleted] | エクスペリエンスは [!DNL Creative] から削除され、[!UICONTROL Experiences] ビューに表示されなくなります。 |

>[!NOTE]
>
>[!DNL Creative] のエクスペリエンスステータスに影響を与えることなく、DSP内で広告のステータスを変更できます。

## [!UICONTROL Experiences] ビュー

[!UICONTROL Experiences] ビューには、ターゲット設定されたエクスペリエンスとターゲット設定されていないエクスペリエンスがすべて表示されます。 エクスペリエンスの名前、ステータス、開始日と終了日、割り当てられたクリエイティブまたはクリエイティブバンドルの数とディメンション、エクスペリエンスに動的広告が含まれているかどうかがわかります。 [!UICONTROL Experiences] ビューで「[!UICONTROL Metrics]」オプションを有効にすると、各エクスペリエンスカードまたは行は、エクスペリエンスが受け取ったインプレッション数とクリック数を示します。

エクスペリエンスの作成と管理、広告エクスペリエンスタグの作成と名前変更、JavaScriptのタグと iframe 形式のタグの書き出しを行って、DSP に実装できます。 Advertising DSPを使用する広告主は、オプションで、広告タグをAdvertising DSP キャンペーンに直接アップロードできます。

### 使用可能なアクション

使用可能な主要なアクションを次に示します。 完全なリストについては、クリエイティブ / エクスペリエンスの章の目次を参照してください。

* [ビュー内でのデータのダウンロード](experience-download-view.md)

* ターゲティングを使用したエクスペリエンスの [ 作成 ](/help/creative/experiences/experience-create-targeting.md) および [ 編集 ](/help/creative/experiences/experience-edit-targeting.md)

* ターゲティングを使用しないエクスペリエンスについては、[ 作成 ](/help/creative/experiences/experience-create-no-targeting.md)、[ 編集 ](/help/creative/experiences/experience-edit-no-targeting.md) および [ 手動で広告タグを作成 ](/help/creative/experiences/experience-tag-create-manually.md) します

* [ クローン ](experience-clone.md) エクスペリエンス

* [ プレビュー ](experience-preview.md) エクスペリエンス

* エクスペリエンスの [ デモ URL を共有 ](experience-share-demo-url.md)

* [ エクスペリエンスの広告タグのエクスポート ](experience-tag-export.md) （オプションで、広告タグをAdvertising DSP キャンペーンに直接アップロードする）

* エクスペリエンスの [ 削除 ](experience-delete.md)

>[!MORELIKETHIS]
>
>* [ デシジョンツリーのターゲット設定を使用したエクスペリエンスの作成 ](experience-create-targeting.md)
>* [ ターゲティングを使用しないエクスペリエンスの作成 ](experience-create-no-targeting.md)
