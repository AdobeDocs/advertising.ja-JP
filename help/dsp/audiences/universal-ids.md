---
title: ユニバーサル ID をアクティベートするサポート
description: ユニバーサル ID セグメントのインポート、ユニバーサル ID を追跡するためのカスタムセグメントの作成、ファーストパーティセグメント内のその他の ユーザー ID のユニバーサル ID への Cookie レスターゲティングのユニバーサル ID への変換するのサポートについて説明します。
feature: DSP Audiences
exl-id: e238537b-217f-44bb-8a69-8adc83dbdfb9
source-git-commit: ea50b94ebc6d27fda9c0bd9f61da16750fa58f83
workflow-type: tm+mt
source-wordcount: '1403'
ht-degree: 0%

---

# ユニバーサル ID をアクティベートするサポート

<!-- Once we have CDP support for ID5 and can set up activation via sources, then maybe I can move this info into "About Sources" and "About Audiences." Or maybe make this the go-to page, removing info from those other pages? -->

*ベータ版機能*

DSPは、DSPでサポートされているデジタル形式全体で、Cookieのないシングルデバイス(クロスデバイスではない)ターゲティングのためのユーザーベースのユニバーサルIDをサポートしています。

* [!DNL LiveRamp] [!DNL Connect]ダッシュボードを使用して、認証済み [[!DNL LiveRamp] [!DNL RampIDs]] を手動で DSP に直接送信できます。「[認証済みセグメントの手動インポート元 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)」を参照してください。

* DSP、顧客データプラットフォーム(CDP)内で構築されたハッシュ化された電子メールIDで構成されるファーストパーティセグメントを取り込み、それらを [!DNL LiveRamp] [!DNL RampIDs] および [!DNL Unified ID 2.0 (UID2.0)] IDに変換するできます。 サポートされている顧客データプラットフォーム、サポートされている各ユニバーサルIDタイプで使用できる機能、および関連ワークフローについては、「[ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)」を参照してください。

* ID5 ユニバーサル ID に関連付けられた、デスクトップ やモバイルデバイスからの広告が表示され、特定のウェブページ訪問ユーザーをトラッキングするカスタム セグメントを作成できます。 ID5 は、確率モデルを使用して、さまざまなユーザーシグナルとブラウザーシグナルから派生した ID を割り当てます。 手順については、「特例文字 セグメント](/help/dsp/audiences/custom-segment-create.md)[作成と実装」を参照してください。

* 一部のベンダーのサードパーティセグメントには、CookieまたはデバイスIDで追跡されるユーザーに加えて、ユニバーサルIDが自動的に含まれる場合があります。 たとえば、 [!DNL Eyeota] のセグメントには ID5 ID が自動的に含まれ、 [!DNL Lotame] のセグメントには UID2.0 ID が含まれる場合があります。 セグメント詳細には、各タイプのサイズが含まれます。 セグメント名の横に記載されている各セグメントの通常の使用料金が適用されます。ID5 IDに追加料金はかかりません。

## ユニバーサル ID 書式 ＜例外＞Photoshop のみ「テキスト」によるレポート作成

* **特例文字 レポート:** ユニバーサル ID タイプ別のコスト、インプレッション、クリック、コンバージョン、頻度データをカスタム レポートで使用できます。

* **[!DNL Analytics]レポート:** 必要なすべての手順を実装した [[!DNL Adobe] [!DNL Analytics for Advertising]](/help/integrations/analytics/overview.md) を持つ広告主は、 [!DNL Analytics] でユニバーサル ID タイプ別に表示スルー コンバージョンを確認できます。

  >[!IMPORTANT]
  >
  >適切なコンバージョン 属性を得るには、広告のリンク先 URL に [EF ID と AMO ID](/help/integrations/analytics/ids.md) の両方を含めてください。

* **セグメント詳細:** すべてのセグメントタイプについて、セグメントの詳細には、ユニバーサル ID タイプ別のオーディエンスサイズと、Cookie または デバイス ID によって追跡されるデバイスの種類が含まれます。

## プレースメントでユニバーサル ID オーディエンスTarget方法

>[!NOTE]
>
>使用中の配置では、ターゲットとなる ID タイプを変更することはできません。 必要に応じて、ライブ配置重複し、新しい配置のターゲット ID タイプを変更できます。

新しい配置、スケジュールされたまたは一時停止したで、次の操作を行います。

1. [ [!UICONTROL Geo-Targeting] ] セクションで、ターゲットする地理的領域を指定します。 各ユニバーサル ID パートナーでは、特定の地域でのみユーザー ターゲティングが許可され、 [!UICONTROL Targeting] 設定では適格な ID タイプのみを使用できます。

1. [!UICONTROL Audience Targeting]セクションで、次の操作を行います。

   1. [!UICONTROL Included Audiences]設定で、ユーザーデータをユニバーサル ID に変換したセグメントを選択します。

      必要に応じて、追加のセグメントを含めることができます。

   1. [!UICONTROL Targeting]設定で、次の操作を行います。

      1. ターゲットユニバーサル ID タイプを選択します。

         この設定には、オプション「[!UICONTROL Legacy IDs]」と「[!UICONTROL Universal ID]」が含まれ、サブオプション「[!UICONTROL ID5]」、「[!UICONTROL RampID]」、および「[!UICONTROL Unified ID2.0]」が含まれる場合があります。 選択した地域ターゲットによって、使用可能なサブオプションが決まります。

         「[!UICONTROL Legacy IDs]」と「[!UICONTROL Universal ID]」の両方を選択できますが、1配置に選択できるユニバーサルIDは1種類のみです。 レガシー ID とユニバーサル ID の両方を選択すると、ユニバーサル ID が入札優先されます。

      1. (必要な場合)ユニバーサル ID の使用に関するサービス契約の条項承認。

         データを新しい ID タイプに変換するするには、DSP アカウント内のユーザーが利用規約に同意する必要があります。 条件への同意は、ID タイプごと、アカウントごとに 1 回だけ行う必要があります。

[配置設定](/help/dsp/campaign-management/placements/placement-settings.md)」を参照してください。

## テストとデータ検証のベストプラクティス

Adobe Analytics測定が可能な [!DNL RampID] ベースのセグメントと ID5 ベースのセグメントについては、以下のベストプラクティスを使用します。

* セグメントを有効にしてから約 24 時間後に、 [!UICONTROL Audiences] > [!UICONTROL All Audiences] 以内のセグメントのコンバージョン済み ID 数を確認します。 ID 数が予想されない場合は、Adobe Systems アカウントチームにお問い合わせください。

  セグメントカウントがどのように異なるかについては、「[電子メール ID とユニバーサル ID のデータ相違の原因](#universal-ids-data-variances)」を参照してください。

* 既存のパッケージとプレースメントは変更しないでください。 ただし、ユニバーサル ID テストための増分予算がない場合は、テストに資金を提供するために元の予算を減らします。

* 元のパッケージと配置コピー、テストのサイズに基づいて予算を調整し、 [!DNL RampID]ベースのセグメント(認証済みユーザーの場合)または ID5 ベースのセグメント(未認証ユーザーの場合)を使用するようにオーディエンスを変更し、新しいパッケージと配置が予算を全額消化していることを確認します。

   * ユニバーサル ID ベースのセグメントのパフォーマンスを、プレースメントターゲティング Cookie や モバイル広告 ID などの他のオーディエンス識別子のパフォーマンスと比較するには、ユニバーサル ID ベースの配置と従来の ID ベースの配置を個別に使用してキャンペーンを作成します。

     完全な再ターゲット化テストの場合は、認証されたユーザーの RampID と認証されていないユーザーの ID5 の両方ターゲット。

     最高のパフォーマンスを得ることは、主要な比較であってはなりません。 代わりに、どの ID が適切にスケーリングされているかを判断し、後で最適化と予算の割り当てに役立つ可能性があります。 長期的な目標は、Cookie が廃止されたときに失われたインプレッションとサイトトラフィックを補うことです。

   * ブラウザーリーチの合計を比較するには、ユニバーサル ID ベースのセグメントとレガシー ID ベースのセグメントを同じ配置内にターゲットします。 前のユースケースと同じキャンペーン設定を使用しますが、キャンペーン予算を分割する必要はありません。

     ユニバーサル ID には入札優先が与えられますが、ユニバーサル ID が利用できない場合、レガシー ID が入札を受け取ります。 異なるブラウザー(クロム、Safari、Mozilla など)でリーチを比較してください。

     >[!NOTE]
     >
     >頻度 制限は個人 ID に適用されます。 ユーザーに複数の ID タイプがある場合、予想以上にそのユーザーに達する可能性があります。

* 認証されたオーディエンスセグメントのリーチは、cookieベースのセグメントのリーチよりも当然小さく、追加のターゲティングオプションを使用するとリーチがさらに小さくなることに注意してください。 特に複数のターゲットを AND ステートメントで結合する場合は、詳細なターゲティングを使用する際に慎重に使用してください。

## 電子メール ID とユニバーサル ID でデータが異なる原因 {#universal-ids-data-variances}

* ID5 ID に変換されたハッシュ化された電子メール ID:

  確率モデルの誤差平方偏差は +/- 5% です。 これは、オーディエンス数を5%過大評価または過小評価する可能性があることを意味します。

* [!DNL RampIDs]に変換されるハッシュ化された電子メール ID:

   * 複数のプロファイルが同じメール ID を使用している場合、DSP セグメント数は顧客データプラットフォーム内のプロファイル数よりも少なくなる可能性があります。 例えば、Adobe Photoshop では、1 つの電子メール ID を使用して会社 アカウントと個人用アカウントを作成できます。 ただし、両方のプロファイルが同じユーザーに属している場合、プロファイルは 1 つの電子メール ID にマップされ、それに応じて 1 つの [!DNL RampID]にマップされます。

   * [!DNL RampID]は新しい値にアップグレードできます。[!DNL LiveRamp] が電子メール ID を認識できない場合、またはデータベース内の既存の[!DNL RampID]にマップできない場合は、電子メール ID に新しい[!DNL RampID]を割り当てます。将来、電子メール ID を別の [!DNL RampID] にマップしたり、同じ電子メール ID に関するより多くの情報を収集したりできる場合は、 [!DNL RampID] を新しい値にアップグレードします。 [!DNL LiveRamp] は、このアクションを「派生」 [!DNL RampID] から「維持された」 [!DNL RampID]へのアップグレードと呼んでいます。 ただし、DSP派生 [!DNL RampIDs] と維持の間のマッピングを取得しないため、以前のバージョンの RampID をDSP セグメントから削除することはできません。 この場合、セグメント数はプロファイル数より大きくなる可能性があります。

     例:ユーザー が [!DNL Adobe] Web サイトにログインし、Photoshop ページにアクセスします。 電子メール ID に関する既存の情報が [!DNL LiveRamp] ない場合は、派生 [!DNL RampID] (D123 など) を割り当てます。 15日後、ユーザーは同じページを訪問しますが、 [!DNL LiveRamp] はその15日間で [!DNL RampID] をアップグレードし、 [!DNL RampID] をM123に再割り当てしました。 顧客データプラットフォームのセグメント「Photoshop愛好家」にはユーザーの電子メール ID が 1 つしかありませんが、DSP セグメントには D123 と M123 の 2 つの RampID があります。

## トラブルシューティング

ユーザー数が表示されない場合、またはオーディエンスサイズが小さい場合は、以下を確認してください。

* [!DNL Flashtalking]広告や[!DNL Google Campaign Manager 360]広告を使用する場合は、広告のリンク先 URL に正しいマクロが追加されていることを確認してください。[[!DNL Flashtalking] 広告](/help/integrations/analytics/macros-flashtalking.md)および[[!DNL Google Campaign Manager 360] 広告](/help/integrations/analytics/macros-google-campaign-manager.md)のマクロを参照してください。

* オンサイト イベントや広告露出に合わせて、正しいユニバーサル ID パートナー固有のコードがウェブサイトに実装されていることを確認してください。 必要に応じて、 [!DNL LiveRamp] または [!DNL ID5] 担当者に相談してください。

* ( [!DNL RampIDs] ID および [!DNL UID 2.0] ID の場合) [DSP データソースが正しく設定され](/help/dsp/audiences/sources/source-manage.md#source-settings)生成された オーディエンス セグメントに対して ユーザー カウントが入力されていることを確認します。

* リーチが予想よりも少ない場合は、オーディエンスセグメントロジックが細かすぎないことを確認してください。

* キャンペーン、パッケージ、および配置の設定が正しいことを確認します。<!-- wording-->

問題を解決できない場合は、Adobe Systems アカウント チームにお問い合わせください。

>[!MORELIKETHIS]
>
>* [ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [オーディエンスソースを管理してユニバーサル ID Audiencesをアクティベート](/help/dsp/audiences/sources/source-manage.md)
>* [特例文字 セグメント作成と実装](/help/dsp/audiences/custom-segment-create.md)
>* [認証済みセグメントの手動インポート元 [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [オーディエンスマネジメントについて](/help/dsp/audiences/audience-about.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
