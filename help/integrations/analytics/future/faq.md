---
title: FAQ
description: xxx
source-git-commit: 7845129ba6566c1aaaf160cc6f9ad33bf1731f75
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 0%

---

# FAQs xxx

## title

https://adobeadcloud.zendesk.com/agent/tickets/14214
デフォルトでは、Adobe Analyticsは各レポートでキャプチャされたすべてのイベントをレポートします。 「[!UICONTROL Unspecified]」イベントは、Adobe Advertisingに接続されていないフォーム完了イベントを表します。 例えば、Ad Platform レポートでは、メールキャンペーンによるオーガニックコンバージョンまたはコンバージョンは「未指定」に分類されます。

フィルターを使用して、「未指定（なし）を含める」オプションでチェックマークを削除することで、レポートから未指定のイベントを削除できます。<!-- Not sure if this is in DSP or in Analytics Workspace -->

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323
Adobe Analyticsのイベントタグは、Ad Cloudのピクセルと同じ場所に配置し、XXXが一致することを確認します。

## title

https://adobeadcloud.zendesk.com/agent/tickets/24323

質問：内部セキュリティ監査では、Ad Cloudを既存のAdobe Analytics インストールに統合したときに有効になったセキュリティ上の懸念として、特定の機能にフラグが付けられました。

問題の統合は、AdCloudとAdobe Audience Managerの間です。 この機能は、AdCloudとAdobe Audience Manager間の訪問者IDの一致率を高めます。 これは、pagead.l.doubleclick.net、star-mini.c10r.facebook.comおよびpug88000nf.pubmatic.comにネットワークリクエストを送信して、これらのサービスが利用できる訪問者の既存のIDを持っているかどうかを判断します。 これは、セキュリティリスクとしてフラグが立てられ、すべてのサイト訪問者に対して発生しているネットワークリクエストです。

監査人はこの機能を無効にするよう求めています。 これらのネットワークリクエストをブロックするとどうなりますか？

回答：当社の商品を確認したところ、問題のピクセルは、Ad Cloud、特定のインベントリ/SSP パートナー（DSPに関して）、およびAAM間のcookie マッチ率を向上させる目的で使用されていると述べました。  削除された場合、AAC/AAMと各ピクセルのインベントリパートナーとの間の一致率が何らかのレベルで低下する可能性がありますが、大きな影響は期待できません。

Ad Cloud Searchでは、広告主のCX Enterprise Organization IDがMathworks用に設定されていますが、アドビのプロダクトチームには、Ad CloudでオーディエンスをアクティベートするためのMathworksの設定が表示されていません。 Adobe Audience Managerを使用して、Ad Cloud Searchにオーディエンスを送信していますか？ そうでない場合、これらを削除しても現在のワークフローには影響しません。 AAM カスタマーケアでは、これらのピクセルを起動したくない場合は、これらのピクセルの削除を支援できます。

