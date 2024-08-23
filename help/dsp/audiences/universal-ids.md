---
title: ユニバーサル ID の有効化のサポート
description: ユニバーサル ID セグメントを読み込むサポート、ユニバーサル ID を追跡するカスタムセグメントの作成、ファーストパーティセグメントの他のユーザー識別子をユニバーサル ID に変換してクッキーなしのターゲティングを行うサポートについて説明します。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 202f4ae8e6633672b7af12937f0b35da5052f7fc
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# ユニバーサル ID の有効化のサポート

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta機能*

DSPは、DSPでサポートされているデジタル形式をまたいで、クックレスのシングルデバイス（クロスデバイスではなく）ターゲティングを行うための、人物ベースのユニバーサル ID をサポートしています。

* 認証済みの [[!DNL LiveRamp] [!DNL RampIDs]] を、[!DNL LiveRamp] [!DNL Connect] ダッシュボードを使用して手動でDSPに直接送信できます。 「[ 認証済みセグメントの手動インポート  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)」を参照してください。

* DSPは、顧客データプラットフォーム（CDP）内で作成されたハッシュ化されたメール ID で構成されるファーストパーティセグメントを取り込み、[!DNL LiveRamp] [!DNL RampIDs] ID と [!DNL Unified ID 2.0 (UID2.0)] ID に変換できます。 サポートされる顧客データプラットフォーム、サポートされる各ユニバーサル ID タイプで使用可能な機能および関連ワークフローについて詳しくは、「[ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md) を参照してください。

* デスクトップやモバイルデバイスからの広告に晒され、特定の web ページを訪問するユーザーを対象として、ID5 ユニバーサル ID に関連付けられたユーザーを追跡するカスタムセグメントを作成できます。 ID5 は、確率的モデルを使用して、様々なユーザー信号およびブラウザー信号から派生した ID を割り当てます。 手順については、「[ カスタムセグメントの作成と実装 ](/help/dsp/audiences/custom-segment-create.md) を参照してください。

* 一部のベンダーのサードパーティセグメントには、Cookie やデバイス ID で追跡されるユーザーに加えて、ユニバーサル ID が自動的に含まれる場合があります。 例えば、[!DNL Eyeota] のセグメントには ID5 ID が自動的に含まれ、[!DNL Lotame] のセグメントにはUID2.0 ID が含まれる場合があります。 セグメントの詳細には、各タイプのサイズが含まれます。 セグメント名の横に記載されている各セグメントの通常の使用料金が適用されます。ID5 ID に対して追加料金は発生しません。

## ユニバーサル ID タイプ別のレポート

* **カスタムレポート：** コスト、インプレッション、クリック、コンバージョンおよび頻度データ（ユニバーサル ID タイプ別）を、カスタムレポートで使用できます。

* **[!DNL Analytics]レポート：** 必要なすべての手順を実装した [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を持つ広告主は、[!DNL Analytics] でユニバーサル ID タイプ別のビュースルーコンバージョンを確認できます。

  >[!IMPORTANT]
  >
  >適切なコンバージョンアトリビューションを行うには、広告のクリックスルー URL に [EF ID と AMO ID](/help/integrations/analytics/ids.md) の両方が含まれていることを確認してください。

* **セグメントの詳細：** すべてのセグメントタイプについて、セグメントの詳細には、ユニバーサル ID タイプ別のオーディエンスサイズや、Cookie またはデバイス ID で追跡されるデバイスタイプ別のオーディエンスサイズが含まれます。

## プレースメントでユニバーサル ID オーディエンスをターゲットにする方法

>[!NOTE]
>
>ライブプレースメントでターゲットの ID タイプを変更することはできません。 必要に応じて、ライブのプレースメントを複製し、新しいプレースメントでターゲットの ID タイプを変更できます。

新規、スケジュール済み、一時停止のプレースメントで、次の操作を行います。

1. [!UICONTROL Geo-Targeting] のセクションで、ターゲットにする地理的領域を指定します。 各ユニバーサル ID パートナーは、特定の地理的領域でのみユーザーのターゲティングを許可し、[!UICONTROL Targeting] 設定では適格な ID タイプのみを使用できます。

1. [!UICONTROL Audience Targeting] セクションで、次の操作を行います。

   1. [!UICONTROL Included Audiences] 設定で、ユーザーデータがユニバーサル ID に変換されたセグメントを選択します。

      必要に応じて、追加のセグメントを含めることができます。

   1. [!UICONTROL Targeting] の設定で、

      1. ターゲットにするユニバーサル ID タイプを選択します。

         設定には、オプション「[!UICONTROL Legacy IDs]」および「[!UICONTROL Universal ID]」が含まれます。これらのオプションには、サブオプション「[!UICONTROL ID5]」、「[!UICONTROL RampID]」、および「[!UICONTROL Unified ID2.0]」を含めることができます。 選択した地理的ターゲットによって、使用可能なサブオプションが決まります。

         「[!UICONTROL Legacy IDs]」と「[!UICONTROL Universal ID]」の両方を選択できますが、プレースメントごとに選択できるユニバーサル ID のタイプは 1 つだけです。 レガシー ID とユニバーサル ID の両方を選択する場合、入札の環境設定がユニバーサル ID に指定されます。

      1. （必要な場合）ユニバーサル ID を使用するためのサービス利用契約に同意します。

         データを新しい ID タイプに変換する前に、DSP アカウントのユーザーがサービス利用規約に同意する必要があります。 条件は、ID タイプごとに、アカウントごとに 1 回だけ受け入れられます。

「[ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)」を参照してください。

## テストとデータ検証のベストプラクティス

Adobe Analyticsが使用できる [!DNL RampID] ベースのセグメントと ID5 ベースのセグメントには、次のベストプラクティスを使用します。

* セグメントをアクティブ化してから約 24 時間後に、[!UICONTROL Audiences] > [!UICONTROL All Audiences] でセグメントの変換済み ID 数を確認します。 ID 数が予期しない場合は、Adobeアカウントチームにお問い合わせください。

  セグメント数がどのように変化する可能性があるかについて詳しくは ](#universal-ids-data-variances) 「[ メール ID とユニバーサル ID のデータの相違」を参照してください。

* 既存のパッケージやプレースメントを変更しないでください。 ただし、ユニバーサル ID をテストするための増分予算がない場合は、元の予算を減らしてテストに資金を供給します。

* 元のパッケージとプレースメントをコピーし、テストのサイズに基づいて予算を調整し、[!DNL RampID] ベースのセグメント（認証済みユーザーの場合）または ID5 ベースのセグメント（未認証ユーザーの場合）を使用するようにオーディエンスを変更し、新しいパッケージとプレースメントが完全な予算を費やしていることを確認します。

   * ユニバーサル ID ベースのセグメントのパフォーマンスと、Cookie やモバイル広告 ID などの他のオーディエンス識別子をターゲットとするプレースメントのパフォーマンスを比較するには、個別のユニバーサル ID ベースのプレースメントおよび従来の ID ベースのプレースメントを使用するキャンペーンを作成します。

     完全なリターゲティングテストを行うには、認証済みユーザーの RampID と未認証ユーザーの ID5 の両方をターゲットにします。

     最高のパフォーマンスを得ることが主な比較対象ではありません。 代わりに、どの ID が適切にスケーリングされているかを判断します。これにより、後で最適化と予算の割り当てが変わる可能性があります。 長期的な目標は、Cookie が非推奨になった場合に失われたインプレッションとサイトトラフィックを補うことです。

   * ブラウザーのリーチの合計を比較するには、ユニバーサル ID ベースのセグメントとレガシー ID ベースのセグメントを同じプレースメントでターゲットします。 キャンペーンの設定は前のユースケースと同じものを使用します。ただし、キャンペーンの予算を分割する必要はありません。

     入札の環境設定はユニバーサル ID に与えられますが、従来の ID はユニバーサル ID が使用できない場合に入札を受け取ります。 様々なブラウザー（Chrome、Safari、Mozilla を含む）でリーチを比較してください。

     >[!NOTE]
     >
     >フリークエンシーキャップは、個々の ID に適用されます。 ユーザーに複数の ID タイプがある場合、想定以上にそのユーザーに到達する可能性があります。

* 認証済みオーディエンスセグメントのリーチは、当然、cookie ベースのセグメントのリーチよりも小さくなり、追加のターゲティングオプションを使用するとリーチがさらに減少することに注意してください。 特に AND 文で複数のターゲットを結合するなど、詳細なターゲティングの使用には慎重に注意してください。

## メール ID とユニバーサル ID のデータの相違 {#universal-ids-data-variances}

### 許容可能な分散レベル

ハッシュ化されたメールアドレスのユニバーサル ID に対する翻訳率は、90% より大きい必要があります。ハッシュ化されたメールアドレスがすべて一意の場合、特に [!DNL RampIDs] の翻訳率は 95% である必要があります。 例えば、顧客データプラットフォームからハッシュ化されたメールアドレスを 100 個送信する場合は、少なくとも 95[!DNL RampIDs] 以上、それ以外の 90 種類以上のユニバーサル ID に翻訳する必要があります。 翻訳率が低い場合は、問題がある可能性があります。 考えられる説明については、「[ 相違の原因 ] （#universal-ids-data-variances-causes」を参照してください。

[!DNL RampIDs] しくは、翻訳率が 70% 未満の場合は、Adobeアカウントチームに問い合わせて詳細を確認してください。

### 差異の原因 {#universal-ids-data-variances-causes}

* すべてのセグメント：

  セグメント/デバイス数は、確率的モデルを使用します。このモデルのエラー分散は+/- 5% です。 つまり、オーディエンス数を 5% 過大評価または過小評価する可能性があります。

* ハッシュ化されたメール ID を [!DNL RampIDs] に変換しました：

   * 複数のプロファイルが同じメール ID を使用する場合、DSP セグメント数は、カスタマーデータプラットフォーム内のプロファイル数よりも少ない可能性があります。 例えば、Adobe Photoshopでは、1 つのメール ID を使用して会社アカウントと個人アカウントを作成できます。 ただし、両方のプロファイルが同じ人物に属する場合、プロファイルは 1 つのメール ID に、対応して 1 つの [!DNL RampID] ール ID にマッピングされます。

   * [!DNL RampID] は新しい値にアップグレードできます。 [!DNL LiveRamp] がメール ID を認識しない場合や、データベース内の既存の [!DNL RampID] にマッピングできない場合は、新しい [!DNL RampID] をメール ID に割り当てます。 今後、メール ID を別の [!DNL RampID] にマッピングしたり、同じメール ID に関する詳細情報を収集したりできるようになると、[!DNL RampID] を新しい値にアップグレードします。 [!DNL LiveRamp] では、このアクションを「派生」アクションから「メンテナンス済み」アクシ [!DNL RampID] ンへのアップグレ [!DNL RampID] ドと呼びます。 ただし、DSPは、派生 ID とメンテナンス [!DNL RampIDs] の間のマッピングを取得しないので、以前のバージョンの RampID をDSP セグメントから削除できません。 この場合、セグメント数はプロファイル数より多くなる可能性があります。

     例：あるユーザーが [!DNL Adobe] web サイトにログインし、Photoshopページにアクセスしました。 メール ID[!DNL LiveRamp] 関する既存の情報がない場合は、派生 [!DNL RampID] （例：D123）を割り当てます。 15 日後、ユーザーは同じページを訪問しますが、[!DNL LiveRamp] の 15 日間に [!DNL RampID] をアップグレードし、[!DNL RampID] を M123 に再割り当てしました。 顧客データプラットフォームの「Photoshop愛好者」のセグメントには、ユーザーのメール ID が 1 つしかありませんが、DSP セグメントには D123 と M123 の 2 つの RampID があります。

## トラブルシューティング

ユーザー数が表示されない場合や、オーディエンスサイズが小さい場合は、次の点を確認してください。

* [!DNL Flashtalking] または [!DNL Google Campaign Manager 360] の広告を使用する場合は、広告のクリックスルー URL に正しいマクロが追加されていることを確認します。 [[!DNL Flashtalking] ads](/help/integrations/analytics/macros-flashtalking.md) および [[!DNL Google Campaign Manager 360] ads](/help/integrations/analytics/macros-google-campaign-manager.md) マクロを参照してください。

* オンサイトのイベントと広告漏洩を照合するために、正しいユニバーサル ID パートナー固有のコードが Web サイトに実装されていることを確認します。 必要に応じて、[!DNL LiveRamp] または [!DNL ID5] の担当者に相談します。

* （[!DNL RampIDs] ID および [!DNL UID 2.0] ID の場合） [DSP データソースが正しく設定されていること ](/help/dsp/audiences/sources/source-manage.md#source-settings) および生成されたオーディエンスセグメントに対してユーザー数が入力されていることを確認します。

* リーチが予想を下回る場合は、オーディエンスセグメントロジックが精度が高すぎないことを確認します。

* キャンペーン、パッケージ、プレースメントの設定が正しいことを確認します。<!-- wording-->

問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](/help/dsp/audiences/sources/source-manage.md)
>* [ カスタムセグメントの作成と実装 ](/help/dsp/audiences/custom-segment-create.md)
>* [ 認証済みセグメントの手動インポート  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Audience Management について ](/help/dsp/audiences/audience-about.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
