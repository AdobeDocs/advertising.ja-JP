---
title: ' [!DNL Microsoft Advertising]  アカウントに必要なバルクシートデータ'
description: ' [!DNL Microsoft Advertising]  アカウントの必須ヘッダーフィールドとデータフィールドを一括シートで参照します。'
exl-id: 2a5f0e7b-f020-4cca-9b77-807c2ee5c273
feature: Search Bulksheets
TQID: https://experienceleague.adobe.com/sPku0vJW3srDbrbXy3CNjRIlgbTcRIQCU-F7yH8pr6E
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 7024
ht-degree: 0%

---

# 付録 – [!DNL Microsoft Advertising] アカウントに必要なバルクシート データ

[!DNL Microsoft Advertising]件のキャンペーンデータを一括で作成および更新するには、[!DNL Microsoft Advertising]件のアカウントに特化してフォーマットされたSearch、Social、およびCommerceのバルクシート ファイルを使用できます。 a） [&#128279;](../bulksheet-download.md)必要なファイル形式で既存のアカウントの一括シートファイルを生成するか、b）手動で作成できます（サポートされているファイル形式に関する一般的な情報については、「[&#x200B; サポートされている一括シートファイル形式](bulksheet-file-formats.md)」を参照）。

各バルクシートには、実行する[特定の操作（広告の作成など）に必要なヘッダーフィールドと対応するデータフィールドを含める必要があります。 &#x200B;](/help/search-social-commerce/campaign-management/bulksheets/bulksheet-data-formats/bulksheet-operations.md)フィールドが必須でない場合は、ヘッダー行とデータ行からフィールドを省略できます。 一括シートファイルをアップロードすると、すべてのカスタム列が削除されます。

次に、利用可能なすべてのデータフィールドの表と、個々のエンティティ（キャンペーンやキーワードなど）のデータを追加、編集、または削除するために必要なフィールドを示す追加の表を示します。

## 使用可能なすべてのデータフィールド {#bulksheet-fields-all-microsoft}

次の表に、使用可能なすべてのデータフィールドを示します。

アカウントエンティティに関連するデータフィールドについては、「[各アカウントコンポーネントの作成、編集、または削除に必要なフィールド &#x200B;](#bulksheet-fields-per-component-microsoft)」を参照してください。

| フィールド | 説明 |
|----|----|
| [!UICONTROL Platform] | （情報目的で生成されたバルクシートに含まれる）広告プラットフォーム。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Acct Name] | 広告ネットワークアカウントを識別する一意の名前。 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | アカウントのキャンペーンを識別する一意の名前。 最大長は128文字です。 |
| [!UICONTROL Campaign Budget] | 通貨記号や句読点の有無にかかわらず、1日または1か月のキャンペーン予算。 0.05以下ではいけません。 |
| [!UICONTROL Channel Type] | キャンペーンがターゲットとするチャネルのタイプ：<i>[!UICONTROL Audience]</i>、<i>[!UICONTROL DynamicSearchAds]</i>、<i>[!UICONTROL Search]</i>、または<i>[!UICONTROL Shopping]</i>。 |
| [!UICONTROL Delivery Method] | （日別予算を持つキャンペーンのみ）キャンペーンの広告を毎日表示する速度：<ul><li><i>[!UICONTROL Standard (Distributed)]</i> （新しいキャンペーンのデフォルト）：広告インプレッションを一日中広げます。</li><li><i>[!UICONTROL Accelerated]:</i>予算に達するまで、広告を可能な限り頻繁に表示します。 その結果、広告が後で表示されない場合があります。</li></ul> |
| [!UICONTROL Campaign Priority] | （ショッピングキャンペーンのみ）複数のキャンペーンが同じ製品を広告する際にキャンペーンが使用される優先度：<i>[!UICONTROL Low]</i> （新しいキャンペーンのデフォルト）、<i>[!UICONTROL Medium]</i>、または<i>[!UICONTROL High]</i>。<br><br>同じ製品が複数のキャンペーンに含まれている場合、広告ネットワークはキャンペーンの優先度を最初に使用して、どのキャンペーン（および関連する入札）が広告オークションの対象となるかを判断します。 すべてのキャンペーンの優先順位が同じ場合、入札額が最も高いキャンペーンが実施要件を満たします。 |
| [!UICONTROL Has EU Political Ads] | （欧州連合（EU）のオーディエンスをターゲットとするキャンペーンに適用されます） キャンペーンに、EU規則2024/90に基づいて欧州連合で提供される広告の要件に従った政治的広告が含まれているかどうか：<i>[!UICONTROL Yes]</i>または<i>[!UICONTROL No]</i>。 |
| [!UICONTROL Merchant ID] | （ショッピングキャンペーンとオーディエンスキャンペーンは加盟店フィードにリンクされている場合のみ）キャンペーンに使用される製品の加盟店アカウントの顧客ID。 |
| [!UICONTROL Sales Country] | （ショッピングキャンペーンのみ。既存のキャンペーンの読み取り専用）キャンペーンの製品が販売される国。 製品はターゲット国に関連付けられているため、この設定によって、キャンペーンで宣伝される製品が決まります。 |
| [!UICONTROL Product Scope Filter] | （ショッピングネットワークを使用したキャンペーンのみ）キャンペーンに対して商品広告を作成できる加盟店アカウント内の商品。 dimension=attribute形式を使用して、商品をフィルタリングする商品ディメンションと属性の組み合わせを最大7つ入力できます。 「>>」区切りで複数のフィルターを区切ります。 使用可能な製品ディメンションのリストについては、「[&#x200B; ショッピングキャンペーン製品フィルター](/help/search-social-commerce/campaign-management/campaigns/shopping-campaign-product-filters.md)」を参照してください。「<br><br>」 例：&quot;`CategoryL1==Animals & Pet Supplies>>CategoryL2=Pet Supplies>>Brand=Acme Pet Supplies`&quot;<br><br>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL DSA Domain Name] | （タイプ aのキャンペーン） 「<i>[!UICONTROL DynamicSearchAds]</i>」または「<i>[!UICONTROL Search]</i>」 （[!DNL ExperimentId]要素が設定されていない場合）動的検索広告のターゲットとなるweb サイトのドメイン名。 最大長は2,048文字です。 ドメイン名に`www`が含まれる場合、トリミングされ、使用されません。<br><br>既存のキャンペーンの場合、ドメインは編集できませんが、他のプロパティを更新するには、ドメインを含める必要があります。 |
| [!UICONTROL DSA Domain Language] | （タイプ aのキャンペーン）「<i>[!UICONTROL DynamicSearchAds]</i>」または「<i>[!UICONTROL Search]</i>」 （[!DNL ExperimentId]要素が設定されていない場合）動的検索広告のターゲットとなるweb サイトページの言語。 サポートされているドメイン言語は[!UICONTROL Dutch]、[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL German]、[!UICONTROL Italian]、[!UICONTROL Spanish]、および[!UICONTROL Swedish]です。<br><br>既存のキャンペーンの場合、言語を編集することはできませんが、他のプロパティを更新するには、言語を含める必要があります。 |
| [!UICONTROL Ad Group Name] | 広告グループを識別する一意の名前。 最大長は128文字です。 末尾の空白文字は保存されません（例えば、「広告グループ 1」は「広告グループ 1」として保存されます）。 |
| [!UICONTROL Ad Group Type] | （検索ネットワーク上のキャンペーン、既存の広告グループの読み取り専用）広告グループの種類：<i>[!UICONTROL Audience]</i> （オーディエンスキャンペーンのみ）、<i>[!UICONTROL Search Dynamic]</i> （動的検索広告のみ）、<i>[!UICONTROL Search Standard]</i> （レスポンシブ検索広告と既存の拡張テキスト広告のみ）。 一部のキャンペーンタイプには、複数の広告グループタイプを含めることができます。 |
| [!UICONTROL Keyword] | （検索ネットワーク上のキャンペーンのみ）キーワード文字列。 最大長は50文字です。<br><br><b> メモ：</b><ul><li>広告グループまたはキャンペーンレベルでキーワードを除外するには、[!UICONTROL Match Type]を`Negative`に設定します。 行に広告グループ名が含まれている場合、広告グループのキーワードは除外されます。 行に広告グループ名が含まれていない場合、キャンペーン全体でキーワードが除外されます。</li><li>[!DNL Microsoft Advertising] キーワードを変更すると、既存のキーワードが削除され、新しいキーワード IDを持つ新しいキーワードが作成されます。 ただし、一致タイプを変更しても、既存のキーワードは削除されません。</li></ul> |
| プレースメント | 非推奨 |
| [!UICONTROL Audience] | キャンペーンまたは広告グループの検索広告用リマーケティングリスト（RLSA）ターゲットオーディエンス。 |
| [!UICONTROL Target Type] | （RLSA ターゲットのみ）ターゲット タイプ：<i>[!UICONTROL Inclusion]</i>または<i>[!UICONTROL Exclusion]</i>。 |
| [!UICONTROL Auto Target Expression] | 広告グループの動的検索ターゲット： すべてのターゲットに対して、「[!UICONTROL All Web Pages]」を使用します。「<br><br>最大3つの動的検索条件をターゲットにするには、形式`<category>=<target>`を使用します。ここで、&lt;category>には、以下のカテゴリのいずれかを含めることができます。 個々のカテゴリの複数のターゲットを&quot;`[blank space] and [blank space]`&quot;で結合し、複数のカテゴリを&quot;`[blank space] and [blank space]`&quot;で結合します。<br><ul><li><i> カテゴリ：</i>特定のGoogle コンテンツカテゴリを持つインデックス付きページの動的検索広告を表示します。</li><li><i>URL:</i>特定のURLを持つインデックス付きページの動的検索広告を表示するには、URL内の任意の場所に値を含めることができます。</li><li><i> ページタイトル：</i> ページタイトルに特定のテキストを含むインデックス付きページの動的検索広告を表示します。</li><li><i> ページコンテンツ：</i>特定のコンテンツを含むインデックス付きページの動的検索広告を表示します。</li></ul>例：url=shoes.example.comおよびpage title=footwear<br>例：すべてのWeb ページ |
| [!UICONTROL Location] | キャンペーンまたは広告グループの広告を配置する地理的な場所。値は大文字と小文字を区別しません。 キャンペーンまたは広告グループに値を入力しない場合は、すべての場所がターゲットになります。 特定の場所をターゲットにするには、[!DNL Microsoft Advertising]の場所コード形式を使用して場所を入力します。 場所リストをダウンロードするには、[!DNL Microsoft Advertising]広告アカウントの資格情報を使用して[!DNL Microsoft Advertising]開発者ポータルにログインします。 <b> メモ：</b>場所を除外するには、場所コードの前に`-United States`などのマイナス記号（`-`）を付けます。 |
| [!UICONTROL Location Type] | 場所の種類（市区町村、国、メトロエリア、郵便番号、都道府県など）。 場所リストをダウンロードするには、[!DNL Microsoft Advertising]広告アカウントの資格情報を使用して[!DNL Microsoft Advertising]開発者ポータルにログインします。 |
| [!UICONTROL Match Type] | （検索ネットワーク上のキャンペーンのみ）キーワードマッチングオプション。 これには、動的検索ターゲットまたは商品グループのキーワードマッチングオプションが含まれる場合があります。 値には、<i>[!UICONTROL Broad]</i> （新しいキーワードのデフォルト）、<i>[!UICONTROL Exact]</i>、<i>[!UICONTROL Phrase]</i>、<i>[!UICONTROL Content]</i> （広告グループがコンテンツネットワークをターゲットにしている場合にキーワードに自動的に設定）、<i>[!UICONTROL Negative]</i> （コンテンツネットワーク上のキーワードを除外）、<i>[!UICONTROL Dynamic Ad Target]</i> （新しい動的検索目標のデフォルト）、<i>[!UICONTROL Product Group]</i> （新しい製品グループのデフォルト）、または<i>[!UICONTROL Negative Product Group]</i> （製品グループを除外）が含まれます。  複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード IDの値が必要です。<br><br>Broad Match Modifierの場合、「Broad」を選択し、必要なキーワード内の任意の単語（「red」と「shoes」の両方を必要とする「`+red +shoes`」など）の前に`+`を挿入します。<br><br> [!DNL Microsoft Advertising] キーワードの一致タイプを変更しても、既存のキーワードは削除されません。 |
| [!UICONTROL Max CPC] | （検索ネットワークでのキャンペーン）クリック単価（CPC）。キーワード、商品グループ、動的な検索対象に基づいて、広告クリックに対して支払う最大の金額で、金銭的な記号と句読点の有無にかかわらず使用されます。  最適化されたポートフォリオ内の既存のキーワードおよび製品グループ レコードの場合、更新は1日のみ有効で、次の最適化サイクル中に上書きされます。 <b>注：</b>否定的なキーワードに入札を設定することはできません。 |
| [!UICONTROL Max Content CPC] | （2017年に廃止されたコンテンツネットワークより前に作成されたCPC キャンペーンの場合のみ）表示用ネットワークサイトからの広告クリックに対して支払う最大クリック単価（CPC）で、金銭的な記号と句読点の有無に関わらず発生します。 |
| [!UICONTROL Audience Target Method] | （オーディエンス広告グループ）次のかどうか：<ul><li><i>[!UICONTROL Target and Bid]:</i>広告グループの他のターゲットも満たすターゲットオーディエンスに関連付けられたユーザーにのみ広告を表示します。</li><li><i>[!UICONTROL Bid Only]:</i>他の広告グループレベルのターゲットを満たしている限り、ターゲットオーディエンスに関連付けられていないユーザーにも広告を表示します。</li></ul> ただし、特定のオーディエンスに対して高い入札額を設定することで、広告が表示される可能性を高めることができます。 |
| [!UICONTROL Parent Product Groupings] | 任意の親製品グループの階層。<br><br>例：`All Products>>ProductTypeL1=a>>ProductTypeL2=b` |
| [!UICONTROL Product Grouping] | 製品グループ （「brand=acme」または「すべての製品」など）。<br><br><b> メモ：</b><ul><li>指定したプロダクトグループが親プロダクトグループ階層に存在しない場合、Search, Social, &amp; Commerceは、階層の必要な部分を作成します。</li><li>Search, Social, &amp; Commerceでは、ショッピング キャンペーンで広告グループを作成する際に、デフォルトの入札額が広告グループのデフォルト入札額に設定されている場合は、必ず「[!UICONTROL All Products]」グループが自動的に作成されます。 Search, Social, &amp; Commerceは、商品グループ階層の各レベルで広告グループのデフォルト入札額を使用して、「[!UICONTROL Everything Else]」グループを自動的に作成します。 これらのデフォルトグループを明示的に作成し、それらを除外するか、入札を変更することができます。</li><li>各広告グループには、「[!UICONTROL All Products]」やその他7つの階層を含め、最大8つの階層の製品グループを含めることができます。</li></ul> |
| [!UICONTROL Partition Type] | 製品グループのパーティション タイプ：<i>[!UICONTROL subdivision]</i> （子製品グループがある場合）または<i>[!UICONTROL unit]</i> （子製品グループがない場合）。 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | （拡張テキスト広告、マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告のみ）広告の見出し。 各広告タイトルフィールドの最大長は、動的テキスト（キーワードの値、`{Param2}`および`{Param3}`動的な置換変数、広告カスタマイズなど）を含む30文字または15 ダブルバイト文字です。<br><br> レスポンシブ検索広告の場合は、次の形式を使用して広告カスタマイズ機能を挿入します。ここで、「デフォルトテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。`{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br>拡張テキスト広告の場合、広告タイトルと広告タイトル 2が必要で、[!UICONTROL Ad Title 3]はオプションです。 2022年8月に[!DNL Microsoft Advertising]件の非推奨の拡張テキスト広告を使用し、レポートと削除のみを行えるようになりました。<br><br> マルチメディア広告、レスポンシブ広告、およびレスポンシブ検索広告の場合、[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]、[!UICONTROL Ad Title 3]は必須であり、その他のすべての広告タイトルフィールドはオプションです。<br><br>必須でないフィールドの既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。<br><br>拡張テキスト広告を除くすべての広告タイプについて、広告コピーを変更すると、既存の広告が削除され、同じプロパティを持つ新しい広告が作成されます。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | （レスポンシブ検索広告のみ。オプション）対応する広告タイトルをピン留めする位置：`[null]` （値なし、すべてのポジションに対して広告タイトルを有効にします）、1、2、または3。 例えば、[!UICONTROL Ad Title Position]の値が1の場合、[!UICONTROL Ad Title]は位置1にのみ表示できます。 デフォルトでは、すべての広告タイトルはnullです（値はありません）。 既存の値を削除するには、値`[delete]` （角括弧を含む）を使用します。<br><br><b>注意：</b>複数の広告タイトルを同じ位置に固定できます。 広告ネットワークは、位置にピン留めされた広告タイトルの1つを使用します。 3番目にピン留めされたタイトルは、広告で表示されない場合があります。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | （テキスト広告、動的検索広告、マルチメディア広告、レスポンシブ広告、レスポンシブ検索広告、および強化されたキャンペーンレベルのサイトリンクのみ）広告またはサイトリンクの本文。<br><br> サイトリンクの場合、オプションで[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]の両方を使用して、広告ネットワークがリンクテキストの下に表示できる追加テキストを含めます。 各説明フィールドには、最大35個の1 バイト文字または17個の2 バイト文字を含めることができます。<br><br>広告の場合、各説明フィールドの最大長は、動的テキスト（キーワードや広告カスタマイズの値など）を含む90文字または45文字の2 バイト文字です。<br><br> レスポンシブ検索広告の場合は、次の形式を使用して広告カスタマイザーを挿入します。`{CUSTOMIZER.Attribute name:Default text}, such as {CUSTOMIZER.Discount:10%}`<br><br> テキスト広告と動的検索広告の場合、説明行1が必須で、[!UICONTROL Description Line 2]は任意です。<br><br> マルチメディア広告、レスポンシブ広告、およびレスポンシブ検索広告の場合、[!UICONTROL Description Line 1]および[!UICONTROL Description Line 2]は必須で、[!UICONTROL Description Line 3]および[!UICONTROL Description Line 4]はオプションです。<br><br>既存の値を削除するには、値`[delete]` （角括弧を含む）を使用します。<br><br><b> メモ：</b><ul><li>（標準テキスト広告）タイトルとテキストの組み合わせは、少なくとも3単語にする必要があります。</li><li>（拡張テキスト広告）このフィールドには、オプションで{Param2}および{Param3}動的置換変数を含めることができます。 有効な場合、広告テキストの最大長は300 シングルバイトまたは150 ダブルバイト文字です。 2022年8月に[!DNL Microsoft Advertising]件の非推奨の拡張テキスト広告を使用し、レポートと削除のみを行えるようになりました。</li><li>（動的検索広告）動的置換テキストは使用できません。</li><li>拡張テキスト広告を除くすべての広告タイプについて、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。</li></ul> |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | （レスポンシブ検索広告のみ。オプション）対応する説明をピン留めする位置：`[null]` （値なし、すべての位置に対して説明を有効にします）、1、2、または3。 例えば、[!UICONTROL Description 1 Position]の値が1の場合、説明1は位置1にのみ表示されます。 デフォルトでは、説明は位置に固定されません。<br><br>既存の値を削除するには、値`[delete]` （角括弧を含む）を使用します。<br><br><b>注意：</b>複数の説明を同じ位置に固定できます。 広告ネットワークは、位置にピン留めされた説明の1つを使用します。 位置2にピン留めされた説明は、広告で表示されない場合があります。 |
| [!UICONTROL Business Name] | （マルチメディア広告のみ）ビジネス名（最大25文字）。 |
| [!UICONTROL Promotion Line] | （商品リスト広告のみ）検索結果に商品リストに含まれる独自のプロモーションライン（「今すぐ送料無料！」など）。 最大長は45文字です。<br><br> プロモーション行は、広告がページ上のどこに表示されるかに応じて、広告とは異なる場所（広告の下など）に表示される場合があります。 |
| [!UICONTROL Display URL] | 広告に含まれるURL。<br><br>拡張された動的検索広告の場合、広告ネットワークはこの値をweb サイト ドメインから動的に生成するため、値を入力する必要はありません。<br><br>拡張テキスト広告とレスポンシブ検索広告の場合、値を入力する必要はありません。 表示URLは、最終的なURLのドメインから自動的に抽出されます。 オプションで、「パス 1」フィールドと「パス 2」フィールドを使用してURLをカスタマイズできます。<br><br><b> メモ：</b><ul><li>（最終URLを持つアカウント）表示URLと最終URLのドメイン名は一致する必要があります。</li><li>2022年8月に[!DNL Microsoft Advertising]件の非推奨の拡張テキスト広告を使用し、レポートと削除のみを行えるようになりました。</li></ul> |
| [!UICONTROL Display Path 1] | （拡張テキスト広告、動的検索広告、レスポンシブ検索広告のみ）最終的なURLから自動的に抽出された表示URLに追加されたテキスト。 各パスの前には、URL内の先頭にスラッシュ（/）が付きます。 パスにスラッシュ （/）または改行（\n）を含めることはできません。 各パスの最大長は15文字または7つの2 バイト文字です。<br><br>広告カスタマイザーを挿入するには、次の形式を使用します。ここで、「デフォルトテキスト」は、フィードファイルに有効な値が含まれていない場合に挿入するオプションの値です。`{CUSTOMIZER.Attribute name:Default text}`、例：`{CUSTOMIZER.Discount:10%}`<br><br>例：[!UICONTROL Display Path 1]が「deals」の場合、表示URLは&lt;display URL>/deals （例：www.example.com/deals<br><br>[!DNL Microsoft Advertising]）。 2022年8月に非推奨となった拡張テキスト広告で、レポートと削除のみを行えるようになりました。 |
| [!UICONTROL Display Path 1] | （拡張テキスト広告、動的検索広告、およびレスポンシブ検索広告のみ）追加の表示パス。詳しくは、[!UICONTROL Display Path 1]のエントリを参照してください。<br><br>例：[!UICONTROL Display Path 1]が「deals」で、[!UICONTROL Display Path 2]が「local」の場合、表示URLは&lt;<i>display URL</i>>/deals/localになります（例：www.example.com/deals/local）。 |
| [!UICONTROL Start Date] | （拡張サイトリンクのみ）広告主のタイムゾーンで、次のいずれかの形式で、サイトリンクに入札を配置できる最初の日付（m/d/yyyy、m/d/yy、m-d-yyyy、m-d-yy）。 新しい拡張サイトリンクのデフォルトは現在の日付です。 <b>注意：</b>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーン内でのみ作成できます。または、サイトリンクは作成できません。 |
| [!UICONTROL End Date] | 広告主のタイムゾーンで、m/d/yyyy、m/d/yy、m-d-yyyy、またはm-d-yyのいずれかの形式で、サイトリンクが広告とともに表示される最後の日付。 新しいサイトリンクの場合、デフォルトは`[blank]` （つまり、終了日なし）です。 |
| [!UICONTROL Call To Action] | Call to actionを広告に掲載します。 考えられる値のリストについては、[API リファレンスを参照してください](https://learn.microsoft.com/en-us/advertising/campaign-management-service/calltoaction)。ただし、複数の単語のCTAを複数の単語（「BetNow」ではなく「BetNow」など）として一括シートに入力します。 |
| [!UICONTROL Call To Action Language] | Call to action オプションの言語。 使用可能な言語のリストについては、[API リファレンスを参照してください](https://learn.microsoft.com/en-us/advertising/campaign-management-service/languagename)。 |
| [!UICONTROL Base URL/Final URL] | 検索エンジンユーザーが広告をクリックしたときに取得されるランディングページのURL （キャンペーンまたはアカウントに設定された追加パラメーターを含む）。 キーワードレベルのベース/最終URLは、広告レベル以上のURLを上書きします。<br><br>既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Destination URL] | （情報目的で生成されたバルクシートに含まれ、検索エンジンには投稿されません）宛先URLを持つアカウントの場合、これは、広告を広告主のweb サイト上のベース URL/ランディングページにリンクするURLです（クリックを追跡し、ユーザーをランディングページにリダイレクトする別のサイトを介して送信する場合もあります）。 これには、検索、ソーシャル、Commerceのキャンペーンまたはアカウント用に設定された追加パラメーターが含まれます。 トラッキング URLを生成した場合、これは、アカウント設定とキャンペーン設定のトラッキングパラメーターに基づきます。 検索エンジン固有のパラメーターを追加した場合は、検索、ソーシャル、Commerceの同等のパラメーターに置き換えることができます。<br><br>最終URLを持つアカウントの場合、この列には基本URL/最終URL列と同じ値が表示されます。 |
| [!UICONTROL Custom URL Param] | 検索アカウントまたはキャンペーン設定のトラッキングパラメーターに変数が含まれている場合に、`{custom_code}`動的変数の代わりにデータを使用します。 トラッキング URLにカスタム値を挿入するには、「トラッキング URLを生成」オプションを使用してバルクシート ファイルをアップロードする必要があります。 |
| [!UICONTROL Creative Type] | 広告の形式：<i>[!UICONTROL Dynamic Search Ad]</i>、<i>[!UICONTROL Expanded Text Ad]</i>、<i>[!UICONTROL Expanded Dynamic Search Ad]</i>、<i>[!UICONTROL Multimedia Ad]</i>、<i>[!UICONTROL Product Ad]</i> （ショッピング広告）、または<i>[!UICONTROL Responsive Search Ad]</i>、または<i>[!UICONTROL Text ad]</i>。 新規広告のデフォルトは<i>[!UICONTROL Text ad]</i>です。 |
| [!UICONTROL Ad Group Start Date] | 広告グループの入札が最初に行われる日付。広告主のタイムゾーンで、m/d/yyyy、m/d/yy、m-d-yyyy、またはm-d-yyのいずれかの形式で行われます。 新しい広告グループの場合、デフォルトは現在の日付です。 |
| [!UICONTROL Ad Group End Date] | 広告主のタイムゾーンで、広告グループに入札を行うことができる最後の日付。m/d/yyyy、m/d/yy、m-d-yyyy、またはm-d-yyのいずれかの形式です。 新しい広告グループの場合、デフォルトは[blank]です（つまり、終了日はありません）。 |
| [!UICONTROL Tracking Template] | （オプション）すべてのオフランディングドメインのリダイレクトとトラッキングパラメーターを指定し、最終的なURLをパラメーターに埋め込むトラッキングテンプレート。 最も詳細なレベル（キーワードが最も詳細）のトラッキングテンプレートは、より高いレベルのすべての値を上書きします。<br><br> キャンペーン設定に「[!UICONTROL EF Redirect]」と「[!UICONTROL Auto Upload]」が含まれている場合に適用されるAdobe Advertising コンバージョントラッキングの場合、レコードを保存すると、Search, Social, &amp; Commerceはリダイレクトコードとトラッキングコードを自動的に追加します。<br><br> サードパーティのリダイレクトとトラッキングの場合は、値を入力します。<br><br> トラッキングテンプレートの最終的なURLを示すパラメーターのリストについては、[!DNL Microsoft Advertising] ドキュメントを参照してください。<br><br> 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Landing Page Suffix] | 最後のURLの末尾に追加するパラメーターを指定して、情報を追跡します。 例：`param2=value1&param3=value2`<br><br>詳しくは、 [!DNL Microsoft Advertising][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-microsoft.md)の「 クリックトラッキング形式」を参照してください。「<br><br>下位レベルの最終URL サフィックスは、アカウントレベルのサフィックスを上書きします。 メンテナンスを容易にするために、個々のアカウントコンポーネントに対して異なるトラッキングが必要でない限り、アカウントレベルのサフィックスのみを使用します。 広告グループレベル以下でサフィックスを設定するには、[!DNL Microsoft Advertising] エディターを使用します。 |
| 検索ネットワークステータス | 検索ネットワークの様々な要素に広告グループの広告を配置するかどうか：<ul><li><i>すべて：</i>すべてのBing検索ネットワークと同時検索パートナーに広告を配置します。</li><li><i>OwnedAndOperatedOnly:</i>BingとYahoo！にのみ広告を掲載するには web サイト：</li><li><i>SyndicatedSearchOnly:</i> BingとYahoo！にのみ広告を掲載する 同時検索パートナー：</li><li><i> オフ：</i> コンテンツ ネットワークにのみ広告を配置するには（検索ネットワークではなく）。</li></ul> 新しい広告グループの場合、デフォルトはオンです。 |
| [!UICONTROL Content Network Status] | 非推奨 |
| [!UICONTROL Languages] | 広告グループの広告のターゲット言語：[!UICONTROL English]、[!UICONTROL French]、[!UICONTROL Finnish]、[!UICONTROL German]、[!UICONTROL Norwegian]、[!UICONTROL Spanish]、または[!UICONTROL Swedish]。 新しいキャンペーンのデフォルトは[!UICONTROL English]です。<br><br>この設定により、広告を表示できる国と地域が決まります。 キャンペーンの位置情報ターゲットに対応した言語を選ぶようにしましょう。 |
| [!UICONTROL Budget Type] | 予算が<i>[!UICONTROL Daily]</i> （デフォルト）か<i>[!UICONTROL Monthly]</i>かのどちらかです。<br><br>注意：キャンペーンを最適化されたポートフォリオに割り当てると、この値は自動的に[!UICONTROL Daily]に設定されます。 |
| [!UICONTROL Device] | キャンペーンまたは広告グループレベルで入札調整が行われるデバイスタイプ：<i>[!UICONTROL smartphone]</i>、<i>[!UICONTROL tablet]</i>、または<i>[!UICONTROL desktop]</i>。 |
| [!UICONTROL Bid Adjustment] | 指定したターゲットタイプの入札調整。 例えば、キーワードレベルの入札が1米ドルで、スマートフォンの入札調整が50%の場合、スマートフォンの入札は1.50米ドルになります。 デフォルトでは、すべてのターゲットはキーワードレベルの入札で入札されます。 有効なパーセンテージには、次のものが含まれます。<ul><li>スマートフォンとタブレット：-100 （デバイスタイプに入札しない場合）、-90～900</li><li>デスクトップ：0 ～ 900</li></ul> |
| [!UICONTROL Creative Preferred Devices] | 広告またはサイトリンクを表示するデバイスの種類：<i>[!UICONTROL All]</i> （デフォルト）または<i>[!UICONTROL Mobile]</i>。 Mobileを指定すると、ネットワークはデスクトップやタブレットユーザーではなく、モバイルデバイスユーザーに広告やサイトリンクを表示しようとします。 それ以外の場合、ネットワークは任意のデバイスタイプに広告またはサイトリンクを表示します。 <b>注意：</b> ネットワークは、好みのデバイスタイプで広告が表示されることを保証するものではありません。 |
| [!UICONTROL Param2] | キーワードのベース URLまたは広告のタイトル、説明、ベース URLに`{Param2}`動的な置換文字列が含まれている場合に、置換値として使用する文字列。 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Param3] | キーワードのベース URLまたは広告のタイトル、説明、ベース URLに`{Param3}`動的な置換文字列が含まれている場合に、置換値として使用する文字列。 最大長は70文字ですが、使用する広告要素の最大長に注意してください（例えば、タイトル 1とタイトル 2の組み合わせは最大76文字です）。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Link Name] | サイトリンクのテキスト： キャンペーン内で一意である必要があります。 Description1とDescription2を指定した場合、サイトリンク テキストには最大25個の1 バイト文字または12個の2 バイト文字を含めることができます。それ以外の場合、サイトリンク テキストには最大35個の1 バイト文字または17個の2 バイト文字を含めることができます。<br><br>[!DNL Microsoft Advertising] 2つ、4つ、または6つの強化サイトリンクを説明とともに表示したり、1行に4つ、6つのサイトリンクを説明なしで表示したり、広告を表示したりできます。<br><br>新しい拡張サイトリンクは、既存の拡張サイトリンクを含むキャンペーン内でのみ作成できます。また、サイトリンクを含めることはできません。 |
| [!UICONTROL Campaign Status] | キャンペーンの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキャンペーンのみ）。 新規キャンペーンのデフォルトは[!UICONTROL Active]です。 アクティブまたは一時停止したキャンペーンを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Ad Group Status] | 広告グループの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存の広告グループのみ）。 新規広告グループのデフォルトは[!UICONTROL Active]です。 アクティブな広告グループまたは一時停止した広告グループを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Keyword Status] | キーワードの表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のキーワードのみ）。 新しいキーワードのデフォルトは[!UICONTROL Active]です。 アクティブ キーワードまたは一時停止キーワードを削除するには、値`Deleted`を入力します。 <b>注意：</b>複数の一致タイプを持つキーワードのトラッキング URLを作成する場合、各一致タイプのキーワードステータスは同じである必要があります。 |
| [!UICONTROL Placement Status] | 非推奨 |
| [!UICONTROL Ad Status] | 広告の表示ステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Deleted]</i> （既存の広告のみ）、<i>[!UICONTROL Disapproved]</i> （編集不可）、または<i>[!UICONTROL Paused]</i>。 新規広告のデフォルトは[!UICONTROL Active]です。 アクティブな広告または一時停止した広告を削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Target Status] | 動的検索ターゲットのステータス：<i>[!UICONTROL Active]</i>、<i>[!UICONTROL Paused]</i>または<i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新規ターゲットのデフォルトは[!UICONTROL Active]です。 アクティブまたは一時停止したターゲットを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Sitelink Status] | サイトリンクの表示ステータス：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i> （既存のサイトリンクのみ）。 新しいサイトリンクのデフォルトは[!UICONTROL Active]です。 アクティブなサイトリンクを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Location Status] | 場所ターゲットの状態：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i> （既存の場所のみ）。 新しい場所のデフォルトは[!UICONTROL Active]です。 アクティブな場所を削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Product Group Status] | 製品グループの表示ステータス：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i> （既存の製品グループのみ）。 新しい製品グループのデフォルトは[!UICONTROL Active]です。 アクティブな製品グループを削除するには、値`Deleted`を入力します。 |
| [!UICONTROL Device Target Status] | キャンペーン レベルまたは広告グループ レベルのデバイス ターゲットの状態：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i>。 新しいキャンペーンと広告グループの場合、デフォルトは[!UICONTROL Active]です。 |
| [!UICONTROL RLSA Target Status] | キャンペーンまたは広告グループレベルのRLSA ターゲットまたは（Google Adsのみ）除外のステータス：<i>[!UICONTROL Active]</i>または<i>[!UICONTROL Deleted]</i> （既存のターゲットのみ）。 新しいターゲットまたは除外のデフォルトは[!UICONTROL Active]です。 アクティブなターゲットまたは除外を削除するには、値`Deleted`を入力します。 |
| \[広告主固有ラベル分類\] | （広告主固有のラベル分類の名前。例えば、「カラー」というラベル分類の「カラー」など）エンティティに関連付けられている指定された分類の値。 エンティティごとに分類ごとに1つの値のみを含めることができます（キャンペーン Aの「カラー」ラベル分類の「赤」など）。 最大長は100文字で、値にはASCII文字と非ASCII文字を含めることができます。<br><br> ラベル分類とそのラベル値は、すべての子コンポーネントに適用されます。後で追加される新しいコンポーネントは、ラベルに自動的に関連付けられます。 製品グループのラベル分類は、単位（最も詳細）レベルに適用されます。<br><br>分類名も分類値も大文字と小文字を区別しません。 |
| [!UICONTROL Constraints] | エンティティに割り当てられた制約。 エンティティごとに1つの制約のみを割り当てることができます。<br><b>>制約は子エンティティによって継承されるため、継承された値を上書きしない限り、子エンティティの値を入力する必要はありません。 |
| [!UICONTROL Campaign ID] | 既存のキャンペーンを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1] キャンペーン名を変更する場合にのみ必要です。行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り、この行は必須です。 |
| [!UICONTROL Ad Group ID] | 既存の広告グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1]広告グループの「[!UICONTROL AMO ID]」が行に含まれていない限り、キャンペーン名を変更する場合にのみ必要です。 |
| [!UICONTROL Placement ID] | 非推奨 |
| [!UICONTROL Keyword ID] | 既存のキーワードを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1]行にキーワードを識別するのに十分なプロパティ列（a）またはb）「2&rbrace;」が含まれていない限り、キーワードを変更する場合にのみ必要です。」[!UICONTROL AMO ID] |
| [!UICONTROL Ad ID] | <p>既存の広告を識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1] レスポンシブ検索広告の場合、広告データを編集または削除するには、広告IDまたはAMO IDが必要です。 その他のすべてのエンティティタイプでは、行に広告を識別するのに十分な広告プロパティ列（a）またはb）「[!UICONTROL AMO ID]」が含まれていない限り、AMO IDは広告ステータスを変更する場合にのみ必要です。」 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。</p><p><b>注意：</b>既存の広告のステータスを除くa）広告プロパティ列またはb）レスポンシブ検索広告のデータを編集し、[!UICONTROL Ad ID]または[!UICONTROL AMO ID]のいずれも含まない場合、新しい広告が作成され、既存の広告は変更されません。 </p> |
| [!UICONTROL Sitelink ID] | 既存のサイトリンクを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1]行にサイトリンクを識別するのに十分なプロパティ列がa）またはb） an &quot;[!UICONTROL AMO ID]&quot;が含まれていない限り、サイトリンクを変更または削除する場合にのみ必要です。 ただし、[!UICONTROL Sitelink ID]と[!UICONTROL AMO ID]のどちらも含めず、プロパティ列が複数のサイトリンクに一致する場合、サイトリンクの1つのみのステータスが変更されます。</p><p><b>注意：</b>既存のサイトリンクのステータス以外のサイトリンクプロパティ列を編集し、[!UICONTROL Sitelink ID]と[!UICONTROL AMO ID]のどちらも含まない場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL Product Group ID] | 既存の製品グループを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1]製品グループを変更または削除する場合にのみ必要です。行に製品グループを識別するのに十分なプロパティ列が含まれていない限り、または行に「[!UICONTROL AMO ID]」。 |
| 場所ID | 場所ターゲットの一意の[!DNL Microsoft Advertising]識別子。 場所リストをダウンロードするには、[!DNL Microsoft Advertising]広告アカウントの資格情報を使用して[!DNL Microsoft Advertising]開発者ポータルにログインします。 場所のターゲットを変更または削除する場合にのみ必須です。行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL Target ID] | 既存の自動ターゲットを識別する一意のID。 自動ターゲットを変更または削除する場合にのみ必須です。ただし、行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL RLSA Target ID] | 既存のキャンペーンレベルまたは広告グループレベルのRLSA ターゲットを識別する一意のID。 CSV ファイルおよびTSV ファイルでは、先頭に引用符（&#39;）を付ける必要があります。[^1] ターゲットまたは除外を変更または削除する場合にのみ必要です。ただし、行にターゲットの「[!UICONTROL AMO ID]」が含まれていない場合は例外です。 |
| [!UICONTROL AMO ID] | （生成されたバルクシート内）同期されたエンティティに対してAdobeが生成した一意のID。 レスポンシブ検索広告の場合、広告IDを含めない限り、AMO IDは広告の編集または削除に必要です。 AMO IDを持つ他のすべてのエンティティの種類のデータを編集するには、エンティティ IDと親エンティティ IDを含まない限り、AMO IDがデータの編集または削除を行う必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDをアドネットワークに投稿しません。 |
| [!UICONTROL EF Error Message] | （情報目的で生成されたバルクシートに含まれる）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL EF Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL SE Error Message] | （情報目的で生成されたバルクシートに含まれる）行のデータに関する広告ネットワークからのエラーメッセージを表示するためのプレースホルダー。エラーメッセージは[!UICONTROL SE Errors] ファイルに含まれます。 この値は広告ネットワークに投稿されません。 |
| [!UICONTROL Exemption Request] | （情報目的で生成されたバルクシートに含まれる）広告が違反するGoogle広告ポリシーの名前とテキストを表示するためのプレースホルダー。 |
| [!UICONTROL Retail Hash] | （高度なキャンペーン管理を使用して生成されたバルクシートに情報目的で含まれます）高度な（ACM）ビューを使用して生成されたことを示す英数字のハッシュコード（f9639f40cdf56524b541e5dacf55a991など）。 |

[^1]: [!DNL Excel]は、ファイルを開いたときに、大きな数値を科学表記法（2115585666の場合は2.12E+09など）に変換します。 標準表記法で数値を表示するには、列内の任意のセルを選択し、数式バー内をクリックします。

## 各アカウントコンポーネントの作成、編集、削除に必要なフィールド {#bulksheet-fields-per-component-microsoft}

以下のセクションには、特定のアカウントエンティティに関連するフィールドが含まれます。

>[!NOTE]
>
>フィールドがアクションに適用されない場合、フィールドに入力された値は無視されます。

### キャンペーンフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須。 |
| [!UICONTROL Campaign Budget] | キャンペーンの作成に必要です。 |
| [!UICONTROL Channel Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Delivery Method] | オプション |
| [!UICONTROL Campaign Priority] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Has EU Political Ads] | キャンペーンの作成に必要です。 |
| [!UICONTROL Merchant ID] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Sales Country] | ショッピングキャンペーンの作成が必要です。 |
| [!UICONTROL Product Scope Filter] | （ショッピングキャンペーン）オプション |
| [!UICONTROL DSA Domain Name] | [!DNL ExperimentId]要素が設定されていない場合、タイプ a）「[!UICONTROL DynamicSearchAds]」またはタイプ b）「[!UICONTROL Search]」のキャンペーンを作成する必要があります） |
| [!UICONTROL DSA Domain Language] | [!DNL ExperimentId]要素が設定されていない場合、タイプ a）「[!UICONTROL DynamicSearchAds]」またはタイプ b）「[!UICONTROL Search]」のキャンペーンを作成する必要があります） |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Landing Page Suffix] | <p>オプション |
| [!UICONTROL Budget Type] | キャンペーンの作成に必要です。 |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Campaign Status] | キャンペーンを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | キャンペーン名を変更する場合にのみ必須です。行にキャンペーンの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### 広告グループフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Group Type] | 広告グループの作成に必要です。 |
| [!UICONTROL Audience Target Method] | オーディエンス広告グループの作成にのみ必要です。 |
| [!UICONTROL Ad Group Start Date] | オプション |
| [!UICONTROL Ad Group End Date] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Search Network Status] | （検索ネットワーク上のキャンペーンのみ）オプション |
| [!UICONTROL Languages] | オプション |
| [!UICONTROL Device] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Status] | 広告グループを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Ad Group ID] | 広告グループ名を変更する場合にのみ必要です。行に広告グループの「[!UICONTROL AMO ID]」が含まれていない限り除きます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### キーワードフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Keyword] | 必須 |
| [!UICONTROL Match Type] | 複数の一致タイプを持つキーワードを編集または削除するには、一致タイプまたはキーワード IDの値が必要です。 |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Param1] | オプション |
| [!UICONTROL Param2] | オプション |
| [!UICONTROL Keyword Status] | キーワードを削除する場合にのみ必須です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Keyword ID] | キーワードを編集または削除する場合にのみ必要です。ただし、行にa）キーワードを識別するのに十分なプロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれている場合を除きます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### 動的検索広告フィールド

>[!NOTE]
>
>作成サポートは利用できません。

この広告タイプでは、[!UICONTROL Download Bulksheet] ダイアログの「[!UICONTROL Creative (except RSA)]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 説明を編集するために必要です。 <b> メモ：</b>この広告タイプでは、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Display Path 1] | フィールドを編集するために必須です。 |
| [!UICONTROL Display Path 2] | フィールドを編集するために必須です。 |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告のステータスを変更する場合にのみ必要です。行にa&amp;rpar；広告またはb&amp;rparを識別するのに十分な広告プロパティ列、「[!UICONTROL AMO ID]」が含まれていない限り除きます。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### 商品（ショッピング）広告フィールド

ショッピング広告の作成について詳しくは、「[実装 [!DNL Microsoft Advertising]  ショッピングキャンペーン &#x200B;](https://experienceleague.adobe.com/docs/advertising/search-social-commerce/campaign-management/management/special-workflows/microsoft-shopping-campaigns.html?lang=ja)」を参照してください。

この広告タイプでは、[!UICONTROL Download Bulksheet] ダイアログの「[!UICONTROL Creative (except RSA)]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Promotion Line] | オプション |
| [!UICONTROL Base URL/Final URL] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | 製品広告のステータスを作成または編集するために必要です。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告のステータスを変更する場合にのみ必要です。行にa）広告を識別するのに十分な広告プロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### レスポンシブ（マルチメディア）広告フィールド

この広告タイプでは、[!UICONTROL Download Bulksheet] ダイアログの「[!UICONTROL Creative (except RSA)]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ広告の場合、広告を作成するには[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]および[!UICONTROL Ad Title 3]が必要であり、その他のすべての広告タイトルフィールドはオプションです。 必須ではないフィールドの既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 <b> メモ：</b>この広告タイプでは、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | 広告を作成するには[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]が必要で、[!UICONTROL Description Line 3]と[!UICONTROL Description Line 4]はオプションです。 <b> メモ：</b>この広告タイプでは、広告コピーを変更すると、既存の広告が削除され、新しい広告が作成されます。 |
| [!UICONTROL Business Name] | 広告の作成または削除に必要です。 |
| [!UICONTROL Call To Action] | 広告の作成が必要です。 |
| [!UICONTROL Call To Action Language] | 広告の作成が必要です。 |
| [!UICONTROL Base URL/Final URL] | 広告の作成が必要です。 |
| [!UICONTROL Creative Type] | オプション。 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 広告のステータスを変更する場合にのみ必要です。行にa）広告を識別するのに十分な広告プロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 ただし、[!UICONTROL Ad ID]と[!UICONTROL AMO ID]のどちらも含めず、広告プロパティ列が複数の広告に一致する場合、広告の1つのみのステータスが変更されます。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### レスポンシブ検索広告のフィールド

この広告タイプでは、[!UICONTROL Download Bulksheet] ダイアログの「[!UICONTROL Responsive Search Ad]」行を使用します。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 15] | レスポンシブ検索広告の場合、広告を作成するには[!UICONTROL Ad Title]、[!UICONTROL Ad Title 2]および[!UICONTROL Ad Title 3]が必要であり、その他のすべての広告タイトルフィールドはオプションです。 必須ではないフィールドの既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Ad Title 1 Position]-[!UICONTROL Ad Title 15 Position] | オプション |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 4] | レスポンシブ検索広告の場合、広告を作成するには[!UICONTROL Description Line 1]と[!UICONTROL Description Line 2]が必要であり、[!UICONTROL Description Line 3]と[!UICONTROL Description Line 4]はオプションです。 既存の値を削除するには、値`[delete]` （括弧を含む）を使用します。 |
| [!UICONTROL Description Line 1 Position]-[!UICONTROL Description Line 4 Position] | オプション |
| [!UICONTROL Display Path 1] | オプション |
| [!UICONTROL Display Path 2] | オプション |
| [!UICONTROL Base URL/Final URL] | 広告の作成が必要です。 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Ad Status] | 広告の削除が必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない限り、広告を編集または削除する必要があります。 |
| [!UICONTROL AMO ID] | 広告IDを含まない限り、広告の編集または削除が必要です。 |

### テキスト広告フィールド

この広告タイプでは、[!UICONTROL Download Bulksheet] ダイアログの「[!UICONTROL Creative (except RSA)]」行を使用します。

>[!NOTE]
>
>拡張テキスト広告は非推奨（廃止予定）になりました。 既存のテキスト広告のみを削除できます。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Ad Title], [!UICONTROL Ad Title 2]-[!UICONTROL Ad Title 3] | 読み取り専用 |
| [!UICONTROL Description Line 1]-[!UICONTROL Description Line 2] | 読み取り専用 |
| [!UICONTROL Display URL] | 読み取り専用 |
| [!UICONTROL Display Path 1] | 読み取り専用 |
| [!UICONTROL Display Path 2] | 読み取り専用 |
| [!UICONTROL Base URL/Final URL] | 読み取り専用 |
| [!UICONTROL Custom URL Param] | 読み取り専用 |
| [!UICONTROL Creative Type] | オプション |
| [!UICONTROL Tracking Template] | 読み取り専用 |
| [!UICONTROL Creative Preferred Devices] | 読み取り専用 |
| [!UICONTROL Ad Status] | 必須 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Ad ID] | 行に「[!UICONTROL AMO ID]」が含まれていない限り、広告ステータスを変更する場合にのみ必要です。 |
| [!UICONTROL AMO ID] | 広告IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、広告ネットワークにIDを投稿しません。 |

### 動的な検索ターゲット（自動ターゲット）フィールド

>[!NOTE]
>
>作成サポートは利用できません。

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Auto Target Expression] | 必須。 |
| [!UICONTROL Match Type] | オプション |
| [!UICONTROL Max CPC] | オプション |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Target Status] | ターゲットを削除する必要があります |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Target ID] | 自動ターゲットを変更または削除する場合にのみ必須です。ただし、行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り例外です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### 買い物商品のグループフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 必須 |
| [!UICONTROL Match Type] | 製品グループの作成に必要です。 |
| [!UICONTROL Max CPC] | 製品グループの作成に必要です。 |
| [!UICONTROL Parent Product Groupings] | 必須 |
| [!UICONTROL Product Grouping] | 必須 |
| [!UICONTROL Partition Type] | 製品グループの作成に必要です。 |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Product Group Status] | 製品グループを削除する場合にのみ必要です。 |
| \[広告主固有ラベル分類\] | オプション |
| [!UICONTROL Constraints] | オプション |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション |
| [!UICONTROL Product Group ID] | 製品グループを変更または削除する場合にのみ必要です。ただし、行にa）製品グループを識別するのに十分なプロパティ列またはb）および「[!UICONTROL AMO ID]」が含まれていない限り必要です。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### キャンペーンレベルのサイトリンクフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| 説明行1 | オプション |
| [!UICONTROL Description Line 2] | オプション |
| [!UICONTROL Start Date] | オプション |
| [!UICONTROL End Date] | オプション |
| [!UICONTROL Base URL/Final URL] | 必須 |
| [!UICONTROL Custom URL Param] | オプション |
| [!UICONTROL Tracking Template] | オプション |
| [!UICONTROL Creative Preferred Devices] | オプション |
| [!UICONTROL Link Name] | 必須 |
| [!UICONTROL Sitelink Status] | サイトリンクの削除のみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Sitelink ID] | サイトリンクを変更または削除する場合にのみ必須です。ただし、行にa） サイトリンクを識別するのに十分なプロパティ列またはb） 「[!UICONTROL AMO ID]」が含まれている場合を除きます。 ただし、[!UICONTROL Sitelink ID]も[!UICONTROL AMO ID]も含めず、プロパティ列が複数のサイトリンクに一致しない場合、サイトリンクの1つだけのステータスが変更されます。<br><br><b>注意：</b>既存のサイトリンクのステータス以外のサイトリンクプロパティ列を編集し、[!UICONTROL Sitelink ID]も[!UICONTROL AMO ID]も含まない場合、新しいサイトリンクが作成され、既存のサイトリンクは変更されません。 |
| [!UICONTROL AMO ID] | エンティティ IDと親エンティティ IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### 場所ターゲットフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Location] | 必須 |
| [!UICONTROL Location Type] | ターゲットの作成に必要 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Location Status] | 場所ターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL AMO ID] | キャンペーン IDを含めない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDを広告ネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのデバイスターゲットフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Device] | デバイスターゲットを削除するために必要です。 |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL Ad Group Name] | 広告グループレベルのデバイスターゲットに必要です。 キャンペーンレベルのデバイスターゲットには適用できません。 |
| [!UICONTROL Device Target Status] | デバイスターゲットを削除する場合にのみ必要です。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのデバイスターゲットにのみ適用されます。 |
| [!UICONTROL AMO ID] | Device Target IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDをアドネットワークに投稿しません。 |

### キャンペーンレベルおよび広告グループレベルのRLSA ターゲットフィールド

各データフィールドの説明については、「[使用可能なすべてのデータフィールド &#x200B;](#bulksheet-fields-all-microsoft)」を参照してください。

| フィールド | 必要ですか？ |
| ---- | ---- |
| [!UICONTROL Acct Name] | 各行にエンティティの「[!UICONTROL AMO ID]」が含まれていない限り、必須です。 |
| [!UICONTROL Campaign Name] | 必須 |
| [!UICONTROL Ad Group Name] | 広告グループレベルのターゲットに必要です。 キャンペーンレベルのターゲットには適用できません。 |
| [!UICONTROL Audience] | 新しいターゲットを作成する必要があります。 |
| [!UICONTROL Target Type] | オプション |
| [!UICONTROL Bid Adjustment] | オプション |
| [!UICONTROL RLSA Target Status] | ターゲットを削除する必要があります。 |
| [!UICONTROL Campaign ID] | オプション |
| [!UICONTROL Ad Group ID] | オプション。広告グループレベルのターゲットにのみ適用できます。 |
| [!UICONTROL RLSA Target ID] | ターゲットを変更または削除する場合にのみ必須です。行にターゲットの「[!UICONTROL AMO ID]」が含まれていない限り必須です。 |
| [!UICONTROL AMO ID] | RLSA ターゲット IDが含まれていない限り、データを編集または削除する必要があります。<br><br>Search, Social, &amp; Commerceでは、値を使用して正しいIDを判断しますが、IDをアドネットワークに投稿しません。 |

>[!MORELIKETHIS]
>
>* [付録 – バルクシート エラー](../bulksheet-errors.md)
>* [&#x200B; バルクシートで実行できる操作](bulksheet-operations.md)
>* [&#x200B; サポートされているバルクシート ファイル形式](bulksheet-file-formats.md)
>* [&#x200B; バルクシート ファイルのダウンロードと作成](../bulksheet-download.md)
>*  [!DNL Naver][&#128279;](/help/search-social-commerce/tracking/formats-click-tracking-naver.md)の クリックトラッキング形式
>* [&#x200B; バルクシート ファイルをアップロードするか、エラーファイルを修正](../bulksheet-upload.md)
