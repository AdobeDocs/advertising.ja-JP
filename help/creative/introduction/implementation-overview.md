---
title: Adobe Advertising Creative実装の概要
description: ' [!DNL Creative] を実装するための基本ワークフローについて説明します。'
feature: Creative Introduction
source-git-commit: fd925c641bef7953aea50813725252c3913757fa
workflow-type: tm+mt
source-wordcount: '863'
ht-degree: 0%

---

# Adobe Advertising Creative実装の概要

*クローズドベータ版*

<!-- CLARIFY HOW "ad" and "creative" are delineated, if they are. If they're not, why do we have different terms scattered around? -->

[!DNL Creative] オペレーションチームは各広告主と連携して、クリエイティブおよびクリエイティブエクスペリエンスを設定します。具体的には、DSP内で広告エクスペリエンスを広告として実装するか、サードパーティの広告タグをチームに提供して実装し、初期コスト、クリック数およびコンバージョンデータを検証します。

継続的に、Adobeアカウントチーム、エージェンシーチームまたは広告主（service level agreementの条件による）は、各エクスペリエンスをモニタリングし、広告主の目標を達成するために必要に応じて編集する必要があります。

## [!DNL Creative] Campaign <!-- Experiences? "Campaigns" may be confusing now. --> ークフローの初期設定タスク

実装チームや代理店が協力して、以下の作業を行います。

1. パーソナライゼーションの目標（予測やリターゲティングのために広告をパーソナライズするかどうかなど）、使用可能なすべてのファーストパーティ、セカンドパーティ、サードパーティのデータ（クリエイティブアセット、オーディエンスセグメント、CRM データ <!-- used how/where? --> ースなど）および目標達成のための戦略を定義します。

1. （新しい広告主アカウント）管理アカウントを設定します。

   1. [!DNL Creative]<!-- and/or DSP? --> に対して広告主のアカウントを設定し、Advertising検索でアカウントを作成します。

      広告主がDSPのお客様でなくても、[!DNL Creative] アカウントの設定はAdvertising DSP内で行えます。

      同様に、広告主が [!DNL Search] 顧客でない場合でも、[!DNL Search] アカウントは、コンバージョントラッキングタグの作成と、[!DNL Creative] でのコンバージョン列の設定に使用されます。

   1. （必要に応じて）広告主がクリエイティブと広告エクスペリエンスを表示および管理し、レポートを生成するためのユーザーアカウントを作成します。

1. （オプション）クリエイティブのターゲットとして含めるファーストパーティオーディエンスセグメントを作成する場合は、次のいずれかの方法でタグを作成します。

   * [ リターゲティングピクセルを作成 ](/help/creative/pixels/retargeting-pixel-manage.md) して、特定のランディングページまたはコンバージョンページに対して特定の属性を持つ訪問者に広告をリターゲットし、関連する web ページに挿入するタグを生成します。

   * （DSPを使用する広告主）DSP内で [ カスタムオーディエンスセグメントの作成 ](/help/dsp/audiences/custom-segment-create.md) を実行して、特定のランディングページまたはコンバージョンページへのすべての訪問者をトラッキングし、関連する web ページに挿入するタグを生成します。

   どちらのタイプのタグも画像タグで、エンドユーザーには表示されない 1 ピクセル x 1 ピクセルの透明な画像（ピクセル）が、追加先の web ページに表示されます。 後から、特定のリターゲティングピクセルまたはセグメントをターゲット設定するように広告エクスペリエンスのクリエイティブを設定できます。これにより、関連する広告要素は、そのピクセルまたはセグメントに関連付けられたサイトページに以前に訪問したユーザーにのみ表示されます。

   広告主の IT 部門またはその他のグループは、タグのデプロイメントをスケジュールするか、知らせる必要がある場合があります。

   **メモ：** Adobe Audience ManagerおよびAdobe Analyticsのファーストパーティオーディエンスをクリエイティブターゲットとして使用することもできます。 訪問者が [!DNL Analytics] から共有されるオーディエンスの資格を得ると、その情報は [!DNL Creative] で約 24～48 時間でアクション化できます。<!--Still true? And what about AAM and DSP? -->

1. 広告目標に基づいて広告エクスペリエンスを設定します。

   * **自動処理ワークフロー：**[!DNL Creative] の運用チームは、広告テンプレートとデータフィードを使用して、組織の動的広告を作成できます。

     詳しくは、Adobeアカウントチームにお問い合わせください。

     <!-- LATER, in a later phase: (Advertisers with Adobe Experience Manager; optional) Configure access to image assets in the Experience Manager account. -->

   * **手動のワークフロー：** 広告エクスペリエンスを手動で設定する：

      1. エクスペリエンスで使用するクリエイティブの設定：

         * [!DNL Creative] がホストするクリエイティブの場合は、それらをアップロードします。<!-- Add x-ref and reword if necessary to cover all cases -->

         * サポートされているサードパーティの広告サーバーでホストされているクリエイティブの場合は、[ クリエイティブファイルを指します ](/help/creative/creative-libraries/creative-third-party-manage.md)。

      1. （任意） [ クリエイティブをバンドルにグループ化 ](/help/creative/creative-libraries/bundle-manage.md) し、1 つの手順でエクスペリエンスに添付できます。

      1. クリエイティブとオプションの広告ターゲットを [ 広告エクスペリエンス ](/help/creative/experiences/experience-about.md).<!-- maybe change x-ref once that chapter is done --> として順序付けます。

     広告ターゲットには、[!DNL Creative] で作成したリターゲティングピクセル、Adobe Experience Cloudのオーディエンスセグメント（DSP、Audience Manager、[!DNL Analytics] など）、地理ターゲット、web ページ上の特定のデータトリガー（SKU=01234567890123 や買い物かご=空など）が含まれます。&lt;! – 使用可能なオーディエンスセグメントが表示されず、radius ターゲット（機能しない）は表示されますが、他のジオターゲットは表示されません。これらをすべて確認してください。—>

1. 広告エクスペリエンス用のコンバージョントラッキングの設定：


コンバージョントラッキングの設定 実装によっては、の追加が含まれる場合があります。
広告主の web ページへのコンバージョントラッキングタグおよび/または日次を設定
広告主が個別に収集したコンバージョンデータのフィードドロップ。


Advertising Cloud内で、Advertising Cloud コンバージョントラッキングタグを生成できます
Adobeの Dynamic Tag Manager （旧称 Dynamic Tag Manager）内で、または検索します。
メモ：画像タグではなく、JavaScript コンバージョンタグを使用する必要があります。


広告主の IT 部門またはその他のグループは、スケジュールを設定するか、情報を提供する必要がある場合があります
について説明します。


（オプション）Advertising Cloud Search内で、各コンバージョンをおこないます（トランザクションプロパティ）
データビューおよびレポートで個々の列セットとして使用できます。


コンバージョン（トランザクションプロパティ）は、Advertising Cloud Searchの次の場所にリストされます。
1 つ以上のコンバージョンイベントがトラッキングされました。


特定の指標を使用可能にしない場合、すべてのコンバージョンが統合されます
1 つの「コンバージョン」列セットで。


トラッキングされるデータを検証します。


（任意）指定したメールアドレスへの予定レポートの配信を設定します。


手順については、ヘルプの「レポート」の章を参照してください。


Advertising Cloud DSPまたは別のDSPで広告キャンペーンを設定し、JavaScriptを提供します。
または広告主向けの広告エクスペリエンスの iframe タグを提供します。広告主は次の形式で実装できます。
DSPでのサードパーティ広告。


定義済みリストを表示して、完了した広告エクスペリエンスのパフォーマンスを監視します
個々のエクスペリエンスのパフォーマンスの詳細またはカスタムパフォーマンスレポートの作成。


（必要に応じて）パフォーマンスと更新されたメッセージに基づいて広告エクスペリエンスを更新します。






>[!MORELIKETHIS]
>
>* [Adobe Advertising Creativeについて ](/help/creative/introduction/creative-about.md)
>* [ ユーザーインターフェイスの編成方法 ](/help/creative/introduction/ui.md)
