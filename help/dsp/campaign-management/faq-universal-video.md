---
title: ユニバーサルビデオに関するFAQ
description: ユニバーサル動画広告について詳しく見る。
feature: DSP Placements, DSP Ads
exl-id: 48c744ae-90a3-47e9-a5dc-c4e3c01b75a0
TQID: https://experienceleague.adobe.com/LAzSivup-EVuDgtWN1T58lfRjzgrchIiFF9-lMJAVlw
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2: id: a4886037-b6d8-40e1-aeab-edeb7649d7d3id: d9510790-d834-436d-8423-8d69cd50464a
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: c2be0313-b3ae-45e0-b454-d20bf54b23f2id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 348
ht-degree: 0%

---

# ユニバーサルビデオに関するFAQ

[ ユニバーサル動画広告](/help/dsp/campaign-management/ads/ad-about.md#ad-types)を使用すると、VPAIDおよびVASTの広告枠に対応したデスクトップ、モバイル、コネクテッド TV環境の動画広告枠を1つの動画枠でターゲットにすることができます。

## ユニバーサル動画のプレースメントと広告はどのように作成するのですか？

ユニバーサルビデオのプレースメントには、ユニバーサルビデオ広告のみを含めることができ、ユニバーサルビデオ広告は、ユニバーサルビデオのプレースメントにのみ添付することができます。

他の種類のプレースメントやビデオの作成方法と同様に、ユニバーサルビデオのプレースメントと広告を作成します。

1. 目的のキャンペーン内で、[ ユニバーサルビデオ配置](/help/dsp/campaign-management/placements/placement-create.md)を作成し、[!UICONTROL Placement Type] **[!UICONTROL Universal Video]**&#x200B;を選択します。

   ターゲットに少なくとも1つの環境（デスクトップ、モバイル、コネクテッド TV）を指定する必要があります。

1. ユニバーサルビデオのプレースメントと同じキャンペーンで、[単一のユニバーサルビデオ広告を作成](/help/dsp/campaign-management/ads/ad-create.md)または[複数のユニバーサルビデオ広告を作成](/help/dsp/campaign-management/ads/ad-create-multiple.md)。

   複数の広告を作成する場合は、必ず「[!UICONTROL Universal Video]」を[!UICONTROL Ad Type]として指定してください。

   * [!DNL Google]または[!DNL Flashtalking]広告の場合：ファイルをアップロードした後の「[!UICONTROL Review ad types]」ステップで、「**[!UICONTROL Ad Type]**」フィールドをクリックして「**[!UICONTROL Universal Video]**」を選択します。

   * その他のタイプの広告タグの場合：アップロードしたスプレッドシート ファイル内で、各広告の広告タイプ フィールドを&#x200B;**[!UICONTROL Universal Video]**&#x200B;として指定します。

1. [新しい広告ごとに広告設定](/help/dsp/campaign-management/ads/ad-edit.md)を開き、該当するビデオ形式を選択します。

   * **[!UICONTROL VPAID]:** ビューアビリティは常に測定されます。
   * **[!UICONTROL VPAID & VAST (Default)]:** ビューアビリティの測定を許可しないインベントリが含まれています。
   * **[!UICONTROL VAST]** – 接続されたテレビ インベントリに適しています。

   詳しくは、「[ ユニバーサルビデオ広告設定](/help/dsp/campaign-management/ads/ad-settings-universal-video.md)」を参照してください。

1. [新しいユニバーサル ビデオ広告](/help/dsp/campaign-management/ads/ad-attach-to-placement.md)をユニバーサル ビデオ プレースメントに添付します。

## ユニバーサルビデオのプレースメントにコネクテッド TV環境が選択されている場合、一部の最適化目標とパッケージが使用できないのはなぜですか？

「クリック単価が最も低い」など、標準的なコネクテッド TV プレースメントと互換性のない目標は、ユニバーサルビデオプレースメントのコネクテッド TV環境ではサポートされていません。 同様に、互換性のない最適化目標を持つパッケージも選択できません。

## ユニバーサルビデオ広告に&#x200B;**[!UICONTROL VAST]** ビデオ形式をいつ使用しますか？

次のいずれかのシナリオで&#x200B;**[!UICONTROL VAST]**&#x200B;を使用します。

* プレースメントは、コネクテッド TVのインベントリをターゲットにします。
* このプレースメントは、Google Ad Manager、Appnexus、SpotX、FreeWheelなどのビデオインベントリをターゲットにしています。 これらのSSPは、VPAIDおよびVAST ビデオ形式をサポートしていません。

## 複数のユニバーサルビデオ広告を同じユニバーサルビデオの配置に添付できますか？

はい。
