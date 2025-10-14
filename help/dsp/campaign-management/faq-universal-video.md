---
title: ユニバーサルビデオに関する FAQ
description: ユニバーサルビデオ広告の詳細はこちら。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 8d65069b7da5d3c33cc7713c6c80af27eb6bf227
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# ユニバーサルビデオに関する FAQ

[&#x200B; ユニバーサルビデオ広告 &#x200B;](/help/dsp/campaign-management/ads/ad-about.md#ad-types) を使用すると、デスクトップ、モバイル、接続されたテレビ環境から、1 つのビデオの配置を使用して、VPAID および VAST のインベントリのビデオインベントリをターゲットに設定できます。

## ユニバーサルビデオプレースメントと広告を作成するにはどうすればよいですか？

ユニバーサルビデオプレースメントにはユニバーサルビデオ広告のみを含めることができ、ユニバーサルビデオ広告はユニバーサルビデオプレースメントにのみ添付できます。

他のタイプのプレースメントやビデオを作成する場合と同様に、ユニバーサルビデオプレースメントと広告を作成します。

1. 目的のキャンペーン内で [&#x200B; ユニバーサルビデオプレースメントを作成 &#x200B;](/help/dsp/campaign-management/placements/placement-create.md) し、[!UICONTROL Placement Type] のキャン **[!UICONTROL Universal Video]** ーンを選択します。

   ターゲットにする環境（デスクトップ、モバイル、接続テレビ）を少なくとも 1 つ指定する必要があります。

1. ユニバーサルビデオのプレースメントと同じキャンペーンで、[&#x200B; 単一のユニバーサルビデオ広告を作成 &#x200B;](/help/dsp/campaign-management/ads/ad-create.md) または [&#x200B; 複数のユニバーサルビデオ広告を作成 &#x200B;](/help/dsp/campaign-management/ads/ad-create-multiple.md) します。

   複数の広告を作成する場合は、[!UICONTROL Ad Type] のように「[!UICONTROL Universal Video]」を指定します。

   * [!DNL Google] または [!DNL Flashtalking] の広告の場合：ファイルをアップロードした後の「[!UICONTROL Review ad types]」ステップで、「**[!UICONTROL Ad Type]**」フィールドをクリックし、「**[!UICONTROL Universal Video]**」を選択します。

   * その他のタイプの広告タグの場合：アップロードするスプレッドシートファイル内で、**[!UICONTROL Universal Video]** のように各広告の「広告タイプ」フィールドを指定します。

1. 新しい広告ごとに [&#x200B; 広告設定を開く &#x200B;](/help/dsp/campaign-management/ads/ad-edit.md) と、該当するビデオ形式を選択します。

   * **[!UICONTROL VPAID]:** ビューアビリティは常に測定されます。
   * **[!UICONTROL VPAID & VAST (Default)]:** ビューアビリティ測定ができないインベントリが含まれています。
   * **[!UICONTROL VAST]** – 接続された TV インベントリに適しています。

   詳しくは、「[&#x200B; ユニバーサルビデオ広告設定 &#x200B;](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)」を参照してください。

1. ユニバーサルビデオのプレースメントに [&#x200B; 新しいユニバーサルビデオ広告を添付 &#x200B;](/help/dsp/campaign-management/ads/ad-attach-to-placement.md) します。

## ユニバーサルビデオのプレースメントに対して「Connected TV」環境が選択されている場合、一部の最適化目標とパッケージが使用できないのはなぜですか？

クリック単価の最低値など、標準の接続された TV 配置と互換性のない目標は、ユニバーサルビデオ配置の接続された TV 環境ではサポートされません。 同様に、互換性のない最適化目標を持つパッケージも選択できません。

## ユニバーサルビデオ広告に **[!UICONTROL VAST]** ビデオ形式を使用するには、どうしたらよいですか？

**[!UICONTROL VAST]** は、次のいずれかのシナリオで使用します。

* 配置ターゲットが接続された TV インベントリ。
* プレースメントは、Google Ad Manager、Appnexus、SpotX または Freewheel のビデオインベントリをターゲットにします。 これらの SSP は、VPAID &amp; VAST ビデオフォーマットをサポートしていません。

## 同じユニバーサルビデオ配置に複数のユニバーサルビデオ広告を添付できますか？

はい。
