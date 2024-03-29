---
title: 検索、ソーシャル、コマースのトラッキングについて
description: 検索、ソーシャル、コマースのトラッキングオプションについて説明します。
exl-id: 0a26f67c-8b3b-4fa1-ac24-a8461624cfc5
feature: Search Tracking
source-git-commit: 052574217d7ddafb8895c74094da5997b5ff83db
workflow-type: tm+mt
source-wordcount: '767'
ht-degree: 0%

---

# 検索、ソーシャル、コマースのトラッキングについて

広告のパフォーマンスを追跡するには、広告のインプレッション、クリック、コスト、コンバージョン（トランザクション）の各データが必要です。 検索、ソーシャル、コマースは、このデータを使用して、広告ポートフォリオの最適化に必要なデータ予測モデルを作成します。

## コスト、クリック、インプレッションのデータ

検索、Social、および Commerce は、インプレッション、クリック、コストのデータを [サポートされる広告ネットワーク](/help/search-social-commerce/introduction/supported-inventory.md) 毎日。 また、Search、Social、&amp;Commerce では、トラッキングテンプレートと宛先 URL に一意のクリック追跡コード（トラッキングサーバーへのリダイレクトを含む）を追加して、表示/コンテンツのインプレッション数、クリック数およびコストを追跡し、後でイベントをコンバージョンに結び付けます。

検索、ソーシャル、コマースでデータが同期されない広告ネットワーク上のキャンペーンを追跡する場合は、インプレッション、クリック、コストのデータを含む日別フィードファイルを送信して、キャンペーンのデータを提供する必要があります。

### クリック追跡タグ

Search、Social、&amp;Commerce の導入チームが、同期した広告キャンペーンの広告、キーワード、プレースメント、製品グループ、サイトリンク拡張のトラッキングテンプレートと宛先 URL を更新して、一意のトラッキング ID 文字列とAdobe Advertisingリダイレクトを含め、クリック追跡を設定します。 また、のランドページのサフィックス（最終 URL のサフィックス）にトラッキングを追加します。 [!DNL Google Ads] および [!DNL Microsoft Advertising] アカウントとキャンペーン。

トラッキングパラメーターを使用すると、Adobe Advertisingは個々のキーワードレベル（検索キャンペーン）または広告バリエーションレベル（コンテンツまたはサイトのターゲット設定を含む検索キャンペーン、表示キャンペーン、ソーシャルキャンペーン）でクリックを追跡できます。 Adobe Advertisingがディスプレイ/コンテンツ広告を表示したり、いずれかの広告をクリックしたりするたびに、広告ネットワークは、キーワードまたは広告に関連付けられたクリック追跡タグを使用して、イベントを広告ピクセルサーバーに送信します。 クリックの場合：

* 並列追跡をサポートするブラウザー上のGoogle Ads とMicrosoft Advertising 広告の場合、広告ネットワークは最初に Web サイトにクリックを送信し、次にAdobe Advertisingピクセルサーバーに送信します。その後、ユーザーのコンピューターに cookie が存在しない場合は、そのコンピューターに配置します。

* その他すべての場合、広告ネットワークは、クリックをAdobe Advertisingピクセルサーバーに直接送信します。 ピクセルサーバーは、Cookie をユーザーのコンピューターに配置し（まだ存在しない場合）、Web サイト上の関連 URL にユーザーをリダイレクトします。 エンドユーザーの全体的なエクスペリエンスは、リダイレクトがない場合と同じです。

Cookie は、 [!DNL Adobe] ドメイン (`everesttech.net`) をファーストパーティ Cookie として設定する必要があります。 リダイレクト後、ユーザーは広告主のドメインに属し、その Cookie はサードパーティ Cookie として扱われます。 Adobe Advertisingcookie について詳しくは、[Adobe Advertisingcookie](https://experienceleague.adobe.com/docs/core-services/interface/ec-cookies/cookies-advertising-cloud.html).&quot;

## コンバージョンデータ

顧客が広告をクリックしたり、ディスプレイ広告またはソーシャル広告を表示した場合、検索、ソーシャル、コマースでは、結果として得られた各コンバージョンを、元のクリックまたは表示/ソーシャルインプレッションにマッピングする必要があります。

広告主は、すべてのクリック数およびディスプレイ/ソーシャルインプレッション数のコンバージョンデータを提供する際に役立ちます。 コンバージョンデータには、Web サイトで発生し、入札の最適化に使用できるあらゆるタイプのイベントに関する情報を含めることができます。 コンバージョンデータを提供するには、広告主のコンバージョンページ（顧客がトランザクションを完了した後に表示される「成功」ページなど）にコンバージョントラッキングコードを実装するか、別の方法で取り込んだコンバージョンデータを日別フィードファイルに送信します。

### コンバージョントラッキングタグ

以下を使用できます。 [様々なベンダーのコンバージョンタグ](/help/search-social-commerce/tracking/conversion-tracking-about.md).

Adobe Advertisingコンバージョンタグを使用し、Adobe Advertisingがトランザクションを成功させ、「成功」ページに到達すると、ユーザーピクセルサーバーは、クリックのリダイレクト時に設定された、ユーザーのコンピューター上に Cookie が存在するかどうかを確認します。 cookie が見つかると、トランザクションイベントに関する情報が ef_transid パラメーターを使用して渡され、トランザクションがコンバージョンと認識され、前の広告クリックまたは表示インプレッションに与えられます。

Adobe Advertisingが複数の広告をクリックした場合、特に指定しない限り、ユーザーは最終的な広告クリックまたは（ディスプレイまたはビデオキャンペーンの）最終的な広告インプレッションにトランザクションをクレジットします。 お使いの [ルックバックウィンドウをクリック](/help/search-social-commerce/glossary.md#c-d) および [インプレッションのルックバックウィンドウ](/help/search-social-commerce/glossary.md#i-j) 有料クリックまたはディスプレイ/ビデオインプレッション（それぞれ）が発生してからの日数を判断し、その中でイベントがコンバージョンに関連付けられるかどうかを判断します。

Adobe Advertising導入チームは広告主と協力して、広告主が実装する必要のあるコンバージョンタグの形式を決定し、各コンバージョンタグを挿入する Web ページを特定してから、実装するコンバージョンタグを提供します。
