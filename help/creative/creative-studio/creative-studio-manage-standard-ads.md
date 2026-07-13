---
title: Creative Studioで標準広告を管理する
description: Creative Studio クリエイティブライブラリで、標準ディスプレイ広告を作成、編集、複製、ダウンロード、削除する方法について説明します。
exl-id: 01d3cdec-80d0-494c-94dd-d9d0ae8ca53c
product_v2: id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2: id: d0d9f2ed-c163-44e1-97a1-4ace121416b8
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a6ab21a588f5b069ea0783dee711f52d906a46f9
workflow-type: tm+mt
source-wordcount: 1181
ht-degree: 0%

---

# [!UICONTROL Creative Studio]の標準広告の管理

*Beta機能*

[!UICONTROL Creative Studio]の「**[!UICONTROL Creatives]**」タブは、テンプレートから生成された標準ディスプレイ広告のライブラリです。 ここから、[!UICONTROL Ad Variations Generator]を使用して広告を作成し、保存された広告を編集し、既存の広告から新しいバリエーションを生成し、変更ログを表示し、複製、ダウンロード、削除することができます。

## 標準的な広告の制作 {#create-standard-ads}

[!UICONTROL Ad Variations Generator]を使用して、テンプレートからディスプレイ広告コンテンツを生成します。 AI アシスタントを利用して、見出し、CTA、画像、カラーなどを生成および調整し、単一のセッションで新しいサイズのバリエーションを作成できます。

>[!NOTE]
>
>標準の広告生成は現在、ディスプレイ広告テンプレートのみをサポートしています。 ビデオ広告テンプレートは、「**[!UICONTROL Creatives]**」タブまたは「**[!UICONTROL Templates]**」タブのいずれからも開始ポイントとして利用できません。

### 前提条件

少なくとも1つのディスプレイ広告テンプレートがテンプレートライブラリに存在する必要があります。

### 標準広告を生成

1. 次のいずれかの方法で[!UICONTROL Ad Variations Generator]を開きます。

   * **「[!UICONTROL Creatives]」タブから：**

      1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

      1. **[!UICONTROL Creatives]** タブで、**[!UICONTROL Generate standard ads from templates]** クイックアクションカードの&#x200B;**[!UICONTROL Generate]**&#x200B;をクリックします。

      1. テンプレート選択ダイアログで、テンプレートをクリックして選択し、**[!UICONTROL Use this template]**&#x200B;をクリックします。

   * （ディスプレイ広告のみ） **「[!UICONTROL Templates]」タブから：**

      1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

      1. 「**[!UICONTROL Templates]**」タブをクリックします。

      1. テンプレートカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Generate ad variations]**&#x200B;をクリックします。

   [!UICONTROL Ad Variations Generator]が開きます。 キャンバスには、テンプレートの使用可能な広告フォーマットを含む&#x200B;**[!UICONTROL Template Sizes]** セクションと、生成されたコンテンツが表示される&#x200B;**[!UICONTROL Ad Concepts]** セクションが表示されます。

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
      >AI アシスタントは、テキスト（見出し、サブヘッドライン、CTA、ボディコピー）の生成と変更、背景画像の入れ替え、ブランドカラーの適用、ロゴバージョンの切り替え、新しいサイズテンプレートの作成を可能にします。 テンプレートの構造（エレメントの位置、レイアウト、間隔、パディング、フォントファミリー、フォントサイズ、境界線）は変更できません。 セッションを開始する前に、テンプレートエディターで構造的な変更を行います。 [ テンプレートの編集](creative-studio-manage-templates.md#edit-template)を参照してください。

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

1. 生成された概念に満足したら、ヘッダーの&#x200B;**[!UICONTROL Save Standard Ads]**&#x200B;をクリックします。

   このボタンは、少なくとも1つの概念が存在するまで無効になります。

1. **[!UICONTROL Save Standard Ads]** ダイアログで、次の設定を指定し、**[!UICONTROL Save Standard Ads]**&#x200B;をクリックします。

   **[!UICONTROL Advertiser]:** （必須）下のクリエイティブを保存する広告主。

   **[!UICONTROL Creative Library]:** （必須） クリエイターを保存するクリエイティブライブラリ。 広告主を選択すると、ライブラリピッカーが有効になります。

   **[!UICONTROL Attach to Bundles]:** （オプション）有効にすると、保存されたクリエイティブが1つ以上のバンドルに添付されます。 広告バリエーションごとに、バンドルを選択するか、新しいバンドル名を入力します。

   **\[各広告の設定\]:**&#x200B;各広告バリエーションについて、**[!UICONTROL Name]、**、**[!UICONTROL Language]、**、**[!UICONTROL click URL]を表示し、オプションで変更できます。**

## 標準広告の編集 {#edit-standard-ad}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Edit]**&#x200B;をクリックします。

   左側にライブ広告のプレビュー、右側に設定パネルが表示されたフルスクリーンエディターが開きます。

1. **[!UICONTROL Details]**&#x200B;と&#x200B;**[!UICONTROL Attributes]** タブを使用して広告設定を編集します。

   **[!UICONTROL Details]** タブ：

   * **[!UICONTROL Creative Name]:** （必須） クリエイティブの表示名。
   * **[!UICONTROL Language]:** （必須）広告コンテンツの言語。
   * **[!UICONTROL Creative Size]:** （読み取り専用）広告ディメンション。
   * **クリックタグ：** テンプレートでクリックタグが定義されている場合、各クリックタグは、タグ名でラベル付けされた必須フィールドとして表示されます。 各タグのクリックスルー先URLを入力します。
   * **[!UICONTROL Label]:** （オプション）クリエイティブを整理するためのラベル。 既存のラベルを選択するか、新しいタグを入力して、**[!UICONTROL Add tag].**&#x200B;をクリックします

   **[!UICONTROL Attributes]** タブ：

   ライブプレビューは、編集中にリアルタイムで更新されます。 プレビューの読み込み中は、**[!UICONTROL Attributes]** タブを利用できません。

   * **テキスト属性：** テンプレートで定義された編集可能な各テキストレイヤーのテキスト値を入力します。
   * **画像属性：**&#x200B;現在の画像のサムネールを表示します。 **[!UICONTROL Replace Image]**&#x200B;をクリックして、代わりのファイル（PNG、JPEG、GIF、WebP、またはSVG）をアップロードします。

1. **[!UICONTROL Update Creative]**&#x200B;をクリックします。

## 標準的な広告の広告バリエーションを生成 {#generate-ad-variations}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Generate Ad Variations]**&#x200B;をクリックします。

   選択した広告がプリロードされた状態で[!UICONTROL Ad Variations Generator]が開きます。

1. AIのチャットインターフェイスを使用して、追加のバリエーションを生成、改良します。 完全なワークフローについては、「[標準広告を作成](#create-standard-ads)」を参照してください。

## 標準広告の複製 {#duplicate-standard-ad}

標準広告を複製して、同じ設定の新しいクリエイティブをライブラリに追加します。 後で新しいクリエイティブの名前を変更し、必要に応じて設定を編集できます。

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Duplicate]**&#x200B;をクリックします。

   新しいクリエイティブ名は`<original name> (copy)`です。

## 標準広告の変更ログを表示する {#view-change-log}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Change Log]**&#x200B;をクリックします。

   広告の変更表を表示するダイアログが開きます。

## 標準広告をダウンロード {#download-standard-ad}

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Download]**&#x200B;をクリックします。

   クリエイティブは、ブラウザーの通常の手順に従ってダウンロードされます。

## 標準広告の削除 {#delete-standard-ad}

>[!NOTE]
>
>この操作は元に戻せません。

1. メインメニューで、**[!UICONTROL Creative Studio]**&#x200B;をクリックします。

1. 「**[!UICONTROL Creatives]**」タブで、クリエイティブカードの上にカーソルを置き、**[!UICONTROL ...]** > **[!UICONTROL Delete]**&#x200B;をクリックします。

1. 確認メッセージで、**[!UICONTROL Delete]**&#x200B;をクリックします。

>[!MORELIKETHIS]
>
>* [Advertising CreativeのCreative Studioについて](creative-studio-about.md)
>* [Creative Studioで動的なクリエイティブを管理](creative-studio-manage-dynamic-ads.md)
>* [Creative Studioでテンプレートを管理](creative-studio-manage-templates.md)
>* [Advertising Creativeでブランドプロファイルを管理](/help/creative/brands/brand-manage.md)

