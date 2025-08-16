---
title: Advertising Creative 2.0 の新機能
description: Adobe Advertising Creative 2.0 の最新のアップデートと新機能について説明します。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
exl-id: 0d25f665-b5f9-4d27-851a-2a456fe2cbf8
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# [!DNL Creative] 2.0 の相違点

<!-- The following features are new or recently changed. -->

| 日付 | 機能 | 説明 | 詳細情報 |
| ---- | ------- | ----------- | -------------------- |
| 2025 年 8 月 4 日（Pt） | Ad [!DNL] エクスペリエンスのオーディエンスのターゲット | オーディエンスの組み込みと除外に関するより複雑なロジック（Advertising DSPで使用可能なロジックと同じ）が、オーディエンスターゲット設定内で使用できます。 広告エクスペリエンスのオーディエンスターゲットを設定する際に、複数のセグメントグループを設定し、ロジックに基づいてユーザーを含めるか除外するかを指定できるようになりました。<br><br> 各セグメントの合計オーディエンスメンバー数、および各セグメントグループのアクティブなオーディエンスメンバーと合計オーディエンスメンバーの数を確認できます。<br><br> このオプションを使用すると、「[!UICONTROL Split targets to create nodes]」に対する既存のオプションは使用できなくなります。<br><br> 複数のセグメントをターゲットにするオーディエンスノードを使用した既存のエクスペリエンスがある場合、それらは「[!UICONTROL Include Any]」オプションを使用してターゲットに設定され、ユーザーはインプレッションの対象となるセグメントの 1 つにのみ属している必要があります。 以前は、ユーザーはすべてのセグメントに属している必要がありました。 | 「[ 最終レベルへのターゲットノードの追加 ](/help/creative/experiences/experience-target-node-add-final.md)」、「[ ノード間にターゲットノードの挿入 ](/help/creative/experiences/experience-target-node-add-inner.md)」、「[ 兄弟ターゲットノードの追加 ](/help/creative/experiences/experience-target-node-add-sibling.md)」を参照してください。 |
| 2025 年 7 月 10 日（Pt） | ビデオクリエイティブ | ファーストパーティビデオクリエイティブと、ビデオ固有のバンドルおよびエクスペリエンスがサポートされるようになりました。<ul><li>ファーストパーティビデオクリエイティブをアップロードして、ビデオ固有のバンドルに追加できるようになりました。 バンドル設定で、「[!UICONTROL Bundle Type]」オプションに [!UICONTROL Standard Display]、[!UICONTROL Dynamic Display]、[!UICONTROL Standard Video] が含まれるようになりました。</li><li>ビデオバンドルを使用して、ビデオ固有の広告エクスペリエンスを作成できます。 広告エクスペリエンス設定に、[!UICONTROL Ad Type]、[!UICONTROL Standard Display]、[!UICONTROL Dynamic Display] のオプションを含む「[!UICONTROL Video]」設定が含まれるようになりました。 クリックスルー率、完了率またはカスタム目標に応じて、ビデオ広告を最適化できます。</li><li>ビデオとエクスペリエンスのタグは、広告サイズではなく、ビデオの期間とビットレートで定義されます。</li><li>ビデオ広告は、プレビューできるように、Adobe Advertising DSP エンコーディングに自動的にトランスコードされます。 オプションで、[!UICONTROL Tag Manager] 内の任意の広告エクスペリエンスタグに他の DSP のトランスコーディングを適用できます。</li></ul> | 「[ クリエイティブライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md)」、「[ クリエイティブバンドルの管理 ](/help/creative/creative-libraries/bundle-manage.md)」、「[ ターゲット設定されたエクスペリエンス設定 ](/help/creative/experiences/experience-settings-targeting.md)」、「[ ターゲット設定されていないエクスペリエンス設定 ](/help/creative/experiences/experience-settings-no-targeting.md) および「[ ビデオ広告エクスペリエンスタグのトランスコーディングオプションのカスタマイズ ](/help/creative/experiences/experience-tag-video-transcoding.md)」を参照してください。 |
| 2025 年 5 月 21 日（Pt） | [!UICONTROL Creative Libraries] | Adobe Experience Manager アセットライブラリから [!UICONTROL Creative Libraries] に画像を追加して、広告エクスペリエンス内で使用できるようになりました。 | 「[Adobe Experience Manager画像アセットへのアクセスの設定 ](/help/creative/creative-libraries/aem-assets-configure.md)」および「[ クリエイティブライブラリへの標準クリエイティブの追加 ](/help/creative/creative-libraries/creative-add-standard.md) を参照してください。 |
| 2025 年 2 月 10 日（Pt） | [!UICONTROL Creative Libraries] | 以前は、1 つのクリエイティブライブラリがありました。 これで、広告主ごとに複数のライブラリを作成できます。 | [ クリエイティブ・ライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md) を参照してください。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives] ビューには、[!UICONTROL Standard Ads] と [!UICONTROL Dynamic Ads] のタブが含まれています。<ul><li>「**[!UICONTROL Standard Ads]」タブでは** 画像、HTML5、フレキシブル HTML5、サードパーティクリエイティブをアップロードおよび管理できます。</li><li>「**[!UICONTROL Dynamic Ads]**」タブでは、定義済みの広告テンプレートを使用して、アップロードされたフィードファイルから作成された動的に生成された広告を管理できます。以前は、動的広告は [!DNL Adobe Advertising Dynamic Creative Optimization (DCO)] 内で生成されていました。<br><br> 現在、動的広告のプレビュー、複製、削除を行うことができます。 また、ターゲット設定された広告エクスペリエンス用のクリエイティブバンドルや、ターゲット設定されていないエクスペリエンス用の広告タグに動的広告を添付することもできます。 広告を動的に生成できるのは管理者ユーザーのみです。</li></ul> | [ クリエイティブ・ライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md) を参照してください。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 複数のクリエイティブを *バンドル* にグループ化して、エクスペリエンスに簡単に追加できます。 標準広告バンドルを作成し、標準クリエイティブを添付できます。 同様に、動的な広告バンドルを作成し、動的なクリエイティブを添付できます。 | 「[Creative バンドルの管理 ](/help/creative/creative-libraries/bundle-manage.md)」を参照してください。 |
| | [!UICONTROL Experiences] | 新しい広告エクスペリエンス設定では、エクスペリエンスでデシジョンツリーのターゲット設定を使用するかどうかを指定するようになりました。エクスペリエンスを保存すると設定を変更できなくなります。 決定ツリーのターゲット設定を使用したエクスペリエンスと、決定ツリーのターゲット設定を使用しないエクスペリエンスでは、ワークフローが異なります。 | 「[ ターゲティングを使用したエクスペリエンスの作成 ](/help/creative/experiences/experience-create-targeting.md)」および「[ ターゲティングを使用しないエクスペリエンスの作成 ](/help/creative/experiences/experience-create-no-targeting.md)」を参照してください。 |
| | [!UICONTROL Experiences] | ターゲットを絞ったエクスペリエンスは、個々のクリエイティブではなく、1 つのクリエイティブライブラリのクリエイティブバンドルでのみ作成できるようになりました。 デシジョンツリーのターゲット設定を使用しなくても、単一のライブラリからターゲット設定されていないエクスペリエンスに個々のクリエイティブを添付できます。<br><br> 構造の変更により、従来のエクスペリエンスは今年後半に廃止されます。 | セルフサービスのお客様：新しいユーザーインターフェイスでエクスペリエンスを再構築します。 [ ターゲティングを使用したエクスペリエンスの作成 ](/help/creative/experiences/experience-create-targeting.md) を参照してください。<br><br>Managed Service のお客様：担当のAdobe アカウントチームが、新しいユーザーインターフェイスでエクスペリエンスを再構築します。 |
| | [!UICONTROL Experiences] | Advertising DSPを使用する広告主は、オプションで、タグを広告としてAdvertising DSP キャンペーンに直接アップロードできます。 | [ ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装」を参照してください ](/help/creative/experiences/experience-tag-export.md) |
| | DCO エクスペリエンス | 従来の DCO エクスペリエンスは、今年後半に廃止される予定です。 Adobe アカウントチームは、[!DNL Creative] の動的広告として DCO エクスペリエンスを再構築します。ただし、ターゲティングが追加された DCO エクスペリエンスは、[!DNL Creative] エクスペリエンスとして再構築されます。 | — |
| | 広告タグ | 広告サーバーのエンドポイントがAdvertising DSP広告サーバーに変わります。<br><br> 新しい広告タグには、（Cookie ID に加えて）ユニバーサル ID を渡す追加のパラメーターが含まれています。 | セルフサービスのお客様：[!DNL Creative] でエクスペリエンスを利用できるようになったら、既存のキャンペーンの広告タグを置き換えます。 [ ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装 ](/help/creative/experiences/experience-tag-export.md) を参照してください。<br><br>Managed Service のお客様：既存のキャンペーンの広告タグは、Adobe アカウントチームが置き換えます。 |
| | リターゲティングピクセル | リターゲティングピクセルエンドポイントがAdobe Advertising UDB サービスに変わります。<br><br> 新しいピクセルには、Cookie ID に加えてユニバーサル ID を渡す追加のパラメーターが含まれています。 | セルフサービスのお客様：新しいリターゲティングピクセルを作成して web ページに追加します。 「[ リターゲティングピクセルの管理 ](/help/creative/pixels/retargeting-pixel-manage.md)」を参照してください。<br><br>Managed Service のお客様：Adobe アカウントチームは、必要に応じて新しいリターゲティングピクセルを作成および共有します。新しいピクセルは web ページに追加します。 |
| | 変換ピクセル | 従来の DCO ピクセルは今年後半に廃止される予定で、[!DNL Adobe] 変換ピクセルが必要になります。 | セルフサービスのお客様：[!DNL Analytics for Advertising] を使用しているお客様は、DCO 変換ピクセルを [!DNL Analytics for Advertising] [!DNL Last Event Service] ピクセルおよびAdobe Analytics ピクセルに置き換える必要があります。 他のユーザーは全員、DCO 変換ピクセルをAdobe Advertising変換ピクセルに置き換える必要があります。<br><br>Managed Service のお客様：Adobe アカウントチームは、該当するすべてのAdobe Advertising コンバージョンピクセルを作成および共有します。DCO コンバージョンピクセルをAdobe Advertising コンバージョンピクセルに置き換えます。 |
