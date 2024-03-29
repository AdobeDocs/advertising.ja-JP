---
title: ユニバーサルビデオに関する FAQ
description: ユニバーサルビデオ広告の詳細を説明します。
feature: DSP Placements, DSP Ads
source-git-commit: 2caacfcbdb3c9d0d91ca26829de5829654f9ab8a
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# ユニバーサルビデオに関する FAQ

[ユニバーサルビデオ広告](/help/dsp/campaign-management/ads/ad-about.md#ad-types) を使用すると、1 つのビデオを配置して、VPAID および VAST インベントリ用に、デスクトップ、モバイル、接続された TV 環境からビデオインベントリをターゲットに設定できます。

## ユニバーサルビデオ配置と広告は、どのようにして作成しますか？

ユニバーサルビデオ配置には、ユニバーサルビデオ広告のみを含めることができ、ユニバーサルビデオ広告は、ユニバーサルビデオ配置にのみ添付することができます。

ユニバーサルビデオ配置と広告を、他のタイプの配置とビデオの作成方法と同様に作成します。

1. 目的のキャンペーン内で、 [ユニバーサルビデオ配置の作成](/help/dsp/campaign-management/placements/placement-create.md)、選択 [!UICONTROL Placement Type] **[!UICONTROL Universal Video]**.

   ターゲットにする環境（デスクトップ、モバイル、接続済み TV）を少なくとも 1 つ指定する必要があります。

1. ユニバーサルビデオ配置と同じキャンペーン内で、 [単一のユニバーサルビデオ広告の作成](/help/dsp/campaign-management/ads/ad-create.md) または [複数のユニバーサルビデオ広告を作成する](/help/dsp/campaign-management/ads/ad-create-multiple.md).

   複数の広告を作成する場合は、必ず「[!UICONTROL Universal Video]&quot; [!UICONTROL Ad Type]:

   * の場合 [!DNL Google] または [!DNL Flashtalking] 広告：「[!UICONTROL Review ad types]」ファイルをアップロードした後、 **[!UICONTROL Ad Type]** フィールドと選択 **[!UICONTROL Universal Video]**.

   * 他のタイプの広告タグの場合：アップロードするスプレッドシートファイル内で、各広告の「広告タイプ」フィールドに「 」と指定します。 **[!UICONTROL Universal Video]**.

1. [広告設定を開く](/help/dsp/campaign-management/ads/ad-edit.md) 新しい広告ごとに、該当するビデオ形式を選択します。

   * **[!UICONTROL VPAID]:** 視認性は常に測定されます。
   * **[!UICONTROL VPAID & VAST (Default)]:** 視認性の測定を許可しない在庫が含まれます。
   * **[!UICONTROL VAST]**  — 接続された TV インベントリに適しています。

   参照：[ユニバーサルビデオ広告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)」を参照してください。

1. [新しいユニバーサルビデオ広告の添付](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) をユニバーサルビデオ配置に追加します。

## ユニバーサルビデオの配置に Connected TV 環境が選択されている場合に、一部の最適化目標とパッケージが使用できないのはなぜですか？

標準の接続済み TV 配置と互換性のない目標（最低クリックコストなど）は、ユニバーサルビデオ配置の接続済み TV 環境ではサポートされません。 同様に、最適化目標に対応していないパッケージも選択できません。

## 実行するタイミング **[!UICONTROL VAST]** ユニバーサルビデオ広告にビデオ形式を使用しますか？

用途 **[!UICONTROL VAST]** 次のいずれかのシナリオの場合：

* 配置は、接続された TV 在庫をターゲットにします。
* この配置の対象となるのは、Google Ad Manager、Appnexus、SpotX または Freewheel のビデオ在庫です。 これらの SSP は、VPAID &amp; VAST ビデオ形式をサポートしていません。

## 複数のユニバーサルビデオ広告を同じユニバーサルビデオ配置にアタッチすることは可能ですか？

はい。
