---
title: ビデオおよびエクスペリエンスタグのトランスコーディングオプションのカスタマイズ
description: ビデオ広告タグのトランスコーディングオプションをカスタマイズする方法について説明します。
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
source-git-commit: f7d5bf3193cb41ca2a0d4415998209e5a9b724ba
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 0%

---

# ビデオおよびエクスペリエンスタグのトランスコーディングオプションのカスタマイズ

ビデオ広告エクスペリエンスのトランスコーディングオプションをカスタマイズして、パブリッシャー間での高速な再生と品質管理を確保できます。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、[**[!UICONTROL More]**] をクリックしてから [**[!UICONTROL Video Settings]**] をクリックします。

1. **[!UICONTROL Publisher-specific transcodes]** のリストで、トランスコーディングを適用するDSPを選択します。

1. 「**[!UICONTROL Save Settings]**」をクリックします。

## デフォルト（[!DNL Adobe] DSP）のトランスコーディング仕様

| ファイルタイプ | 寸法 | ビデオビットレート | ビデオフレームレート | オーディオビットレート | オーディオサンプルレート | 音声レベル |
|---|---|---|---|---|---|---|
| mp4 | 640x360 | 1,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 400x300 | 1,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1024x768 | 500 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x480 | 1,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 960x540 | 2,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 960x720 | 2,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1280x720 | 2,000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1920x1080 | 3,500 kbps | 23.98 fps | 128 kbps | 44.100 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x360 | 800 kbps | 23.98 fps | 96 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x360 | 400 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1920x1080 | 16000 kbps | 23.98 fps | 256 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |

>[!MORELIKETHIS]
>
>* [ クリエイティブライブラリについて ](/help/creative/creative-libraries/creative-libraries-about.md)
>* [ ターゲティングを使用したエクスペリエンスの作成 ](/help/creative/experiences/experience-create-targeting.md)
>* [ 該当するクリエイティブサイズの広告タグを手動で作成 ](experience-tag-create-manually.md)
>* [ ライブエクスペリエンス用の広告エクスペリエンスタグのエクスポートと実装 ](experience-tag-export.md)
