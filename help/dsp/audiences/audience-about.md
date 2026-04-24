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
source-git-commit: c4d69b3aac9c963d13e3083f71931e507e58e616
workflow-type: tm+mt
source-wordcount: 1394
ht-degree: 0%

---

# Advertising DSPのオーディエンス管理について

DSPでは、オーディエンスセグメントとオーディエンスセットを作成および管理でき、プレースメントのターゲットとして使用できます。

* DSPセグメントを作成して実装することで、独自の1st パーティオーディエンスデータを収集できます。 後で、セグメント内のユーザーを広告でリターゲティングしたり、セグメント内のユーザーが広告を受信するのを防ぐことができます。 セグメントには、次のタイプを作成できます。

   * [&#x200B; カスタムセグメント &#x200B;](/help/dsp/audiences/custom-segment-create.md)を使用して、a） デスクトップおよびモバイルデバイスの広告に表示されたユーザー、およびb）特定のweb ページにアクセスしたユーザーを追跡できます。 トラッキングタグは、Cookie ベースのユーザーまたはID5のユニバーサル IDに関連付けられたユーザーのいずれかを追跡できます。

   * カリフォルニア州消費者プライバシー法（CCPA）に従って、web サイト上の消費者の販売拒否リクエストからユーザーIDを追跡する[CCPA販売拒否セグメント &#x200B;](/help/dsp/audiences/ccpa-opt-out-segment-create.md)。 オプトアウト要求からユーザーIDの月次レポートを取得できます。

     CCPAのオプトアウト要求に対するAdobe Advertising サポートの詳細については、[Adobe AdvertisingのCalifornia Consumer Privacy Act: Consumer opt-out of sale サポート &#x200B;](/help/privacy/ccpa/ccpa-opt-out-of-sale.md)を参照してください。

* （Beta機能） [&#x200B; クッキーレスターゲティング用のユニバーサル IDを取得して使用](/help/dsp/audiences/universal-ids.md):

   * 認証済み[!DNL LiveRamp] [!DNL RampID] セグメントを手動でDSPに直接送信します。

   * DSPでCDPからファーストパーティセグメントをインポートし、サポートされているユニバーサル ID タイプに変換できます。

   * 追加の手順を実行することなく、プレースメントターゲットにユニバーサル IDを含むサードパーティセグメントを含めます。

* [再利用可能なオーディエンス &#x200B;](/help/dsp/audiences/reusable-audience-create.md)のオーディエンスライブラリを作成します。 保存されたオーディエンスは、利用可能なあらゆるオーディエンスセグメントと、保存されたその他のオーディエンスで構成されます。 保存したオーディエンスに加えた変更は、オーディエンスをターゲットまたは除外するすべてのプレースメントと、保存したオーディエンスを含むその他すべてのオーディエンスに自動的に適用されます。

  保存されたオーディエンスを使用して複数のセグメントを含めたり除外したりすることで、メディアプランナーは必要に応じてオーディエンスをグループ化できます。 オーディエンスを構築すると、各セグメントの（ターゲティング可能な）サイズとアクティブなオーディエンスサイズ全体が表示されます。 キャンペーン管理者は、各プレースメントにオーディエンスターゲットを手動で設定するのではなく、プレースメントのターゲットとして保存された1つ以上のオーディエンスを選択するだけです。

プレースメントのターゲティングには、追加のオーディエンスタイプも使用できます。

## ファーストパーティデータとサードパーティデータのセグメントのインポート

DSPのユーザーインターフェイスやカスタムインポートサービスを使用して、ファーストパーティデータとサードパーティデータのセグメントをDSPにインポートする方法は、数多くあります。

* DSPは、Adobe Audience Managerおよびその他の[!DNL Adobe]人のオーディエンスをターゲティング用に取り込むことができます。 前提条件と手順については、「[広告ターゲティング用にAdobe Audience Manager セグメントを読み込む](/help/integrations/audience-manager/import-audiences.md)」を参照してください。

* DSPは、[&#x200B; ソース機能](/help/dsp/audiences/sources/source-about.md)を使用して、サポートされている顧客データプラットフォームの1st パーティデータセグメントを、ユニバーサル IDを持つセグメントに変換できます。 また、認証済み [!DNL LiveRamp] [!DNL RampID] セグメントを[手動でDSP](/help/dsp/audiences/sources/source-import-liveramp-segments.md)に直接送信することもできます。

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

* ユニバーサル IDに変換されたセグメントを含む、インポートした1st パーティデータセグメントのすべてを取得できます。

  ユニバーサル IDに配信されたインプレッションには、追加料金が発生します。 料金については、「[&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)」を参照してください。

* インポートしたカスタムのサードパーティデータセグメントはすべて。

* （米国のみを対象としたプレースメント） [DSPのお客様は、[!DNL eXelate]、（[!DNL Eyeota]）、（[!DNL LiveRamp]）、[!DNL Lotame]、[!DNL Neustar]など、30 プロバイダー](/help/dsp/audiences/third-party-data-providers.md)を超えるすべてのサードパーティデータセグメントを利用できます。

  オーディエンスデータ（特定のデモグラフィック、興味や意図、行動プロファイルなどを持つ利用者など）にもとづいて、利用者をターゲティングする特定のセグメントを作成できます。 データプロバイダーとカテゴリー別に参照したり、名前またはセグメント ID別にセグメントを検索したり、データプロバイダー、アクティブなセグメントサイズ、web ブラウザー数、デバイス数で結果をフィルタリングしたりできます。

  サードパーティセグメントには追加料金が発生し、各セグメント名の横に表示されます。

* （Adobe Experience Platformおよび[!DNL Real-Time CDP]、Adobe Audience Manager、またはAdobe Analyticsを使用する広告主で、Adobe Advertising JavaScript コンバージョンタグのみを使用する場合）すべての利用可能なファーストパーティ、セカンドパーティ、またはサードパーティのオーディエンスセグメントが[!DNL Real-Time CDP]で作成され、Audience Managerで作成され、Audience Managerまたは[!DNL Analytics]からAdobe CX Enterpriseに公開されます。

  セグメントの利用価格は事前に交渉されており、DSPには表示されません。

  [!DNL Analytics]のセグメントは、作成またはCX Enterprise オーディエンスとして公開してから約1時間後に利用できます。 Audience Managerまたは[!DNL Real-Time CDP]から直接取得したセグメントは、共有してから24時間以内に利用できます。

  >[!NOTE]
  >
  >これらのソリューションのセグメントの設定と収集について詳しくは、[Audience Manager](https://experienceleague.adobe.com/docs/audience-manager/user-guide/aam-home.html?lang=ja)、[Analytics](https://experienceleague.adobe.com/docs/analytics.html?lang=ja)、[the [!DNL Real-Time CDP]](https://experienceleague.adobe.com/docs/experience-platform/rtcdp/segmentation/segment-builder-guide.html?lang=ja)のドキュメントを参照してください。

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

The [!UICONTROL Segments] view also lists the following segment types:

* All user-created custom segments available to the user.

  You can view tracking tags for any of the custom segments you created, and share those segments with other users. You can also edit or delete the custom segments you created.

  You can&#39;t edit or share custom segments that other users have shared with you.

* All first-party segments imported as-is that are available to the user.

  You can&#39;t edit or share first-party segments that were shared with you. Contact your Adobe Account Team if you need to share first-party segments with additional users.

* All custom third-party segments available to the user.

  You can&#39;t edit or share third-party segments that were shared with you. Contact your Adobe Account Team if you need to share third-party segments with additional users.

### [!UICONTROL Sources] ビュー

In the [!UICONTROL Sources] view, you can configure sources for first-party segments in supported customer data platforms that you want to convert to segments containing specified universal ID types. The source settings include an auto-generated source key, which you&#39;ll provide to your customer data platform to establish the connection.

For more information about the supported customer data platforms, supported universal ID types, and the workflows to set up connections to each customer data platform, see &quot;[About first-party audience sources](/help/dsp/audiences/sources/source-about.md).&quot;

The translated segments are available to include in reusable audiences and in placement settings for cookieless targeting.

>[!MORELIKETHIS]
>
>* [&#x200B; ユニバーサル IDのアクティブ化のサポート &#x200B;](/help/dsp/audiences/universal-ids.md)
>* [Create a reusable audience](reusable-audience-create.md)
>* [&#x200B; カスタムセグメントを作成して実装](custom-segment-create.md)
>* [[!UICONTROL CCPA Opt-Out-of-Sale] セグメントを作成して実装](ccpa-opt-out-segment-create.md)
>* [&#x200B; ファーストパーティのオーディエンスソースについて](/help/dsp/audiences/sources/source-about.md)
>* [&#x200B; オーディエンスソースを管理してユニバーサル ID オーディエンスをアクティブ化](/help/dsp/audiences/sources/source-manage.md)
>* [Manually import authenticated segments from [!DNL LiveRamp]](/help/dsp/audiences/sources/source-import-liveramp-segments.md)
>* [使用可能なサードパーティのデータプロバイダー](third-party-data-providers.md)
>* [配置の設定](/help/dsp/campaign-management/placements/placement-settings.md)
