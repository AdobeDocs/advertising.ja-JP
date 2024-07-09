---
title: ユニバーサル ID の有効化のサポート
description: ユニバーサル ID セグメントを読み込むサポート、ユニバーサル ID を追跡するカスタムセグメントの作成、ファーストパーティセグメントの他のユーザー識別子をユニバーサル ID に変換してクッキーなしのターゲティングを行うサポートについて説明します。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: 8a8f19c7db95c0eda05a3262eeaf4c8a0aeaaa64
workflow-type: tm+mt
source-wordcount: '1500'
ht-degree: 0%

---

# ユニバーサル ID の有効化のサポート

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*Beta機能*

DSPは、DSPでサポートされているデジタル形式をまたいで、クックレスのシングルデバイス（クロスデバイスではなく）ターゲティングを行うための、人物ベースのユニバーサル ID をサポートしています。

* 認証済み [[!DNL LiveRamp] [!DNL RampIDs]] を使用してDSPに直接アクセスします [!DNL LiveRamp] [!DNL Connect] ダッシュボード。 参照先」[認証済みセグメントの手動インポート： [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md).」と入力します。

* DSPは、顧客データプラットフォーム（CDP）内で作成されたハッシュ化されたメール ID で構成されるファーストパーティセグメントを取り込み、に変換できます [!DNL LiveRamp] [!DNL RampIDs] および [!DNL Unified ID 2.0 (UID2.0)] ID。 サポートされる顧客データプラットフォーム、サポートされる各ユニバーサル ID タイプで使用できる機能、関連するワークフローについて詳しくは、「」を参照してください[ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md).」と入力します。

* デスクトップやモバイルデバイスからの広告に晒され、特定の web ページを訪問するユーザーを対象として、ID5 ユニバーサル ID に関連付けられたユーザーを追跡するカスタムセグメントを作成できます。 ID5 は、確率的モデルを使用して、様々なユーザー信号およびブラウザー信号から派生した ID を割り当てます。 手順については、「」を参照してください[カスタムセグメントの作成と実装](/help/dsp/audiences/custom-segment-create.md).」と入力します。

* 一部のベンダーのサードパーティセグメントには、Cookie やデバイス ID で追跡されるユーザーに加えて、ユニバーサル ID が自動的に含まれる場合があります。 例えば、次からのセグメント： [!DNL Eyeota] からの ID5 ID およびセグメントを自動的に含めることができます [!DNL Lotame] uid2.0 の ID を含めることができます。 セグメントの詳細には、各タイプのサイズが含まれます。 セグメント名の横に記載されている各セグメントの通常の使用料金が適用されます。ID5 ID に対して追加料金は発生しません。

## ユニバーサル ID タイプ別のレポート

* **カスタムレポート：** コスト、インプレッション、クリック、コンバージョンおよび頻度データ（ユニバーサル ID タイプ別）を、カスタムレポートで使用できます。

* **[!DNL Analytics]レポート：** を使用した広告主 [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) 必要な手順をすべて実装しているユーザーは、でユニバーサル ID タイプ別のビュースルーコンバージョンを確認できます [!DNL Analytics].

  >[!IMPORTANT]
  >
  >適切なコンバージョンアトリビューションを得るには、広告のクリックスルー URL に次の両方が含まれていることを確認します。 [EF ID と AMO ID](/help/integrations/analytics/ids.md).

* **セグメント詳細：** すべてのセグメントタイプの場合、セグメントの詳細には、ユニバーサル ID タイプ別のオーディエンスサイズや、Cookie またはデバイス ID で追跡されるデバイスタイプ別のオーディエンスサイズが含まれます。

## プレースメントでユニバーサル ID オーディエンスをターゲットにする方法

>[!NOTE]
>
>ライブプレースメントでターゲットの ID タイプを変更することはできません。 必要に応じて、ライブのプレースメントを複製し、新しいプレースメントでターゲットの ID タイプを変更できます。

新規、スケジュール済み、一時停止のプレースメントで、次の操作を行います。

1. が含まれる [!UICONTROL Geo-Targeting] セクションで、ターゲットとする地理的領域を指定します。 各ユニバーサル ID パートナーは、特定の地理的領域でのみユーザーターゲティングを行え、で使用できるのは適格な ID タイプのみです [!UICONTROL Targeting] 設定。

1. が含まれる [!UICONTROL Audience Targeting] セクションで、次の操作を行います。

   1. が含まれる [!UICONTROL Included Audiences] 設定で、ユーザーデータがユニバーサル ID に変換されたセグメントを選択します。

      必要に応じて、追加のセグメントを含めることができます。

   1. が含まれる [!UICONTROL Targeting] 設定：

      1. ターゲットにするユニバーサル ID タイプを選択します。

         この設定には「」オプションが含まれています[!UICONTROL Legacy IDs]「」と「」に対して検査する値[!UICONTROL Universal ID],&quot; サブオプションを含めることができます&quot;[!UICONTROL ID5],&quot; &quot;[!UICONTROL RampID]、」および「[!UICONTROL Unified ID2.0].」と入力します。 選択した地理的ターゲットによって、使用可能なサブオプションが決まります。

         両方の「」を選択できます[!UICONTROL Legacy IDs]「」と「」に対して検査する値[!UICONTROL Universal ID]ただし、各プレースメントで選択できるユニバーサル ID のタイプは 1 つだけです。 レガシー ID とユニバーサル ID の両方を選択する場合、入札の環境設定がユニバーサル ID に指定されます。

      1. （必要な場合）ユニバーサル ID を使用するためのサービス利用契約に同意します。

         データを新しい ID タイプに変換する前に、DSP アカウントのユーザーがサービス利用規約に同意する必要があります。 条件は、ID タイプごとに、アカウントごとに 1 回だけ受け入れられます。

参照先」[プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md).」と入力します。

## テストとデータ検証のベストプラクティス

次のベストプラクティスを使用： [!DNL RampID]Adobe Analyticsが使用できる、ベースのセグメントと ID5 ベースのセグメント。

* セグメントをアクティブ化してから約 24 時間後に、内のセグメントの変換済み ID 数を確認します [!UICONTROL Audiences] > [!UICONTROL All Audiences]. ID 数が予期しない場合は、Adobeアカウントチームにお問い合わせください。

  参照先」[メール ID とユニバーサル ID のデータの相違](#universal-ids-data-variances)セグメント数の変化の詳細については、「」を参照してください。

* 既存のパッケージやプレースメントを変更しないでください。 ただし、ユニバーサル ID をテストするための増分予算がない場合は、元の予算を減らしてテストに資金を供給します。

* 元のパッケージとプレースメントをコピーし、テストのサイズに基づいて予算を調整し、使用するオーディエンスを変更する [!DNL RampID]ベースのセグメント（認証済みユーザーの場合）または ID5 ベースのセグメント（未認証ユーザーの場合）を使用し、新しいパッケージとプレースメントが予算の全額を費やしていることを確認します。

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

ハッシュ化されたメールアドレスのユニバーサル ID への翻訳率は、90% を超える必要があります。この翻訳率は [!DNL RampIDs] ハッシュ化されたメールアドレスがすべて一意の場合、特に 95% である必要があります。 例えば、ハッシュ化されたメールアドレスが 100 個ある場合は、少なくとも 95 個に翻訳する必要があります [!DNL RampIDs] または、90 を超えるその他のタイプのユニバーサル ID。 翻訳率が低い場合は、問題がある可能性があります。 参照先」[差異の原因]（可能な説明については、「#universal-ids-data-variances-causes」を参照してください。

の場合 [!DNL RampIDs]の翻訳率が 70% を下回る場合は、Adobeアカウントチームに連絡して詳細な調査を依頼してください。

### 差異の原因 {#universal-ids-data-variances-causes}

* ハッシュ化されたメール ID を ID5 ID に変換する：

  確率的モデルの誤差分散は+/- 5% です。 つまり、オーディエンス数を 5% 過大評価または過小評価する可能性があります。

* に変換されたハッシュ化されたメール ID [!DNL RampIDs]:

   * 複数のプロファイルが同じメール ID を使用する場合、DSP セグメント数は、カスタマーデータプラットフォーム内のプロファイル数よりも少ない可能性があります。 例えば、Adobe Photoshopでは、1 つのメール ID を使用して会社アカウントと個人アカウントを作成できます。 ただし、両方のプロファイルが同じ人物に属する場合、プロファイルは 1 つのメール ID に、対応して 1 つのメール ID にマッピングされます [!DNL RampID].

   * A [!DNL RampID] 新しい値にアップグレードできます。 次の場合 [!DNL LiveRamp] メール ID を認識しないか、既存の ID にマッピングできません [!DNL RampID] データベース内で、新しい [!DNL RampID] をメール ID に送信します。 今後、メール ID を別の ID にマッピングできる場合 [!DNL RampID] または、同じメール ID に関する詳細情報を収集でき、をアップグレードします [!DNL RampID] を新しい値に変更します。 [!DNL LiveRamp] では、このアクションを「派生」からのアップグレードと見なします [!DNL RampID] 「維持」される [!DNL RampID]. ただし、DSPは、派生とメンテナンス間のマッピングを取得しません [!DNL RampIDs] したがって、DSP セグメントから以前のバージョンの RampID を削除することはできません。 この場合、セグメント数はプロファイル数より多くなる可能性があります。

     例：ユーザーがにログインした [!DNL Adobe] Photoshopページの web サイトおよび訪問数。 次の場合 [!DNL LiveRamp] メール ID に関する既存の情報がないので、派生したを割り当てます [!DNL RampID]例えば、D123 と答えてください。 15 日後、ユーザーは同じページにアクセスしますが、 [!DNL LiveRamp] は、をアップグレードしました [!DNL RampID] この 15 日間にを再割り当てしました [!DNL RampID] を M123 に変更します。 顧客データプラットフォームの「Photoshop愛好者」のセグメントには、ユーザーのメール ID が 1 つしかありませんが、DSP セグメントには D123 と M123 の 2 つの RampID があります。

## トラブルシューティング

ユーザー数が表示されない場合や、オーディエンスサイズが小さい場合は、次の点を確認してください。

* を使用する場合 [!DNL Flashtalking] または [!DNL Google Campaign Manager 360] 広告する場合は、広告のクリックスルー URL に正しいマクロが追加されていることを確認します。 のマクロを参照してください [[!DNL Flashtalking] 広告](/help/integrations/analytics/macros-flashtalking.md) および [[!DNL Google Campaign Manager 360] 広告](/help/integrations/analytics/macros-google-campaign-manager.md).

* オンサイトのイベントと広告漏洩を照合するために、正しいユニバーサル ID パートナー固有のコードが Web サイトに実装されていることを確認します。 の操作 [!DNL LiveRamp] または [!DNL ID5] 必要に応じて担当者に依頼します。

* （用 [!DNL RampIDs] および [!DNL UID 2.0] ID）を使用している [DSP データソースが正しく設定されている](/help/dsp/audiences/sources/source-manage.md#source-settings)、およびそのユーザー数が、生成されたオーディエンスセグメントに対して入力されます。

* リーチが予想を下回る場合は、オーディエンスセグメントロジックが精度が高すぎないことを確認します。

* キャンペーン、パッケージ、プレースメントの設定が正しいことを確認します。<!-- wording-->

問題が解決しない場合は、Adobeアカウントチームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID オーディエンスを有効化](/help/dsp/audiences/sources/source-manage.md)
>* [カスタムセグメントの作成と実装](/help/dsp/audiences/custom-segment-create.md)
>* [認証済みセグメントの手動インポート： [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [Audience Management について](/help/dsp/audiences/audience-about.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
