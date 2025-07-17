---
title: 該当するクリエイティブサイズの広告タグを手動で作成
description: 特定のクリエイティブサイズの広告タグを作成する方法を説明します。
feature: Creative Experiences
exl-id: 77dedfa2-33de-4a92-a58b-1a2b91842f0a
source-git-commit: e79becc860143b749ec96134e7b224649686c672
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 0%

---

# （ターゲティングなしのエクスペリエンス）該当するクリエイティブサイズの広告タグを手動で作成します

*デシジョンツリーのターゲット設定を使用しないエクスペリエンスのみ*
*クローズドベータ版*

エクスペリエンスに使用するクリエイティブサイズ（非ビデオクリエイティブ）またはビデオ時間ごとに、言語ごとに 1 つ以上の広告タグを作成できます。 後から [ クリエイティブを広告タグに割り当てる ](experience-tag-assign-creatives.md) ことができます。

>[!NOTE]
>
>デシジョンツリーのターゲット設定を使用するエクスペリエンスの場合、[!DNL Creative] では、該当するクリエイティブサイズまたはビデオ時間ごとに、言語ごとに 1 つのタグを自動的に作成します。

1. メインメニューで、**[!UICONTROL Creative]**/**[!UICONTROL Experiences]** をクリックします。

1. 次のいずれかの操作を行います。

   * カード表示で、エクスペリエンス名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Tag Manager]**」をクリックします。

   * テーブル ビューで、行の上にカーソルを置き、**[!UICONTROL More]** をクリックし、**[!UICONTROL Tag Manager]** をクリックします。

1. 右上で、「**[!UICONTROL Create Tag]**」をクリックします。

1. 一意の **[!UICONTROL Tag name]** を入力し、**[!UICONTROL Tag size]** ージの（標準ディスプレイ広告）または **[!UICONTROL Duration]** ージの（標準ビデオ広告）を選択します。

   エクスペリエンスのデフォルトのクリエイティブのサイズまたは時間によって、使用可能なクリエイティブのサイズやビデオの時間が決まります。

   同じクリエイティブサイズまたは期間に対して複数のタグを作成できます。<!-- What are the implications? -->

1. 「**[!UICONTROL Create]**」をクリックします。

   タグ行を展開すると、含まれているクリエイティブを確認できます。

   ビデオ広告エクスペリエンスの場合、ビデオクリエイティブは、Adobe Advertising DSP エンコーディングを使用して VAST 2.0 タグとして自動的にトランスコードされるので、プレビューできます。 オプションで [ 別のDSP用にトランスコーディングを適用する ](experience-tag-video-transcoding.md) ことができます。

>[!MORELIKETHIS]
>
>* [ ターゲティングを行わないエクスペリエンスの広告タグへのクリエイティブの割り当て ](experience-tag-assign-creatives.md)
>* [ ターゲット設定を行わないエクスペリエンス用のトラッキング URL のカスタマイズ ](experience-tracking-urls-no-targeting.md)
>* [ ターゲティングを行わないエクスペリエンスのクリエイティブな最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-no-targeting.md)
>* [ ビデオ広告エクスペリエンスタグのトランスコーディングオプションのカスタマイズ ](experience-tag-video-transcoding.md)
>* [ ライブエクスペリエンス用の広告エクスペリエンスタグのエクスポートと実装 ](experience-tag-export.md)
>* [ 広告タグの名前を変更 ](experience-tag-rename.md)
