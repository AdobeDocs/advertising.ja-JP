---
title: 生成AIを使用して再利用可能なオーディエンスを作成する
description: AIを活用したオーディエンスエージェントを使用して、Adobe Advertising DSPで再利用可能なオーディエンスを作成する方法を説明します。 ターゲットオーディエンスを自然言語プロンプトで説明します。担当者はサードパーティセグメントを提案し、ターゲットまたは除外として使用するオーディエンス式を作成します。
feature: DSP Audiences
hidefromtoc: true
hide: true
exl-id: 82c9f122-2bdd-409f-a4d6-1da21ecbe913
source-git-commit: d450159cfcc0298a0bb9bb0984cd49ac75836519
workflow-type: tm+mt
source-wordcount: '1090'
ht-degree: 0%

---

# 生成AIを使用して再利用可能なオーディエンスを作成する

*Beta機能*

*英語のみサポート*

<!-- Redo the legacy file to include the new info. It's probably cleanest to keep it as two separate procedures (gen AI and manually) rather than one big, long procedure. -->

AIを活用したオーディエンスエージェントを使用して、記載された要件に従って利用可能なすべてのサードパーティセグメントを使用して、新しい再利用可能なオーディエンスを生成します。 複数のプレースメントのターゲットまたは除外としてオーディエンスを使用できます。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

>[!NOTE]
>
>この機能はベータモードで、一部変更される可能性があります。 オーディエンスを作成してプレースメントに使用する前に、生成されたオーディエンス式が必要なオーディエンスを表していることを確認してください。

## 生成AIを使用して再利用可能なオーディエンスを作成する

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

1. 一意の&#x200B;**[!UICONTROL Audience Name]**&#x200B;を入力してください。

1. （オプション）オプションの選択を&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;に解除します。

   オーディエンスを共有すると、そのオーディエンスは、アカウント内のすべての広告主に対してターゲットまたは除外として使用できるようになります。 ただし、オーディエンス内の個々のセグメントは、セグメントを共有するユーザーのみが使用できます。

1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. オーディエンスの構築：

   ベータ版の権限を持つユーザーの場合、AI オプションがデフォルトになります。 [自分でオーディエンスを組み立てる](/help/dsp/audiences/reusable-audience-create.md)には、下部にある「手動モードに切り替える」ボタンをクリックします。

   1. 含めたり除外したりするオーディエンス特性を説明する1つ以上のプロンプトを入力します。 各プロンプトを送信するには、![&#x200B; プロンプトを送信](/help/dsp/assets/submit-prompt.png " プロンプトを送信")をクリックします。

      詳しくは、「[&#x200B; プロンプトの作成](#writing-prompts)」および「[&#x200B; オーディエンス概要の作成に関するベストプラクティス &#x200B;](#audience-brief-best-practices)」を参照してください。

      オーディエンスエージェントが関連セグメントを見つけると、条件に基づいてブール値のオーディエンス式が作成されます。 また、オーディエンスを作成するための一致するセグメントを探す前に、承認を求めることもできます。

      オプションで、リクエストを無視し、代わりに追加のオーディエンス条件を引き続き指定できます。

   1. オーディエンスエージェントがオーディエンスを適切に説明するオーディエンス式を提示したら、オーディエンスエージェントにオーディエンスの作成を続行するように指示します。

      「続行」、「OK」、「OK」、「はい」または他の類似する単語を入力できます。 エージェントは、各特性に対するすべての推奨セグメント（「親」など）をリストします。 任意の特性を展開すると、その特性に対して提案された個々のセグメントに関する詳細が表示されます。

   1. （必要に応じて）追加の基準を指定します。 オーディエンスエージェントが、すべての基準を満たすオーディエンス式を提示したら、オーディエンスエージェントにオーディエンスの組み立てを続行するように指示します。

      オーディエンスを組み立てるには、「続行」、「OK」、「はい」、または他の類似する単語を入力します。 エージェントは、各特性に対するすべての推奨セグメント（「親」など）をリストします。 任意の特性を展開すると、その特性に対して提案された個々のセグメントに関する詳細が表示されます。

1. 組み立てられたオーディエンスに満足したら、**[!UICONTROL Create]**&#x200B;をクリックして、指定したオーディエンスを作成します。

   >[!NOTE]
   >
   >Audience Agentを使用して後でオーディエンスを編集することはできません。 代わりに、[&#x200B; オーディエンス式を手動で編集します](/help/dsp/audiences/reusable-audience-edit.md)。

## プロンプトの作成の基本 {#writing-prompts}

### プロンプトには何を含めるべきですか？

* ターゲットオーディエンスについて、わかりやすい言葉を使って説明します。

   * 完全な文章または特性の文字列のみを入力できます。 明確にするために必要な場合を除いて、句読点は必要ありません。

   * 一般に、プロンプトでは大文字と小文字が区別されません。

   * オーディエンスエージェントは、最も一般的な類義語を認識します。

* 含めたいオーディエンスの特徴と、除外したいオーディエンスの特徴を具体的に提示します。 詳細情報を提供すればするほど、ニーズに合った結果を得られる可能性が高くなります。

* 含めるまたは除外する場所、デバイスの種類、データプロバイダーを特定します。

* オーディエンスを保存する前に、基準と生成されたオーディエンス式を調整するための詳細を繰り返し提供します。

* テストによるプロンプトの作成についてご確認ください。

  プロンプトが明確でない場合は、オーディエンスエージェントが別のプロンプトをリクエストするため、もう一度試すことができます。

  オーディエンスエージェントは、生成されたオーディエンス式をオーディエンスとして自動的に保存しません。 オーディエンスを保存するには、プロンプトエリアの外にある[!UICONTROL Create] ボタンをクリックする必要があるので、保存しない変更を取り消すことができます。

オーディエンスのプロンプトを最適化する方法について詳しくは、「[&#x200B; オーディエンス概要の作成に関するベストプラクティス &#x200B;](#audience-brief-best-practices)」を参照してください。

<!--
 I think these are happening later:

DSP uses "smart" defaults based on the user's previous audiences (all user-created audiences or only ones created via AI prompting?)

you can use a predefined prompt (fill in the blanks, and some fields might have selectors where you can choose values)

Over time, DSP XXXX defaults [clarify this]

 onsider starting by asking for a general template, which contains placeholder values that you can replace with your desired values. The default template is something like "Create a xxx with NNN xxx."

you can give thumbs up or down to [what exactly?]. Verify what info is carried over from session to session and what starts from scratch.

-->

### プロンプトに含めることができないものは何か？

* 既存のオーディエンス式への参照。

* 英語以外の言語のテキスト。

### オーディエンスエージェントの応答の例と返信方法

オーディエンスエージェントがユーザーからの応答を必要とする場合、リクエストのキーワードを使用するか、一般的な類義語を使用して返信できます。

#### 質問をするオーディエンスエージェント

`If you are okay with the proposed expression, I can start searching third party segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

あなたの肯定的な返信：「続行」、「OK」、「OK」、「はい」または他の類似の単語

また、リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

#### 複数のオプションから選択するよう求めるオーディエンスエージェント

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

返信：`1`、`proceed`、`2`、`maximum reach`など。

また、リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

## オーディエンス概要の作成に関するベストプラクティス {#audience-brief-best-practices}

オーディエンス概要は、施策のターゲットオーディエンスを定義する戦略的な文章です。 DSPのオーディエンス担当者は、綿密に作成されたブリーフをもとに、最も関連性の高いセグメントを特定し、ターゲットを絞ったオーディエンスを作成できます。

### 効果的なオーディエンスブリーフの要素

オーディエンス属性の種類を、次のリストからできるだけ多く含めるようにしましょう。 除外する属性を具体的に設定する。

<!--
 What about these:

* Device specifications
* Presence in audiences from specific third-party data providers
* Presence of a universal ID
* Target cost per thousand (CPM) impressions or a total target cost

-->

* **デモグラフィック**

  年齢層、性別、配偶者の有無、世帯構成（家族の規模、子供の存在、多世代世帯）などの属性が含まれます。

* **社会経済指標**

  世帯収入（HHI）バンド、学歴、職業/役職、雇用状況、および住宅所有状況を通じて財務能力を確立します。

* **地理的パラメーター**

  国/国、地域（EMEA、APAC、NA）、人口密度（都市部/郊外/農村部）を含む場所の範囲を定義します。

* **興味関心と親和性**

  趣味（スポーツ、アート、アウトドア活動）、メディア消費パターン、ブランド好感度、ライフスタイル活動（旅行、食事、エンターテイメント）などの情熱や嗜好を特定できます。

* **心理的特性**

  目標（ステータスを求める、自己改善）、コアバリュー（持続可能性、イノベーション、伝統）、パーソナリティ特性（リスク担当者、アーリーアダプター）、購買意欲など、マインドセットと価値観を把握します。

* **行動シグナル**

  購入行動（ショッピング頻度、チャネルの好み、ブランドロイヤルティ）、オンライン行動（web サイトへの訪問、コンテンツのエンゲージメント、ソーシャルメディアでの行動）、オフライン行動（店舗への訪問、イベントへの参加、メンバーシップ）などの観察可能なアクション。

* **市場内インテント**

  調査中の製品/サービスのカテゴリー、購入スケジュール（即時、短期的、長期的）、購入を決定する要因となる関連するライフイベントを通じて、購入の準備状況を特定します。

* **ライフステージ**

  現在の段階の理解には、キャリアステージ（学生、初級、中級、幹部、退職）、家族ステージ（新婚、新しい両親、空のネスター）、および主要な人生の移行が含まれます。

### 見込み顧客開拓キャンペーン向けの構造化されたオーディエンス概要の例

プレミアム食事キット サブスクリプションサービスの認知と試用版を促進するキャンペーンの強力なオーディエンスブリーフの例を次に示します。

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [再利用可能なオーディエンスを複製](/help/dsp/audiences/reusable-audience-duplicate.md)
>* [再利用可能なオーディエンスの編集](/help/dsp/audiences/reusable-audience-edit.md)
>* [再利用可能なオーディエンスに関する詳細を表示](/help/dsp/audiences/reusable-audience-view-details.md)
>* [再利用可能なオーディエンスを共有](/help/dsp/audiences/reusable-audience-share.md)
>* [再利用可能なオーディエンスの書き出し](/help/dsp/audiences/reusable-audience-export.md)
>* [再利用可能なオーディエンスのセグメントキーをクリップボードにコピー](/help/dsp/audiences/reusable-audience-clipboard.md)
>* [再利用可能なオーディエンスを削除](/help/dsp/audiences/reusable-audience-delete.md)
