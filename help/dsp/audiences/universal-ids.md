---
title: ユニバーサル IDのアクティブ化のサポート
description: ユニバーサル ID セグメントのインポート、ユニバーサル IDの追跡のためのカスタムセグメントの作成、ファーストパーティセグメント内の他のユーザーIDのクッキーレスターゲティングのためのユニバーサル IDへの変換のサポートをご紹介します。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 2dddf3560e1f98dab7158c28625bcd54b4efbdb2
workflow-type: tm+mt
source-wordcount: '1513'
ht-degree: 0%

---

# ユニバーサル IDのアクティブ化のサポート

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta機能*

DSPは、DSPでサポートされているデジタル形式をまたいで、クッキーレスのシングルデバイス（クロスデバイスではなく）ターゲティングを行うためのピープルベースのユニバーサル IDをサポートしています。

* [!DNL LiveRamp] [!DNL RampIDs] ダッシュボードを使用して、認証済み[[!DNL LiveRamp] [!DNL Connect]]を手動でDSPに直接送信できます。 「[認証済みセグメントを [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)から手動で読み込む」を参照してください。

* DSPは、Customer Data Platform （CDP）内に構築されたファーストパーティセグメントを取り込み、[!DNL LiveRamp] [!DNL RampIDs]および[!DNL Unified ID 2.0 (UID2.0)]のIDに変換できます。 サポートされている顧客データプラットフォームとユーザーIDのタイプ、サポートされている各ユニバーサル ID タイプで使用できる機能、および関連するワークフローについて詳しくは、「[ ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)」を参照してください。

* ID5 ユニバーサル IDに関連付けられたユーザーを追跡するカスタムセグメントを作成できます。このユーザーは、デスクトップおよびモバイルデバイスの広告に表示され、特定のweb ページにアクセスします。 ID5は、確率的モデルを使用して、様々なユーザー信号とブラウザー信号から導き出されたIDを割り当てます。 手順については、「[ カスタムセグメントの作成と実装](/help/dsp/audiences/custom-segment-create.md)」を参照してください。

* 一部のベンダーのサードパーティセグメントでは、Cookieやデバイス IDによって追跡されたユーザーに加えて、ユニバーサル IDが自動的に含まれる場合があります。 例えば、[!DNL Eyeota]のセグメントにはID5 IDが自動的に含まれ、[!DNL Lotame]のセグメントにはUID 2.0 IDが含まれる場合があります。 セグメントの詳細には、各タイプのサイズが含まれます。 セグメント名の横に記載されている各セグメントの通常の使用料が適用されます。ID5 IDに追加料金は発生しません。

## ユニバーサル ID タイプによるレポート

* **カスタムレポート：** ユニバーサル ID タイプ別のコスト、インプレッション、クリック、コンバージョン、頻度データは、カスタムレポートで利用できます。

* **[!DNL Analytics]件のレポート：**&#x200B;必要なすべての手順を実装した[[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md)の広告主は、[!DNL Analytics]のユニバーサル ID タイプによるビュースルーコンバージョンを確認できます。

  >[!IMPORTANT]
  >
  >コンバージョンのアトリビューションを適切に行うには、広告のクリックスルーURLに[EF IDとAMO ID](/help/integrations/analytics/ids.md)の両方が含まれていることを確認します。

* **セグメントの詳細：**&#x200B;すべてのセグメントタイプについて、セグメントの詳細には、ユニバーサル ID タイプと、Cookieまたはデバイス IDで追跡されたデバイスタイプによるオーディエンスサイズが含まれます。

## プレースメントでユニバーサル ID オーディエンスをターゲットにする方法

>[!NOTE]
>
>ライブプレースメントでターゲット ID タイプを変更することはできません。 必要に応じて、ライブプレースメントを複製し、新しいプレースメントでターゲット ID タイプを変更できます。

新しいプレースメント、スケジュール済みプレースメントまたは一時停止プレースメントで、次の操作を行います。

1. 「[!UICONTROL Geo-Targeting]」セクションで、ターゲットとする地理的区分を指定します。 各ユニバーサル ID パートナーは、特定の地域でのみユーザーのターゲティングを許可し、適格なID タイプのみが[!UICONTROL Targeting]設定で使用できます。

1. [!UICONTROL Audience Targeting] セクションで、次の操作を行います。

   1. [!UICONTROL Included Audiences]設定で、ユーザーデータがユニバーサル IDに変換されたセグメントを選択します。

      必要に応じて、さらにセグメントを含めることができます。

   1. [!UICONTROL Targeting]設定で：

      1. ターゲットにするユニバーサル ID タイプを選択します。

         設定には、サブオプション「[!UICONTROL Legacy IDs]」、「[!UICONTROL Universal ID]」、「[!UICONTROL ID5]」を含むオプション「[!UICONTROL RampID]」と「[!UICONTROL Unified ID2.0]」が含まれます。 選択した地理的目標によって、使用可能なサブオプションが決まります。

         「[!UICONTROL Legacy IDs]」と「[!UICONTROL Universal ID]」の両方を選択できますが、1つのプレースメントにつき1種類のユニバーサル IDのみを選択できます。 レガシーIDとユニバーサル IDの両方を選択すると、入札設定がユニバーサル IDに与えられます。

      1. （必要に応じて）ユニバーサル IDを使用するための利用規約に同意します。

         データを新しいID タイプに変換する前に、DSP アカウントのユーザーが利用規約に同意する必要があります。 この条件は、IDの種類、アカウントごとに1回のみ受け入れられる必要があります。

「[配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)」を参照してください。

## テストとデータ検証のベストプラクティス

Adobe Analytics measurementが利用可能な[!DNL RampID] ベースのセグメントとID5 ベースのセグメントに対して、次のベストプラクティスを使用します。

* セグメントをアクティブ化してから約24時間後、[!UICONTROL Audiences] > [!UICONTROL All Audiences]の範囲内で、セグメントの変換済みID数を確認します。 ID数が予期しない場合は、Adobe アカウントチームにお問い合わせください。

  セグメント数の違いについて詳しくは、「[ メール IDとユニバーサル IDの間のデータの相違](#universal-ids-data-variances)」を参照してください。

* 既存のパッケージやプレースメントは変更しないでください。 ただし、ユニバーサル IDをテストするための増分予算がない場合は、テストに予算を割り当てるために元の予算を削減します。

* 元のパッケージとプレースメントをコピーし、テストのサイズに基づいて予算を調整し、[!DNL RampID] ベースのセグメント （認証済みユーザーの場合）またはID5 ベースのセグメント （未認証ユーザーの場合）を使用するようにオーディエンスを変更し、新しいパッケージとプレースメントが完全な予算を費やしていることを確認します。

   * ユニバーサル ID ベースのセグメントのパフォーマンスと、Cookieやモバイル広告IDなどの他のオーディエンス IDをターゲットとするプレースメントのパフォーマンスを比較するには、別のユニバーサル ID ベースのプレースメントと従来のID ベースのプレースメントを使用したキャンペーンを作成します。

     包括的なリターゲティングテストでは、認証済みユーザーのRampIDと未認証ユーザーのID5の両方をターゲットにします。

     最も優れたパフォーマンスを得ることが、最初の比較となるわけではありません。 その代わりに、どのIDが適切に拡張されているかを判断し、後で最適化や予算配分に役立てることができます。 長期的な目標は、Cookieが廃止されたときに失われたインプレッションとサイトトラフィックを補うことです。

   * ブラウザーのリーチ全体を比較するには、ユニバーサル ID ベースのセグメントと従来のID ベースのセグメントを同じプレースメントでターゲットにします。 キャンペーン予算を分割する必要がない点を除いて、以前のユースケースと同じキャンペーン設定を使用します。

     入札設定はユニバーサル IDに与えられますが、ユニバーサル IDが使用できない場合はレガシーIDが入札を受け取ります。 さまざまなブラウザー（Chrome、Safari、Mozillaなど）でのリーチを比較してください。

     >[!NOTE]
     >
     >頻度の上限は、個々のIDに適用されます。 ユーザーが複数のID タイプを持っている場合、そのユーザーに期待よりも多くリーチできる可能性があります。

* 認証されたオーディエンスセグメントのリーチは、Cookie ベースのセグメントのリーチよりも自然に小さく、追加のターゲティングオプションを使用すると、リーチがさらに減少することを忘れないでください。 詳細なターゲティングを使用する場合は、特に複数のターゲットをAND ステートメントで結合する場合は、慎重に行う必要があります。

## メール IDとユニバーサル ID間のデータの相違 {#universal-ids-data-variances}

このセクションは、ユニバーサル IDに変換されるメール IDにのみ適用されます。

### 許容レベルの差異

ハッシュ化された電子メールアドレスのユニバーサル IDへの翻訳率は90%を超える必要があります。特に[!DNL RampIDs]の翻訳率は、ハッシュ化された電子メールアドレスがすべて一意である場合は95%になります。 例えば、顧客データプラットフォームから100個のハッシュ化されたメールアドレスを送信する場合、それらのメールアドレスは少なくとも95 [!DNL RampIDs]または90種類以上のユニバーサル IDに変換する必要があります。 翻訳率が低い場合は、問題があることを示している可能性があります。 考えられる説明については、「[差異の原因] （#universal-ids-data-variances-causes」を参照してください。

[!DNL RampIDs]の場合、翻訳率が70%未満の場合は、Adobe アカウントチームに問い合わせて詳細を確認してください。

### 差異の原因 {#universal-ids-data-variances-causes}

* すべてのセグメント：

  セグメントからデバイスへのカウントは、誤差の分散が+/- 5%の確率的モデルを使用します。 つまり、オーディエンスサイズを5%過大評価したり、過小評価したりする可能性があります。

* ハッシュ化されたメール IDが[!DNL RampIDs]に変換されました：

   * 複数のプロファイルが同じメール IDを使用する場合、DSP セグメント数は、CDP内のプロファイル数よりも少ない可能性があります。 例えば、Adobe Photoshopでは、1つの電子メール IDを使用して、会社アカウントと個人アカウントを作成できます。 しかし、両方のプロファイルが同じ人物に属している場合、プロファイルは1つのメール IDにマッピングされ、対応する1つの[!DNL RampID]にマッピングされます。

   * [!DNL RampID]を新しい値にアップグレードできます。 [!DNL LiveRamp]が電子メール IDを認識しないか、データベース内の既存の[!DNL RampID]にマッピングできない場合は、新しい[!DNL RampID]を電子メール IDに割り当てます。 将来的には、電子メール IDを別の[!DNL RampID]にマッピングしたり、同じ電子メール IDに関する詳細情報を収集したりできる場合、[!DNL RampID]を新しい値にアップグレードします。 [!DNL LiveRamp]は、このアクションを「派生」から「維持」へのアップグレード [!DNL RampID]と呼んでいます。 [!DNL RampID]ただし、DSPでは、派生と維持された[!DNL RampIDs]の間にマッピングが取得されないため、以前のバージョンのRampIDをDSP セグメントから削除できません。 この場合、セグメント数はプロファイル数を超えることができます。

     例：ユーザーが[!DNL Adobe] web サイトにログインし、Photoshop ページにアクセスします。 [!DNL LiveRamp]に電子メール IDに関する既存の情報がない場合は、派生した[!DNL RampID]を割り当てます（例：D123）。 15日後、ユーザーは同じページにアクセスしますが、[!DNL LiveRamp]はその15日間に[!DNL RampID]をアップグレードし、[!DNL RampID]をM123に再割り当てしました。 Customer Data Platformのセグメント「Photoshop Enthusiast」には、ユーザー用のメール IDが1つしかありませんが、DSP セグメントには、D123とM123の2つのRampIDがあります。

## トラブルシューティング

ユーザー数が表示されない場合、またはオーディエンスサイズが小さい場合は、次の点を確認してください。

* [!DNL Flashtalking]または[!DNL Google Campaign Manager 360]個の広告を使用する場合は、広告のクリックスルーURLに正しいマクロが追加されていることを確認してください。 [[!DNL Flashtalking] ads](/help/integrations/analytics/macros-flashtalking.md)と[[!DNL Google Campaign Manager 360] ads](/help/integrations/analytics/macros-google-campaign-manager.md)のマクロを参照してください。

* オンサイトのイベントや広告露出と一致するように、ユニバーサル ID パートナー固有の正しいコードをweb サイトに実装する必要があります。 必要に応じて、[!DNL LiveRamp]または[!DNL ID5]担当者と連携してください。

* （[!DNL RampIDs]および[!DNL UID 2.0] IDの場合） [DSP データソースが正しく設定されていること](/help/dsp/audiences/sources/source-manage.md#source-settings)を確認し、生成されたオーディエンスセグメントにユーザーカウントが入力されていることを確認します。

* リーチが予想を下回っている場合は、オーディエンスセグメントロジックが詳細でないことを確認します。

* キャンペーン、パッケージ、プレースメントの設定が正しいことを確認してください。<!-- wording-->

問題が解決しない場合は、Adobe アカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [ オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](/help/dsp/audiences/sources/source-manage.md)
>* [ カスタムセグメントを作成して実装](/help/dsp/audiences/custom-segment-create.md)
>* [認証済みセグメントを [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)から手動でインポートします
>* [ オーディエンス管理について](/help/dsp/audiences/audience-about.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
