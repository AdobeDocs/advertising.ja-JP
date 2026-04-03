---
title: ターゲットを絞らないエクスペリエンスの設定
description: 決定木ターゲティングを使用しない広告エクスペリエンスに関するすべての設定の説明を参照してください。
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
TQID: https://experienceleague.adobe.com/Qz-MUPLNsdn4PvnaF-uDAZQjd-iXJD0oEZOkMSUGuEs
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: b2025470-04ef-4dd9-bdd4-44407644aeb6
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 527ca2bb74de388c13ba1ce5bde3f8be1cead8d0
workflow-type: tm+mt
source-wordcount: 1126
ht-degree: 0%

---

# ターゲットを絞らないエクスペリエンスの設定

## [!UICONTROL Experience basics] セクション

**[!UICONTROL Ad Type]:** （既存のエクスペリエンスの読み取り専用） エクスペリエンスに含まれる広告の種類：*[!UICONTROL Standard Display]*、*[!UICONTROL Dynamic Display]*、*[!UICONTROL Standard Video]*&#x200B;または&#x200B;*[!UICONTROL Display Video]*。 エクスペリエンスを保存すると、広告の種類を変更することはできません。

**[!UICONTROL Advertiser]:** （既存のエクスペリエンスの読み取り専用） エクスペリエンスに含まれるクリエイティブに入札する広告主。 エクスペリエンスを保存しても、広告主を変更することはできません。

**[!UICONTROL Experience Name]:** エクスペリエンスの一意の名前。 **ヒント：** Advertising DSPまたはその他のDSPでエクスペリエンスを広告として使用する際に、簡単に見つけることができる名前を使用します。

**[!UICONTROL Creative Library]:** （既存のエクスペリエンスの読み取り専用） エクスペリエンスに使用する単一のクリエイティブライブラリ。 エクスペリエンスを保存すると、ライブラリを変更することはできません。

## [!UICONTROL Default creatives] セクション

**\[Default creatives specified\]:** ブラウザーがJavaScriptに対応していない場合や、広告サーバーが遅延のために広告をパーソナライズできない場合など、ブラウザーがエクスペリエンスに割り当てられたクリエイティブを表示できない場合に使用するデフォルトのクリエイター。 標準的なディスプレイエクスペリエンスの場合は、エクスペリエンスが適用される広告サイズごとに1つの画像クリエイティブを含めます。 標準的な動画エクスペリエンスの場合は、広告サイズごとにエクスペリエンスが適用される動画クリエイティブを1つ含めます。 エクスペリエンスに使用できるクリエイティブサイズは、選択によって決まります。

決定木のターゲット設定がないエクスペリエンスの場合は、[!UICONTROL Tag Manager]内で同じサイズのクリエイターを使用して、デフォルトのクリエイターを上書きできます。

* ディメンションが異なるデフォルトのクリエイティブを追加するには、**[!UICONTROL + Add Sizes]**&#x200B;をクリックし、右側のペインから追加する各クリエイティブの横にあるチェックボックスをオンにして、**[!UICONTROL Add Creatives]**&#x200B;をクリックします。

* デフォルトのクリエイティブを削除するには、クリエイティブのサムネールの上にカーソルを置き、![削除](/help/creative/assets/delete.png "削除")をクリックします。

* すべてのデフォルトのクリエイティブを削除するには、![削除](/help/creative/assets/delete.png "削除") **[!UICONTROL Delete all]**&#x200B;をクリックします。

* 右側のクリエイティブペインを表示または非表示にするには、右側のペインの右上にある![表示/非表示](/help/creative/assets/hide-show-creatives.png "表示/非表示")をクリックします。

## [!UICONTROL Targeting] セクション

**[!UICONTROL Targeting]:** （既存のエクスペリエンスの読み取り専用）決定ツリーを使用してターゲティングを有効にしない場合は適用されません。このオプションを無効のままにしてください。 **注意：** ターゲティングなしでエクスペリエンスを保存すると、後でターゲティングを追加することはできません。

**[!UICONTROL Language Targeting]:** （標準広告を含むエクスペリエンスのみ。オプション。既存のエクスペリエンスの読み取り専用）ユーザーのブラウザー言語設定を確認し、その言語のクリエイティブが使用可能な場合に、指定された言語でクリエイティブを表示します。 ブラウザー指定の言語のクリエイティブが使用できない場合は、代わりに[!UICONTROL Preferred language]設定が使用されます。 エクスペリエンスを保存すると、この設定を変更することはできません。

**[!UICONTROL Preferred language]:** （標準広告を含むエクスペリエンスのみ。既存のエクスペリエンスの読み取り専用） [!UICONTROL Language Targeting]が有効になっている場合を除き、エクスペリエンスから作成されたすべての広告の言語。 エクスペリエンスを保存すると、この設定を変更することはできません。

## [!UICONTROL Advanced] セクション

**データパス：** （動的な広告を含むエクスペリエンスのみ。オプション）インプレッションでDSP、パブリッシャー、またはパートナーがリアルタイムで渡す特定のキーと値のペア（SKU=01234567890123またはCart=emptyなど）に基づいてユーザーをターゲティングします。 最大5つのデータパスキー（パラメーター）を指定できます。<!-- May move this to just within the decision tree. -->

特定のクリエイティブサイズの広告エクスペリエンスタグを作成すると、このフィールドで指定された各キーが、タグ内のマクロとして追加されます。 DSPに広告としてタグを実装する前に、タグ内の各キーと値のペアの値を入力します。

**半径：** （動的な広告を使用したエクスペリエンスのみ。オプション）ターゲットにするフィードファイルで指定された米国の郵便番号からの半径。0 マイルから200 マイルまでの半径を選択します。 エクスペリエンスの動的広告の作成に使用されるフィードファイルには、ファイル内の各製品行の値を含む[!UICONTROL ZIP]列<!-- or a user-named column mapped to a ZIP column -->が含まれている必要があります。 例えば、半径10 マイルの場合、95110で利用可能な商品の広告を、95110から10 マイル以内のユーザーに表示することができます（ユーザーのIP アドレスによって決定されます）。

**RT ピクセル：** （動的な広告を使用したエクスペリエンスのみ。オプション）潜在的にターゲットにする[!UICONTROL Creative] リターゲティングピクセル。 決定ツリー内でターゲティングを設定する場合、RT ピクセルターゲットノードの1つのレベルを含めることができます。 各ノードに対して、ターゲットとするピクセルと、割り当てられたクリエイティブバンドル内のクリエイターを表示するために必要なピクセルの属性の値を指定します。 このフィールドでピクセルを指定しない場合でも、決定ツリー内でピクセルを指定できます。<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> （オプション）エクスペリエンスに適用する[!DNL Creative]固有のラベル。 エクスペリエンスビューでラベルでエクスペリエンスをフィルタリングし、[!UICONTROL Experience Label] ディメンションを[!UICONTROL Custom Creative Report]に含めることができます。

* 既存のラベルを選択するには、![&#x200B; ダウン &#x200B;](/help/creative/assets/chevron-down.png " ダウン ")をクリックし、適用する各ラベルの横にあるチェックボックスをオンにします。

* 既存のラベルを検索するには、ラベル名の中にテキスト文字列を入力します。

* 適用する新しいラベルを作成するには、リストを開き、**+ ラベルを追加**&#x200B;をクリックし、[!UICONTROL Label] フィールドに新しいラベル名を入力して、**作成**&#x200B;をクリックします。

* ラベルを削除するには、ラベル名の横にあるチェックボックスの選択を解除します。

**[!UICONTROL Impression Tracking URL]:** （オプション） エクスペリエンスから作成された任意の広告のランディングページ URLに追加する、サードパーティのインプレッション追跡URL。 5つまでURLを含めることができます。 追加のURLを追加するには、![icon](/help/creative/assets/create.png) **[!UICONTROL Add More]をクリックし、URLを入力します。

URLを入力すると、使用可能なすべての[&#x200B; マクロ &#x200B;](/help/creative/creative-macros.md)と、その代わりに使用するデータがページの下部に表示されます。 URLにマクロのいずれかを挿入するには、マクロの説明にカーソルを合わせて![&#x200B; クリップボードにコピー](/help/creative/assets/copy-to-clipboard.png " クリップボードにコピー")をクリックし、URL フィールドにマクロを任意の場所に貼り付けます。

>[!NOTE]
>
>* [!DNL Creative]は、ランディングページ URLに独自のインプレッション追跡タグを自動的にプレフィックスします。
>* このURLは、エクスペリエンス内の任意のクリエイティブに対して上書きできます。
>* サードパーティのJavaScript インプレッション トラッキング コードを[!UICONTROL Client JS] フィールドに入力することもできます

**[!UICONTROL Click Tracking URL]:** （オプション） （オプション） ランディングページ URLに追加するサードパーティのクリックトラッキング URL。 5つまでURLを含めることができます。 追加のURLを追加するには、![icon](/help/creative/assets/create.png) **[!UICONTROL Add More]**&#x200B;をクリックし、URLを入力します。

URLを入力すると、使用可能なすべての[&#x200B; マクロ &#x200B;](/help/creative/creative-macros.md)と、その代わりに使用するデータがページの下部に表示されます。 URLにマクロのいずれかを挿入するには、マクロの説明にカーソルを合わせて![&#x200B; クリップボードにコピー](/help/creative/assets/copy-to-clipboard.png " クリップボードにコピー")をクリックし、URL フィールドにマクロを任意の場所に貼り付けます。

>[!NOTE]
>
>* [!DNL Creative]は、ランディングページ URLに独自のインプレッション追跡タグを自動的にプレフィックスします。
>* このURLは、エクスペリエンス内の任意のクリエイティブ <!-- creative bundle for targeted experiences -->に対して上書きできます。

**[!UICONTROL Client JS]:** （オプション）次のいずれか：

* （広告主が広告にOBA コンプライアンスベンダーを使用する場合）ユーザーがオンライン行動ターゲティング（OBA）をオプトアウトできる広告オーバーレイを指すJavaScript コード。

* ランディングページに追加する、サードパーティのJavaScriptインプレッショントラッキングコード。 **メモ：** サードパーティのインプレッション追跡URLを[!UICONTROL Impression Tracking URL] フィールドに入力することもできます。

>[!MORELIKETHIS]
>
>* [決定木ターゲティングを使用せずにエクスペリエンスを作成](experience-create-no-targeting.md)
>* [決定木ターゲティングを使用せずにエクスペリエンスを編集](experience-edit-no-targeting.md)
>* [URLのトラッキングに使用できるマクロ &#x200B;](/help/creative/creative-macros.md)
>* [該当するクリエイティブサイズの広告タグを手動で作成する](experience-tag-create-manually.md)
>* [&#x200B; ターゲティングせずにエクスペリエンス用の広告タグにクリエイターを割り当てる](experience-tag-assign-creatives.md)
>* [&#x200B; ターゲットを設定せずにエクスペリエンスのトラッキング URLをカスタマイズする](experience-tracking-urls-no-targeting.md)
>* [&#x200B; クリエイティブの最適化とスケジュールをカスタマイズして、ターゲットを設定せずにエクスペリエンスを利用](experience-optimization-scheduling-no-targeting.md)
