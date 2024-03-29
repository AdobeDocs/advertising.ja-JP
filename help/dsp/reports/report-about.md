---
title: カスタムレポートについて
description: カスタムレポートを手動で作成するか、事前設定済みのレポートテンプレートを使用するかのオプションについて説明します。
feature: DSP Custom Reports
exl-id: 321062f3-754b-4379-9587-003862c4221b
source-git-commit: 1ac58da2d538cc682161ebc944a0412ad4a8af17
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 0%

---

# カスタムレポートについて

カスタムレポートでは、キャンペーンディメンション（広告主、プレースメント、サイト、地域など）と最も重要な指標を使用して、レポートデータのコンテンツと配信をカスタマイズできます。 次のいずれかを実行できます。

* 詳細なレベルで、キャンペーンパフォーマンスレポートを完全に設定します。
* 事前設定済みのレポートテンプレートから選択し、必要に応じてそれらをカスタマイズします。

1 回だけレポートを生成することも、指定したタイムゾーンの日別、週別、月別の 03:00 にレポートを生成するようにスケジュールすることもできます。 レポートが生成されると、指定した電子メールの受信者またはリンク先に配信されます [レポートの宛先](/help/dsp/reports/report-destinations/report-destination-about.md) 次のタイプの

* [!DNL Amazon Simple Storage Service] ([!DNL S3])
* FTP
* SFTP
* FTP SSL（ベータ版）

>[!NOTE]
>
>また、キャンペーン（キャンペーン、パッケージ、配置、広告）のすべてのレベルでオンデマンドデータを表示することもできます [関連するキャンペーン管理ビュー内](/help/dsp/campaign-management/reports/campaign-reports-about.md).

## 使用可能なレポートタイプ

* **[!UICONTROL Custom]:** このレポートは、ほとんどのディメンションと指標を使用して独自のカスタムレポートを作成するのに使用できる空白のテンプレートです。 [!UICONTROL Conversion], [!UICONTROL Device], [!UICONTROL Geo]、および [!UICONTROL Site] レポートは、このテンプレートのバリエーションで、それぞれの使用例に対して事前に選択された列とディメンションがあります。

* 事前設定済みレポートテンプレート

   * **[!UICONTROL Billing]:** このレポートを使用して、キャンペーンごとのメディア請求の支出指標など、主要な請求指標を把握します。

     >[!NOTE]
     >
     >このレポートには、請求セグメントに関するデータが含まれます。 ユーザーまたはデバイスに複数のセグメントに属するインプレッションが提供された場合、インプレッションに対してクレジットが付与されるのは 1 つの請求可能なセグメントのみです。

   * **[!UICONTROL Conversion]:** このレポートを使用して、Adobe Advertisingコンバージョントラッキングを使用してキャプチャされたコンバージョン指標に基づくキャンペーンのパフォーマンスを把握します。 このレポートには、マルチタッチ属性が含まれます。

   * **[!UICONTROL Device]:** この事前入力済みテンプレートを使用して、デバイス関連のディメンション別の主要指標を表示します。

   * **[!UICONTROL Frequency (by Impression)]:** このレポートを使用して、個別視聴者に表示されるインプレッション数の分布（1 つのインプレッションを表示した個別視聴者数、2 つのインプレッション、3 つのインプレッションなど）を把握します。 データは、プレースメントまたはキャンペーンで使用できます。

     >[!NOTE]
     >
     >* データは 2019 年 3 月 2 日以降に使用可能になります。
     >* データのサンプリングに基づいて周波数を推定する。
     >* 一部のインベントリでは、パブリッシャーはデバイス識別子を渡さないので、頻度の追跡ができません。 このレポートには、デバイス識別子が使用可能だったインプレッションのみが含まれます。

   * **[!UICONTROL Frequency (by App/Site)]:** このレポートを使用して、アプリまたはサイトでユニークユーザーにリーチした数を把握します。 また、特定のアプリまたはサイト（「ユニークユーザー」）を介してのみ到達したユニークユーザーの数を確認することもできます。

     >[!NOTE]
     >
     >* データは 2018 年 11 月 16 日以降に利用可能になります。
     >* 一部のプライベートインベントリでは、パブリッシャーはデバイス識別子を渡さないので、頻度の追跡ができません。

   * **[!UICONTROL Geo]**：この事前入力済みテンプレートを使用して、地理的ディメンション別に主要指標を表示します。

   * **[!UICONTROL Margin]:** このレポートを使用して、キャンペーン別またはプレースメント別の利益、利益、その他の支出指標などの主要指標を確認します。

   * **[!UICONTROL Segment]:** この事前設定済みのテンプレートを使用して、セグメント別の主要指標を表示します。

     >[!NOTE]
     >
     >* このレポートは、様々なターゲットセグメントのパフォーマンスを示すためのものです。 セグメントメンバーシップデータを使用します。 2 つ以上のターゲットセグメントに属する個人またはデバイスにインプレッションが提供された場合、このレポートには各セグメントに対して 1 つの行が含まれます。 このため、このレポートの合計は、実際の配信と一致しない場合があります。
     >* セグメントのコンバージョン指標およびカスタム目標データは、2019 年 8 月 3 日以降で利用できるようになります。 セグメントのその他すべてのデータは、2018 年 6 月 1 日以降に利用可能になります。

   * **[!UICONTROL Site]:** デフォルトでは、には標準指標、メディアの総支出およびサイト別の合計請求可能な純支出が含まれます。

   * **[!UICONTROL Household Reach & Frequency]:** このレポートを使用して、デバイスや cookie レベルではなく、IP アドレスに基づいた世帯レベルで、様々な広告フォーマットの単一のディメンションのインプレッション数、リーチおよび頻度を表示します。 インサイトを活用して、メディアミックスを最適化し、パフォーマンスを向上させ、リーチを増やす機会を特定します。 参照：[世帯レポートに関する FAQ](/help/dsp/reports/faq-household-report.md)」を参照してください。

   * **[!UICONTROL Household Conversions]:** このレポートを使用して、デバイス/cookie レベルではなく、IP アドレスに基づく世帯レベルでビュースルーコンバージョンを確認します。 インサイトを使用して、キャンペーンのパフォーマンスを測定および最適化します。 参照：[世帯レポートに関する FAQ](/help/dsp/reports/faq-household-report.md)」を参照してください。

## クロスアカウントレポート {#cross-account-reporting}

複数のDSPアカウントを持つ組織では、組織のニーズに応じて、オプションでカスタムレポートでクロスアカウントデータを有効にすることができます。 例えば、アカウント A にアカウント B のデータへのアクセス権を付与し、アカウント B にアカウント C のデータ（アカウント A のデータではなく）へのアクセス権を付与することができます。 この機能を有効にして設定するには、担当のAdobeアカウントチームにお問い合わせください。

この機能を組織で有効にした後、次の操作を実行できます。 [フィルター](report-settings.md) アカウント別に、次のいずれかのレポートタイプを選択します。  [!UICONTROL Custom], [!UICONTROL Site], [!UICONTROL Segment], [!UICONTROL Geo], [!UICONTROL Device], [!UICONTROL Frequency (by Impression)]、および [!UICONTROL Conversion].

アカウント設定： [!UICONTROL Settings] > [!UICONTROL Account] a) 自分のアカウントでデータを利用できる他のアカウントと、b) 自分のアカウントのデータにアクセスできる他のアカウントを示します。

>[!MORELIKETHIS]
>
>* [カスタムレポートの作成](/help/dsp/reports/report-create.md)
>* [カスタムレポート設定](/help/dsp/reports/report-settings.md)
>* [世帯レポートに関する FAQ](/help/dsp/reports/faq-household-report.md)
>* [Campaign Managementビューでのパフォーマンスレポートのタイプ](/help/dsp/campaign-management/reports/campaign-reports-about.md)
>* [使用可能なレポート列](/help/dsp/reports/report-columns.md)
>* [について [!UICONTROL Report Destinations]](/help/dsp/reports/report-destinations/report-destination-about.md)
