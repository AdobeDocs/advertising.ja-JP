---
title: Advertising DSPのオーディエンス管理について
description: オーディエンス管理機能の詳細。
feature: DSP Audiences, DSP Segments
exl-id: 44cfe67e-e495-447f-b08f-d3789bd4dd09
TQID: https://experienceleague.adobe.com/IocF0s67I-vJAUx9Eom-aWEf-Q6H-ZOjczyGr0f9PsA
product_v2:
  - id: a829a185-511f-4bf8-8dcf-9e684f8011cf
feature_v2:
  - id: ee30758d-9ffe-4cd7-8f26-0d4394f041f6
subfeature_v2:
  - id: c193c532-b70e-4556-bde7-857186cbe140
  - id: fef5c122-6482-4d17-a8ce-4e70b906f1f4
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
topic_v2:
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 477ab8f27ad0873b8cd919085cb2dba0db58924d
workflow-type: tm+mt
source-wordcount: 1457
ht-degree: 0%

---

# Advertising DSPのオーディエンス管理について

DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理でき、プレースメントのターゲットとして使用できます。

* DSPセグメントを作成して実装することで、独自の1st パーティオーディエンスデータを収集できます。 後で、セグメント内のユーザーを広告でリターゲティングしたり、セグメント内のユーザーが広告を受信するのを防ぐことができます。 セグメントには、次のタイプを作成できます。

   * [&#x200B; カスタムセグメント &#x200B;](/help/dsp/audiences/custom-segment-create.md)を使用して、a） デスクトップおよびモバイルデバイスの広告に表示されたユーザー、およびb）特定のweb ページにアクセスしたユーザーを追跡できます。 トラッキングタグは、Cookie ベースのユーザーまたはID5のユニバーサル IDに関連付けられたユーザーのいずれかを追跡できます。

   * カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイト上の消費者の販売拒否リクエストからユーザーIDを追跡する[CCPA販売拒否セグメント &#x200B;](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。 オプトアウト要求からユーザーIDの月次レポートを取得できます。

     CCPAのオプトアウト要求に対するAdobe Advertising サポートの詳細については、[Adobe AdvertisingのCalifornia Consumer Privacy Act: Consumer opt-out of sale サポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)を参照してください。

* [&#x200B; クッキーレスターゲティング用のユニバーサル IDを取得して使用](/help/dsp/audiences/universal-ids.md):

   * 認証済み[!DNL LiveRamp] [!DNL RampID] セグメントを手動でDSPに直接送信します。

   * DSPでCDPからファーストパーティセグメントをインポートし、サポートされているユニバーサル ID タイプに変換できます。

   * [!DNL AdFixus]個のユニバーサル IDを含むファーストパーティ [!DNL AdFixus] セグメントを読み込みます（オーストラリアのみ）。 その後、プレースメントを[!DNL AdFixus]IDにターゲット化し、これらのセグメントを[再利用可能なオーディエンス &#x200B;](/help/dsp/audiences/reusable-audience-create.md)に追加し、「[1st パーティセグメントを [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)からインポート」で説明されているレポートを使用できます。

   * 追加の手順を実行することなく、プレースメントターゲットにユニバーサル IDを含むサードパーティセグメントを含めます。

* [再利用可能なオーディエンス &#x200B;](/help/dsp/audiences/reusable-audience-create.md)のオーディエンスライブラリを作成します。 保存されたオーディエンスは、利用可能なあらゆるオーディエンスセグメントと、保存されたその他のオーディエンスで構成されます。 保存したオーディエンスに加えた変更は、オーディエンスをターゲットまたは除外するすべてのプレースメントと、保存したオーディエンスを含むその他すべてのオーディエンスに自動的に適用されます。

  保存されたオーディエンスを使用して複数のセグメントを含めたり除外したりすることで、メディアプランナーは必要に応じてオーディエンスをグループ化できます。 オーディエンスを構築すると、各セグメントの（ターゲティング可能な）サイズとアクティブなオーディエンスサイズ全体が表示されます。 キャンペーン管理者は、各プレースメントにオーディエンスターゲットを手動で設定するのではなく、プレースメントのターゲットとして保存された1つ以上のオーディエンスを選択するだけです。

プレースメントのターゲティングには、追加のオーディエンスタイプも使用できます。

## ファーストパーティデータとサードパーティデータのセグメントのインポート

DSPのユーザーインターフェイスやカスタムインポートサービスを使用して、ファーストパーティデータとサードパーティデータのセグメントをDSPにインポートする方法は、数多くあります。

* DSPは、Adobe Audience Managerおよびその他の[!DNL Adobe]人のオーディエンスをターゲティング用に取り込むことができます。 前提条件と手順については、「[広告ターゲティング用にAdobe Audience Manager セグメントを読み込む](/help/integrations/audience-manager/import-audiences.md)」を参照してください。

* DSPは、[&#x200B; ソース機能](/help/dsp/audiences/sources/source-about.md)を使用して、サポートされている顧客データプラットフォームの1st パーティデータセグメントを、ユニバーサル IDを持つセグメントに変換できます。

* オーストラリアの広告主は、[!DNL AdFixus]のユニバーサル IDを他のID タイプに変換することなく、[&#x200B; ソース機能](/help/dsp/audiences/sources/source-about.md)を使用して[!DNL AdFixus]のファーストパーティセグメントを読み込むことができます。

* DSPは[!DNL LiveRamp]の宛先プラットフォームなので、認証済み [!DNL LiveRamp] [!DNL RampID] セグメントを[手動でDSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)に直接送信できます。

* DSPでは、他のファーストパーティデータセグメントをData Management Platform （DMP）から直接インポートし、必要に応じて任意の広告主に提供できます。

* DSPでは、サードパーティセグメントの複雑な組み合わせなど、カスタムのサードパーティセグメントを読み込むことができます。 必要に応じて、任意の広告主にセグメントを提供できます。

詳しくは、Adobe アカウントチームにお問い合わせください。

## プレースメントターゲットとして使用できるオーディエンス

プレースメントは、次のすべてのタイプのオーディエンスにターゲット設定できます。

* DSPに保存されたすべてのユーザー作成オーディエンスセット。

* DSPで作成されたすべてのユーザー作成オーディエンスセグメント：

   * 特定のweb ページを訪問したユーザーや、特定の広告のインプレッションに接触したユーザー向けのカスタムセグメント。

     ユニバーサル IDに配信されたインプレッションに対して、料金は発生しません。

   * カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイトで販売拒否リクエストを送信したユーザーを対象とした、CCPA販売拒否オーディエンスセグメント。

* ユニバーサル IDに変換されたセグメントや、インポートした[!DNL AdFixus] ユニバーサル IDを含むセグメントなど、インポートしたファーストパーティデータセグメントのすべてを含みます。

  ユニバーサル IDに配信されたインプレッションには、追加料金が発生します。 料金については、「[&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)」を参照してください。

* インポートしたカスタムのサードパーティデータセグメントはすべて。

* （米国のみを対象としたプレースメント） [DSPのお客様は、[!DNL eXelate]、（[!DNL Eyeota]）、（[!DNL LiveRamp]）、[!DNL Lotame]、[!DNL TransUnion]など、30 プロバイダー](/help/dsp/audiences/third-party-data-providers.md)を超えるすべてのサードパーティデータセグメントを利用できます。

  オーディエンスデータ（特定のデモグラフィック、興味や意図、行動プロファイルなどを持つ利用者など）にもとづいて、利用者をターゲティングする特定のセグメントを作成できます。 データプロバイダーとカテゴリー別に参照したり、名前またはセグメント ID別にセグメントを検索したり、データプロバイダー、アクティブなセグメントサイズ、web ブラウザー数、デバイス数で結果をフィルタリングしたりできます。

  サードパーティセグメントには追加料金が発生し、各セグメント名の横に表示されます。

* （Adobe Experience Platformおよび[!DNL Real-Time CDP]、Adobe Audience Manager、またはAdobe Analyticsを使用し、Adobe Advertising JavaScript コンバージョンタグのみを使用する広告主）すべての利用可能なファーストパーティ、セカンドパーティ、またはサードパーティのオーディエンスセグメントが[!DNL Real-Time CDP]で作成され、Audience Managerで作成され、Audience Managerまたは[!DNL Analytics]からAdobe CX Enterpriseに公開されます。

  セグメントの利用価格は事前に交渉されており、DSPには表示されません。

  [!DNL Analytics]のセグメントは、CX Enterprise オーディエンスとして作成または公開してから約1時間後に利用できます。 Audience Managerまたは[!DNL Real-Time CDP]から直接取得したセグメントは、共有してから24時間以内に利用できます。

  >[!NOTE]
  >
  >これらのソリューションのセグメントの設定と収集について詳しくは、[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html)、[the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html)のドキュメントを参照してください。

## オーディエンスサイズデータ

オーディエンス/すべてのオーディエンスおよびプレースメント設定の「オーディエンスのターゲット設定」セクションでは、特定のデバイスタイプまたはユニバーサル ID タイプに対する個別の範囲を含む、サイズ範囲で各セグメントリストをフィルタリングできます。

![&#x200B; オーディエンスサイズでフィルター](/help/dsp/assets/audience-size-filter.png)

また、次の詳細なオーディエンスサイズデータも確認できます。

* 選択したすべてのセグメントおよび保存されたオーディエンスのアクティブな重複排除オーディエンスサイズが表示され、デバイスタイプ（ブラウザー、モバイル、またはコネクテッド TV）別の詳細を表示できます。

  ![組み合わせたオーディエンスサイズ &#x200B;](/help/dsp/assets/audience-size.png)

* 個々のセグメントの場合、アクティブなオーディエンスサイズとCPM（該当する場合）がセグメント名の横に表示されます。

  ![個々のセグメントサイズ &#x200B;](/help/dsp/assets/audience-size-segment.png)

* ブラウザー別、モバイル別、コネクテッド TV別、ユニバーサル ID タイプパートナー別など、個々のセグメントや保存されたオーディエンスに関する詳細を表示できます。 保存されたオーディエンスの場合、アクティブなオーディエンスの合計サイズは重複排除された合計になります。

  ![個々のセグメントまたは保存されたオーディエンスの詳細](/help/dsp/assets/audience-size-segment-details.png)

## [!UICONTROL Audiences] ビュー

### [!UICONTROL All Audiences] ビュー

[!UICONTROL All Audiences] ビューまたはオーディエンスライブラリで、オーディエンスセグメントのグループやその他の保存されたオーディエンスを含む、再利用可能なオーディエンスを保存および管理できます。 複数のプレースメントのターゲットとしてオーディエンスを使用できます。 各オーディエンスを使用するプレースメントの数は、プレースメント名の横に示されます。

任意のオーディエンスを編集、複製、削除、書き出し、共有できます。

### [!UICONTROL Segments] ビュー

[!UICONTROL Segments] ビューでは、すべてのユーザーが追加のカスタムセグメントを作成できます。

[!UICONTROL Segments] ビューには、次のセグメントタイプも一覧表示されます。

* ユーザーが作成したすべてのカスタムセグメント。

  作成したカスタムセグメントのトラッキングタグを表示し、他のユーザーとセグメントを共有できます。 作成したカスタムセグメントは、編集または削除することもできます。

  他のユーザーが共有したカスタムセグメントは、編集または共有できません。

* ユーザーが使用できる、そのまま読み込まれたすべての1st パーティセグメント。

  共有された1st パーティセグメントは、編集または共有できません。 1st パーティセグメントをほかのユーザーと共有する必要がある場合は、Adobeアカウントチームにお問い合わせください。

* ユーザーが使用できるすべてのカスタムサードパーティセグメント。

  共有されたサードパーティセグメントは、編集または共有できません。 サードパーティセグメントをほかのユーザーと共有する必要がある場合は、Adobe アカウントチームにお問い合わせください。

### [!UICONTROL Sources] ビュー

[!UICONTROL Sources] ビューでは、指定したユニバーサル ID タイプを含むセグメントに変換するサポート対象の顧客データプラットフォームのファーストパーティセグメントのソースを設定できます。 [!DNL AdFixus]個のユニバーサル IDを持つセグメントをインポートするように[!UICONTROL AdFixus ID]個のソースを設定することもできます（オーストラリアのみ）。 ソース設定には、CDPまたは[!DNL AdFixus] チームと共有するための自動生成ソースキーが含まれています。

サポートされているプラットフォーム、サポートされているユニバーサル ID タイプ、設定ワークフローについて詳しくは、「[&#x200B; ファーストパーティオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)」を参照してください。

[!UICONTROL Sources]を通じて読み込まれたセグメントは、再利用可能なオーディエンスと、該当する場合はプレースメント設定で[!UICONTROL Universal ID]のターゲティングに使用できます。

>[!MORELIKETHIS]
>
>* [&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [再利用可能なオーディエンスを作成](reusable-audience-create.md)
>* [&#x200B; カスタムセグメントを作成して実装](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](/help/dsp/audiences/sources/source-manage.md)
>* [認証済みセグメントを [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)から手動でインポートします
>* [1st パーティセグメントを [!DNL AdFixus]](/help/dsp/audiences/sources/source-adfixus.md)からインポート
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
