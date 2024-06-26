---
title: クロスデバイスソリューション
description: クロスデバイス機能の詳細を説明します。
feature: DSP Introduction
exl-id: d21917ef-5cac-46f8-8222-099667797683
source-git-commit: e517dd5f5fa283ff8a2f57728612937148889732
workflow-type: tm+mt
source-wordcount: '1000'
ht-degree: 0%

---

# クロスデバイスソリューション

と Advertising DSPの統合 [!DNL LiveRamp] では、ブランドが追跡したデバイスだけでなく、その人の既知のすべてのデバイスにオーディエンスを拡張できます。 また、この統合により、すべてのデバイスでフリークエンシーキャップとアトリビューションの測定も可能になります。

サポートされているユーザーベースのデバイスグラフを使用すると、次のことができます。

* デバイスではなく、人物や世帯に広告を配信するために、チャネルやデバイスをまたいでオーディエンスを一致させます。
* 個々のユーザーの把握とキャッピング頻度の把握により、広告への露出のバランスを取ります。
* チャネルやデバイスをまたいでオーディエンスを公開またはコンバージョンするテスト戦略。

## の利点 [!DNL LiveRamp] デバイスグラフ

* オフライン顧客データを含む決定論的なデータプールを提供

* cookie ID とモバイルデバイス ID を均等にカバーします

* 米国のデータを主に含む

* フリークエンシーキャップおよびアトリビューション測定に無料

* 拡張インプレッション数（を使用してのみ配信されるインプレッション数）の場合、価格は午後 0.35 CPM （ [!DNL LiveRamp] ターゲットオーディエンスセグメント内のデバイスではなく、デバイスグラフ）

  料金はアカウントの料金カードに反映されます。

## People-Based Frequency Management

人物ベースの頻度管理を使用すると、デバイスレベルではなく人物レベルでフリークエンシーキャップを指定して、真のメディア露出制御を行うことができます。

### People-Based Frequency Management の有効化

* **キャンペーン：** 新しいキャンペーンを作成する際に、 [!UICONTROL Cross-Device Level] の設定値。 「」を有効にする[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]デバイスグラフを選択します。 指定されたデバイスグラフは、プレースメント レベルでのクロスデバイスターゲティングと、キャンペーン、パッケージ、プレースメントの各レベルでの人物ベースの頻度管理の両方に使用されます。 フリークエンシーキャップは、人の既知のすべてのデバイスに適用されます。

詳しくは、を参照してください [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

キャンペーンを保存すると、そのキャンペーンを変更できなくなります [!UICONTROL Cross Device Level] の設定値。

* **パッケージ：**  オプションで、パッケージレベルで追加のフリークエンシーキャップを設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

* **プレースメント :** オプションで、プレースメントレベルに追加のフリークエンシーキャップを設定できます。 DSPは、キャンペーン階層内で最も厳格なフリークエンシーキャップに従います。

## 人物ベースのターゲティング

人物ベースのターゲティングを使用すると、デスクトップとモバイルをまたいで顧客を見つけることができます。

### 人物ベースのターゲティングの有効化

* **キャンペーン：** 新しいキャンペーンを作成する際に、 [!UICONTROL Cross-Device Level] の設定値。 「」を有効にする[!UICONTROL Same Device]&quot; -> &quot;[!UICONTROL People]デバイスグラフを選択します。 指定したデバイスグラフは、配置レベルでのクロスデバイスターゲティングと、人物ベースの頻度管理の両方に使用されます。

詳しくは、を参照してください [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md).

* **プレースメント :** 指定したデバイスグラフを使用して、キャンペーン内のプレースメントに対してオーディエンスターゲットを選択する場合、 [!UICONTROL Cross-Device Targeting] オプションを使用すると、指定したセグメントに含まれていないデバイスも含め、個人の既知のすべてのデバイス（キャンペーン設定で指定したデバイスグラフごと）にターゲティングを拡張できます。

### 人物ベースのターゲティングのレポートの設定

カスタムレポートには、次の指標を含めることができます。

* **拡張インプレッション：** （ [!UICONTROL Build Your Report] の下のセクション [!UICONTROL Metrics] > [!UICONTROL Std. Metrics]）デバイスグラフを活用することで配信された（元のオーディエンスセグメントには見つからない）増分インプレッション数。 この指標は、サードパーティのデバイスグラフの使用に関連する適用料金の計算にも使用されます。

  ある期間の拡張インプレッションのコストを判断するには、以下を含むカスタムレポートを実行します [!UICONTROL Extended Impressions] 列を展開し、拡張インプレッションの合計数に 0.00035 ドル （1,000 インプレッション数は 0.35 ドル）を掛けます。

  集計されたコストは、次の項目にも含まれます [!UICONTROL Billable Other Net Spend] 列（下 [!UICONTROL Metrics] > [!UICONTROL Spend]）ただし、その指標には、追加した他のキャンペーン料金も含まれる場合があります。

* **デバイスグラフ：** （ [!UICONTROL Build Your Report] の下のセクション [!UICONTROL Dimensions] > [!UICONTROL Campaign]）特定のキャンペーン、パッケージまたはプレースメントに対して選択したデバイスグラフ。

## 人物ベースのアトリビューション測定

*Adobe Advertisingコンバージョントラッキングのみを使用する広告主*

人物ベースのアトリビューションを使用すると、メディア漏洩が発生したデバイスとは別のデバイスで発生したコンバージョンを関連付けることができます。 人物ベースのアトリビューション測定は、DSP全体で使用できます。 [!DNL Adobe Advertising Creative]、および [!DNL Adobe Advertising Search, Social, & Commerce] サイトにAdobe Advertisingコンバージョンピクセルを実装している広告主の場合。

### 人物ベースのアトリビューション測定の有効化

クロスデバイスアトリビューション測定をアクティブ化する場合は、Adobeアカウントチームにお問い合わせください。

### クロスデバイスコンバージョンアトリビューション用のコンバージョンレポートを設定します

#### コンバージョンレポート設定

デバイスグラフがアトリビューション測定に対して有効になっている場合、 [!UICONTROL Conversion] レポートに含まれる [!UICONTROL Cross-Device Breakout] の設定。各コンバージョン指標に最大 3 つの異なる列を含めることができます。これには、以下が含まれます。

* &lt;*変換*>[!UICONTROL (tp)]：コンバージョンの合計（ユーザーの合計）を含みます。これには、同じデバイスのコンバージョンとクロスデバイスのコンバージョンの両方が含まれます（該当する場合）。 レポートでは、「[!UICONTROL (tp)]」がコンバージョンパスのコンバージョン指標名、ルールタイプおよびコンバージョンタイプに追加されます（例：「Responses （le）（tl）（tp））。

* &lt;*変換*>[!UICONTROL (sd)]:（任意）コンバージョンパスで追跡されたデバイスが 1 つのみのコンバージョンを含めます。 レポートでは、「[!UICONTROL (sd)]」がコンバージョンパスのコンバージョン指標名、ルールタイプおよびコンバージョンタイプに追加されます（例：「Responses （le）（tl）（sd））。

* &lt;*変換*>[!UICONTROL (xd)]:（任意）コンバージョンパスで複数のデバイスが追跡されたコンバージョンのみを含めます。 レポートでは、「[!UICONTROL (xd)]」がコンバージョンパスのコンバージョン指標名、ルールタイプおよびコンバージョンタイプに追加されます（例：「Responses （le）（tl）（xd）」）。

#### コンバージョンレポートの解釈方法

クロスデバイスの合計コンバージョンの割合を並べ替えます（[!UICONTROL (xd)]/[!UICONTROL (tl)]）から順に選択して、クロスデバイスの平均を上回るコンバージョンを引き起こしている原因を把握します。 これを使用して、メッセージやチャネルへの投資をユーザーの行動に一致させるために、クリエイティブ戦略やターゲティング戦略を通知できます。

* パッケージ – 合計コンバージョン数に最も貢献しているパッケージと、クロスデバイス変換の割合が高いパッケージを確認します。 これは、どこにお金を集中させるべきかを理解するのに役立ちます。

* プレースメント – プレースメントのパフォーマンスとアトリビューションを比較します（例えば、モバイル web 広告はデスクトップ上でコンバージョンを促進する可能性があります）。 アトリビューション用のデバイスグラフがないと、モバイル web プレースメントがデスクトップのコンバージョンに与える影響を見落とす場合や、大部分のユーザーがモバイル web ではなくデスクトップでコンバージョンを行った場合に、影響が埋め込まれる場合があります。

* 広告 – どの広告がより高いコンバージョンを促進するかを検出し、web ブラウザーとモバイルアプリ環境の両方でその価値と影響を定量化します。

* サイト – サイトを完全に手動で除外するのではなく、サイト全体で最適化します。 Web サイトでクロスデバイス変換が促進される場合は、この動作が発生するデバイスを確認できます。

* 契約 – どの在庫契約がクロスデバイスコンバージョンを提供するかを確認し、それらの契約により多くのデバイスとチャネルを含めるようにターゲティングを拡張する必要があるかどうかを決定することで、手動の最適化を改善します。

>[!MORELIKETHIS]
>
>* [レポート設定](/help/dsp/reports/report-settings.md)
>* [キャンペーン設定](/help/dsp/campaign-management/campaigns/campaign-settings.md)
>* [パッケージ設定](/help/dsp/campaign-management/packages/package-settings.md)
>* [プレースメント設定](/help/dsp/campaign-management/placements/placement-settings.md)
