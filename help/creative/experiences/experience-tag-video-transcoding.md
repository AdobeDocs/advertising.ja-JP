---
title: 動画広告エクスペリエンスタグのトランスコーディングオプションをカスタマイズする
description: ビデオ広告タグのトランスコーディングオプションをカスタマイズする方法について説明します。
feature: Creative Experiences
exl-id: 6100213c-2e7d-4e98-a3ab-045ca10e5174
TQID: https://experienceleague.adobe.com/N-tKrSHyE18QVazmdUlurPsW-7QVwGKAOPl2ArnI-2c
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 306
ht-degree: 0%

---

# 動画広告エクスペリエンスタグのトランスコーディングオプションをカスタマイズする

ビデオ広告エクスペリエンスのトランスコーディングオプションをカスタマイズして、パブリッシャー間で迅速な再生と品質管理を確保できます。

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Experiences]**&#x200B;をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

   * テーブル表示で、行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Tag Manager]**&#x200B;をクリックします。

1. 該当する広告タグの行の上にカーソルを置き、**[!UICONTROL More]**&#x200B;をクリックしてから、**[!UICONTROL Video Settings]**&#x200B;をクリックします。

1. **[!UICONTROL Publisher-specific transcodes]**&#x200B;のリストで、トランスコードを適用するDSPを選択します。

1. **[!UICONTROL Save Settings]**&#x200B;をクリックします。

## 既定（[!DNL Adobe] DSP）のトランスコード仕様

| ファイルタイプ | ディメンション | ビデオビットレート | ビデオフレームレート | オーディオビットレート | オーディオサンプルレート | 音声レベル |
|---|---|---|---|---|---|---|
| mp4 | 640x360 | 1000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 400x300 | 1000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1024x768 | 500 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x480 | 1000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 960x540 | 2000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 960x720 | 2000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1280 x 720 | 2000 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1920x1080 | 3500 kbps | 23.98 fps | 128 kbps | 44.100 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x360 | 800 kbps | 23.98 fps | 96 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 640x360 | 400 kbps | 23.98 fps | 128 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |
| mp4 | 1920x1080 | 16000 kbps | 23.98 fps | 256 kbps | 48.000 kHz | 24 LKFS （+/- 2.0 dB） |

>[!MORELIKETHIS]
>
>* [&#x200B; クリエイティブライブラリについて](/help/creative/creative-libraries/creative-libraries-about.md)
>* [&#x200B; ターゲティングでエクスペリエンスを作成](/help/creative/experiences/experience-create-targeting.md)
>* [該当するクリエイティブサイズの広告タグを手動で作成する](experience-tag-create-manually.md)
>* [&#x200B; ライブエクスペリエンスの広告エクスペリエンスタグの書き出しと実装](experience-tag-export.md)
