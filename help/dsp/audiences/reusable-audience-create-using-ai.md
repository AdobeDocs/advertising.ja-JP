---
title: 生成 AI を使用した再利用可能なオーディエンスの作成
description: AI 支援オーディエンスエージェントを使用して、Adobe Advertising DSPで再利用可能なオーディエンスを作成する方法を説明します。 自然言語プロンプトでターゲットオーディエンスを記述します。このエージェントは、サードパーティのセグメントを提案し、ターゲットまたは除外として使用するオーディエンス式を構築します。
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: 4eefcca15d4f84152278e7680917b9daed15f45d
workflow-type: tm+mt
source-wordcount: '994'
ht-degree: 0%

---

# 生成 AI を使用した再利用可能なオーディエンスの作成

*Beta機能*

*プロンプトを英語のみで表示*

<!-- I thought it was all segment types? -->

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

AI 支援オーディエンスエージェントを使用して、明言された要件に従って、使用可能なすべてのサードパーティセグメントを使用して、新しい再利用可能なオーディエンスを生成します。 オーディエンスを、複数のプレースメントのターゲットまたは除外として使用できます。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>この機能はベータモードにあり、変更される可能性があります。 生成されたオーディエンス式が、オーディエンスを作成してプレースメントに使用する前に、必要なオーディエンスを表していることを確認します。

## 生成 AI を使用した再利用可能なオーディエンスの作成

1. メインメニューで、**[!UICONTROL Audiences]**/**[!UICONTROL All Audiences]** をクリックします。

1. データ テーブルの上にある [**[!UICONTROL Create]**] をクリックします。

1. 一意の **[!UICONTROL Audience Name]** を入力します。

1. （オプション） **[!UICONTROL Share with all advertisers in my account]** すオプションの選択を解除します。

   オーディエンスを共有すると、アカウント内のすべての広告主に対するターゲットまたは除外として、オーディエンスを使用できるようになります。 ただし、オーディエンスの個々のセグメントは、そのセグメントが共有されているユーザーのみが使用できます。

1. 「**[!UICONTROL Save]**」をクリックします。

1. オーディエンスを作成します。

   ベータ版の権限を持つユーザーの場合は、「AI」オプションがデフォルトです。 [ オーディエンスを自分で組み立てる ](/help/dsp/audiences/reusable-audience-create.md) には、下部の「手動モードに切り替え」ボタンをクリックします。

   1. 1 つ以上のプロンプトを入力して、含めるおよび除外するオーディエンス特性を説明します。 各プロンプトを送信するには、「![ プロンプトの送信 ](/help/dsp/assets/submit-prompt.png " プロンプトの送信 ") をクリックします。

      詳しくは、「[ プロンプトの作成 ](#writing-prompts)」および「[ オーディエンスブリーフを作成するためのベストプラクティス ](#audience-brief-best-practices)」を参照してください。

      AI エージェントは、関連するセグメントを見つけると、条件に基づいてオーディエンス式を作成します。 また、オーディエンスを組み合わせるための一致するセグメントを探す前に、承認を求められます。

      オプションでリクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

   1. AI エージェントがオーディエンスを適切に説明するオーディエンス式を提示する場合は、オーディエンスの組み立てを続行するように AI エージェントに指示します。

      「続行」、「OK」、「OK」、「YES」または他の類似した単語を入力できます。

   1. （必要に応じて）追加の基準を指定します。 AI エージェントが条件をすべて満たすオーディエンスの式を提示したら、オーディエンスの組み立てを続行するように AI エージェントに指示します。

1. 組み合わせたオーディエンスに満足したら、「**[!UICONTROL Create]**」をクリックして、指定したオーディエンスを作成します。

   >[!NOTE]
   >
   >後で AI エージェントを使用してオーディエンスを編集することはできません。 代わりに [ オーディエンス式を手動で編集 ](/help/dsp/audiences/reusable-audience-edit.md) します。

## プロンプトの記述の基本 {#writing-prompts}

### プロンプトには何を含めるべきですか？

* ターゲットオーディエンスを説明するには、明確でわかりやすい言語を使用します。

  一般的に、プロンプトでは大文字と小文字が区別されず、明確にすることを除いて句読点は必要ありません。

* 具体的に指定し、含めるすべてのオーディエンス特性と、除外する特性の詳細を指定します。 提供する詳細情報が多いほど、ニーズを満たす結果が得られる可能性が高くなります。

* 含める、または除外する場所、デバイスタイプ、データプロバイダーを特定します。

* 条件と生成されたオーディエンス式を絞り込むための詳細を、オーディエンスを保存する前に繰り返し指定します。

* 実験を通じてプロンプトを表示する方法について説明します。

  オーディエンスエージェントは、生成されたオーディエンス式をオーディエンスとして自動的に保存しません。 オーディエンスを保存するには、プロンプト領域の外側にある「[!UICONTROL Create]」ボタンをクリックする必要があります。これにより、保存したくない変更を元に戻すことができます。

オーディエンスのプロンプトを最適化する方法について詳しくは [](#audience-brief-best-practices) オーディエンス概要の作成に関するベストプラクティス」を参照してください。

<!-- I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### プロンプトには何を含めることができないのですか？

* 既存のオーディエンス式への参照。

* 英語以外の言語のテキスト。

### AI エージェントの応答例と返信方法

AI エージェントから回答が必要な場合は、リクエストにキーワードを使用するか、同等の共通用語を使用して返信できます。

#### 質問する AI エージェントの応答

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

あなたの肯定的な答え：「続行」、「OK」、「OK」、「YES」、または他の類似した言葉

リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

#### 複数のオプションから選択するように求める AI エージェント応答

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

あなたの返信：`1`、`proceed`、`2`、`maximum reach` など。

リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

## オーディエンス概要の作成に関するベストプラクティス {#audience-brief-best-practices}

オーディエンス概要は、キャンペーンのターゲットオーディエンスを定義する戦略的書き上げです。 適切に作成された概要は、DSP オーディエンスエージェントがターゲット可能なオーディエンスを組み立てるために最も関連性の高いセグメントを特定するのに役立ちます。

### 効果的なオーディエンス概要の基本的な構成要素

概要の以下のリストから、できるだけ多くのオーディエンス属性タイプを含めます。 除外する属性を指定します。

<!-- What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **人口統計**

  年齢、性別、婚姻状況、世帯構成（家族の人数、子供の有無、複数世代の世帯）などの属性が含まれます。

* **社会経済指標**

  家計収入（HHI）バンド、教育レベル、職業/役職、雇用状況、および自宅所有状況を通じて財務能力を確立します。

* **地理的パラメーター**

  国/国、地域（EMEA、APAC、NA）、人口密度（都市/郊外/農村）などの位置範囲を定義します。

* **関心と親和性**

  趣味（スポーツ、芸術、アウトドア活動）、メディア消費パターン、ブランド親和性、ライフスタイルアクティビティ（旅行、食事、エンターテイメント）などの情熱と好みを特定します。

* **サイコグラフィック**

  願望（ステータスの追求、自己向上）、中心的価値（持続可能性、イノベーション、伝統）、性格特性（リスクの取り手、早期導入者）、購入の動機などの考え方と価値をキャプチャします。

* **行動信号**

  購入行動（ショッピング頻度、チャネル環境設定、ブランドロイヤルティ）、オンライン行動（web サイト訪問、コンテンツエンゲージメント、ソーシャルメディアアクティビティ）、オフライン行動（ストア訪問、イベント出席、メンバーシップ）などの観察可能なアクション。

* **市場内の意図**

  調査中の製品/サービス・カテゴリー、購入のタイムライン（即時、短期、長期）、購入の意思決定のトリガーとなる関連ライフ・イベントを通じて、購入の準備を特定します。

* **ライフステージ**

  キャリア段階（学生、新入生、キャリア途中、役員、退職者）、家族段階（新婚、新しい親、空のネスター）、主要な生活移行を含む現在の段階的理解。

### 予測キャンペーンに関する適切に構造化されたオーディエンス概要の例

次に、プレミアムミールキットのサブスクリプションサービスの認知と体験版を促進するキャンペーンの強力なオーディエンスブリーフの例を示します。

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [ 再利用可能なオーディエンスを複製 ](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [ 再利用可能なオーディエンスの編集 ](/help/dsp/audiences/reusable-audience-edit.md)
>* [ 再利用可能なオーディエンスに関する詳細の表示 ](/help/dsp/audiences/reusable-audience-view-details.md)
>* [ 再利用可能なオーディエンスの共有 ](/help/dsp/audiences/reusable-audience-share.md)
>* [ 再利用可能なオーディエンスの書き出し ](/help/dsp/audiences/reusable-audience-export.md)
>* [ 再利用可能なオーディエンスのセグメントキーをクリップボードにコピー ](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [ 再利用可能なオーディエンスを削除 ](/help/dsp/audiences/reusable-audience-delete.md)
