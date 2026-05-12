---
title: 再利用可能なオーディエンスの作成
description: オーディエンスセグメントやその他の保存されたオーディエンスで構成される再利用可能なオーディエンスを作成する方法について説明します。 オプションで、AI支援オーディエンスエージェントを使用して、自然言語プロンプトでターゲットオーディエンスを説明します。エージェントは、サードパーティセグメントを提案し、ターゲットまたは除外として使用するオーディエンス式を構築します。
feature: DSP Audiences
exl-id: 5f4a0abb-c285-4452-a6c3-a91d5281df9b
TQID: https://experienceleague.adobe.com/KhAxVTvMx4yBz3tfDtng3nOur2IodZAFFHMUQM1lKhQ
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
source-git-commit: a4b509995f362ed81e00485409b0c729b5130e35
workflow-type: tm+mt
source-wordcount: 1667
ht-degree: 0%

---

# 再利用可能なオーディエンスの作成

<!-- "Saved audience" is used in UI (where?), but "saved" is a state, not a type. "Reusable audience" sounds better in a description. "Audience template" isn't right, either, since it implies you can edit it on the fly to create a new, different audience. Some other term? -->

再利用可能なオーディエンスを保存および管理できます。これは、オーディエンスセグメントのグループであり、その他の保存されたオーディエンスも含みます。これらのオーディエンスは、複数のプレースメントのターゲットまたは除外として使用できます。 オーディエンスを手動で作成することも、AI支援のオーディエンスエージェントを使用して、記載された要件に従って利用可能なすべてのファーストパーティセグメントとサードパーティセグメントを使用して、新しい再利用可能なオーディエンスを生成することもできます。

>[!NOTE]
>
>（DSPがハッシュ化されたメール IDをLiveRamp RampID セグメントに変換する広告主）アクティブなプレースメント、スケジュール済みプレースメント、または一時停止されたプレースメントにアタッチされていないファーストパーティのRampID セグメントは一時停止されます。 セグメントは、「自動一時停止」としてセグメントリストに表示されます。

## 再利用可能なオーディエンスを手作業で作成する

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

1. [!UICONTROL New Audience]設定で：

   1. 一意の&#x200B;**[!UICONTROL Audience Name]**&#x200B;を入力してください。

   1. （オプション）オプションの選択を&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;に解除します。

      オーディエンスを共有すると、そのオーディエンスは、アカウント内のすべての広告主に対してターゲットまたは除外として使用できるようになります。 ただし、オーディエンス内の個々のセグメントは、セグメントを共有するユーザーのみが使用できます。 例えば、Adobe Analytics セグメントを含むオーディエンスを、同じ[!DNL Analytics] アカウントにマッピングされていない広告主と共有する場合、そのセグメントはその広告主のそのオーディエンスでプレビューされません。 その広告主が利用できるセグメントのみが、オーディエンスでプレビューされます。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. 右側のパネルの「**[!UICONTROL Switch to manual mode]**」ボタンをクリックします。

   AI オプションがデフォルトです。

1. オーディエンスの構築：

   >[!NOTE]
   >
   >オーディエンスを作成すると、右側のパネルに詳細な[&#x200B; オーディエンスサイズデータ &#x200B;](audience-about.md)が更新されます

   * [[!UICONTROL Third Party Segments]、[!UICONTROL First Party Segments]、[!UICONTROL Adobe Segments]、[!UICONTROL Custom Segments]、および[!UICONTROL Saved Audiences] タブ &#x200B;](audience-settings.md)で使用可能なセグメントを使用して、セグメントロジックを手動で作成するには、次の操作を行います。

      * （オプション）セグメント名、説明、またはパスを検索します。

        検索結果には、使用した用語にもとづいたセグメントが表示されます。 複数の用語を入力すると、1つのセグメントに対するすべての用語が見つかる必要があります。

      * 最初のセグメントを追加するには、左側のパネルでセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

      * 既存のセグメントグループにセグメントを追加するには：

         1. 右側のパネルでセグメントグループをクリックします。

         1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

            *[!UICONTROL Exclude All]*&#x200B;は、最初のセグメント グループでは使用できません。 除外のみを含むオーディエンスの場合は、このオーディエンスを&#x200B;*[!UICONTROL Include Any]*&#x200B;として作成し、プレースメント内の除外オーディエンス メニューからそのオーディエンスを選択します。

         1. 左側のパネルで新しいセグメントを見つけ、セグメント名の横にあるチェックボックスを選択します。

            セグメントグループは、新しいセグメントで自動的に更新されます。

      * 新しいセグメントグループを追加するには：

         1. 右側のパネルで「**[!UICONTROL + New Group]**」をクリックします。

            1. （オプション）必要に応じて、前のグループと新しいグループの間のロジックを&#x200B;*[!UICONTROL And]*&#x200B;または&#x200B;*[!UICONTROL Or]*&#x200B;に変更します。

            1. 左側のパネルで新しいグループのセグメントを探し、セグメント名の横にあるチェックボックスを選択します。

            1. （オプション）必要に応じて、グループロジックを&#x200B;*[!UICONTROL Include Any]*、*[!UICONTROL Include All]*&#x200B;または&#x200B;*[!UICONTROL Exclude All]*&#x200B;に変更します。

   * 既存のオーディエンスからセグメントロジックを使用するには：

      1. 次のいずれかの方法で、既存のオーディエンスからセグメントロジックをコピーします。

         * すべてのオーディエンス ビューで、オーディエンス行の上にカーソルを置き、**[!UICONTROL More]** > **[!UICONTROL Copy to Clipboard]**&#x200B;をクリックします。

         * 既存のオーディエンスの設定で、セグメントロジックパネルの上部にある「**[!UICONTROL More]**」 > 「**[!UICONTROL Copy to Clipboard]**」をクリックします。

         * テキストエディターで、英数字のセグメント IDと[&#x200B; ブール構文](audience-segment-logic-syntax.md)を使用してセグメントロジックを手動で作成し、クリップボードにコピーします。

      1. **[!UICONTROL paste in an audience rule to begin building]**&#x200B;をクリックし、既存のセグメントロジックを入力フィールドに貼り付け、**[!UICONTROL Apply]**&#x200B;をクリックします。

         >[!NOTE]
         >
         >オーディエンスにセグメントロジックが既に含まれている場合、新しいセグメントロジックにペーストすると、既存のロジックが上書きされます。

1. **[!UICONTROL Create]**&#x200B;をクリックします。

## 生成AIを使用して再利用可能なオーディエンスを作成する

*Beta機能*

*英語のみサポート*

>[!NOTE]
>
>この機能はベータモードで、一部変更される可能性があります。 オーディエンスを作成してプレースメントに使用する前に、生成されたオーディエンス式が必要なオーディエンスを表していることを確認してください。

<!-- Later:  Audiences built using generative AI have the indicator [icon] in **[!UICONTROL Audiences] > [!UICONTROL All Audiences]**. -->

1. メインメニューで、**[!UICONTROL Audiences]** > **[!UICONTROL All Audiences]**&#x200B;をクリックします。

1. データテーブルの上で、**[!UICONTROL Create]**&#x200B;をクリックします。

1. [!UICONTROL New Audience]設定で：

   1. 一意の&#x200B;**[!UICONTROL Audience Name]**&#x200B;を入力してください。

   1. （オプション）オプションの選択を&#x200B;**[!UICONTROL Share with all advertisers in my account]**&#x200B;に解除します。

      オーディエンスを共有すると、そのオーディエンスは、アカウント内のすべての広告主に対してターゲットまたは除外として使用できるようになります。 ただし、オーディエンス内の個々のセグメントは、セグメントを共有するユーザーのみが使用できます。 例えば、Adobe Analytics セグメントを含むオーディエンスを、同じ[!DNL Analytics] アカウントにマッピングされていない広告主と共有する場合、そのセグメントはその広告主のそのオーディエンスでプレビューされません。 その広告主が利用できるセグメントのみが、オーディエンスでプレビューされます。

   1. **[!UICONTROL Save]**&#x200B;をクリックします。

1. オーディエンスの構築：

   1. 含めたり除外したりするオーディエンス特性を説明する1つ以上のプロンプトを入力します。 各プロンプトを送信するには、![&#x200B; プロンプトを送信](/help/dsp/assets/submit-prompt.png " プロンプトを送信")をクリックします。

      詳しくは、「[&#x200B; プロンプトの作成](#writing-prompts)」および「[&#x200B; オーディエンス概要の作成に関するベストプラクティス &#x200B;](#audience-brief-best-practices)」を参照してください。

      該当する場合、担当者は、より効果的なオーディエンス概要の作成に役立つ追加のセグメントフィルターを提案します。 提案を承認または却下できます。

      オーディエンスエージェントが関連セグメントを見つけると、条件に基づいてブール値のオーディエンス式が作成されます。 また、オーディエンスを作成するための一致するセグメントを探す前に、承認を求めることもできます。 オプションで、リクエストを無視し、代わりに追加のオーディエンス条件を引き続き指定できます。

   1. オーディエンスエージェントがオーディエンスを適切に説明するオーディエンス式を提示したら、オーディエンスエージェントにオーディエンスの作成を続行するように指示します。

      「続行」、「OK」、「OK」、「はい」または他の類似する単語を入力できます。 エージェントは、各特性に対するすべての推奨セグメント（「親」など）をリストします。 任意の特性を展開すると、その特性に対して提案された個々のセグメントに関する詳細が表示されます。

   1. （必要に応じて）追加の基準を指定します。 オーディエンスエージェントが、すべての基準を満たすオーディエンス式を提示したら、オーディエンスエージェントにオーディエンスの組み立てを続行するように指示します。

      オーディエンスを組み立てるには、「続行」、「OK」、「はい」、または他の類似する単語を入力します。 エージェントは、各特性に対するすべての推奨セグメント（「親」など）をリストします。 任意の特性を展開すると、その特性に対して提案された個々のセグメントに関する詳細が表示されます。

1. 組み立てられたオーディエンスに満足したら、**[!UICONTROL Create]**&#x200B;をクリックして、指定したオーディエンスを作成します。

   >[!NOTE]
   >
   >Audience Agentを使用して後でオーディエンスを編集することはできません。 代わりに、[&#x200B; オーディエンス式を手動で編集します](/help/dsp/audiences/reusable-audience-edit.md)。

### プロンプトの作成の基本 {#writing-prompts}

<!-- Change heading level for this whole section to fit under AI procedure -->

#### プロンプトには何を含めるべきですか？

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
Consider starting by asking for what you should include.

you can give thumbs up or down to [what exactly?].

Verify what info is carried over from session to session and what starts from scratch.

-->

#### プロンプトに含めることができないものは何か？

* 既存のオーディエンス式への参照。

* 英語以外の言語のテキスト。

#### オーディエンスエージェントの応答の例と返信方法

オーディエンスエージェントがユーザーからの応答を必要とする場合、リクエストのキーワードを使用するか、一般的な類義語を使用して返信できます。

#### 質問をするオーディエンスエージェント

`If you are okay with the proposed expression, I can start searching segments for each of the traits (based on the search filters above), and assemble the matching segments into the audience. Would you like me to proceed?`

あなたの肯定的な返信：「続行」、「OK」、「OK」、「はい」または他の類似の単語

また、リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

##### 複数のオプションから選択するよう求めるオーディエンスエージェント

`Would you like to:`
`1) Proceed with this expression,`
`2) Get maximum reach alternatives, or`
`3) Modify the expression manually?`

返信：`1`、`proceed`、`2`、`maximum reach`など。

また、リクエストを無視して、代わりに追加のオーディエンス条件を引き続き指定することもできます。

### オーディエンス概要の作成に関するベストプラクティス {#audience-brief-best-practices}

オーディエンス概要は、施策のターゲットオーディエンスを定義する戦略的な文章です。 DSPのオーディエンス担当者は、綿密に作成されたブリーフをもとに、最も関連性の高いセグメントを特定し、ターゲットを絞ったオーディエンスを作成できます。

#### 効果的なオーディエンスブリーフの要素

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

#### 見込み顧客開拓キャンペーン向けの構造化されたオーディエンス概要の例

プレミアム食事キット サブスクリプションサービスの認知と試用版を促進するキャンペーンの強力なオーディエンスブリーフの例を次に示します。

`The target audience consists of adults aged 28-45 (60% female, 40% male) with household incomes of $85K or more, college-educated professionals living in the USA. Psychographically, they are health-conscious individuals who value convenience and quality, aspire to be home cooks, and are food enthusiasts seeking better work-life balance. They actively engage with cooking and culinary content, follow health and wellness trends, shop at farmers markets, and prefer organic foods. Behaviorally, they are online grocery shoppers who use subscription services, dine out at restaurants 2+ times per week, and engage with food content on social media. They are currently in-market for meal planning solutions and food subscription services, with many focused on weight management and healthy eating programmes. The audience includes young families with children and dual-income households, as well as career-focused professionals. The brief excludes current subscribers and those following vegan/vegetarian diets as the initial launch focuses on protein-centric meal plans.`

>[!MORELIKETHIS]
>
>* [&#x200B; オーディエンス管理について](audience-about.md)
>* [&#x200B; オーディエンス設定](audience-settings.md)
>* [&#x200B; オーディエンスセグメントロジックの構文](audience-segment-logic-syntax.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
>* [&#x200B; カスタムセグメントを作成して実装](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
