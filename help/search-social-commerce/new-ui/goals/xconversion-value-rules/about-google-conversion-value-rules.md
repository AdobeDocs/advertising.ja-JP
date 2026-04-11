---
title: 約 [!DNL Google Ads]  コンバージョン値ルール
description: Search, Social, & Commerceで [!DNL Google Ads]  コンバージョン値ルールを表示および管理する方法について説明します。
source-git-commit: e15d34f3f32a8565735e53f1ce40e71008dbb4d9
workflow-type: tm+mt
source-wordcount: '454'
ht-degree: 0%

---

# [!DNL Google Ads]個のコンバージョン値ルールについて

Search, Social, &amp; Commerceは、[&#x200B; コンバージョン値ルール &#x200B;](https://support.google.com/google-ads/answer/10518330)を[!DNL Google Ads] アカウントから自動的に同期します。 コンバージョン値ルールを使用すると、デバイスの種類、場所、オーディエンスセグメントなどのユーザー情報に基づいて、コンバージョンイベントの値を調整できます。 Google Smart Biddingを使用すると、検索、表示、ショッピング、パフォーマンスの最大化キャンペーンでバリューベース入札のルールを使用できます。 コンバージョンの最大化とターゲット ROAS入札戦略を使用するキャンペーンの場合、[!DNL Google Ads] アルゴリズムは、より高い値のコンバージョンを優先します。

キャンペーンレベルのコンバージョン値ルールは、アカウントレベルのルールを上書きします。 コンバージョンが複数のコンバージョン値ルールを満たす場合、ルールのうち1つだけが適用されます。 通常、最も特定のルールが適用されますが、様々なルール条件タイプの優先順位に関する[[!DNL Google Ads]  ドキュメント &#x200B;](https://support.google.com/google-ads/answer/10520348)を参照してください。

## [!UICONTROL Conversion Value Rules] ビューと機能

[!DNL Google Ads] インターフェイスで作成されたすべてのルールは、24時間以内に同期され、[!UICONTROL Goals] > [!UICONTROL Conversion Value Rules] ビューで使用できます。 一部のアカウントでは、コンバージョン値のルールを管理できます。

* 個人のアカウントレベルまたはキャンペーンレベルでコンバージョンを追跡するアカウントでは、アカウントレベルおよびキャンペーンレベルのルールのステータスを作成、編集および変更できます。

  アカウントは[!DNL Google Ads]個のマネージャーアカウントにリンクできますが、クロスアカウントコンバージョントラッキング（マネージャーアカウント内のすべてのアカウントでコンバージョンがトラッキングされる）を使用することはできません。

* クロスアカウントのコンバージョントラッキングを使用するアカウントでは、アカウントレベルのルールとキャンペーンレベルのルールがマネージャーアカウントから継承され、読み取り専用です。

## Search, Social, &amp; Commerceのポートフォリオによるコンバージョン価値ルール

広告主アカウントがSearch, Social, &amp; Commerceの目標を[!DNL Google Ads]にアップロードするように設定されており、目標を持つポートフォリオにコンバージョン値ルールを使用するキャンペーンを含める場合、[!DNL Google Ads]は、目標で指定された元のコンバージョン値にコンバージョン値ルールを適用します。 その結果、Search、Social、およびCommerceのコンバージョンデータは、[!DNL Google Ads]のコンバージョンデータとは異なります。

例えば、目標が単一のコンバージョン指標「リード」を使用し、モバイルデバイスからのコンバージョンに10の重みを与え、非モバイルデバイスからのコンバージョンに10の重みを与えるとします。 Search, Social, &amp; Commerceでは、いずれかのデバイスタイプのイベントを1回のコンバージョンとしてカウントし、コンバージョン値を10としてクレジットします。 ただし、そのポートフォリオのキャンペーンで「デバイスがモバイルの場合は、2を掛ける」というコンバージョン値ルールが使用されているとします。 モバイルリードイベントがそのキャンペーンで追跡されると、[!DNL Google Ads]はコンバージョン数を1つ（1）とクレジットしますが、コンバージョン値は（10 x 2） = 20とクレジットします。

ルールが適用される前の元のコンバージョン値を含む、ルールの詳細については、[&#x200B; [!DNL Google Ads]の](https://support.google.com/google-ads/answer/10519848) コンバージョン値ルール レポートを参照してください。

>[!MORELIKETHIS]
>
>* [&#x200B; コンバージョン値ルールを作成 [!DNL Google Ads] します](create-google-conversion-value-rule.md)
>* [&#x200B; コンバージョン値ルールの編集 [!DNL Google Ads] &#x200B;](edit-google-conversion-value-rule.md)
>* [&#x200B; コンバージョン値ルール  [!DNL Google Ads] のステータスを変更](change-the-status-of-google-conversion-value-rule.md)
>* [[!DNL Google Ads]  コンバージョン値ルール設定](google-conversion-value-rule-settings.md)

