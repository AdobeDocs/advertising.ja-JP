---
title: 広告の管理
description: 利用可能な広告タイプを含む、検索、ソーシャル、コマースの広告について説明します。
exl-id: 01bd211d-fe6b-4329-90e1-0e54d626c125
feature: Search Campaign Management
source-git-commit: b2d578d0e15e647a57353dbfbde666b5e72d79f2
workflow-type: tm+mt
source-wordcount: '883'
ht-degree: 0%

---

# 広告について

*[!DNL Google Ads], [!DNL Microsoft® Advertising], [!DNL Yahoo! Japan Ads], [!DNL Yandex]、および既存 [!DNL Baidu] アカウントのみ*

広告は、ターゲット Web サイト（コンテンツ、プレースメントターゲット、キャンペーン）に表示できます。ユーザーが広告グループ内のキーワードの 1 つを検索すると（検索キャンペーン用）、Web サイト上のコンテンツ ( 動的検索広告 [!DNL Google Ads] 検索のみのキャンペーン )、またはユーザーが [!DNL Google Merchant Center] または [!DNL Microsoft® Merchant Center] 製品フィード ( [!DNL Google Ads] または製品広告 [!DNL Microsoft® Advertising] キャンペーン )。

## 使用可能な広告タイプ

同期済み広告ネットワークアカウント内の広告グループに対して、サポートされる広告タイプを作成および管理できます。

* **テキスト広告または拡張テキスト広告** 検索ネットワークをターゲットとするキャンペーン内の広告グループの場合。 テキスト広告には、広告グループまたはキャンペーンレベルのパラメーターを上書きする、オプションのトラッキングパラメーターを含めることができます。 広告ネットワークに応じて、拡張/拡張テキスト広告または標準テキスト広告を作成できます。

* クロスデバイス、ネイティブ **オーディエンス広告** 対象： [!DNL Microsoft® Advertising] キャンペーン [!DNL Microsoft® Audience Network]. オーディエンス広告には、キャンペーン設定に基づく 2 つのオプションがあります。

   * キャンペーンがマーチャントセンターのストアにリンクされている場合は、広告ネットワークで、ストアの製品情報を使用して、キャンペーンの広告フィードベースの広告を自動的に生成できます。 キャンペーン用にフィードベースの広告を作成する必要はありませんが、ユーザーターゲティングを使用して広告グループを作成する必要があります。

   * キャンペーンがマーチャントセンターアカウントにリンクされていない場合は、複数のテキストおよび画像アセットを含むレスポンシブ広告形式を使用して画像ベースのオーディエンス広告を作成します。 広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を構築し、広告を [!DNL MSN], [!DNL Outlook.com]、および [!DNL Microsoft® Edge].

* **通話のみの広告** 対象： [!DNL Google Ads] キャンペーンを検索ネットワーク上に配置します。 通話のみの広告は、電話番号を含むテキスト広告です。 オプションで、 [!DNL Google Ads] — 高度な通話レポート用に割り当てられた転送番号。

* **動的検索広告の拡張** （現在は、広告ネットワーク上で「動的検索広告」と呼ばれます） [!DNL Google Ads] および [!DNL Microsoft® Advertising] 検索キャンペーンの動的検索広告グループ。 動的検索広告は、広告を表示するタイミングを決定するために、キーワードの代わりに Web サイトのコンテンツを使用します。 広告ネットワークはヘッドラインを動的に生成し、ランディングページの URL と表示 URL を選択して、最終的な URL を自動的に生成します。

  広告グループの特定の動的検索ターゲットを設定することで、動的検索広告のターゲットにコンテンツを使用する Web サイト内のページを定義できます。 の場合 [!DNL Google Ads]検索、ソーシャル、コマースで動的検索ターゲットを作成できます。 [!DNL Microsoft® Advertising]に設定する場合は、内で作成する必要があります [!DNL Microsoft® Advertising]. In [!DNL Google Ads] キャンペーンの場合は、必要に応じて、キャンペーンの「[!DNL DSA Options]」セクションに追加する必要があります。

  ユーザーの検索語句がキーワードベースのキャンペーンの 1 つのキーワードと完全に一致する場合、動的な検索広告の代わりに、キーワードベースのキャンペーンの広告が表示されます。 ユーザーの検索語句がキーワードの 1 つに一致し、動的検索広告の広告ランクが高い場合、広告ネットワークは、キーワードターゲット広告ではなく動的検索広告を表示します。

  動的検索広告について詳しくは、 [[!DNL Google Ads] ドキュメント](https://support.google.com/google-ads/answer/2471185) および [[!DNL Microsoft® Advertising] ドキュメント](https://help.ads.microsoft.com/#apex/ads/en/56794).

* **マルチメディア広告** 対象： [!DNL Microsoft® Advertising] キャンペーンを検索します。 マルチメディア広告は、大きな画像広告で、目立つメインラインやサイドバーの位置に表示され、1 ページにつき 1 つのマルチメディア広告のみが表示されます。 レスポンシブ広告のように、複数のテキストおよび画像アセットを含めることができ、広告ネットワークは、広告要素の最も効果的な組み合わせを使用して広告を構築します。 マルチメディア広告がテキスト広告の配置を置き換えることはありません。

* 次のプロモーション行： **[!DNL Microsoft® Advertising]製品（買い物）広告** 買い物ネットワーク上で ショッピング広告は、既存の [!DNL Microsoft® Merchant Center] 広告の表示方法と表示場所を決定するために、キーワードの代わりに製品フィードを使用します。 広告コピーとランディングページの URL は、フィードの製品情報から自動的に生成されますが、オプションで広告グループに含めるプロモーション行を設定できます。

  どの製品を [!DNL Microsoft® Advertising] 広告グループに対して、 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Product Groups] 表示。

  製品/ショッピング広告のワークフローについて詳しくは、[実装方法 [!DNL Microsoft® Advertising] 買い物キャンペーン](/help/search-social-commerce/campaign-management/special-campaign-types/microsoft-shopping-campaigns.md).&quot;  製品広告について詳しくは、 [Microsoft® Advertising ドキュメント](https://help.ads.microsoft.com/#apex/3/en/51082).

* レスポンシブ検索広告： [!DNL Google Ads] および [!DNL Microsoft® Advertising] キャンペーンを検索ネットワーク上に配置します。 広告ネットワークは、一連の広告タイトルと説明から、テキストベースのレスポンシブ検索広告を動的に構築し、互いに良くパフォーマンスを発揮する組み合わせをお気に入りに組み込みます。 広告には、最大 3 つのヘッドライン、2 つの説明、およびベース URL からのカスタマイズ可能な URL と、オプションの path1 および path2 フィールドが含まれます。 オプションで、広告タイトルと説明を特定の位置に固定できます。

>[!NOTE]
>
>[!DNL Google Ads] 広告として表示されたテキストの組み合わせに関するデータをネイティブエディター以外で提供しない。 各テキストの組み合わせのレポートについて詳しくは、 [Google Ads ドキュメント](https://support.google.com/google-ads/answer/7684791).

## The [!UICONTROL Ads] 表示

広告のステータスは、 [!UICONTROL Campaigns] > [!UICONTROL Campaigns] > [!UICONTROL Ads] 表示。

## 広告レベルのパフォーマンスデータ

広告レベルのデータは、ほとんどの広告タイプで使用できます。

ただし、では使用できません。 [!DNL Google Ads] 動的検索広告 (DSA)、パフォーマンスの最大値、スマートショッピング、 [!DNL YouTube] キャンペーン。 キャンペーンの広告レベルの合計データとキャンペーンの合計データの間に相違が生じることを想定しています。

| 広告ネットワーク/キャンペーン/広告タイプ | データの可用性 |
|---|---|
| [!DNL Google Ads] 動的検索広告 (DSA) | キャンペーン、広告グループ |
| [!DNL Google Ads] 最大パフォーマンス | Campaign |
| [!DNL Google Ads] 買い物，スマートショッピング | キャンペーン、広告グループ |
| [!DNL Google Ads] [!DNL YouTube] | キャンペーン、広告グループ |

>[!MORELIKETHIS]
>
>* [広告の管理](ad-manage.md)
