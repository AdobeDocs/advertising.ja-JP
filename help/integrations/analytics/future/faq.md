---
title: よくある質問
description: xxx
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '355'
ht-degree: 0%

---

# FAQ xxx

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/14214
デフォルトでは、Adobe Analyticsは、すべてのレポートで取り込まれたすべてのイベントをレポートします。 「[!UICONTROL Unspecified]」イベントは、Adobe Advertisingに接続されなかったフォーム完了イベントを表します。 例えば、広告プラットフォームレポートでは、オーガニックコンバージョンまたはメールキャンペーンによるコンバージョンは、「未指定」に分類されます。

このフィルターを使用して「未指定（なし）を含める」オプションのチェックマークを削除すると、レポートから未指定のイベントを削除できます。<!-- Not sure if this is in DSP or in Analytics Workspace -->

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/24323
Analytics イベントタグをAd Cloud ピクセルと同じ場所に配置して、XXX が一致することを確認します。

## タイトル

https://adobeadcloud.zendesk.com/agent/tickets/24323

Q：内部セキュリティ監査で、Ad Cloudを既存のAdobe Analytics インストールに統合した際に有効にしたセキュリティ上の問題として特定の機能がフラグ付けされました。

問題となっている統合は、AdCloud とAdobe Audience Managerの間です。 この機能により、AdCloud とAdobe Audience Managerの間の訪問者 ID の一致率が高まります。 これを行うには、pagead.l.doubleclick.net、star-mini.c10r.facebook.comおよびpug88000nf.pubmatic.comにネットワークリクエストを送信し、これらのサービスが活用可能な訪問者の既存の ID を持っているかどうかを確認します。 これらは、セキュリティ上のリスクとしてフラグが設定され、すべてのサイト訪問者に対して発生しているネットワークリクエストです。

この機能を無効にするよう監査担当者から依頼されています。 これらのネットワークリクエストをブロックするとどうなりますか？

A：商品を確認したところ、問題のピクセルは、Ad Cloud、特定の在庫/SSP パートナー（DSPに関するもの）およびAAMの間で cookie の一致率を高めることを目的としているとのことでした。  削除すると、AAC/AAMと、それぞれのピクセルがある在庫パートナーとの間で、ある程度のマッチ率の低下が見られる場合がありますが、それほど大きな差は期待できません。

Ad Cloud検索では、広告主のExperience Cloud組織 ID が Mathworks 用に設定されていますが、アドビのプロダクトチームには、Ad Cloudでオーディエンスをアクティブ化するための Mathworks 設定が表示されません。 オーディエンスをAd Cloud検索に送信するために、Adobe Audience Manager を使用していますか？ そうでない場合、これらを削除しても現在のワークフローには影響しません。 これらのピクセルを使用したくない場合は、AAM カスタマーケアにお問い合わせください。

