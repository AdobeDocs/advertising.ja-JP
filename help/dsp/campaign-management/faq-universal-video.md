---
title: ユニバーサルビデオに関するFAQ
description: ユニバーサル動画広告について詳しく見る。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
source-git-commit: 1e307a95d597f20c97683ee20c0a3b99f662f7fd
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 0%

---

# ユニバーサルビデオに関するFAQ

[&#x200B; ユニバーサル動画広告](/help/dsp/campaign-management/ads/ad-about.md#ad-types)を使用すると、VPAIDおよびVASTの広告枠に対応したデスクトップ、モバイル、コネクテッド TV環境の動画広告枠を1つの動画枠でターゲットにすることができます。

## ユニバーサル動画のプレースメントと広告はどのように作成するのですか？

ユニバーサルビデオのプレースメントには、ユニバーサルビデオ広告のみを含めることができ、ユニバーサルビデオ広告は、ユニバーサルビデオのプレースメントにのみ添付することができます。

他の種類のプレースメントやビデオの作成方法と同様に、ユニバーサルビデオのプレースメントと広告を作成します。

1. 目的のキャンペーン内で、[&#x200B; ユニバーサルビデオ配置](/help/dsp/campaign-management/placements/placement-create.md)を作成し、[!UICONTROL Placement Type] **[!UICONTROL Universal Video]**&#x200B;を選択します。

   ターゲットに少なくとも1つの環境（デスクトップ、モバイル、コネクテッド TV）を指定する必要があります。

1. ユニバーサルビデオのプレースメントと同じキャンペーンで、[単一のユニバーサルビデオ広告を作成](/help/dsp/campaign-management/ads/ad-create.md)または[複数のユニバーサルビデオ広告を作成](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

   複数の広告を作成する場合は、必ず「[!UICONTROL Universal Video]」を[!UICONTROL Ad Type]として指定してください。

   * [!DNL Google]または[!DNL Flashtalking]広告の場合：ファイルをアップロードした後の「[!UICONTROL Review ad types]」ステップで、「**[!UICONTROL Ad Type]**」フィールドをクリックして「**[!UICONTROL Universal Video]**」を選択します。

   * その他のタイプの広告タグの場合：アップロードしたスプレッドシート ファイル内で、各広告の広告タイプ フィールドを&#x200B;**[!UICONTROL Universal Video]**&#x200B;として指定します。

1. [新しい広告ごとに広告設定](/help/dsp/campaign-management/ads/ad-edit.md)を開き、該当するビデオ形式を選択します。

   * **[!UICONTROL VPAID]:** ビューアビリティは常に測定されます。
   * **[!UICONTROL VPAID & VAST (Default)]:** ビューアビリティの測定を許可しないインベントリが含まれています。
   * **[!UICONTROL VAST]** – 接続されたテレビ インベントリに適しています。

   詳しくは、「[&#x200B; ユニバーサルビデオ広告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)」を参照してください。

1. [新しいユニバーサル ビデオ広告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)をユニバーサル ビデオ プレースメントに添付します。

## ユニバーサルビデオのプレースメントにコネクテッド TV環境が選択されている場合、一部の最適化目標とパッケージが使用できないのはなぜですか？

「クリック単価が最も低い」など、標準的なコネクテッド TV プレースメントと互換性のない目標は、ユニバーサルビデオプレースメントのコネクテッド TV環境ではサポートされていません。 同様に、互換性のない最適化目標を持つパッケージも選択できません。

## ユニバーサルビデオ広告に&#x200B;**[!UICONTROL VAST]** ビデオ形式をいつ使用しますか？

次のいずれかのシナリオで&#x200B;**[!UICONTROL VAST]**&#x200B;を使用します。

* プレースメントは、コネクテッド TVのインベントリをターゲットにします。
* このプレースメントは、Google Ad Manager、Appnexus、SpotX、FreeWheelなどのビデオインベントリをターゲットにしています。 これらのSSPは、VPAIDおよびVAST ビデオ形式をサポートしていません。

## 複数のユニバーサルビデオ広告を同じユニバーサルビデオの配置に添付できますか？

はい。
