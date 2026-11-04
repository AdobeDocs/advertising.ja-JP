---
title: 柔軟性の高いHTML5のクリエイティブバリエーションの制作
description: AIを活用して、柔軟性に優れたHTML5のクリエイティブのバリエーションを制作し、保存する方法を学びましょう。
feature: Creative Standard Creatives
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
    internal-label: Advertising
feature_v2:
  - id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
    internal-label: Creative
subfeature_v2:
  - id: d06c1576-7039-4934-b256-7366e138fbb6
    internal-label: Creative Standard Creatives
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
    internal-label: User
source-git-commit: 1cc477f531051d94ea88eaae0a4fb83918e95ea5
workflow-type: tm+mt
source-wordcount: '840'
ht-degree: 0%
---
# 柔軟性の高いHTML5のクリエイティブバリエーションの制作

[!UICONTROL Ad Variations Generator]を使用して、既存の柔軟なHTML 5 クリエイティブの新しいバリエーションを作成します。 AI アシスタントを利用して、見出し、CTA、画像、カラーなどを生成および調整し、単一のセッションで新しいサイズのバリエーションを作成できます。 生成されたバリエーションを新しい標準広告としてクリエイティブライブラリに保存します。

>[!NOTE]
>
>[!UICONTROL Creative Studio]から広告バリエーションを生成することもできます。 両方のエントリ ポイントが同じ[!UICONTROL Ad Variations Generator]を開きます。 その他のエントリポイントについては、「[Creative Studioで標準広告の広告バリエーションを生成する](/help/creative/creative-studio/creative-studio-manage-standard-ads.md#generate-ad-variations)」を参照してください。

## 対象 {#availability}

**[!UICONTROL Generate Variations]** アクションは、新しい[!UICONTROL Creative Libraries] UIで、システムテンプレートに基づくクリエイティブを含む、柔軟なHTML5 クリエイティブで使用できます。 動的クリエイティブを含む他のクリエイティブタイプでは使用できません。

クリエイティブに、ジェネレーターで必要な内部親広告テンプレート参照がない場合、このアクションは無効になります。 この参照は、編集できる設定ではありません。クリエイティブの&#x200B;**[!UICONTROL Template]** タブにファイルをアップロードまたは置き換えても、明示的に設定されません。

## 広告バリエーション生成ツールを開き {#open-generator}

1. メインメニューで、**[!UICONTROL Creative]** > **[!UICONTROL Creative Libraries]**&#x200B;をクリックします。

1. 次のいずれかの方法でライブラリを開きます。

   * ライブラリ名をクリックします。
   * ライブラリ名の横にある「**[!UICONTROL ...]**」 > 「**[!UICONTROL Open]**」をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、柔軟なHTML5 クリエイティブ名の横にある「**[!UICONTROL ...]**」をクリックし、「**[!UICONTROL Generate Variations]**」をクリックします。

   [!UICONTROL Ad Variations Generator]が開き、選択したクリエイティブのコンテンツが表示されます。 キャンバスには、テンプレートの使用可能な広告フォーマットを含む&#x200B;**[!UICONTROL Template Sizes]** セクションと、生成されたコンテンツが表示される&#x200B;**[!UICONTROL Ad Concepts]** セクションが表示されます。

## バリエーションの生成と調整 {#generate-variations}

1. （オプション）広告にブランドプロファイルを適用するには、キャンバスツールバーで&#x200B;**[!UICONTROL Brand Profile]**&#x200B;を選択します。

   AI アシスタントは、コンテンツを生成する際に、ブランドのロゴ、カラーパレット、音声ガイドライン、画像標準、チャネルガイドラインを使用します。

1. [!UICONTROL AI Assistant]を使用して広告バリエーションを作成します：

   1. **[!UICONTROL Ask AI to generate ad variations…]** フィールドにリクエストを入力して&#x200B;**[!UICONTROL Enter]**&#x200B;を押すか、機能プロンプトのいずれかをクリックします。

      * **[!UICONTROL Write 3 headline variations for this template]**
      * **[!UICONTROL Generate 3 versions of this ad that will help with performance]**
      * **[!UICONTROL Create a new size template]**

      AIはキャンバス上で結果を生成し、それらを&#x200B;*概念*&#x200B;に整理します。各コンセプトは、明確なコンテンツのバリエーションを表します。 **[!UICONTROL Ad Concepts]** セクションの概念カウンターは、存在する概念の数を追跡します（例：**（2/10）**）。 1 セッションにつき最大10個のコンセプトを使用できます。

   1. フォローアップメッセージを送信して改善を続ける。 例：

      * 「すべてのコピーをより遊び心のあるものにし、企業的な側面を減らしましょう。」
      * 「ロゴを白いバージョンに変更します。」
      * 「すべてのコンセプトでCTAを『 Shop Now 』にセットしよう」
      * 「この広告のサイズを6つすべてのIAB標準ディスプレイサイズに変更します。」
      * 「各見出しに一致する背景画像を含む3つの異なる見出しコンセプトを提供してください。」

      >[!NOTE]
      >
      >AI アシスタントは、テキスト（見出し、サブヘッドライン、CTA、ボディコピー）の生成と変更、背景画像の入れ替え、ブランドカラーの適用、ロゴバージョンの切り替え、新しいサイズテンプレートの作成を可能にします。 テンプレートの構造（エレメントの位置、レイアウト、間隔、パディング、フォントファミリー、フォントサイズ、境界線）は変更できません。 セッションを開始する前に、テンプレートエディターで構造的な変更を行います。 [&#x200B; テンプレートの編集](/help/creative/creative-studio/creative-studio-manage-templates.md#edit-template)を参照してください。

   1. （オプション）リクエストにビジュアル参照を含めるには、チャット入力領域の「**[!UICONTROL +]**」ボタンをクリックします。 **[!UICONTROL Select from Asset Library]** ダイアログで、次の操作を行います。

      * アセットライブラリでアセットを使用するには、アセットをクリックし、**[!UICONTROL Add to chat]**&#x200B;をクリックします。 メッセージを送信して、アセットをコンテキストとして含めます。

      * 1つ以上のアセットをアップロードするには、**[!UICONTROL Upload Assets]**&#x200B;をクリックし、デバイスまたはネットワーク上のファイルを選択します。

1. （オプション）生成された広告を確認するには、キャンバスツールバーを使用します。

   * **[!UICONTROL Brand]:** セッションに適用されたブランド プロファイルを選択または変更します。
   * **[!UICONTROL Zoom in]** / **[!UICONTROL Zoom out]:** キャンバスのズームレベルを調整します。
   * **[!UICONTROL Fit to screen]:**&#x200B;すべてのサイズを表示するには、ビューをリセットします。
   * **[!UICONTROL Replay animations]:** テンプレートのアニメーションを再生します。

   AIが新しいサイズを作成すると、新しいサイズ カードに&#x200B;**[!UICONTROL Adjust]**、**[!UICONTROL Keep]**、削除コントロールが表示されます。 **[!UICONTROL Keep]**&#x200B;をクリックしてサイズをそのまま受け入れ、**[!UICONTROL Adjust]**&#x200B;をクリックして表示エディターでテンプレートを開き、構造的な変更を行い、**[!UICONTROL Update Ad Format]**&#x200B;をクリックして保存するか、削除アイコンをクリックして新しいサイズを削除します。

1. （オプション）コンセプトとバリエーションを管理する：

   * コンセプトを管理するには、コンセプトラベルの上にカーソルを置き（例：**[!UICONTROL Concept 3]**）、**[!UICONTROL ...]**&#x200B;をクリックしてから、オプションを選択します。

     * **[!UICONTROL Add to chat]:**&#x200B;次のプロンプトでコンセプトを参照します。
     * **[!UICONTROL Delete]:**&#x200B;概念を削除します。

   * 個々のバリエーションを管理するには、バリエーション カードにカーソルを合わせて&#x200B;**[!UICONTROL ...]**&#x200B;をクリックし、次のオプションを選択します。

     * **[!UICONTROL Add to Chat]:**&#x200B;次のプロンプトでバリエーションを参照します。 また、バリエーションのカード本文を直接クリックして、メンションを切り替えることもできます。
     * **[!UICONTROL Edit Data]:** バリエーション **[!UICONTROL Name]**&#x200B;と、テンプレートで定義された各クリックタグのクリックスルーURLを更新できるダイアログが開きます。 **[!UICONTROL Save]**&#x200B;をクリックして適用します。
     * **[!UICONTROL Delete]:** バリエーションを削除します。

## バリエーションを保存 {#save-variations}

1. 生成された概念に満足したら、ヘッダーの&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;をクリックします。

   このボタンは、少なくとも1つの概念が存在するまで無効になります。

1. **[!UICONTROL Save Standard Ads]** ダイアログで、次の設定を確認し、**[!UICONTROL Save Standard Ads]**&#x200B;をクリックします。

   **[!UICONTROL Advertiser]:** ソース クリエイティブ ライブラリに関連付けられている広告主。 この値は変更できません。

   **[!UICONTROL Creative Library]:**&#x200B;新しい広告が保存されるソース クリエイティブ ライブラリ。 この値は変更できません。

   **[!UICONTROL Attach to Bundles]:** （オプション）有効にすると、保存されたクリエイティブが1つ以上のバンドルに添付されます。 広告バリエーションごとに、バンドルを選択するか、新しいバンドル名を入力します。

   **\[各広告の設定]:**&#x200B;各広告バリエーションについて、クリックタグごとに&#x200B;**[!UICONTROL Name]**、**[!UICONTROL Language]**、クリックスルーURLを表示し、オプションで変更できます。

   クリエイティブライブラリに戻ります。

>[!MORELIKETHIS]
>
>* [標準クリエイティブの編集](creative-edit-standard.md)
>* [Creative Studioで標準広告を管理](/help/creative/creative-studio/creative-studio-manage-standard-ads.md)
>* [Advertising Creativeでブランドプロファイルを管理](/help/creative/brands/brand-manage.md)
>* [!UICONTROL Creative Studio]&#x200B;[&#128279;](/help/creative/creative-studio/creative-studio-content-credentials.md)のC2PA メタデータ
