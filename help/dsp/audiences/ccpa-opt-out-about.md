---
title: '[!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポートについて'
description: CCPA の販売オプトアウトリクエストから ID をトラックするセグメントを作成する方法と、ID のレポートを取得する方法について説明します。
feature: CCPA, DSP Segments
exl-id: 28b5e00b-a695-46f1-abbf-7bbd78f05411
source-git-commit: 4b9cc5956d573b346eacdf71a8ea490c162b4660
workflow-type: tm+mt
source-wordcount: '243'
ht-degree: 0%

---

# [!UICONTROL CCPA Opt-out-of-Sale] セグメントとレポートについて

カリフォルニア州消費者プライバシー法（CCPA）に従い、web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡するには、[CCPA の販売オプトアウトセグメントを作成および実装する &#x200B;](ccpa-opt-out-segment-create.md) ことができます。 ユーザーは、CCPA の販売のオプトアウトセグメントに無期限に残ります。

セグメントピクセルタグが実装されると、Adobe Advertisingは、広告主に代わって ID のプールの収集を開始します。

## 消費者の販売オプトアウトレポート

Adobe Advertisingは、アカウントの販売オプトアウトリクエスト用に顧客が送信した ID の月間レポートを生成します。 データは、DSPで作成された CCPA の販売のオプトアウトセグメントと、Privacy ServiceAPI を介して行われた送信を使用してキャプチャされたリクエストを統合します。  レポートは、前月の各月の最初に生成されます。 例えば、6 月の月次ユーザーリストは 7 月 1 日に利用できます。

各レポートは、タブ区切りのテキストファイルとして、GZIP 形式に圧縮して利用できます。 CCPA の販売オプトアウトセグメントで取得されたユーザー ID は、セグメント別および広告主別に識別されます。

過去 3 か月以内にDSP内から [&#x200B; またはDSP [!DNL Trafficking API] を使用して作成した &#x200B;](ccpa-opt-out-segment-report-retrieve.md) 月次レポートへのリンクを取得）できます。 各リンクは 7 日間有効ですが、顧客がリンクを取得しようとするたびに更新されます。

>[!MORELIKETHIS]
>
>* [&#x200B; カリフォルニア州消費者プライバシー法のAdobe Advertisingサポート：消費者オプトアウトサポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントの作成と実装 &#x200B;](ccpa-opt-out-segment-create.md)
>* [&#x200B; 消費者の販売オプトアウトレポートの取得 &#x200B;](ccpa-opt-out-segment-report-retrieve.md)
>* [Audience Management について &#x200B;](audience-about.md)
