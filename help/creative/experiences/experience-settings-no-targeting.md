---
title: ターゲット以外のエクスペリエンスの設定
description: デシジョンツリーのターゲット設定を使用しない広告エクスペリエンスのすべての設定の説明を参照してください。
feature: Creative Experiences
exl-id: aeeca035-8ae2-4173-827a-b8690d228549
source-git-commit: e070e676b9ae321ddc73acfff0dfc05ea91f9715
workflow-type: tm+mt
source-wordcount: '1096'
ht-degree: 0%

---

# ターゲット以外のエクスペリエンスの設定

*クローズドベータ版*

## [!UICONTROL Experience basics] セクション

**[!UICONTROL Advertiser]:** （既存のエクスペリエンスの場合は読み取り専用）エクスペリエンスに含まれるクリエイティブに入札する広告主。 エクスペリエンスを保存すると、広告主を変更できなくなります。

**[!UICONTROL Experience Name]:** エクスペリエンスの一意の名前。 **ヒント：** Advertising DSPまたは他のDSPで広告としてエクスペリエンスを使用する際に見つけやすい名前を使用します。

**[!UICONTROL Creative Library]:** （既存のエクスペリエンスの場合は読み取り専用）エクスペリエンスに使用する単一のクリエイティブライブラリ。 エクスペリエンスを保存すると、ライブラリを変更できなくなります。

## [!UICONTROL Default creatives] セクション

**\[ 指定されたデフォルトのクリエイティブ ]:** ブラウザーがJavaScriptに対応していない場合や、遅延が原因で広告サーバーが広告をパーソナライズできない場合など、エクスペリエンスに割り当てられたクリエイティブをブラウザーで表示できない場合に使用するデフォルトの画像クリエイティブです。 エクスペリエンスが適用される広告サイズごとに 1 つの画像クリエイティブを含めます。 選択肢によって、エクスペリエンスに使用できるクリエイティブのサイズが決まります。<!-- In the legacy product, you selected the ad sizes for the experience, and then selected default images for each of those ad sizes. -->

デシジョンツリーのターゲット設定を使用しないエクスペリエンスの場合、デフォルトのクリエイティブを [!UICONTROL Tag Manager] 内で同じサイズのクリエイティブに上書きできます。

* 異なるサイズの既定のクリエイティブを追加するには、[**[!UICONTROL + Add Sizes]**] をクリックし、追加する各クリエイティブの横にあるチェック ボックスを右側のウィンドウから選択して、[**[!UICONTROL Add Creatives]**] をクリックします。

* デフォルトのクリエイティブを削除するには、クリエイティブサムネールの上にカーソルを置き、![ 削除 ](/help/creative/assets/delete.png " 削除 ") をクリックします。

* デフォルトのクリエイティブをすべて削除するには、「![ 削除 ](/help/creative/assets/delete.png " 削除 ")」をクリッ **[!UICONTROL Delete all]** します。

* 右側のクリエイティブパネルを表示または非表示にするには、右側のパネルの右上にある ![ 表示/非表示 ](/help/creative/assets/hide-show-creatives.png " 表示/非表示 ") をクリックします。

## [!UICONTROL Targeting] セクション

**[!UICONTROL Targeting]:** （既存のエクスペリエンスに対しては読み取り専用）デシジョンツリーを使用してターゲティングを有効にしない場合は適用されません。このオプションは無効のままにしてください。 **メモ：** ターゲティングを行わずにエクスペリエンスを保存すると、後でターゲティングを追加することはできません。

**[!UICONTROL Dynamic ads]:** （既存のエクスペリエンスの読み取り専用）エクスペリエンスに動的広告が含まれていることを示します。 **メモ：** エクスペリエンスには、すべての標準広告またはすべての動的広告のいずれかを含めることができます。

**[!UICONTROL Language Targeting]:** （標準広告を使用したエクスペリエンスのみ。オプション。既存のエクスペリエンスの場合は読み取り専用） ユーザーのブラウザーの言語設定を確認し、指定した言語のクリエイティブが使用可能な場合に、その言語のクリエイティブを表示します。 ブラウザーで指定された言語のクリエイティブが使用できない場合は、代わりに [!UICONTROL Preferred language] 設定が使用されます。 エクスペリエンスを保存すると、この設定を変更できなくなります。

**[!UICONTROL Preferred language]:** （標準広告を使用したエクスペリエンスのみ。既存のエクスペリエンスの場合は読み取り専用） [!UICONTROL Language Targeting] が有効になっている場合を除き、エクスペリエンスから作成されたすべての広告の言語。 エクスペリエンスを保存すると、この設定を変更できなくなります。

## [!UICONTROL Advanced] セクション

**データパス：** （Dynamic Ads を使用したエクスペリエンスのみ。オプション） DSP、パブリッシャー、パートナーがインプレッションでリアルタイムに渡す特定のキーと値のペアに基づいてユーザーをターゲットに設定します。 最大 5 つのデータパスキー（パラメーター）を指定できます。<!-- May move this to just within the decision tree. -->

特定のクリエイティブサイズの広告エクスペリエンスタグを作成すると、このフィールドで指定された各キーがタグのマクロとして追加されます。 DSPでタグを広告として実装する前に、タグ内の各キーと値のペアを入力します。

**半径：** （動的広告を使用したエクスペリエンスのみ。オプション）フィードファイルで指定されている米国の郵便番号からターゲットまでの半径。0 マイルから 200 マイルまでの半径を選択します。 エクスペリエンスの動的広告の作成に使用するフィードファイルには <!-- or a user-named column mapped to a ZIP column --> ファイル内の各製品行の値を持つ [!UICONTROL ZIP] 列を含める必要があります。 例えば、半径が 10 マイルの場合、95110 で利用可能な製品の広告を、95110 から 10 マイル以内のユーザーに表示できます（ユーザーの IP アドレスによって決定されます）。

**RT Pixel:** （動的広告を含むエクスペリエンスのみ。オプション）潜在的にターゲットにする [!UICONTROL Creative] リターゲティングピクセル。 デシジョンツリー内でターゲティングを設定する場合、1 レベルの RT ピクセルターゲットノードを含めることができます。 各ノードには、ターゲットとするピクセルと、割り当てられたクリエイティブバンドル内のクリエイティブを表示するために必要なピクセルの属性の値を指定します。 このフィールドでピクセルを指定しない場合でも、デシジョンツリー内でピクセルを指定できます。<!-- From R: "the RT Pixel should be via the content selection in the Dynamic ad setup." Clarify. I do see "Datapass" (oneword) in the dynamic ad settings, but I'm not sure how that setting and this experience-level one work together. -->

**[!UICONTROL Label]:**<!-- should be "Labels" --> （任意）エクスペリエンスに適用する [!DNL Creative] 固有のラベル。 エクスペリエンス <!-- sic --> ビューで、ラベル別にエクスペリエンスをフィルタリングできます。

* 既存のラベルを選択するには、[![ 下 ](/help/creative/assets/chevron-down.png " 下 ")] をクリックし、適用する各ラベルの横にあるチェック ボックスをオンにします。

* 既存のラベルを検索するには、ラベル名の中にテキスト文字列を入力します。

* 適用する新しいラベルを作成するには、リストを開き、「**+ ラベルを追加**」をクリックし、「[!UICONTROL Label]」フィールドに新しいラベル名を入力して、「**作成**」をクリックします。

* ラベルを削除するには、ラベル名の横にあるチェックボックスの選択を解除します。

**[!UICONTROL Impression Tracking URL]:** （任意）エクスペリエンスから作成された広告のランディングページ URL に追加するサードパーティのインプレッショントラッキング URL。 最大 5 つの URL を含めることができます。 追加の URL を追加するには、![ アイコン ](/help/creative/assets/create.png) **[!UICONTROL Add More] をクリックして URL を入力します。

URL を入力すると、すべての [ 使用可能なマクロ ](/help/creative/creative-macros.md) とそれらを置き換えるデータが、ページの下部に表示されます。 URL 内にマクロの 1 つを挿入するには、マクロの説明の上にカーソルを置き、![ クリップボードにコピー ](/help/creative/assets/copy-to-clipboard.png " クリップボードにコピー ") をクリックし、必要な場所にマクロを URL フィールドに貼り付けます。

>[!NOTE]
>
>* [!DNL Creative] ランディングページの URL に、独自のインプレッショントラッキングタグを自動的にプレフィックスします。
>* エクスペリエンス内の任意のクリエイティブに対してこの URL を上書きできます。
>* また、「[!UICONTROL Client JS]」フィールドには、サードパーティのJavaScript インプレッショントラッキングコードを入力することもできます

**[!UICONTROL Click Tracking URL]:** （任意）（任意）ランディングページ URL に追加するサードパーティのクリックトラッキング URL。 最大 5 つの URL を含めることができます。 追加の URL を追加するには、![ アイコン ](/help/creative/assets/create.png) **[!UICONTROL Add More]** をクリックして URL を入力します。

URL を入力すると、すべての [ 使用可能なマクロ ](/help/creative/creative-macros.md) とそれらを置き換えるデータが、ページの下部に表示されます。 URL 内にマクロの 1 つを挿入するには、マクロの説明の上にカーソルを置き、![ クリップボードにコピー ](/help/creative/assets/copy-to-clipboard.png " クリップボードにコピー ") をクリックし、必要な場所にマクロを URL フィールドに貼り付けます。

>[!NOTE]
>
>* [!DNL Creative] ランディングページの URL に、独自のインプレッショントラッキングタグを自動的にプレフィックスします。
>* エクスペリエンス内の任意のクリエイティブに対して、この URL を上書き <!-- creative bundle for targeted experiences --> きます。

**[!UICONTROL Client JS]:** （オプション）次のいずれか：

* （広告主が広告に OBA コンプライアンスベンダーを使用している場合）ユーザーがオンライン行動ターゲティング（OBA）をオプトアウトできるようにする広告オーバーレイを指すJavaScript コード。

* ランディングページに追加するサードパーティのJavaScript インプレッショントラッキングコード。 **メモ：** 「[!UICONTROL Impression Tracking URL]」フィールドにサードパーティのインプレッショントラッキング URL を入力することもできます。

>[!MORELIKETHIS]
>
>* [ デシジョンツリーのターゲット設定を使用しないエクスペリエンスの作成 ](experience-create-no-targeting.md)
>* [ デシジョンツリーのターゲット設定を使用しないエクスペリエンスの編集 ](experience-edit-no-targeting.md)
>* [URL をトラッキングするために使用可能なマクロ ](/help/creative/creative-macros.md)
>* [ 該当するクリエイティブサイズの広告タグを手動で作成 ](experience-tag-create-manually.md)
>* [ ターゲティングを行わないエクスペリエンスの広告タグへのクリエイティブの割り当て ](experience-tag-assign-creatives.md)
>* [ ターゲット設定を行わないエクスペリエンス用のトラッキング URL のカスタマイズ ](experience-tracking-urls-no-targeting.md)
>* [ ターゲティングを行わないエクスペリエンスのクリエイティブな最適化とスケジュールのカスタマイズ ](experience-optimization-scheduling-no-targeting.md)
