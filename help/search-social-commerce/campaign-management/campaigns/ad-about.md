---
title: 広告を管理
description: Search, Social, & Commerceの広告について説明します。
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
TQID: https://experienceleague.adobe.com/zjdXTfuUM3gknKy2-ASRGz5wv7DAr-SZmpfLSuhhpoU
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
source-git-commit: 47de92fd6d4b1d481380a58f75ec4735d95fca73
workflow-type: tm+mt
source-wordcount: 918
ht-degree: 0%

---

# 広告について

*[!DNL Google Ads]、[!DNL LY Ads]、[!DNL Microsoft Advertising]、[!DNL Yandex]および既存の[!DNL Baidu] アカウントのみ*

ターゲット web サイト（コンテンツまたはプレースメントをターゲットにしたキャンペーン）に広告を表示できます。ユーザーが広告グループ内のキーワード（検索キャンペーン用）またはweb サイト上のコンテンツ（検索専用キャンペーンの[!DNL Google Ads]の動的検索広告）を検索する場合、またはユーザーが[!DNL Google Merchant Center]または[!DNL Microsoft Merchant Center]製品フィード内の項目のいずれかに関連する検索を実行する場合（[!DNL Google Ads]のショッピング広告または[!DNL Microsoft Advertising] キャンペーンの製品広告）。

## 利用可能な広告タイプ

同期広告ネットワークアカウント内の広告グループでサポートされている広告タイプを作成および管理できます。

* 検索ネットワークをターゲットとするキャンペーンの広告グループの&#x200B;**テキスト広告または拡張テキスト広告**。 テキスト広告には、広告グループレベルまたはキャンペーンレベルのパラメーターを上書きする、オプションのトラッキングパラメーターを含めることができます。 広告ネットワークによっては、拡張/拡張テキスト広告または標準テキスト広告を作成できる場合があります。

* [!DNL Microsoft Audience Network]の[!DNL Microsoft Advertising]件のキャンペーンに対するクロスデバイスのネイティブ **オーディエンス広告**。 キャンペーン設定に基づいて、オーディエンス広告には2つのオプションがあります。

   * キャンペーンが加盟店センターストアにリンクされている場合、広告ネットワークは、ストアの商品情報を使用して、キャンペーン用の広告フィードベースの広告を自動的に生成します。 キャンペーン用にフィードベースの広告を作成する必要はありませんが、ユーザーターゲティングを使用して広告グループを作成する必要があります。

   * キャンペーンが加盟店センターのアカウントにリンクされていない場合は、複数のテキストや画像アセットを含むレスポンシブ広告フォーマットを使用して、画像ベースのオーディエンス広告を作成します。 広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を組み立て、[!DNL MSN]、[!DNL Outlook.com]、[!DNL Microsoft Edge]などのサイトに表示します。

* 検索ネットワーク上の[!DNL Google Ads]件のキャンペーンに対する&#x200B;**呼び出し専用広告**。 通話のみの広告は、電話番号を含むテキスト広告です。 オプションで、高度な通話レポートに[!DNL Google Ads]割り当てられた転送番号を使用できます。

* **検索キャンペーンの[!DNL Google Ads]および[!DNL Microsoft Advertising]の動的検索広告グループに対して、動的検索広告** （現在は広告ネットワーク上で「動的検索広告」と呼ばれています）を拡張しました。 動的検索広告では、広告を表示するタイミングを決定するために、キーワードではなくweb サイトのコンテンツを使用します。 広告ネットワークは、見出しを動的に生成し、ランディングページのURLと表示URLを選択し、最終的なURLを自動的に生成します。

  広告グループに特定の動的検索対象を設定することで、動的検索広告のターゲットにコンテンツを使用するweb サイト内のページを定義できます。 [!DNL Google Ads]では、Search, Social, &amp; Commerceで動的検索対象を作成できます。[!DNL Microsoft Advertising]では、[!DNL Microsoft Advertising]内で動的検索対象を作成する必要があります。 [!DNL Google Ads] キャンペーンでは、動的な検索ターゲットを作成する代わりに、または動的な検索ターゲットに加えて、キャンペーンの「[!DNL DSA Options]」セクションでweb サイトのドメインと言語をオプションで指定できます。

  ユーザーの検索語が、キーワードベースのキャンペーンの1つのキーワードと完全に一致すると、動的な検索広告の代わりに、キーワードベースのキャンペーンの広告が表示されます。 ユーザーの検索語句がキーワードの1つに一致するかフレーズ一致し、動的検索広告の広告ランクが高い場合、広告ネットワークには、キーワードをターゲットにした広告ではなく動的検索広告が表示されます。

  動的検索広告について詳しくは、[[!DNL Google Ads]  ドキュメント ](https://support.google.com/google-ads/answer/2471185)および[[!DNL Microsoft Advertising]  ドキュメント ](https://help.ads.microsoft.com/#apex/ads/en/56794)を参照してください。

* [!DNL Microsoft Advertising]件の検索キャンペーンの&#x200B;**マルチメディア広告**。 マルチメディア広告は、メインラインとサイドバーの目立つ位置に表示される大きな画像広告で、ページごとに1つのマルチメディア広告のみが表示されます。 レスポンシブ広告のように、複数のテキストや画像のアセットを含めることができます。また、広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を組み立てます。 マルチメディア広告がテキスト広告の配置を置き換えることはありません。

* ショッピング ネットワーク上の&#x200B;**[!DNL Microsoft Advertising]製品（ショッピング）広告**&#x200B;のプロモーション ライン。 ショッピング広告では、広告の表示方法と場所を決定するために、キーワードの代わりに既存の[!DNL Microsoft Merchant Center]製品フィードで製品を使用します。 広告のコピーとランディングページのURLは、フィード内の製品情報から自動的に生成されますが、オプションで広告グループに含めるプロモーションラインを設定できます。

  広告グループに個別の製品グループを設定して、[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] ビューから、[!DNL Microsoft Advertising] ショッピング広告に表示される製品を制御できます。

  商品/ショッピング広告のワークフローについて詳しくは、「[実装 [!DNL Microsoft Advertising]  ショッピングキャンペーン ](/help/search-social-commerce/campaign-management/special-workflows/microsoft-shopping-campaigns.md)」を参照してください。  商品の広告について詳しくは、[Microsoft Advertising ドキュメント ](https://help.ads.microsoft.com/#apex/3/en/51082)を参照してください。

* 検索ネットワーク上の[!DNL Google Ads]および[!DNL Microsoft Advertising]件のキャンペーンのレスポンシブ検索広告。 広告ネットワークは、一連の広告タイトルと説明からテキストベースのレスポンシブ検索広告を動的に組み合わせ、パフォーマンスが高い組み合わせを好みます。 この広告には、最大3つの見出し、2つの説明、およびベース URLとオプションのpath1およびpath2 フィールドからのカスタマイズ可能なURLが含まれます。 オプションで、特定の位置に広告タイトルと説明をピン留めすることができます。

>[!NOTE]
>
>[!DNL Google Ads]は、ネイティブエディター以外では、広告として表示されたテキストの組み合わせに関するデータを提供しません。 各テキストの組み合わせのレポートについて詳しくは、[Google Ads ドキュメント ](https://support.google.com/google-ads/answer/7684791)を参照してください。

## [!UICONTROL Ads] ビュー

広告のステータスは、[!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] ビューから作成、編集、変更できます。

## 広告レベルのパフォーマンスデータ

広告レベルのデータは、ほとんどの広告タイプで利用可能です。

ただし、[!DNL Google Ads]件の動的検索広告（DSA）、パフォーマンスの最大値、スマートショッピング、および[!DNL YouTube]件のキャンペーンでは使用できません。 キャンペーンの広告レベルの合計データとキャンペーンの合計データの間に不一致が生じることを想定しています。

| 広告ネットワーク/キャンペーン/広告タイプ | データの可用性 |
|---|---|
| [!DNL Google Ads]件の動的検索広告（DSA） | キャンペーン、広告グループ |
| パフォーマンスの最大値：[!DNL Google Ads] | キャンペーン |
| [!DNL Google Ads]件のショッピング、スマートショッピング | キャンペーン、広告グループ |
| [!DNL Google Ads] [!DNL YouTube] | キャンペーン、広告グループ |

>[!MORELIKETHIS]
>
>* [広告の管理](ad-manage.md)
