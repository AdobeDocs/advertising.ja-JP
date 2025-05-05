---
title: Advertising DSPの Audience Management について
description: Audience Management の機能について説明します。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
source-git-commit: 31f20bcfb79265326f515218a02d8a4fa3efd586
workflow-type: tm+mt
source-wordcount: '1324'
ht-degree: 0%

---

# Advertising DSPの Audience Management について

DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理できます。これらをプレースメントのターゲットとして使用できます。

* DSP セグメントを作成して実装することで、独自のファーストパーティオーディエンスデータを収集します。 後から、セグメント内のユーザーを広告で再ターゲットしたり、セグメント内のユーザーが広告を受け取らないようにしたりできます。 次のタイプのセグメントを作成できます。

   * [ カスタムセグメント ](/help/dsp/audiences/custom-segment-create.md)a）デスクトップおよびモバイルデバイスから広告にさらされるユーザーと b）特定の web ページを訪問するユーザーを追跡します。 トラッキングタグは、cookie ベースのユーザー、または ID5 のユニバーサル ID に関連付けられたユーザーを追跡できます。

   * [CCPA の販売オプトアウトセグメント ](/help/dsp/audiences/ccpa-opt-out-segment-create.md)：カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイト上の消費者の販売オプトアウトリクエストからユーザー ID を追跡します。 販売のオプトアウトリクエストから、ユーザー ID の月間レポートを取得できます。

     CCPA のAdobe Advertisingオプトアウト要求の販売サポートの詳細については、[California Consumer Privacy Act: Consumer Opt-out Support のAdobe Advertisingサポート ](/help/privacy/ccpa/ccpa-opt-out-of-sale.md) を参照してください。

* （Beta機能） [ クッキーレスターゲティング用のユニバーサル ID の取得と使用 ](/help/dsp/audiences/universal-ids.md):

   * 認証済みの [!DNL LiveRamp] [!DNL RampID] セグメントをDSPに手動で直接送信します。

   * DSPがファーストパーティセグメントをカスタマーデータプラットフォームから読み込んで、サポートされているユニバーサル ID タイプに変換できるようにします。

   * 追加手順を必要とせずに、プレースメントターゲットにユニバーサル ID を含むサードパーティセグメントを含めます。

* [ 再利用可能なオーディエンス ](/help/dsp/audiences/reusable-audience-create.md) のオーディエンスライブラリを作成します。 保存されたオーディエンスは、使用可能なオーディエンスセグメントおよび他の保存されたオーディエンスで構成されます。 保存したオーディエンスに加えた変更は、オーディエンスをターゲットまたは除外するすべてのプレースメントと、保存したオーディエンスを含むその他のすべてのオーディエンスに自動的に適用されます。

  保存されたオーディエンスを使用すると、メディアプランナーは必要に応じてオーディエンスをグループ化できます。そのためには、複雑なブール論理を使用して複数のセグメントを含めたり除外したりします。 オーディエンスを作成すると、個々のセグメントのサイズと合計オーディエンスサイズが示されます。 Campaign の実行者は、各プレースメントに対してオーディエンスターゲットを手動で設定するのではなく、プレースメントターゲットとして 1 つ以上の保存済みオーディエンスを選択するだけで済みます。

追加のオーディエンスタイプも、プレースメントのターゲティングに使用できます。

## ファーストパーティおよびサードパーティのデータセグメントの読み込み

DSP ユーザーインターフェイスを使用したり、カスタムインポートサービスを通じてファーストパーティおよびサードパーティのデータセグメントをDSPに読み込んだりするには、多くのオプションがあります。

* DSPは、ターゲティングのためにAdobe Audience Managerやその他の [!DNL Adobe] オーディエンスを取り込むことができます。 前提条件と手順については、「[ 広告ターゲティング用のAdobe Audience Manager セグメントの読み込み ](/help/integrations/audience-manager/import-audiences.md) を参照してください。

* DSPでは、[ ソース機能 ](/help/dsp/audiences/sources/source-about.md) を使用して、サポートされている顧客データプラットフォームからユニバーサル ID を持つセグメントに、ファーストパーティデータセグメントを変換できます。 また、[ 認証済みのセグメントを手動で  [!DNL LiveRamp] [!DNL RampID]DSPに直接送信 ](/help/dsp/audiences/sources/source-import-liveramp-segments.md) することもできます。

* DSPは、他のファーストパーティデータセグメントを Data Management Platform （DMP）から直接読み込み、必要に応じて任意のセットの広告主に提供できます。

* DSPでは、サードパーティセグメントの複雑な組み合わせなど、カスタムのサードパーティセグメントを読み込むことができます。 必要に応じて、任意のセットの広告主にセグメントを提供できます。

詳しくは、Adobeアカウントチームにお問い合わせください。

## プレースメントのターゲットとして使用できるオーディエンス

プレースメントのターゲットは、次のタイプのオーディエンスのすべてに設定できます。

* DSPに保存されたすべてのユーザー作成オーディエンスセット。

* DSPで作成されたすべてのユーザー作成オーディエンスセグメント：

   * 特定の web ページを訪問したユーザーと、特定の広告のインプレッションを受けたユーザーのカスタムセグメント。

     ユニバーサル ID に配信されるインプレッションには料金は発生しません。

   * カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイトで販売オプトアウトリクエストを送信したユーザーの CCPA 販売オプトアウトオーディエンスセグメント。

* ユニバーサル ID に翻訳されたセグメントを含む、読み込まれたすべてのファーストパーティデータセグメント。

  ユニバーサル ID に配信されたインプレッションには追加料金が発生します。 料率については、「[ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)」を参照してください。

* 読み込まれたすべてのカスタムのサードパーティデータセグメント。

* （米国のみを対象としたプレースメント） [30 を超えるプロバイダーのDSPのお客様が利用できるすべてのサードパーティデータセグメント ](/help/dsp/audiences/third-party-data-providers.md) [!DNL eXelate]、（[!DNL Eyeota]）、（[!DNL LiveRamp]）、[!DNL Lotame]、[!DNL Neustar] など、多数。

  特定のセグメントをターゲット設定できます。このセグメントは、オーディエンスデータに基づいてユーザーをターゲット設定します（例えば、特定の人口統計、興味や意図、行動プロファイルを持つユーザー）。 データプロバイダーとカテゴリで参照したり、名前またはセグメント ID でセグメントを検索したり、データプロバイダー、合計セグメントサイズ、web ブラウザー数、デバイス数で結果をフィルタリングしたりできます。

  サードパーティセグメントには追加料金が発生し、各セグメント名の横に示されています。

* （Adobe AdvertisingのAdobe Experience Platform コンバージョンタグのみを使用する、JavaScript and [!DNL Real-Time CDP]、Adobe Audience ManagerまたはAdobe Analyticsを使用する広告主） [!DNL Real-Time CDP] で作成された、Audience Managerで作成された、またはAudience Managerまたは [!DNL Analytics] からAdobe Experience Cloudに公開された、使用可能なファーストパーティ、セカンドパーティまたはサードパーティオーディエンスセグメントすべて。

  セグメントを使用するための価格は事前に交渉されており、DSPには表示されません。

  [!DNL Analytics] のセグメントは、Experience Cloudオーディエンスとして作成または公開してから約 1 時間後に使用できるようになります。 Audience Managerまたは [!DNL Real-Time CDP] から直接取得したセグメントは、共有後 24 時間以内に使用可能になります。

  >[!NOTE]
  >
  >これらのソリューションでセグメントのデータを設定および収集する方法について詳しくは、[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html) および [the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html) のドキュメントを参照してください。

## オーディエンスサイズデータ

オーディエンス /すべてのオーディエンス、およびプレースメント設定のオーディエンスターゲティング セクションでは、サイズ範囲（特定のデバイスタイプまたはユニバーサル ID タイプの合計範囲と別々の範囲を含む）で各セグメントリストをフィルタリングできます。

![ オーディエンスサイズでフィルタリング ](/help/dsp/assets/audience-size-filter.png)

また、詳細なオーディエンスサイズデータも確認できます。

* 選択したすべてのセグメントと保存されたオーディエンスにわたる、重複排除されたアクティブな合計オーディエンスサイズが表示され、デバイスタイプ（ブラウザー、モバイルまたは接続されたテレビ）別に詳細を表示できます。

  ![ 組み合わせたオーディエンスサイズ ](/help/dsp/assets/audience-size.png)

* 個々のセグメントの場合、合計オーディエンスサイズと CPM （該当する場合）がセグメント名の横に表示されます。

  ![ 個々のセグメントサイズ ](/help/dsp/assets/audience-size-segment.png)

* ブラウザー、モバイル、接続されたテレビ、ユニバーサル ID タイプのパートナー別のサイズなど、個々のセグメントまたは保存されたオーディエンスに関する詳細を表示できます。 保存されたオーディエンスの場合、合計サイズは重複排除された合計です。

  ![ 個々のセグメントまたは保存したオーディエンスの詳細 ](/help/dsp/assets/audience-size-segment-details.png)

## オーディエンスビュー

### すべてのオーディエンス ビュー

オーディエンスライブラリと呼ばれる [!UICONTROL All Audiences] ビューでは、再利用可能なオーディエンス（オーディエンスセグメントのグループや他の保存済みオーディエンスも含む）を保存および管理できます。 オーディエンスは、複数のプレースメントのターゲットとして使用できます。 各オーディエンスが使用されるプレースメントの数は、プレースメント名の横に表示されます。

任意のオーディエンスを編集、クローン、削除、書き出し、共有できます。

### セグメントビュー

[!UICONTROL Segments] ビューでは、すべてのユーザーが追加のカスタムセグメントを作成できます。

[!UICONTROL Segments] 表示には、次のセグメントタイプも表示されます。

* ユーザーが使用できるすべてのユーザー作成カスタムセグメント。

  作成した任意のカスタムセグメントのトラッキングタグを表示し、それらのセグメントを他のユーザーと共有できます。 また、作成したカスタムセグメントを編集または削除することもできます。

  他のユーザーが共有しているカスタムセグメントを編集または共有することはできません。

* そのまま読み込まれたファーストパーティセグメントは、すべてユーザーが使用できます。

  自分と共有されたファーストパーティセグメントを編集または共有することはできません。 ファーストパーティセグメントを他のユーザーと共有する必要がある場合は、Adobeアカウントチームにお問い合わせください。

* ユーザーが使用できるすべてのカスタムサードパーティセグメント。

  自分と共有されていたサードパーティセグメントを編集または共有することはできません。 他のユーザーとサードパーティのセグメントを共有する必要がある場合は、Adobeアカウントチームにお問い合わせください。

### ソースビュー

[!UICONTROL Sources] ビューでは、サポートされている顧客データプラットフォーム内のファーストパーティセグメントのソースを設定し、指定したユニバーサル ID タイプを含むセグメントに変換できます。 ソース設定には、自動生成されたソースキーが含まれ、接続を確立するために顧客データプラットフォームに提供されます。

サポートされる顧客データ・プラットフォーム、サポートされるユニバーサル ID タイプおよび各顧客データ・プラットフォームへの接続を設定するワークフローの詳細は、「[ ソースについて ](/help/dsp/audiences/sources/source-about.md) を参照してください。

翻訳されたセグメントは、再利用可能なオーディエンスや、クッキーのないターゲティングのためのプレースメント設定に含めることができます。

>[!MORELIKETHIS]
>
>* [ ユニバーサル ID のアクティブ化のサポート ](/help/dsp/audiences/universal-ids.md)
>* [ 再利用可能なオーディエンスを作成 ](reusable-audience-create.md)
>* [ カスタムセグメントの作成と実装 ](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントの作成と実装 ](ccpa-opt-out-segment-create.md)
>* [ ファーストパーティオーディエンスソースについて ](/help/dsp/audiences/sources/source-about.md)
>* [ ユニバーサル ID オーディエンスをアクティブ化するためのオーディエンスソースの管理 ](/help/dsp/audiences/sources/source-manage.md)
>* [ 認証済みセグメントの手動インポート  [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [ 利用可能なサードパーティデータプロバイダー ](third-party-data-providers.md)
>* [ プレースメント設定 ](/help/dsp/campaign-management/placements/placement-settings.md)
