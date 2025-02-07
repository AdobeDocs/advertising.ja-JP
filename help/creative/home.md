---
title: Advertising Creative 2.0 の新機能
description: Adobe Advertising Creative 2.0 の最新のアップデートと新機能について説明します。
cloud: Experience Cloud
product: advertising cloud
solution: Advertising
index: false
source-git-commit: 561846c1a909620df198498aca8db8868bbf5fbe
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 0%

---

# [!DNL Creative] 2.0 の相違点

*クローズドベータ版*

<!-- The following features are new or recently changed. -->

| 日付 | 機能 | 説明 | 詳細情報 |
| ---- | ------- | ----------- | -------------------- |
| 2025 年 2 月 10 日（Pt） | [!UICONTROL Creative Libraries] | 以前は、1 つのクリエイティブライブラリがありました。 これで、広告主ごとに複数のライブラリを作成できます。 | [ クリエイティブ・ライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md) を参照してください。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Creatives] | [!UICONTROL Creatives] ビューには、[!UICONTROL Standard Ads] と [!UICONTROL Dynamic Ads] のタブが含まれています。<ul><lu>「**[!UICONTROL Standard Ads]」タブでは** 画像、HTML 5、フレキシブルHTML 5、サードパーティクリエイティブをアップロードおよび管理できます。</li><li>「**[!UICONTROL Dynamic Ads]**」タブでは、定義済みの広告テンプレートを使用して、アップロードされたフィードファイルから作成された動的に生成された広告を管理できます。動的な広告の生成は以前 [!DNL Adobe Advertising Dynamic Creative Optimization (DCO)] 内で行われていました。<br><br> 現在、動的広告のプレビュー、複製、削除を行え、ターゲット設定された広告エクスペリエンスのクリエイティブバンドルや、ターゲット設定されていないエクスペリエンスの広告タグに動的広告を添付できます。 動的に生成された広告を作成できるのは、管理者ユーザーのみです。</li></ul> | [ クリエイティブ・ライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md) を参照してください。 |
| | [!UICONTROL Creative Libraries] > [!UICONTROL Bundles] | 複数のクリエイティブを *バンドル* にグループ化して、エクスペリエンスに簡単に追加できます。 標準広告バンドルを作成し、標準クリエイティブを添付できます。 同様に、動的な広告バンドルを作成し、動的なクリエイティブを添付できます。 | 「[ クリエイティブバンドルの管理 ](/help/creative/creative-libraries/bundle-manage.md)」を参照してください。 |
| | [!UICONTROL Experiences] | 広告エクスペリエンスの設定で、エクスペリエンスでデシジョンツリーのターゲット設定を使用するかどうかを指定できるようになりました。 決定ツリーのターゲット設定を使用したエクスペリエンスと、そうでないエクスペリエンスのワークフローは異なります。 | 「デシジョンツリーターゲティングを使用したエクスペリエンスのワークフロー」および「デシジョンツリーターゲティングを使用しないエクスペリエンスのワークフロー」を参照してください。 |
| | [!UICONTROL Experiences] | ターゲットを絞ったエクスペリエンスは、個々のクリエイティブではなく、1 つのクリエイティブライブラリのクリエイティブバンドルでのみ作成できるようになりました。 デシジョンツリーのターゲット設定を使用しなくても、単一のライブラリからターゲット設定されていないエクスペリエンスに個々のクリエイティブを添付できます。<br><br> 構造の変更により、従来のエクスペリエンスは今年後半に廃止されます。 | セルフサービスのお客様：新しいユーザーインターフェイスでエクスペリエンスを再構築します。 [ ターゲティングを使用したエクスペリエンスの作成 ](/help/creative/experiences/experience-create-targeting.md) を参照してください。<br><br>Managed Service のお客様：担当のAdobeアカウントチームが、新しいユーザーインターフェイスでエクスペリエンスを再構築します。 |
| | [!UICONTROL Experiences] | Advertising DSPを使用する広告主は、オプションで、タグを広告としてAdvertising DSP キャンペーンに直接アップロードできます。 | [ ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装」を参照してください ](/help/creative/experiences/experience-tag-export.md) |
| | DCO エクスペリエンス | 従来の DCO エクスペリエンスは、今年後半に廃止される予定です。 Adobeアカウントチームが、[!DNL Creative] の動的広告として DCO エクスペリエンスを再構築します。ただし、ターゲティングが追加された DCO エクスペリエンスは、[!DNL Creative] エクスペリエンスとして再構築されます。 | — |
| | 広告タグ | 広告サーバーのエンドポイントがAdvertising DSP広告サーバーに変更されます。<br><br> 広告タグには、（Cookie ID に加えて）ユニバーサル ID を渡す追加のパラメーターが含まれます。 | セルフサービスのお客様：[!DNL Creative] でエクスペリエンスを利用できるようになったら、既存のキャンペーンの広告タグを置き換えます。 [ ライブエクスペリエンス用の広告エクスペリエンスタグの書き出しと実装 ](/help/creative/experiences/experience-tag-export.md) を参照してください。<br><br>Managed Service のお客様：既存のキャンペーンの広告タグは、Adobeアカウントチームが置き換えます。 |
| | リターゲティングピクセル | リターゲティング ピクセル エンドポイントがAdobe Advertising UDB サービスに変更されます。<br><br> 新しいピクセルには、Cookie ID に加えてユニバーサル ID を渡す追加のパラメーターが含まれます。 | セルフサービスのお客様：新しいリターゲティングピクセルを作成して web ページに追加します。 「[ リターゲティングピクセルの管理 ](/help/creative/pixels/retargeting-pixel-manage.md)」を参照してください。<br><br>Managed Service のお客様：お客様のAdobeアカウントチームは、必要に応じて新しいリターゲティングピクセルを作成および共有します。新しいピクセルは web ページに追加します。 |
| | 変換ピクセル | 従来の DCO ピクセルは今年後半に廃止される予定で、[!DNL Adobe] 変換ピクセルが必要になります。 | セルフサービスのお客様：[!DNL Analytics for Advertising] を使用しているお客様は、DCO 変換ピクセルを [!DNL Analytics for Advertising] [!DNL Last Event Service] ピクセルおよびAdobe Analytics ピクセルに置き換える必要があります。 他のユーザーは、DCO 変換ピクセルをAdobe Advertising変換ピクセルに置き換える必要があります。<br><br>Managed Service のお客様：Adobeアカウントチームは、該当するすべてのAdobe Advertisingコンバージョンピクセルを作成および共有します。DCO コンバージョンピクセルをAdobe Advertisingコンバージョンピクセルに置き換えます。 |
